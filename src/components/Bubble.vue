<template>
  <div :class="$style.bubble">
    <div :class="$style.heading">
      <p :class="$style.appleDesignQream">
        Apple Design: Qream UI utilizes the sleek and intuitive Apple Design
        language to enhance user engagement and interaction.
      </p>
      <p :class="$style.blankLine">&nbsp;</p>
      <p :class="$style.forDesignersAnd">
        For Designers and Developers: Our UI Kit serves as a comprehensive
        toolkit for both designers and developers, facilitating efficient design
        handoff and smoothing the transition from design to code.
      </p>
    </div>
  </div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";

  export default defineComponent({
    name: "Bubble",
  });
</script>
<style module>
  .appleDesignQream {
    margin: 0;
  }
  .blankLine {
    margin: 0;
  }
  .forDesignersAnd {
    margin: 0;
  }
  .heading {
    flex: 1;
    position: relative;
    letter-spacing: -0.4px;
    line-height: 22px;
    font-weight: 600;
    display: inline-block;
    max-width: 100%;
  }
  .bubble {
    align-self: stretch;
    border-radius: var(--radius-radius-l);
    background-color: var(--background-background-container);
    box-shadow: 0px 0px 10.4px rgba(0, 0, 0, 0.19);
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    justify-content: flex-start;
    padding: var(--spacing-16) var(--spacing-24) var(--spacing-24);
    box-sizing: border-box;
    max-width: 100%;
    text-align: left;
    font-size: var(--body-size);
    color: var(--text-text-primary);
    font-family: var(--callout-emphasized);
  }
</style>
