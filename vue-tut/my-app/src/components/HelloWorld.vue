<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

    <div class="twiiter-box">
      <form action="" @submit.prevent="submit">
        <input type="text" v-model="text">
        <button :disabled="triggerTO < 0 ? true : false" type="submit">Submit</button>
      </form>
      <span :class="triggerTO < 0 ? 'red' : ''">{{ triggerTO }}</span>
      <div class="messages">
        <div class="message" v-for="(item, key) in messages" :key="key">{{ item.message }}</div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      text: "",
      maxLength: 120,
      messages: []
    }
  },
  computed: {

    triggerTO() {
      return this.maxLength - this.text.length;
    }
  },
  props: {
    msg: String
  },
  methods: {
    submit() {
      this.messages.push({
        message: this.text
      })
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.red {
  color: red !important;
}
</style>


<!--
Computed properties : {
 in every situation when property has changed which is inside of computed property it will work
}

Watcher are : {
  They watch for any change and returns old value and new value access it in option propertyName(oldvalue, newvalue)
}

Components diff with react : {
  have to declare usable in components array
}

Props are {
  we can pass them like react and can validate them with props property in export obj as
  number : Number or number : { type : Number, default : 1 }
}

????????????????????????????????????????????????????

what is the $emit('eventName')

-->