<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
      flat
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink ml-4"
          contain
          src="https://chain.link/assets/images/icon-logo-white-ef878c98.svg"
          transition="scale-transition"
          width="40"
        />

        <v-toolbar-title class="ml-5"> <span class="title font-weight-bold">LINK</span> News</v-toolbar-title>
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
      </v-btn>
    </v-app-bar>

    <v-main>
      <SideMenu/>
    </v-main>
  </v-app>
</template>

<script>
import SideMenu from './components/SideMenu';

export default {
  name: 'App',

  components: {
    SideMenu,
  },
};
</script>
