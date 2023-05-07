<template>
  <div>
    <v-sheet color="black" rounded="b-xl">
      <v-container>
        <v-card width="476px" color="transparent">
          <v-card-title class="text-h4">Ventiladores</v-card-title>
          <v-card-text class="text-subtitle-1"
            >Os ventiladores têm sido uma escolha popular para refrescar
            ambientes por décadas, mas agora estão evoluindo para atender às
            demandas de consumidores preocupados com a
            sustentabilidade.</v-card-text
          >
        </v-card>
      </v-container>
    </v-sheet>

    <v-container class="my-6 px-12">
      <v-row>
        <v-col cols="2">
          <v-row class="ml-4" align="center">
            <span class="text-h6 mr-4">Filtros</span>
            <v-btn class="text-decoration-underline" plain small
              >Limpar Filtros</v-btn
            >
          </v-row>

          <v-list class="mt-3" color="transparent" subheader flat>
            <v-subheader class="white--text">Categorias</v-subheader>
            <v-list-item-group multiple>
              <v-list-item>
                <template #default="{ active }">
                  <v-list-item-action>
                    <v-checkbox
                      :input-value="active"
                      color="indigo darken-1"
                    ></v-checkbox>
                  </v-list-item-action>

                  <v-list-item-content>
                    <v-list-item-title>Ventiladores de teto</v-list-item-title>
                  </v-list-item-content>
                </template>
              </v-list-item>

              <v-list-item>
                <template #default="{ active }">
                  <v-list-item-action>
                    <v-checkbox
                      :input-value="active"
                      color="indigo darken-1"
                    ></v-checkbox>
                  </v-list-item-action>

                  <v-list-item-content>
                    <v-list-item-title>Ventiladores de mesa</v-list-item-title>
                  </v-list-item-content>
                </template>
              </v-list-item>

              <v-list-item>
                <template #default="{ active }">
                  <v-list-item-action>
                    <v-checkbox
                      :input-value="active"
                      color="indigo darken-1"
                    ></v-checkbox>
                  </v-list-item-action>

                  <v-list-item-content>
                    <v-list-item-title
                      >Ventiladores de coluna</v-list-item-title
                    >
                  </v-list-item-content>
                </template>
              </v-list-item>

              <v-list-item>
                <template #default="{ active }">
                  <v-list-item-action>
                    <v-checkbox
                      :input-value="active"
                      color="indigo darken-1"
                    ></v-checkbox>
                  </v-list-item-action>

                  <v-list-item-content>
                    <v-list-item-title>Ventiladores de torre</v-list-item-title>
                  </v-list-item-content>
                </template>
              </v-list-item>
            </v-list-item-group>
          </v-list>
        </v-col>
        <v-col>
          <v-row justify="end">
            <v-col cols="2">
              <v-select
                v-model="sort"
                prefix="Ordenar por:"
                :items="sortBy"
                outlined
                messages="Mostrando 6 produtos"
              ></v-select>
            </v-col>
          </v-row>
          <v-row>
            <v-col v-for="i in 6" :key="i" cols="4">
              <CardProduct />
            </v-col>
          </v-row>
          <v-row justify="center">
            <v-btn
              class="my-6"
              width="300"
              outlined
              large
              elevation="4"
              color="indigo darken-1"
              >Carregar mais produtos</v-btn
            >
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import CardProduct from '@/components/CardProducts.vue'
export default {
  components: {
    CardProduct,
  },
  data() {
    return {
      sort: 'Mais vendidos',
      sortBy: ['Mais vendidos', 'Lançamentos'],
    }
  },
}
</script>

<style>
</style>
