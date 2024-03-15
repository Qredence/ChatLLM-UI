<template>
  <div :class="$style.date">
    <div :class="$style.date1">{{date}}</div>
  </div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";

  export default defineComponent({
    name: "Date1",
    props: {
      date: { type: String },
    },
  });
</script>
<style module>
  .date1 {
    position: relative;
    letter-spacing: -0.4px;
    line-height: 22px;
    font-weight: 600;
    display: inline-block;
    min-width: 43px;
    white-space: nowrap;
  }
  .date {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    justify-content: flex-start;
    padding: var(--padding-4xs) 0px;
    text-align: left;
    font-size: var(--body-size);
    color: var(--text-text-primary);
    font-family: var(--callout-emphasized);
  }
</style>
