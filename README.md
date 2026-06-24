<!-- Banner. Replace assets/banner.svg with a PNG export if you prefer raster. -->
![ForgeWire Labs — inspectable agentic infrastructure, repo-native governance, distributed execution, human attention boundaries, practical AI](assets/banner.svg)

# Jeremy Shows

**Founder & Principal Engineer, ForgeWire Labs**

I build **inspectable agentic infrastructure**: repo-native work governance, secure distributed execution, human-in-the-loop communication boundaries, and practical AI software that stays useful under real-world constraints — when models are fallible, hardware is limited, infrastructure shifts, and real people depend on the result.

Former mechanic, race-car builder, fabricator, IT professional, and small-business owner, now building distributed systems and applied AI infrastructure. I see AI systems as **machinery** — assemblies of components with interfaces, tolerances, feedback paths, authority boundaries, and failure modes — and I hold them to that standard: a convincing demo is not enough; the system has to keep working when a part fails, the hardware is constrained, the requirements change, or an automated process exceeds its authority.

> **Build it. Test it under failure. Preserve the evidence. Understand its limits. Then decide whether it is useful.**

---

## What ForgeWire Labs Builds

ForgeWire Labs creates infrastructure for agentic systems that can be inspected, governed, delegated, audited, and recovered.

Most agent products ask you to trust the agent.

ForgeWire Labs is built around a different premise:

> **Inspect the work. Bound the authority. Preserve the evidence.**

The public projects are organized around the boundaries agentic systems need when they move from demos into real work:

```text
RepoPact  → inspectable work governance
Fabric    → inspectable execution governance
ForgeLink → inspectable human-attention governance
ForgeWire → integrated agentic environment
```

The goal is not to make a model appear autonomous. The goal is to build the surrounding infrastructure that lets models, agents, tools, humans, and machines cooperate without hiding state, authority, failure, or responsibility.

---

## Agentic Infrastructure

### 🧵 [ForgeWire Fabric](https://github.com/ForgeWireLabs/forgewire-fabric) · **Available — Alpha**

[![release](https://img.shields.io/github/v/release/ForgeWireLabs/forgewire-fabric?label=release&color=f59e0b)](https://github.com/ForgeWireLabs/forgewire-fabric/releases)
[![license](https://img.shields.io/github/license/ForgeWireLabs/forgewire-fabric?color=3b82f6)](https://github.com/ForgeWireLabs/forgewire-fabric/blob/main/LICENSE)

A self-hosted control plane for **authenticated remote task execution**.

Fabric moves work across machines while keeping authority, policy, provenance, and execution history explicit. It provides signed dispatch, scoped capability routing, policy-gated runners, structured task events, live streams, audit/replay, and a private control plane for running agentic and command work on hardware you control.

```text
authorized intent → signed dispatch → scoped runner → streamed execution → audit trail
```

Fabric is for teams and operators who want remote agents, local compute, GPU boxes, build hosts, lab machines, and private infrastructure without surrendering execution control to a hosted agent platform.

`agentic-ai` · `remote-execution` · `mcp` · `distributed-systems` · `rust`

![forgewire-fabric-cli doctor — a healthy hub on an rqlite-backed cluster](assets/fabric-doctor.svg)

> 📐 Architecture diagram lives in the [Fabric README](https://github.com/ForgeWireLabs/forgewire-fabric#how-it-works).
<!-- TODO: add a short terminal/demo recording (assets/fabric-demo.gif). -->

---

### 📜 [RepoPact](https://github.com/ForgeWireLabs/repopact) · **Available — Early Development**

[![license](https://img.shields.io/github/license/ForgeWireLabs/repopact?color=3b82f6)](https://github.com/ForgeWireLabs/repopact/blob/main/LICENSE)

A **repo-native kernel for durable work between humans and coding agents**.

RepoPact keeps authority, intent, work state, evidence, decisions, drift checks, and project history inside the repository instead of letting them vanish with each agent session. It is the harness inside the harness: Claude Code, Codex, Cursor, OpenHands, VS Code agents, Minion-style agents, or any other coding harness can enter the same governed work environment.

```text
intent → scoped authority → work item → implementation → evidence → audit → history
```

RepoPact makes short prompts possible because the repository carries the operating context. A prompt like:

```text
Proceed to the next active work item.
```

can be meaningful when the repo already defines active work, invariants, evidence gates, validation rules, completion protocol, and update expectations.

RepoPact does not replace coding agents. It gives them a durable operating environment.

`coding-agents` · `repository-governance` · `agents-md` · `developer-tools` · `ai-governance`

![RepoPact core loop over a filesystem state machine](assets/repopact-flow.svg)

---

### ☎️ [ForgeLink](https://github.com/ForgeWireLabs/ForgeLink) · **Available — Early Development**

A local-first **human attention and approval boundary for agentic systems**.

ForgeLink gives local agents, MCP clients, and ForgeWire/Fabric workflows a controlled way to ask for human attention, request approval, and receive human decisions without becoming another feed, leaking sensitive context into ordinary chat surfaces, or turning the operator into a notification target.

```text
agent request → attention policy → human decision → recorded outcome
```

ForgeLink currently ships as an Electron desktop app with a TypeScript backend, local SQLite storage, Twilio SMS/MMS support, an MCP human bridge, per-channel credentials, backup/export tools, delivery-state handling, and explicit attention policy.

It is not a social feed, public messaging platform, work runner, or hosted notification relay. It is a private operator boundary for agent-human communication.

`human-in-the-loop` · `mcp` · `electron` · `twilio` · `agentic-ai`

---

## Product Work

### 🎓 [SkillForge Academy](https://github.com/ForgeWireLabs/skillforge-academy) · **Downloadable Product**

[![release](https://img.shields.io/github/v/release/ForgeWireLabs/skillforge-academy?label=download&color=22c55e)](https://github.com/ForgeWireLabs/skillforge-academy/releases)

An **offline-first certification learning and exam-prep desktop app**, starting with CompTIA A+.

SkillForge Academy includes original practice questions, performance-based questions, mock exams, spaced-repetition flashcards, readiness analytics, and local progress storage. It is built with Tauri, Rust, and React.

SkillForge is not part of the agentic infrastructure stack, but it reflects the same engineering priorities: local-first operation, practical usefulness, visible progress, durable state, and software that remains useful without a cloud dependency.

`comptia` · `exam-prep` · `tauri` · `rust` · `react` · `offline-first`

![SkillForge Academy — Study Command Center](assets/skillforge-command-center.png)

---

## The Larger System: [ForgeWire](https://github.com/ForgeWireLabs/ForgeWire-Overview)

The public projects above are extracted from, adjacent to, or designed for a larger **privately developed** system.

ForgeWire is a modular architecture for coordinating models, agents, tools, skills, personas, memory, knowledge, task execution, automation, policy, human interaction, and distributed compute.

Its engineering thesis:

> **Agentic systems are systems first and models second.**

A capable model can still be part of an unreliable system.

Models can be wrong, slow, expensive, unavailable, deprecated, or replaced. Providers change. Dependencies fail. Hardware becomes constrained. Requirements evolve. People still need the system to preserve context, expose what happened, recover when possible, and respect authority boundaries.

ForgeWire focuses on the infrastructure around models:

- graceful degradation
- explicit ownership boundaries
- provider freedom
- behavioral parity
- durable audit trails
- recoverable execution
- bounded agent authority
- replaceable components
- inspectable failure states
- human approval paths
- repo-native memory and governance

The [public overview](https://github.com/ForgeWireLabs/ForgeWire-Overview) documents the direction and release status without presenting unfinished private work as a product.

---

## How the Pieces Fit

```text
Outer harness
Claude Code / Codex / Cursor / OpenHands / VS Code agents / local agents
        |
        v
RepoPact
repo-native work governance:
invariants, active work, evidence, drift, decisions, history
        |
        v
ForgeWire
provider network, personas, skills, memory, knowledge, orchestration
        |
        +----------------------+
        |                      |
        v                      v
Fabric                 ForgeLink
secure execution       human attention / approval
dispatch, policy,      ask, escalate, decide,
streams, audit         record outcome
        |
        v
Runner / model
minimal safe projection needed to act
```

The model should not be the security boundary.

The prompt should not be the only memory.

The chat window should not be the audit log.

The human should not become a notification endpoint.

ForgeWire Labs projects are built to move those responsibilities into inspectable infrastructure.

---

## How I Build

- **Systems before components.** A working part is not a working system. I design for seams, failure modes, authority boundaries, recovery paths, and operational evidence first.
- **Evidence over demos.** Releases should include documentation, tests, security context, known limitations, architecture, and validation paths so they can be evaluated seriously.
- **Prompt text is not a security boundary.** Agents receive projected authority; tools, policy, scope, and execution layers enforce what is actually allowed.
- **Parity and portability.** Acceleration paths get portable reference implementations. The system should not be pinned to one language, model provider, database, harness, cloud, or machine.
- **Local-first where it matters.** Human communication, credentials, private state, and operator decisions should remain close to the person unless a stronger boundary is deliberately designed.
- **Research is gated.** Speculative ideas move through isolated implementation, baseline comparison, controlled evaluation, failure analysis, observe-only integration, and limited canary testing before production adoption.
- **Failure should become state.** A failed provider, denied approval, broken dependency, missing capability, or exceeded authority should be visible, recoverable system state — not confident language hiding uncertainty.

**Stack:** Rust · Python · TypeScript · React · Tauri · Electron · GTK · SQLite · rqlite · PostgreSQL · PowerShell · GitHub Actions

---

## Lineage & Archive

The current work descends from years of building, failure, and reconstruction:

```text
SCOUT → SCOUT-2 → ATLAS → PhrenForge → ForgeWire
```

Across those generations:

- a chatbot became a multi-persona assistant
- prompts became tools, skills, permissions, and services
- direct execution gained policy and capability boundaries
- scattered context became repo-native memory and governance
- local workflows expanded into authenticated distributed execution
- human communication became a private attention and approval boundary
- model-centered development became systems-first engineering

Historical projects:

- [SCOUT-2](https://github.com/ForgeWireLabs/SCOUT-2) — *Historical.* Multi-agent assistant platform; a record of experiments, communication tools, agent patterns, and architectural limits that led to ForgeWire, ForgeLink, and later infrastructure.
- Earlier public projects (**SCOUT**, **Feed-Portal**, **MED.I.C.**) are *archived* and kept for history — not current work.

---

<!-- TODO (headshot — on you): once you add assets/headshot.jpg, uncomment the block below.
<img src="assets/headshot.jpg" align="right" width="180" alt="Jeremy Shows" />
-->

<!-- TODO (writing): drafts live in writing/. Once finalized, uncomment to surface them.
## Writing

- **Agentic systems are systems first and models second** — reliability lives in the assembly, not the component.
- **Why coding agents need repository-native governance** — binding invariants and durable state in the repo.
- **Remote agents without surrendering execution control** — signed dispatch, scope-bound tokens, audited runs.
- **Human attention is infrastructure** — why agent systems need private communication boundaries.
- **Building serious AI infrastructure on constrained hardware** — constraints as a design input.
- **What failed between SCOUT and ForgeWire** — the lineage read as corrected structural failures.

---
-->

**Independent · founder-led · evidence-driven.** Reach me through the repositories above, or open an issue/security advisory on the relevant project.
