# 🕌 Life OS — PWA Installation Guide
## Step-by-Step Cara Menggunakan sebagai Aplikasi

---

## 📁 File yang Disediakan

```
LifeOS_PWA/
├── index.html      ← Aplikasi utama
├── manifest.json   ← Konfigurasi PWA
├── sw.js           ← Service Worker (offline support)
├── icon-192.png    ← Ikon aplikasi (192x192)
├── icon-512.png    ← Ikon aplikasi (512x512)
└── README.md       ← Panduan ini
```

---

## 🚀 Cara Menggunakan

### Opsi A: Langsung dari File (Paling Mudah)

1. **Extract** file ZIP yang didownload
2. **Buka** `index.html` langsung di browser (Chrome/Edge/Firefox/Safari)
3. Aplikasi langsung berjalan!

> ⚠️ Catatan: Dengan cara ini PWA (install sebagai app) tidak bisa aktif karena butuh HTTPS. Tapi aplikasi tetap berfungsi penuh.

---

### Opsi B: Install sebagai Aplikasi di HP (Recommended)

Agar bisa di-install seperti aplikasi native, file perlu di-host di server HTTPS. Ada beberapa cara gratis:

#### Cara 1: Menggunakan GitHub Pages (GRATIS, Permanent)

1. **Buat akun GitHub** di https://github.com (jika belum punya)

2. **Buat repository baru:**
   - Klik "New Repository"
   - Nama: `life-os` (atau terserah)
   - Pilih **Public**
   - Klik "Create Repository"

3. **Upload semua file:**
   - Klik "Upload files"
   - Drag & drop SEMUA 5 file (index.html, manifest.json, sw.js, icon-192.png, icon-512.png)
   - Klik "Commit changes"

4. **Aktifkan GitHub Pages:**
   - Masuk ke **Settings** → **Pages**
   - Source: pilih **main** branch
   - Folder: **/ (root)**
   - Klik **Save**
   - Tunggu 1-2 menit

5. **Akses aplikasi:**
   - URL-nya akan menjadi: `https://[username].github.io/life-os/`
   - Buka URL ini di HP

6. **Install sebagai app di HP:**
   - **Android (Chrome):** Buka URL → ketuk titik tiga (⋮) → "Add to Home Screen" atau "Install App"
   - **iPhone (Safari):** Buka URL → ketuk tombol Share (□↑) → "Add to Home Screen"
   - Aplikasi akan muncul di home screen seperti app biasa!

#### Cara 2: Menggunakan Netlify (GRATIS, Drag & Drop)

1. Buka https://app.netlify.com
2. Daftar/login (bisa pakai akun Google)
3. Di dashboard, **drag & drop folder** yang berisi semua file
4. Tunggu deploy selesai (±30 detik)
5. Dapat URL seperti `https://random-name.netlify.app`
6. Buka di HP → Install ke home screen

#### Cara 3: Menggunakan Vercel (GRATIS)

1. Buka https://vercel.com
2. Daftar/login
3. Klik "Add New" → "Project"
4. Upload folder atau connect ke GitHub repo
5. Deploy otomatis
6. Buka URL di HP → Install

---

### Opsi C: Jalankan Server Lokal di Komputer

Jika hanya ingin test PWA di komputer/HP dalam jaringan yang sama:

#### Menggunakan Python (sudah terinstall di Mac/Linux):
```bash
# Buka terminal, masuk ke folder file
cd /path/to/LifeOS_PWA

# Jalankan server
python3 -m http.server 8080

# Buka di browser: http://localhost:8080
# Dari HP di WiFi yang sama: http://[IP-komputer]:8080
```

#### Menggunakan Node.js:
```bash
npx serve .
```

#### Menggunakan VS Code:
- Install extension "Live Server"
- Klik kanan index.html → "Open with Live Server"

---

## 📱 Setelah Install di HP

- Aplikasi berjalan **fullscreen** seperti app native
- Semua data tersimpan di browser (localStorage + IndexedDB)
- **Bisa digunakan offline** setelah pertama kali dibuka
- Export backup secara berkala untuk keamanan data!

---

## 💾 Backup & Restore

- **Export:** Settings → Export Backup → file JSON tersimpan
- **Import:** Settings → Import Backup → pilih file JSON
- Lakukan backup rutin karena data tersimpan di browser!
- Jika clear browser data, data aplikasi akan hilang (kecuali ada backup)

---

## 📖 Download Al-Quran Offline

1. Pastikan ada koneksi internet
2. Buka Settings → "Download Al-Quran Lengkap"
3. Klik "Download Sekarang"
4. Tunggu hingga 6.236 ayat selesai diunduh
5. Setelah itu, ayat Quran bisa tampil offline di Morning Salam

---

## ❓ FAQ

**Q: Apakah data saya aman?**
A: Data tersimpan lokal di browser kamu. Tidak ada yang dikirim ke server manapun.

**Q: Bagaimana jika saya ganti HP?**
A: Export backup di HP lama → Transfer file JSON → Import di HP baru.

**Q: Kenapa tidak bisa install di HP langsung dari file?**
A: Browser membutuhkan HTTPS untuk mengaktifkan PWA. Gunakan GitHub Pages (gratis) untuk mendapatkan HTTPS.

**Q: Berapa ukuran aplikasi?**
A: File HTML sekitar 215KB. Dengan data Quran lengkap, total storage sekitar 5-8MB.
