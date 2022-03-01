<template>
  <SharedTemplateSection :data="data">
    <div class="about__list">
      <div class="about__item" v-for="(item, index) in data.items" :key="index">
        <img class="about__image" :src="item.image" />
        <p class="about__name">{{ item.name }}</p>
        <p class="about__role">{{ item.role }}</p>
        <div class="about__social">
          <img
            v-for="(item, index) in item.social"
            :key="index"
            class="about__social_item"
            :src="item"
          />
        </div>
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
.about__list {
  width: 100%;
  display: flex;
  flex-direction: column;
  margin-top: 40px;

  @include breakpoint(md) {
    flex-direction: row;
    justify-content: space-evenly;
  }

  .about__item {
    margin-bottom: 60px;

    @include breakpoint(md) {
      margin-bottom: 40px;
    }
  }

  .about__name {
    font-weight: 600;
    font-size: 24px;
    margin-bottom: 0;
  }

  .about__role {
    font-size: 18px;
  }

  .about__social {
    display: flex;
    column-gap: 60px;
    justify-content: center;
  }

  .about__social_item {
    width: 32px;
    cursor: pointer;
  }
}
</style>
