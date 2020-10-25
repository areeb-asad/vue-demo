<template>
  <div >
    <h2>{{title}}</h2>
  <ul>
    <li>Text 1</li>
    <li>Text 2</li>
    <li>Text 3</li>
  </ul>
  </div>
</template>

<script>
export default {
  name: "Polls",
  props: {
    title: String
  },

  }
</script>

<style scoped>

</style>