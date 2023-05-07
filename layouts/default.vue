<template>
  <v-app dark>
    <AppBar />
    <v-main>
      <Nuxt />
    </v-main>

    <FooterPage />
  </v-app>
</template>

<script>
import AppBar from '~/components/AppBarShop.vue'
import FooterPage from '~/components/FooterPage.vue'
export default {
  name: 'DefaultLayout',
  components: {
    AppBar,
    FooterPage,
  },
  data() {
    return {}
  },
}
</script>
