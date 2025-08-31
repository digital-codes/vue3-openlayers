# ol-graticule-layer

Layer that renders a grid for a coordinate system (currently only EPSG:4326 is supported).
Note that the view projection must define both extent and worldExtent.

[[toc]]

## Demo

<script setup lang="ts">
import GraticuleDemo from "@demos/GraticuleDemo.vue"
</script>
<ClientOnly>
<GraticuleDemo />
</ClientOnly>

## Setup

<!--@include: ../../layers.plugin.md-->

## Usage

| Plugin Usage           |       Explicit Import       |
| ---------------------- | :-------------------------: |
| `<ol-graticule-layer>` | `<Layers.OlGraticuleLayer>` |

::: code-group

<<< ../../../../src/demos/GraticuleDemo.vue

:::

## Properties

### Props from OpenLayers

Properties are passed-trough from OpenLayers directly.
Their types and default values can be checked-out [in the official OpenLayers docs](https://openlayers.org/en/latest/apidoc/module-ol_layer_Graticule-Graticule.html).
Only some properties deviate caused by reserved keywords from Vue / HTML.
This deviating props are described in the section below.

### Deviating Properties

none.

## Events

You have access to all Events from the underlying source.
Check out [the official OpenLayers docs](https://openlayers.org/en/latest/apidoc/module-ol_layer_Graticule-Graticule.html) to see the available events tht will be fired.

```html
<ol-graticule-layer @error="handleEvent" />
```

## Methods

You have access to all Methods from the underlying source.
Check out [the official OpenLayers docs](https://openlayers.org/en/latest/apidoc/module-ol_layer_Graticule-Graticule.html) to see the available methods.

To access the source, you can use a `ref()` as shown below:

```vue
<template>
  <!-- ... -->
  <ol-graticule-layer ref="layerRef" />
  <!-- ... -->
</template>

<script setup lang="ts">
import { ref, onMounted } from "vue";
import type GraticuleLayer from "ol/layer/Graticule";

const layerRef = ref<{ vectorLayer: GraticuleLayer }>(null);

onMounted(() => {
  const layer: WebGLTileLayer = sourceRef.value?.vectorLayer;
  // call your method on `layer`
});
</script>
```
