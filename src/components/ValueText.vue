<template>
  <div :class="$style.value">{{value}}</div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";

  export default defineComponent({
    name: "ValueText",
    props: {
      value: { type: String },
    },
  });
</script>
<style module>
  .value {
    flex: 1;
    position: relative;
    font-size: var(--body-size);
    line-height: 22px;
    font-weight: 500;
    font-family: var(--callout-emphasized);
    color: var(--text-text-secondary);
    text-align: left;
    display: inline-block;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    min-width: 95px;
    max-width: 100%;
  }
</style>
