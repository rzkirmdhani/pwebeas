<template>
    <div>
      <h2>Form Registrasi Lomba</h2>
      <form @submit.prevent="submitForm">
        <div>
          <label for="nama">Nama:</label>
          <input type="text" id="nama" v-model="formData.nama" required />
        </div>
        <div>
          <label for="email">Email:</label>
          <input type="email" id="email" v-model="formData.email" required />
        </div>
        <div>
          <label for="asalSekolah">Asal Sekolah:</label>
          <input type="text" id="asalSekolah" v-model="formData.asalSekolah" required />
        </div>
        <button type="submit">Daftar</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        formData: {
          nama: '',
          email: '',
          asalSekolah: '',
        },
      };
    },
    methods: {
      submitForm() {
        
        console.log('Data yang dikirim:', this.formData);
        
        this.formData = {
          nama: '',
          email: '',
          asalSekolah: '',
        };
      },
    },
  };
  </script>
  
  <style scoped>
  </style>
  