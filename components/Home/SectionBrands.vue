<template>
  <section class="brands">
    <div class="brands__container custom_container">
      <div class="brands__title">
        All of your favorite brands and collectibles.
      </div>
      <div class="brands__title">All in one place.</div>
      <div class="brands__list">
        <div class="brands__item" v-for="(item, index) in data" :key="index">
          <div
            class="brands__image_container"
            v-bind:class="{ 'brands__image_container--small': item.small }"
          >
            <img class="brands__image" :src="item.image" />
          </div>
        </div>
      </div>
      <v-btn rounded color="#1aa2c0" dark large width="160px">buy now</v-btn>
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

.brands {
  background-image: url(/images/background-mobile.jpg);
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;

  @include breakpoint(md) {
    background: transparent;
  }

  .brands__container {
    width: 320px;
    padding: 70px 6px;
    text-align: center;

    @include breakpoint(sm) {
      width: 620px;
    }

    @include breakpoint(md) {
      padding: 110px 25px 60px;
      width: auto;
    }
  }

  .brands__title {
    margin-bottom: 20px;
    font-weight: 800;
    font-size: 36px;
    line-height: 1.1;
    color: #4f5052;
  }

  .brands__list {
    margin: 80px 0;
    align-items: center;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
    row-gap: 20px;
  }

  .brands__item {
    width: 33%;
    max-width: 100%;

    &:nth-child(4),
    &:nth-child(5),
    &:nth-child(9),
    &:nth-child(10) {
      width: 50%;
      @include breakpoint(md) {
        width: 25%;
      }
    }

    @include breakpoint(md) {
      width: 25%;

      &:nth-child(5),
      &:nth-child(6),
      &:nth-child(7) {
        width: 33%;
      }
    }
  }

  .brands__image_container {
    padding: 0 10px;

    @include breakpoint(sm) {
      padding: 0 25px;
    }
  }

  .brands__image {
    width: initial;
    max-width: 100%;
  }
}
</style>
