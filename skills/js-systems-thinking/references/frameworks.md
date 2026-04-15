# Practical Frameworks for Systems Thinking

---

## The Iceberg Model

Move from reactive to transformative thinking by going deeper.

| Level | Question | Response Type |
|---|---|---|
| **Events** | What happened? | Reactive |
| **Patterns** | What trends over time? | Adaptive |
| **Structures** | What feedback loops, rules, incentives produce these patterns? | Creative/Design |
| **Mental Models** | What beliefs and assumptions created these structures? | Transformative |

**Example — "Sales dropped 15% last quarter":**
- **Event:** Sales dropped 15%
- **Pattern:** Sales drop every Q3 for three years, recover in Q4
- **Structure:** Compensation rewards new acquisition over retention; Q3 is renewal season so churn spikes while sales chase new logos
- **Mental Model:** "Growth comes from new customers, not deepening existing relationships"

**Application:** When facing a problem, discipline yourself below the event level. Intervene at the deepest level you can reach.

---

## Causal Loop Diagrams (CLDs)

Show the feedback structure of a system.

### How to Build One

1. **Identify key variables** — things that increase or decrease: revenue, trust, morale, inventory, technical debt
2. **Map causal links** — arrows from cause to effect, marked:
   - **S / +** (same direction): cause up → effect up
   - **O / -** (opposite): cause up → effect down
3. **Identify feedback loops** — paths returning to starting variable:
   - **R (Reinforcing):** even number of O links (or all S). Amplifies change.
   - **B (Balancing):** odd number of O links. Resists change, seeks equilibrium.
4. **Mark delays** — significant time lags marked with ||
5. **Name the loops** — descriptive names capturing behaviour

**Example:**
```
Customer Satisfaction --S--> Word of Mouth --S--> New Customers --S--> Workload
Workload --O--> Service Quality --S--> Customer Satisfaction
                                                     [B: Service Capacity Limit]

Customer Satisfaction --S--> Revenue --S--> Investment in Staff --S--> Service Quality
                                                     [R: Growth Engine]
```

---

## Stock and Flow Diagrams

More precise than CLDs. Better for quantitative modelling.

**Components:**
- **Stock** (rectangle): accumulation measurable at a point in time
- **Inflow** (arrow in): rate increasing the stock
- **Outflow** (arrow out): rate decreasing the stock
- **Converter** (circle): variable influencing flows
- **Connector** (thin arrow): information links

**Key principles:**
- Stocks change slowly even when flows change suddenly (momentum)
- Stocks act as buffers, decoupling inflows from outflows
- You can only change a stock by changing its flows
- Dynamic equilibrium = inflows equal outflows (not nothing happening)

---

## Identifying Leverage Points — Step by Step

1. **Define problem behaviour over time.** Draw the key variable(s) over time. Growing? Declining? Oscillating?
2. **Identify key stocks.** What's accumulating or depleting? (Cash, trust, skill, technical debt, reputation...)
3. **Map feedback loops.** What reinforcing loops drive growth/decline? What balancing loops maintain status quo?
4. **Find the dominant loop.** Which loop is currently winning?
5. **Look for the archetype.** Does this match a known pattern? If so, the archetype tells you where leverage is.
6. **Ask: where is the constraint?** Stock, flow, information gap, rule, goal, mental model?
7. **Apply Meadows' hierarchy.** Work from bottom (#12 parameters) up (#1 transcend paradigms). Usually the real leverage is NOT where people are pushing.
8. **Test your hypothesis.** Trace the causal chain: "If I do X, then what? And then? And then?" Look for unintended consequences.

---

## Questions a Systems Thinker Asks

### About the System
- What is this system's purpose? (What does it actually DO, not say?)
- What are the key stocks? Accumulating or depleting?
- What are the main feedback loops? Reinforcing? Balancing?
- Which loop is dominant? Is dominance shifting?
- Where are the significant delays?
- What are the boundaries? What's included/excluded?
- What information is missing? Who lacks feedback?
- What are the rules? Who makes them? Who benefits?

### About Behaviour Over Time
- What has been the trend? (Not just now — over time)
- Is this growing, declining, oscillating, or stagnating?
- Has this happened before? Known archetype?
- What changed just before the behaviour changed?

### About Interventions
- Where is the leverage point?
- What would be the unintended consequences?
- Are we pushing a reinforcing loop or addressing a balancing loop?
- Treating symptom or cause?
- How long before we see effects? (Delay awareness)
- Can we test at small scale first?

### About Mental Models
- What assumptions are we making?
- Whose perspective are we missing?
- What would someone who disagrees say?
- What if the opposite were true?

### About Goals
- What is this system actually optimised for?
- Is that what we want?
- Are our metrics measuring what we care about?
- Are our goals eroding?
- Would we design this way from scratch?

---

## Common Traps and Antidotes

| Trap | Description | Antidote |
|---|---|---|
| **Event-level thinking** | Reacting to events without seeing patterns or structures | Use the Iceberg Model. "What's the pattern? What structure produces it?" |
| **Linear thinking** | Assuming proportional cause-and-effect | Look for feedback loops, thresholds, saturation, delays |
| **Blame** | Attributing systemic problems to individuals | "What structure would produce this with well-intentioned people?" (Deming's 95/5) |
| **Quick fix addiction** | Choosing fast symptomatic solutions, capacity atrophies | "Symptom or cause?" Make fixes explicitly temporary |
| **Optimising the wrong thing** | Measuring a bad proxy. Goodhart's Law | "Is this metric still a good proxy? What behaviour does it incentivise?" |
| **Ignoring delays** | Aggressive corrections, overshoot | Map delays. Be patient. Monitor trends not snapshots |
| **Narrow boundaries** | Missing critical feedback loops, externalising costs | "What am I leaving out? Who is affected but not represented?" |
| **Illusion of control** | Believing you can predict/control a complex system | Design for resilience, not optimisation. Maintain options. Experiment |
| **Sub-optimisation** | Each part optimises locally, whole degrades | Clarify whole-system purpose. Align subsystem goals |
| **Paradigm blindness** | Can't see alternatives from inside current paradigm | Seek radically different worldviews. "What if the opposite were true?" |
