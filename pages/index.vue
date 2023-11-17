<template>
  <div class="landing-page">
    <header>
      <h1>Selamat Datang di Satria Aji Store</h1>
      <p>Web Penjualan Elektronik Terbaik</p>
    </header>
    <main>
      <section class="features">
        <div class="feature">
          <i class="fas fa-desktop"></i>
          <h2>Amanah</h2>
          <p>Tempat jual beli elektronik terpercaya</p>
        </div>
        <div class="feature">
          <i class="fas fa-cogs"></i>
          <h2>Mudah</h2>
          <p>mudah dalam melakukan pembelian tidak memerlukan syarat tambahan dan bebas ribet</p>
        </div>
        <div class="feature">
          <i class="fas fa-rocket"></i>
          <h2>Murah</h2>
          <p>Harga barang terjangkau untuk produk lama atau produk terbaru di toko kami </p>
        </div>
      </section>
    </main>
    <NuxtLink to="/product" class="text-base">
        <button @click="addToCart(product)">Lihat Produk</button>
        </NuxtLink>
  </div>
</template>

<script>
export default {
  name: 'LandingPage'
}
</script>

<style scoped>
/* Tambahkan kode CSS berikut untuk mengatur tampilan menarik */
.landing-page {
  text-align: center;
  background: url('images/iconss/Background.jpg') no-repeat center center fixed;
  background-size: cover;
  padding: 30px;
}

header {
  background: rgba(0, 0, 0, 0.5); /* Memberikan efek transparansi pada latar belakang header */
  color: white;
  padding: 20px;
}

header h1 {
  font-size: 2rem;
}

header p {
  font-size: 1.2rem;
}

.features {
  display: flex;
  justify-content: space-around;
  margin-top: 30px;
}

.feature {
  background: white;
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 5px;
  text-align: center;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.feature i {
  font-size: 3rem;
  margin-bottom: 10px;
}

.feature h2 {
  font-size: 1.5rem;
  margin: 10px 0;
}
</style>
