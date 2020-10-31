<template>
  <v-app>
    <Navbar/>
    <SideMenu />
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
  import Navbar from './components/Navbar'
  import SideMenu from './components/SideMenu'
  export default {
    components: {Navbar, SideMenu}
  }
</script>

<style lang="scss">
</style>
