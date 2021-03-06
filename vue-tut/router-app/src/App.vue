<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link :to="{ name : 'Profile', params : {id : 122, category : 'mycat'} }">Profile</router-link>
  </div>
  <router-view />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>

<!--
  Routing {
    define routing in router/index.js after user <router-link></router-link> and pass params if want
    pass params { name : "some", params : {}, query : {} },
    children {
      passing children routes for the main routes
    }
    lazy-loading : {
      about is lazy-loaded it optimize the code and loading
    }
  }
-->