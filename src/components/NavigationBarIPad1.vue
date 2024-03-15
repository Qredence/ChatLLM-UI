<template>
  <div :class="$style.navigationBarIpad"><TitleAndControls /></div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";
  import TitleAndControls from "./TitleAndControls.vue";

  export default defineComponent({
    name: "NavigationBarIPad1",
    components: { TitleAndControls },
  });
</script>
<style module>
  .navigationBarIpad {
    align-self: stretch;
    background-color: var(--container-surface-tertiary);
    backdrop-filter: blur(50px);
    border-bottom: 0.3px solid var(--separator-separator-thin);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    padding: var(--spacing-16) var(--spacing-4);
    text-align: center;
    font-size: var(--font-size-xl);
    color: var(--text-text-primary);
    font-family: var(--font-inter-display);
  }
</style>
