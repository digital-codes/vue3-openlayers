# ol-animation-zoom

> Zoom animation for feature

[[toc]]

## Demo

<script setup>
import ZoomAnimation from "@demos/ZoomAnimation.vue"
</script>

<ClientOnly>
<ZoomAnimation />
</ClientOnly>

## Setup

<!--@include: ../../animations.plugin.md-->

## Usage

| Plugin Usage          |        Explicit Import         |
| --------------------- | :----------------------------: |
| `<ol-animation-zoom>` | `<Animations.OlAnimationZoom>` |

::: code-group

<<< ../../../../src/demos/ZoomAnimation.vue

:::

## Properties

### duration

- **Type**: `Number`
- **Default**: `1000`

duration of the animation in ms, default 1000

### revers

- **Type**: `Boolean`
- **Default**: `false`

revers the animation direction

### repeat

- **Type**: `Number`
- **Default**: `0`

number of time to repeat the animation, default 0

### hiddenStyle

- **Type**: `ol.style.Style`

a style to display the feature when playing the animation to be used to make the feature selectable when playing animation , default the feature will be hidden when playing (and not selectable)

### fade

- **Type**: `function`
- **Default**: `none`

an easing function used to fade in the feature, default none

### easing

- **Type**: `function`
- **Default**: `0`

an easing function for the animation, default ol.easing.linear

### zoomOut

- **Type**: `Boolean`
- **Default**: `false`

to zoom out
