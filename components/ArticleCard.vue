<template>
  <nuxt-link
    class="block text-gray-800 rounded-lg shadow-lg p-6"
    :to="`/${slug}`"
  >
    <header class="text-2xl font-bold">{{ title }}</header>
    <p class="mt-4">{{ teaser }}</p>
    <footer class="flex items-center mt-6">
      <div class="ml-6">
        <p class="text-xl font-bold">{{ author.metadata.name }}</p>
        <p class="text-sm mt-1"><span v-html="content"></span></p>
      </div>
    </footer>
  </nuxt-link>
</template>

<script>
export default {
  props: {
    title: String,
    slug: String,
    title: String,
    teaser: String,
    author: Object,
    content: Object
  },
}
</script>