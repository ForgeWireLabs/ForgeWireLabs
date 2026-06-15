# ForgeWire Labs

ForgeWire Labs is an independent engineering and applied AI research lab founded by Jeremy Shows.

I build systems around a simple question: how capable can AI-assisted software become while remaining constrained, inspectable, user-owned, and useful on real hardware?

ForgeWire began as an attempt to build a better personal AI system. It has grown into a modular architecture for coordinating models, agents, tools, memory, knowledge, compute, and remote execution without surrendering control to a hosted platform. The work combines production engineering with longer-term research into recurrent reasoning, continual learning, adaptive routing, persistent agency, and human-directed automation.

ForgeWire Labs is where those ideas become working systems.

## Start here

- **[ForgeWire Fabric](https://github.com/ForgeWireLabs/forgewire-fabric)** — self-hosted control plane for trusted remote task execution.
- **[SkillForge Academy](https://github.com/ForgeWireLabs/skillforge-academy)** — offline-first certification learning and exam-preparation software, beginning with CompTIA A+.
- **[SCOUT-2](https://github.com/ForgeWireLabs/SCOUT-2)** — earlier multi-agent assistant platform and historical foundation for later ForgeWire work.

## What makes this different?

Most AI tooling assumes hosted control planes, cloud-first state, and broad agent permissions. ForgeWire Labs works in the opposite direction:

- user-owned machines
- signed task envelopes
- explicit policy gates
- auditable execution trails
- local-first app data
- agents treated as constrained tools, not magic

The goal is practical infrastructure that remains useful under real-world constraints.

## Current projects

### ForgeWire Fabric

ForgeWire Fabric is the public control-plane layer of the ForgeWire ecosystem. It focuses on authenticated dispatch, capability-aware runner integration, structured events, policy gates, and auditable coordination across machines.

### SkillForge Academy

SkillForge Academy is an offline-first certification learning and exam-preparation desktop app. The first track is CompTIA A+, with structured objectives, original practice questions, PBQs, mock exams, flashcards, spaced repetition, readiness analytics, notes, search, and encrypted local progress backups.

### SCOUT-2

SCOUT-2 is an earlier multi-agent assistant platform. It remains public as historical context for the experiments and lessons that informed later ForgeWire work.

## Focus areas

- Local-first AI and developer tooling
- Agent orchestration and constrained automation
- Secure task dispatch and event-driven control planes
- Offline-capable desktop applications
- Certification learning systems and technical education software
- Practical ML systems, routing, replay, and evaluation workflows

## Working principles

- Build useful systems before making large claims.
- Prefer auditable workflows over opaque automation.
- Keep local ownership and user control central.
- Treat agents as constrained tools, not magic.
- Make research ideas earn their way into working software.

## Primary stack

Rust · Python · TypeScript · React · Tauri · SQLite/rqlite · PowerShell · GitHub Actions

## Public status

ForgeWire Labs uses private development branches and public release mirrors. Public repositories are cleaned before release so docs, tests, security notes, and changelogs remain understandable to outside readers.

Current public focus:

- ForgeWire Fabric: public mirror and documentation hardening
- SkillForge Academy: desktop certification-learning MVP
- ForgeWire core: private active development
