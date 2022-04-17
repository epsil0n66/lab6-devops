<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <v-img
          :src="require('../assets/logo.svg')"
          class="my-3"
          contain
          height="200"
        />
      </v-col>
      <v-dialog
      v-model="dialog"
      width="25vw">
        <v-card>
          <v-card-title class="text-h5 grey lighten-2">
           {{dialog_message}}
            <v-icon>
             mdi-cross
            </v-icon>
          </v-card-title>
        </v-card>
      </v-dialog>
      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3">
          Приложение на Vue
        </h1>

        <p class="subheading font-weight-regular">
          <v-btn
          @click="handle_button()">
            Ошибиться
          </v-btn>
          <v-btn
          @click="handle_button2()">
            Серьезно ошибиться
          </v-btn>
        </p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'HelloWorld',

    data: () => ({
      dialog: false,
      dialog_message: null,
    }),
    methods: {
      handle_button(){
        this.dialog = true
        this.dialog_message = 'Вы поступили в СурГУ'
        throw new ReferenceError('Sentry error')

      },
      handle_button2(){
        this.dialog = true
        this.dialog_message = 'Вы получили диплом СурГУ'
        throw new Error('Another error')
      }
    }
  }
</script>
