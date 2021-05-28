<template>
  <div>
    <h1>Featured Articles</h1>
    <div>
      <ArticleCard
        v-for="article in articles"
        :key="article.slug"
        :slug="article.slug"
        :title="article.title"
        :teaser="article.metadata.teaser"
        :author="article.metadata.author"
        :content="article.content"
      />
    </div>
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
      /*props: 'slug,title,content,metadata' // Limit the API response data by props*/
    })
    const articles = await data.objects
    return {
      articles
    }
  },
}
</script>