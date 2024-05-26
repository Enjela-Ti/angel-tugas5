<template>
    <q-toolbar>
      <q-toolbar-title>
        Ayo Sewa Online
      </q-toolbar-title>
  
      <q-btn flat icon="menu" @click="toggleDrawer" />
      <q-drawer v-model="drawer" side="right" overlay>
        <q-list class="item">
          <q-item clickable v-ripple>
            <q-item-section>Home</q-item-section>
          </q-item>
          <q-item clickable v-ripple>
            <q-item-section>Riwayat Pemesanan</q-item-section>
          </q-item>
          <q-item clickable v-ripple>
            <q-item-section>Payment</q-item-section>
          </q-item>
          <q-item clickable v-ripple>
            <q-item-section>Setting</q-item-section>
          </q-item>
          <q-item clickable v-ripple>
            <q-item-section>Logout</q-item-section>
          </q-item>
        </q-list>
      </q-drawer>
    </q-toolbar>
  </template>
  
  <script>
  export default {
    data() {
      return {
        drawer: false
      };
    },
    methods: {
      toggleDrawer() {
        this.drawer = !this.drawer;
      }
    }
  };
  </script>
<style scoped>
.item{
    color: black;
}
</style>
  