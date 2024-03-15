<template>
  <div :class="$style.chat">
    <header :class="$style.navigationBarIpad"><NavigationBarIPad /></header>
    <main :class="$style.body">
      <div :class="$style.chatBubble">
        <div :class="$style.container"><AssistantBubble /><UserBubble /></div>
      </div>
      <InputPrompt />
    </main>
  </div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";
  import NavigationBarIPad from "../components/NavigationBarIPad.vue";
  import AssistantBubble from "../ChatBubble.vue";
  import UserBubble from "../components/ChatBubble.vue";
  import InputPrompt from "../components/inputWrapper.vue";

  export default defineComponent({
    name: "Chat",
    components: { NavigationBarIPad, AssistantBubble, UserBubble, InputPrompt },
  });
</script>
<style module>
  .navigationBarIpad {
    align-self: stretch;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
  }
  .container {
    flex: 1;
    overflow-y: auto;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    padding: var(--padding-5xl) var(--spacing-10) 26px;
    box-sizing: border-box;
    gap: 24px;
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
    padding: 0px 77px;
    box-sizing: border-box;
    max-width: 100%;
  }
  .body {
    align-self: stretch;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    padding: 0px 20px 56px;
    box-sizing: border-box;
    gap: 118px;
    max-width: 100%;
  }
  .chat {
    width: 100%;
    position: relative;
    background-color: var(--background-background-page);
    overflow: hidden;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    letter-spacing: normal;
  }
</style>
