<template>
  <div class="container mx-auto px-4 mt-4">
    <header>
      <h2 class="text-5xl">{{ this.slug }}</h2>
      <p>Path: {{ $route.path }}</p>
      <div class="flex items-center mt-6">
        <img
          class="w-20 rounded-full border-4 border-main"
          
        />
        <div class="ml-6">
          <p class="text-xl font-bold"></p>
          <p class="text-sm mt-1">

          </p>
        </div>
      </div>
    </header>
    <div class="mt-8">
    </div>
  </div>
</template>

<script>  
export default {
  async asyncData({ params }) {
    const slug = params.slug
    return { slug }
  }
}
</script>

