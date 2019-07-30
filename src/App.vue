/* eslint-disable */
<template>
  <div id="app">
    <h1>art gallery</h1>
    <Images></Images>
  </div>
</template>

<script>
import axios from 'axios';
import Images from './components/Images';
import {API_KEY} from './config';
export default {
  name: 'app',
  components: {
    Images
  },
  data() {
    return {
      images: []
    }
  },
  methods: {
   
  },
   created() {
    axios.get(`https://api.harvardartmuseums.org/image/?apikey=${API_KEY}`)
      .then(res => this.images=res.data.records)
      .catch(err => console.log(err));
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
