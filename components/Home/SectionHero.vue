<template>
  <section class="hero">
    <div class="hero__container custom_container custom_container--lg">
      <h1 class="hero__title">
        vIRL<span class="hero__r">®</span>Commerce Starts Here
      </h1>
      <p class="hero__description">
        The Worldwide Asset eXchange™ (WAX) is the world's most proven and
        eco-friendly blockchain for NFTs, video games and collectibles.
      </p>
      <div class="hero__list">
        <div class="hero__item" v-for="(item, index) in data" :key="index">
          <div class="hero__item_image"><img :src="item.image" /></div>
          <div class="hero__item_title" v-html="item.title"></div>
          <div class="hero__item_description">{{ item.description }}</div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    data: Array
  }
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";

.hero {
  background: white;
  color: #4f5052;

  background-image: url(images/background-mobile.jpg);
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;

  @include breakpoint(md) {
    background: transparent;
  }

  .hero__container {
    width: 320px;
    padding: 40px 6px;

    @include breakpoint(sm) {
      width: 620px;
    }

    @include breakpoint(md) {
      padding: 40px 25px;

      width: auto;
      column-gap: 50px;
      display: grid;
      grid-template-areas:
        "title list"
        "description list";
      align-items: center;
    }
  }

  .hero__title {
    margin-bottom: 20px;
    font-weight: 800;
    font-size: 36px;
    line-height: 1.1;
    grid-area: title;
  }

  .hero__r {
    font-size: 11px;
    vertical-align: top;
  }

  .hero__description {
    font-size: 18px;
    line-height: 1.4;
    margin-bottom: 35px;
    grid-area: description;
  }

  .hero__list {
    display: grid;
    grid-template-columns: 1fr 1fr;
    text-align: center;
    column-gap: 20px;
    row-gap: 40px;
    grid-area: list;

    @include breakpoint(md) {
      grid-template-columns: repeat(4, 1fr);
      column-gap: 10px;
    }
  }

  .hero__item_title {
    font-size: 28px;
  }

  .hero__item_description {
    font-size: 14px;
  }
}
</style>
