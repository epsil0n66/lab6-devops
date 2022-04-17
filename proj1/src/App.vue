<template
class="grey darken-1">
  <v-app>
  <div>
    <v-card
      flat
      tile
  >
    <v-container
    fluid
    class = "d-flex blue darken-4">
        <v-btn
          fab
          rounded
          x-small
          class = "red ma-2"
        ></v-btn>
        <v-btn
          class = "yellow ma-2"
          fab
          rounded
          x-small
        ></v-btn>
        <v-btn
          class="green ma-2"
          fab
          rounded
          x-small
        ></v-btn>
        <v-btn
          class="ma-2"
          color="white"
          text
          @click="mission"
        >
        <v-divider
        vertical
        class="mx-4 grey darken-2"
        ></v-divider>
        ЗАДАНИЕ НА СЪЕМКУ 001
        </v-btn>
    



      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon
        >mdi-bell</v-icon>
      </v-btn>

      <v-btn
        elevation="2"
        class="ma-2"
        outlined
        color="white"
      >
      НА СЕРВЕР
      </v-btn>
      
      <v-btn
        elevation="2"
        color="primary"
        class="ma-2"
      >
      С СЕРВЕРА
      </v-btn>
      </v-container>

  </v-card>

  <v-container
   class="grey lighten-5 rounded-lg"
   >
    <v-row no-gutters>
      <v-col
      md="8">
        <div
          style="min-height: 70hv;"
          class="pa-2 rounded-lg"
          outlined
          tile
        >
          <v-btn
          class="ma-3">
            Карта участка
          </v-btn>
          <v-btn
          class="ma-3"
          >
            Информация
          </v-btn>
          <v-img
          src="https://sun9-75.userapi.com/impg/BUIILY8-N49b70aJou1PpyKiTlcQlRy7J5Krww/VS-19mKwNmI.jpg?size=746x546&quality=96&sign=6ad0ec9e15ad8e602931e76cb5bbe2d6&type=album"
          >
          </v-img>
        </div>
      </v-col>
      <v-col>
        <div
          class="pa-2"
          outlined
          tile
        >
          <v-btn
          class="ma-3">
            Задания на вылет
          </v-btn>
          <v-btn
          class="ma-3">
            Обработка данных
          </v-btn>
            <v-data-table
              :headers="headers"
              :items="desserts"
              :items-per-page="5"
              class="elevation-1"
            ></v-data-table>
        </div>
      </v-col>
    </v-row>
  </v-container>
  </div>
    <v-main>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  components: {
  },

  data: () => ({
    //
  }),
};
</script>
