<template>
  <div :class="$style.trailing">
    <div :class="$style.trailingButton1">
      <PaperPlaneTiltIcon
        paperPlaneTilt="/twitterlogo.svg"
        paperPlaneTiltIconHeight="24px"
        paperPlaneTiltIconWidth="24px"
      />
    </div>
    <div :class="$style.trailingButton11">
      <PaperPlaneTiltIcon
        paperPlaneTilt="/githublogo.svg"
        paperPlaneTiltIconHeight="24px"
        paperPlaneTiltIconWidth="24px"
      />
    </div>
  </div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";
  import PaperPlaneTiltIcon from "./PaperPlaneTiltIcon.vue";

  export default defineComponent({
    name: "Trailing",
    components: { PaperPlaneTiltIcon },
  });
</script>
<style module>
  .trailingButton1 {
    border-radius: var(--radius-radius-xs);
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    padding: var(--spacing-4);
  }
  .trailingButton11 {
    border-radius: var(--radius-radius-xs);
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    padding: var(--spacing-4);
  }
  .trailing {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-end;
    padding: var(--padding-2xs) var(--spacing-16) var(--padding-2xs) 0px;
    gap: var(--spacing-16);
  }
</style>
