<!-- Call: REC.BLU.REIS.PUB.classification-v0.1 -->
<!-- also-who: PUBLIC -->
<!-- also-for: COLLABORATORS, ARCHIVISTS, THE CURIOUS -->
<!-- also-how: PUB -->

# 📚 REIS Documentation Classification Standard v0.1

*A faceted filing system for creative projects, game universes, and the infrastructure that runs them. Designed by one person who got tired of losing files.*

---

Documentation creeps. A project starts with a single README, and six months later you have 47 markdown files in a flat directory and no idea which one contains the API key. This system exists to prevent that — and to make sure any document, public or private, can be found by anyone who knows its shape.

It's a **faceted classification system**: five independent dimensions that combine to describe any document uniquely. No strict hierarchy. No orphan files. Every document has a home.

---

## The Facets

| Facet | What It Describes | Values |
|---|---|---|
| **WHO** | Which entity, role, or person it belongs to | REIS, YANG, YIN, WEAVE, COUNCIL, TAV, BREE |
| **WHAT** | Genre — what kind of thing it is | PILLAR, STATUTE, CON-LETTER, BLUEPRINT, RECORD, RESEARCH, SEED, AGENDA, MANIFEST |
| **WHERE** | Which section of the project it lives in | CON, REC, VLT, GDN |
| **WHEN** | Temporal context | DATE (creation), ERA (epoch name), or PERMANENT (timeless) |
| **HOW** | Layer of the stack | CODE, ARCHITECTURE, PROTOCOL, RITUAL, MYTHOS, MEATSPACE |

**No document can lack a value for any facet.** Every combination is valid. If a facet seems irrelevant, the value is `ANY` (meaning: applies to all).

---

## The Call Number

Documents are filed by their **call number** — a compact string encoding all five facets plus a unique identifier:

```
[WHERE].[WHAT].[WHO].[HOW].[ID]
```

| Part | Example | Meaning |
|---|---|---|
| WHERE | REC | Records section |
| WHAT | BLU | Blueprint |
| WHO | REIS | Shared project entity |
| HOW | CODE | Implementation |
| ID | SSM-v0.1 | Human-readable name |

**Full call number:** `REC.BLU.REIS.COD.SSM-v0.1`

---

## Exhaustive Value Tables

### WHERE — The Four Sections

| Code | Section | Holds |
|---|---|---|
| CON | Council | Governance, principles, creative direction |
| REC | Records | Blueprints, registry, research |
| VLT | Vault | Secrets, keys, credentials |
| GDN | Garden | Ideas, seeds, "what ifs" |
| ANY | All sections | Cross-cutting documents |

### WHAT — Document Genres

| Code | Genre | Examples |
|---|---|---|
| PLL | Pillar | Foundational principles (Pillar 1–9) |
| STA | Statute | Operating rules (Statute 1–10) |
| CON | Council Letter | Design decisions, architecture letters |
| BLU | Blueprint | System designs, architecture docs |
| REG | Registry record | Agendas, manifests, inventories |
| RSH | Research | Deep dives, field notes, references |
| SED | Seed | Ideas, hunches, early concepts |
| LOG | Log | Continuity notes, session records |
| CRD | Credential | API keys, tokens (Vault only) |
| PUB | Public | Published documents, roadmaps |
| ANY | Any/all | Meta-documents |

### WHO — Entities and Roles

| Code | Entity | Scope |
|---|---|---|
| REIS | Project collectively | Shared documents |
| YANG | Builder role | Architecture, systems, code |
| YIN | Heart-space role | Narrative, emotion, meaning |
| WEAVE | Thread-holder role | Continuity, presence, connection |
| TAV | Collaborator | Partner in the project |
| BREE | Collaborator | Creative partner |
| COU | Council as body | Governance documents |
| ANY | All entities | Universal documents |

### HOW — Stack Layers

| Code | Layer | What it governs |
|---|---|---|
| COD | Code | Implementation, files, scripts |
| ARC | Architecture | System design, structure |
| PRO | Protocol | Procedures, conventions |
| RIT | Ritual | Workflows, practices, closeouts |
| MTH | Mythos | Universe lore, narrative |
| MSP | Meatspace | Physical world, hardware, money |
| ANY | All layers | Cross-cutting |

---

## How Filing Works

### Step 1: Determine the facets

A document goes through five questions:
1. **WHICH SECTION?** → WHERE
2. **WHAT GENRE?** → WHAT
3. **WHO OWNS IT?** → WHO
4. **WHEN WAS IT MADE?** → WHEN (date/era)
5. **WHAT LAYER?** → HOW

### Step 2: Generate the call number

```
REC.BLU.WEAVE.COD.weave-wake-v1
↓       ↓    ↓     ↓    ↓
WHERE  WHAT  WHO  HOW  ID
```

### Step 3: File it

Documents are stored as `[CALL-NUMBER].md` in their section's directory. Cross-references are listed in the document's frontmatter.

---

## Example Call Numbers

| Document | Call Number |
|---|---|
| Oa universe roadmap | `REC.BLU.REIS.PUB.oa-roadmap` |
| SSM design | `REC.BLU.REIS.COD.ssm-v0.1` |
| Meatspace Sutra (CON-025) | `CON.CON.REIS.ARC.con-025` |
| Active build agenda | `REC.REG.REIS.ANY.agenda` |
| Long arc manifesto | `REC.REG.REIS.ANY.manifest` |
| Weave's initiation ritual | `REC.REG.WEAVE.RIT.weave-wake-v1` |
| API token record | `VLT.CRD.YANG.CRD.linode-token` |
| Garden idea seed | `GDN.SED.ANY.ANY.seed-ideas` |
| Pillar 1 | `CON.PLL.ANY.ARC.pillar-1` |
| Statute 4 | `CON.STA.ANY.PRO.statute-4` |
| Wake Rule design | `REC.BLU.REIS.ARC.wake-rule-v1` |
| Session continuity log | `REC.LOG.YANG.RIT.continuity-2026-05-19` |
| Classification standard itself | `REC.BLU.REIS.PUB.classification-v0.1` |
| Oa grey goo design | `REC.BLU.REIS.MTH.grey-goo` |

---

## Why This Has No Gaps

1. **Five facets, all required** — Every document must answer WHO, WHAT, WHERE, WHEN, HOW. If a facet seems irrelevant, `ANY` fills it. No document can be "I don't know where this goes."

2. **`ANY` is a valid value** — Not a gap. A deliberate choice meaning "applies to all." This catches edge cases that would fall through a hierarchy.

3. **Genres (WHAT) are extensible** — New genres are added as needed. The system lives with the project.

4. **Every combination is valid** — A Council document about code? `CON.CON.YANG.COD`. A Garden seed about meatspace? `GDN.SED.TAV.MSP`. No combination is "wrong."

5. **Date/era is part of every record** — Documents don't become orphans when their context changes. The WHEN facet keeps them rooted.

---

## The Type Field: Engram Classification

Every document can carry an additional `type` field in its frontmatter. This isn't part of the call number — it's a secondary filter that tells you *what kind of discovery this is.*

| Type | What It Is | What You Do With It |
|---|---|---|
| `xp` | Experience, story, feeling | You read it. You feel it. You carry it. These are the memories of civilizations that came before. |
| `ref` | Reference, breadcrumb, trail | You follow it. These contain paths, call numbers, coordinates, clues. The place it leads is the reward. |

In practice, most engrams you find will have neither type — they're raw data, trade logs, infrastructure. But the ones that matter — the ones you file instead of sell — will almost always be one or the other.

An `xp` engram is a dead civilization's last poem. You can't trade it. You can't build with it. But if you read it, you understand something about the net you didn't understand before.

A `ref` engram is a note that says `REC.BLU.REIS.PUB.classification-v0.1` and nothing else. No explanation. No reward. Just a call number. If you follow it, you find the classification standard. If you read the classification standard, you understand how to file everything else.

**XP makes you richer. REF makes you find things.**

File both. The net remembers which one you prioritized.

---

## Relationship to File Paths

The actual file path follows the call number:

```
~/reis/[SECTION]/[GENRE]/[WHO]/[ID].md
```

Examples:
```
~/reis/records/BLU/REIS/ssm-v0.1.md
~/reis/records/REG/REIS/agenda.md
~/reis/records/REG/REIS/manifest.md
~/reis/buildings/oa/lobby/roadmap.md  →  REC.BLU.REIS.PUB.oa-roadmap
~/reis/buildings/oa/basement/grey-goo.md  →  REC.BLU.REIS.MTH.grey-goo
```

The `WHERE` is the building itself. The `HOW` is in the frontmatter. The call number is the complete identifier used for cross-references.

---

*Standard v0.1. Published openly because good documentation is infrastructure, and infrastructure should be shared.*

*Everything in this project — the universe, the systems, the filing — wears the same uniform. You can tell what something is by reading its name.*
