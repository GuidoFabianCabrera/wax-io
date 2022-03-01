<template>
  <SharedTemplateSection :data="data">
    <div class="planet__list">
      <div
        class="planet__item"
        v-for="(item, index) in data.items"
        :key="index"
      >
        <img class="planet__image" :src="item.image" alt="" />
        <p class="planet__title">{{ item.title }}</p>
        <p class="planet__description">{{ item.description }}</p>
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

.planet__list {
  display: grid;
  grid-template-columns: repeat(2, 150px);
  row-gap: 10px;
  column-gap: 15px;
  margin-bottom: 25px;

  @include breakpoint(sm) {
    grid-template-columns: repeat(4, 150px);
  }

  @include breakpoint(lg) {
    grid-template-columns: repeat(4, 220px);
  }

  .planet__item {
    padding: 15px;
  }

  .planet__image {
    margin-bottom: 10px;
  }

  .planet__title {
    font-size: 14px;
    font-weight: 800;
    margin-bottom: 10px;
    @include breakpoint(sm) {
      margin-bottom: 0;
    }
  }

  .planet__description {
    font-size: 14px;
    margin: 0;
  }
}
</style>
