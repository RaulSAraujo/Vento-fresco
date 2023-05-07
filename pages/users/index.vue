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
        <v-btn outlined color="blue" x-large to="/users/new">Adicionar usuario</v-btn>
      </v-col>
    </v-row>
    <v-data-table
      :headers="headers"
      :items="items"
      :search="search"
      mobile-breakpoint="0"
    >
      <template #[`item.actions`]="{ item }">
        <v-icon small class="mr-2" color="blue"> mdi-pencil </v-icon>
        <v-icon small color="pink" @click="deleteItem(item)">
          mdi-delete
        </v-icon>
      </template>
    </v-data-table>
  </v-container>
</template>

<script>
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
    }
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
    deleteItem(item) {
      const editedIndex = this.items.indexOf(item)
      this.items.splice(editedIndex, 1)
    },
  },
}
</script>

<style>
</style>
