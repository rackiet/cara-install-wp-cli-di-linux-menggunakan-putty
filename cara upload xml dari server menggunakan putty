# Tutorial Upload Artikel Menggunakan XML di WordPress Melalui PuTTY

Tutorial ini akan membimbing Anda melalui proses upload artikel ke situs WordPress Anda menggunakan file XML melalui sesi SSH di PuTTY. Ini sangat berguna ketika Anda ingin memindahkan konten antar situs atau melakukan import besar-besaran.

## Persiapan

Pastikan Anda telah menginstal WP-CLI pada server Anda dan memiliki akses SSH ke server tersebut. Jika belum, silakan ikuti panduan instalasi WP-CLI terlebih dahulu.

## Langkah-langkah

### 1. Mulai Sesi PuTTY

Buka PuTTY dan masuk ke server Anda menggunakan detail SSH yang telah disiapkan.

### 2. Gunakan Screen

Untuk memastikan proses berjalan di latar belakang dan tidak terputus jika sesi SSH terputus, gunakan `screen`. Ketik perintah berikut:

```
screen -S upload_artikel
```

Ini akan membuat sesi screen baru dengan nama "upload_artikel". Anda dapat menggunakan nama sesi lain yang Anda inginkan.

### 3. Navigasi ke Folder Penyimpanan File XML

Sesuaikan direktori kerja ke lokasi dimana file XML yang berisi artikel tersimpan. Misalnya:

```
cd /www/wwwroot/namadomainanda.com
```

Ganti `namadomainanda.com` dengan nama domain Anda dan sesuaikan lokasi penyimpanan sesuai kebutuhan.

### 4. Upload Artikel Menggunakan WP-CLI

Gunakan perintah berikut untuk memulai proses import artikel dari file XML:

```
wp import "/www/wwwroot/namadomainanda.com/artikelnya/output.xml" --authors=create --skip=attachment --allow-root
```

Pastikan Anda mengganti `/www/wwwroot/namadomainanda.com/artikelnya/output.xml` dengan path aktual ke file XML Anda.

### 5. Memantau Proses

Jika Anda melihat banyak teks berjalan di layar, itu menandakan proses import sedang berlangsung.

### 6. Menyembunyikan Sesi Screen

Setelah proses import dimulai, Anda bisa menyembunyikan sesi screen untuk menjalankan proses di latar belakang. Tekan `CTRL+A` diikuti dengan `CTRL+D` untuk melakukan ini.

### 7. Cek Berkala pada Bagian Post WordPress

Setelah beberapa waktu, cek situs WordPress Anda untuk melihat apakah artikel telah berhasil diupload. Anda bisa melihatnya di bagian posts dari dashboard WordPress.

## Kesimpulan

Dengan mengikuti langkah-langkah di atas, Anda dapat dengan mudah mengupload artikel ke situs WordPress Anda menggunakan file XML melalui PuTTY. Proses ini memudahkan pengelolaan situs WordPress Anda, terutama saat melakukan import konten dalam jumlah besar.

Semoga tutorial ini bermanfaat. Selamat mencoba!
