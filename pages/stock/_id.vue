<template>
  <v-container>
    <v-row class="my-7" justify="space-between">
      <v-col cols="3">
        <span class="text-h4">Editar produto ID.{{ $route.params.id }}</span>
      </v-col>
      <v-col cols="2">
        <v-btn plain to="/stock">
          <v-icon class="mr-2">mdi-arrow-left</v-icon>
          Retornar para os produtos
        </v-btn>
      </v-col>
    </v-row>
    <v-card class="pa-5">
      <span class="text-h5">Nome produto</span>
      <v-text-field v-model="details.product" filled></v-text-field>
      <span class="text-h5">Descrição</span>
      <v-text-field v-model="details.description" filled></v-text-field>
      <v-row>
        <v-col>
          <span class="text-h5">Quantidade</span>
          <v-text-field v-model="details.stock" filled></v-text-field>
        </v-col>
        <v-col>
          <span class="text-h5">Cor</span>
          <v-text-field v-model="details.cor" filled></v-text-field>
        </v-col>
        <v-col>
          <span class="text-h5">Status</span>
          <v-radio-group v-model="details.status" row>
            <v-radio value="Ativo" label="Ativo"></v-radio>
            <v-radio value="Inativo" label="Inativo"></v-radio>
          </v-radio-group>
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
  head: {
    titleTemplate: 'Editar produto - %s',
  },
  computed: {
    ...mapState({
      details: (state) => state.details,
    }),
  },
}
</script>

<style>
</style>
