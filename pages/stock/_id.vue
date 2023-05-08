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
      <v-text-field filled></v-text-field>
      <span class="text-h5">Descrição</span>
      <v-text-field filled></v-text-field>
      <v-row>
        <v-col>
          <span class="text-h5">Quantidade</span>
          <v-text-field filled></v-text-field>
        </v-col>
        <v-col>
          <span class="text-h5">Cor</span>
          <v-text-field filled></v-text-field>
        </v-col>
        <v-col>
          <span class="text-h5">Status</span>
          <v-radio-group row>
            <v-radio value="active" label="Ativo"></v-radio>
            <v-radio value="desactive" label="Inativo"></v-radio>
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
export default {
  layout: 'ManagementLayout',
  props: {

  },
}
</script>

<style>
</style>
