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
      <p>
        {{ page.description }}
      </p>
      <h2 class="text-center m-auto" >à lire :</h2>
      <div class="lg:grid lg:grid-cols-2 lg:gap-8">
        <div
          v-for="(post, index) in posts"
          :key="index"
          class="px-6 border rounded-lg shadow"
        >
          <h3>
            <nuxt-link :to="`/blog/${post.slug}`">{{ post.title }}</nuxt-link>
          </h3>
          <p>
            {{ post.description }}
          </p>
          <p>
            <nuxt-link :to="`/blog/${post.slug}`">Read more</nuxt-link>
          </p>
        </div>
      </div>
      <p class="text-center">
        <nuxt-link
          to="/blog"
          class="inline-flex items-center px-6 py-3 text-base font-medium leading-6 transition duration-150 ease-in-out bg-white border border-gray-300 rounded-md text-kaldi hover:text-orange-500 focus:outline-none focus:border-blue-300 focus:shadow-outline-blue active:text-gray-800 active:bg-gray-50"
        >
          Read more
        </nuxt-link>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const page = await $content('index').fetch()
    const posts = await $content('blog').fetch()

    return {
      page,
      posts,
    }
  },
}
</script>
