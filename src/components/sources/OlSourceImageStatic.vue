<template>
  <div v-if="false"></div>
</template>
<script setup lang="ts">
import Static, { type Options } from "ol/source/ImageStatic";
import { inject, type Ref } from "vue";
import type ImageLayer from "ol/layer/Image";
import type { ImageSourceEvents } from "@/composables/useOpenLayersEvents";
import useSource from "@/composables/useSource";

// prevent warnings caused by event pass-through via useOpenLayersEvents composable
defineOptions({
  inheritAttrs: false,
});

const props = withDefaults(defineProps<Options>(), {
  interpolate: true,
});
defineEmits<ImageSourceEvents>();

const layer = inject<Ref<ImageLayer<Static>> | null>("imageLayer");

const { source } = useSource(Static, layer, props);

defineExpose({
  layer,
  source,
});
</script>
