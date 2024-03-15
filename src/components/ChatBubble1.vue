<template>
  <div :class="$style.chatbubble">
    <div :class="$style.bubble">
      <div :class="$style.heading">
        <p :class="$style.whyQreamUi">Why Qream UI?</p>
        <p :class="$style.figmasLatestFeatures">
          Figma's Latest Features: Stay ahead of the competition with our
          pioneering use of Figma's modern features like variables. Streamline
          your design process with reusable, dynamic components.
        </p>
        <p :class="$style.blankLine">&nbsp;</p>
        <p :class="$style.appleDesignQream">
          Apple Design: Qream UI utilizes the sleek and intuitive Apple Design
          language to enhance user engagement and interaction.
        </p>
        <p :class="$style.blankLine1">&nbsp;</p>
        <p :class="$style.forDesignersAnd">
          For Designers and Developers: Our UI Kit serves as a comprehensive
          toolkit for both designers and developers, facilitating efficient
          design handoff and smoothing the transition from design to code.
        </p>
      </div>
    </div>
    <BottomInfo
      avatarSrcBackgroundColor="rgba(0, 0, 0, 0.85)"
      role="U"
      bFontWeight="700"
      bColor="#fcfcfc"
      thumbsUp="https://d1xzdqg8s8ggsr.cloudfront.net/65f483ea235522b0403ebbfa/eb4f692b-8cf4-45b6-a85c-c3e2051c5c9f_1710523443620415871?Expires=-62135596800&Signature=cfEFe4MhkVD-Z7Rn5kMTVlhKQpAC~Vbp8Y-8w4O5e-FVBYm3KLkg91PEMn12NNE6XuZco0kBpy0FciOLfMuDkHROHrLplItxgolCZcQ73aUws0D26QeFI-WHTINZMlGeUhWyU-WLNZqruT8tDveNYBY9houiZAmT5rR-Gy5Xlr-bn34iEEBn2w7lblN1q1SXoJLTn0bmsEpFzufP1ImkkCmyEyN~kONlqPlfDjRjhAAi7QsOIQZEJP8y2v0xF8hQfo7LktMgQK2~EtxN6YNM4dhKwpgjbulhGWNx~eva3uNPrAdU-6yqjIFab26HoK9jXMk99U0kaBoOH2Todx3xqQ__&Key-Pair-Id=K1P54FZWCHCL6J"
      thumbsDown="https://d1xzdqg8s8ggsr.cloudfront.net/65f483ea235522b0403ebbfa/0828a9ea-92d4-4872-be77-b7794a9e5733_1710523443620507152?Expires=-62135596800&Signature=OeWxMLbBXyaZbiqa3nNnId12hT-f90cROaPRk5klDS4Ja6oK9pcGHILzWL7zKeEWoJhdqE3NMWopx7aKhMhlIyoUoZAxMIAZIyvrs519lm8wRWDgr~2N8o5SiwctEZqGsJE8hGYhn8xp6meFNPg5d34dnSGLD8DWokDAmMvrZvCCkVQsfz3aVISRZNv4UDYhcbnWbCq8cuQe3v0ImUhZ3YUwHXeH7G7WvCpRZt7i25Ew2S8QgAqiOWUtWVx89mqLrSFW6tnzwLmn0d1bcDI90ZkE~mAEhHNQUSrR3iCePaPWBf8kSVJPJgnExBPbAz20CkEQGtGehXutPjFXT971lg__&Key-Pair-Id=K1P54FZWCHCL6J"
      date="15:15"
    />
  </div>
</template>
<script lang="ts">
  import { defineComponent } from "vue";
  import BottomInfo from "./BottomInfo.vue";

  export default defineComponent({
    name: "ChatBubble1",
    components: { BottomInfo },
  });
</script>
<style module>
  .whyQreamUi {
    margin: 0;
  }
  .figmasLatestFeatures {
    margin: 0;
  }
  .blankLine {
    margin: 0;
  }
  .appleDesignQream {
    margin: 0;
  }
  .blankLine1 {
    margin: 0;
  }
  .forDesignersAnd {
    margin: 0;
  }
  .heading {
    flex: 1;
    position: relative;
    letter-spacing: -0.4px;
    line-height: 22px;
    font-weight: 600;
    display: inline-block;
    max-width: 100%;
  }
  .bubble {
    align-self: stretch;
    border-radius: var(--br-5xl);
    background: linear-gradient(
        rgba(120, 120, 128, 0.08),
        rgba(120, 120, 128, 0.08)
      ),
      #fcfcfc;
    border: 1px solid var(--text-quarternary);
    box-sizing: border-box;
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    justify-content: flex-start;
    padding: var(--spacing-16) var(--padding-4xl) var(--spacing-24);
    max-width: 100%;
  }
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
