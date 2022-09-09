<template>
  <div>
    Hello Nuxt!<br />
    <nuxt-link to="/about">About</nuxt-link>
    <Foo :posts="posts" />
  </div>
</template>
<script>
import Foo from '../components/Foo.vue';
import axios from 'axios';

export default {
  name: 'HomePage',
  components: {
    Foo,
  },
  async asyncData({isDev, route, store, env, params, query, req, res, redirect, error}) {
    console.log('====-19asyncData');
    const data = await axios({
      method: 'GET',
      url: 'http://localhost:3000/data.json',
    });
    return data.data; 
  },
}
</script>