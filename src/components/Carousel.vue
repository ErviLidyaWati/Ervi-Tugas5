<template>
    <div class="carousel">
      <div v-for="(image, index) in images" :key="index" class="carousel-item">
        <img :src="image.url" :alt="image.alt" class="carousel-image" />
        <div class="carousel-caption">
          <p>{{ image.caption }}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Carousel',
    data() {
      return {
        images: [
          { 
            url: 'https://i.pinimg.com/564x/3c/ac/f4/3cacf4c7f2cb8ffb85cc2671ff03f0aa.jpg', 
            alt: 'Rolex Cosmograph Daytona', 
            caption: 'Rolex Cosmograph Daytona' 
          },
          { 
            url: 'https://i.pinimg.com/564x/4e/1b/4f/4e1b4ff35ace3b9298b32d9d1c3270d1.jpg', 
            alt: 'Image 2', 
            caption: 'Rolex Lady-Datejust 28 in Everose Rolesor ' 
          },
          { 
            url: 'https://i.pinimg.com/564x/c4/3c/72/c43c72b67eb75d73af5d0d49675b3244.jpg', 
            alt: 'Image 3', 
            caption: 'Rhinestone Decor Quartz', 
          }
        ]
      }
    }
  }
  </script>
  
  <style>
  .carousel {
    display: flex;
    overflow-x: auto;
    scroll-snap-type: x mandatory;
    padding: 10px 0; /* Padding atas dan bawah */
    margin-bottom: 20px; /* Jarak bawah */
  }
  
  .carousel-item {
    scroll-snap-align: start;
    flex: none;
    width: 70%; /* Lebar item carousel */
    margin-right: 20px; /* Jarak antar item */
    border-radius: 12px; /* Sudut bulat */
    overflow: hidden; /* Mengatasi overflow */
    position: relative; /* Position relative untuk posisi absolut overlay */
  }
  
  .carousel-image {
    width: 100%; /* Lebar gambar */
    height: auto; /* Tinggi otomatis */
    object-fit: cover; /* Memastikan gambar mengisi seluruh area */
    border-radius: 12px 12px 0 0; /* Memberikan sudut bulat pada sudut atas */
    box-shadow: 0px 8px 16px rgba(0, 0, 0, 0.1); /* Efek bayangan untuk tampilan yang lebih menarik */
    transition: transform 0.3s ease; /* Efek transisi saat gambar dihover */
  }
  
  .carousel-caption {
    background-color: rgba(0, 0, 0, 0.7); /* Warna latar belakang semi-transparan */
    color: #fff; /* Warna teks */
    text-align: center; /* Tengah teks */
    padding: 10px; /* Ruang di sekitar teks */
    border-radius: 0 0 12px 12px; /* Memberikan sudut bulat pada sudut bawah */
    position: absolute; /* Position absolut untuk overlay teks */
    bottom: 0; /* Letakkan di bagian bawah gambar */
    left: 0; /* Menyelaraskan ke kiri */
    width: 100%; /* Lebar penuh */
    opacity: 0; /* Mulai dengan tidak terlihat */
    transform: translateY(100%); /* Geser ke bawah saat tidak terlihat */
    transition: transform 0.3s ease, opacity 0.3s ease; /* Efek transisi saat tampilan/hilang */
  }
  
  .carousel-item:hover .carousel-image {
    transform: scale(1.05); /* Memperbesar gambar saat dihover */
  }
  
  .carousel-item:hover .carousel-caption {
    opacity: 1; /* Tampilkan teks saat dihover */
    transform: translateY(0); /* Geser ke atas saat dihover */
  }
  </style>
  