<template>
  <div>
    <Navbar />
    <div class="container mt-4">
      <Carousel />
      <div class="card-container mt-4">
        <Card 
          v-for="product in products" 
          :key="product.id" 
          :title="product.name" 
          :description="product.description" 
          :url="product.url" 
        />
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Carousel from './components/Carousel.vue';
import Card from './components/Card.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Carousel,
    Card,
    Footer
  },
  data() {
    return {
      products: [
        { 
          id: 1, 
          name: 'Montres Dior VIII ', 
          description: 'Shop the 19 of the most stylish womens Watchs: Dior Montres VIII .', 
          url: 'https://i.pinimg.com/564x/e6/31/10/e631107e83487b73730e590117c0aa99.jpg' 
        },
        { 
          id: 2, 
          name: 'Rolex Oyster Perpetua', 
          description: 'As the quintessential wristwatch, the Oyster Perpetual carries Rolex’s founding legacy while following the movement of its era', 
          url: 'https://i.pinimg.com/564x/7c/cd/3c/7ccd3c2f10a1caa2be97502f6f6955af.jpg' 
        },
        { 
          id: 3, 
          name: 'Rolex Lady-Datejust', 
          description: 'The classic feminine watch. The Rolex Lady-Datejust in Oystersteel and yellow gold, 28 mm case, white dial, a Jubilee bracelet.', 
          url: 'https://i.pinimg.com/564x/de/62/1e/de621e5f86595fffe655766ad6d68803.jpg' 
        },
        { 
          id: 4, 
          name: 'Guccis Diamantissima ', 
          description: 'Gold-tone markers gleam from the mother-of-pearl dial on this fine black leather strap watch from Guccis Diamantissima collectionn', 
          url: 'https://i.pinimg.com/564x/0e/56/97/0e56978ac58124bdd14212281946232d.jpg' 
        },
        { 
          id: 5, 
          name: 'Oyster bracelet', 
          description: 'Time for inspiration. The Rolex Explorer in Oystersteel and yellow gold, 36 mm case, black dial, an Oyster bracelet.', 
          url: 'https://i.pinimg.com/564x/5f/b7/ca/5fb7cac8f60f655623e50350d3191fb9.jpg' 
        },
        { 
          id: 6, 
          name: 'Rolex Datejust', 
          description: ' The Rolex Datejust 36 in Oystersteel, white gold and diamonds, 36 mm case, pink set with diamonds dial, an Oyster bracelet.', 
          url: 'https://i.pinimg.com/564x/cb/3f/4f/cb3f4f958c983b90a65ec2218c60c933.jpg' 
        }
      ]
    };
  }
};
</script>

<style>
body {
  font-family: Arial, sans-serif; /* Ganti font agar lebih mudah dibaca */
  background-color: #fdf9ec; /* Warna latar belakang cream */
}

.container {
  max-width: 1200px; /* Batasi lebar konten agar lebih mudah dibaca */
  margin: 0 auto; /* Pusatkan konten */
  padding: 0 20px; /* Tambahkan padding agar konten tidak menempel ke tepi */
}

.card-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center; /* Pusatkan kartu-kartu */
  gap: 20px; /* Atur jarak antar kartu */
}

.card img {
  width: 100%;
  height: 100%; /* Atur tinggi gambar agar mengisi konten tanpa merubah rasio aspek */
  object-fit: cover; /* Memastikan gambar mengisi seluruh area tanpa terputus */
  border-radius: 10px 10px 0 0;
}

.card:hover {
  transform: translateY(-5px); /* Angkat kartu saat dihover */
}

.card {
  flex: 0 0 calc(30% - 20px);
  background-color: #fce9e1; /* Warna latar belakang kartu abu-abu */
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  transition: transform 0.3s ease;
  display: flex; /* Membuat kontainer kartu menjadi flexbox */
  flex-direction: column; /* Menetapkan arah tata letak flexbox ke vertikal */
}

.card-content {
  padding: 20px; /* Tambahkan padding ke konten kartu */
}

.card-title {
  font-size: 1.2rem; /* Ukuran judul yang lebih besar */
  margin-bottom: 10px; /* Spasi bawah antara judul dan deskripsi */
  color: #333; /* Warna teks judul abu-abu lebih gelap */
}

.card-description {
  color: #666; /* Warna deskripsi yang lebih gelap */
}

.buy-button {
  display: block;
  width: 100%;
  padding: 8px 16px;
  margin-top: 8px;
  font-family: "Arial", sans-serif;
  font-size: 16px;
  color: #fff;
  background-color: #51bef1; /* Warna biru */
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s ease; /* Efek transisi saat hover */
}

.buy-button:hover {
  background-color: #0056b3; /* Warna biru lebih gelap saat dihover */
}

@media (max-width: 768px) {
  .card {
    flex-basis: calc(50% - 20px); /* Ubah menjadi dua kolom pada layar kecil */
  }
}

@media (max-width: 576px) {
  .card {
    flex-basis: calc(100% - 20px); /* Ubah menjadi satu kolom pada layar sangat kecil */
  }
}

</style>

