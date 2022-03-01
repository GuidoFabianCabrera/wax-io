<template>
  <SharedTemplateSection :data="data">
    <div class="email__content">
      <label class="email__title" for="email">Email</label>
      <input class="email__input" type="email" name="email" id="email" />
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

.email__content {
  text-align: left;

  .email__title {
    font-weight: bolder;
    font-size: 14px;
    display: block;
    margin-bottom: 10px;
  }

  .email__input {
    font-size: 10px;
    background-color: #dddddd;
    color: #000;
    border-radius: 20px;
    height: 41px;
    font-size: 13px;
    line-height: 13px;
    padding-left: 13px;
    padding-right: 13px;
    width: 295px;
  }

  .email__input:focus {
    outline: none;
  }
}
</style>
