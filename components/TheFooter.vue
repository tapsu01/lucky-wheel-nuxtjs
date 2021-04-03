<template>
  <footer
    class="lg:border-t border-light-border dark:border-dark-border transition-colors duration-300 ease-linear bg-white"
  >
    <div
      class="container mx-auto px-4 flex flex-row items-center content-center justify-center py-4"
    >
      <p>Copyright {{ getFullYear() }} &copy; JetCare</p>
    </div>
  </footer>
</template>

<script>
import DevToIcon from '@/assets/icons/dev-to.svg?inline';
import NuxtIcon from '@/assets/icons/nuxt.svg?inline';
export default {
  components: {
    DevToIcon,
    NuxtIcon,
  },
  methods: {
    getFullYear() {
      const d = new Date();
      const n = d.getFullYear();
      return n;
    },
  },
};
</script>
