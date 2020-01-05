<template>
  <div>
    <h1>{{ title }}</h1>
    <nuxt-link to="/">Home</nuxt-link>
    <!-- <NuxtLink to="/">Home</NuxtLink>
    <NLink to="/">Home</NLink>
    <n-link to="/">Home</n-link> -->
  </div>
</template>

<script>
export default {
  asynData() {
    return { title: 'About' }
  },
  fetch() {},
  head() {
    return {
      title: 'About',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'My Amazing About Page'
        }
      ],
      script: [{ src: '/about.js' }]
    }
  }
}
</script>

<style></style>
