<template>
    <q-carousel
      v-model="slide"
      animated
      autoplay
      autoplay-interval="3000"
      infinite
    >
      <q-carousel-slide
        v-for="(image, index) in images"
        :key="index"
        :name="index"
        :img-src="image"
      />
    </q-carousel>
  </template>
  
  <script>
  export default {
    data() {
      return {
        slide: 0,
        images: [
          'https://img.okezone.com/content/2023/08/16/406/2865667/promo-hotel-mulai-dari-rp100-ribu-aja-di-mister-aladin-yuk-liburan-SGK0c47knd.jpg',
          'https://bankmega.com/media/filer_public/1f/8c/1f8c9a62-fd2a-43cb-afba-c0e6de07e5e5/0-banner-bm-new-intercontinental.jpg',
          'https://img.hotelmurah.com/promo/mobile16100429972.png'
        ]
      };
    }
  };
  </script>
  