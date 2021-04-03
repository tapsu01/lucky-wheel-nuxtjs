<template>
  <div class="container min-h-screen">
    <div>
      <section
        id="luckywheel"
        class="hc-luckywheel fixed top-1/2 left-1/2 -ml-64 -mt-64 rounded-full border-8"
      >
        <div
          class="hc-luckywheel-container absolute left-0 top-0 z-1 w-inherit h-inherit rounded-inherit bg-clip-padding bg-yellow-400"
        >
          <canvas
            class="hc-luckywheel-canvas w-inherit h-inherit rounded-full"
            width="500px"
            height="500px"
            >Vòng Xoay May Mắn</canvas
          >
        </div>
        <a
          class="hc-luckywheel-btn absolute z-3 rounded-full"
          href="javascript:;"
          >Xoay</a
        >
      </section>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({});
</script>

<style lang="scss" scoped>
.z-1 {
  z-index: 1;
}

.z-3 {
  z-index: 3;
}

.rounded-inherit {
  border-radius: inherit;
}

.h-inherit {
  height: inherit;
}

.w-inherit {
  width: inherit;
}
</style>
