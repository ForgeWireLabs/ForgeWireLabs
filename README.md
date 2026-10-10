![ForgeWire Labs: software for AI work, remote execution, and human decisions](assets/banner.svg)

<p align="center"><strong>FORGEWIRE · COMING SOON</strong><br>Private development · No public download or release date announced</p>

**ForgeWire is the main application under development at ForgeWire Labs.** It brings personas, model providers, tools, skills, projects, and tasks into a workspace the operator controls. See the [ForgeWire overview](https://github.com/ForgeWireLabs/ForgeWire-Overview) for a screen capture, architecture diagrams, instructions for private workspaces, and release status.

| Explore | What you will find |
| --- | --- |
| [ForgeWire overview](https://github.com/ForgeWireLabs/ForgeWire-Overview) | Current public presentation, a genuine development-build Projects capture, five architecture diagrams, and Coming Soon status. |
| [RepoPact Core](https://github.com/ForgeWireLabs/repopact-core) | Public, early-development repository governance. |
| [ForgeLink](https://github.com/JeremyShows/ForgeLink) | Public, early-development human-agent communication. |
| ForgeWire Fabric | Private alpha execution control plane; no public deployment path. |

---

# Jeremy Shows

**Founder & Principal Engineer, ForgeWire Labs**

I build **inspectable agentic infrastructure**: repo-native work governance, secure distributed execution, human-in-the-loop communication boundaries, and practical AI software that stays useful under real-world constraints. Models can be fallible, hardware can be limited, infrastructure can change, and real people depend on the result.

ForgeWire Labs is a **largely solo, human-led, deeply AI-assisted engineering and research effort**. I work directly alongside multiple AI systems across technical research, architecture, implementation, debugging, testing, review, and documentation. I choose runtimes, languages, system boundaries, patterns, workflows, and product direction; challenge or reject agent proposals; and often step into deadlocked implementation loops with the root-cause fix or missing abstraction before sending the work back through implementation and validation.

AI systems make substantial contributions to the work. I do not claim unaided authorship, and the projects build extensively on open research, open-source software, commercial AI tools, and established systems engineering. At the same time, the engineering process is not delegated wholesale to agents: I research alongside them, integrate the resulting work, and retain technical responsibility for architecture, system behavior, validation, and final acceptance.

Former mechanic, race-car builder, fabricator, IT professional, and small-business owner, now building distributed systems and applied AI infrastructure. I see AI systems as **machinery**, with interfaces, tolerances, feedback paths, authority boundaries, and failure modes. I hold them to that standard: a convincing demo is not enough; the system has to keep working when a part fails, the hardware is constrained, the requirements change, or an automated process exceeds its authority.

> **Build it. Test it under failure. Preserve the evidence. Understand its limits. Then decide whether it is useful.**

---

## What ForgeWire Labs Builds

ForgeWire Labs builds tools for tracking agent work, setting permissions, running tasks, and recording decisions.

The projects cover different parts of that work. Some have public repositories; others are still private:

```text
RepoPact  → repository work records                 [public / Apache-2.0]
Fabric    → remote execution                       [private / proprietary]
ForgeLink → human-agent communication               [public project]
ForgeWire → application and runtime                 [private development]
```

The common concern is practical: people need to know what ran, what it changed, and what to do when it fails.

---

## Agentic Infrastructure

### 🧵 ForgeWire Fabric · **Private Development: Alpha**

A self-hosted control plane for **authenticated remote task execution**.

Fabric moves work across machines while keeping authority, policy, provenance, and execution history explicit. It provides signed dispatch, scoped capability routing, policy-gated runners, structured task events, live streams, audit/replay, and a private control plane for running agentic and command work on hardware you control.

```text
authorized intent → signed dispatch → scoped runner → streamed execution → audit trail
```

Fabric is for operators who want remote agents, local compute, GPU boxes, build hosts, lab machines, and private infrastructure without surrendering execution control to a hosted agent platform.

**Licensing status:** current Fabric source and current/future ForgeWire Labs development are private and proprietary, not open source, unless a specific distribution is explicitly licensed otherwise. Versions or copies previously distributed under Apache License 2.0 remain licensed under the terms that accompanied those specific versions or copies. The move to private development does not revoke rights already granted for historical Apache-2.0 distributions.

`agentic-ai` · `remote-execution` · `mcp` · `distributed-systems` · `rust`

![forgewire-fabric-cli doctor: a healthy hub on an rqlite-backed cluster](assets/fabric-doctor.svg)

---

### 📜 [RepoPact Core](https://github.com/ForgeWireLabs/repopact-core) · **Available: Early Development**

[![license](https://img.shields.io/github/license/ForgeWireLabs/repopact-core?color=3b82f6)](https://github.com/ForgeWireLabs/repopact-core/blob/main/LICENSE)

A **repo-native kernel for durable work between humans and coding agents**.

RepoPact keeps authority, intent, work state, evidence, decisions, drift checks, and project history inside the repository instead of letting them vanish with each agent session. Claude Code, Codex, Cursor, OpenHands, VS Code agents, and other coding tools can use that repository state.

```text
intent → scoped authority → work item → implementation → evidence → audit → history
```

RepoPact makes short prompts possible because the repository carries the operating context. A prompt like:

```text
Proceed to the next active work item.
```

can be meaningful when the repo already defines active work, invariants, evidence gates, validation rules, completion protocol, and update expectations.

RepoPact does not replace coding agents. It gives them a durable operating environment.

The desktop and mobile application is developed separately in [RepoPact Workbench](https://github.com/ForgeWireLabs/repopact-workbench).

`coding-agents` · `repository-governance` · `agents-md` · `developer-tools` · `ai-governance`

![RepoPact core loop over a filesystem state machine](assets/repopact-flow.svg)

---

### ☎️ [ForgeLink](https://github.com/JeremyShows/ForgeLink) · **Available: Early Development**

A local-first **communications and decision runtime for humans and agents**.

ForgeLink gives agents a way to request attention or approval and gives people one place to review those requests. It records decisions and outcomes without pushing sensitive context into ordinary chat channels.

```text
human / agent / channel → governed communication state → decision → recorded outcome → replay
```

ForgeLink currently includes SMS/MMS through Twilio and Telnyx, Twilio Voice, call history, contacts, approval requests with supporting evidence, signed decision records, and an audit chain. It runs as an Electron/TypeScript app with local SQLite storage, an MCP bridge, and backup/export tools. An operator view and mobile companion are in progress.

It is not a phone clone, social feed, public messaging platform, work runner, or hosted notification relay. It is a private operator boundary for human-agent communication.

`human-in-the-loop` · `operator-cockpit` · `communications-runtime` · `mcp` · `electron` · `agentic-ai`

---

## Product Work

### 🎓 [SkillForge Academy](https://github.com/JeremyShows/skillforge-academy) · **Downloadable Product**

[![release](https://img.shields.io/github/v/release/JeremyShows/skillforge-academy?label=download&color=22c55e)](https://github.com/JeremyShows/skillforge-academy/releases)

An **offline-first certification learning and exam-prep desktop app**, starting with CompTIA A+.

SkillForge Academy includes original practice questions, performance-based questions, mock exams, spaced-repetition flashcards, readiness analytics, and local progress storage. It is built with Tauri, Rust, and React.

SkillForge is not part of the agentic infrastructure stack, but it reflects the same engineering priorities: local-first operation, practical usefulness, visible progress, durable state, and software that remains useful without a cloud dependency.

`comptia` · `exam-prep` · `tauri` · `rust` · `react` · `offline-first`

![SkillForge Academy: Study Command Center](assets/skillforge-command-center.png)

---

## The Larger System: [ForgeWire](https://github.com/ForgeWireLabs/ForgeWire-Overview)

The projects above are extracted from, adjacent to, or designed for a larger **privately developed** system.

ForgeWire is an application and runtime being built to coordinate models, personas, tools, skills, context, tasks, and compute around real work. Selected private workflows already use application services and graph execution. Broader run-lifecycle convergence and distributed execution integration remain active work.

Its engineering thesis:

> **Agentic systems are systems first and models second.**

A capable model can still be part of an unreliable system.

Models can be wrong, slow, expensive, unavailable, deprecated, or replaced. Providers change. Dependencies fail. Hardware becomes constrained. Requirements evolve. People still need the system to preserve context, expose what happened, recover when possible, and respect authority boundaries.

ForgeWire's engineering direction focuses on the infrastructure around models:

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

The [public overview](https://github.com/ForgeWireLabs/ForgeWire-Overview) shows the current interface evidence, architecture and limits. ForgeWire has no public build, supported install path, stable API, or announced release date.

---

## How the Pieces Relate

| Project | Boundary | Relationship to ForgeWire |
| --- | --- | --- |
| **RepoPact Core** | Repository-native work governance for humans and coding agents | A separate public project whose governance ideas inform the engineering workflow. It is not a required ForgeWire installation step. |
| **ForgeWire** | Operator-owned application and runtime | Coordinates configured personas, providers, tools, state, and selected workflows in the private application. |
| **ForgeWire Fabric** | Authenticated remote execution and operator control | A separate private alpha control plane. Selected, configuration-dependent application paths integrate with it; broad composition and public deployment remain open. |
| **ForgeLink** | Human-agent communication and decisions | A separately maintained public project adjacent to ForgeWire's human-authority direction. The profile does not imply a shipped end-to-end integration. |

Each project has its own scope and development pace. The [ForgeWire architecture diagrams](https://github.com/ForgeWireLabs/ForgeWire-Overview#how-the-system-fits-together) distinguish existing paths, optional configuration, private implementation, and proposed work.

Permissions belong in software controls. Work history belongs in durable records. Requests for human decisions need a place where those decisions can be reviewed later.

---

## How I Build

I start by defining who owns an action, what data it can use, and how a failure will appear to the operator. I use AI coding tools throughout the work, but I check their results against the code, the tests, and the behavior of the running system.

When a proposed fix keeps failing, I revisit the design instead of adding another patch. I keep decisions and evidence in the repository so a later session can pick up the work. Experimental ideas go through isolated trials and comparison with a baseline before they enter the application.

I prefer local storage for private state and operator decisions. Remote execution has to carry explicit scope and leave a record of what ran. These choices are visible in RepoPact, Fabric, ForgeLink, and ForgeWire, though each project is at a different stage.

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

- [SCOUT-2](https://github.com/ForgeWireLabs/SCOUT-2): *Historical.* Multi-agent assistant platform; a record of experiments, communication tools, agent patterns, and architectural limits that led to ForgeWire, ForgeLink, and later infrastructure.
- Earlier public projects (**SCOUT**, **Feed-Portal**, **MED.I.C.**) are *archived* and kept for history: not current work.

---

<!-- TODO (headshot: on you): once you add assets/headshot.jpg, uncomment the block below.
<img src="assets/headshot.jpg" align="right" width="180" alt="Jeremy Shows" />
-->

<!-- TODO (writing): drafts live in writing/. Once finalized, uncomment to surface them.
## Writing

- **Agentic systems are systems first and models second**: reliability lives in the assembly, not the component.
- **Why coding agents need repository-native governance**: binding invariants and durable state in the repo.
- **Remote agents without surrendering execution control**: signed dispatch, scope-bound tokens, audited runs.
- **Human attention is infrastructure**: why agent systems need private communication boundaries.
- **Building serious AI infrastructure on constrained hardware**: constraints as a design input.
- **What failed between SCOUT and ForgeWire**: the lineage read as corrected structural failures.

---
-->

**Independent, founder-led engineering with substantial AI assistance.** Reach me through the repositories above, or open an issue/security advisory on the relevant public project.
