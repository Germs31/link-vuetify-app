<template>
  <v-row justify="space-around">
    <v-card
        dark
        width=400
        outlined
        shaped
        >
        <div class="link-header">
            <v-card-title>
                <v-avatar size="50">
                    <img :src="`${link[0].logo_url}`" alt="">
                </v-avatar>
                <v-card-title>{{link[0].currency}}</v-card-title>
            </v-card-title>
        </div>

        <v-card-title>${{Math.round(link[0].price)}}</v-card-title>
        <v-card-text>
            <div>
                Circulating Supply:
                {{link[0].circulating_supply}}
            </div>
            <div>
                Max Supply:
                {{link[0].max_supply}}
            </div>
            <div>
                Market Cap: 
                {{link[0].market_cap}}
            </div>
        </v-card-text>
    </v-card>
  </v-row>
</template>

<script>
export default {
    name: 'LinkPrice',
    props: ['link']
}
</script>

<style>
</style>