<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <LatestPosts title="Latest Posts Title"/>
    <polls title="Polls Title" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import LatestPosts from "./components/LatestPosts";
import Polls from "@/components/Polls";

export default {
  name: 'App',
  components: {
    Polls,
    LatestPosts,
    HelloWorld
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
