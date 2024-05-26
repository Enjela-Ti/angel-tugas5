<template>
    <q-card class="my-card">
      <q-img :src="hotel.image" class="card-image">
        <q-card-section>
          <div class="text-h6">{{ hotel.name }}</div>
          <div>{{ hotel.price }}</div>
        </q-card-section>
      </q-img>
      <q-card-actions align="right">
        <q-btn flat @click="showDetail">Lihat Detail</q-btn>
      </q-card-actions>
    </q-card>
  </template>
  
  <script>
  import Swal from 'sweetalert2';
  import 'sweetalert2/src/sweetalert2.scss';
  
  export default {
    name: 'Card',
    props: {
      hotel: Object
    },
    methods: {
      showDetail() {
        Swal.fire({
          title: this.hotel.name,
          text: this.hotel.description,
          imageUrl: this.hotel.image,
          imageWidth: 400,
          imageHeight: 200,
          imageAlt: this.hotel.name,
          confirmButtonText: 'Beli',
          customClass: {
            container: 'swal2-custom-container'
          }
        });
      }
    }
  };
  </script>
  
  <style>
  .my-card {
    flex: 1 1 calc(25% - 1em);
    max-width: calc(25% - 1em);
    margin: 1em 0;
  }
  .card-image {
    height: 200px;
    object-fit: cover;
  }
  
  .swal2-custom-container {
    z-index: 1100;
  }
  </style>
  