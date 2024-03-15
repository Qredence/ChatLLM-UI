<template>
  <div :class="$style.heading">
    <p :class="$style.appleDesignQream">
      Apple Design: Qream UI utilizes the sleek and intuitive Apple Design
      language to enhance user engagement and interaction.
    </p>
    <p :class="$style.appleDesignQream">&nbsp;</p>
    <p :class="$style.appleDesignQream">
      For Designers and Developers: Our UI Kit serves as a comprehensive toolkit
      for both designers and developers, facilitating efficient design handoff
      and smoothing the transition from design to code.
    </p>
  </div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";

  export default defineComponent({
    name: "HeadingText1",
  });
</script>
<style module>
  .appleDesignQream {
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
