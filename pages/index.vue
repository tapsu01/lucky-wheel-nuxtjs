<template>
  <div class="container min-h-screen">
    <div>
      <section id="luckywheel" class="hc-luckywheel">
        <div class="hc-luckywheel-container">
          <canvas class="hc-luckywheel-canvas" width="500px" height="500px"
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

export default {
  data() {
    return {
      isPercentage: true,
      prizes: [
        {
          text: 'Áo thun J2Team',
          img: 'images/Ao.png',
          number: 1, // 1%,
          percentpage: 0.01, // 1%
        },
        {
          text: 'Nón J2 Team',
          img: 'images/Non.png',
          number: 1,
          percentpage: 0.05, // 5%
        },
        {
          text: 'Vòng Tay J2Team',
          img: 'images/Vong.png',
          number: 1,
          percentpage: 0.1, // 10%
        },
        {
          text: 'J2Team Security',
          img: 'images/j2_logo.png',
          number: 1,
          percentpage: 0.24, // 24%
        },
        {
          text: 'Chúc bạn may mắn lần sau',
          img: 'images/miss.png',
          percentpage: 0.6, // 60%
        },
      ],
    };
  },
  methods: {
    randomIndex(prizes: any): any {
      const vm = this;
      if (vm.isPercentage) {
        var counter = 1;
        for (let i = 0; i < prizes.length; i++) {
          if (prizes[i].number == 0) {
            counter++;
          }
        }
        if (counter == prizes.length) {
          return null;
        }
        let rand = Math.random();
        let prizeIndex = null;
        console.log(rand);
        switch (true) {
          case rand < prizes[4].percentpage:
            prizeIndex = 4;
            break;
          case rand < prizes[4].percentpage + prizes[3].percentpage:
            prizeIndex = 3;
            break;
          case rand <
            prizes[4].percentpage +
              prizes[3].percentpage +
              prizes[2].percentpage:
            prizeIndex = 2;
            break;
          case rand <
            prizes[4].percentpage +
              prizes[3].percentpage +
              prizes[2].percentpage +
              prizes[1].percentpage:
            prizeIndex = 1;
            break;
          case rand <
            prizes[4].percentpage +
              prizes[3].percentpage +
              prizes[2].percentpage +
              prizes[1].percentpage +
              prizes[0].percentpage:
            prizeIndex = 0;
            break;
        }
        if (prizeIndex && prizes[prizeIndex].number != 0) {
          prizes[prizeIndex].number = prizes[prizeIndex].number - 1;
          return prizeIndex;
        } else {
          return vm.randomIndex(prizes);
        }
      } else {
        var counter = 0;
        for (let i = 0; i < prizes.length; i++) {
          if (prizes[i].number == 0) {
            counter++;
          }
        }
        if (counter == prizes.length) {
          return null;
        }
        var rand = (Math.random() * prizes.length) >>> 0;
        if (prizes[rand].number != 0) {
          prizes[rand].number = prizes[rand].number - 1;
          return rand;
        } else {
          return vm.randomIndex(prizes);
        }
      }
    },
  },
};
</script>

<style lang="scss" scoped>
.hc-luckywheel ul,
.hc-luckywheel li {
  margin: 0;
  padding: 0;
  list-style: none;
}

.hc-luckywheel {
  position: relative;
  width: 500px; /*Change this when change size*/
  height: 500px; /*Change this when change size*/
  border-radius: 50%;
  border: 16px solid #e44025;
  box-shadow: 0 2px 3px #333, 0 0 2px #000;
  box-sizing: content-box;
}

.hc-luckywheel {
  position: fixed;
  top: 50%;
  left: 50%;
  margin-top: -250px;
  margin-left: -250px;
}

.hc-luckywheel-container {
  position: absolute;
  left: 0;
  top: 0;
  z-index: 1;
  width: inherit;
  height: inherit;
  border-radius: inherit;
  background-clip: padding-box;
  background-color: #ffcb3f;
  -webkit-transition: transform 6s ease;
  transition: transform 6s ease;
}

.hc-luckywheel-container canvas {
  width: inherit;
  height: inherit;
  border-radius: 50%;
}

.hc-luckywheel-list {
  position: absolute;
  left: 0;
  top: 0;
  width: inherit;
  height: inherit;
  z-index: 2;
}

.hc-luckywheel-item {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  color: #e4370e;
  font-weight: bold;
  text-shadow: 0 1px 1px rgba(255, 255, 255, 0.6);
}

.hc-luckywheel-item span {
  position: relative;
  display: block;
  padding-top: 20px;
  /* width: 50px; */
  margin: 0 auto;
  text-align: center;
  -webkit-transform-origin: 50% 250px; /*Change this when change size*/
  -ms-transform-origin: 50% 250px; /*Change this when change size*/
  transform-origin: 50% 250px;
} /*Change this when change size*/

.hc-luckywheel-item img {
  position: relative;
  top: -20px;
  left: 0px;
  width: 100px; /*Change this when change size*/
  height: 100px;
} /*Change this when change size*/

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

.hc-luckywheel-btn::after {
  position: absolute;
  display: block;
  content: '';
  left: 10px;
  top: -46px;
  width: 0;
  height: 0;
  overflow: hidden;
  border-width: 30px;
  border-style: solid;
  border-color: transparent;
  border-bottom-color: #e44025;
}

.hc-luckywheel-btn.disabled {
  pointer-events: none;
  background: #b07a7b;
  color: #ccc;
}

.hc-luckywheel-btn.disabled::after {
  border-bottom-color: #b07a7b;
}

body {
  margin: 0;
  padding: 0;
  height: 100vh;
  width: 100%;
}

// .bg {
//   background-image: url('../images/bg.png');
// }
</style>
