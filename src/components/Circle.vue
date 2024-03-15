<template>
  <div :class="$style.circle" v-if="!showCircle">{{role}}</div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";

  export default defineComponent({
    name: "Avatar",
    props: {
      showCircle: { type: Boolean },
      role: { type: String },
    },
  });
</script>
<style module>
  .circle {
    position: absolute;
    top: 0px;
    left: 0px;
    border-radius: 50%;
    width: 100%;
    height: 100%;
  }
</style>
