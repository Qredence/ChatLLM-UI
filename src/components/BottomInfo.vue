<template>
  <div :class="$style.bottominfo">
    <div :class="$style.bubbleinformation">
      <div
        :class="$style.avatarsrc"
        v-if="!showAvatarSrc"
        :style="avatarSrcStyle"
      >
        <div :class="$style.avatar">
          <Avatar :showCircle="true" />
          <h2 :class="$style.b" v-if="!show" :style="bStyle">{{role}}</h2>
        </div>
      </div>
      <div :class="$style.leftinformationWrapper">
        <div :class="$style.leftinformation">
          <div :class="$style.date">
            <div :class="$style.date1">15:15</div>
          </div>
          <div :class="$style.thumbsWrapper">
            <div :class="$style.thumbs">
              <img
                :class="$style.thumbsupIcon"
                loading="lazy"
                alt=""
                src="/thumbsup.svg"
              /><ThumbsDownIcon />
            </div>
          </div>
        </div>
      </div>
    </div>
    <IconCopy />
  </div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";
  import type * as CSS from "csstype";
  import Avatar from "./Circle.vue";
  import ThumbsDownIcon from "./ThumbsDownIcon.vue";
  import IconCopy from "./Frame 3.vue";

  export default defineComponent({
    name: "BottomInfo",
    components: { Avatar, ThumbsDownIcon, IconCopy },
    props: {
      role: { type: String },
      showAvatarSrc: { type: Boolean, default: true },
      show: { type: Boolean },
      showCircle: { type: Boolean },
      role1: { type: String },
      avatarSrcBackgroundColor: { type: String },
      bFontWeight: { type: String },
      bColor: { type: String },
      bAccentColor: { type: String },
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
          accentColor: this.bAccentColor,
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
  .date1 {
    position: relative;
    letter-spacing: -0.4px;
    line-height: 22px;
    font-weight: 600;
    display: inline-block;
    min-width: 43px;
    white-space: nowrap;
  }
  .date {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    justify-content: flex-start;
    padding: var(--padding-4xs) 0px;
  }
  .thumbsupIcon {
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
  }
  .bubbleinformation {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    justify-content: flex-start;
    gap: var(--gap-base);
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
    font-family: var(--callout-emphasized);
  }
</style>
