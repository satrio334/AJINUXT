<template>
  <div>
    <h1>Detail Pesanan</h1>
    <table>
      <thead>
        <tr>
          <th>Barang</th>
          <th>Harga</th>
          <th>Jumlah</th>
          <th>Total</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(item, index) in cartItems" :key="index">
          <td>{{ item.namaBarang }}</td>
          <td>{{ item.harga }}</td>
          <td>{{ item.jumlah }}</td>
          <td>{{ item.harga * item.jumlah }}</td>
        </tr>
      </tbody>
    </table>
    <p>Total Harga: {{ totalHarga }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cartItems: [
        { namaBarang: 'Product 1', harga: 10000000, jumlah: 1 },
        { namaBarang: 'Product 2', harga: 1500000, jumlah: 1 },
        { namaBarang: 'Product 3', harga: 1200000, jumlah: 1 },
        // Tambahkan item pesanan Anda di sini
      ],
    };
  },
  computed: {
    totalHarga() {
      return this.cartItems.reduce((total, item) => total + item.harga * item.jumlah, 0);
    },
  },
};
</script>

<style scoped>
h1 {
  font-size: 24px;
  text-align: center;
  margin-bottom: 20px;
}

table {
  width: 100%;
  border-collapse: collapse;
}

table, th, td {
  border: 1px solid #0e1213;
}

th, td {
  padding: 10px;
  text-align: left;
}

th {
  background-color: #6cd4f0;
}

tr:hover {
  background-color: #fefbfb;
}

p {
  text-align: right;
  font-weight: bold;
  margin-top: 20px;
}

/* Gaya tambahan sesuai kebutuhan Anda */
</style>

