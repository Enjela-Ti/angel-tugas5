<template>
    <q-footer class="footer">
      <div class="q-pa-md">
        <div class="row">
          <div class="col">
            <p>Kontak: +62-8124-5789-11</p>
            <p>Email: info@ayosewaonline.com</p>
            <q-icon name="mail" />
            <q-icon name="phone" />
          </div>
          <div class="col">
            <p>&copy; 2024 Ayo Sewa Online</p>
            <q-input class="input" filled placeholder="Kirim Feedback" />
            <q-btn label="Kirim" color="primary" />
          </div>
        </div>
      </div>
    </q-footer>
  </template>
  
  <script>
  export default {
    name: 'Footer'
  };
  </script>
  
  <style>
  .footer {
    background-color: #000;
    color: #fff;
    position: absolute;
    bottom: 0;
    width: 100%;
    z-index: 1000; 
  }
  
  .input {
    background-color: white;
    margin-bottom: 5px;
    width: 50%;
  }

  </style>
  