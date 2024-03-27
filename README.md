# Point Tool

![Version of EditorJS that the plugin is compatible with](https://badgen.net/badge/Editor.js/v2.0/blue)

Provides Points Blocks for the [Editor.js](https://ifmo.su/editor).

## Installation

Get the package

```shell
yarn add @kalebu2468/editorjs-points
```

Include module at your application

```javascript
import Point from "@kalebu2468/editorjs-points";
```

Optionally, you can load this tool from CDN [JsDelivr CDN](https://cdn.jsdelivr.net/npm/@editorjs/header@latest)

## Usage

Add a new Tool to the `tools` property of the Editor.js initial config.

```javascript
var editor = EditorJS({
  ...

  tools: {
    ...
    points: Point,
  },

  ...
});
```

## Shortcut

You can insert this Block by a useful shortcut. Set it up with the `tools[].shortcut` property of the Editor's initial config.

```javascript
var editor = EditorJS({
  ...

  tools: {
    ...
    points: {
      class: Point,
    },
  },

  ...
});
```

## Config Params

All properties are optional.

| Field        | Type       | Description                |
| ------------ | ---------- | -------------------------- |
| placeholder  | `string`   | point's placeholder string |
| levels       | `number[]` | enabled point levels       |
| defaultLevel | `number`   | default point level        |

```javascript
var editor = EditorJS({
  ...

  tools: {
    ...
    points: {
      class: Point,
      config: {
        placeholder: 'Enter a point',
        levels: [3],
        defaultLevel: 3
      }
    }
  }

  ...
});
```

## Tool's settings

![An image showing the point block tool](https://capella.pics/634ad545-08d7-4cb7-8409-f01289e0e5e1.jpg)

You can select one of six levels for point.

## Output data

| Field | Type     | Description    |
| ----- | -------- | -------------- |
| text  | `string` | point's text   |
| level | `number` | level of point |

```json
{
  "type": "points",
  "data": {
    "text": "Why Telegram is the best messenger",
    "level": 3
  }
}
```
