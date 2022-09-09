<template>
  <div>
    <h1>Foo</h1>
    <ul>
      <li v-for="item in posts" :key="item.id">
        <h4>{{ item.title }}</h4>
        <p>{{ item.body }}</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Foo',
  props: {
    posts: Array
  }
}
</script>

<style>

</style>