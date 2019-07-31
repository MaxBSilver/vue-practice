<template>
  <div id="Images">
    <div v-bind:key="image.id" v-for="image in images">
      <ImageItem v-bind:image="image" />
    </div>
  </div>
</template>

<script>
import ImageItem from './ImageItem';
export default {
  name: 'Images',
   props: ["images"],
  components: {
    ImageItem
  }
}
</script>

<style>
#Images {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  display: flex;
  flex-wrap: wrap;
  margin-top: 30px;
  justify-content: space-around
}
</style>
