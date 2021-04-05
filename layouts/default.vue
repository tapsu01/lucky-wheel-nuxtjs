<template>
  <div>
    <the-header />
    <Nuxt />
    <the-footer />
  </div>
</template>

<script>
import TheHeader from '@/components/TheHeader';
import TheFooter from '@/components/TheFooter';

export default {
  components: {
    TheHeader,
    TheFooter,
  },
};
</script>

<style lang="scss">
html,
body {
  font-family: 'Quicksand Light', sans-serif;
}
</style>
