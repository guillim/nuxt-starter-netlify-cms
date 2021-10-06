<template>
  <footer class="mt-12 bg-gray-800">
    <div class="max-w-screen-xl px-4 py-12 mx-auto sm:px-6 lg:py-16 lg:px-8">
      <div class="">
        <div class="">
          <div class="">
            <div>
              <ul class="mt-4 space-y-4 flex justify-between">
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
