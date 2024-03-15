<template>
  <footer :class="$style.inputwrapper"><UserPrompt /></footer>
</template>
<script lang="ts">
  import { defineComponent } from "vue";
  import UserPrompt from "./UserPrompt.vue";

  export default defineComponent({
    name: "InputPrompt",
    components: { UserPrompt },
  });
</script>
<style module>
  .inputwrapper {
    width: 918px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
    max-width: 100%;
    text-align: left;
    font-size: var(--body-size);
    color: var(--text-text-secondary);
    font-family: var(--callout-emphasized);
  }
</style>
