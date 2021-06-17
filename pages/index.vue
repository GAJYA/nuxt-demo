<template>
  <div>
      <h1>{{ title }}</h1>
      <nuxt-link to="/fun">fun</nuxt-link>
      <br>
      <foo :posts="posts" />
  </div>
</template>

<script>
import axios from 'axios'
import Foo from '@/components/foo.vue'
export default {
  name: 'HomePage',
  components: {
    Foo
  },
  async asyncData () {
    console.log('asyncData');
    const res = await axios({
      method: 'get',
      url: 'http://localhost:3333/data.json'
    })
    return res.data
  }

}
</script>

<style>

</style>