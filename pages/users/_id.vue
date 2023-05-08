<template>
  <v-container>
    <v-row class="my-7" justify="space-between">
      <v-col cols="3">
        <span class="text-h4">Editar produto ID.{{ $route.params.id }}</span>
      </v-col>
      <v-col cols="2">
        <v-btn plain to="/users">
          <v-icon class="mr-2">mdi-arrow-left</v-icon>
          Retornar para os produtos
        </v-btn>
      </v-col>
    </v-row>
    <v-card class="pa-5">
      <span class="text-h5">Nome completo</span>
      <v-text-field v-model="details.name" filled></v-text-field>
      <span class="text-h5">Função</span>
      <v-text-field v-model="details.function" filled></v-text-field>
      <span class="text-h5">Status</span>
      <v-radio-group v-model="details.status" row>
        <v-radio value="Ativo" label="Ativo"></v-radio>
        <v-radio value="Inativo" label="Inativo"></v-radio>
      </v-radio-group>

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
