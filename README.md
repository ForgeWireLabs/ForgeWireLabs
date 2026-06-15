# ForgeWire Labs

**Independent engineering and applied AI research focused on capable, constrained, and user-owned systems.**

ForgeWire Labs is an independent engineering and applied AI research lab founded by **Jeremy Shows**.

I build systems around a simple question:

> How capable can AI-assisted software become while remaining constrained, inspectable, user-owned, and useful on real hardware?

ForgeWire began as an attempt to build a better personal AI system. It has since grown into a modular architecture for coordinating models, agents, tools, memory, knowledge, compute, and remote execution without surrendering control to a hosted platform.

The work combines production engineering with longer-term research into recurrent reasoning, continual learning, adaptive routing, persistent agency, distributed coordination, and human-directed automation.

**ForgeWire Labs is where those ideas become working systems.**

---

## The ForgeWire Thesis

AI systems should not require users to surrender their data, infrastructure, or authority in exchange for capability.

They should be able to:

* run across hardware the user controls
* operate within explicit permissions and policy boundaries
* preserve useful state without creating opaque dependencies
* coordinate models, tools, services, and machines
* expose what they did and why
* degrade gracefully under limited compute or connectivity
* improve through measured, testable changes
* keep consequential decisions under human authority

ForgeWire is built around **usefulness under constraint**.

The objective is not unrestricted autonomy. It is dependable capability: systems that can perform meaningful work while remaining bounded, observable, and accountable.

---

## What ForgeWire Is

ForgeWire is a local-first architecture for building and operating AI-assisted systems.

It brings together:

* model and provider coordination
* agents, tools, and skills
* memory and knowledge systems
* authenticated task dispatch
* capability-scoped execution
* policy-gated automation
* structured event transport
* distributed compute
* evaluation and replay
* desktop applications
* repo-native operational memory
* human oversight and intervention

ForgeWire is not a single chatbot, model wrapper, or agent framework. It is an evolving systems architecture for connecting intelligence, execution, state, and control.

The private ForgeWire monorepo is the primary integration environment. Stable components and products are released publicly as their boundaries, documentation, tests, and security models mature.

---

## Architecture

The ForgeWire ecosystem is divided into specialized but interoperable layers.

### ForgeCore

The local coordination and intelligence layer.

ForgeCore is responsible for bringing together models, providers, tools, skills, memory, knowledge, routing, and task-local control. Its purpose is to support useful AI-assisted workflows without tying the system to one model vendor or one execution environment.

### ForgeWire Fabric

The distributed execution and control-plane layer.

Fabric coordinates authenticated work across machines through signed dispatch envelopes, constrained capabilities, policy-aware runners, structured events, and auditable execution records.

It extends ForgeWire beyond a single machine without treating remote execution as implicit trust.

### ForgeWire Bus

The communication substrate connecting components and services.

The Bus provides structured event transport, persistence boundaries, and integration paths for local and distributed workflows.

### ForgeWire Loom

The orchestration layer for coordinating runners, services, and execution environments across the ForgeWire system.

### Knowledge, Memory, and Evaluation

ForgeWire treats memory, retrieval, replay, and evaluation as architectural concerns rather than optional chatbot features.

The system is being developed to support:

* durable and inspectable state
* provenance-aware retrieval
* task-local checkpoints
* privacy-conscious telemetry
* reproducible evaluation
* bounded replay
* measurable routing and fusion behavior

---

## Public Projects

### [ForgeWire Fabric](https://github.com/ForgeWireLabs/forgewire-fabric)

A self-hosted control plane for trusted remote task execution.

Fabric focuses on:

* authenticated task dispatch
* signed execution envelopes
* scope-bound capabilities
* policy-gated runners
* structured event streams
* auditable coordination
* federated transport
* Python and Rust implementation parity
* integration with agent and developer tooling

Fabric is one public component of the larger ForgeWire architecture, not the entirety of ForgeWire itself.

### [SkillForge Academy](https://github.com/ForgeWireLabs/skillforge-academy)

An offline-first certification learning and exam-preparation platform.

The first curriculum targets CompTIA A+ and includes:

* structured certification objectives
* original practice questions
* performance-based questions
* mock examinations
* flashcards and spaced repetition
* readiness analytics
* notes and search
* local progress storage
* encrypted backups

SkillForge Academy applies the same principles as ForgeWire in a different domain: useful software, local ownership, offline capability, transparent progress, and accessibility to people working with limited resources or unreliable connectivity.

### [SCOUT-2](https://github.com/ForgeWireLabs/SCOUT-2)

An earlier multi-agent assistant platform and an important part of ForgeWire's engineering lineage.

SCOUT explored provider coordination, personas, tools, retrieval, speech, background services, message transport, and desktop AI interaction. Its successes and failures helped expose the architectural problems that ForgeWire was later built to address.

SCOUT-2 remains public as a record of that evolution.

---

## Research Directions

ForgeWire Labs explores ideas that may eventually improve the production architecture, but experimental work is not presented as finished capability.

Research must earn its way into the system through implementation, measurement, replay, and controlled integration.

### Recurrent Cognitive Control

Investigating bounded recurrent processing that allows a system to revisit, compare, refine, and evaluate intermediate work without requiring unrestricted agent loops.

Current interests include:

* task-local recurrent state
* bounded reasoning passes
* confidence and drift signals
* controlled route histories
* checkpointed execution
* observe-only controllers
* measurable stopping conditions
* constrained adaptive behavior

### Continual Learning

Exploring how systems can incorporate useful experience without uncontrolled model drift or catastrophic forgetting.

This includes work related to:

* specialist routing
* replay and evaluation
* adaptive caches
* confuser-focused training
* calibrated fusion
* provenance-preserving updates
* function-preserving growth

### Routing and Fusion

Earlier HCDM research produced two continuing architectural lines:

* **Ariadne**, focused on routing information or tasks among specialized paths
* **Centrifuse**, focused on calibrated comparison and fusion of multiple outputs

These ideas inform later work in orchestration, recurrent control, evaluation, and model coordination.

### Hybrid Cognitive Systems

Exploring cooperation between small language models and dense state-oriented models operating across compatible representational spaces.

The goal is not to imitate biological systems literally. It is to investigate whether complementary models can combine semantic reasoning, persistent state, efficient recurrence, and continual adaptation on modest hardware.

### Temporal Continuity

The TC/TCI/TIC research line examines distinctions between:

* continuity of information
* continuity of agency
* continuity of subjectivity

This work provides a conceptual framework for discussing persistent AI systems without casually equating memory, autonomy, agency, and consciousness.

ForgeWire does not make consciousness or sentience claims. The purpose of this research is to develop better vocabulary, architecture, and ethical boundaries for systems that maintain state and act across time.

---

## How I Build

ForgeWire Labs follows several working principles:

* **Build before claiming.** Ideas should become testable systems.
* **Constrain consequential action.** Capability should not imply unrestricted authority.
* **Make execution inspectable.** Important actions need provenance, events, and audit trails.
* **Preserve user ownership.** Local operation and data control are architectural priorities.
* **Design for real hardware.** Useful systems should not require unlimited compute.
* **Measure experimental changes.** Research components need baselines, evaluation, and rollback paths.
* **Promote cautiously.** Experimental work enters production only after its behavior is understood.
* **Learn from failure.** Abandoned experiments can still produce valuable components and better questions.
* **Keep humans in control.** Automation should extend human capability rather than obscure responsibility.

Agents inside ForgeWire are treated as constrained participants in a larger system, not as magic and not as inherently trustworthy actors.

---

## About Jeremy

I am a self-taught engineer and independent researcher with a background spanning mechanical work, race-car fabrication, construction, small-business ownership, and information technology.

That history shapes how I approach software.

I tend to see AI systems as machinery: assemblies of components with interfaces, tolerances, failure modes, feedback loops, and operational limits. A convincing demonstration is not enough. The system must still work when the network is unreliable, the hardware is limited, a component fails, or an automated process exceeds its authority.

My work now crosses:

* distributed systems
* AI and agent infrastructure
* applied machine learning
* developer tooling
* desktop software
* technical education
* cognitive architecture
* neuroscience-inspired computation
* security and policy boundaries
* evaluation and automation

ForgeWire Labs is both an engineering effort and a long-running investigation into how these disciplines fit together.

---

## Evolution

The work did not begin with ForgeWire.

It developed through several generations of assistants, automation experiments, model-routing systems, communication layers, and cognitive architecture research.

The broad lineage is:

**SCOUT → ATLAS → PhrenForge → ForgeWire**

Each generation revealed limitations in the previous one:

* monolithic assistants gave way to modular services
* implicit coordination gave way to structured events
* broad agent permissions gave way to scoped capabilities
* single-machine assumptions gave way to authenticated distributed execution
* ad hoc prompts gave way to repo-native memory, policy, and operational state
* speculative cognitive ideas gave way to gated experimental programs

ForgeWire is the current synthesis of that work.

---

## Development Model

ForgeWire is developed as an integrated private system, while mature components are prepared for public release.

Public releases are intended to include enough context to be evaluated seriously:

* architectural documentation
* tests and validation
* security boundaries
* changelogs
* operational guidance
* known limitations
* clear separation between production and experimental work

### Current Public Focus

* **ForgeWire Fabric:** public mirror, validation, and documentation hardening
* **SkillForge Academy:** certification-learning desktop application
* **SCOUT-2:** historical foundation and architectural lineage

### Active Private Work

* ForgeWire core integration
* Fabric control-plane development
* knowledge and memory productization
* evaluation and benchmarking
* recurrent cognitive control planning
* routing, fusion, and continual-learning experiments

---

## Technical Foundation

ForgeWire Labs currently works primarily with:

**Rust · Python · TypeScript · React · Tauri · SQLite · rqlite · PowerShell · GitHub Actions**

The technology is selected according to the role it serves. ForgeWire is not organized around promoting a particular language, framework, model provider, or cloud platform.

---

## Current Status

ForgeWire Labs is an independent, founder-led lab under active development.

Some systems are public. Some remain private while their architecture and release boundaries are stabilized. Experimental research is identified separately from production capability.

The work is ambitious, but the standard remains practical:

> Build systems that are useful, testable, inspectable, and worthy of trust.
