<template>
  <div>
    <h2>{{ title }}</h2>

    <ul>

      <li v-for="post in posts" :key="post.id">

        {{ post.content }}

      </li>

    </ul>
    <h1 class="error">{{error_message}}</h1>
    <h1 v-if="!loaded">Loading...</h1>

  </div>
</template>

<script>
/* eslint-disable */
import axios from 'axios'

export default {
  name: "LatestPosts",
  props: {
    title: String
  },

  data() {
    return {
      posts: null,
      error_message:'',
      loaded : false

    }
  },
  created() {
    console.log('fetching Data')
    let configs = {
      responseType: 'json',
    }
    axios.get('http://127.0.0.1:8000/blog/posts/', configs)
        .then(response => {
              console.log('response arrived')
              let data_from_server = response.data
              let status_code = response.status
              console.log(data_from_server)
              console.log(status_code)
              this.posts = data_from_server
              this.loaded=true
            }
        ).catch(error => {
          console.log('response Error')
          this.error_message = "please see Areeb for help"
          this.loaded = true
        }
    )
    console.log('fetching Data done')

  },
}
</script>

<style scoped>
.error{
  color: red;
}
</style>