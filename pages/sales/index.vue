<template>
  <v-container>
    <v-row no-gutters class="mt-12">
      <span class="text-h3">Vendas</span>
    </v-row>
    <v-row class="mt-2" justify="space-between">
      <v-col cols="3">
        <v-text-field
          v-model="search"
          filled
          placeholder="Busque o cliente"
          append-icon="mdi-magnify"
          hint="Filtre por cliente, produtos, endereço ou cep."
        ></v-text-field>
      </v-col>
    </v-row>

    <v-toolbar>
      <v-toolbar-title>LISTA DE VENDAS</v-toolbar-title>
    </v-toolbar>
    <v-data-table
      :headers="headers"
      :items="items"
      :search="search"
      mobile-breakpoint="0"
    >
      <template #[`item.actions`]="{ item }">
        <NuxtLink :to="`/sales/${item.id}`">
          <v-icon small class="mr-2" color="blue" @click="setDetail(item)">
            mdi-pencil
          </v-icon>
        </NuxtLink>
      </template>
    </v-data-table>
  </v-container>
</template>

<script>
import { mapMutations } from 'vuex'
export default {
  layout: 'ManagementLayout',
  data() {
    return {
      search: '',
      items: [
        {
          id: 1,
          client: 'Raul',
          product: 'Ventilador 1',
          quantity: 1,
          address: 'R. Irênio Greco, 4580',
          cep: '14405-191',
          value: '120.00',
          status: 'A enviar',
        },
      ],
    }
  },
  head: {
    titleTemplate: 'Vendas - %s',
  },
  computed: {
    headers() {
      return [
        { text: 'Ações', align: 'start', sortable: false, value: 'actions' },
        { text: 'ID', align: 'start', sortable: false, value: 'id' },
        { text: 'CLIENTE', align: 'start', sortable: false, value: 'client' },
        {
          text: 'PRODUTOS',
          align: 'start',
          sortable: false,
          value: 'product',
        },
        {
          text: 'QUANTIDADE',
          align: 'start',
          sortable: false,
          value: 'quantity',
        },
        {
          text: 'ENDEREÇO',
          align: 'start',
          sortable: false,
          value: 'address',
        },
        { text: 'CEP', align: 'start', sortable: false, value: 'cep' },
        { text: 'VALOR', align: 'start', sortable: false, value: 'value' },
        { text: 'STATUS', align: 'start', sortable: false, value: 'status' },
      ]
    },
  },
  methods: {
    ...mapMutations({
      setDetails: 'setDetails',
    }),
    setDetail(details) {
      this.setDetails(details)
    },
  },
}
</script>

<style>
</style>
