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
  components: {
    ImageItem
  },
  props: ["images"]
}
</script>

<style>
#Images {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
}
</style>
