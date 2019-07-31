<template>
  <div id="ImageItem">
      <img  class="img" :src=image.baseimageurl alt="">
      <h4>Date: {{image.date}}</h4>
  </div>
</template>

<script>
export default {
  name: 'ImageItem',
  props: ["image"]
}
</script>
<style>
#ImageItem {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  padding: 5px;
  border: black solid 2px;
  margin-bottom: 25px;
  background-color: #41b883;
}
.img {
  height: 300px;
  width: 300px;
}
</style>
