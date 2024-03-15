<template>
  <div :class="$style.bubble"><HeadingText /></div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";
  import HeadingText from "./HeadingText.vue";

  export default defineComponent({
    name: "Bubble",
    components: { HeadingText },
  });
</script>
<style module>
  .bubble {
    align-self: stretch;
    border-radius: var(--br-5xl);
    background: linear-gradient(
        rgba(120, 120, 128, 0.08),
        rgba(120, 120, 128, 0.08)
      ),
      #fcfcfc;
    border: 1px solid var(--text-quarternary);
    box-sizing: border-box;
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    justify-content: flex-start;
    padding: var(--spacing-16) var(--padding-4xl) var(--spacing-24);
    max-width: 100%;
    text-align: left;
    font-size: var(--body-size);
    color: var(--text-text-primary);
    font-family: var(--callout-emphasized);
  }
</style>
