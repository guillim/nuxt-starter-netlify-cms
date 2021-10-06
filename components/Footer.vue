<template>
  <footer class="mt-12 bg-gray-800">
    <div class="max-w-screen-xl px-4 py-12 mx-auto sm:px-6 lg:py-16 lg:px-8">
      <div class="xl:grid xl:grid-cols-3 xl:gap-8">
        <div class="grid grid-cols-2 gap-8 xl:col-span-2">
          <div class="md:grid md:grid-cols-2 md:gap-8">
            <div>
              <ul class="mt-4 space-y-4">
                <li>
                  <nuxt-link
                    to="/"
                    class="text-base leading-6 text-gray-300 hover:text-white"
                  >
                    Retour
                  </nuxt-link>
                </li>
                <li>
                  <a
                    href="/admin"
                    target="_blank"
                    nofollow
                    class="text-base leading-6 text-gray-300 hover:text-white"
                  >
                    Admin
                  </a>
                </li>
              </ul>
            </div>
            <div class="mt-12 md:mt-0">
              <ul class="mt-4 space-y-4">
                <li>
                  <nuxt-link
                    to="/contact"
                    class="text-base leading-6 text-gray-300 hover:text-white"
                  >
                    Nous contacter
                  </nuxt-link>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {}
</script>

<style scoped></style>
