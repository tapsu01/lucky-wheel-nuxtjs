<template>
  <header
    class="sticky top-0 left-0 right-0 z-30 bg-light-elevatedSurface dark:bg-dark-elevatedSurface h-16 lg:h-18 transition-colors duration-300 ease-linear shadow bg-white"
  >
    <div
      class="container relative mx-auto px-4 flex items-center lg:py-6 h-full"
    >
      <a
        href="/"
        class="inline-block text-nuxt-gray h-7 lg:h-10 z-10 mr-auto nuxt-link-active"
      >
        <h1 class="m-0 h-0 w-0 overflow-hidden">
          NUXTJS
        </h1>
        <img src="@/assets/images/logo-without-txt.png" class="w-8" />
      </a>
      <nav class="hidden lg:flex lg:pt-1 xl:pt-0 mx-auto">
        <ul class="flex text-center">
          <li class="xl:px-4 lg:py-0 lg:px-2 py-2">
            <a
              href="/docs/2.x/get-started/installation"
              class="block font-medium uppercase hover:no-underline light:hover:text-nuxt-lightgreen dark:hover:text-nuxt-lightgreen text-light-onSurfacePrimary dark:text-dark-onSurfacePrimary transition-colors duration-300 ease-linear"
            >
              Giới thiệu
            </a>
          </li>
          <li class="xl:px-4 lg:py-0 lg:px-2 py-2">
            <a
              href="/examples"
              class="block font-medium uppercase hover:no-underline light:hover:text-nuxt-lightgreen dark:hover:text-nuxt-lightgreen text-light-onSurfacePrimary dark:text-dark-onSurfacePrimary transition-colors duration-300 ease-linear"
            >
              Sản phẩm
            </a>
          </li>
          <li class="xl:px-4 lg:py-0 lg:px-2 py-2">
            <a
              href="/resources"
              class="block font-medium uppercase hover:no-underline light:hover:text-nuxt-lightgreen dark:hover:text-nuxt-lightgreen text-light-onSurfacePrimary dark:text-dark-onSurfacePrimary transition-colors duration-300 ease-linear"
            >
              Hợp tác
            </a>
          </li>
          <li class="xl:px-4 lg:py-0 lg:px-2 py-2">
            <a
              href="/blog"
              class="block font-medium uppercase hover:no-underline light:hover:text-nuxt-lightgreen dark:hover:text-nuxt-lightgreen text-light-onSurfacePrimary dark:text-dark-onSurfacePrimary transition-colors duration-300 ease-linear"
            >
              Blog
            </a>
          </li>
          <li class="xl:px-4 lg:py-0 lg:px-2 py-2">
            <a
              href="https://masteringnuxt.com/?utm_source=nuxt&amp;utm_medium=link&amp;utm_campaign=navbar_link"
              target="_blank"
              rel="noopener"
              class="block font-medium uppercase hover:no-underline hover:text-nuxt-lightgreen text-light-onSurfacePrimary dark:text-dark-onSurfacePrimary transition-colors duration-300 ease-linear"
            >
              Liên hệ
            </a>
          </li>
        </ul>
      </nav>
      <div>
        <div
          class="relative inline-block w-10 mr-2 align-middle select-none transition duration-200 ease-in"
        >
          <input
            type="checkbox"
            name="dark-mode"
            id="dark-mode"
            class="toggle-checkbox absolute block w-6 h-6 rounded-full bg-white border-4 appearance-none cursor-pointer"
          /><label
            for="dark-mode"
            class="toggle-label block overflow-hidden h-6 rounded-full cursor-pointer"
          ></label>
        </div>
        <label for="dark-mode" class="text-xs text-gray-700 dark:text-gray-500"
          >Dark Mode</label
        >
      </div>
    </div>
  </header>
</template>

<script>
import NuxtIcon from '@/assets/icons/nuxt.svg?inline';
export default {
  components: {
    NuxtIcon,
  },
  data() {
    return {
      links: [
        {
          name: 'New',
          slug: 'index',
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
