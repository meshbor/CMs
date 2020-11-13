<template>
  <v-app>
    <v-app-bar
      app
      color="blue-grey darken-2"
      dark
    >
      <div class="d-flex align-center">

        MEF test
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Something Later</span>
        <!-- <v-icon>mdi-open-in-new</v-icon> -->
      </v-btn>
    </v-app-bar>

    <v-main>
      <List/>
      <Mef/>
    </v-main>
  </v-app>

</template>

<script>
import List from './components/List';
import Mef from './components/Mef'

export default {
  name: 'App',

  components: {
    List,
    Mef,
  },

  data: () => ({
    //
  }),
};
</script>
