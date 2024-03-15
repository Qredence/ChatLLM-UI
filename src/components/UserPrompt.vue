<template>
  <div :class="$style.userprompt">
    <ValueText value="Ask a question" /><button label="Send" />
  </div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";
  import ValueText from "./ValueText.vue";
  import Button from "./Button.vue";

  export default defineComponent({
    name: "UserPrompt",
    components: { ValueText, Button },
  });
</script>
<style module>
  .userprompt {
    align-self: stretch;
    border-radius: var(--br-xs);
    background-color: var(--background-background-container);
    box-shadow: var(--shadows-shadow-l);
    border: 1px solid var(--container-surface-primary);
    box-sizing: border-box;
    overflow: hidden;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-items: center;
    justify-content: flex-start;
    padding: var(--padding-2xs-5) var(--padding-6xs) var(--padding-2xs-5)
      var(--padding-lgi);
    max-width: 100%;
    row-gap: 20px;
    text-align: left;
    font-size: var(--body-size);
    color: var(--text-text-secondary);
    font-family: var(--callout-emphasized);
  }
</style>
