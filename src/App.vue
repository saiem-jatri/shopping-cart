<template>
  <nav>
    <router-link :class="{active: $route.name === 'home'}" :to="{ name: 'home'}">Home</router-link> |
    <router-link :class="{active: $route.name === 'cart'}" :to="{ name: 'cart'}">Cart</router-link>
  </nav>
  <router-view/>
</template>

<script>
export default {
  // mounted() {
  //   this.$store.commit('updateCartFromLocalStorage')
  // }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

html, body{
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}

body{
  background-color: rgb(245,245,245);
}

#nav{
  padding: 10px;
  width: 100%;
  height: 30px;
  background-color: white;
  line-height: 30px;
}

a{
  font-weight: bold;
  color: darkgray;
  text-decoration: none;
  margin: 0 5px;
  font-size: 1.25rem;

  &.active{
    color: #2c3e50;
  }
}

.text-center{
  text-align: center;
}
</style>
