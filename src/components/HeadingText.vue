<template>
  <div :class="$style.heading">
    <p :class="$style.whyQreamUi">Why Qream UI?</p>
    <p :class="$style.whyQreamUi">
      Figma's Latest Features: Stay ahead of the competition with our pioneering
      use of Figma's modern features like variables. Streamline your design
      process with reusable, dynamic components.
    </p>
    <p :class="$style.whyQreamUi">&nbsp;</p>
    <p :class="$style.whyQreamUi">
      Apple Design: Qream UI utilizes the sleek and intuitive Apple Design
      language to enhance user engagement and interaction.
    </p>
    <p :class="$style.whyQreamUi">&nbsp;</p>
    <p :class="$style.whyQreamUi">
      For Designers and Developers: Our UI Kit serves as a comprehensive toolkit
      for both designers and developers, facilitating efficient design handoff
      and smoothing the transition from design to code.
    </p>
  </div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";

  export default defineComponent({
    name: "HeadingText",
  });
</script>
<style module>
  .whyQreamUi {
    margin: 0;
  }
  .heading {
    flex: 1;
    position: relative;
    font-size: var(--body-size);
    letter-spacing: -0.4px;
    line-height: 22px;
    font-weight: 600;
    font-family: var(--callout-emphasized);
    color: var(--text-text-primary);
    text-align: left;
    display: inline-block;
    max-width: 100%;
  }
</style>
