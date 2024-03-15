<template>
  <div :class="$style.titleAndControls">
    <div :class="$style.leadingControls">
      <div :class="$style.leading">
        <input :class="$style.leadingButton1" type="checkbox" />
      </div>
      <div :class="$style.documentTitle">
        <title
          title="Qredence.ai"
          titleMargin="unset"
          titleHeight="unset"
          titleFontSize="20px"
          titleLineHeight="25px"
          titleFontWeight="bold"
          titleFontFamily="'Inter Display'"
          titleDisplay="inline-block"
        />
        <img
          :class="$style.downArrowCircle"
          alt=""
          src="/down-arrow-circle.svg"
        />
      </div>
    </div>
    <Trailing />
    <div :class="$style.githubLogo"><title title="Chat huxLLM" /></div>
  </div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";
  import Title from "./Title.vue";
  import Trailing from "./Trailing.vue";

  export default defineComponent({
    name: "TitleAndControls",
    components: { Title, Trailing },
  });
</script>
<style module>
  .leadingButton1 {
    margin: 0;
    height: 28px;
    width: 28px;
  }
  .leading {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-start;
    padding: var(--padding-2xs) 0px var(--padding-2xs) var(--spacing-16);
  }
  .downArrowCircle {
    height: 13.7px;
    width: 13.7px;
    position: relative;
  }
  .documentTitle {
    overflow: hidden;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    padding: var(--padding-2xs) 0px var(--padding-2xs) var(--spacing-16);
    gap: var(--spacing-8);
  }
  .leadingControls {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-start;
    gap: var(--spacing-8);
  }
  .githubLogo {
    margin: 0 !important;
    position: absolute;
    top: 0px;
    left: 637px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    font-size: var(--title-title1-emphasized-size);
    font-family: var(--title-title1-emphasized);
  }
  .titleAndControls {
    align-self: stretch;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    padding: 0px 0px 0px;
    position: relative;
    gap: var(--gap-xl);
    text-align: center;
    font-size: var(--font-size-xl);
    color: var(--text-text-primary);
    font-family: var(--font-inter-display);
  }
</style>
