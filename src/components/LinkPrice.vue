<template>
  <v-card
    dark
    max-width=500
    outlined
    shaped
    >
      <v-card-subtitle>{{link[0].currency}}</v-card-subtitle>
      <v-card-title>{{link[0].price}}</v-card-title>
      <v-card-text>
          Circulating Supply: {{link[0].circulating_supply}}
          Market Cap: {{link[0].market_cap}}
          Max Supply: {{link[0].max_supply}}
      </v-card-text>
      <v-card-text>
          Market Cap: {{link[0].market_cap}}
      </v-card-text>
      <v-card-text>
          Max Supply: {{link[0].max_supply}}
      </v-card-text>


  </v-card>
</template>

<script>
// import axios from 'axios'
export default {
    name: 'LinkPrice',
    props: ['link']
}
</script>

<style>

</style>