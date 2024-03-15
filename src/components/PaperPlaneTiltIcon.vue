<template>
  <img
    :class="$style.paperplanetiltIcon"
    alt=""
    :src="paperPlaneTilt"
    :style="paperPlaneTiltIconStyle"
  />
</template>
<script lang="ts">
  import { defineComponent } from "vue";
  import type * as CSS from "csstype";

  export default defineComponent({
    name: "PaperPlaneTiltIcon",
    props: {
      paperPlaneTilt: { type: String },
      paperPlaneTiltIconHeight: {
        type: [Object, Array, String, Number, Boolean],
      },
      paperPlaneTiltIconWidth: {
        type: [Object, Array, String, Number, Boolean],
      },
    },
    computed: {
      paperPlaneTiltIconStyle(): CSS.Properties {
        return {
          height: this.paperPlaneTiltIconHeight,
          width: this.paperPlaneTiltIconWidth,
        };
      },
    },
  });
</script>
<style module>
  .paperplanetiltIcon {
    height: 16px;
    width: 16px;
    position: relative;
  }
</style>
