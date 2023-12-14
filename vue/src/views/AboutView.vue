<template>
  <div>
    <h2>Cek Status Pendaftaran</h2>
    <form @submit.prevent="checkStatus">
      <label for="email">Email:</label>
      <input type="email" id="email" v-model="inputEmail" required />
      <button type="submit">Cek Status</button>
    </form>

    <div v-if="status !== null">
      <p>Status Pendaftaran: {{ status }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputEmail: '',
      status: null,
    };
  },
  methods: {
    checkStatus() {
      if (this.inputEmail === 'john.doe@example.com') {
        this.status = 'Pendaftaran Berhasil';
      } else {
        this.status = 'Belum Terdaftar';
      }
    },
  },
};
</script>

<style scoped>

</style>
