<template>
  <button :class="$style.button">
    <div :class="$style.label">Send</div>
    <img :class="$style.paperplanetiltIcon" alt="" src="/paperplanetilt.svg" />
  </button>
</template>
<script lang="ts">
  import { defineComponent } from "vue";

  export default defineComponent({
    name: "Button",
  });
</script>
<style module>
  .label {
    position: relative;
    font-size: var(--callout-emphasized-size);
    letter-spacing: -0.4px;
    line-height: 21px;
    font-weight: 600;
    font-family: var(--callout-emphasized);
    color: var(--light-colors-blue);
    text-align: left;
    display: inline-block;
    min-width: 39px;
  }
  .paperplanetiltIcon {
    height: 16px;
    width: 16px;
    position: relative;
  }
  .button {
    cursor: pointer;
    border: none;
    padding: var(--padding-6xs) var(--padding-sm);
    background-color: var(--light-fills-tertiary);
    height: 36px;
    border-radius: var(--br-21xl);
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    box-sizing: border-box;
    gap: var(--gap-9xs);
  }
  .button:hover {
    background-color: var(--color-lightslategray);
  }
</style>
