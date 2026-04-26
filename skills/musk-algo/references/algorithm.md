# Musk's Algorithm: A Reference

> "I have this very basic first principles algorithm that I run."
> — Elon Musk, Starbase tour with Tim Dodd (Everyday Astronaut), Part 2, August 2021

A dense reference for applying Musk's 5-step engineering and decision-making algorithm to coding, strategy, business, and personal systems. Sourced primarily from the Everyday Astronaut Starbase tour (the canonical articulation), Walter Isaacson's *Elon Musk* (2023), Lex Fridman interviews, Tesla earnings calls, and Musk's own posts.

## Table of Contents

1. The Algorithm — Verbatim
2. Each Step in Depth (Steps 1-5)
3. Adjacent Mental Models (first principles, physics-based reasoning, "best part is no part", tag-to-person, comfortable pace of being wrong, alien dreadnought lesson)
4. Application Heuristics (software, business, personal)
5. Sources
6. Operational Checklist

---

## Part 1: The Algorithm — Verbatim

The canonical articulation is from Tim Dodd's Starbase factory tour (Everyday Astronaut, "Starbase Tour with Elon Musk [PART 2]", published August 2021). Musk repeats it verbatim in Walter Isaacson's biography (Chapter 64, "The Algorithm").

### The Five Steps

**1. Make the requirements less dumb.**
> "Your requirements are definitely dumb. It does not matter who gave them to you. It's particularly dangerous if a smart person gave you the requirements, because you might not question them enough. Everyone's wrong. No matter who you are, everyone is wrong some of the time. All designs are wrong, it's just a matter of how wrong."
> — Musk, Starbase Tour Part 2

**2. Delete the part or process step.**
> "If you're not adding things back in at least 10% of the time, you're clearly not deleting enough. The bias tends to be very strongly toward 'let's add this part or process step in case we need it.' But you can basically make 'in case' arguments for so many things."
> — Musk, Starbase Tour Part 2

**3. Simplify or optimize.**
> "Possibly the most common error of a smart engineer is to optimize a thing that should not exist."
> — Musk, Starbase Tour Part 2 (also quoted in Isaacson, Ch. 64)

**4. Accelerate cycle time.**
> "Every process can be sped up. But only do this after you've followed the first three steps. If you're digging your grave, don't dig it faster."
> — Musk, Starbase Tour Part 2

**5. Automate.**
> "I have personally made the mistake of going backwards on all five steps multiple times. I automated, accelerated, simplified, and then deleted."
> — Musk, Starbase Tour Part 2

### The Hard Rule About Order

The order is non-negotiable. Musk repeatedly emphasizes this is the most common failure mode — including his own. From Isaacson Ch. 64: "I have made this mistake often enough that I am hopefully not going to make it again." He frames doing the steps out of order as the single biggest source of waste at Tesla and SpaceX.

---

## Part 2: Each Step in Depth

### Step 1: Make the Requirements Less Dumb

**The core claim.** Every requirement is wrong to some degree. Smart people produce smart-sounding requirements that are often the most dangerous, because they survive scrutiny that dumber requirements wouldn't.

**The reasoning.** Most engineering effort is spent satisfying requirements. If the requirement itself is wrong, every downstream optimization is waste. Worse, requirements get laundered through organizations until nobody remembers who set them or why — they become "the spec" and acquire false authority.

**Tag every requirement to a name, not a department.** Musk's hard rule: requirements must come from a person, never "the safety department" or "the legal team" or "engineering." From the Starbase tour: *"All departments should be deleted by default. If you don't end up adding back 10% of them, you didn't delete enough. Requirements from a department are particularly dangerous."* The reason: a person can be argued with, can update their belief, can be wrong. A department is a fog. Isaacson (Ch. 64) describes Musk demanding the name of whoever specified a particular component tolerance on Raptor — and when no one could produce a name, the requirement was struck.

**Canonical example — the Falcon 9 stage separation bracket.** Tim Dodd asks about a particular bracket. Musk explains it was over-spec'd because someone in propulsion specified a load case that someone in structures then doubled "for margin," and someone in manufacturing added a fastener "to be safe." Three people, each adding 50% margin, compounding to 3.4x the actual requirement. None of them were wrong individually. The system was wrong.

**Canonical example — the battery pack cost (Tesla).** Musk's most-cited first-principles example, from a 2012 Foundation interview and re-told in Isaacson: industry "knew" battery packs cost ~$600/kWh and would always be expensive. Musk asked: what are batteries actually made of? Cobalt, nickel, aluminum, carbon, polymers, steel can. What do those raw materials cost on the London Metal Exchange? About $80/kWh. The other $520 was just how people were currently doing it. The requirement "batteries cost $600/kWh" was dumb.

**Canonical example — Raptor engine pressure sensor.** Isaacson, Ch. 64: an engineer defended a pressure sensor by saying "the regulations require it." Musk asked which regulation. The engineer couldn't say. It turned out the regulation was internal SpaceX, which traced to a previous project, which traced to a NASA spec for Apollo-era hardware that no longer applied.

**Common failure mode this prevents.** "Cargo cult engineering" — replicating the form of a previous successful system without understanding which parts were load-bearing. Also prevents what Musk calls "the second-hand requirement" — a spec that everyone follows but no one currently believes in.

**Application question.** For every requirement on your list, ask: *Whose name is on this? When did they last revisit it? What evidence would change their mind? What does this requirement actually optimize for?*

---

### Step 2: Delete the Part or the Process Step

**The core claim.** The default should be deletion. Adding back is the exception. If you delete things and never have to add them back, you didn't delete aggressively enough.

**The 10% rule.** *"If you're not adding back in at least 10% of what you delete, you're not deleting enough."* This is calibration, not a target. It's how you know you're cutting close enough to the bone. If you delete 100 things and have to restore 5, you were too cautious. If you restore 30, you cut too deep. Around 10% means you're at the actual frontier.

**Why deletion is hard.** Adding is rewarded socially (you "contributed"). Deleting is punished — if the thing you deleted turns out to be needed, you're blamed; if it works, no one notices. So organizations accumulate parts, process steps, meetings, approval gates, and code paths via a one-way ratchet. Musk's algorithm is a deliberate counter-pressure.

**The "in case" trap.** From the Starbase tour: *"The bias tends to be very strongly toward 'let's add this part or process step in case we need it.' But you can basically make 'in case' arguments for so many things."* "In case" is unfalsifiable. Once you accept "in case" as justification, you can never delete anything.

**Canonical example — Model 3 production line.** Isaacson (Ch. 39, "Production Hell"; Ch. 64): Musk walked the Fremont line and pointed at a machine that placed a fiberglass mat on top of the battery pack to dampen sound. Why? "NVH team said cabin was too loud." When tested, removing the mat changed cabin noise by inaudible decibels. The mat was deleted. The machine was deleted. The team was deleted. The supplier contract was deleted.

**Canonical example — Raptor engine flanges.** Starbase tour: Musk points to flanges joining engine sections and notes most of them existed because the engine was made by separate teams whose work met at flanges. The flanges weren't engineering — they were org chart. Many were deleted by having one team own contiguous sections.

**Canonical example — SpaceX whiteboard requirement deletion.** Isaacson Ch. 64: in a 2021 review Musk had teams literally bring requirements to a whiteboard, name the person who owned each, and justify it. Roughly 10% of requirements were deleted on the spot. A subsequent test showed the rocket flew fine without them.

**"The best part is no part."** A Musk maxim, repeated in nearly every Tesla/SpaceX all-hands, and on his X/Twitter posts. "The best part is no part. The best process is no process." It's the deletion principle compressed to six words. Every part has cost — purchase, inventory, assembly time, inspection, failure mode, replacement supply chain. A non-existent part has zero of all of those.

**Common failure mode this prevents.** "Defensive accretion" — the slow buildup of parts/steps/code/process that no individual person added irresponsibly but which collectively destroys the system's velocity and clarity.

**Application question.** For every component, line of code, meeting, document, and process step: *what happens if I delete this entirely?* Not "what happens if I optimize it" — what happens if it doesn't exist at all. Default to deletion; require a named person and a falsifiable reason to keep.

---

### Step 3: Simplify or Optimize

**The core claim.** Only after you've validated requirements and aggressively deleted should you optimize what remains. *"Possibly the most common error of a smart engineer is to optimize a thing that should not exist."*

**Why this order matters.** Optimization is intellectually satisfying — it's the work that engineers were trained to do. So engineers default to optimization even when deletion or requirement-revision would be 10x better. By placing optimization third, the algorithm forces you to earn the right to optimize by first proving the thing should exist.

**The "smart engineer" trap.** Isaacson Ch. 64: Musk describes this as the trap that catches the most capable people. A B-grade engineer optimizing a part that should be deleted produces 50% improvement. An A-grade engineer optimizing the same part produces 80% improvement. Both are zero — the part shouldn't exist. The smart engineer's superior optimization actually entrenches the wasteful part by making it harder to argue for deleting.

**Canonical example — Raptor electronics.** Starbase tour: Musk points to a wire harness and explains that early Raptor versions had a complex harness that was beautifully optimized — minimum length, ideal routing, perfect strain relief. When they revisited Step 1 (requirements), they realized half the wires went to sensors that weren't needed. Deleting the sensors deleted the harness section, deleting the optimization work entirely.

**Canonical example — Tesla cost reduction.** From Tesla Q4 2022 earnings call: Musk describes Tesla's cost engineering as iterative passes through the algorithm. Each pass through a part's BOM (bill of materials) starts with re-questioning whether the part should exist before any cost optimization. He cites this as why Tesla's cost-down curves outpace traditional auto.

**The idiot index.** A core Musk concept, articulated in Isaacson Ch. 64. **The "idiot index" = (cost of finished part) / (cost of raw materials).** A high idiot index means most of the cost is in how the part is made, not what it's made of — which means there's massive room to delete process steps, simplify the design, or change manufacturing.

> "If a part has a high idiot index, that means it's idiotic. You're paying way too much for the manufacturing complexity."
> — Musk, quoted in Isaacson Ch. 64

Example given: a SpaceX engine valve cost $13,000 to manufacture but the raw aluminum was about $200. Idiot index ≈ 65. That's a screaming signal to redesign — most of that cost is process complexity that may be deletable. Tesla and SpaceX teams rank parts by idiot index and attack the highest first.

**Common failure mode this prevents.** Local optimization within global waste. Polishing a turd. Making the wrong thing better.

**Application question.** Before any optimization: *am I optimizing something that should be deleted? Have I revisited the requirement that justifies this thing's existence within the last 30 days?*

---

### Step 4: Accelerate Cycle Time

**The core claim.** Once you've validated, deleted, and simplified, then make iteration faster. Never before.

**Why this is fourth, not first.** *"If you're digging your grave, don't dig it faster."* Speed amplifies whatever you're doing — including doing the wrong thing. Acceleration applied to a flawed process produces flawed output faster, with more momentum and more sunk cost making the flaws harder to fix.

**Canonical example — Tesla Nevada Gigafactory walk.** Isaacson Ch. 64: Musk asks about a battery cell production step that takes 16 seconds. The team is proud they've reduced it from 18. Musk asks why it can't be 5. Team explains the chemistry needs time to settle. Musk asks why. Long discussion reveals the 16 seconds was set by an upstream temperature spec that itself was set by a downstream coating step that had been deleted six months earlier. The 16-second cycle was solving a problem that no longer existed. Cycle time dropped to 4. **The lesson Musk extracts: they accelerated a process that should have been deleted.**

**Canonical example — Starship build cadence.** Starbase tour: Musk shows Tim Dodd Starship prototypes being built in a tent in Boca Chica. The whole point of the tent and the rapid succession of prototypes (SN8, SN9, SN10, SN11, SN15...) was cycle time. SpaceX explicitly traded perfection for iteration speed once they were confident the requirements and architecture were right. Each prototype's failure produced a learning that fed the next one within weeks, not years.

**The "comfortable pace of being wrong" concept.** Discussed in the Lex Fridman interviews (Lex #252, December 2021; Lex #400, November 2023). Musk argues that organizations should iterate at a pace where being wrong is normal and survivable. If your cycle is so slow that each release "must" succeed, you'll over-engineer, over-review, and over-delay each one — which makes failure more catastrophic, which makes you more cautious, in a death spiral. Fast cycles let you be wrong cheaply, learn, and converge. *"Failure is an option here. If things are not failing, you are not innovating enough."* — Musk, oft-repeated, including 2014 Reddit AMA.

**Common failure mode this prevents.** Premature optimization of throughput. Building a fast factory for the wrong product. Shipping more bugs faster.

**Application question.** *Have I done steps 1–3? If yes, where is the iteration loop bottlenecked, and what would 10x faster cycles change about how I work?*

---

### Step 5: Automate

**The core claim.** Automation is last. Only automate processes that you've validated, deleted from, simplified, and accelerated.

**Why automation is last.** Automation is the highest-cost, highest-commitment, most rigid form of any process. It encodes assumptions in steel and silicon. If the underlying process is wrong, automation makes the wrongness permanent and expensive.

**Canonical example — Tesla Model 3 "alien dreadnought" mistake.** Isaacson Ch. 39 covers this in painful detail. In 2017–2018, Musk pushed Tesla's Fremont and Nevada lines to be "the machine that builds the machine" — hyper-automated, with humans removed wherever possible. He coined the term "alien dreadnought" for what the line would look like. It nearly killed the company.

What went wrong: complex automated systems were built around process steps that hadn't been simplified or validated. A machine to place a fiberglass mat that shouldn't have existed. A robot to fasten a bolt that should have been a single-piece casting. Automation locked in the wrong process.

Musk's public admission, on Twitter (April 13, 2018): *"Yes, excessive automation at Tesla was a mistake. To be precise, my mistake. Humans are underrated."*

The recovery: Musk slept on the factory floor, ripped out automation, ran the algorithm in order. Many "smart" automated cells were deleted entirely. Humans replaced robots in steps where the underlying process was changing too fast for automation to be worth it. Production stabilized.

**Canonical example — SpaceX welding.** Starbase tour: Musk shows automated welding equipment and notes some welds were de-automated because the design was iterating too fast for fixed automation tooling to keep up. Once the design stabilized, automation went back in.

**The lesson Musk extracts from his own mistakes.** From the Starbase tour, this is the rawest moment in the algorithm: *"I have personally made the mistake of going backwards on all five steps multiple times. I automated, accelerated, simplified, and then deleted."* He's confessing that even *he* — the person who articulates the algorithm — has done the steps in reverse order on multiple billion-dollar projects.

**Common failure mode this prevents.** Encoding waste into infrastructure. Building elaborate machines and systems around tasks that should not exist.

**Application question.** *Is this process stable? Have I iterated on it recently? If I automate it, what's the cost to change it later? Could I just delete it instead?*

---

## Part 3: Adjacent Mental Models

### First Principles Thinking (vs. Reasoning by Analogy)

Musk's most-discussed mental model. See `first-principles.md` for full treatment. Compressed:

> "I think it's important to reason from first principles rather than by analogy. The normal way we conduct our lives is we reason by analogy. We're doing this because it's like something else that was done, or it is like what other people are doing. With slight iterations on a theme. And it's mentally easier to reason by analogy rather than from first principles. First principles is kind of a physics way of looking at the world. You boil things down to the most fundamental truths and say, 'What are we sure is true?' and then reason up from there."
> — Musk, Foundation interview with Kevin Rose, 2012

Step 1 of the algorithm ("make requirements less dumb") is operationally a first-principles audit of every requirement. The algorithm is first-principles thinking compiled into a repeatable process.

---

### Physics-Based Reasoning

Musk's preferred mode. He has a physics undergrad (Penn) and frames most engineering and business problems through physics constraints.

**The framing.** Physics tells you what's *possible*, not what's *currently done*. The speed of light, the energy density of chemical bonds, thermodynamic limits, structural limits of materials — these are real constraints. Almost everything else is convention.

> "Physics is the law. Everything else is a recommendation."
> — Musk, attributed across multiple interviews

**Application.** Before accepting that something is hard or impossible, calculate the physics floor. Rocket fuel costs are roughly 0.3% of a Falcon 9 launch — so the physics floor for cost-to-orbit is ~100x cheaper than 2010 prices. That gap is engineering and business model, not physics. This logic justifies SpaceX's existence.

**For non-physics domains.** Substitute the equivalent fundamental constraint:
- Software: Big-O complexity, network round trips, disk I/O latency, human reading speed
- Business: unit economics floor (CAC, gross margin given commodity inputs), time-to-payback math
- Personal: hours in a day, sleep requirements, energy budgets

---

### "The Best Part Is No Part"

The deletion principle generalised. Musk applies it beyond physical parts:

- **Best meeting is no meeting.** From a 2018 internal Tesla email: *"Walk out of a meeting or drop off a call as soon as it is obvious you aren't adding value. It is not rude to leave, it is rude to make someone stay and waste their time."*
- **Best process is no process** — process exists to compensate for low trust or unstable requirements. Fix the underlying issue and the process is unneeded.
- **Best line of code is no line of code** — every line is a liability: bugs, maintenance, comprehension cost.
- **Best report is no report** — most reports exist because someone once asked, then stopped reading, but no one stopped writing.

---

### Tag Requirements to a Person, Never a Department

Already covered in Step 1 but the principle generalises. Musk's organisational rule: every requirement, decision, and deliverable has a single human name attached. Departments are abstractions that diffuse responsibility.

**Why.** Departments don't think. They don't update beliefs. They don't have skin in the game. A person can be wrong, learn, and revise. "Legal said no" is not a thinkable statement — *which* lawyer said no, when, on what evidence?

**Practical implication.** Replace "the team thinks" with "[Name] thinks." Replace "engineering decided" with "[Name] decided." When a requirement comes from a department, find the actual person and route the question to them.

---

### The "Comfortable Pace of Being Wrong"

Organisations have a natural cadence at which being wrong is survivable. Below that cadence (too slow), each decision becomes high-stakes, leading to over-caution and slower decisions in a doom loop. Above that cadence (too fast), you can't learn from outcomes before the next decision is locked in.

The right cadence is *fast enough that being wrong is normal* but *slow enough that you can integrate learning between iterations*. SpaceX prototyping (weeks per iteration), Tesla's weekly cost-down reviews, and X/Twitter's same-day deploys are all calibrated to this principle.

---

### The Idiot Index (deep dive)

**Formula:** `idiot index = cost of finished part / cost of raw materials`

A high idiot index means most of the cost is in *how the part is made*, not *what it's made of*. That's a screaming signal that there's massive process bloat, design complexity, or supply-chain markup that may be deletable.

**Generalisation beyond manufacturing:**
- Software: lines of code per unit of business value delivered. Time-to-feature divided by engineer-hours of theoretical floor.
- Business: cost-to-acquire-customer / theoretical cost-to-deliver-message-to-customer.
- Personal: time-spent-on-task / time-required-by-physics.

Rank items by idiot index. Attack the highest first. Don't bother optimising things with low idiot indices — they're already close to physics-bound.

---

### Musk's View on Automation (the Alien Dreadnought Lesson)

The most explicitly self-critical of Musk's models. Compressed lesson:

1. Automation is powerful but rigid.
2. Rigid systems applied to unstable processes amplify waste.
3. Humans are flexible, fast to retrain, and underrated for evolving processes.
4. Automate only after the underlying process is validated, lean, and stable.
5. *"Humans are underrated."* — Musk, April 2018

---

## Part 4: Application Heuristics

### Applying the Algorithm to Software Engineering

**Step 1 — Make the requirements less dumb.**
- For each feature in the spec: who specifically asked for it? When? Are they still here? Do they still want it? What user evidence supports it?
- For each non-functional requirement (latency targets, uptime SLOs, scale numbers): where did the number come from? Is it still valid?
- For each library/framework dependency: which constraint forced this choice? Is that constraint still real?

**Step 2 — Delete the part or process step.**
- Delete code paths, not just lines. Whole files. Whole services. Whole microservices.
- Delete abstractions used in only one place. ("Premature abstraction is the root of much evil.")
- Delete config options that no production environment uses.
- Delete tests that test the framework, not your logic.
- Delete CI steps that haven't caught a real bug in 6 months.
- Delete meetings, standups, status docs that produce no decision.
- Calibration: if you don't restore ~10% of what you delete, delete more aggressively.

**Step 3 — Simplify or optimize.**
- Apply the idiot index to code: lines of code per unit of business value delivered. Functions with high "idiot index" (lots of code, little value) are redesign candidates.
- Reduce indirection. Fewer layers. Fewer interfaces with one implementation. Fewer wrappers.
- Optimize hot paths only after profiling. Cold paths are deletion candidates, not optimization candidates.

**Step 4 — Accelerate cycle time.**
- Faster local feedback (test runs, type checks, hot reload).
- Faster CI.
- Faster deploys (continuous deployment over weekly releases).
- Faster decisions (DRIs, written async docs over meetings).
- Only after steps 1–3.

**Step 5 — Automate.**
- Automate stable, repeated, validated processes (deploys, tests, infra provisioning).
- Don't automate exploratory or rapidly-changing work.
- If a process is changing weekly, manual is correct.

**Common software anti-patterns the algorithm catches:**
- Over-engineered abstractions for use cases that never materialised (Step 2)
- Microservices added "in case we need to scale" (Step 1, then Step 2)
- Optimising endpoint latency for a feature with 3 users (Step 3 before Step 2)
- Building a custom CI/CD pipeline for a 2-person team (Step 5 before Step 1)

---

### Applying the Algorithm to Business and Strategy

**Step 1 — Make the requirements less dumb.**
- Why does this product need this feature? Whose name is on that requirement?
- Why is the org structured this way? Who decided? When? Is the rationale still valid?
- Why does this contract have these terms? Have they been re-negotiated since the original deal context changed?
- Why do we sell at this price? Is it cost-plus, market-comparison (analogy!), or value-based?

**Step 2 — Delete the part or process step.**
- Delete product features used by <5% of customers. Measure actual usage, not stated preference.
- Delete entire SKUs that confuse customers and dilute focus.
- Delete recurring meetings with no decision outcome (the Musk email rule: walk out).
- Delete approval gates. Replace with a single named DRI.
- Delete reports no one reads. (Stop writing them; see who complains.)
- Delete entire job functions that exist to manage process the company shouldn't have.
- Calibration: if you don't reinstate ~10%, you didn't cut deep enough.

**Step 3 — Simplify or optimize.**
- Apply idiot index to business processes: time-to-decision, cost-per-customer-acquired, headcount-per-output.
- Simplify pricing (Tesla famously has ~5 SKUs vs. legacy auto's hundreds).
- Simplify org chart (Musk targets ~7 direct reports max, with explicit named ownership).

**Step 4 — Accelerate cycle time.**
- Weekly business reviews, not quarterly.
- Same-week hiring decisions.
- Same-day product decisions where possible.
- Calibrate to a cadence where being wrong is normal — see "comfortable pace of being wrong."

**Step 5 — Automate.**
- Automate billing, reporting, onboarding once stable.
- Don't automate sales conversations while still finding product-market fit.
- Don't build elaborate CRM workflows for a sales motion that's still iterating.

**Common business anti-patterns the algorithm catches:**
- "We've always done it this way" (Step 1)
- Process bloat from a crisis 3 years ago that's no longer relevant (Step 2)
- Optimising a sales funnel for a market segment you should exit (Step 3 before Step 2)
- Hiring an ops team to manage a process that should be deleted (Step 5 before Step 2)

---

### Applying the Algorithm to Personal Productivity

**Step 1 — Make the requirements less dumb.**
- Why am I doing this task? Who asked? Is the answer "past me thought it was important"? When did past-me last revisit?
- Why is this on my calendar? What outcome does it produce?
- Why am I subscribed to this, reading this, attending this?
- The "future self" test: would future-me thank present-me for this requirement?

**Step 2 — Delete the part or process step.**
- Delete recurring commitments that don't produce energy or output.
- Delete tools and apps that fragment attention without proportional value.
- Delete projects that haven't moved in 90 days. (Either restart or delete; "someday" is a deletion in disguise.)
- Delete inputs (newsletters, feeds, notifications) more aggressively than you add them.
- Calibration: re-add ~10%. If you re-add nothing, you weren't cutting close to the bone. If you re-add 50%, you over-deleted.

**Step 3 — Simplify or optimize.**
- Apply idiot index to your time: time spent / value produced. Highest-ratio activities get redesigned, not optimised.
- Simplify decision rules (defaults, heuristics, "if X then always Y").
- Reduce decision count: fewer choices about food, clothes, schedule.

**Step 4 — Accelerate cycle time.**
- Faster review cycles on goals (weekly, not quarterly).
- Faster feedback on what's working (daily journal, weekly retrospective).
- Faster decisions on commitments (24-hour rule for most yes/no choices).

**Step 5 — Automate.**
- Automate stable recurring tasks (bill pay, recurring orders, calendar templates).
- Don't automate work you're still figuring out how to do.
- Templates and snippets for repeated writing — but only after the writing pattern is stable.

**Common personal anti-patterns the algorithm catches:**
- Productivity stack with 14 apps to manage tasks you should just do or delete (Step 5 before Step 2)
- Optimising morning routine for a goal you no longer hold (Step 3 before Step 1)
- Speed-reading more books in a domain you should exit (Step 4 before Step 1)
- "In case I need it later" hoarding of files, tabs, notes (the "in case" trap from Step 2)

---

## Part 5: Sources

**Primary — the canonical articulation:**
- **Tim Dodd / Everyday Astronaut, "Starbase Tour with Elon Musk [PART 2]"**, YouTube, August 2021. The clearest single articulation of the 5 steps with examples. Roughly 25 minutes of the 2-hour tour.

**Primary — the most thorough written treatment:**
- **Walter Isaacson, *Elon Musk* (Simon & Schuster, September 2023).** Chapter 64 ("The Algorithm") states the 5 steps verbatim and adds the idiot index and the "tag requirements to a person" rule. Chapters 39 (Production Hell) and 40 (Sleeping on the Factory Floor) cover the alien dreadnought failure. Chapters 73–74 cover the Twitter/X application of the algorithm.

**Primary — first-principles articulation:**
- **Kevin Rose / Foundation interview with Elon Musk**, 2012. The battery pack first-principles example.
- **Musk TED talk**, 2013 and 2017. First principles thinking explained for a general audience.

**Secondary — expansions and applications:**
- **Lex Fridman Podcast #252 with Elon Musk**, December 2021. First principles, "comfortable pace of being wrong," automation lessons.
- **Lex Fridman Podcast #400 with Elon Musk**, November 2023. Algorithm applied to X/Twitter post-acquisition.
- **Tesla earnings calls Q4 2018, Q4 2022, Q1 2023.** Cost-down methodology, idiot index applied to Tesla BOM.

**Musk's own posts (X / Twitter):**
- April 13, 2018: *"Yes, excessive automation at Tesla was a mistake. To be precise, my mistake. Humans are underrated."*
- Multiple posts 2020–2023 reiterating "the best part is no part" and "the best process is no process."
- Internal Tesla email (leaked, widely reproduced), April 2018: rules on meetings, communication chains, and walking out of valueless meetings.

**Tertiary — useful synthesis:**
- Tim Urban, *Wait But Why*, "The Cook and the Chef: Musk's Secret Sauce" (2015).
- Ashlee Vance, *Elon Musk: Tesla, SpaceX, and the Quest for a Fantastic Future* (2015).

---

## Part 6: Operational Checklist

```
Before you build, optimise, or automate ANYTHING, run the algorithm in order:

[ ] 1. REQUIREMENTS — For every requirement on this work:
       - Whose name is attached? (Not a department.)
       - When did they last revisit it?
       - What evidence would change their mind?
       - Is the requirement actually true, or true-by-analogy?

[ ] 2. DELETE — For every part / step / line / meeting / process:
       - Default to deletion.
       - Require a named person and falsifiable reason to keep.
       - If you don't restore ~10% later, you didn't delete enough.
       - Beware "in case" arguments — they're unfalsifiable.

[ ] 3. SIMPLIFY — Only what survived Steps 1 and 2:
       - Calculate the idiot index (cost / raw materials, or output / input).
       - Attack high idiot indices first.
       - Don't optimise a thing that should not exist.

[ ] 4. ACCELERATE — Only what survived Steps 1–3:
       - Where is the iteration loop bottlenecked?
       - Calibrate to the "comfortable pace of being wrong."
       - Don't dig your grave faster.

[ ] 5. AUTOMATE — Only stable, validated, simplified, accelerated processes:
       - Will this process change in the next 6 months?
       - What's the cost to undo automation?
       - Could it just be deleted instead?
       - Humans are underrated.

CHECK: Did I do them in order? Going backwards is the most common failure mode — including Musk's own.
```
