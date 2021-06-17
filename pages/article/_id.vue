<template>
  <div>
      <h1>{{ article.title }}</h1>
      <p>{{ article.body }}</p>
  </div>
</template>

<script>
import axios from 'axios'
export default {
    async asyncData (context) {
        const { data } = await axios({
            method: 'GET',
            url: 'http://localhost:3333/data.json'
        })
        console.log(context);
        return {
            article: data.posts.find(item => item.id === Number.parseInt(context.params.id))
        }
    }

}
</script>

<style>

</style>