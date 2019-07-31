/* eslint-disable */
<template>
  <div id="app">
    <h1>Harvard Image Gallery</h1>
    <Images v-bind:images="images"></Images>
    <footer> This application was made possible by the <img class="logo" src=https://calendar.artsboston.org/wp-content/uploads/sites/calendar.artsboston.org/images/venue/1030/harvard_logo_square.jpg></footer>
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

   created() {
    axios.get(`https://api.harvardartmuseums.org/image/?apikey=${API_KEY}`)
      .then(res => this.images=res.data.records)
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
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
h1 {
  color :#41b883;
  border-bottom: 1px solid #34495e;
  margin: 0 auto;
  padding: 10px;
}
.logo {
  width: 150px;
  height: 150px;
}
footer {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
