<template>
  <div :class="$style.navigationBarIpad">
    <div :class="$style.titleAndControls">
      <div :class="$style.leadingControls">
        <div :class="$style.leading">
          <input :class="$style.leadingButton1" type="checkbox" />
        </div>
        <v-select
          :class="$style.documentTitleVselect"
          variant="outlined"
          color="primary"
        />
      </div>
      <div :class="$style.trailing">
        <div :class="$style.trailingButton1">
          <img
            :class="$style.twitterlogoIcon"
            loading="lazy"
            alt=""
            src="/twitterlogo.svg"
          />
        </div>
        <div :class="$style.trailingButton1">
          <img
            :class="$style.twitterlogoIcon"
            loading="lazy"
            alt=""
            src="/githublogo.svg"
          />
        </div>
      </div>
      <div :class="$style.githubLogo">
        <h2 :class="$style.title">Chat huxLLM</h2>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";

  export default defineComponent({
    name: "NavigationBarIPad",
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
  .documentTitleVselect {
    flex: 1;
    font-family: var(--font-inter-display);
    font-weight: 700;
    font-size: var(--font-size-xl);
    color: var(--text-text-primary);
  }
  .leadingControls {
    width: 197.7px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-start;
    gap: var(--spacing-8);
  }
  .twitterlogoIcon {
    height: 24px;
    width: 24px;
    position: relative;
  }
  .trailingButton1 {
    border-radius: var(--radius-radius-xs);
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    padding: var(--spacing-4);
  }
  .trailing {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-end;
    padding: var(--padding-2xs) var(--spacing-16) var(--padding-2xs) 0px;
    gap: var(--spacing-16);
  }
  .title {
    margin: 0;
    height: 58px;
    flex: 1;
    position: relative;
    font-size: inherit;
    letter-spacing: -0.4px;
    line-height: 34px;
    font-weight: 700;
    font-family: inherit;
    display: flex;
    align-items: center;
    justify-content: center;
    white-space: nowrap;
  }
  .githubLogo {
    width: 169px;
    margin: 0 !important;
    position: absolute;
    top: 0px;
    left: 637px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
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
  }
  .navigationBarIpad {
    align-self: stretch;
    background-color: var(--container-surface-tertiary);
    backdrop-filter: blur(50px);
    border-bottom: 0.3px solid var(--separator-separator-thin);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    padding: var(--spacing-16) var(--spacing-4);
    text-align: center;
    font-size: var(--title-title1-emphasized-size);
    color: var(--text-text-primary);
    font-family: var(--title-title1-emphasized);
  }
</style>
