<template>
  <SharedTemplateSection :data="data">
    <div class="games__list">
      <div class="games__item" v-for="(item, index) in data.items" :key="index">
        <img class="games__background" :src="item.background" />
        <div class="games__content">
          <img class="games__logo" :src="item.logo" />
          <p class="games__name" v-show="item.name">{{ item.name }}</p>
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

.games__list {
  display: flex;
  flex-direction: column;
  row-gap: 25px;
  cursor: pointer;
  margin-bottom: 25px;

  @include breakpoint(lg) {
    flex-direction: row;
    column-gap: 20px;
    margin-bottom: 35px;
  }

  .games__item {
    position: relative;
    border-radius: 5px;
    overflow: hidden;
  }

  .games__background {
    display: block;
  }

  .games__content {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    background: rgba(0, 0, 0, 0.7);
    display: grid;
    justify-content: center;
    align-items: center;
    padding: 20px;
  }

  .games__logo {
    margin: 0 auto;
  }

  .games__name {
    color: white;
  }
}
</style>
