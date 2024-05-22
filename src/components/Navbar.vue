<template>
  <nav class="navbar">
    <div class="logo">RV WATCH'S</div>
    <ul class="nav-links">
      <li><a href="#home">Home</a></li>
      <li><a href="#products">Products</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Navbar'
}
</script>

<style>

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center; /* Rata tengah secara vertikal */
  background-color: #ffe3d4; /* Ubah warna latar belakang menjadi cream */
  padding: 10px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* Tambahkan efek bayangan yang halus */
  transition: background-color 0.3s ease; /* Tambahkan efek transisi saat warna berubah */
}

.logo {
  color: #333; /* Ubah warna teks logo menjadi lebih gelap */
  font-size: 24px;
  font-family: 'Broadway';
  transition: color 0.3s ease; /* Tambahkan efek transisi saat warna berubah */
}

.nav-links {
  list-style: none;
  display: flex;
}

.nav-links li {
  margin: 0 10px;
}

.nav-links a {
  color: #333; /* Ubah warna teks link menjadi lebih gelap */
  text-decoration: none;
  transition: color 0.3s ease; /* Tambahkan efek transisi saat warna berubah */
}

.nav-links a:hover {
  color: #1dc7e1; /* Ubah warna teks link menjadi warna navbar saat dihover */
}


</style>
