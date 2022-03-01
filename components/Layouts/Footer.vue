<template>
  <div class="footer">
    <div class="footer__container custom_container custom_container--lg">
      <img class="footer__logo footer__logo--desktop" src="images/footer.png" />
      <img
        class="footer__logo footer__logo--mobile"
        src="images/footer-mobile.png"
      />
      <div class="footer__social">
        <div
          class="footer__social_item"
          v-for="(item, index) in icons"
          :key="index"
        >
          <img class="footer__social_image" :src="item" />
        </div>
      </div>
      <div class="footer__links">
        <div
          class="footer__item"
          v-for="(itemLink, index) in links"
          :key="index"
        >
          <div class="footer__item_title">{{ itemLink.title }}</div>
          <div
            class="footer__item_link"
            v-for="(list, index) in itemLink.item"
            :key="index"
          >
            {{ list }}
          </div>
        </div>
      </div>
      <div class="footer__copyright">
        © 2021 WAX, Worldwide Asset eXchange.™ All rights reserved.
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      icons: [
        "images/twitter-logo.svg",
        "images/discord-logo.svg",
        "images/artboard-logo.svg",
        "images/youtube-logo.svg",
        "images/instagram-logo.svg",
        "images/facebook-logo.svg"
      ],
      links: [
        {
          title: "RESOURCES",
          item: ["Privacy", "Terms", "Whitepaper", "Careers"]
        },
        { title: "COMMUNITY", item: ["Join the Community", "Blog"] },
        {
          title: "BLOCKCHAIN",
          item: ["WAX Cloud Wallet", "WAX Proposal System", "WAX Explorer"]
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";
.footer {
  background: white;

  .footer__container {
    width: 352px;
    padding-top: 70px;
    padding-bottom: 10px;
    display: grid;
    row-gap: 60px;
    text-align: center;

    @include breakpoint(md) {
      width: initial;
      grid-template-columns: 1fr 4fr;
      column-gap: 30px;
      row-gap: 40px;
    }
  }

  .footer__logo {
    margin: 0 auto;
    cursor: pointer;
    @include breakpoint(md) {
      margin: 0 0;
      grid-column: 2 span;
    }
  }

  .footer__logo--desktop {
    display: none;
    @include breakpoint(md) {
      display: block;
    }
  }

  .footer__logo--mobile {
    display: block;
    @include breakpoint(md) {
      display: none;
    }
  }

  .footer__social {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    align-items: center;
    row-gap: 30px;
    @include breakpoint(md) {
      height: fit-content;
    }
  }

  .footer__social_item {
    width: 48px;
    margin: 0 auto;
    cursor: pointer;
    @include breakpoint(md) {
      width: 32px;
    }
  }

  .footer__social_image {
    width: 100%;
    display: block;
  }

  .footer__links {
    display: flex;
    flex-direction: column;
    row-gap: 45px;
    margin-top: 20px;

    @include breakpoint(md) {
      margin-top: 0;
      flex-direction: row;
      justify-content: space-evenly;
      text-align: left;
    }
  }

  .footer__item {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    @include breakpoint(md) {
      flex-direction: column;
      flex-wrap: nowrap;
      justify-content: initial;
    }
  }

  .footer__item_title {
    width: 100%;
    color: #4f5052;
    font-weight: 800;
  }

  .footer__item_link {
    margin-top: 15px;
    font-size: 13px;
    cursor: pointer;
    @include breakpoint(md) {
      margin-top: 30px;
    }
  }

  .footer__item_link:hover {
    color: #1aa2c0;
  }

  .footer__copyright {
    font-size: 12px;
    color: rgb(145, 147, 150);
    @include breakpoint(md) {
      grid-column: 2 span;
      margin-top: 45px;
      margin-bottom: 20px;
    }
  }
}
</style>
