<template>
  <img
    :class="$style.thumbsdownIcon"
    loading="lazy"
    alt=""
    src="/thumbsdown.svg"
  />
</template>
<script lang="ts">
  import { defineComponent } from "vue";

  export default defineComponent({
    name: "ThumbsDownIcon",
  });
</script>
<style module>
  .thumbsdownIcon {
    height: 20px;
    width: 20px;
    position: relative;
    min-height: 20px;
  }
</style>
