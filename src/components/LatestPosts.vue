<template>
<div >
<h2>{{title}}</h2>
  <ul>

    <li v-for="post in posts" :key="post">

      {{post.title}}

    </li>

  </ul>

</div>
</template>

<script>
export default {
name: "LatestPosts",
  props: {
    title: String
  },

  data() {
    return {
      posts:   [
        {
          "title": "Fifth Post",
          "pub_date": "2020-10-19T11:03:03Z",
          "content": "This Is Your FifthPost"
        },
        {
          "title": "Forth Post",
          "pub_date": "2020-10-19T11:02:41Z",
          "content": "This Is Your Forth Post"
        },
        {
          "title": "Third Post",
          "pub_date": "2020-10-10T05:35:27Z",
          "content": "This Is Your Third Post"
        },
        {
          "title": "Second Post",
          "pub_date": "2020-10-10T05:35:05Z",
          "content": "This Is Your Second Post"
        },
        {
          "title": "First Post",
          "pub_date": "2020-10-10T05:34:52Z",
          "content": "This Is Your First Post"
        }
      ]

    }
  }
}
</script>

<style scoped>

</style>