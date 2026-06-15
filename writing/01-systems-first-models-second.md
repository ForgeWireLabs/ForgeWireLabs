# Agentic systems are systems first and models second

*Jeremy Shows, ForgeWire Labs*

A model demo is a closed-loop highlight reel. You give it a clean prompt, it produces a clean answer, everyone nods. Then you wire that same model into something real, a pipeline that runs unattended, touches a filesystem, calls a tool, and feeds the next step, and the highlight reel stops mattering. What matters now is what happens on the bad path: the malformed output, the tool that times out, the step that ran twice, the authority the model quietly exceeded.

I came to software from machinery, engines, electrical systems, fabrication. In that world you learn early that a part passing on the bench tells you almost nothing. The question is always *what happens to the rest of the assembly when this part fails*, because parts fail. A system is the answer to that question. An agentic system is no different. The model is one component with an interface, a tolerance band, and a set of failure modes. Treating it as the system is a category error, and it is the most common one I see.

## The model is the easy part to replace

Here is the uncomfortable truth for anyone building on top of a frontier model: the model is the part of your system most likely to change and least under your control. Providers deprecate versions. Prices move. A better model ships and you want to switch. If your system is *built around* a specific model's behavior, its quirks, its prompt format, its exact output shape, then every one of those changes is a rebuild.

So the durable engineering is not in the model. It is in everything around it:

* **Graceful degradation.** When the model is slow, wrong, or unavailable, the system should do something defined, fall back, retry with a budget, escalate to a human, not collapse.
* **Explicit ownership.** Every action an agent takes should map to an authority it was actually granted. "The model decided to" is not an authorization model.
* **Behavioral parity.** If you have more than one implementation of a path, a fast one and a portable one, say, they must agree, and you must be able to prove it. Otherwise you have two systems pretending to be one.
* **Recoverable execution.** You should be able to replay what happened, not reconstruct it from memory and a disappearing chat log.
* **Bounded authority.** An automated process that can exceed its mandate will, eventually, exceed its mandate. The boundary has to be enforced by the system, not requested in a prompt.
* **Replaceable components.** The model included. If swapping it is a rewrite, you built a monolith with extra steps.

## Capability, not reliability, is the trap

A more capable model makes this *harder* to see, not easier, because it pushes the failure rate low enough to ignore, until the system is doing enough volume that "low enough to ignore" is a daily incident. The reliability of the whole is not the reliability of the model. It is the reliability of the model constrained by every interface, dependency, and unguarded failure path around it. You can keep improving the component and still ship an unreliable system if you never strengthen the assembly.

This is why I keep coming back to the same framing: **a capable model can still be part of an unreliable system.** The capability lives in the component. The reliability lives in the assembly. They are different engineering problems and they want different attention.

## What this looks like in practice

It looks boring, which is the point. It looks like signed work envelopes instead of trust-by-default. It looks like a runner that can only claim work it is eligible for, checked at the claim, not requested by convention. It looks like a policy gate that runs before *and during* execution, and a hash-chained record that can explain a run after the fact. None of that is model work. All of it is what decides whether the model's output is something you can stand behind.

When I build, I design for the model to be added late and replaced early. I define the interfaces, failure modes, authority boundaries, and recovery paths before I tune a single prompt. Then I treat the model as what it is: a strong, fallible component I will almost certainly replace, plugged into a system built to outlive it.

Build the whole system. Test it under failure. Preserve the evidence. The model is the part everyone watches. The system is the part that has to work.

