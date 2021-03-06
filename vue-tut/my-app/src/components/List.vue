<template>
  <div>
    <div v-for="(item, inx) in fruits" :key="inx">{{ item }}</div>
    <button @click="$emit('clicked')">Add</button>
  </div>
</template>

<script>
export default {
  props : {
    fruits : Array
  }
}
</script>

<style scoped>

</style>