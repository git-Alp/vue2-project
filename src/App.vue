<template>
  <div id="app">
    <nav>
      <router-link v-for="item in nav" :key="item.name" :to="item.path"> {{item.name}} </router-link>
    </nav>
    <router-view />
  </div>
</template>

<script>
export default {
  data() {
    return {
      nav: this.$router.options.routes
    }
  },
  created () {
    this.init();
  },
  methods: {
    init: function () {
     console.log("this.$router.options.routes", this.$router.options.routes); 
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
