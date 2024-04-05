<template>
  <div class="background-container">
  <div id="app">
    <nav class="navbar">
      <a href="#home" class="nav-item">Home</a>
      <a href="#features" class="nav-item">Features</a>
      <a href="#pricing" class="nav-item">Pricing</a>
      <a href="#about" class="nav-item">About</a>
    </nav>
  </div>
  <br>
  <br>
  <br>
  <div id="app" class="container">
    <div class="profile">
      <!-- Tempatkan konten profil Anda di sini -->
      <img src="../src/assets/WhatsApp Image 2023-09-25 at 00.00.52.jpg" alt="Profil" class="profile-pic">
      <h3>Nama Anda</h3>
      <p>GILANG RAHMADANI</p>
      <!-- Tambahkan lebih banyak detail profil jika diperlukan -->
    </div>
    <div class="description">
      <!-- Tempatkan penjelasan tentang diri Anda di sini -->
      <h1>Tentang Saya</h1>
      <p>Saya adalah seorang mahasiswa teknik angkatan 22 yang berkuliah di Universitas Islam Riau, Fakultas Teknik, Prodi Informatika. 
        Kenapa saya memilih jurusan ini, karena saya ingin mempelajari tentang ilmu komputer lebih dalam lagi dan juga menurut saya jurusan Informatika mempunyai bidang pekerjaan yang luas. Saya lulusan dari SMK Taruna Satria Pekanbaru.</p>
      <!-- Tambahkan lebih banyak paragraf atau poin jika diperlukan -->
    </div>
  </div>
  <div id="app">
    <h1>Hobi Saya</h1>
    <div class="hobby-container">
      <div v-for="(hobby, index) in hobbies" :key="index" class="hobby-item">
        <h2>{{ hobby.name }}</h2>
        <p>{{ hobby.description }}</p>
      </div>
    </div>
  </div>
  <footer class="footer">
    <p>&copy; 2024 Hak Cipta dilindungi. Dibuat oleh gilangrahmadani.</p>
  </footer>
</div>
</template>

<script>
export default {
  name: 'HobbyPage',
  data() {
    return {
      hobbies: [
        { name: 'OLAHRAGA', description: 'Saya suka berolahraga, karena dapat menghilangkan stress dan juga menyehatkan tubuh.' },
        { name: 'MAIN GAME', description: 'Bermain game menurut saya itu tergantung diri masing-masing. Karena saya lumayan suka bermain game dengan teman saya untuk sekedar menghibur diri.' },
        // Tambahkan hobi lainnya di sini
      ]
    };
  }
}

</script>

<style>
.background-container {
  /* Atau untuk latar belakang gambar */
  background-image: url('../src/assets/logo2.jpg'); /* Ganti dengan link gambar Anda */
  background-size: cover; /* Pastikan gambar menutupi seluruh halaman */
  background-repeat: no-repeat; /* Jangan ulangi gambar */
  background-position: center; /* Pusatkan gambar */
}
.footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 10px 0;
}
.hobby-container {
  display: flex;
  flex-direction: column;
  align-items: center; /* Menyelaraskan item ke tengah secara horizontal */
}

.hobby-item {
  margin-bottom: 20px;
  text-align: center; /* Menyelaraskan teks ke tengah */
}


/* Tambahkan lebih banyak gaya sesuai kebutuhan */
.container {
  display: flex;
  align-items: center; /* Menyelaraskan item secara vertikal */
}
#app > h1 {
  text-align: center; /* Menyelaraskan teks ke tengah secara horizontal */
}
.profile {
  display: flex; /* Menggunakan flexbox */
  flex-direction: column; /* Menyusun item secara vertikal */
  align-items: center; /* Menyelaraskan item ke tengah secara horizontal */
  width: 25%;
  padding-right: 20px;
}

.profile-pic {
  width: 80%;
  border-radius: 50%;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  margin-bottom: 10px; /* Menambahkan ruang di bawah gambar */
}

.profile-name, .profile-description {
  text-align: center; /* Menyelaraskan teks ke tengah */
  width: 100%; /* Memastikan teks memenuhi lebar container */
}

.description {
  width: 70%; /* Menyesuaikan lebar deskripsi */
  padding-left: 20px; /* Menambahkan padding di sisi kiri */
}

.navbar {
  overflow: hidden;
  background-color: #333;
  display: flex;
  justify-content: space-around;
}

.nav-item {
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

.nav-item:hover {
  background-color: #ddd;
  color: black;
}
</style>
