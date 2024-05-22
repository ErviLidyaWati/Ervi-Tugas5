<template>
    <footer class="footer">
      <p>&copy; 2024 Online Store. All rights reserved.</p>
    </footer>
  </template>
  
  <script>
  export default {
    name: 'Footer'
  }
  </script>
  
  <style>
  .footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 20px; /* Menambahkan ruang di sekitar teks */
    width: 100%;
    position: fixed; /* Membuat footer tetap di bagian bawah layar */
    bottom: 0; /* Menempatkan footer di bagian bawah */
    left: 0; /* Menyelaraskan footer ke kiri */
    right: 0; /* Menyelaraskan footer ke kanan */
  }
  
  .footer p {
    margin: 0; /* Menghilangkan margin bawaan */
  }
  
  /* Menambahkan efek hover */
  .footer p:hover {
    text-decoration: underline;
  }
  
  /* Efek transisi saat hover */
  .footer p {
    transition: color 0.3s ease;
  }
  </style>
  