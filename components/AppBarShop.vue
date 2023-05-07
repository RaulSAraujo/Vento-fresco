<template>
  <v-app-bar app color="black" outlined>
    <v-row justify="space-around">
      <v-col cols="7">
        <v-row align="center">
          <span
            class="text-h5 mr-5"
            style="cursor: pointer"
            @click="LandingPage"
            >Vento Fresco</span
          >

          <v-btn-toggle group>
            <v-btn plain to="/shop">Loja</v-btn>
            <v-btn plain>Ajuda</v-btn>
            <v-btn plain>Sobre</v-btn>
            <v-btn plain>
              <v-icon class="mr-1">mdi-magnify</v-icon>
              Buscar
            </v-btn>
          </v-btn-toggle>
        </v-row>
      </v-col>
      <v-col cols="1">
        <v-btn plain color="blue darken-1" to="/login">
          <v-icon class="mr-2">mdi-shopping</v-icon>
          Login
        </v-btn>
      </v-col>
    </v-row>
  </v-app-bar>
</template>

<script>
export default {
  methods: {
    LandingPage() {
      this.$router.push('/')
    },
  },
}
</script>

<style>
</style>
