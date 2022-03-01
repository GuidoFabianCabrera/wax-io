<template>
  <v-app app>
    <LayoutNav />
    <v-main>
      <Nuxt />
    </v-main>
    <LayoutFooter />
  </v-app>
</template>

<script>
import LayoutNav from "@/components/Layouts/Nav";
import LayoutFooter from "@/components/Layouts/Footer";

export default {
  components: {
    LayoutNav,
    LayoutFooter
  }
};
</script>
