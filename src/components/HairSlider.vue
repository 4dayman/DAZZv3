<template>
    <Swiper class="swiper"
    :modules="modules"
    :slides-per-view="1"
    :space-between="50"
    loop
    autoplay
    @swiper="onSwiper"
    @slideChange="onSlideChange"
  >
        <SwiperSlide 
            v-for="image in images"
            :key="image.id"
        >
        <figure class="slide-bgimg">
            <img :src="image.url" />
        </figure>
        </SwiperSlide>
    </Swiper>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Navigation, Autoplay, Pagination, Scrollbar, A11y } from 'swiper';
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/autoplay';
export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    data() {
      return{
        images: [
          {id:1, url: require('@/assets/hairSlider/img_1.jpg')},
          {id:1, url: require('@/assets/hairSlider/img_2.jpg')},
          {id:1, url: require('@/assets/hairSlider/img_3.jpg')},
          {id:1, url: require('@/assets/hairSlider/img_4.jpg')},
          {id:1, url: require('@/assets/hairSlider/img_5.jpg')},
          {id:1, url: require('@/assets/hairSlider/img_6.jpg')},
          {id:1, url: require('@/assets/hairSlider/img_7.jpg')},
        ]
      }
    },
    setup() {
      const onSwiper = (swiper) => {
      };
      const onSlideChange = () => {
      };
      return {
        onSwiper,
        onSlideChange,
        modules: [Navigation, Autoplay, Pagination, Scrollbar, A11y],
      };
    },
}
</script>

<style lang="scss" scoped>
.swiper{
  z-index: 1;
}
.slide-bgimg{
    max-width: 100%;
    height: 60vh;
    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
}


</style>