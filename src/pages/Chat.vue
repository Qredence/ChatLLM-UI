<template>
  <div :class="$style.chat">
    <NavigationBarIPad />
    <main :class="$style.body"><ChatBubble /><InputWrapper /></main>
  </div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";
  import NavigationBarIPad from "../components/NavigationBarIPad.vue";
  import ChatBubble from "../components/ChatBubble.vue";
  import InputWrapper from "../components/InputWrapper.vue";

  export default defineComponent({
    name: "Chat",
    components: { NavigationBarIPad, ChatBubble, InputWrapper },
  });
</script>
<style module>
  .body {
    align-self: stretch;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    padding: 0px var(--padding-xl) 56px;
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

  @media screen and (max-width: 975px) {
    .body {
      gap: 59px 118px;
    }
  }
  @media screen and (max-width: 950px) {
    .body {
      padding-bottom: 36px;
      box-sizing: border-box;
    }
  }
  @media screen and (max-width: 700px) {
    .body {
      gap: 29px 118px;
      padding-bottom: var(--padding-4xl);
      box-sizing: border-box;
    }
  }
</style>
