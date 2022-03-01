<template>
  <SharedTemplateSection :data="data">
    <div class="capitalize__list">
      <div
        class="capitalize__item"
        v-for="(item, index) in data.items"
        :key="index"
      >
        <img class="capitalize__image" v-bind:src="item.logo" />
        <img class="capitalize__image_mobile" v-bind:src="item.logoMobile" />
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
.capitalize__list {
  display: flex;
  column-gap: 30px;
  margin-bottom: 40px;

  @include breakpoint(md) {
    column-gap: 63px;
  }

  .capitalize__image {
    margin: 0 auto;
    display: none;
    @include breakpoint(md) {
      display: block;
    }
  }

  .capitalize__image_mobile {
    margin: 0 auto;
    @include breakpoint(md) {
      display: none;
    }
  }
}
</style>
