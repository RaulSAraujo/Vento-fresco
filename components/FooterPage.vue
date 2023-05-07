<template>
  <v-footer height="350">
    <v-row justify="center">
      <v-col cols="3">
        <v-card color="transparent" elevation="0">
          <v-card-title class="text-h4 blue--text text--darken-1">
            Assine a nossa newsletter
          </v-card-title>
          <v-card-text class="white--text">
            Seja o primeiro a saber sobre nossas ofertas especiais, lançamentos
            de novos produtos e eventos
          </v-card-text>
          <v-card-actions>
            <v-text-field outlined label="Email" color="indigo darken-1" filled>
              <template #append>
                <v-row dense>
                  <v-btn plain small>Inscrever-se</v-btn>
                </v-row>
              </template>
            </v-text-field>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col cols="2">
        <v-card color="transparent" elevation="0">
          <v-card-title class="text-h6 blue--text text--darken-1">
            Loja
          </v-card-title>
          <v-card-text class="white--text">
            <v-btn plain>Ventilador de teto</v-btn>
            <v-btn plain>Ventilador de mesa</v-btn>
            <v-btn plain>Ventilador de coluna</v-btn>
            <v-btn plain>Ventilador de torre</v-btn>
            <v-btn plain>Cartões de presente</v-btn>
            <v-btn plain>Oferta</v-btn>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="2">
        <v-card color="transparent" elevation="0">
          <v-card-title class="text-h6 blue--text text--darken-1">
            Ajuda
          </v-card-title>
          <v-card-text class="white--text">
            <v-btn plain>Centro de ajuda</v-btn>
            <v-btn plain>Status do pedido</v-btn>
            <v-btn plain>Devoluções e Garantia</v-btn>
            <v-btn plain>Contate-nos</v-btn>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="2">
        <v-card color="transparent" elevation="0">
          <v-card-title class="text-h6 blue--text text--darken-1">
            Sobre
          </v-card-title>
          <v-card-text class="white--text">
            <v-btn plain>Sobre nós</v-btn>
            <v-btn plain>Responsabilidade</v-btn>
            <v-btn plain>Tecnologia e Inovação</v-btn>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-footer>
</template>

<script>
export default {}
</script>

<style>
</style>
