# Why coding agents need repository-native governance

*Draft — Jeremy Shows, ForgeWire Labs*

A coding agent rarely fails because it cannot write code. Modern models write
code well. It fails because the things that should constrain and inform the
change — the intent behind the project, who is allowed to touch what, the
decisions already made and why, the evidence that something actually works — live
somewhere the agent cannot reliably see. They live in a previous conversation, a
closed tab, a teammate's head, a Slack thread from three weeks ago. So the agent
does the locally reasonable thing, which is frequently the globally wrong thing,
and it does it with complete confidence.

The usual response is to write a longer prompt. Better instructions, more
context pasted in, a bigger system message. This treats a *state* problem as a
*phrasing* problem, and it does not survive contact with a second session. The
moment the conversation resets — new agent, new model, new day — the carefully
assembled context is gone, and you are reconstructing it by hand.

## Conventions capture fragments, not the binding part

We already have partial answers. `AGENTS.md` files put instructions near the
code. Architecture decision records capture why a choice was made. Issue trackers
hold work. Each of these captures a fragment of project knowledge. None of them
makes the *binding* part explicit — the guarantees an agent must not silently
weaken.

That gap is the whole problem. "Prefer composition over inheritance" is advice;
an agent can reasonably override it. "This module must never make a network call
during import" is an invariant; an agent that overrides it has broken the system,
even if the code compiles and the tests it bothered to run pass. The difference
between advice and invariant is not tone. It is whether violating it requires
escalation to a human. A folder convention has no way to express that. A contract
does.

## Make the repository the pact

The wedge I keep returning to is the **binding invariant**: a declared guarantee,
with a rationale, an escalation path, and — where possible — a machine enforcer.
Around that, a small set of primitives turns a folder of conventions into
something an agent can actually be held to:

- **Charter and invariants.** The project thesis, and the guarantees that must
  not be quietly weakened. Judgment and law, kept separate.
- **Scopes and roles.** Layered instructions located next to the code they
  govern, plus an explicit map of who — human or agent — may change what.
- **A frozen surface.** Paths and symbols that require operator approval to
  touch, enforced rather than requested.
- **Work items.** A narrative plan paired with machine-readable state, with
  acceptance criteria that are linked to evidence rather than asserted.
- **Evidence.** Immutable run records tied to the criteria they satisfy, so
  "done" means "demonstrated," not "claimed."
- **Reconciliation.** Audits that compare the declared architecture against what
  the repository actually contains, because drift is silent until you look.

The point of all of this is not ceremony. It is that a new contributor — human or
agent — can walk into the repository cold and recover the operational state of the
project: what it is for, what they may change, what has already been decided, what
counts as proof, and where the edges are. Without depending on a prior
conversation that no longer exists.

## Why the repository, specifically

Because the repository is the one artifact that survives. Conversations end.
Tools change. The model you used last month is deprecated this month. The git
history, the files, the directory structure — those persist, get cloned, get
reviewed, outlive every session. If the governing context lives anywhere else, it
is one tab-close away from gone. If it lives in the repository, it travels with
the work by construction.

There is a second-order effect that matters more than it first appears: durable
state moves *with* the work item. When a task is blocked, deferred, or completed,
its reasoning and evidence move with it instead of collapsing into a one-line
summary. History stops being a changelog and starts being a record you can
actually reconstruct decisions from.

The long-term goal is not better prompting. It is durable coordination between
people and agents across sessions, tools, models, and project lifetimes — the
kind of coordination that does not evaporate the moment someone closes a window.
The repository is already the contract everyone agrees to work against. Governance
should live there too.
