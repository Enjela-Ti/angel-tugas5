<template>
  <q-layout>
    <q-header elevated class="bg-green-8 text-white">
      <Navbar />
    </q-header>

    <q-page-container>
      <q-page class="bg-light page-content">
        <Carousel />
        <div class="q-pa-md">
          <div class="card-container">
            <Card v-for="hotel in hotels" :key="hotel.id" :hotel="hotel" />
          </div>
        </div>
      </q-page>
    </q-page-container>

    <Footer />
  </q-layout>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Carousel from './components/Carousel.vue';
import Card from './components/Card.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Carousel,
    Card,
    Footer
  },
  data() {
    return {
      hotels: [
        { id: 1, name: 'Hotel Pangeran Pekanbaru', price: 'Rp. 500,000', image: 'https://bzpublishassets.blob.core.windows.net/media/assets_big/new-pool-and-balcony-8.webp', description: 'Jl. Jend. Sudirman No.371-373, Cinta Raja, Kec. Sail, Kota Pekanbaru, Riau 28126' },
        { id: 2, name: 'PRIME PARK Hotel', price: 'Rp. 600,000', image: 'https://static.promediateknologi.id/crop/0x0:0x0/0x0/webp/photo/riaupos/276-5-prime-park.gif', description: 'Alamat: Jl. Jend. Sudirman No.3 Blok A, Simpang Tiga, Kec. Bukit Raya, Kota Pekanbaru, Riau 28284' },
        { id: 3, name: 'Ameera Hotel', price: 'Rp. 600,000', image: 'https://ik.imagekit.io/tvlk/apr-asset/dgXfoyh24ryQLRcGq00cIdKHRmotrWLNlvG-TxlcLxGkiDwaUSggleJNPRgIHCX6/hotel/asset/10006704-ce9df15f08d9889e32c4c078e689f77b.jpeg?_src=imagekit&tr=c-at_max,h-280,q-40,w-412', description: 'Jl.Pasar Kodim,Pekanbaru,Riau' },
        { id: 4, name: 'Grand Zuri Hotel Pekanbaru', price: 'Rp. 600,000', image: 'https://ik.imagekit.io/tvlk/apr-asset/Ixf4aptF5N2Qdfmh4fGGYhTN274kJXuNMkUAzpL5HuD9jzSxIGG5kZNhhHY-p7nw/hotel/asset/10000621-940c6009718dfdf68b1400aed6b894ae.jpeg?tr=q-40,c-at_max,w-740,h-500&_src=imagekit', description: 'Jl.Riau ,Pekanbaru, Riau' },
        { id: 5, name: 'Aryaduta Pekanbaru', price: 'Rp. 600,000', image: 'https://aryaduta-pekanbaru-hotel.hotelmix.id/data/Photos/OriginalPhoto/12839/1283944/1283944408/Aryaduta-Pekanbaru-Exterior.JPEG', description: 'Alamat: Jl. Diponegoro No.34, Simpang Empat, Kec. Pekanbaru Kota, Kota Pekanbaru, Riau 28113' },
        { id: 6, name: 'The Premiere Hotel Pekanbaru', price: 'Rp. 600,000', image: 'https://media-cdn.tripadvisor.com/media/photo-s/0d/42/0a/ef/logo-depannya.jpg', description: 'Alamat: Jl. Jend. Sudirman No.389, Simpang Empat, Kec. Pekanbaru Kota, Kota Pekanbaru, Riau 28121.' },
        { id: 7, name: 'Hotel Novotel Pekanbaru', price: 'Rp. 600,000', image: 'https://s-light.tiket.photos/t/01E25EBZS3W0FY9GTG6C42E1SE/t_htl-dskt/tix-hotel/images-web/2020/11/16/d43e6346-5ae4-4b5c-8d21-581d65301e6b-1605528213898-344cbf5d52ffb4369a92ca4e2e7c6ad7.jpg', description: 'Alamat: Jl. Riau No.59, Kp. Baru, Kec. Senapelan, Kota Pekanbaru, Riau 28154.' },
        { id: 8, name: 'Grand Jatra Hotel Pekanbaru', price: 'Rp. 600,000', image: 'https://lh3.googleusercontent.com/p/AF1QipNcOboOJzsPPsOtG2e1FfEz06eafZQe-nkao2ql=s1360-w1360-h1020', description: 'Berlokasi di: Mal Pekanbaru Alamat: Jl. Tengku Zainal Abidin No.1, Kota Tinggi, Kec. Pekanbaru Kota, Kota Pekanbaru, Riau 28116' }
      ]
    };
  }
};
</script>

<style>
.bg-light {
  background-color: #f5f5f5;
}

.page-content {
  padding-bottom: 100px; 
}

.card-container {
  display: flex;
  flex-wrap: wrap;
  gap: 1em;
  justify-content: space-around;
}
</style>
