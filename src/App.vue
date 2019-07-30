<template>
  <div id="app">
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import axios from 'axios';

export default {
  name: 'app',
  components: {
  },
  data() {
    return {
      images: []
    }
  },
  methods: {
    created() {
    axios.get(`https://api.harvardartmuseums.org/image/?apikey=${}`)
      .then(res => this.images = res.data)
      .catch(err => console.log(err));
  }
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
