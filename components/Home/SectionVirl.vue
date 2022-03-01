<template>
  <SharedTemplateSection :data="data">
    <div class="video__container">
      <iframe
        width="100%"
        height="100%"
        src="https://www.youtube.com/embed/PNKtZfVPt-s"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      ></iframe>
    </div>
  </SharedTemplateSection>
</template>

<script>
import SharedTemplateSection from "@/components/Shared/TemplateSection";

export default {
  props: {
    data: Object
  },
  components: {
    SharedTemplateSection
  }
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";

.video__container {
  width: 320px;
  height: 180px;

  @include breakpoint(sm) {
    width: 420px;
    height: 280px;
  }

  @include breakpoint(lg) {
    width: 940px;
    height: 528px;
  }
}
</style>
