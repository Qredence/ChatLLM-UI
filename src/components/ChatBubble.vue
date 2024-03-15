<template>
  <div :class="$style.chatbubble">
    <Bubble /><BottomInfo
      avatarSrcBackgroundColor="rgba(0, 0, 0, 0.85)"
      role="Z"
      bFontWeight="700"
      bColor="#fcfcfc"
      :showAvatarSrc="true"
      :show="true"
      :showCircle="true"
      role1="Z"
      bAccentColor="#FFFFF"
    />
  </div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";
  import Bubble from "./Bubble.vue";
  import BottomInfo from "./BottomInfo.vue";

  export default defineComponent({
    name: "UserBubble",
    components: { Bubble, BottomInfo },
  });
</script>
<style module>
  .chatbubble {
    align-self: stretch;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    gap: var(--gap-4xl);
    max-width: 100%;
    text-align: left;
    font-size: var(--body-size);
    color: var(--text-text-primary);
    font-family: var(--callout-emphasized);
  }
</style>
