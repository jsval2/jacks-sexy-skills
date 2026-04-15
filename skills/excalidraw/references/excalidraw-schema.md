# Excalidraw JSON Schema Reference

Generate valid Excalidraw JSON that can be imported directly into Excalidraw or pasted from clipboard.

---

## Table of Contents

1. [Clipboard Wrapper](#clipboard-wrapper)
2. [Base Properties](#base-properties)
3. [Element Types](#element-types)
4. [Text Inside Shapes](#text-inside-shapes)
5. [Connected Arrows](#connected-arrows)
6. [Multi-Segment Arrows](#multi-segment-arrows)
7. [Frames](#frames)
8. [Grouping](#grouping)
9. [Stroke Styles](#stroke-styles)
10. [Arrowhead Types](#arrowhead-types)
11. [Shape Usage Guide](#shape-usage-guide)
12. [Text Sizing Guide](#text-sizing-guide)
13. [Boundary / Container Pattern](#boundary-container-pattern)
14. [Color Palette](#color-palette)
15. [Canvas & Coordinate System](#canvas-coordinate-system)
16. [Layout Guidelines](#layout-guidelines)

---

## Clipboard Wrapper

```json
{
  "type": "excalidraw/clipboard",
  "elements": [ ... ],
  "files": {}
}
```

---

## Base Properties

Every element requires these fields:

```json
{
  "type": "rectangle",
  "id": "unique-id",
  "x": 100,
  "y": 100,
  "width": 200,
  "height": 80,
  "angle": 0,
  "strokeColor": "#1e1e1e",
  "backgroundColor": "#a5d8ff",
  "fillStyle": "solid",
  "strokeWidth": 2,
  "strokeStyle": "solid",
  "roughness": 1,
  "opacity": 100,
  "seed": 12345,
  "version": 1,
  "versionNonce": 12345,
  "isDeleted": false,
  "groupIds": [],
  "boundElements": null,
  "link": null,
  "locked": false
}
```

- `id`: Any unique string. Use readable IDs: `"rect-auth"`, `"arrow-auth-db"`, `"text-title"`.
- `seed` / `versionNonce`: Any integer. Affects hand-drawn rendering variation.
- `roughness`: `0` = clean lines, `1` = hand-drawn (default), `2` = very rough.
- `roundness`: Add `"roundness": { "type": 3 }` for rounded corners on rectangles.

---

## Element Types

### Rectangle / Ellipse / Diamond

No extra fields beyond base. Set `"type"` to `"rectangle"`, `"ellipse"`, or `"diamond"`.

### Text

Additional required fields:

```json
{
  "type": "text",
  "text": "Label Here",
  "fontSize": 16,
  "fontFamily": 2,
  "textAlign": "center",
  "verticalAlign": "middle",
  "containerId": null,
  "originalText": "Label Here",
  "autoResize": true,
  "lineHeight": 1.25
}
```

- `fontFamily`: `1` = Virgil (hand-drawn), `2` = Helvetica, `3` = Cascadia (mono).
- `containerId`: Set to a shape's `id` to bind text inside it. `null` for standalone.
- Use `\n` for line breaks in `text` and `originalText`.

### Arrow / Line

Additional required fields:

```json
{
  "type": "arrow",
  "points": [[0, 0], [200, 0]],
  "startArrowhead": null,
  "endArrowhead": "arrow",
  "startBinding": { "elementId": "rect-1", "focus": 0, "gap": 5 },
  "endBinding": { "elementId": "rect-2", "focus": 0, "gap": 5 }
}
```

- `points`: Offsets from `(x, y)`. First point always `[0, 0]`.
- `width`/`height` must match the bounding box of points.
- `focus`: `-1` to `1`. `0` = center of bound element.
- `gap`: Pixels between arrow endpoint and shape edge. Use `5`.
- Set `startBinding` / `endBinding` to `null` for unconnected ends.

---

## Text Inside Shapes (Bound Text)

Two-element system: a container shape + a text element referencing it.

**Container shape** must list the text in `boundElements`:
```json
"boundElements": [
  { "id": "text-auth", "type": "text" }
]
```

**Text element** must set:
```json
"containerId": "rect-auth",
"textAlign": "center",
"verticalAlign": "middle"
```

Position text approximately centered: `text.x = shape.x + (shape.width - text.width) / 2`.

---

## Connected Arrows

Bidirectional references required:

1. Each connected shape lists the arrow in `boundElements` with `"type": "arrow"`
2. Arrow's `startBinding.elementId` references source shape
3. Arrow's `endBinding.elementId` references target shape

Both the source and target shapes must include the arrow ID in their `boundElements` array.

---

## Multi-Segment Arrows

For routed paths (L-shapes, Z-shapes, bypasses), use 3+ points:

```json
{
  "type": "arrow",
  "points": [[0, 0], [100, 0], [100, 80], [200, 80]],
  "width": 200,
  "height": 80
}
```

This creates an arrow that goes right, then down, then right again.

- `width` = max x offset across all points.
- `height` = max y offset across all points (use absolute values).
- Each point is an offset from the arrow's `(x, y)` position.
- First point is always `[0, 0]`.

---

## Frames

Frames create labeled container regions. Child elements visually clip to the frame.

```json
{
  "type": "frame",
  "id": "frame-backend",
  "name": "Backend Services",
  "x": 50,
  "y": 100,
  "width": 600,
  "height": 300
}
```

- `name`: Displayed as a label above the frame.
- Elements inside the frame area are visually grouped.
- Frames have a subtle border and label — use for high-level grouping.

---

## Grouping

Elements sharing a `groupIds` entry move and select together:

```json
// Element A
"groupIds": ["group-auth"]

// Element B
"groupIds": ["group-auth"]
```

- Multiple elements can share the same group ID.
- An element can belong to multiple groups (nested grouping).
- Use for keeping related elements together (a boundary box + its label + its children).

---

## Stroke Styles

Set via `strokeStyle` on any element:

| Value | Visual | When to use |
|---|---|---|
| `"solid"` | ─────── | Default. Primary connections, data flow, main components |
| `"dashed"` | - - - - | Boundaries, optional/async paths, grouping regions, planned connections |
| `"dotted"` | · · · · · | Weak relationships, future/planned items, metadata links |

---

## Arrowhead Types

Set via `startArrowhead` and `endArrowhead`:

| Value | Visual | When to use |
|---|---|---|
| `null` | No head | Undirected connections, lines. Pair with another arrow for bidirectional |
| `"arrow"` | ▷ | Standard directional flow (default) |
| `"triangle"` | ▶ | Strong/definitive flow, primary data path |
| `"dot"` | ● | Data/event emission, publish/subscribe |
| `"bar"` | \| | Termination, end states, constraints |

For bidirectional arrows: set both `startArrowhead` and `endArrowhead`.

---

## Shape Usage Guide

| Shape | When to use |
|---|---|
| **Rectangle** | Processes, components, services, data stores, APIs, generic nodes |
| **Ellipse** | States (in state machines), start/end points, events, milestones |
| **Diamond** | Decisions, conditions, branch points, yes/no gates |

Default to rectangle. Only use ellipse/diamond when the content semantically calls for it.

---

## Text Sizing Guide

| Purpose | fontSize | Style | Binding |
|---|---|---|---|
| Diagram title | 24 | Standalone, `textAlign: "left"` | `containerId: null` |
| Section labels | 12 | Standalone, grey stroke (`#868e96`) | `containerId: null` |
| Node labels | 14-16 | Bound to container, centered | `containerId: "shape-id"` |
| Annotations | 12 | Standalone, positioned near relevant element | `containerId: null` |
| Arrow labels | 12-14 | Standalone, positioned above arrow midpoint | `containerId: null` |

---

## Boundary / Container Pattern

For grouping related elements with a visible region:

1. Create a large dashed rectangle as the boundary:
```json
{
  "type": "rectangle",
  "strokeStyle": "dashed",
  "backgroundColor": "#f8f9fa",
  "fillStyle": "solid",
  "strokeColor": "#1e1e1e"
}
```

2. Add a section label at the top-left corner:
```json
{
  "type": "text",
  "text": "SECTION NAME",
  "fontSize": 12,
  "strokeColor": "#868e96",
  "containerId": null
}
```

3. Position child elements inside the boundary rectangle.
4. Optionally share a `groupIds` entry across the boundary, label, and children.

---

## Color Palette

| Semantic Role | Background | Stroke | When to use |
|---|---|---|---|
| Input / Source | `#a5d8ff` (blue) | `#1e1e1e` | Data sources, entry points, triggers, user actions |
| Core Processing | `#a5d8ff` (blue) | `#1e1e1e` | Main system components, primary services |
| AI / Intelligence | `#e5dbff` (purple) | `#6741d9` | LLM calls, ML models, AI agents, smart logic |
| Automation / Infra | `#ffe8cc` (orange) | `#e8590c` | Orchestration, pipelines, queues, middleware |
| Output / Delivery | `#b2f2bb` (green) | `#1e1e1e` | Results, destinations, endpoints, final stores |
| Warning / Human | `#ffc9c9` (red) | `#c92a2a` | Manual steps, errors, edge cases, review queues |
| Container / Boundary | `#f8f9fa` (grey) | `#1e1e1e` | Grouping regions, swimlane headers, frames |
| Decision | `#fff3bf` (yellow) | `#e67700` | Diamond shapes, yes/no gates, conditional branches |
| Arrows / Lines | `transparent` | `#1e1e1e` | Default connections. Use semantic stroke color for typed connections |

---

## Canvas & Coordinate System

- `x` increases rightward, `y` increases downward.
- Origin `(0, 0)` is top-left.
- Recommended starting position: title at `y: 30-80`, first row of elements at `y: 120-200`.
- Canvas sizes by complexity:
  - **Small** (3-6 nodes): ~800 x 500
  - **Medium** (7-12 nodes): ~1400 x 700
  - **Large** (13-20 nodes): ~1800 x 900+

---

## Layout Guidelines

- **Box size:** 160-200w x 70-80h for standard nodes. Use 220x90 for primary/important nodes.
- **Spacing:** ~100px horizontal gap between boxes, ~80px vertical gap.
- **Full-width bars:** 760w x 80h for cross-cutting layers.
- **Flow direction:** Left-to-right for sequential, top-to-bottom for hierarchy.
- **Arrows:** Place arrow `x,y` at the edge of the source shape. Match `width`/`height` to point offsets.
- **Title:** Always include a title text element at the top with `fontSize: 24`.
- **Whitespace:** Dense = related. Spaced = independent. Use whitespace as information.

---

## Generating the File

1. Generate valid JSON following this schema.
2. Verify all bindings reference existing element IDs.
3. Save to the specified output path as `.excalidraw.json`.
4. Tell the user the file path and how to import into Excalidraw.
