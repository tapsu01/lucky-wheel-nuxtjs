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
        <a class="hc-luckywheel-btn" href="javascript:;">Xoay</a>
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

.hc-luckywheel {
  position: relative;
  width: 500px; /*Change this when change size*/
  height: 500px; /*Change this when change size*/
  border-radius: 50%;
  border: 16px solid #e44025;
  box-shadow: 0 2px 3px #333, 0 0 2px #000;
}

.hc-luckywheel {
  position: fixed;
  top: 50%;
  left: 50%;
  margin-top: -250px;
  margin-left: -250px;
}

.hc-luckywheel-btn {
  position: absolute;
  left: 210px; /*Change this when change size*/
  top: 210px; /*Change this when change size*/
  z-index: 3;
  width: 80px;
  height: 80px;
  border-radius: 50%;
  color: #f4e9cc;
  background-color: #e44025;
  line-height: 80px;
  text-align: center;
  font-size: 20px;
  text-shadow: 0 -1px 1px rgba(0, 0, 0, 0.6);
  box-shadow: 0 3px 5px rgba(0, 0, 0, 0.6);
  text-decoration: none;
}
</style>
