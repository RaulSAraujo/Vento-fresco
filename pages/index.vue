<template>
  <v-card color="black">
    <v-row justify="center" class="pt-8">
      <v-card color="transparent" width="35vw" class="pa-4">
        <v-card-title>
          <v-row justify="center">
            <span class="white--text text-h3">Bem-vindo à Vento Fresco</span>
          </v-row>
        </v-card-title>
        <v-card-text class="mt-8 d-flex justify-center">
          <v-sheet width="25vw" class="text-center" color="transparent">
            <span class="text-body-1 grey--text"
              >a nossa empresa tem como objetivo criar ventiladores
              revolucionários, que sejam controlados por aplicativos móveis e
              apresentem recursos avançados para minimizar o impacto
              ambiental.</span
            >
          </v-sheet>
        </v-card-text>
      </v-card>
    </v-row>

    <v-row justify="center" class="mt-12">
      <v-card width="1113px" height="519px" rounded="xl">
        <v-img src="/Banner.png" alt="banner" />
      </v-card>
    </v-row>

    <v-row justify="center" class="pt-8 mb-16">
      <v-card color="transparent" width="40vw" class="pa-4">
        <v-card-title>
          <v-row justify="center">
            <span class="white--text text-h3">VENTILADORES SUSTENTÁVEIS</span>
          </v-row>
        </v-card-title>
        <v-card-text class="mt-8 d-flex justify-center">
          <v-sheet width="25vw" class="text-center" color="transparent">
            <span class="text-body-1 grey--text"
              >Descubra como nossos ventiladores estão definindo o futuro da
              ventilação sustentável!
            </span>
          </v-sheet>
        </v-card-text>
        <v-card-actions class="mt-5">
          <v-row justify="center">
            <v-btn outlined color="indigo darken-1" x-large class="px-12"
              >Veja mais</v-btn
            >
          </v-row>
        </v-card-actions>
      </v-card>
    </v-row>

    <v-row justify="center" class="mt-16 py-10">
      <v-sheet color="transparent">
        <v-row>
          <v-card class="mt-16 mx-4" width="368" height="521" rounded="xl">
            <v-img src="/Ventilador1.png" alt="produto1" />
          </v-card>

          <v-card class="mt-n16 mx-4" width="368" height="521" rounded="xl">
            <v-img src="/Ventilador2.png" alt="produto2" />
          </v-card>

          <v-card class="mt-16 mx-4" width="368" height="521" rounded="xl">
            <v-img src="/Ventilador3.png" alt="produto3" />
          </v-card>
        </v-row>
      </v-sheet>
    </v-row>
  </v-card>
</template>

<script>
export default {

}
</script>

<style>
</style>
