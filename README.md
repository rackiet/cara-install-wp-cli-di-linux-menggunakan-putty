# Panduan Instalasi WP-CLI Melalui PuTTY

WP-CLI adalah alat baris perintah yang berguna untuk mengelola situs WordPress. Ini memungkinkan Anda untuk melakukan berbagai tugas administratif dan pengembangan langsung dari baris perintah. Panduan ini akan menunjukkan cara menginstal WP-CLI pada server Linux Anda menggunakan PuTTY, sebuah klien SSH untuk Windows.

## Persyaratan

- Akses SSH ke server Linux.
- Hak akses sudo pada server tersebut.

## Langkah-langkah Instalasi

### 1. Masuk ke Server Linux Menggunakan PuTTY

Buka aplikasi PuTTY dan gunakan detail SSH Anda untuk masuk ke server Linux.

### 2. Perbarui Daftar Paket Sistem

Sebelum memulai, sangat penting untuk memastikan bahwa daftar paket pada sistem Anda sudah terbaru. Jalankan perintah berikut:

```
sudo apt update
```

### 3. Instal Dependensi yang Diperlukan

WP-CLI memerlukan beberapa paket untuk berjalan. Instal paket-paket tersebut dengan perintah:

```
sudo apt install curl php-cli php-mbstring git unzip
```

### 4. Unduh File Instalasi WP-CLI

Menggunakan `curl`, unduh file instalasi WP-CLI:

```
curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
```

### 5. Periksa File Instalasi

Setelah mengunduh, verifikasi bahwa file tersebut siap digunakan:

```
php wp-cli.phar --info
```

Jika berhasil, Anda akan melihat informasi tentang versi WP-CLI yang telah diinstal.

### 6. Ubah Izin File

Ubah izin file `wp-cli.phar` agar dapat dieksekusi:

```
chmod +x wp-cli.phar
```

### 7. Pindahkan ke Direktori Sistem

Untuk dapat menggunakan WP-CLI dari lokasi mana pun, pindahkan file ke direktori sistem:

```
sudo mv wp-cli.phar /usr/local/bin/wp
```

### 8. Verifikasi Instalasi

Terakhir, verifikasi bahwa WP-CLI telah terinstal dengan benar:

```
wp --info
```

Jika instalasi berhasil, Anda akan melihat informasi mengenai versi WP-CLI dan konfigurasi sistem.

## Kesimpulan

Sekarang Anda telah berhasil menginstal WP-CLI melalui PuTTY pada server Linux Anda. Gunakan perintah `wp` untuk mulai menjalankan berbagai perintah WP-CLI melalui sesi SSH.

Semoga panduan ini membantu Anda dalam menginstal dan mulai menggunakan WP-CLI. Selamat mencoba!
