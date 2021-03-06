<template>
  <div id="app">
<!--    <HelloWorld msg="HelloWorld"/>-->

    <my--header :update="update"></my--header>
    <MyList @clicked="add()" :fruits="fruits" />
    {{ counter }}
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import List from '@/components/List.vue'

export default {
  name: 'App',
  data (){
    return {
      counter : 0,
      fruits : [
          "apple",
          "orange",
          "banana"
      ]
    }
  },
  components: {
    "my--header" : Header,
    "MyList" : List
  },
  methods : {
    update(){
      this.counter++;
    },
    add(){
      this.fruits.push("hello");
    }
  }
}
</script>

<style>
  *{
    padding: 0;
    margin: 0;
    font-family: sans-serif;
  }
</style>