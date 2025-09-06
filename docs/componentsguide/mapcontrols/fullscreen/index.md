# ol-full-screen-control

> A Fullscreen control for OpenLayers.

[[toc]]

## Demo

<script setup lang="ts">
import FullScreenControlDemo from "@demos/FullScreenControlDemo.vue"
</script>
<ClientOnly>
<FullScreenControlDemo />
</ClientOnly>

## Setup

<!--@include: ../../mapcontrols.plugin.md-->

## Usage

| Plugin Usage               |           Explicit Import           |
| -------------------------- | :---------------------------------: |
| `<ol-full-screen-control>` | `<MapControls.OlFullScreenControl>` |

::: code-group

<<< ../../../../src/demos/FullScreenControlDemo.vue

:::

## Properties

### className

- **Type**: `String`
- **Default**: `ol-full-screen`

### label

- **Type**: `String`
- **Default**: `\u2922`

### labelActive

- **Type**: `String`
- **Default**: `\u00d7`

### activeClassName

- **Type**: `String`
- **Default**: `ol-full-screen-true`

### inactiveClassName

- **Type**: `String`
- **Default**: `ol-full-screen-false`

### tipLabel

- **Type**: `String`
- **Default**: `Toggle full-screen`

### keys

- **Type**: `Boolean`
- **Default**: `false`

### target

- **Type**: `Object`

### source

- **Type**: `Object`
