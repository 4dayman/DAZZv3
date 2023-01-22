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
        <div class="content">
            <p class="title">{{image.title}}</p>
            <span class="desc">{{image.desc}}</span>
        </div>
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
          {id:1, title: '', desc: '', url: require('@/assets/mainSlider/img_1.jpg')},
          {id:2, title: 'hair', desc: 'Some description', url: require('@/assets/mainSlider/img_2.jpg')},
          {id:3, title: 'nails', desc: 'Some description', url: require('@/assets/mainSlider/img_3.jpg')},
          {id:4, title: 'make up', desc: 'Some description', url: require('@/assets/mainSlider/img_4.jpg')},
          {id:5, title: 'lash&brow', desc: 'Some description', url: require('@/assets/mainSlider/img_5.jpg')},
          {id:6, title: 'kids', desc: 'Some description', url: require('@/assets/mainSlider/img_6.jpg')},
          {id:7, title: 'cosmetology', desc: 'Some description', url: require('@/assets/mainSlider/img_7.jpg')},
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
    height: 70vh;
    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
}
.content{
    position:absolute;
    top:40%;
    left:0;
    width:50%;
    padding-left:5%;
    color:#fff;
    .title{
      font-size:2.6em;
      font-weight:bold;
      margin-bottom:30px;
      text-transform: uppercase;
    }
    .desc{
      display:block;
      font-size:13px;
      line-height:1.4;
      // transform:translateX(50px);
      opacity:1;
      transition:opacity .3s ease, transform .7s ease;
    }
  }

</style>