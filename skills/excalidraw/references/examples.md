# Excalidraw Examples

Three annotated examples demonstrating patterns beyond basic left-to-right pipelines. Each is a complete, valid Excalidraw clipboard JSON.

---

## Example 1: Flowchart with Decision Diamond

A simple approval workflow: submit → review → approved? → yes/no branches.

Demonstrates: ellipse for start/end, diamond for decisions, branching arrows, yellow decision color, branch labels.

```json
{
  "type": "excalidraw/clipboard",
  "elements": [
    {
      "type": "text", "id": "title", "x": 60, "y": 30, "width": 400, "height": 30,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 100, "version": 1, "versionNonce": 100,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "text": "Document Approval Workflow", "fontSize": 24, "fontFamily": 2,
      "textAlign": "left", "verticalAlign": "top", "containerId": null,
      "originalText": "Document Approval Workflow", "autoResize": true, "lineHeight": 1.25
    },

    {
      "type": "ellipse", "id": "start", "x": 200, "y": 100, "width": 120, "height": 60,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "#b2f2bb",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 200, "version": 1, "versionNonce": 200,
      "isDeleted": false, "groupIds": [],
      "boundElements": [
        { "id": "text-start", "type": "text" },
        { "id": "arrow-start-submit", "type": "arrow" }
      ],
      "link": null, "locked": false
    },
    {
      "type": "text", "id": "text-start", "x": 225, "y": 118, "width": 70, "height": 25,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 201, "version": 1, "versionNonce": 201,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "text": "Start", "fontSize": 16, "fontFamily": 2,
      "textAlign": "center", "verticalAlign": "middle", "containerId": "start",
      "originalText": "Start", "autoResize": true, "lineHeight": 1.25
    },

    {
      "type": "rectangle", "id": "submit", "x": 190, "y": 220, "width": 140, "height": 70,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "#a5d8ff",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 300, "version": 1, "versionNonce": 300,
      "isDeleted": false, "groupIds": [],
      "boundElements": [
        { "id": "text-submit", "type": "text" },
        { "id": "arrow-start-submit", "type": "arrow" },
        { "id": "arrow-submit-review", "type": "arrow" }
      ],
      "link": null, "locked": false, "roundness": { "type": 3 }
    },
    {
      "type": "text", "id": "text-submit", "x": 210, "y": 243, "width": 100, "height": 25,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 301, "version": 1, "versionNonce": 301,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "text": "Submit Doc", "fontSize": 16, "fontFamily": 2,
      "textAlign": "center", "verticalAlign": "middle", "containerId": "submit",
      "originalText": "Submit Doc", "autoResize": true, "lineHeight": 1.25
    },

    {
      "type": "diamond", "id": "decision", "x": 185, "y": 360, "width": 150, "height": 100,
      "angle": 0, "strokeColor": "#e67700", "backgroundColor": "#fff3bf",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 400, "version": 1, "versionNonce": 400,
      "isDeleted": false, "groupIds": [],
      "boundElements": [
        { "id": "text-decision", "type": "text" },
        { "id": "arrow-submit-review", "type": "arrow" },
        { "id": "arrow-yes", "type": "arrow" },
        { "id": "arrow-no", "type": "arrow" }
      ],
      "link": null, "locked": false
    },
    {
      "type": "text", "id": "text-decision", "x": 215, "y": 398, "width": 90, "height": 25,
      "angle": 0, "strokeColor": "#e67700", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 401, "version": 1, "versionNonce": 401,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "text": "Approved?", "fontSize": 16, "fontFamily": 2,
      "textAlign": "center", "verticalAlign": "middle", "containerId": "decision",
      "originalText": "Approved?", "autoResize": true, "lineHeight": 1.25
    },

    {
      "type": "rectangle", "id": "publish", "x": 40, "y": 530, "width": 140, "height": 70,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "#b2f2bb",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 500, "version": 1, "versionNonce": 500,
      "isDeleted": false, "groupIds": [],
      "boundElements": [
        { "id": "text-publish", "type": "text" },
        { "id": "arrow-yes", "type": "arrow" }
      ],
      "link": null, "locked": false, "roundness": { "type": 3 }
    },
    {
      "type": "text", "id": "text-publish", "x": 75, "y": 553, "width": 70, "height": 25,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 501, "version": 1, "versionNonce": 501,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "text": "Publish", "fontSize": 16, "fontFamily": 2,
      "textAlign": "center", "verticalAlign": "middle", "containerId": "publish",
      "originalText": "Publish", "autoResize": true, "lineHeight": 1.25
    },

    {
      "type": "rectangle", "id": "revise", "x": 340, "y": 530, "width": 140, "height": 70,
      "angle": 0, "strokeColor": "#c92a2a", "backgroundColor": "#ffc9c9",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 600, "version": 1, "versionNonce": 600,
      "isDeleted": false, "groupIds": [],
      "boundElements": [
        { "id": "text-revise", "type": "text" },
        { "id": "arrow-no", "type": "arrow" }
      ],
      "link": null, "locked": false, "roundness": { "type": 3 }
    },
    {
      "type": "text", "id": "text-revise", "x": 370, "y": 553, "width": 80, "height": 25,
      "angle": 0, "strokeColor": "#c92a2a", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 601, "version": 1, "versionNonce": 601,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "text": "Revise", "fontSize": 16, "fontFamily": 2,
      "textAlign": "center", "verticalAlign": "middle", "containerId": "revise",
      "originalText": "Revise", "autoResize": true, "lineHeight": 1.25
    },

    {
      "type": "arrow", "id": "arrow-start-submit",
      "x": 260, "y": 160, "width": 0, "height": 60,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 700, "version": 1, "versionNonce": 700,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "points": [[0, 0], [0, 60]],
      "startArrowhead": null, "endArrowhead": "arrow",
      "startBinding": { "elementId": "start", "focus": 0, "gap": 5 },
      "endBinding": { "elementId": "submit", "focus": 0, "gap": 5 }
    },
    {
      "type": "arrow", "id": "arrow-submit-review",
      "x": 260, "y": 290, "width": 0, "height": 70,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 701, "version": 1, "versionNonce": 701,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "points": [[0, 0], [0, 70]],
      "startArrowhead": null, "endArrowhead": "arrow",
      "startBinding": { "elementId": "submit", "focus": 0, "gap": 5 },
      "endBinding": { "elementId": "decision", "focus": 0, "gap": 5 }
    },
    {
      "type": "arrow", "id": "arrow-yes",
      "x": 185, "y": 440, "width": 75, "height": 90,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 702, "version": 1, "versionNonce": 702,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "points": [[0, 0], [-75, 90]],
      "startArrowhead": null, "endArrowhead": "arrow",
      "startBinding": { "elementId": "decision", "focus": 0, "gap": 5 },
      "endBinding": { "elementId": "publish", "focus": 0, "gap": 5 }
    },
    {
      "type": "arrow", "id": "arrow-no",
      "x": 335, "y": 440, "width": 75, "height": 90,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 703, "version": 1, "versionNonce": 703,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "points": [[0, 0], [75, 90]],
      "startArrowhead": null, "endArrowhead": "arrow",
      "startBinding": { "elementId": "decision", "focus": 0, "gap": 5 },
      "endBinding": { "elementId": "revise", "focus": 0, "gap": 5 }
    },

    {
      "type": "text", "id": "label-yes", "x": 90, "y": 475, "width": 30, "height": 20,
      "angle": 0, "strokeColor": "#2b8a3e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 800, "version": 1, "versionNonce": 800,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "text": "Yes", "fontSize": 14, "fontFamily": 2,
      "textAlign": "center", "verticalAlign": "top", "containerId": null,
      "originalText": "Yes", "autoResize": true, "lineHeight": 1.25
    },
    {
      "type": "text", "id": "label-no", "x": 385, "y": 475, "width": 25, "height": 20,
      "angle": 0, "strokeColor": "#c92a2a", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 801, "version": 1, "versionNonce": 801,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "text": "No", "fontSize": 14, "fontFamily": 2,
      "textAlign": "center", "verticalAlign": "top", "containerId": null,
      "originalText": "No", "autoResize": true, "lineHeight": 1.25
    }
  ],
  "files": {}
}
```

---

## Example 2: Layered Architecture with Boundaries

A 3-tier stack with component boxes inside each layer.

Demonstrates: dashed boundary rectangles, section labels, varied component sizes within layers, vertical arrows between layers.

```json
{
  "type": "excalidraw/clipboard",
  "elements": [
    {
      "type": "text", "id": "title", "x": 60, "y": 30, "width": 300, "height": 30,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 100, "version": 1, "versionNonce": 100,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "text": "Application Architecture", "fontSize": 24, "fontFamily": 2,
      "textAlign": "left", "verticalAlign": "top", "containerId": null,
      "originalText": "Application Architecture", "autoResize": true, "lineHeight": 1.25
    },

    {
      "type": "rectangle", "id": "layer-ui", "x": 60, "y": 90, "width": 700, "height": 120,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "#f8f9fa",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "dashed", "roughness": 1,
      "opacity": 100, "seed": 200, "version": 1, "versionNonce": 200,
      "isDeleted": false, "groupIds": ["group-ui"], "boundElements": null,
      "link": null, "locked": false, "roundness": { "type": 3 }
    },
    {
      "type": "text", "id": "label-ui", "x": 75, "y": 95, "width": 100, "height": 20,
      "angle": 0, "strokeColor": "#868e96", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 201, "version": 1, "versionNonce": 201,
      "isDeleted": false, "groupIds": ["group-ui"], "boundElements": null,
      "link": null, "locked": false,
      "text": "PRESENTATION", "fontSize": 12, "fontFamily": 2,
      "textAlign": "left", "verticalAlign": "top", "containerId": null,
      "originalText": "PRESENTATION", "autoResize": true, "lineHeight": 1.25
    },
    {
      "type": "rectangle", "id": "react", "x": 100, "y": 125, "width": 150, "height": 60,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "#a5d8ff",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 210, "version": 1, "versionNonce": 210,
      "isDeleted": false, "groupIds": ["group-ui"],
      "boundElements": [
        { "id": "text-react", "type": "text" },
        { "id": "arrow-react-api", "type": "arrow" }
      ],
      "link": null, "locked": false, "roundness": { "type": 3 }
    },
    {
      "type": "text", "id": "text-react", "x": 130, "y": 143, "width": 90, "height": 25,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 211, "version": 1, "versionNonce": 211,
      "isDeleted": false, "groupIds": ["group-ui"], "boundElements": null,
      "link": null, "locked": false,
      "text": "React App", "fontSize": 16, "fontFamily": 2,
      "textAlign": "center", "verticalAlign": "middle", "containerId": "react",
      "originalText": "React App", "autoResize": true, "lineHeight": 1.25
    },

    {
      "type": "rectangle", "id": "layer-api", "x": 60, "y": 230, "width": 700, "height": 120,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "#f8f9fa",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "dashed", "roughness": 1,
      "opacity": 100, "seed": 300, "version": 1, "versionNonce": 300,
      "isDeleted": false, "groupIds": ["group-api"], "boundElements": null,
      "link": null, "locked": false, "roundness": { "type": 3 }
    },
    {
      "type": "text", "id": "label-api", "x": 75, "y": 235, "width": 80, "height": 20,
      "angle": 0, "strokeColor": "#868e96", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 301, "version": 1, "versionNonce": 301,
      "isDeleted": false, "groupIds": ["group-api"], "boundElements": null,
      "link": null, "locked": false,
      "text": "API LAYER", "fontSize": 12, "fontFamily": 2,
      "textAlign": "left", "verticalAlign": "top", "containerId": null,
      "originalText": "API LAYER", "autoResize": true, "lineHeight": 1.25
    },
    {
      "type": "rectangle", "id": "rest-api", "x": 100, "y": 265, "width": 150, "height": 60,
      "angle": 0, "strokeColor": "#e8590c", "backgroundColor": "#ffe8cc",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 310, "version": 1, "versionNonce": 310,
      "isDeleted": false, "groupIds": ["group-api"],
      "boundElements": [
        { "id": "text-rest-api", "type": "text" },
        { "id": "arrow-react-api", "type": "arrow" },
        { "id": "arrow-api-db", "type": "arrow" }
      ],
      "link": null, "locked": false, "roundness": { "type": 3 }
    },
    {
      "type": "text", "id": "text-rest-api", "x": 125, "y": 283, "width": 100, "height": 25,
      "angle": 0, "strokeColor": "#e8590c", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 311, "version": 1, "versionNonce": 311,
      "isDeleted": false, "groupIds": ["group-api"], "boundElements": null,
      "link": null, "locked": false,
      "text": "REST API", "fontSize": 16, "fontFamily": 2,
      "textAlign": "center", "verticalAlign": "middle", "containerId": "rest-api",
      "originalText": "REST API", "autoResize": true, "lineHeight": 1.25
    },

    {
      "type": "rectangle", "id": "layer-data", "x": 60, "y": 370, "width": 700, "height": 120,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "#f8f9fa",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "dashed", "roughness": 1,
      "opacity": 100, "seed": 400, "version": 1, "versionNonce": 400,
      "isDeleted": false, "groupIds": ["group-data"], "boundElements": null,
      "link": null, "locked": false, "roundness": { "type": 3 }
    },
    {
      "type": "text", "id": "label-data", "x": 75, "y": 375, "width": 80, "height": 20,
      "angle": 0, "strokeColor": "#868e96", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 401, "version": 1, "versionNonce": 401,
      "isDeleted": false, "groupIds": ["group-data"], "boundElements": null,
      "link": null, "locked": false,
      "text": "DATA LAYER", "fontSize": 12, "fontFamily": 2,
      "textAlign": "left", "verticalAlign": "top", "containerId": null,
      "originalText": "DATA LAYER", "autoResize": true, "lineHeight": 1.25
    },
    {
      "type": "rectangle", "id": "postgres", "x": 100, "y": 405, "width": 150, "height": 60,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "#b2f2bb",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 410, "version": 1, "versionNonce": 410,
      "isDeleted": false, "groupIds": ["group-data"],
      "boundElements": [
        { "id": "text-postgres", "type": "text" },
        { "id": "arrow-api-db", "type": "arrow" }
      ],
      "link": null, "locked": false, "roundness": { "type": 3 }
    },
    {
      "type": "text", "id": "text-postgres", "x": 125, "y": 423, "width": 100, "height": 25,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 411, "version": 1, "versionNonce": 411,
      "isDeleted": false, "groupIds": ["group-data"], "boundElements": null,
      "link": null, "locked": false,
      "text": "PostgreSQL", "fontSize": 16, "fontFamily": 2,
      "textAlign": "center", "verticalAlign": "middle", "containerId": "postgres",
      "originalText": "PostgreSQL", "autoResize": true, "lineHeight": 1.25
    },
    {
      "type": "rectangle", "id": "redis", "x": 300, "y": 405, "width": 150, "height": 60,
      "angle": 0, "strokeColor": "#c92a2a", "backgroundColor": "#ffc9c9",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 420, "version": 1, "versionNonce": 420,
      "isDeleted": false, "groupIds": ["group-data"],
      "boundElements": [
        { "id": "text-redis", "type": "text" }
      ],
      "link": null, "locked": false, "roundness": { "type": 3 }
    },
    {
      "type": "text", "id": "text-redis", "x": 335, "y": 423, "width": 80, "height": 25,
      "angle": 0, "strokeColor": "#c92a2a", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 421, "version": 1, "versionNonce": 421,
      "isDeleted": false, "groupIds": ["group-data"], "boundElements": null,
      "link": null, "locked": false,
      "text": "Redis", "fontSize": 16, "fontFamily": 2,
      "textAlign": "center", "verticalAlign": "middle", "containerId": "redis",
      "originalText": "Redis", "autoResize": true, "lineHeight": 1.25
    },

    {
      "type": "arrow", "id": "arrow-react-api",
      "x": 175, "y": 185, "width": 0, "height": 80,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 500, "version": 1, "versionNonce": 500,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "points": [[0, 0], [0, 80]],
      "startArrowhead": null, "endArrowhead": "arrow",
      "startBinding": { "elementId": "react", "focus": 0, "gap": 5 },
      "endBinding": { "elementId": "rest-api", "focus": 0, "gap": 5 }
    },
    {
      "type": "arrow", "id": "arrow-api-db",
      "x": 175, "y": 325, "width": 0, "height": 80,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 501, "version": 1, "versionNonce": 501,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "points": [[0, 0], [0, 80]],
      "startArrowhead": null, "endArrowhead": "arrow",
      "startBinding": { "elementId": "rest-api", "focus": 0, "gap": 5 },
      "endBinding": { "elementId": "postgres", "focus": 0, "gap": 5 }
    }
  ],
  "files": {}
}
```

---

## Example 3: Three-Level Hierarchy

A simple org/taxonomy tree: root → 3 children → 2 grandchildren.

Demonstrates: top-to-bottom layout, centered children under parents, consistent vertical spacing, size hierarchy.

```json
{
  "type": "excalidraw/clipboard",
  "elements": [
    {
      "type": "text", "id": "title", "x": 200, "y": 20, "width": 250, "height": 30,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 100, "version": 1, "versionNonce": 100,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "text": "Team Structure", "fontSize": 24, "fontFamily": 2,
      "textAlign": "left", "verticalAlign": "top", "containerId": null,
      "originalText": "Team Structure", "autoResize": true, "lineHeight": 1.25
    },

    {
      "type": "rectangle", "id": "root", "x": 230, "y": 80, "width": 200, "height": 80,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "#a5d8ff",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 200, "version": 1, "versionNonce": 200,
      "isDeleted": false, "groupIds": [],
      "boundElements": [
        { "id": "text-root", "type": "text" },
        { "id": "arrow-root-a", "type": "arrow" },
        { "id": "arrow-root-b", "type": "arrow" },
        { "id": "arrow-root-c", "type": "arrow" }
      ],
      "link": null, "locked": false, "roundness": { "type": 3 }
    },
    {
      "type": "text", "id": "text-root", "x": 280, "y": 108, "width": 100, "height": 25,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 201, "version": 1, "versionNonce": 201,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "text": "CEO", "fontSize": 16, "fontFamily": 2,
      "textAlign": "center", "verticalAlign": "middle", "containerId": "root",
      "originalText": "CEO", "autoResize": true, "lineHeight": 1.25
    },

    {
      "type": "rectangle", "id": "child-a", "x": 30, "y": 250, "width": 170, "height": 70,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "#b2f2bb",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 300, "version": 1, "versionNonce": 300,
      "isDeleted": false, "groupIds": [],
      "boundElements": [
        { "id": "text-child-a", "type": "text" },
        { "id": "arrow-root-a", "type": "arrow" },
        { "id": "arrow-a-a1", "type": "arrow" },
        { "id": "arrow-a-a2", "type": "arrow" }
      ],
      "link": null, "locked": false, "roundness": { "type": 3 }
    },
    {
      "type": "text", "id": "text-child-a", "x": 60, "y": 273, "width": 110, "height": 25,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 301, "version": 1, "versionNonce": 301,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "text": "VP Product", "fontSize": 16, "fontFamily": 2,
      "textAlign": "center", "verticalAlign": "middle", "containerId": "child-a",
      "originalText": "VP Product", "autoResize": true, "lineHeight": 1.25
    },

    {
      "type": "rectangle", "id": "child-b", "x": 245, "y": 250, "width": 170, "height": 70,
      "angle": 0, "strokeColor": "#6741d9", "backgroundColor": "#e5dbff",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 400, "version": 1, "versionNonce": 400,
      "isDeleted": false, "groupIds": [],
      "boundElements": [
        { "id": "text-child-b", "type": "text" },
        { "id": "arrow-root-b", "type": "arrow" }
      ],
      "link": null, "locked": false, "roundness": { "type": 3 }
    },
    {
      "type": "text", "id": "text-child-b", "x": 270, "y": 273, "width": 120, "height": 25,
      "angle": 0, "strokeColor": "#6741d9", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 401, "version": 1, "versionNonce": 401,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "text": "VP Engineering", "fontSize": 16, "fontFamily": 2,
      "textAlign": "center", "verticalAlign": "middle", "containerId": "child-b",
      "originalText": "VP Engineering", "autoResize": true, "lineHeight": 1.25
    },

    {
      "type": "rectangle", "id": "child-c", "x": 460, "y": 250, "width": 170, "height": 70,
      "angle": 0, "strokeColor": "#e8590c", "backgroundColor": "#ffe8cc",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 500, "version": 1, "versionNonce": 500,
      "isDeleted": false, "groupIds": [],
      "boundElements": [
        { "id": "text-child-c", "type": "text" },
        { "id": "arrow-root-c", "type": "arrow" }
      ],
      "link": null, "locked": false, "roundness": { "type": 3 }
    },
    {
      "type": "text", "id": "text-child-c", "x": 500, "y": 273, "width": 90, "height": 25,
      "angle": 0, "strokeColor": "#e8590c", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 501, "version": 1, "versionNonce": 501,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "text": "VP Sales", "fontSize": 16, "fontFamily": 2,
      "textAlign": "center", "verticalAlign": "middle", "containerId": "child-c",
      "originalText": "VP Sales", "autoResize": true, "lineHeight": 1.25
    },

    {
      "type": "rectangle", "id": "grandchild-a1", "x": 0, "y": 410, "width": 140, "height": 55,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "#b2f2bb",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 600, "version": 1, "versionNonce": 600,
      "isDeleted": false, "groupIds": [],
      "boundElements": [
        { "id": "text-a1", "type": "text" },
        { "id": "arrow-a-a1", "type": "arrow" }
      ],
      "link": null, "locked": false, "roundness": { "type": 3 }
    },
    {
      "type": "text", "id": "text-a1", "x": 15, "y": 425, "width": 110, "height": 25,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 601, "version": 1, "versionNonce": 601,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "text": "PM Lead", "fontSize": 14, "fontFamily": 2,
      "textAlign": "center", "verticalAlign": "middle", "containerId": "grandchild-a1",
      "originalText": "PM Lead", "autoResize": true, "lineHeight": 1.25
    },

    {
      "type": "rectangle", "id": "grandchild-a2", "x": 160, "y": 410, "width": 140, "height": 55,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "#b2f2bb",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 700, "version": 1, "versionNonce": 700,
      "isDeleted": false, "groupIds": [],
      "boundElements": [
        { "id": "text-a2", "type": "text" },
        { "id": "arrow-a-a2", "type": "arrow" }
      ],
      "link": null, "locked": false, "roundness": { "type": 3 }
    },
    {
      "type": "text", "id": "text-a2", "x": 175, "y": 425, "width": 110, "height": 25,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 701, "version": 1, "versionNonce": 701,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "text": "UX Designer", "fontSize": 14, "fontFamily": 2,
      "textAlign": "center", "verticalAlign": "middle", "containerId": "grandchild-a2",
      "originalText": "UX Designer", "autoResize": true, "lineHeight": 1.25
    },

    {
      "type": "arrow", "id": "arrow-root-a",
      "x": 280, "y": 160, "width": 165, "height": 90,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 800, "version": 1, "versionNonce": 800,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "points": [[0, 0], [-165, 90]],
      "startArrowhead": null, "endArrowhead": "arrow",
      "startBinding": { "elementId": "root", "focus": 0, "gap": 5 },
      "endBinding": { "elementId": "child-a", "focus": 0, "gap": 5 }
    },
    {
      "type": "arrow", "id": "arrow-root-b",
      "x": 330, "y": 160, "width": 0, "height": 90,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 801, "version": 1, "versionNonce": 801,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "points": [[0, 0], [0, 90]],
      "startArrowhead": null, "endArrowhead": "arrow",
      "startBinding": { "elementId": "root", "focus": 0, "gap": 5 },
      "endBinding": { "elementId": "child-b", "focus": 0, "gap": 5 }
    },
    {
      "type": "arrow", "id": "arrow-root-c",
      "x": 380, "y": 160, "width": 165, "height": 90,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 802, "version": 1, "versionNonce": 802,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "points": [[0, 0], [165, 90]],
      "startArrowhead": null, "endArrowhead": "arrow",
      "startBinding": { "elementId": "root", "focus": 0, "gap": 5 },
      "endBinding": { "elementId": "child-c", "focus": 0, "gap": 5 }
    },
    {
      "type": "arrow", "id": "arrow-a-a1",
      "x": 85, "y": 320, "width": 45, "height": 90,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 803, "version": 1, "versionNonce": 803,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "points": [[0, 0], [-45, 90]],
      "startArrowhead": null, "endArrowhead": "arrow",
      "startBinding": { "elementId": "child-a", "focus": 0, "gap": 5 },
      "endBinding": { "elementId": "grandchild-a1", "focus": 0, "gap": 5 }
    },
    {
      "type": "arrow", "id": "arrow-a-a2",
      "x": 145, "y": 320, "width": 85, "height": 90,
      "angle": 0, "strokeColor": "#1e1e1e", "backgroundColor": "transparent",
      "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid", "roughness": 1,
      "opacity": 100, "seed": 804, "version": 1, "versionNonce": 804,
      "isDeleted": false, "groupIds": [], "boundElements": null, "link": null, "locked": false,
      "points": [[0, 0], [85, 90]],
      "startArrowhead": null, "endArrowhead": "arrow",
      "startBinding": { "elementId": "child-a", "focus": 0, "gap": 5 },
      "endBinding": { "elementId": "grandchild-a2", "focus": 0, "gap": 5 }
    }
  ],
  "files": {}
}
```
