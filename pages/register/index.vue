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
      <v-card-title class="my-5">
        <v-row justify="center" class="text-h4">
          CADASTRO
        </v-row>
      </v-card-title>
      <v-card-text class="px-8">
        <v-text-field label="Nome completo" filled clearable></v-text-field>
        <v-text-field label="E-mail" filled clearable></v-text-field>
        <v-text-field label="Senha" filled clearable></v-text-field>
        <v-text-field
          label="Confirmação da senha"
          filled
          clearable
        ></v-text-field>
        <v-text-field label="Username" filled clearable></v-text-field>
        <v-checkbox
          label="Gostaria de receber novidades de nossos produtos em seu email."
          hide-details
        ></v-checkbox>
        <v-checkbox label="Li e aceito os Termos de uso"></v-checkbox>

        <v-row no-gutters justify="center" class="my-5">
          <v-btn outlined color="blue darken-1" class="px-10" large
            >Login</v-btn
          >
        </v-row>
      </v-card-text>
    </v-card>
  </v-sheet>
</template>

<script>
export default {
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
