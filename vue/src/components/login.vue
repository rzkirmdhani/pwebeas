<template>
  <div class="container">
    <h1>Form Registrasi Lomba</h1>
    <form @submit.prevent="onSubmit">
      <div class="form-group">
        <label for="nama">Nama</label>
        <input type="text" class="form-control" id="nama" v-model="nama" placeholder="Masukkan nama lengkap Anda">
      </div>
      <div class="form-group">
        <label for="email">Email</label>
        <input type="email" class="form-control" id="email" v-model="email" placeholder="Masukkan alamat email Anda">
        <small class="form-text text-muted">Email harus unik</small>
      </div>
      <div class="form-group">
        <label for="asal-sekolah">Asal Sekolah</label>
        <input type="text" class="form-control" id="asal-sekolah" v-model="asal_sekolah" placeholder="Masukkan nama sekolah Anda">
      </div>
      <div class="form-group">
        <label for="status">Status</label>
        <select class="form-control" id="status" v-model="status">
          <option value="waiting">Menunggu</option>
          <option value="rejected">Ditolak</option>
          <option value="accepted">Diterima</option>
        </select>
      </div>
      <div class="form-group">
        <label for="tanggal-pendaftaran">Tanggal Pendaftaran</label>
        <input type="date" class="form-control" id="tanggal-pendaftaran" v-model="tanggal_pendaftaran">
      </div>
      <button type="submit" class="btn btn-primary">Daftar</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nama: '',
      email: '',
      asal_sekolah: '',
      status: 'waiting',
      tanggal_pendaftaran: new Date()
    }
  },
  methods: {
    onSubmit() {
      // Kirim data ke API
    }
  }
}
</script>

<style>
  .container {
    width: 500px;
    margin: 0 auto;
  }

  .form-group {
    margin-bottom: 1rem;
  }

  input {
    border: 1px solid #ccc;
    padding: .5rem;
  }

  button {
    width: 100%;
    margin-top: 1rem;
  }
</style>
