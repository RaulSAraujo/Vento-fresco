<template>
  <v-app-bar app>
    <v-breadcrumbs :items="items"></v-breadcrumbs>
    <v-spacer></v-spacer>
    <v-avatar color="indigo" size="38px">
      <span class="white--text text-h5">RA</span>
    </v-avatar>
    <v-btn plain to="/">
      SAIR
      <v-icon>mdi-exit-to-app</v-icon>
    </v-btn>
  </v-app-bar>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          text: 'Estoque',
          href: '/stock',
        },
        {
          text: 'Usuario',
          href: '/users',
        },
        {
          text: 'Vendas',
          href: '/sales',
        },
      ],
    }
  },
}
</script>

<style>
</style>
