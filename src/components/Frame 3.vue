<template>
  <input :class="$style.frameInput" type="checkbox" />
</template>
<script lang="ts">
  import { defineComponent } from "vue";

  export default defineComponent({
    name: "IconCopy",
  });
</script>
<style module>
  .frameInput {
    margin: 0;
    height: 40px;
    width: 32px;
  }
</style>
