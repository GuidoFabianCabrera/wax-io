<template>
  <SharedTemplateSection :data="data">
    <div class="educational__list">
      <div
        class="educational__item"
        v-for="(item, index) in data.items"
        :key="index"
      >
        <div v-show="item.title" class="educational__title">
          {{ item.title }}
        </div>
        <div v-show="item.image" class="educational__image_container">
          <img class="educational__image" :src="item.image" />
          <img class="educational__image_mobile" :src="item.imageMobile" />
        </div>
        <iframe
          class="educational__video"
          v-show="item.video"
          width="100%"
          height="100%"
          :src="item.video"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
        <v-btn
          v-if="item.button"
          class="educational__button"
          rounded
          color="#1aa2c0"
          dark
          large
          outlined
          >{{ item.button }}</v-btn
        >
      </div>
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
.educational__list {
  display: grid;
  row-gap: 50px;

  @include breakpoint(lg) {
    grid-template-columns: repeat(3, 1fr);
    column-gap: 20px;
  }

  // .educational__item {
  // border: 1px solid red;
  // }

  .educational__title {
    font-size: 20px;
    font-weight: 700;
    margin-bottom: 10px;
  }

  .educational__image_container {
    margin-bottom: 24px;
  }

  .educational__image {
    margin: 0 auto;
    display: none;
    @include breakpoint(md) {
      display: block;
    }
  }

  .educational__image_mobile {
    margin: 0 auto;
    @include breakpoint(md) {
      display: none;
    }
  }

  .educational__video {
    width: 320px;
    height: 170px;

    @include breakpoint(md) {
      width: 300px;
      height: 170px;
    }
  }

  .educational__button {
    width: 200px;
    @include breakpoint(md) {
      width: 100px;
    }
  }
}
</style>
