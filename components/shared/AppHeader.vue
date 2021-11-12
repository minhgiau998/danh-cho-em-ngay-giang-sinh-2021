<template>
  <header class="relative w-screen h-screen bg-green-600">
    <div class="text-3xl font-bold text-gray-300">
      <div class="absolute left-10 top-10">
        <div class="w-10 h-2 mb-2 bg-gray-300 rounded-md"></div>
        <p>MERRY</p>
        <p>CHRISTMAS</p>
      </div>
      <div class="absolute left-10 bottom-10">
        <p>FEEL IT</p>
      </div>
    </div>

    <swiper
      style="
        transform: translate(-50%, -50%);
        height: calc(100vh - 100px);
        position: absolute;
      "
      class="w-1/3 bg-gray-300 rounded-lg top-2/4 left-2/4"
      ref="mySwiper"
      :options="swiperOptions"
    >
      <swiper-slide v-for="card in cards" :key="card">
        <img
          style="height: calc(100vh - 100px)"
          class="object-cover object-center w-full"
          :src="require(`~/assets/images/${card}`)"
          alt=""
        />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
    <div class="text-3xl font-bold text-gray-300">
      <div class="absolute right-10 top-10">
        <p>0000000</p>
      </div>
      <div class="absolute right-10 bottom-10">
        <p>RICH</p>
      </div>
    </div>
  </header>
</template>

<script>
import { Swiper, SwiperSlide, directive } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'

export default {
  name: 'app-header',
  components: {
    Swiper,
    SwiperSlide,
  },
  directives: {
    swiper: directive,
  },
  data() {
    return {
      swiperOptions: {
        pagination: {
          el: '.swiper-pagination',
          dynamicBullets: true,
        },
        loop: true,
        grabCursor: true,
        autoplay: {
          delay: 5000,
          disableOnInteraction: false,
        },
        // Some Swiper option/callback...
      },
      cards: [
        'holiday-card-01.png',
        'holiday-card-02.png',
        'holiday-card-03.png',
        'holiday-card-04.png',
        'holiday-card-05.png',
        'holiday-card-06.png',
        'holiday-card-07.png',
        'holiday-card-08.png',
        'holiday-card-09.png',
        'holiday-card-10.png',
        'holiday-card-11.png',
        'holiday-card-12.png',
      ],
    }
  },
  computed: {
    swiper() {
      return this.$refs.mySwiper.$swiper
    },
  },
  mounted() {
    console.log('Current Swiper instance object', this.swiper)
    this.swiper.slideTo(3, 1000, false)
  },
}
</script>

<style lang="css" scoped>
.swiper-pagination >>> .swiper-pagination-bullet {
  opacity: 1;
  border: #059669 solid 1px;
  background-color: transparent;
}

.swiper-pagination >>> .swiper-pagination-bullet-active {
  background-color: #059669;
}
</style>
