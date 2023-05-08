<template>
  <v-container>
    <v-row no-gutters class="mt-12">
      <span class="text-h3">Usuarios</span>
    </v-row>
    <v-row class="mt-2" justify="space-between">
      <v-col cols="3">
        <v-text-field
          v-model="search"
          filled
          placeholder="Busque o usuario"
          append-icon="mdi-magnify"
          hint="Filtre por nome, função ou status"
        ></v-text-field>
      </v-col>
      <v-col cols="2">
        <v-btn outlined color="blue" x-large to="/users/new"
          >Adicionar usuario</v-btn
        >
      </v-col>
    </v-row>
    <v-toolbar>
      <v-toolbar-title>LISTA DE USUARIOS</v-toolbar-title>
    </v-toolbar>
    <v-data-table
      :headers="headers"
      :items="items"
      :search="search"
      mobile-breakpoint="0"
    >
      <template #[`item.actions`]="{ item }">
        <NuxtLink :to="`/users/${item.id}`">
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
          name: 'Raul Silva Araujo',
          function: 'Admin',
          status: 'Ativo',
        },
        {
          id: 2,
          name: 'João paulo',
          function: 'Gerente vendas',
          status: 'Ativo',
        },
        {
          id: 3,
          name: 'Eduarda',
          function: 'Gerente produção',
          status: 'Desativo',
        },
      ],
      snack: false,
      editedIndex: 0,
    }
  },
  head: {
    titleTemplate: 'Usuarios - %s',
  },
  computed: {
    headers() {
      return [
        { text: 'Ações', align: 'start', sortable: false, value: 'actions' },
        { text: 'ID', align: 'start', sortable: false, value: 'id' },
        {
          text: 'NOME',
          align: 'start',
          sortable: false,
          value: 'name',
        },
        { text: 'FUNÇÃO', align: 'start', sortable: false, value: 'function' },
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
