<template>
  <div class="home">
    <v-container>
      <LinkPrice :link="linkData"/>
    </v-container>
  </div>
</template>

<script>
import axios from 'axios'
import LinkPrice from '@/components/LinkPrice'
export default {
  name: 'Home',
  components: {LinkPrice},
  data() {
    return {
      linkData: null
    }
  },
  mounted() {
      axios.get(`https://api.nomics.com/v1/currencies/ticker?key=${process.env.VUE_APP_APIKEY}&ids=LINK`)
      .then(res => {
        console.log(res.data)
        this.linkData = res.data
      })
      .catch(err => console.log(err))
  }
}
</script>
