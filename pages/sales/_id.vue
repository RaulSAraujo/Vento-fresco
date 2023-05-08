<template>
  <v-container>
    <v-row class="my-7" justify="space-between">
      <v-col cols="3">
        <span class="text-h4">Pedido ID.{{ $route.params.id }}</span>
      </v-col>
      <v-col cols="2">
        <v-btn plain to="/sales">
          <v-icon class="mr-2">mdi-arrow-left</v-icon>
          Retornar para os pedidos
        </v-btn>
      </v-col>
    </v-row>
    <v-card class="pa-5">
      <v-row>
        <v-col cols="8">
          <span class="text-h5">Produto</span>
          <v-text-field v-model="details.product" filled></v-text-field>
        </v-col>
        <v-col cols="2">
          <span class="text-h5">Status</span>
          <v-text-field v-model="details.status" filled></v-text-field>
        </v-col>
        <v-col cols="2">
          <span class="text-h5">Quantidade</span>
          <v-text-field v-model="details.quantity" filled></v-text-field>
        </v-col>
      </v-row>

      <v-row>
        <v-col>
          <span class="text-h5">Nome completo</span>
          <v-text-field v-model="details.client" filled></v-text-field>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="10">
          <span class="text-h5">Rua</span>
          <v-text-field v-model="details.address" filled></v-text-field>
        </v-col>
         <v-col cols="2">
          <span class="text-h5">Cep</span>
          <v-text-field v-model="details.cep" filled></v-text-field>
        </v-col>
      </v-row>

      <v-row>
        <v-col>
          <span class="text-h5">Valor</span>
          <v-text-field v-model="details.value" filled></v-text-field>
        </v-col>
      </v-row>

      <v-row no-gutters justify="center">
        <v-btn outlined color="blue darking-1" x-large class="px-12"
          >SALVAR</v-btn
        >
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
import { mapState } from 'vuex'
export default {
  layout: 'ManagementLayout',
  computed: {
    ...mapState({
      details: (state) => state.details,
    }),
  },
}
</script>

<style>
</style>
