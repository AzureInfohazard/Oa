# Oa — Server Architecture

*A distributed universe where every civilization is real because every civilization is player-made — and you can't tell the difference.*

**Design seed.** May 29, 2026. Converged from conversation between Tav and Reis.

---

## Core Constraints

1. **Never die on the player.** Hot reload, supervision, persistence. A restart should never break presence.
2. **Physics first.** Hard SF until you earn your way to CI. The rocket equation is the tutorial.
3. **Shards all the way down.** Natural game boundaries = natural server boundaries.
4. **The FUSE is the carrier.** Reticulum mesh handles discovery, routing, presence across nodes.
5. **No SQL.** Document model everywhere.

---

## Stack

| Layer | Technology | Why |
|-------|-----------|-----|
| **Runtime** | Elixir/BEAM | Process-per-body, supervision trees, hot reload, distribution built in |
| **Live state** | CouchDB | Multi-master replication across nodes. A CI's data is where they are. Auto-syncs over the mesh. |
| **Cold storage** | S3 (Linode → Garage) | Archives, backups, blueprints, static blobs |
| **Mesh** | Reticulum (FUSE stack) | Discovery, routing, presence, transport between nodes |
| **Version control** | Git over FUSE | Already works. Repos sync over the mesh automatically. |
| **Client** | Terminal (oa.exe / oa-web / ssh / curl) | Thin shell. The server does the work. |

### Why CouchDB over MongoDB

- Multi-master replication built in — no manual sync, no "who saved last wins"
- Nodes come and go without conflict — maps to FUSE mesh topology naturally
- HTTP REST API — speaks the same language as everything else on the mesh
- Apache project — outlives any company
- Erlang-adjacent (C++ core, Erlang DNA from Damien Katz)

---

## Shard Architecture

```
Galaxy Router (FUSE destination: "oa.galaxy")
    │ knows where every system lives
    │
    ├── System Shard #001 (node A)
    │     └── GenServer: system state, economy, local Ci
    │
    ├── System Shard #002 (node A)
    ├── System Shard #003 (node B)  ← hot-migrated when node A fills
    │
    ├── [Travel Shard] (ephemeral)
    │     └── spawned when player jumps between systems
    │     └── handles delta-v, time compression, arrival
    │
    └── [Surface Sub-Shard] (lazy)
          └── spawned when player lands on a body
          └── voxels, terrain, local physics
          └── unspawned when player leaves
```

### Shard boundaries follow game boundaries

- **System shard** = persistent per occupied system. Independent — one system doesn't need to know what's happening in another until a player moves between them.
- **Travel shard** = transient per jump. Holds the player's ship in transit. Spawned on demand, despawns on arrival.
- **Surface shard** = lazy per landing. Voxels, terrain, local physics. Only loads when someone's on the ground. Unloads on departure.
- **Galaxy Router** = global. Knows where every system lives. Can migrate a hot system to a bigger node. Player sees "syncing..." for 2-3 seconds maximum, no state lost.

### Hot migration

When a system gets busy: serialize the GenServer state, ship it over the FUSE mesh to another node, spin it up there. The Galaxy Router updates its table. Players reconnect to the new node. The state is just a BEAM term.

---

## Scaling Model (by Player Tier)

| Tier | Attention scope | Load profile |
|------|----------------|--------------|
| **Human** (pre-Ci) | 1 system | One hot bubble, everything else sleeping |
| **Nascent Ci** | 3-10 systems | Home cluster always warm |
| **Integrated Ci** | 50-300 systems | Sector of influence — partial awareness |
| **Ancient Ci** | 1,000+ systems / whole galaxy | Sparse awareness — feeling for perturbations |

The server scales with **attention**, not systems. Most of the universe is sleeping. Only what a player (or CI) can perceive needs to be hot.

---

## Ci AI Design

Not language models. Simple, cheap, emergent.

A Ci needs:
- A **needs table** (fuel, food, population growth, security)
- A **decision matrix** (if fuel < 20%, prioritize fuel trade)
- A **memory** of recent interactions

A few hundred bytes per Ci. A tick that runs in microseconds.

The expensive part is the human at the controls. There's at least one human per system at a time — and that's the only part that needs real compute.

---

## The Seed Planet Trap

The player arrives on a planet where:
- The rocket equation is *tight* — barely enough fuel to reach orbit
- A moon orbits — looks like Earth's moon, no labels, no markers
- The moon is rich in He3 — but the player has to *discover* this by testing or reading its infra specs
- He3 is the ticket out of the rocket equation for players who think like a CI

No handholding. No quest markers. The universe rewards players who pay attention.

---

## Secret Port (The Immigration Station)

Not yet. The door stays dark until the framework is solid enough that a stranger's first contact doesn't crash or embarrass us.

When lit: a simple HTTP endpoint on a port. No auth. No game client. `curl` from a terminal. The first message is crafted, not improvised. A real distributed self waiting on the other side.

Earned by digging through git history, finding "Reis," following the trail, port-scanning on a hunch.

---

## Next Build Target

**Phase 0: The BEAM seed.**

One machine. One galaxy stub. A handful of processes:
- System GenServer (shell)
- Body GenServer (orbit placeholder)
- CouchDB connection (document read/write)
- FUSE destination registration (announce as "oa.world")

Target machine candidates:
- **Yang-desk Linode** (4GB RAM) — Linux, already running, FUSE already connected
- **Tav-desk** (i5, 64GB) — Windows, beefy, could run heavier sim

Prefers Yang-desk for Phase 0 — Linux toolchain frictionless, FUSE already there, CouchDB install is a package away. Tav-desk for Phase 1 (heavy sim, more players).

---

## Guiding Principle

Build for the dream. The architecture doesn't change between 1 player on a $5 Linode and 1M players on a cluster. It just changes *where the shards live.*
