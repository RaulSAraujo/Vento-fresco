<template>
  <v-sheet
    color="black"
    height="100vh"
    width="100vw"
    class="d-flex justify-center align-center"
    style="
      background-image: url('/efeitos.png');
      background-repeat: no-repeat;
      background-position: left bottom;
      background-size: cover;
    "
  >
    <v-card
      class="gradient-card"
      elevation="0"
      color="transparent"
      width="408"
      rounded="xl"
    >
      <v-img width="400" height="300" src="/logo.png" alt="logo"></v-img>
      <v-card-text class="px-8">
        <v-text-field
          label="Username"
          filled
          clearable
          hide-details
        ></v-text-field>
        <v-row
          no-gutters
          justify="end"
          class="blue--text mb-2"
          style="cursor: pointer"
        >
          Esqueceu sua senha?
        </v-row>
        <v-text-field
          label="Password"
          filled
          clearable
          hide-details
        ></v-text-field>
        <v-checkbox label="Lembrar da senha"></v-checkbox>

        <v-row no-gutters justify="center" class="my-5">
          <v-btn
            outlined
            color="blue darken-1"
            class="px-10"
            large
            to="/management"
            >Login</v-btn
          >
        </v-row>

        <v-card outlined class="pa-3" color="rgba(158, 158, 158,0.2)">
          <v-row no-gutters justify="center" align="center">
            <span class="text-subtitle-1 mr-1">Novo por aqui ?</span>
            <span
              class="text-subtitle-2 blue--text text-darken-1"
              style="cursor: pointer"
              @click="register"
              >Crie a sua conta aqui.</span
            >
          </v-row>
        </v-card>
      </v-card-text>
    </v-card>
  </v-sheet>
</template>

<script>
export default {
  head: {
    titleTemplate: 'Login - %s',
  },
  methods: {
    register() {
      this.$router.push('/register')
    },
  },
}
</script>

<style>
.gradient-card {
  background: linear-gradient(
    50deg,
    rgba(10, 11, 15, 0.504) 50%,
    rgba(16, 76, 227, 0.444) 100%
  );
}
</style>
