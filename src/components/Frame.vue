<template>
  <div :class="$style.thumbsWrapper">
    <div :class="$style.thumbs">
      <img :class="$style.thumbsupIcon" loading="lazy" alt="" :src="thumbsUp" />
      <img
        :class="$style.thumbsdownIcon"
        loading="lazy"
        alt=""
        :src="thumbsDown"
      />
    </div>
  </div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";

  export default defineComponent({
    name: "Frame",
    props: {
      thumbsUp: { type: String },
      thumbsDown: { type: String },
    },
  });
</script>
<style module>
  .thumbsupIcon {
    height: 20px;
    width: 20px;
    position: relative;
    min-height: 20px;
  }
  .thumbsdownIcon {
    height: 20px;
    width: 20px;
    position: relative;
    min-height: 20px;
  }
  .thumbs {
    height: 20px;
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    justify-content: flex-start;
    gap: var(--gap-5xs);
  }
  .thumbsWrapper {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    padding: var(--padding-3xs) 0px 0px;
  }
</style>
