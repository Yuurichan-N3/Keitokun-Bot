# 🌟 Keito Bot - Auto Airdrop Farmer

Script Node.js untuk mengotomatiskan tugas permainan dan farming airdrop di Keito. Dirancang untuk mengelola multiple akun dengan proxy support, logging visual, dan antarmuka CLI yang informatif.

---

## 🚀 Fitur Utama
- Mengotomatiskan permainan Keito (start/end game) dan klaim quest
- Dukungan multi-akun melalui `accounts.json`
- Penggunaan proxy opsional dari `proxy.txt`
- Logging aktivitas dengan tabel dan progress bar
- Pembaruan status game dan user secara real-time
- Penanganan error dan retry otomatis
- Gradient banner dan output berwarna menggunakan `gradient-string` dan `colors`

---

## 📋 Prasyarat
Sebelum memulai, pastikan Anda memiliki:
- Node.js (versi 16 atau lebih tinggi) terinstal
- NPM untuk mengelola dependensi
- File `accounts.json` dengan data akun
- File `proxy.txt` (opsional) untuk konfigurasi proxy

---

## 🛠️ Cara Instalasi
1. **Clone Repository**
   ```bash
   git clone https://github.com/Yuurichan-N3/Keitokun-Bot.git
   cd Keitokun-Bot
   ```

2. **Instal Dependensi**
   Jalankan perintah berikut untuk menginstal library yang dibutuhkan:
   ```bash
   npm install
   ```
   Dependensi yang akan diinstal:
   - `axios`
   - `colors`
   - `https-proxy-agent`
   - `cli-progress`
   - `cli-table3`
   - `gradient-string`

3. **Siapkan File `accounts.json`**
   - Buat file `accounts.json` di direktori yang sama dengan script
   - Format contoh:
     ```json
     [
       {
         "uid": "user123",
         "X_TOKEN": "your-token-here",
         "COOKIES": "your-cookies-here"
       },
       {
         "uid": "user456",
         "X_TOKEN": "another-token",
         "COOKIES": "another-cookies"
       }
     ]
     ```
   - Masukkan `uid`, `X_TOKEN`, dan `COOKIES` untuk setiap akun

4. **Siapkan File `proxy.txt` (Opsional)**
   - Buat file `proxy.txt` jika ingin menggunakan proxy
   - Format: satu proxy per baris, contoh:
     ```
     http://user:pass@host:port
     http://user2:pass2@host2:port2
     ```
   - Proxy akan diassign secara round-robin ke setiap akun

---

## ▶️ Cara Penggunaan
1. **Jalankan Script**
   Dari terminal, ketik:
   ```bash
   node bot.js
   ```

2. **Pantau Output**
   - Script akan menampilkan banner berwarna dan memulai bot untuk setiap akun
   - Aktivitas akan dilog dalam tabel dengan timestamp
   - Progress bar akan muncul saat menunggu drop berikutnya
   - Contoh output:
     ```
     Time          | Activity
     10:00:00      | Starting Keito Auto-Play Bot
     10:00:01      | Game started successfully
     Next Drop: [██████████] 100% | ETA: 0s
     ```

3. **Hentikan Jika Diperlukan**
   Tekan `Ctrl+C` untuk menghentikan eksekusi kapan saja

---

## 📂 Struktur File
- `index.js`: Script utama
- `accounts.json`: File input berisi data akun (harus dibuat manual)
- `proxy.txt`: File input berisi daftar proxy (opsional, harus dibuat manual)
- `README.md`: Dokumentasi ini

---

## ⚠️ Catatan Penting
- Pastikan koneksi internet stabil
- File `accounts.json` harus ada dan berisi minimal satu akun valid
- Proxy bersifat opsional; jika tidak ada `proxy.txt`, bot akan berjalan tanpa proxy
- Interval pengecekan game (60 detik) dan quest (5 menit) dapat diubah di config
- Bot akan retry otomatis jika terjadi error jaringan

---

## 📜 Lisensi
Script ini didistribusikan untuk keperluan pembelajaran dan pengujian. Penggunaan di luar tanggung jawab pengembang.

Untuk update terbaru, bergabunglah di grup **Telegram**: [Klik di sini](https://t.me/sentineldiscus).

---

## 💡 Disclaimer
Penggunaan bot ini sepenuhnya tanggung jawab pengguna. Kami tidak bertanggung jawab atas penyalahgunaan skrip ini.
