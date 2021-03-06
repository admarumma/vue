<template>
  <header>
    <div class="logo">
      <h3>MyLogo</h3>
    </div>
    <div class="navigation">
      <nav class="navs">
        <a href="">Home</a>
      </nav>
      <nav class="navs">
        <a href="">Menu</a>
      </nav>
      <nav class="navs">
        <a href="">About</a>
      </nav>
      <nav class="navs">
        <a href="">Contact</a>
      </nav>
      <button @click="update">click me</button>
    </div>
  </header>
</template>

<script>
export default {
  props : {
    update : {
      type : Function,
      default : () => {alert(11)}
    }
  }
}
</script>

<style scoped>
  header{
    padding: 20px;
    display: flex;
    justify-content: space-between;
    align-content: center;
    background-color: #3b3b3b;
    color: white;
  }
  .navigation{
    display: flex;
  }
  a{
    color: white;
    text-decoration: none;
    padding: 10px 20px;
  }
</style>