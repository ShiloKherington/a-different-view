<template>
  <div class="mt-4">
    <section>
      <div class="container mx-auto px-4">
        <h1 class="text-4xl font-bold">Featured Articles</h1>
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 mt-4">
          <ArticleCard
            v-for="article in articles"
            :key="article.slug"
            :slug="article.slug"
            :title="article.title"
            :content="article.content"
            :date="article.metadata.date"
            :teaser="article.metadata.teaser"
            :hero="article.metadata.hero"
            :author="article.metadata.author"
            :tags="article.metadata.tags"
          />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
const Cosmic = require('cosmicjs')
const api = Cosmic()
const bucket = api.bucket({
  slug: '41947280-bf62-11eb-be48-39507926bc2a',
  read_key: 'ngXWCk42H3ub0anSeqBZx1TaFH1Qb0PVWnObyjqkNtsuG4jbsQ'
})
export default {
  async asyncData() {
    const data = await bucket.getObjects({
     query: {
        type: 'articles'
      },
      props: 'slug,title,content,metadata.date,metadata.teaser,metadata.hero,metadata.author,metadata.tags'
    })
    const articles = await data.objects
    return {
      articles
    }
  },
}
</script>