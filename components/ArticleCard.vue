<template>
  <nuxt-link
    class="block text-gray-800 rounded-lg shadow-lg p-6"
    :to="slug"
    >
    <header class="text-2xl font-bold mb-4">Article Title: {{ title }}</header>
    <img :src="hero.imgix_url" alt="" />
    <p class="mt-4">Teaser: {{ teaser }}</p>
    <!--<div class="ml-3">
      <p class="text-sm mt-1"><span v-html="content"></span></p>
    </div>
    -->
  </nuxt-link>
</template>

<script>
export default {
  props: {
    slug: String,
    title: String,
    teaser: String,
    author: Object,
    content: String,
    hero: Object,
    date: String,
    tags: Array
  },
}
</script>

<style scoped>
p {
  margin-bottom: 10px;
}
</style>