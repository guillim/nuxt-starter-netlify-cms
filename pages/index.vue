<template>
  <div>
    <Hero
      :heading="page.heading"
      :subheading="page.subheading"
      :image="page.image"
    />
    <div
      class="px-8 mx-auto mt-12 prose sm:px-6 md:px-4 lg:px-2 xl:px-0 xl:prose-xl lg:prose-lg md:prose-md"
    >
      <p>
        {{ page.mainpitch.description }}
      </p>

      <div class="lg:grid lg:grid-cols-2 lg:gap-8">
        <div
          v-for="(post, index) in posts"
          :key="index"
          class="px-6 border rounded-lg shadow my-2"
          style="box-shadow:0 1px 3px 0 #3c814b66"
        >
          <h3>
            <nuxt-link :to="`/blog/${post.slug}`">{{ post.title }}</nuxt-link>
          </h3>
          <p>
            {{ post.description }}
          </p>
          <p>
            <nuxt-link :to="`/blog/${post.slug}`">En savoir plus</nuxt-link>
          </p>
        </div>
      </div>
      <p class="text-center">
        On a hâte de vous voir !
      </p>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const page = await $content('index').fetch()
    const posts = await $content('blog').fetch()
    posts.sort( (a,b) => a.order - b.order)
    return {
      page,
      posts,
    }
  },
}
</script>
