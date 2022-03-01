<template>
  <section
    class="template_section"
    v-bind:style="{ background: data.background }"
  >
    <div
      class="template_section__container custom_container custom_container--lg"
      v-bind:class="{ 'template_section__container--large': data.large }"
    >
      <h1
        class="template_section__title"
        v-bind:class="{ 'template_section__title--large': data.large }"
      >
        {{ data.title }}
      </h1>
      <p
        class="template_section__description"
        v-bind:class="{ 'template_section__description--large': data.large }"
        v-html="data.description"
      ></p>
      <slot></slot>
      <div class="template_section__button_container" v-if="data.button">
        <v-btn
          class="template_section__button"
          v-for="(item, index) in data.button"
          :key="index"
          rounded
          color="#1aa2c0"
          dark
          large
          :outlined="item.outlined"
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
.template_section {
  // background: transparent;
  color: #4f5052;

  background-image: url(/images/background-mobile.jpg);
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;

  @include breakpoint(md) {
    background: transparent;
  }

  .template_section__container {
    padding-top: 50px;
    padding-bottom: 50px;
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;

    @include breakpoint(md) {
      padding-top: 80px;
      padding-bottom: 70px;
    }
  }

  .template_section__container--large {
    @include breakpoint(md) {
      width: 771px;
    }
  }

  .template_section__title {
    margin-bottom: 25px;
    font-weight: 800;
    font-size: 36px;
    line-height: 1.1;

    width: 320px;
    margin-left: auto;
    margin-right: auto;
    @include breakpoint(sm) {
      width: 556px;
    }

    @include breakpoint(md) {
      width: 568px;
    }
  }

  .template_section__title--large {
    @include breakpoint(md) {
      width: 100%;
    }
  }

  .template_section__description {
    margin-bottom: 40px;
    font-size: 18px;
    line-height: 1.4;

    width: 320px;
    margin-left: auto;
    margin-right: auto;
    @include breakpoint(sm) {
      width: 556px;
    }

    @include breakpoint(md) {
      width: 568px;
    }
  }

  .template_section__description--large {
    @include breakpoint(md) {
      width: 100%;
    }
  }

  .template_section__button {
    margin-top: 20px;
  }

  .template_section__button_container {
    display: flex;
    flex-direction: column;

    @include breakpoint(sm) {
      flex-direction: row;
      column-gap: 15px;
    }
  }
}
</style>
