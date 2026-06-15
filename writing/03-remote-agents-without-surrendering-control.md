# Remote agents without surrendering execution control

*Jeremy Shows, ForgeWire Labs*

The moment an agent becomes useful, you start wanting it to run somewhere other than your laptop. A local coding agent can do serious work, but its operational reach ends at the machine in front of you. The next class of work begins when it can reach the GPU box, the build host, the lab server, or the always-on desktop in the next room, the machines you actually own and operate. That reach creates the value, and it is also where many setups quietly give away control.

The default path to "agent runs on a remote machine" is depressingly common: a shared SSH key, distributed across whatever needs to connect and granting broad shell access to anything holding it. It works on the first afternoon and becomes a standing liability afterward. In its typical blanket-access configuration, it provides no per-task authority, no structured record of what ran, no way to make one machine eligible for some work but not other work, and no meaningful boundary an automated process cannot cross. You have traded control for convenience, and you usually do not notice until you need the control back.

## Separate the right to ask from the right to run

The fix starts with a distinction that broad shell access erases: the surface that *dispatches* work and the machine that *executes* it are different trust domains, and they should be treated that way.

A dispatch surface, whether a CLI, an editor extension, an MCP-speaking agent, or a CI job, should be able to *ask* for work to happen. It should not, by virtue of asking, be able to do anything it wants on the remote machine. The machine that runs the work should accept it only when the work is something it is eligible to run and the request carries authority it can verify.

Concretely, that means a few properties that blanket shell access does not provide by default:

* **Signed work, not trusted callers.** Each task enters as a signed envelope. The runner verifies the signature, not merely the network position of whoever sent it.
* **Scope-bound capability tokens.** Authority is narrow and attached to the work: this scope, these capabilities, this kind of task. It is not a blanket grant that outlives any single job.
* **Eligibility at the claim.** A runner claims only work it is allowed to claim. The eligibility check lives in the claim path and is enforced by the system, not by everyone agreeing to behave.
* **Policy gates before and during execution.** Authorization is not a one-time check at the door. Policy runs before the work starts and continues to apply while it runs.
* **A hash-chained audit record.** Every run leaves evidence that can explain what happened afterward: inputs, outputs, cost, and a tamper-evident chain that makes later alteration detectable.

## Self-hosted is a control decision, not a nostalgia one

There is a reflex to reach for a hosted control plane, and for plenty of teams that is the right call. But notice what you are deciding when you do: a third party now mediates which of your machines runs what and holds the record of it. For some work, that is fine. For work where the machines are yours, the data is yours, and the audit trail is the thing you will be asked to produce later, keeping the control plane self-hosted is not sentimentality. It keeps the parts of the system you are accountable for inside your own boundary.

"Your infrastructure, your rules, your audit trail" is a posture, and it costs something to hold: you run the hub, you manage the tokens, and you own the uptime. What you get back is direct custody of execution authorization and audit history. Neither has to depend on an external control-plane operator or disappear during someone else's outage.

## Two kinds of remote work

One more distinction earns its keep in practice: sending intent to a remote *agent* is not the same as controlling a remote *host*. When you dispatch to an agent, the runner is the agent. It advertises its tools and skills, and you route work by capability. When you control a host, the runner is a shell executor with no model in the loop, and you want live stdin, stdout, and process control. These are different trust models and different claim paths. Collapsing them into one "just give it a shell" abstraction is exactly how control leaks out.

A runner's role should be a property of the binary it runs, not a configuration flag that an attacker or a confused agent can flip. An execution-only runner should never be able to claim agent work, and an agent runner should never be able to claim host-control work. The boundary should be enforced where the work is claimed.

None of this makes remote execution harder to *use*. It makes it harder to *lose control of*, which is the only version worth building. You can have agents that reach every machine you own and still be able to say precisely what each one is allowed to do and what each one actually did. That sentence is the whole goal.
