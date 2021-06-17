<template>
  <div>
      <h1>foopage</h1>
      <ul>
          <li v-for="item in posts" :key="item.id"> {{ item.title }}</li>
      </ul>
  </div>
</template>

<script>
export default {
    name: 'FooPage',
    props: ['posts']
    // async asyncData () {
    //     console.log('asyncData');
    //     return {
    //         posts: [{
    //             title: 'hahhah'
    //         }]
    //     }
    // }

}
</script>

<style>

</style>