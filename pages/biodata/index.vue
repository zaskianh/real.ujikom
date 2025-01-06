<template>
  <div class="container mt-5">
    <div class="text-center mb-4">
      <h1 class="text-warning">Biodata</h1>
    </div>
    <div class="card shadow-sm">
      <div class="card-body">
        <!-- Informasi -->
        <h3 class="mb-3">Profil</h3>
        <div class="row mb-2">
          <div class="col-md-3 text-center">
            <img src="~/assets/biodata/zaskia.jpg" alt="" class="aisiti">
          </div>
          <div class="col-md-9">
            <ul class="list-group">
              <li class="list-group-item">ZASKIA NURUL HUDA</li>
              <li class="list-group-item">Jl.Kh.Tb.Abdullah Kp.Cimerak </li>
              <li class="list-group-item">08-06-2006</li>
              <li class="list-group-item">PEREMPUAN</li>
              <li class="list-group-item">ISLAM</li>
              <li class="list-group-item">(+62) 896-2741-0207</li>
            </ul>
          </div>
        </div>

        <!-- Pendidikan -->
        <h3 class="mb-3">Pendidikan</h3>
        <ul class="list-group mb-4">
          <li v-for="(education, index) in biodata.education" :key="index" class="list-group-item">
            {{ education }}
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      biodata: {// Ganti dengan URL foto asli
        name: '',
        place: '',
        birthdate: '',
        religion: '',
        address: '',
        email: '',
        phone: '',
        website: '',
        education: [
          '2013 - 2019 : MI CIMERAK ',
          '2019 - 2022 : SMP Negeri 17 Tasikmalaya',
          '2022 - 2025 : SMK Negeri 4 Tasikmalaya',
        ],
      }
    };
  }
};
</script>

<style>
  .container {
    max-width: 2000px;
    margin: 0 auto;
    font-family: Arial, sans-serif;
  }

  .text-warning {
    color: #ffcc00;
  }

  .card {
    border-radius: 10px;
    border: none;
  }

  .card-body {
    padding: 20px;
    background-color: #f8f9fa;
  }

  .aisiti {
    border-radius: 50%;
    max-width: 100%;
    height: auto;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }

  .list-group-item {
    border: none;
    padding: 10px 15px;
    background-color: transparent;
  }

  .list-group-item:nth-child(odd) {
    background-color: #f9f9f9;
  }

  .list-group-item:nth-child(even) {
    background-color: #ffffff;
  }

  h1, h3 {
    font-weight: bold;
  }

  ul {
    padding-left: 0;
  }

  .text-center {
    text-align: center;
  }
</style>