<template>
  <div :class="$style.chatBubble">
    <div :class="$style.container"><AssistantBubble /><ChatBubble1 /></div>
  </div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";
  import AssistantBubble from "../../ChatBubble.vue";
  import ChatBubble1 from "./ChatBubble1.vue";

  export default defineComponent({
    name: "ChatBubble",
    components: { AssistantBubble, ChatBubble1 },
  });
</script>
<style module>
  .container {
    flex: 1;
    overflow-y: auto;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    padding: var(--padding-5xl) var(--spacing-10) var(--padding-7xl);
    box-sizing: border-box;
    gap: var(--gap-5xl);
    mix-blend-mode: normal;
    min-width: 390px;
    max-width: 764px;
  }
  .chatBubble {
    width: 918px;
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    justify-content: flex-start;
    padding: 0px var(--padding-58xl);
    box-sizing: border-box;
    max-width: 100%;
    text-align: left;
    font-size: var(--body-size);
    color: var(--text-text-primary);
    font-family: var(--callout-emphasized);
  }

  @media screen and (max-width: 950px) {
    .container {
      padding-top: var(--spacing-10);
      padding-bottom: var(--spacing-10);
      box-sizing: border-box;
      max-width: 100%;
    }

    .chatBubble {
      padding-left: var(--padding-19xl);
      padding-right: var(--padding-19xl);
      box-sizing: border-box;
    }
  }
</style>
