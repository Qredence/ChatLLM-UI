<template>
  <div :class="$style.bottominfo">
    <div :class="$style.bubbleinformation">
      <div :class="$style.avatarsrc" :style="avatarSrcStyle">
        <div :class="$style.avatar">
          <Avatar />
          <h2 :class="$style.b" :style="bStyle">{{role}}</h2>
        </div>
      </div>
      <div :class="$style.leftinformationWrapper">
        <div :class="$style.leftinformation">
          <Date1 :date="15:15" /><frame
            :thumbsUp="/thumbsup.svg"
            :thumbsDown="/thumbsdown.svg"
          />
        </div>
      </div>
    </div>
    <input :class="$style.frameInput" type="checkbox" />
  </div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";
  import type * as CSS from "csstype";
  import Avatar from "../../Circle.vue";
  import Date1 from "./Date1.vue";
  import Frame from "./Frame.vue";

  export default defineComponent({
    name: "BottomInfo",
    components: { Avatar, Date1, Frame },
    props: {
      role: { type: String },
      thumbsUp: { type: String },
      thumbsDown: { type: String },
      date: { type: String },
      avatarSrcBackgroundColor: { type: String },
      bFontWeight: { type: String },
      bColor: { type: String },
    },
    computed: {
      avatarSrcStyle(): CSS.Properties {
        return {
          backgroundColor: this.avatarSrcBackgroundColor,
        };
      },
      bStyle(): CSS.Properties {
        return {
          fontWeight: this.bFontWeight,
          color: this.bColor,
        };
      },
    },
  });
</script>
<style module>
  .b {
    margin: 0;
    position: absolute;
    top: 4px;
    left: 15px;
    font-size: inherit;
    line-height: 40px;
    font-weight: 600;
    font-family: inherit;
    display: inline-block;
    min-width: 19px;
    z-index: 1;
  }
  .avatar {
    height: 48px;
    flex: 1;
    position: relative;
  }
  .avatarsrc {
    width: 48px;
    border-radius: var(--numeric-500);
    background-color: var(--container-surface-primary);
    overflow: hidden;
    flex-shrink: 0;
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    justify-content: flex-start;
  }
  .leftinformation {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    justify-content: flex-start;
    gap: var(--gap-sm);
  }
  .leftinformationWrapper {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    padding: var(--padding-9xs) 0px 0px;
    font-size: var(--body-size);
    font-family: var(--callout-emphasized);
  }
  .bubbleinformation {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    justify-content: flex-start;
    gap: var(--gap-base);
  }
  .frameInput {
    margin: 0;
    height: 40px;
    width: 32px;
  }
  .bottominfo {
    align-self: stretch;
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    justify-content: space-between;
    padding: var(--padding-3xs);
    gap: var(--gap-xl);
    text-align: left;
    font-size: var(--title-title1-emphasized-size);
    color: var(--text-text-primary);
    font-family: var(--font-inter);
  }

  @media screen and (max-width: 450px) {
    .b {
      font-size: var(--font-size-3xl);
      line-height: 32px;
    }

    .bottominfo {
      flex-wrap: wrap;
    }
  }
</style>
