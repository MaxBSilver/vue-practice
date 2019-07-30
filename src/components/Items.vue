<template>
  <div id="Items">

  </div>
</template>

<script>
import Item from './Item';
export default {
  name: 'Items',
  components: {
    Item
  },
  props: ["images"]
}
</script>

<style>
#items {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
}
</style>
