<template>
  <div>
    About Page!
    <h2>a链接</h2>
    <a href="/">首页</a>
    <h2>router-link</h2>
    <router-link to="/">首页</router-link>
    <h2>编程导航</h2>
    <button @click="onClick">首页</button>
  </div>
</template>
<script>
export default {
  name: 'AboutPage',
  methods: {
    onClick() {
      this.$router.push('/');
    }
  },
}
</script>