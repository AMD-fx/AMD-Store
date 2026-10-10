# AMD Store

Website toko digital responsif untuk brand **AMD Store**, dengan katalog preset, aset, dan font serta alur pemesanan melalui WhatsApp.

## Fitur

- Tampilan responsif untuk HP dan desktop.
- Kategori produk: Preset, Aset, dan Font.
- Pencarian produk, keranjang, jumlah produk, dan total sementara.
- Checkout membuat pesan pesanan terformat dan membuka WhatsApp admin.
- Menu **Ples** di navigasi bawah membuka halaman **Isi Saldo** dan mengirim permintaan isi saldo ke WhatsApp.
- Halaman histori lokal, pusat bantuan, dan akun sederhana.
- Tidak ada pembayaran otomatis di website. Admin dan pembeli mengonfirmasi metode pembayaran melalui WhatsApp.

## Sebelum website dipublikasikan

Buka `index.html` dan temukan bagian `const STORE` di dekat bagian akhir file.

### 1. Atur nomor WhatsApp admin

Ganti:

```js
whatsappNumber: "628xxxxxxxxxx",
```

dengan nomor WhatsApp admin yang benar dalam format internasional tanpa tanda plus, spasi, atau strip. Contoh format: `6281234567890`.

### 2. Ganti produk contoh dengan produk AMD milikmu

Edit array `products` di bagian `STORE`. Setiap produk berisi:

```js
{id:"preset-01", name:"Nama Produk", category:"preset", price:15000,
 description:"Deskripsi produk", art:"PRESET"}
```

- `id`: ID unik untuk produk.
- `name`: nama produk yang tampil di toko.
- `category`: gunakan `preset`, `aset`, atau `font`.
- `price`: harga dalam rupiah sebagai angka.
- `description`: deskripsi singkat produk.
- `art`: teks dekoratif pada gambar produk.

Produk yang saat ini ditampilkan adalah **contoh/demo**, bukan daftar produk asli. Katalog sengaja dikosongkan sampai kamu memberikan daftar produk asli. Tambahkan nama, harga, deskripsi, kategori, dan materi produk milik AMD sebelum menerima pesanan sungguhan. Untuk memakai foto produk asli, bagian gambar kartu produk dapat disesuaikan untuk memuat URL atau file gambar.

### 3. Publikasikan dengan GitHub Pages

1. Buka **Settings** pada repositori GitHub.
2. Masuk ke **Pages**.
3. Pada bagian **Build and deployment**, pilih **GitHub Actions** sebagai source.
4. Simpan pengaturan. File workflow `.github/workflows/pages.yml` sudah ditambahkan untuk membangun dan menerbitkan situs setiap ada push ke branch `main`.
5. Buka tab **Actions** untuk memeriksa status deployment. Setelah berhasil, buka URL GitHub Pages yang ditampilkan di **Settings → Pages**.

## Catatan

- Keranjang hanya berada di memori browser; histori dan nama tersimpan lokal pada browser perangkat itu saja.
- Website ini belum memiliki backend, akun pengguna sungguhan, stok tersinkron, dashboard admin, atau histori lintas perangkat.
- WhatsApp checkout hanya menyiapkan pesan. Pesan belum terkirim sampai pembeli menekan tombol kirim di WhatsApp.
- Jangan mengklaim pembayaran berhasil sebelum admin memeriksa dan mengonfirmasinya.
