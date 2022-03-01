<template>
  <SharedTemplateSection :data="data">
    <div class="roadmap__content">
      <div
        class="roadmap__container"
        v-for="(item, index) in data.items"
        :key="index"
      >
        <div class="roadmap__item">
          <img
            class="roadmap__check"
            v-if="item.complete"
            src="images/checkgreen.svg"
          />
          <img class="roadmap__check" v-else src="images/checkgray.svg" />

          <div class="roadmap__title">{{ item.title }}</div>
          <div class="roadmap__description">{{ item.description }}</div>
        </div>
        <img
          v-show="index !== data.items.length - 1"
          class="roadmap__dots"
          src="images/dots.svg"
          alt=""
        />
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

.roadmap__content {
  .roadmap__item {
    width: 240px;
    height: 140px;
    padding: 20px 10px;
    background: linear-gradient(#edf0fa, #dcdce5);
  }

  .roadmap__check {
    width: 32px;
  }

  .roadmap__title {
    font-weight: 800;
  }

  .roadmap__dots {
    width: 10px;
    height: 44px;
  }
}
</style>
