<template>
  <v-sheet
    height="93vh"
    width="100vw"
    color="black"
    class="d-flex justify-center align-center"
  >
    <div class="text-center">
      <span class="blue--text text-h3">GERENCIAR</span>
      <v-card height="50" hidden color="transparent"></v-card>
      <v-sheet
        width="60vw"
        height="35vh"
        rounded="xl"
        style="border: 1px solid blue; background: transparent"
        class="d-flex justify-space-around align-center"
      >
        <div>
          <v-card
            width="200px"
            height="200px"
            outlined
            rounded="xl"
            style="border: 1px solid blue; background: transparent"
            class="d-flex justify-center"
            elevation="5"
            to="/users"
          >
            <v-icon size="150" color="blue">mdi-account-cog</v-icon>
          </v-card>
          <span class="blue--text text-h6">USUARIOS</span>
        </div>

        <div>
          <v-card
            width="200px"
            height="200px"
            outlined
            rounded="xl"
            style="border: 1px solid blue; background: transparent"
            class="d-flex justify-center"
            elevation="5"
            to="/stock"
          >
            <v-icon size="150" color="blue">mdi-window-shutter-cog</v-icon>
          </v-card>
          <span class="blue--text text-h6">ESTOQUE</span>
        </div>

        <div>
          <v-card
            width="200px"
            height="200px"
            rounded="xl"
            class="d-flex justify-center"
            style="border: 1px solid blue; background: transparent"
            elevation="5"
            to="/sales"
          >
            <v-icon size="150" color="blue">mdi-store-cog-outline</v-icon>
          </v-card>
          <span class="blue--text text-h6">VENDAS</span>
        </div>
      </v-sheet>
    </div>
  </v-sheet>
</template>

<script>
export default {
  layout: 'ManagementLayout',
  head: {
    titleTemplate: 'Gerencial - %s',
  },
}
</script>

<style>
</style>
