<template>
  <v-app dark>
    <AppBar />
    <v-main>
      <Nuxt />
    </v-main>
  </v-app>
</template>

<script>
import AppBar from '@/components/AppBarManage.vue'
export default {
  name: 'ManagementLayout',
  components: { AppBar },
  data() {
    return {}
  },
}
</script>
