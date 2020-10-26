<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <LatestPosts title="Latest Posts Title"/>
  </div>
</template>

<script>
import LatestPosts from "@/components/LatestPosts";

export default {
  name: 'App',
  components: {
    LatestPosts
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
