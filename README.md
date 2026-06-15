# ForgeWire Labs

**Independent engineering, applied AI research, and practical software built for the real world.**

ForgeWire Labs is the independent lab of **Jeremy Shows**.

I design and build systems across agent infrastructure, distributed computing, applied machine learning, developer tooling, cognitive architecture, repository-native governance, and technical education.

My work is driven by a practical question:

> How do we turn ambitious ideas about intelligence, automation, and learning into systems that remain useful when models are fallible, hardware is limited, infrastructure changes, and real people depend on the result?

ForgeWire Labs is not centered on a single application. It is the home for a growing body of engineering, products, experiments, and research developed through years of building, testing, failure, and reconstruction.

The work ranges from production-oriented infrastructure to experimental model architectures, but the standard remains the same:

**Build it. Test it. Understand its limits. Make it useful.**

---

## What I Work On

ForgeWire Labs works across several connected areas.

### Agentic Systems

Infrastructure for coordinating models, agents, tools, memory, knowledge, compute, and human authority as parts of a complete system.

This includes:

* agent and tool orchestration
* task decomposition and execution
* policy and capability boundaries
* memory and knowledge systems
* local and distributed compute
* structured events and messaging
* evaluation, replay, and recovery

### Repository-Native Governance

Systems for preserving authority, intent, work state, decisions, evidence, and project history inside the repository.

This work explores how humans and coding agents can coordinate across sessions without depending on one model, one tool, or a disappearing conversation history.

It includes:

* scoped instructions and ownership
* durable work items
* acceptance criteria
* validation evidence
* architectural decision records
* protected surfaces
* audits and reconciliation
* human escalation boundaries

### Applied AI Research

Experimental work investigating how intelligent systems can reason, adapt, specialize, preserve useful state, and operate across time.

Current and continuing research interests include:

* recurrent reasoning
* continual learning
* adaptive routing
* calibrated fusion
* small and hybrid model systems
* cognitive control
* persistent agency
* temporal continuity
* neuroscience-inspired computation

### Practical Software

Products that apply the same engineering discipline outside AI infrastructure.

These projects emphasize useful workflows, clear ownership, offline capability where appropriate, and software that works under ordinary constraints rather than ideal conditions.

### Technical Education

Tools that make technical knowledge more structured, measurable, and accessible.

The goal is not simply to present information, but to help people develop demonstrable capability.

---

## Selected Work

### [ForgeWire](https://github.com/ForgeWireLabs/ForgeWire-Overview) · Coming Soon

ForgeWire is an unreleased modular system for coordinating models, agents, tools, memory, knowledge, compute, and distributed execution.

It began as a personal AI assistant and evolved through several generations into a much broader architecture for intelligent work.

Its central engineering thesis is:

> **Agentic systems are systems first and models second.**

A capable model can still be part of an unreliable system. ForgeWire therefore focuses on the infrastructure surrounding models: graceful degradation, explicit ownership, behavioral parity, audit trails, recoverable execution, bounded authority, and replaceable components.

ForgeWire remains under active private development. Its public overview documents the system's direction, history, and release status without presenting unfinished work as an available product.

### [ForgeWire Fabric](https://github.com/ForgeWireLabs/forgewire-fabric)

ForgeWire Fabric is a self-hosted control plane for authenticated remote task execution.

Fabric provides infrastructure for moving work across machines while preserving explicit authority, policy, provenance, and execution history.

Its engineering areas include:

* signed task dispatch
* scope-bound capabilities
* policy-gated runners
* structured task events
* distributed persistence
* audit and replay
* federated transport
* Python and Rust behavioral parity
* integration with agent and developer tooling

Fabric is publicly available as an independent infrastructure project and as one component of the future ForgeWire system.

### [RepoPact](https://github.com/ForgeWireLabs/repopact)

RepoPact is a repository-native operating system for durable work between humans and coding agents.

It extracts and formalizes governance patterns developed through ForgeWire: keeping authority, intent, work state, evidence, architectural decisions, and project history inside the repository rather than allowing them to disappear with each agent session.

Its core loop is:

```text
intent -> scoped authority -> work item -> implementation -> evidence -> audit -> history
```

RepoPact is organized around five primitives:

* **Charter:** the project thesis and governing invariants
* **Scopes:** layered instructions located near the code they govern
* **Work items:** narrative plans paired with machine-readable state
* **Evidence:** immutable validation records linked to acceptance criteria
* **Reconciliation:** audits comparing declared architecture with repository reality

Work moves through explicit filesystem states such as active, blocked, deferred, and completed. Its reasoning, decisions, and evidence move with it, preserving history rather than reducing completed work to a summary.

RepoPact grew from the governance and agent-coordination system built inside ForgeWire, but it is being developed as an independent, reusable project. Its purpose is to let a new human or agent recover the operational state of a repository without depending on an earlier conversation.

The project is still young. Its continuing direction includes stronger binding invariants and escalation rules, distinct roles and ownership scopes, protected surfaces, durable architectural decisions, and safe coordination among concurrent agents.

### [SkillForge Academy](https://github.com/ForgeWireLabs/skillforge-academy)

SkillForge Academy is an offline-capable certification learning and exam-preparation platform.

Its first learning track targets CompTIA A+ and is being designed around:

* structured certification objectives
* original practice questions
* performance-based questions
* mock examinations
* flashcards and spaced repetition
* readiness analytics
* notes and search
* local progress storage
* encrypted backups

SkillForge Academy is not a ForgeWire subsystem. It is a ForgeWire Labs product focused on helping people build and measure practical technical knowledge.

### [SCOUT-2](https://github.com/ForgeWireLabs/SCOUT-2)

SCOUT-2 is an earlier multi-agent assistant platform and an important part of my engineering history.

It explored provider coordination, personas, tools, retrieval, speech, background work, messaging, and desktop AI interaction.

SCOUT-2 remains public as a record of the experiments, successes, and architectural limitations that eventually led to ForgeWire.

---

## Research

ForgeWire Labs provides a home for research that may inform future systems without being prematurely presented as production capability.

### Routing and Fusion

ForgeWire Labs explores how intelligent systems can divide work among specialized processing paths and combine their outputs without assuming that one model, one route, or simple agreement is necessarily correct.

Routing research examines questions such as:

* how inputs should be directed among specialists
* how a system can recognize ambiguity or unfamiliar examples
* when multiple processing paths should be consulted
* how routing confidence should be measured
* how specialist overlap and disagreement should be handled
* how routing decisions can adapt without becoming unstable
* how route histories can support evaluation and replay
* how limited compute should be allocated among competing paths

Fusion research examines how multiple candidate outputs can be evaluated, calibrated, and combined.

This includes:

* confidence calibration
* weighted output combination
* disagreement analysis
* specialist reliability tracking
* uncertainty-aware selection
* comparison against strong baselines
* replay of routing and fusion decisions
* detection of cases where consensus may still be wrong
* preservation of provenance through the final result

The objective is not to create unnecessary collections of models. It is to determine when specialization provides measurable value and how that value can be used without hiding uncertainty or weakening accountability.

This work informs broader research involving orchestration, recurrent control, continual learning, specialist systems, evaluation, replay, and hybrid model coordination.

### Recurrent and Hybrid Systems

Current experiments investigate whether small complementary models can combine:

* semantic reasoning
* dense state representation
* recurrent processing
* persistent task state
* continual adaptation
* efficient operation on modest hardware

Biological systems can provide useful questions and structural analogies, but they are not treated as proof that an artificial implementation will behave in the same way.

### From Research to Engineering

Experimental ideas do not become production components merely because they are interesting.

Research is expected to pass through stages such as:

1. conceptual framing
2. isolated implementation
3. baseline comparison
4. controlled evaluation
5. failure analysis
6. observe-only integration
7. limited canary deployment
8. production gating

Research can also succeed by producing a better question, clearer boundary, useful measurement, or reusable component. It does not have to become a product feature.

---

## How I Build

My engineering approach is shaped by several recurring principles.

### Systems Before Components

The behavior of the complete system matters more than the apparent intelligence or performance of one part.

### Real Conditions Matter

A successful demonstration is only a beginning. Software must survive missing dependencies, partial failures, limited hardware, provider changes, invalid outputs, and evolving requirements.

### Authority Must Be Explicit

An agent's ability to perform an action does not automatically give it permission to do so.

Authority should be defined by scope, ownership, policy, and human intent rather than inferred from technical capability.

### Important Behavior Must Be Inspectable

Execution state, decisions, failures, and outcomes should leave enough evidence to be understood and reconstructed.

### Components Should Remain Replaceable

Models, providers, runtimes, transports, databases, and accelerators are implementation choices. None should become the identity of the whole system.

### Research Must Earn Integration

Experimental work remains separate until it demonstrates value without weakening established operational guarantees.

### Failure Is Useful Evidence

Abandoned systems and unsuccessful experiments are not erased from the history. They often reveal the constraint or architectural boundary that the next system needs.

### History Should Survive the Session

Project knowledge should not disappear when a conversation ends, a contributor leaves, or a model is replaced.

Intent, decisions, evidence, and unresolved work should remain recoverable from the project itself.

---

## Repository-Native Agent Work

A coding agent rarely fails only because it cannot write code. It also fails because earlier intent, authority, decisions, evidence, and project state are missing or scattered across conversations.

ForgeWire Labs treats the repository itself as part of the operating environment for agent-assisted development.

ForgeWire developed a layered system of:

* scoped agent instructions
* ownership boundaries
* roadmaps and durable work items
* architecture records
* validation evidence
* audits and reconciliation
* repository-native project memory
* escalation to human authority

These structures allow agents to recover context, understand what they may change, perform bounded work, validate results, preserve history, and escalate decisions beyond their authority.

[RepoPact](https://github.com/ForgeWireLabs/repopact) extracts and formalizes this approach as an independent project so it can be applied beyond ForgeWire.

The long-term objective is not merely better prompting. It is durable coordination between people and agents across sessions, tools, models, and project lifetimes.

---

## Evolution

The work behind ForgeWire Labs did not begin with its current name.

A broad part of its agent-system lineage is:

**SCOUT → SCOUT-2 → SCOUT-3 → ATLAS → PhrenForge → ForgeWire**

Across those generations:

* monolithic assistants became modular services
* prompts became personas, tools, skills, and permissions
* implicit coordination became structured events
* direct execution gained policy and capability boundaries
* single-machine assumptions expanded into authenticated distributed work
* acceleration paths gained portable parity implementations
* scattered project context became repository-native memory and governance
* speculative cognitive ideas became gated research programs
* model-centered development became systems-first engineering

RepoPact represents a second kind of evolution: an internal operating method extracted from ForgeWire and rebuilt as an independent project.

ForgeWire Labs provides an identity under which products, infrastructure, research, governance systems, and experiments can develop without all becoming parts of one application.

---

## About Jeremy

I am a self-taught engineer and independent researcher with a background spanning military (63W), mechanics, electrical systems, low-level hardware repair, systems design and infrastructure builds, race-car engineering, fabrication, construction, small-business ownership, and information technology.

That history shapes how I approach software.

I tend to see AI systems as machinery: assemblies of components with interfaces, tolerances, failure modes, feedback paths, and operational limits.

A convincing demonstration is not enough. The system must still work when a component fails, hardware is constrained, requirements change, or an automated process exceeds its authority.

My work now crosses:

* distributed systems
* agent infrastructure
* applied machine learning
* repository-native governance
* developer tooling
* desktop applications
* technical education
* cognitive architecture
* neuroscience-inspired computation
* security and policy boundaries
* evaluation and automation

I did not arrive here through a single academic discipline or a conventional software career.

ForgeWire Labs grew from repeatedly learning what was necessary to build the next part, testing it, discovering where it failed, and rebuilding it with a better understanding of the problem.

---

## Current Direction

ForgeWire Labs is an independent, founder-led lab under active development.

### Public Work

* **ForgeWire Fabric:** distributed task execution and control-plane infrastructure
* **RepoPact:** repository-native governance and durable human-agent coordination
* **SkillForge Academy:** certification learning and exam preparation
* **SCOUT-2:** historical multi-agent platform
* **ForgeWire Overview:** public documentation for the unreleased ForgeWire system

### Private Development

* ForgeWire system integration
* portable and accelerated execution substrates
* knowledge and memory systems
* agent-assisted repository operations
* evaluation and benchmarking
* recurrent cognitive control
* routing, fusion, and continual-learning experiments

Public releases are prepared with enough documentation, testing, security context, known limitations, and architectural explanation to be evaluated seriously.

---

## Technical Foundation

Current work primarily uses:

**Rust · Python · TypeScript · React · Tauri · GTK · SQLite · rqlite · PostgreSQL · PowerShell · GitHub Actions**

Technologies are selected for the roles they serve.

ForgeWire Labs is not defined by one language, framework, model provider, database, accelerator, or cloud platform.

---

> Build the whole system. Test it under failure. Preserve the evidence. Understand its limits. Then determine whether it is useful.
