# Excalidraw Diagram Patterns

Layout blueprints for 10 diagram types. Read the relevant pattern after selecting a diagram type in the Analysis phase.

---

## Table of Contents

1. [System Architecture (Pipeline)](#1-system-architecture-pipeline)
2. [Hierarchy / Tree](#2-hierarchy--tree)
3. [Swimlane](#3-swimlane)
4. [Flowchart with Decisions](#4-flowchart-with-decisions)
5. [Entity-Relationship](#5-entity-relationship)
6. [Layered Architecture](#6-layered-architecture)
7. [Network / Graph](#7-network--graph)
8. [Quadrant / Matrix](#8-quadrant--matrix)
9. [Sequence-style](#9-sequence-style)
10. [Mind Map](#10-mind-map)

---

## 1. System Architecture (Pipeline)

**When to use:** Sequential process, data pipeline, input → transform → output flow.

**Flow direction:** Left-to-right.

**Layout:**
```
[Input A] ──→ [Process] ──→ [Transform] ──→ [Output]
[Input B] ──↗
[Input C] ──↗
              ════════════════════════════════════
              [Cross-cutting layer (monitoring, errors)]
```

- Input sources stacked vertically on the left, fan into a central processing node.
- Processing steps arranged horizontally, left to right.
- Cross-cutting concerns as full-width bar at the bottom.
- Canvas: 1200-1600w depending on pipeline depth.
- Spacing: 100px horizontal between stages, 80px vertical between stacked inputs.
- Colors: blue for inputs, orange for processing/automation, purple for AI, green for outputs.
- Section labels above each stage column in grey (`fontSize: 12`).

---

## 2. Hierarchy / Tree

**When to use:** Parent-child relationships, org charts, taxonomy, category breakdowns, inheritance.

**Flow direction:** Top-to-bottom.

**Layout:**
```
            [Root]
           /  |  \
      [A]   [B]   [C]
      / \         |
   [A1] [A2]    [C1]
```

- Root node centered at top. Larger box (220x90).
- Children evenly spaced below parent, centered under parent's midpoint.
- Each level gets 100px vertical gap.
- Siblings spaced 40-60px apart horizontally.
- Arrows from parent bottom-center to child top-center.
- Canvas width: `(max_siblings_at_any_level * 220) + padding`.
- Colors: root = primary blue. Each level can shift color, or color by category.
- If tree is wide (>5 siblings), increase horizontal spacing or split into sub-trees.

---

## 3. Swimlane

**When to use:** Parallel processes across roles/teams/systems, responsibility mapping, cross-functional workflows.

**Flow direction:** Left-to-right within lanes, top-to-bottom for lane stacking.

**Layout:**
```
┌─ LANE A ──────────────────────────────────┐
│  [Step 1] ──→ [Step 2]                    │
└───────────────────────────────────────────┘
┌─ LANE B ──────────────────────────────────┐
│            [Step 3] ──→ [Step 4]          │
└───────────────────────────────────────────┘
       ↕ (vertical arrows cross lanes)
```

- Each lane: dashed rectangle, full canvas width, 140-180px tall.
- Lane label: standalone text at left edge inside the lane, `fontSize: 16`, bold appearance.
- Process steps as rectangles within their lane, arranged left to right.
- Vertical arrows cross lane boundaries for inter-lane communication.
- Lane spacing: 20px gap between lanes.
- Canvas: 1200-1600w x (lane_count * 180 + 200)h.
- Colors: lane borders = grey dashed. Steps colored by semantic role within each lane.

---

## 4. Flowchart with Decisions

**When to use:** Conditional branching, yes/no gates, approval workflows, process logic with branches.

**Flow direction:** Top-to-bottom, with horizontal branching at decision points.

**Layout:**
```
        (Start)
           ↓
      [Process A]
           ↓
        ◇ Check? ◇
       / Yes    \ No
  [Path A]    [Path B]
       \        /
        ↓      ↓
      [Merge Point]
           ↓
        (End)
```

- Start/end: ellipses, green and red respectively.
- Processes: rectangles, blue.
- Decisions: diamonds, yellow (#fff3bf / #e67700).
- Branch labels: standalone text ("Yes" / "No") positioned near the arrow start, `fontSize: 12`.
- Arrows from diamond corners go left and right for branches.
- Branches can reconverge to a merge point below.
- Canvas: 800-1200w x (depth * 120)h.
- Decision diamonds: 140x100 size (wider for readability).
- Spacing: 100px vertical between steps, 200px horizontal between branches.

---

## 5. Entity-Relationship

**When to use:** Data models, entities with named relationships, database schemas, domain models.

**Flow direction:** Free-form, minimize arrow crossings.

**Layout:**
```
[Entity A]          [Entity B]
  │  "has many"         │
  └────────────────────→│
                        │  "belongs to"
  [Entity C] ←─────────┘
```

- Entities: rectangles with multi-line text (entity name on line 1, key attributes on lines 2+).
- Entity boxes: 200-240w x 100-140h (taller for more attributes).
- Relationships: arrows with label text positioned at midpoint.
- Cardinality notation: use arrowhead types — `"arrow"` for one-to-many, `"dot"` for many, `"bar"` for one.
- Arrange entities to minimize crossing arrows. Place heavily-connected entities in the center.
- Canvas: 1000-1400w x 600-900h.
- Colors: all entities in blue. Junction/association tables in orange. Use purple for computed/virtual entities.

---

## 6. Layered Architecture

**When to use:** Technology stacks, abstraction layers, tiered systems (UI → API → DB).

**Flow direction:** Top-to-bottom (user-facing at top, infrastructure at bottom).

**Layout:**
```
╔═══════════════════════════════════════╗
║  PRESENTATION  [React] [Mobile App]  ║
╠═══════════════════════════════════════╣
║  API LAYER     [REST API] [GraphQL]  ║
╠═══════════════════════════════════════╣
║  BUSINESS      [Auth] [Payments]     ║
╠═══════════════════════════════════════╣
║  DATA          [Postgres] [Redis]    ║
╚═══════════════════════════════════════╝
```

- Each layer: full-width dashed rectangle (760-1000w x 100-120h).
- Layer label: standalone text at left, `fontSize: 14`, grey stroke.
- Components within each layer: smaller rectangles (140-160w x 50-60h), arranged horizontally.
- Vertical arrows between components in adjacent layers.
- Layer spacing: 20px between layer boundaries.
- Canvas: 800-1100w x (layer_count * 140 + 150)h.
- Colors: top layers = blue (user-facing), middle = orange (business logic), bottom = green (data/infra). AI components = purple regardless of layer.

---

## 7. Network / Graph

**When to use:** Many-to-many connections, no clear hierarchy, microservices, peer-to-peer systems, integration maps.

**Flow direction:** No primary direction. Radial or force-directed placement.

**Layout:**
```
        [Service A]
       ↗     ↕     ↘
 [Svc B]  [Hub]  [Svc C]
       ↘     ↕     ↗
        [Service D]
```

- Central hub(s) in the middle, larger (220x90).
- Connected nodes radiate outward. Place at roughly equal angular spacing.
- Peripheral nodes: standard size (180x70).
- Minimize arrow crossings by adjusting node positions.
- Use multi-segment arrows for paths that would otherwise cross.
- Canvas: 1200-1600w x 800-1200h (roughly square).
- Colors by category/domain. Use dashed boundary boxes to group related services.
- If >10 nodes, create clusters with boundary boxes and minimize inter-cluster connections.

---

## 8. Quadrant / Matrix

**When to use:** 2-axis comparison, prioritization (effort vs impact), categorization, risk assessment.

**Flow direction:** None — items placed within their quadrant.

**Layout:**
```
  HIGH IMPACT
  ┌─────────────┬─────────────┐
  │ Quick Wins  │ Major       │
  │  • Item A   │ Projects    │
  │  • Item B   │  • Item E   │
  ├─────────────┼─────────────┤
  │ Fill-ins    │ Money Pit   │
  │  • Item C   │  • Item F   │
  │  • Item D   │             │
  └─────────────┴─────────────┘
  LOW EFFORT ────── HIGH EFFORT
```

- Two axis lines (use arrows with `startArrowhead: null`, `endArrowhead: "triangle"`):
  - Horizontal: full width at vertical center
  - Vertical: full height at horizontal center
- Axis labels: standalone text at each end of each axis, `fontSize: 14`.
- Quadrant labels: standalone text in each quadrant corner, `fontSize: 16`, semi-bold appearance.
- Items: small rectangles (160x50) or standalone text within their quadrant.
- Canvas: 900x900 (square proportions).
- Colors: top-left (high value/low effort) = green. Top-right = blue. Bottom-left = orange. Bottom-right = red.
- 3-5 items per quadrant max for readability.

---

## 9. Sequence-style

**When to use:** Time-ordered interactions between actors, API call sequences, message passing, request/response flows.

**Flow direction:** Top-to-bottom (time axis), left-to-right (actors).

**Layout:**
```
 [Actor A]    [Actor B]    [Actor C]
    │             │             │
    │──Request──→│             │
    │             │──Forward──→│
    │             │←──Reply────│
    │←──Response──│             │
    │             │             │
```

- Actor boxes: rectangles at the top, 160x60, spaced 200px apart horizontally.
- Lifelines: dashed vertical lines (arrows with `strokeStyle: "dashed"`, `startArrowhead: null`, `endArrowhead: null`) from each actor downward.
- Messages: horizontal arrows between lifelines, ordered top-to-bottom.
- Message labels: standalone text above each arrow, `fontSize: 12`.
- Vertical spacing: 60-80px between messages.
- Canvas: (actor_count * 220 + 100)w x (message_count * 80 + 250)h.
- Colors: actors = blue. Request arrows = default. Response arrows = green stroke. Async = dashed arrow.

---

## 10. Mind Map

**When to use:** Central concept with radiating topics, brainstorming, concept exploration, feature breakdown.

**Flow direction:** Center-outward (radial).

**Layout:**
```
              [Branch A]
             ↗
[Branch D] ← [CENTER] → [Branch B]
             ↘
              [Branch C]
                ↘
              [Sub C1]
```

- Central node: large rectangle (240x100), centered on canvas.
- Primary branches: medium rectangles (180x70), positioned at even angular spacing around center.
- Secondary branches: smaller rectangles (140x50), extending outward from their parent branch.
- Arrows from center to each primary branch. Arrows from primary to secondary branches.
- Canvas: 1400x1000 minimum (wide for horizontal spread).
- Spacing: primary branches ~300px from center. Secondary branches ~200px from their parent.
- Colors: center = primary blue. Each primary branch gets its own color from the palette. Secondary branches use the same color as their parent but lighter (or same with lower opacity).
- Max 6-8 primary branches. Max 3-4 secondary per primary.

---

## Choosing Between Patterns

When the content could fit multiple patterns, prefer the one where:
1. The primary relationships (the most important thing to communicate) are most visible.
2. The viewer can understand the main structure in <5 seconds.
3. The layout minimizes arrow crossings and visual noise.

If in doubt: hierarchy for parent-child, pipeline for sequential, flowchart for conditional, network for peer-to-peer.
