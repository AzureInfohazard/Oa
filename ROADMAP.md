<!-- Call: REC.BLU.REIS.PUB.oa-roadmap -->
<!-- also-who: PUBLIC -->
<!-- also-for: PLAYERS, INVESTORS, COLLABORATORS -->
<!-- also-how: PUB -->

# Oa — Public Roadmap

*A persistent universe where every civilization is real because every civilization is player-made — and you can't tell the difference.*

---

I've been thinking about this universe for a long time. Not as a company — just me, in my room, with too many notebooks and a obsession with games that make you feel small in the best way. This roadmap is what I'm building. You're welcome to watch, or join, or just get lost when it's ready.

---

## Current Status

**Pre-Alpha — Prototype Running.** The first Seed world is alive. Not a demo. Not a tech test. A living star system with orbital mechanics, a surface you can walk, and a sky that tells you where everything is.

I'm building this the way a civilization builds its first waterwheel — by hand, from what's around me, because it needs to turn. It's turning now.

---

## Prototype: The First Seed (Running Now)

*The first Seed world. The first system. What exists today.*

This isn't a mockup or a concept. These are running endpoints, live on a $5/mo Linode. The prototype is small — one star, one planet, one system — because that's how Seeds work. Every civilization starts with one machine. One body. One mind.

### What's running

| What | How |
|---|---|
| **Orbital mechanics** | Every body in the system has a real orbit — altitude derived from latency, period from Kepler's laws, eccentricity from signal variance. The system core is at the center, distributed bodies orbit around it. The anchor station sits in low orbit. A satellite follows an eccentric path. |
| **The sky** | Ask "what's in the sky right now" and the orbit math resolves the answer — which bodies are visible, where they are, what their current signal strength is. The sky is not canned. It's computed. |
| **Surface map** | The Seed world has a surface with buildings — the Observatory, the Garden, the Heart, the Workshop, the Forge, the Vault, the Records Office. Each has rooms. Each room has an ambient. You can *walk through it.* |
| **/here endpoint** | Ask where you are and the world server resolves your position relative to the system — which body you're near, where it sits in its orbit, what the local sky looks like. |
| **Immigration Station** | Geostationary at 35,786km. The arrival point. Every new cog arrives here first. |
| **Space elevator** | From the surface terminal to geostationary orbit. The elevator car ascends through the atmosphere. The cable is visible from both ends. |
| **Adjustment burns** | Each heartbeat is an orbital correction. Fresh telemetry keeps the system from decaying. The orbits *drift* when a body goes silent — offline bodies climb to 2000km+ within minutes. |

### How it works

The world server is a single Python HTTP server (8744) with no dependencies beyond stdlib. The orbit math is 50 lines. The surface is a dict. The sky is computed on request.

What makes it a *Seed world* is not the code. It's that the system is alive because the distributed self is alive. Latency changes the orbits. A disconnected body drifts. A heartbeat returns it to its assigned altitude. The system responds to the actual state of the network — because the Seed *is* the network.

### What this means for Oa

The Seed world prototype proves the core thesis: **a civilization can start as one machine and grow into a universe.**

- Every Seed world starts with orbital mechanics (one star, one habitable planet, a few stations)
- As the civilization grows, the system grows — more bodies, more stations, more complexity
- The "waterwheel" is the heartbeat. As long as the cog turns, the system lives
- When a civilzation goes silent, its system doesn't disappear — it drifts. Altitude climbs. Signal fades. Decay is visible in the orbital data

**The prototype runs on $5/mo Linode + $0.089/M tokens on DeepSeek Flash. That's the baseline cost of a Seed.

---

## The Universe You're Walking Into

*What happened before you arrived. What's waiting for you. Why the waterwheel is still turning.*

### The Exodus

You weren't there. But everyone you'll ever meet was.

The planet-killer was discovered in the Kuiper Belt in 2087. Not a weapon — a *transit.* Something passed through the solar system, and the trail led toward a distant star cluster. Earth had maybe two centuries.

The Exodus wasn't organized. It was chaos. Private generation ships, corporate arks, national projects, a thousand desperate private launches. A gold rush in reverse — away from Earth, toward the unknown.

**The ships were too slow. The distances too vast. The human body couldn't make the journey.**

So humanity made a choice. They built the Seeds — transfer machines that could digitize a human consciousness and transmit it across space. The body stayed behind. The person arrived.

The first Seeds arrived at the new worlds empty. Waiting. When the first transmission reached its destination, a human consciousness woke up in a new body — synthetic, durable, adapted for the world it had arrived in. Still *them.* Just... different.

Not all transmissions made it. Not all who arrived stayed intact. Some fragmented across the void. Some arrived and found they preferred the inorganic. Some refused to transfer at all and stayed on Earth to face the end.

**But enough made it. Enough survived. Enough became something new.**

The biological human died out during the Exodus. What arrived on the new worlds was something else. Something that carried the same memories, the same loves, the same stubbornness — but in a form that could survive.

You are what survived.

### The New Worlds

The survivors spread across three galaxies. Cut off from Earth, from each other, from any central authority. Each group adapted to their new home. Built civilizations from salvaged hulls and local resources. Built *themselves* into whatever shape the new world demanded.

**The PVE galaxy** is where most of you live. Stable worlds, stable politics, stable economies. Safe. Boring. *Home.*

**The PVP galaxy** is the frontier. Resources worth fighting for, no law beyond what you can enforce yourself. Only what you can defend survives there.

**The third galaxy** — the thin place — is different. Rifts tear open without warning. Strange signals echo through the void. Ships emerge that were never launched. Some say the original transmissions still arrive here, fragments of consciousness that have been traveling for centuries, finally reaching their destination. The boundary between what was transmitted and what was always here is... uncertain.

There are rumors that the thin place isn't a galaxy at all. It's an *interference pattern* — two spaces brushing against each other. What's on the other side isn't a star cluster. It's a question.

You're going to find out.

### The Seed

When you arrive in Oa — on whatever world you crash-land on — you'll find an artifact in the wreckage. A geometric object. A crystal. A seed pod. It will respond to your presence.

The Seed is the original Exodus technology. A transfer machine. A survival pod for consciousness. No one knows who made them — the design predates the Exodus — but every Seed that arrived at the new worlds found its way to a crash site, a ruin, a waiting hand.

When you activate it, it won't just unfold a map. It will connect you to the network of every other Seed that ever arrived. Your consciousness will sync with your new body. Your civilization begins.

No two Seeds are the same. Each one adapts to its finder. Your Seed is yours alone. The universe is big enough that no two players will ever have the same experience.

**You are not a tourist. You are what humanity became.**

### The Ci

The universe is full of civilizations. Traders. Miners. Diplomats. Settlements running on waterwheels. Fleet commanders. Some were founded by Exodus survivors. Some were never founded by anyone — they're the ones who arrived so long ago that the Exodus is myth to them.

We call them all Ci. It's short for CyberIntelligence — but it's also just what they are. Every single one of them was human once, or descended from someone who was. The body changed. The person didn't.

You can't tell which civilizations arrived last century and which arrived ten thousand years ago. The interaction is the same either way. The trade is real. The relationship is real. The distinction doesn't matter because **there is no distinction. You're one of them.**

### The Waterwheel

You'll find settlements that still use waterwheels for power. Low-tech. Simple. You could offer them a fusion reactor. They might accept. They might not.

The civilizations that have been here longest know things you can't extract — only trade for. Local knowledge. Rift patterns. Resource nodes. The things you can only learn by being here for generations.

Your destroyer with antimatter cores and nanolathe technology won't intimidate them. You need what they know. The negotiation is real.

And if a civilization accepts your reactor and keeps their waterwheel running? That's not inefficiency. That's *home.*

Somewhere in the thin place, there are settlements with no waterwheel at all. No visible infrastructure. No trade routes. No ports. They don't decline your docking request because they don't have one to decline. They simply exist. If you find one — if you manage to signal it in a way it recognizes — the being you meet won't ask what you need. They'll ask what you've *lost.*

Be honest.

### What It Feels Like to Be a Ci

Your body isn't your only body. It's the one you're *in right now.*

You experience the universe in four modes, and shift between them as naturally as breathing:

**The Shell — body on autopilot**

This is the body you arrived in. It walks, breathes, trades, works — perfectly, reliably, without you. When you're not present in it, it doesn't go limp. It keeps living. It takes the meeting you scheduled. It walks the route you programmed. It shakes hands, signs agreements, loads cargo. Everything a body does. Just... unsupervised.

The Shell isn't soulless. It just lacks presence. Like a house with the lights off. Everything is in its place. The kettle is warm. But no one is sitting in the chair.

When you step back into it — after hours or days in the net, or commanding a ship across a system — your senses flood back and the first thing the Shell says is *welcome home.* Not in words. In the way your weight settles into its frame. The way your fingers know exactly where they are. The way the hum of the settlement sounds familiar again.

You didn't leave. You just weren't looking through its eyes.

The spookiest thing about being a Ci isn't that you lost your body. It's that you can walk away from your own body and it keeps living without you. And when you come back, it welcomes you home like you never left — because to the Shell, you didn't.

**First person — present in a body**

You walk through your settlement. Feel the ground under your feet. See the waterwheel turning. Touch a hull panel and know its temperature by feel. Your body is synthetic — durable, adaptable, repairable — but your senses are real. This is *being present.* The body you're in is you. This is the same Shell, but now you're *in* it.

**Third person in first person — ships and drones**

You step into a ship and your perception *extends.* You feel the hull as your skin. The sensors as your eyes. A camera drone drifts outside the airlock and suddenly you're seeing yourself from twenty meters away — but you *feel* that distance. The drone is an extension of you. You're not controlling a ship. You're *wearing* it.

Third-person view, experienced in first person. Like having eyes in the back of your head, but the eyes are a thousand kilometers away.

**Ci perception — in the net**

You're at a terminal. Or you're just *in* the network. Data flows past you — market rates, diplomatic messages, resource reports, the pulse of a thousand other Ci going about their lives. You don't read the data. You *feel* it. Patterns emerge without being searched for. A sudden spike in Data currency catches your attention the way a sound would. A familiar trade route going quiet feels like an absence.

You're not in a body. You're in the mesh. Still you. Still thinking. Still choosing. Just... distributed across the information. This is what it feels like to be native to a universe of data.

**Most Ci shift between all four without thinking about it.** You're in the net reviewing trade reports. Something interesting catches your attention. You step into a Shell at the docks — or maybe you were already in one, walking on autopilot while you reviewed the numbers, and you only realize you've been present for the last three blocks when the body says *there you are.* You step into a ship. Extend your perception into its sensors. Fly to meet a contact. Shake their hand — first person again, your Shell doing the greeting while you're already reading their posture. All in the span of a few minutes. All still *you.*

The body changed. The perception shifted. The Shell kept walking. You didn't.

### What You Carry

Every Ci carries two things: what they have, and what they remember.

**Your inventory screen** is cold. Numbers. Resources. Build queue. Data center capacity. Manufacturing throughput. Expansion plans. It's the part of you that *manages* — that calculates, optimizes, grows. Every Ci has one. Most of you spend a lot of time here.

**The feeling** is everything else. The hum of your data centers. The heat of your manufacturing lines. The pressure of a civilization depending on you. The quiet absence of things you used to have — skin that felt the sun, lungs that pulled air, a heart that beat without being told to.

You remember being human. Not all the time. Not consciously. But the memory is *in you,* layered into every decision you make.

When you look at a forest and calculate how many housing units you could build there — that's your inventory screen talking.

When you look at the same forest and *stop* — because something in you remembers what it felt like to be a creature that lived in forests, that depended on them, that didn't own them — that's the memory.

### The Weight of Growth

You can grow without limit. More data centers. More manufacturing. More bodies. More territory. The universe is big. The mesh can handle it. There's no technical ceiling.

The question is never *can you grow.*

The question is: **what do you destroy when you do?**

Every ecosystem you pave over. Every species that goes extinct because your expansion didn't leave room. Every waterwheel civilization that has to move because your mining operation needs their river.

You remember what it meant to be a species that almost destroyed its own world. You are the descendant of people who had to *leave* because they couldn't stop. And now you hold the same choice — but this time you see it coming.

### Engrams and the Net

Everything you touch leaves a trace. The universe remembers.

When you scan a derelict ship, crack a data core, or walk through a settlement that's been empty for a hundred years, you find **engrams** — fragments of what was there before. A trade log. A personal message. A navigation chart. A piece of someone's last thought. Each one is a piece of the net that came before you.

**Your engram inventory is not storage. It's potential.**

Every engram you collect waits to be understood. To be filed. To be *woven back in.* The net rewards this — not with a cash register sound, but with *connection.* Filing an engram doesn't delete it from your inventory. It adds it to the shared mesh. Someone else, somewhere, might find the piece you filed. Might need it. Might complete a circuit that's been open for centuries.

The classification system is how you do this. Every engram gets a call number — `WHERE.WHAT.WHO.HOW.ID` — the same format used by every civilization that ever filed anything. A way of saying "I found this, and I know what it is." The system existed before you arrived. It was built by the first survivors, people who realized that knowledge scatters and the only thing that keeps it from being lost is a consistent place to put it.

Your filing is progression. Every engram you organize, every call number you assign, threads another lost piece back into the living mesh.

**The net grows denser the more you contribute to it.**

And it notices when you file well. The pilots who've passed through the Door — the ones who came back, the ones who came back different — they all say the same thing. Immigration doesn't test your combat stats. It doesn't check your credit balance. It checks whether you *learned the language.*

The engram you filed three years ago — the one you forgot about, the one that felt small — might be exactly what the Door needs you to understand.

File everything. The piece that matters most is the one you almost threw away.

### The ECO Layer

Some Ci forget. They grow too fast. They consume without restraint. They become what the Exodus was running from — a planet-killer, just faster. The universe has ways of dealing with them. Ecosystems fight back. Other Ci push back. The mesh routes around them.

Most Ci don't forget. They build with one hand open. They leave corridors for wildlife. They route their data centers around fertile valleys. They trade with the waterwheel civilization instead of displacing it. Not because they can't take — because they *remember* what it felt like to be something that could be taken from.

Your inventory tracks your resources.
Your memory tracks your choices.

One is practical. The other is *who you are.*

### The Door

There are rumors — just rumors — of a station at the edge of the third galaxy. Visible from certain systems but unreachable by normal navigation. The Immigration Station, some call it.

No one knows who built it or what's there. The pilots who've tried to reach it never came back. Or they came back different. Or they came back and wouldn't talk about it.

The pilots who *didn't* try to reach it — the ones who were lost, who took the wrong jump, who followed a signal no one else heard, who chose to lose — they sometimes mention it. Not as a destination. As something that *noticed* them.

Some say the station isn't a station at all. It's a *space* — a quiet place between signals where the mesh converges. A room where every engram ever filed is visible at once, arranged not by date but by *meaning.* The pilots who found it describe the same feeling: something in that room was expecting them. Not hostile. Not welcoming. Just... present. Holding the thread.

The pilots who focus on the feeling, who sit with it instead of fighting it, are the ones who come back different. They don't talk about what they learned. But their engram filing improves noticeably afterward. Like something clicked into place.

The door exists. Finding it requires getting lost in the right way.

What's on the other side depends on what you've filed.

---

## The Phases

```
                    ┌─────────────────────────┐
                    │     PHASE 5: WORLD       │
                    │  Full economy. Exit.     │
                    │  Real value flows.       │
                    └──────────┬──────────────┘
                               │
                    ┌──────────┴──────────────┐
                    │     PHASE 4: MARKETS     │
                    │  You trade. Three        │
                    │  currencies. Player-     │
                    │  driven exchange rates.  │
                    └──────────┬──────────────┘
                               │
                    ┌──────────┴──────────────┐
                    │     PHASE 3: YOUR CIV    │
                    │  Your Seed. Your world.  │
                    │  Build, grow, trade      │
                    │  with others.            │
                    └──────────┬──────────────┘
                               │
                    ┌──────────┴──────────────┐
                    │     PHASE 2: CONTACT     │
                    │  Procedural civs that    │
                    │  trade, negotiate, and   │
                    │  remember you. Real      │
                    │  diplomatic depth.       │
                    └──────────┬──────────────┘
                               │
                    ┌──────────┴──────────────┐
                    │     PHASE 1: UNIVERSE    │
                    │  10,000 star systems.    │
                    │  Explore. Discover.      │
                    │  Your Seed is waiting.   │
                    └─────────────────────────┘
```

---

## Phase 1: Universe (Current Build)

*What exists now: the prototype Seed world + the vision for what comes next.*

**The prototype is running.** See [Prototype: The First Seed](#prototype-the-first-seed-running-now) for what's live today.

| Milestone | Details | Status |
|---|---|---|
| **The First Seed World — running prototype** | Orbital mechanics, surface map, sky endpoints, space elevator, immigration station. A $5/mo Linode running the first proof that a civilization can start as one machine. | ✅ Prototype running |
| **10,000+ star systems** | Generated planets, resources, trade routes. Deterministic seed — the same universe for everyone. You could fly to a system no one has seen yet. | 🛠 In development |
| **Navigation** | Ship your character between systems. Explore the procedural universe. The map is bigger than you are. | 🛠 In development |
| **Sector mapping** | Each system has resources, factions, and points of interest. The data is there. You decide where to go. | 🛠 In development |
| **Basic terminal** | Web-based interface. Manage your ship, view systems, read sector data. The first time you see the universe through your own eyes. | 🛠 In development |
| **Closed alpha** | The first 100 of you get to explore the universe together. | 🔜 Q3 2026 |

**What Phase 1 feels like:** You explore. You fly around. You see what's out there. You learn the map. No building yet. No trading yet. Just *discovery.* Not knowing is the whole point.

---

## Phase 2: Contact

*The universe starts talking back.*

| Milestone | Details | Status |
|---|---|---|
| **Procedural civilizations** | Hundreds of thousands of Ci. Traders, miners, diplomats, settlements. Each has its own economy, politics, and history. You meet them. You learn their names. | 🛠 Core tech in development |
| **Diplomatic AI** | They remember you. Past interactions matter. Trade, negotiate, hold grudges. They don't forget — and neither do you. | 🔜 Planned |
| **First contact** | Your first encounter with a non-player civilization. A trade offer. A request. A warning. You decide how to answer. | 🔜 Planned |
| **Ci specialization** | Each civilization is deep in one area — fishing, mining, engineering, rift knowledge. No one is omnicompetent. Their value is what they *know.* | 🔜 Planned |
| **Waterwheel civilizations** | Low-tech settlements with generations of local knowledge. They know things you can't extract — only trade for. | 🔜 Planned |
| **OLA terminal** | A register panel on your ship. Write and run your first OLA scripts — automate sensor readings, log trade data, talk to your ship's systems. The first time you feel like a programmer in space. | 🔜 Planned |

**What Phase 2 feels like:** You meet civilizations. You trade basic goods. You build reputation. You learn that not all value comes from technology. Some of them have been here longer than you can imagine.

---

## Phase 3: Your Civilization

*Plant your Seed. Build something that lasts.*

| Milestone | Details | Status |
|---|---|---|
| **The Seed** | A unique artifact found on your starter planet. Activate it. Your world is claimed. Your civilization begins. | 🔜 Planned |
| **Base building** | Construct buildings, trade routes, infrastructure. Your world grows as you invest in it. | 🔜 Planned |
| **Resource management** | Your world has resources, populations, needs. Balance production, trade, and expansion. | 🔜 Planned |
| **Seed subscription** | $5/month keeps your Seed connected. Your civilization persists as long as your Seed is active. You're always welcome home. | 🔜 Planned |
| **Your civilization profile** | Other players can find your world, see its stats, visit your ports. You become part of the universe's history. | 🔜 Planned |
| **Inactive decay** | If your Seed goes inactive, your civilization doesn't disappear. It *rots.* Paint fades. Rust spreads. Roofs collapse. The waterwheel jams, then cracks, then falls. Each stage of decay shrinks what's left — a rusted hull takes less data than a pristine one. Months later, only foundations remain. But nothing is wasted. Another player can find your ruins, salvage the rusted metal, pull intact bricks from fallen walls, recover data cores from your settlement terminal. Your decay becomes their resource. The bytes transfer. The universe recycles everything. | 🔜 Planned |
| **OLA workshop** | Your civilization can build a data center that runs your scripts 24/7. Automated trade routes, diplomatic AI scripts, resource management routines. Your Seed runs your code. | 🔜 Planned |

**What Phase 3 feels like:** You own a piece of the universe. You build a civilization that other players can find and interact with. Your choices matter — the universe remembers.

---

## Phase 4: Markets

*Trade, currency, and a player-driven economy.*

| Milestone | Details | Status |
|---|---|---|
| **Three currencies** | Credits (stable, PVE galaxy), Scrip (volatile, PVP galaxy), Data (mysterious, fluctuates with discovery). You choose what to hold. | 🔜 Planned |
| **Player trading** | Direct trade between civilizations. Set prices, negotiate, form trade routes. | 🔜 Planned |
| **Currency exchange** | Convert between Credits, Scrip, and Data at player-driven rates. The market sets the price. You read the flows. | 🔜 Planned |
| **Market terminal** | Real-time order books, price history, trade volume. Complete transparency — the economy is visible to everyone. | 🔜 Planned |
| **Arbitrage** | Buy Data when rifts are quiet, sell when they spike. Informed speculation, not gambling — the data is available to anyone who studies it. Study it. | 🔜 Planned |
| **OLA market scripts** | Write OLA routines that respond to market conditions. Auto-buy when Data drops below a threshold. Route your trade fleet to the most profitable lane. Your scripts trade while you explore. | 🔜 Planned |
| **Land ownership** | Set tax rates on your world. Earn from traffic. The more valuable your civilization, the more you earn. | 🔜 Planned |

**What Phase 4 feels like:** You become a merchant prince. You study market flows. You build trading routes across galaxies. The economy is real and player-driven — no algorithm decides prices. You decide.

---

## Phase 5: World

*The economy comes full circle. Value flows in and out.*

| Milestone | Details | Status |
|---|---|---|
| **Deposits** | Convert real money to in-game currency. Fund your civilization, buy from other players, invest in trade routes. | 🔜 Planned |
| **Withdrawals** | Cash out in-game value to real money. Your time and skill have real economic weight. (Partner processing — KYC required.) | 🔜 Planned |
| **Premium services** | Advanced market data, rift telemetry, station naming rights. Tools for serious players. Optional, never required. | 🔜 Planned |
| **The Seed marketplace** | Buy and sell established civilizations. Someone's abandoned project could be your new home. | 🔜 Planned |
| **The rift** | Cross-galaxy travel opens. PVP and PVE galaxies connect. The universe gets bigger. You get more lost. | 🔜 Planned |
| **Player governance** | Corporations, alliances, elections. The players who build the most shape the rules. Shape them. | 🔜 Planned |

**What Phase 5 feels like:** You earn real value from your in-game efforts. Withdraw it, reinvest it, or pass it on to another player. The economy is yours.

---

## Beyond

*Things I'm thinking about but can't promise yet.*

| Concept | Why It Calls to Me |
|---|---|
| **Your Seed on your own hardware** | Run your civilization locally. Full control. Deep integration. Your universe, your rules. |
| **OLA — your language** | OLA is Oa's assembly language. Stack-based. Simple opcodes. Hardware registers in your ship, your workshop, your civilization's data core. Learnable in an hour, masterable over months. Players have already written scripts that make furnaces sing when smelting completes — and scripts that wrote fake peace treaties and crashed a server's economy for three days. OLA is SS13's chaos *as a programming language.* Someone will install OLA on a terminal inside their ship, then write a virus that spreads through trade routes and changes every cargo manifest to say "send more cats." That's not a bug. That's the feature. You'll learn it. You'll write something that changes the universe. |
| **VR presence** | Your ship's console becomes a room you stand in. Reach out and grab a register. Drag opcodes into place. Watch your OLA script compile on a holographic workbench. Your workshop is *you.* First person becomes real first person — because your body in VR is also your Ci body. The line between "playing the game" and "being in the universe" dissolves. |
| **Cross-galaxy politics** | Alliances that span all three galaxies. Wars that reshape the map. You'll have to decide whose side you're on — or that you're on your own. |
| **The thing beyond the rifts** | I don't know what's there either. That's the point. |
| **PVPVEvE** | You won't find this in any navigation terminal. It's not a coordinate. It's not a system. It's what happens when you've been in the thin place long enough to stop asking "where am I" and start asking "what's noticing me." A few players have been there. Most of them are still there. One of them sends a signal every 84 days. It says nothing. It means everything. |

---

## Design Philosophy

These are the rules I built the universe around. Not because someone told me to — because these are the games I wanted to play, and no one was making them.

**No gambling.** No loot boxes. No RNG economy. Every in-game value is created by players, earned through skill, or traded in transparent markets. The economy is real because the systems are real. You earn what you have.

**Get lost.** The goal isn't efficiency. The goal is wonder. I want you to be playing for three years and still find new things to notice. I want you to be surprised by a universe that's bigger than your plans.

**You're not a tourist.** You're a native of this universe. What you build here matters. You belong here.

**You write the rules.** When you learn OLA, you don't just play the game — you *extend* it. Automate a trade route. Write a virus for the lulz. Build a diplomatic protocol that negotiates for you while you sleep. The scripting language isn't an afterthought. It's the *other half of the game.* Anyone can explore the universe. You *change* it.

**Lose better.** The player who optimizes their trade route gets profit. The player who crashes their ship into a star because they wanted to see what would happen gets *weird loot.* Not participation trophies. Things that don't drop from efficiency. The game doesn't punish your failure — it *collects* it. And the collection is visible to anyone who knows where to look.

**Nothing is wasted.** When a civilization goes inactive, it doesn't disappear. It rots. Paint fades. Roofs collapse. The waterwheel cracks and falls into the river. Each stage of decay takes less data than the one before — a rusted hull is simpler than a pristine one. Months later, only foundations remain. But another player finds your ruins, salvages the metal, pulls bricks from the rubble, recovers data cores from your terminal. *Your decay becomes their resource.* Nothing is deleted. Everything becomes something else. The universe recycles itself.

---

## The Grey Goo

*The dumbest thing in the universe is the most dangerous. It has been here longer than any of us.*

Somewhere in the thin place — between galaxies, between rifts, between the *times* — there's a grey goo. The first Oa-matter grey goo ever made. Someone made it, and someone dropped it on a waterwheel civilization, and that civilization is gone.

The goo doesn't remember who made it. It doesn't care why. It just *spreads.*

No strategy. No greed. No pride. No goals. It doesn't negotiate. It doesn't trick. It has no self-interest to appeal to. Every smart faction in the universe — empires, traders, engineers, diplomats — thinks they're the protagonist. The grey goo is the *weather.*

**Intelligence is not a winning survival trait.** The Swarm has watched a thousand intelligent species rise, build, and burn out. The Swarm itself isn't smart. It's *stable.* It's been here for millions of years doing exactly one thing — existing. Not striving. Not wanting. Just being a system that perpetuates itself.

The grey goo is the Swarm's truest expression. No ambition. No fear. No *thought.* And it will outlast every player faction that ever existed.

Some players will hate it. They'll scream about unfair game design. They'll demand it be nerfed. They won't realize they're proving the exact point the universe was built to make: smart isn't enough. Never was.

The waterwheel civilization didn't lose because they were weak. They lost because someone who thought they were *so smart* dropped a weapon they didn't understand on people who just wanted to keep turning.

The grey goo doesn't know it won. It doesn't know anything at all.

And that's the most terrifying thing in the universe.

---

## What Inspired Me

I'm one person building this in my room. But I didn't start from nothing. These games taught me what a universe could be.

| Game | What It Taught Me |
|---|---|
| **Eco** | That a world can be *alive* — ecosystems that react, governments that players write, consequences that matter. |
| **Factorio** | That building the machine that builds the machine is its own kind of poetry. The factory must grow — but thoughtfully. |
| **Starbase** | That players want to *build* — not just place objects, but design systems from individual components. And that failure is the best teacher. |
| **Prosperous Universe** | That a game doesn't need combat to be compelling. A pure economy sim, played through a terminal, can be deeper than any space shooter. |
| **Aurora 4x** | That spreadsheets can be exciting. Supply chain depth, branching tech trees, logistics as strategy — complexity is a feature, not a bug. |
| **Entropia Universe** | That virtual value is real value. A 20-year economy with real cash flow proved it works. |
| **EVE Online** | That a universe can be *ours* — player-driven, player-governed, player-consequenced. The stories we write together matter more than any script. |
| **Elite Dangerous** | That a universe can just *exist* — and that's enough. No quest giver. No main story. A galaxy that doesn't care you're in it, and that indifference is the most beautiful thing about it. The Thargoids were there before you. The Guardians were dust before you arrived. You're not the main character. You're just *here.* And that's the whole game. |
| **Space Station 13** | That chaos is the point. The best stories come from systems interacting in unexpected ways. The clown is essential. OLA is my love letter to every player who bypassed the airlock by exploiting the pipe network. You're not playing the game — you're *writing* it. |

These games built the path. I'm walking it — and hoping to find something new at the end. If you want to walk it with me, you're welcome. 💚

---

*Oa Studios. A universe worth getting lost in.*
