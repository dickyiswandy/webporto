<template>
   <div class="full-background">
 <nav class="navbar">
    <!-- Navbar sebagai kontainer utama -->
    <div class="nav-brand">Welcome To My Portofolio</div>
    <!-- Ganti dengan nama brand atau logo Anda -->
    <ul class="nav-links">
      <!-- List untuk navigasi link -->
      <li v-for="link in links" :key="link" class="nav-item">
        <!-- Menggunakan v-for untuk menampilkan link -->
        <a href="#" class="nav-link">{{ link }}</a>
        <!-- Tampilkan nama link -->
      </li>
    </ul>
  </nav>
  <div class="container">
    <!-- Kontainer utama untuk halaman profil -->
    <div class="profile">
      <!-- Bagian deskripsi -->
      <div class="description">
        <h1>{{ nama }}</h1>
        <!-- Nama Anda -->
        <p>{{ deskripsiSingkat }}</p>
        <!-- Deskripsi singkat tentang diri Anda -->
        <h2>Pengalaman</h2>
        <p>{{ pengalaman }}</p>
        <!-- Penjelasan pengalaman Anda -->
        <h2>Hobby</h2>
        <!-- Bagian hobi pertama dengan gambar dan penjelasan -->
        <div class="hobi-section">
          <h3>{{ judulHobi1 }}</h3>
          <!-- Judul hobi pertama -->
          <img :src="hobiImageUrl1" alt="Gambar Hobi 1" class="hobi-image">
          <!-- Gambar hobi pertama akan ditampilkan di sini -->
          <p>{{ penjelasanHobi1 }}</p>
          <!-- Penjelasan hobi pertama di bawah gambar -->
        </div>
        <!-- Bagian hobi kedua dengan gambar dan penjelasan -->
        <div class="hobi-section">
          <h3>{{ judulHobi2 }}</h3>
          <!-- Judul hobi kedua -->
          <img :src="hobiImageUrl2" alt="Gambar Hobi 2" class="hobi-image">
          <!-- Gambar hobi kedua akan ditampilkan di sini -->
          <p>{{ penjelasanHobi2 }}</p>
          <!-- Penjelasan hobi kedua di bawah gambar -->
        </div>
      </div>
      <!-- Bagian gambar -->
      <div class="profile-image">
        <img :src="profileImageUrl" alt="Gambar Profil">
        <!-- Gambar profil akan ditampilkan di sini -->
      </div>
    </div>
  </div>
  <footer class="footer">
    <p>© 2024 Hak Cipta Dilindungi. Didesain oleh <strong>DickyIswandy</strong>.</p>
    <p>Ikuti kami di media sosial:</p>
    <ul>
      <li><a href="#">Facebook</a></li>
      <li><a href="#">Twitter</a></li>
      <li><a href="#">Instagram</a></li>
    </ul>
  </footer>

</div>
</template>

<script>
// Impor gambar dari folder 'assets'
import ProfileImage from '@/assets/fotosaya.png';
import HobiImage1 from '@/assets/valorant.png';
import HobiImage2 from '@/assets/badminton.png';

export default {
  data() {
    return {
      links: ['Home', 'About', 'Portfolio', 'Contact'],
      // Properti lainnya...
      nama: 'DICKY ISWANDY',
      deskripsiSingkat: 'Perkenalkan nama saya Dicky Iswandy, saya adalah mahasiswa semester 4 di Univeristas Islam Riau, jurusan teknik informatika. Saya tertarik dengan bidang ini karena menawarkan peluang yang luas dalam pemrograman komputer, pengembangan perangkat lunak, analisis keamanan informasi, analisis data, perancangan dan pemeliharaan database, hingga konsultan IT. Selain itu, saya juga merasa bahwa teknik informatika itu mengagumkan dan menyenangkan karena berhubungan dengan komputer, kode, perangkat lunak logika, perangkat keras, dan segala sesuatu yang berhubungan dengan teknologi',
      pengalaman: 'Selama masa sekolah menengah saya, saya aktif berpartisipasi dalam kegiatan Pramuka, sebuah organisasi yang memiliki misi untuk mengembangkan karakter, kepemimpinan, dan keterampilan siswa. Menjadi bagian dari Pramuka telah memberikan saya pengalaman yang berharga dalam hal kerjasama tim, kemandirian, dan ketahanan mental..',
      hobList: ['Hobi 1', 'Hobi 2', 'Hobi 3'],
      profileImageUrl: ProfileImage, // Gunakan gambar yang telah diimpor
      hobiImageUrl1: HobiImage1,
      hobiImageUrl2: HobiImage2,
      
    };
  },
  methods: {
    setActive(link) {
      this.activeLink = link;
    }
  }
};
</script>




<style scoped>
  .footer {
  background-color: #808080; /* Warna abu-abu */
  padding: 20px 0;
  font-family: 'Arial', sans-serif;
  color: #333;
  text-align: center;
  border-top: 4px solid #ff4500;
}

  .footer p {
    margin: 0;
  }

  .footer ul {
    list-style: none;
    padding: 0;
    display: flex;
    justify-content: center;
  }

  .footer ul li {
    display: inline;
    margin: 0 10px;
  }

  .footer a {
    text-decoration: none;
    color: #ff4500;
    transition: color 0.3s ease;
  }

  .footer a:hover {
    color: #333;
  }

.full-background {
  background-image: url('~@/assets/xx.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  height: vh; /* Atur tinggi div agar sesuai dengan tinggi viewport */
  width: 100vw; /* Atur lebar div agar sesuai dengan lebar viewport */
}
/* Style untuk kontainer hobi */
.hobi-section {
  background-color: #f9f9f9; /* Warna latar belakang */
  border-radius: 10px; /* Sudut bulat */
  padding: 20px; /* Padding di dalam kontainer */
  margin-bottom: 20px; /* Jarak antar kontainer hobi */
  box-shadow: 0 1px 3px rgba(0,0,0,0.2); /* Bayangan kotak yang lebih kecil */
  transition: transform 0.3s ease, box-shadow 0.3s ease; /* Transisi untuk animasi */
}

/* Style untuk judul hobi */
.hobi-section h3 {
  color: #f9f7f7f5; /* Warna teks */
  margin-bottom: 15px; /* Jarak antara judul dan gambar */
}

/* Style untuk gambar hobi */
.hobi-image {
  width: 100px; /* Lebar gambar yang ditentukan */
  height: auto; /* Tinggi gambar otomatis */
  border-radius: 5px; /* Sudut bulat untuk gambar */
}


/* Style untuk kontainer hobi */
.hobi-section {
  background-color: #f9f9f9; /* Warna latar belakang */
  border-radius: 10px; /* Sudut bulat */
  padding: 10px; /* Padding di dalam kontainer yang lebih kecil */
  margin-bottom: 20px; /* Jarak antar kontainer hobi */
  box-shadow: 0 1px 3px rgba(0,0,0,0.2); /* Bayangan kotak yang lebih kecil */
  transition: transform 0.3s ease, box-shadow 0.3s ease; /* Transisi untuk animasi */
  width: 50%; /* Lebar kontainer yang ditentukan */
}

/* Efek hover untuk kontainer hobi */
.hobi-section:hover {
  transform: translateY(-5px); /* Mengangkat kontainer sedikit ke atas */
  box-shadow: 0 2px 6px rgba(0,0,0,0.3); /* Bayangan kotak yang lebih besar saat hover */
}

.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.profile {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 95%;
  height: 85%;
  /* Sesuaikan lebar kontainer profil */
}

.description {
  width: 50%;
  height: 120%;
  /* Sesuaikan lebar bagian deskripsi */
  color: white; /* Set the color to white */
}


.profile-image {
  width: 40%; /* Lebar bagian gambar sesuai dengan 50% dari kontainer induk */
  align-self: flex-start; /* Menambahkan ini akan menaikkan gambar ke atas */
  display: inline-block; /* Ubah display untuk menerapkan animasi */

  position: relative; /* Menetapkan posisi relatif untuk pseudo-element */
}
 
@keyframes shadow-pulse {
  0% {
    box-shadow: 0 0 0 0 rgba(0, 0, 0, 0.2);
  }
  100% {
    box-shadow: 0 0 10px 10px rgba(0, 0, 0, 0.2);
  }
}
.profile-image img {
  position: absolute; /* Posisi absolut relatif terhadap induknya */
  top: 0;
  left: 0;
  width: 500px; /* Lebar gambar sesuai dengan kontainer induk */
  height: 500px; /* Tinggi gambar sesuai dengan kontainer induk */
  border-radius: 50%; /* Membuat gambar menjadi bulat */
  object-fit: cover; /* Pastikan gambar menutupi area tanpa distorsi */
}
.profile-image::before {
  content: '';
  display: block;
  padding-top: 100%; /* Aspek rasio 1:1 untuk mempertahankan bentuk bulat */
}
  

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #333;
  color: white;
  padding: 0 20px;
}

.nav-brand {
  font-size: 1.5em;
  font-weight: bold;
}

.nav-links {
  list-style: none;
  display: flex;
}

.nav-item {
  margin-left: 20px;
}

.nav-link {
  text-decoration: none;
  color: white;
  transition: color 0.3s ease;
}

.nav-link:hover {
  color: #f0db4f;
}
</style>
