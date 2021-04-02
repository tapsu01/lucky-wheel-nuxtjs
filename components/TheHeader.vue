<template>
  <header
    class="flex justify-between items-center bg-white dark:bg-gray-900 border-b dark:border-gray-900 p-4 text-gray-700 dark:text-gray-500 text-xl font-bold"
  >
    <nuxt-link to="/" class="logo-wrapper">
      <nuxt-icon />
    </nuxt-link>
    <nav>
      <ul>
        <li v-for="link in links" :key="link.slug">
          <nuxt-link :to="{ name: link.slug }">
            {{ link.name }}
          </nuxt-link>
        </li>
      </ul>
    </nav>
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
