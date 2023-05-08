<template>
  <v-container>
    <v-row no-gutters class="mt-12">
      <span class="text-h3">Estoque</span>
    </v-row>
    <v-row class="mt-2" justify="space-between">
      <v-col cols="3">
        <v-text-field
          v-model="search"
          filled
          placeholder="Busque o produto"
          append-icon="mdi-magnify"
          hint="Filtre por produto, descrição, cor, estoque ou status."
        ></v-text-field>
      </v-col>
      <v-col cols="2">
        <v-btn outlined color="blue" x-large to="/stock/new"
          >Adicionar produto</v-btn
        >
      </v-col>
    </v-row>

    <v-toolbar>
      <v-toolbar-title>LISTA DE PRODUTOS</v-toolbar-title>
    </v-toolbar>
    <v-data-table
      :headers="headers"
      :items="items"
      :search="search"
      mobile-breakpoint="0"
    >
      <template #[`item.actions`]="{ item }">
        <NuxtLink :to="`/stock/${item.id}`">
          <v-icon small class="mr-2" color="blue" @click="setDetail(item)">
            mdi-pencil
          </v-icon>
        </NuxtLink>

        <v-icon small color="pink" @click="deleteItem(item)">
          mdi-delete
        </v-icon>
      </template>
    </v-data-table>

    <v-snackbar
      v-model="snack"
      color="blue"
      top
      centered
      outlined
      rounded="xl"
      :timeout="-1"
    >
      Deseja deletar o produto ?

      <v-btn color="green" plain @click="snack = false">Não</v-btn>
      <v-btn color="pink" plain @click="removeItem">Sim</v-btn>
    </v-snackbar>
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
          product: 'Ventilador 1',
          description: 'Ventilador 120v',
          stock: 1,
          cor: 'Preto',
          status: 'Ativo',
        },
        {
          id: 2,
          product: 'Ventilador 2',
          description: 'Ventilador 220v',
          stock: 10,
          cor: 'Verde',
          status: 'Ativo',
        },
        {
          id: 3,
          product: 'Ventilador 3',
          description: 'Ventilador 120v',
          stock: 2,
          cor: 'Branco',
          status: 'Ativo',
        },
        {
          id: 4,
          product: 'Ventilador 4',
          description: 'Ventilador 220v',
          stock: 50,
          cor: 'Vermelho',
          status: 'Ativo',
        },
        {
          id: 5,
          product: 'Ventilador 5',
          description: 'Ventilador 120v',
          stock: 40,
          cor: 'Azul',
          status: 'Ativo',
        },
        {
          id: 6,
          product: 'Ventilador 6',
          description: 'Ventilador 220v',
          stock: 30,
          cor: 'Amarelo',
          status: 'Ativo',
        },
      ],
      snack: false,
      editedIndex: 0,
    }
  },
  computed: {
    headers() {
      return [
        { text: 'Ações', align: 'start', sortable: false, value: 'actions' },
        { text: 'ID', align: 'start', sortable: false, value: 'id' },
        {
          text: 'PRODUTO',
          align: 'start',
          sortable: false,
          value: 'product',
        },
        {
          text: 'DESCRIÇÃO',
          align: 'start',
          sortable: false,
          value: 'description',
        },
        {
          text: 'ESTOQUE',
          align: 'start',
          sortable: false,
          value: 'stock',
        },
        { text: 'COR', align: 'start', sortable: false, value: 'cor' },
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
    deleteItem(item) {
      this.editedIndex = this.items.indexOf(item)
      this.snack = true
    },
    removeItem() {
      this.items.splice(this.editedIndex, 1)
      this.snack = false
    },
  },
}
</script>

<style>
</style>
