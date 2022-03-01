<template>
  <section class="image_section" v-bind:style="{ background: data.background }">
    <div
      class="image_section__container custom_container custom_container--lg"
      v-bind:class="{ 'image_section__container--large': data.large }"
    >
      <img class="image_section__logo_top" :src="data.logoTop" />
      <h1 class="image_section__title">{{ data.title }}</h1>
      <p class="image_section__description" v-html="data.description"></p>
      <div v-bind:class="{ image_section__image_container: data.button }">
        <img class="image_section__image" v-bind:src="data.image" />
        <img
          class="image_section__image_mobile"
          v-bind:src="data.imageMobile"
        />
      </div>
      <div class="image_section__button_container" v-if="data.button">
        <v-btn
          class="image_section__button"
          v-for="(item, index) in data.button"
          :key="index"
          rounded
          color="#1aa2c0"
          dark
          large
          >{{ item.text }}</v-btn
        >
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    data: Object
  }
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";
.image_section {
  // background: transparent;
  color: #4f5052;

  background-image: url(/wax-io/images/background-mobile.jpg);
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;

  @include breakpoint(md) {
    background: transparent;
  }

  .image_section__container {
    width: 320px;
    padding-top: 50px;
    padding-bottom: 50px;
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;

    @include breakpoint(sm) {
      width: 620px;
    }

    @include breakpoint(md) {
      padding-top: 80px;
      padding-bottom: 70px;
      width: 568px;
    }
  }

  .image_section__container--large {
    @include breakpoint(md) {
      width: 771px;
    }
  }

  .image_section__logo_top {
    width: 84px;
    margin-bottom: 15px;
  }

  .image_section__title {
    margin-bottom: 25px;
    font-weight: 800;
    font-size: 36px;
    line-height: 1.1;
  }

  .image_section__description {
    margin-bottom: 40px;
    font-size: 18px;
    line-height: 1.4;
  }

  .image_section__image_container {
    margin-bottom: 20px;
  }

  .image_section__image {
    margin: 0 auto;
    display: none;
    @include breakpoint(md) {
      display: block;
    }
  }

  .image_section__image_mobile {
    margin: 0 auto;
    @include breakpoint(md) {
      display: none;
    }
  }

  .image_section__button {
    margin-top: 20px;
  }
}
</style>
