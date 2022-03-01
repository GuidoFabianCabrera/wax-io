<template>
  <div class="nav">
    <div class="nav__container custom_container custom_container--lg ">
      <v-app-bar color="white" flat>
        <img class="nav__image" src="images/wax-logo.png" />
        <v-spacer></v-spacer>

        <v-menu
          transition="slide-y-transition"
          offset-y
          bottom
          min-width="100vw"
          content-class="nav__mobile"
        >
          <template v-slot:activator="{ on, attrs }">
            <v-app-bar-nav-icon
              class="nav__icon"
              v-bind="attrs"
              v-on="on"
            ></v-app-bar-nav-icon>
          </template>

          <v-list>
            <v-list-item
              style="display:block"
              v-for="(item, i) in items"
              :key="i"
            >
              <v-list-item
                style="color:#4f5052;font-weight:bold;font-size:14.4px;cursor:pointer"
                >{{ item.title
                }}<v-icon v-show="item.hasArrow"
                  >mdi-chevron-right</v-icon
                ></v-list-item
              >
              <v-list-item
                style="color:#4f5052;font-size:14.4px;margin-left:32px;cursor:pointer"
                v-for="(item, index) in item.item"
                :key="index"
                >{{ item }}<v-icon>mdi-chevron-right</v-icon></v-list-item
              >
            </v-list-item>
          </v-list>
        </v-menu>

        <div class="nav__list">
          <v-menu
            v-for="(item, index) in items"
            :key="index"
            open-on-hover
            offset-y
          >
            <template v-slot:activator="{ on, attrs }">
              <v-btn text light v-bind="attrs" v-on="on">
                {{ item.title }}
              </v-btn>
            </template>

            <v-list v-if="item.item" style="border:none">
              <v-list-item v-for="(item, index) in item.item" :key="index">
                <v-list-item-title class="nav__item">{{
                  item
                }}</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>
        </div>
      </v-app-bar>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          title: "Get Started",
          hasArrow: false,
          item: [
            "Wax Cloud Wallet",
            "How to Buy",
            "Trade or Sell NFTs",
            "Create NFTs",
            "Earn with WAX",
            "Games on WAX"
          ]
        },
        { title: "Carbon Neutrality", hasArrow: true, item: null },
        {
          title: "WAX Blockchain",
          hasArrow: false,
          item: [
            "WAX Labs",
            "Developer Portal",
            "Product Roadmap",
            "Become a Guild",
            "Resources"
          ]
        },
        { title: "About WAX", hasArrow: true, item: null },
        { title: "News", hasArrow: true, item: null }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";
.v-menu__content {
  box-shadow: none;
  border-radius: 0;
}

.theme--light.v-sheet--outlined {
  border: none;
}

.nav__mobile {
  display: initial;
  @include breakpoint(lg) {
    display: none;
  }
}

.test .v-list {
  color: red;
}
.nav {
  background: white;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 10;

  .nav__image {
    width: 115px;
    height: 100%;
  }

  .nav__icon {
    @include breakpoint(lg) {
      display: none;
    }
  }

  .nav__icon span i {
    font-size: 44px;
    color: #cdcdcd;
  }

  .nav__list {
    display: none;
    @include breakpoint(lg) {
      color: #4f5052;
      display: flex;
    }
  }
}
</style>
