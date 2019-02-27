<template>
  <div class="crypto">
    <div class="crypto-wrap">
      <h1>Crytpo information daily</h1>
      <h2>{{cryptoData}}</h2>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import axios from 'axios'

export default {
  name: 'Crypto',
  components: {
  },
  data() {
    return {
      cryptoData: null
    }
  },
  mounted () {
    axios.get('https://api.coindesk.com/v1/bpi/currentprice.json')
    .then(response => (this.cryptoData = response))
  }
}
</script>

<style>

.crypto-wrap{
  position: absolute;
  top: 10%;
  left:5%;
  border: 3px gray groove;
  width: 600px;
  height: 400px;
  overflow: auto;
}
</style>
