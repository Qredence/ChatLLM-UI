<template>
  <h2 :class="$style.title" :style="titleStyle">{{title}}</h2>
</template>
<script lang="ts">
  import { defineComponent } from "vue";
  import type * as CSS from "csstype";

  export default defineComponent({
    name: "Title",
    props: {
      title: { type: String },
      titleMargin: { type: [Object, Array, String, Number, Boolean] },
      titleHeight: { type: [Object, Array, String, Number, Boolean] },
      titleFontSize: { type: String },
      titleLineHeight: { type: String },
      titleFontWeight: { type: String },
      titleFontFamily: { type: String },
      titleDisplay: { type: String },
    },
    computed: {
      titleStyle(): CSS.Properties {
        return {
          margin: this.titleMargin,
          height: this.titleHeight,
          fontSize: this.titleFontSize,
          lineHeight: this.titleLineHeight,
          fontWeight: this.titleFontWeight,
          fontFamily: this.titleFontFamily,
          display: this.titleDisplay,
        };
      },
    },
  });
</script>
<style module>
  .title {
    margin: 0;
    height: 58px;
    position: relative;
    font-size: var(--title-title1-emphasized-size);
    letter-spacing: -0.4px;
    line-height: 34px;
    font-weight: 700;
    font-family: var(--title-title1-emphasized);
    color: var(--text-text-primary);
    text-align: center;
    display: flex;
    align-items: center;
    justify-content: center;
    white-space: nowrap;
  }
</style>
