# First Principles Thinking — Reference

A dense reference for reasoning from fundamental truths rather than analogy. Compiled for use as a thinking partner skill.

## Table of Contents

1. What First Principles Thinking Actually Is
2. Musk's Specific Framework (battery pack, rockets, the formal procedure)
3. The Procedural Method — Step by Step
4. Common Traps
5. Adjacent Thinkers and Frameworks (Aristotle, Feynman, Bezos, Munger, others)
6. Application Examples (software, business, personal, engineering)
7. When to Use This (and When Not To)
8. Self-Check Protocol

---

## 1. What First Principles Thinking Actually Is

### The definition

First principles thinking is the practice of decomposing a problem to its irreducible, demonstrably true components — physical laws, mathematical identities, definitional truths, verifiable economic facts — and reconstructing a solution from those components without inheriting assumptions from how the problem is currently solved.

A "first principle" is a foundational proposition that cannot be deduced from any other proposition. It is bedrock. Everything else is built on top of it.

### Musk's own framing

> "I think it is important to reason from first principles rather than by analogy. The normal way we conduct our lives is we reason by analogy. We are doing this because it's like something else that was done, or it is like what other people are doing. With first principles you boil things down to the most fundamental truths and say, 'okay, what are we sure is true?' and then reason up from there." — Elon Musk, TED interview with Chris Anderson, 2013

The procedure has two phases: **destruction** (decomposing the inherited answer down to physics, math, or definitional truths) and **reconstruction** (rebuilding upward without re-importing the assumptions you just stripped out).

### Reasoning by analogy — the default

Analogical reasoning says: *X is like Y, and Y works this way, so X should work this way too.* It is fast, cheap, socially defensible, and usually correct enough. It is how humans run 95%+ of their cognition because evaluating every decision from physics would be paralysing.

Analogy fails specifically when:
- The reference class (Y) is itself a product of historical accident, not optimisation
- The constraints that made Y the right answer have changed (technology, cost curves, regulation)
- "Everyone does it this way" is mistaken for "this is the way it must be done"
- The analogy is load-bearing for a high-stakes decision (capital allocation, architectural choices, life direction)

The danger of analogy is that it **inherits the assumptions of the reference case silently**. You don't see what you've assumed because you didn't choose to assume it — you imported it.

### Why first principles is rare

It is expensive. Decomposing to physics takes time, domain knowledge, and tolerance for looking stupid while you ask "but *why* does it cost that much?" five layers down. Most people, most of the time, cannot afford the cognitive overhead. The skill is knowing **when** the overhead is worth paying — usually when the decision is large, irreversible, or when the inherited answer feels suspiciously expensive, slow, or arbitrary.

---

## 2. Musk's Specific Framework

### The battery pack example (canonical)

The most-cited illustration of Musk's method, in his own words:

> "Somebody could say battery packs are really expensive and that's just the way they will always be. Historically it has cost $600 per kilowatt hour, and so it's not going to be much better than that in the future. You say, no, what are the material constituents of the batteries? What is the spot market value of the material constituents? It's got cobalt, nickel, aluminium, carbon, and some polymers for separation, and a steel can. So break that down on a material basis, if we bought that on the London Metal Exchange, what would each of these things cost? Like, oh jeez, it's $80 per kilowatt hour. So clearly you just need to think of clever ways to take those materials and combine them into the shape of a battery cell, and you can have batteries that are much, much cheaper than anyone realises." — Elon Musk

The structure of this argument:
1. **Inherited claim:** Batteries cost $600/kWh and always will.
2. **Decomposition:** What is a battery, *physically*? Cobalt, nickel, aluminium, carbon, polymer separator, steel can.
3. **Re-pricing at the floor:** What do those materials cost on the open commodities market? ~$80/kWh.
4. **Identify the gap:** The remaining ~$520/kWh is process, manufacturing scale, margins, and engineering — *not physics*. Therefore it is attackable.
5. **Reconstruction:** Build a manufacturing process (Gigafactory, vertical integration, cell design) that closes the gap between physics floor and market price.

The critical move is step 4 — separating what is **physically required** from what is **historically contingent**. Physics is fixed. History is negotiable.

### Application to rockets (SpaceX origin)

The same procedure produced SpaceX:

> "I tend to approach things from a physics framework. Physics teaches you to reason from first principles rather than by analogy. So I said, okay, let's look at the first principles. What is a rocket made of? Aerospace-grade aluminium alloys, plus some titanium, copper, and carbon fibre. Then I asked, what is the value of those materials on the commodity market? It turned out that the materials cost of a rocket was around 2 percent of the typical price."

The inherited belief in 2002 was that orbital launch was inherently a $60M+ problem because that's what it had always cost. The other 98% turned out to be: expendability (throwing the vehicle away every flight), low launch cadence, cost-plus government contracting, and supply chains optimised for reliability over cost. **None of those are physics.** Reusability (Falcon 9 booster recovery) is the direct industrial consequence of this analysis.

### The mental procedure, formalised

1. **State the inherited price/timeline/constraint** plainly. ("X costs $Y." "X takes Z years.")
2. **Ask what X is made of, physically.** Materials, energy, time, information — the irreducible inputs.
3. **Price each input at its theoretical floor.** Commodity markets, energy in joules, information-theoretic limits.
4. **Compute the floor cost / time / size.**
5. **Identify the delta between floor and inherited.** This delta is where the opportunity lives — and where the inherited answer's hidden assumptions reside.
6. **Attack the delta** with engineering, process redesign, vertical integration, or volume.

This isn't only a cost framework. It works for time ("how long must this physically take?"), for size ("how small can this be?"), for energy ("what's the thermodynamic minimum?"), and for organisational design ("what does this team physically need to produce?").

---

## 3. The Procedural Method — Step by Step

A working protocol for actually applying this rather than just admiring it.

### Step 1 — Identify the assumption or conclusion under examination

Write the claim down in one sentence. Be specific. Vague claims cannot be decomposed.

- Bad: "Software is expensive."
- Good: "Building a CRM for our use case will cost £200k and take 9 months."

### Step 2 — Decompose to fundamental truths

Ask: *what is true here that cannot be otherwise?* Sort the inputs into three buckets:

- **Physical / mathematical truths.** Conservation of energy, speed of light, arithmetic, information theory limits. Non-negotiable.
- **Definitional truths.** What the thing *is* by definition. ("A CRM is a database with a UI for relationship records.")
- **Empirical / market truths.** What inputs cost on open markets, what time labour takes, what regulation requires.

Anything *not* in these three buckets is convention, precedent, or assumption — and is therefore in scope for challenge.

The key discipline: **keep asking "why" until the answer is physics, math, definition, or a verifiable price.** If the answer is "because that's how it's done" or "because [authority] says so," you have not decomposed — you have stopped early.

### Step 3 — Reconstruct from the truths

Build upward. Given only the items in your three buckets, what is the minimum viable solution?
- What does it physically need to do?
- What is the cheapest set of inputs that satisfies the physics / definition?
- What is the shortest path from inputs to output?

The output is a **floor estimate** — the theoretical minimum cost, time, or complexity. It will almost always be dramatically lower than the inherited number.

### Step 4 — Compare to the analogical answer

- **Gap is small (<2x):** The inherited answer is roughly physics-bound. Don't waste time attacking it.
- **Gap is large (5x+):** The inherited answer is loaded with historical assumption. There is real opportunity here.
- **Gap is enormous (10x+):** Either you've missed something in your decomposition, *or* this is a category-defining opportunity (Tesla, SpaceX scale).

### Step 5 — Stress-test your decomposition

- Have I confused convention with physics anywhere?
- Have I stopped decomposing too early on any input?
- Are there second-order costs I've omitted (regulation, integration, support, distribution)?
- Is there a reason — not yet visible to me — that the gap exists and persists despite many smart people knowing about it?

The last question is the most important. If you can't articulate why the gap has persisted (capital intensity, regulatory moat, requires unusual cross-domain expertise, low-status problem), your decomposition is probably wrong.

---

## 4. Common Traps

### Trap 1 — Stopping decomposition too early

The most common failure. You ask "why" three times, get an answer that sounds reasonable, and stop. But the real assumption is six layers down.

Symptom: your "fundamental truths" still contain words like "industry standard," "best practice," or "typically."

### Trap 2 — Mistaking convention for physics

Convention feels like physics from inside the convention. Test: ask "if this constraint disappeared tomorrow, what specifically would break?" If the answer is "the laws of physics would be violated," it's physics. If the answer is "people would have to change how they work" or "regulators would object" or "no one has ever done it that way," it's convention.

### Trap 3 — The "smart people" assumption

> "A lot of times people will think something can't be done. But if you really look at it from first principles, you see that it can be done. Often people will say something is impossible, and what they really mean is that it would be hard or that they don't want to do it." — Musk

Assuming "if it were possible, smart people would have done it" is itself analogical reasoning. Incumbents have sunk costs, internal politics, career incentives misaligned with experimentation, and acculturation that makes them blind to convention. First principles asks: *would they have, given their actual incentives and constraints?*

### Trap 4 — Confusing precedent with constraint

Precedent says "this has happened before." Constraint says "this must be true." Most "constraints" in business contexts are precedents wearing constraint costumes.

### Trap 5 — First-principles theatre

Performing the decomposition without doing it. Writing "materials," "labour," "energy" but never looking up actual prices. Invoking "physics" without computing anything.

Test: do you have numbers, with units, sourced from somewhere verifiable? If not, you have not done first-principles thinking.

### Trap 6 — Over-applying it

Not every decision deserves a decomposition to physics. First-principles thinking is metabolically expensive. Reserve it for decisions that are large, irreversible, suspicious, or category-defining.

### Trap 7 — Ignoring path-dependence

Sometimes the inherited answer *is* roughly physics-bound, and the gap is real but uncrossable from where you stand. Distinguish "theoretically attackable" from "attackable by me, now."

---

## 5. Adjacent Thinkers and Frameworks

### Aristotle — the original conception

The term comes from Aristotle (*Posterior Analytics*, *Metaphysics*). His phrase is *archē* — a beginning, origin, or starting point of knowledge. A first principle for Aristotle is "the first basis from which a thing is known."

> "In every systematic inquiry where there are first principles, or causes, or elements, knowledge and science result from acquiring knowledge of these." — Aristotle, *Physics*, Book I

Aristotle's contribution: **all reasoning bottoms out somewhere**, and the quality of your reasoning depends on the quality and identification of your bottoms-out points.

### Feynman — "imagine the answer" and the Feynman Technique

Feynman's contribution is methodological: when stuck, imagine you already know the answer and reason backward. The Feynman Technique:

1. Pick a concept.
2. Explain it as if to a child, in plain language.
3. Wherever you stumble or reach for jargon, that's where your understanding fails.
4. Go back to source material on that specific gap.
5. Repeat.

> "The first principle is that you must not fool yourself — and you are the easiest person to fool." — Richard Feynman, Caltech commencement, 1974

This quote is the epistemic backbone of the entire framework.

### Bezos — regret minimization (complementary, not equivalent)

> "I projected myself forward to age 80 and said, 'Okay, now I'm looking back on my life. I want to have minimised the number of regrets I have.'" — Jeff Bezos

First principles tells you **what is actually possible**. Regret minimization tells you **which of the possible paths to take given asymmetric outcomes**. Bezos also separates Type 1 (irreversible — apply heavy analysis) from Type 2 (reversible — decide fast). First-principles thinking is expensive enough that it should mostly be applied to Type 1 decisions.

Bezos's "working backward from the customer" — defining the press release for a product before building it — is also a first-principles move: it forces decomposition of what the product *actually does* before you import assumptions about how to build it.

### Charlie Munger — mental models and the latticework

Munger's framework is broader: build a "latticework of mental models" from the major disciplines and use multiple models to triangulate any problem.

Relevant contributions:
- **Inversion.** Don't ask "how do I succeed?" Ask "how do I fail?" and avoid that.
- **Circle of competence.** Know where your knowledge is genuinely first-principles deep vs. where it's analogical and shallow.
- **Lollapalooza effects.** When multiple models point the same way, the effect is non-linear.
- **Avoiding stupidity beats seeking brilliance.**

### Adjacent: Toyota's Five Whys, Karl Popper, Naval Ravikant

- **Five Whys** (Sakichi Toyoda, Taiichi Ohno) — keep asking "why" until you reach root cause.
- **Popper** — knowledge advances by falsification. First-principles claims should be stated specifically enough to be wrong.
- **Naval Ravikant** — "Clear thinking requires clear writing. If you can't put your idea into words, you don't have an idea."

---

## 6. Application Examples

### Software architecture decisions

**Inherited:** "We need a microservices architecture because that's how modern systems are built."

**Decomposition:**
- What does the system physically need to do? Receive requests, transform data, store state, return responses.
- What are the actual constraints? Team size, deploy frequency, latency budget, failure isolation requirements.
- What does microservices *cost*? Network overhead, distributed-system complexity, operational surface area.
- What does it *buy*? Independent deployability, isolated failure domains, polyglot teams.

**Reconstruction:** For a 4-person team with one product, the costs of microservices vastly exceed the benefits. A modular monolith satisfies the same physical requirements at a fraction of the operational complexity. The "microservices is modern" claim is analogical reasoning from companies (Netflix, Amazon) whose constraints are nothing like yours.

### Business model design

**Inherited:** "Agencies charge hourly because that's what agencies do."

**Decomposition:**
- What is the agency physically delivering? An outcome.
- What does the client physically value? The outcome, not the hours.
- What does hourly billing actually optimise for? Maximising hours billed — misaligned with client value.
- Floor: cost of inputs (labour, tools, time) plus margin. Ceiling: value of outcome to client.

**Reconstruction:** Outcome-based, retainer, or productised pricing aligns incentives with delivery. Hourly is precedent (lawyers did it, agencies copied), not constraint.

### Personal life decisions

**Inherited:** "I should go to university because that's the path."

**Decomposition:**
- What does university physically provide? Credential, knowledge, network, time-structured environment, signalling.
- What do I actually need? Depends on goal.
- What are the costs? Time (3-4 years), money, opportunity cost, location lock-in.

**Reconstruction:** For some goals (medicine, law, academic research) the credential is load-bearing. For others (founding a company, learning to code, sales) the credential is convention and the physical inputs can be acquired more cheaply elsewhere.

### Engineering trade-offs

**Inherited:** "We need redundancy on this system because production systems need redundancy."

**Decomposition:**
- What is the cost of the system being down for X minutes? (Compute it. In money.)
- What does redundancy cost? (Compute it.)
- What is the actual probability of failure of the non-redundant system?
- What is the probability of redundancy itself introducing failure?

**Reconstruction:** Redundancy is justified when expected downtime cost > redundancy cost + redundancy-introduced failure cost. Often it isn't.

---

## 7. When to Use This (and When Not To)

### Use it when

- The decision is large, irreversible, or compounding (architecture, hiring, capital allocation, life direction)
- The inherited answer is suspiciously expensive, slow, or arbitrary
- You suspect convention has calcified (regulated industries, mature markets, "this is just how it's done" energy)
- You are competing against incumbents and need an asymmetric edge
- Multiple smart people give confident answers that contradict each other

### Don't use it when

- The decision is small or reversible — analogy is faster and cheaper
- You lack domain knowledge to decompose accurately — confident wrongness beats deferral to expertise
- The inherited answer is genuinely physics-bound — wins are marginal
- You're using it to rationalise a decision you've already made — that's theatre, not thinking

### A working heuristic

> If the inherited answer has been stable for 50+ years across multiple competitors with different incentives, it's probably close to physics. If it's a 10-20 year old convention in a fast-moving industry, it's probably attackable. If it's "best practice" within a single company or sub-culture, it's almost certainly attackable.

---

## 8. Self-Check Protocol

Before concluding a first-principles analysis, run this checklist:

1. Did I state the inherited claim specifically, with numbers and units?
2. Did I decompose to physics / math / definition / verifiable price — not to "industry standard"?
3. Did I actually compute a floor estimate, with sources for the input prices?
4. Did I identify the gap between floor and inherited, and articulate where the gap comes from?
5. Did I ask why the gap has persisted despite smart, well-resourced people existing?
6. Did I distinguish "theoretically attackable" from "attackable by me, now"?
7. Did I stress-test by inverting — what would have to be true for the inherited answer to be right?
8. Have I avoided confusing my own conclusion-by-analogy with first-principles reasoning?

---

## 9. Closing — Why This Matters

First-principles thinking is the deliberate refusal to inherit answers from a context whose constraints may no longer apply. It is expensive, slow, and socially uncomfortable. It is also the single most reliable way to find non-obvious leverage in domains where convention has calcified.

The combined picture:
- **Aristotle** gives the structure (knowledge bottoms out at first principles).
- **Feynman** gives the epistemic discipline (don't fool yourself; explain it simply).
- **Munger** gives the toolkit (multiple models, inversion, circle of competence).
- **Bezos** gives the decision frame (which decisions deserve heavy analysis).
- **Musk** gives the operational procedure (decompose to materials, price the floor, attack the gap).

> "Boil things down to their fundamental truths and reason up from there." — Elon Musk
