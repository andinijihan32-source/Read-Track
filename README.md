# 📚 Read Track

Platform literasi interaktif berbasis AI untuk siswa SD.

## 🚀 Deploy ke Vercel (Gratis)

### Langkah 1 — Upload ke GitHub

1. Buat akun di [github.com](https://github.com) (kalau belum punya)
2. Klik tombol **"New repository"** (tombol hijau)
3. Isi nama repo: `readtrack`
4. Pilih **Public**
5. Klik **Create repository**
6. Upload semua file ini:
   - `index.html`
   - `vercel.json`
   - folder `api/` beserta `api/chat.js`

> **Cara upload:** di halaman repo kosong, klik **"uploading an existing file"**, lalu drag & drop semua file.

---

### Langkah 2 — Daftar & Deploy di Vercel

1. Buka [vercel.com](https://vercel.com)
2. Klik **"Sign Up"** → pilih **"Continue with GitHub"**
3. Setelah login, klik **"Add New Project"**
4. Pilih repo `readtrack` yang tadi dibuat
5. Klik **Deploy** — tunggu ~1 menit
6. Websitemu akan live di: `https://readtrack-[namamu].vercel.app`

---

### Langkah 3 — Tambahkan API Key Claude

Ini bagian terpenting agar fitur AI cerita berjalan!

1. Buka [console.anthropic.com](https://console.anthropic.com)
2. Login / daftar akun Anthropic
3. Klik **"API Keys"** di sidebar kiri
4. Klik **"Create Key"** → copy API key-nya (simpan baik-baik!)

Lalu masukkan ke Vercel:

1. Buka dashboard Vercel → klik project `readtrack`
2. Klik tab **"Settings"**
3. Klik **"Environment Variables"** di sidebar
4. Klik **"Add"**, isi:
   - **Name:** `ANTHROPIC_API_KEY`
   - **Value:** paste API key dari Anthropic
   - **Environment:** centang semua (Production, Preview, Development)
5. Klik **Save**
6. Kembali ke tab **Deployments** → klik **"Redeploy"**

✅ Selesai! Fitur AI sudah aktif.

---

## 📁 Struktur File

```
readtrack/
├── index.html       ← Website utama (semua UI + JS)
├── vercel.json      ← Konfigurasi Vercel
├── README.md        ← Panduan ini
└── api/
    └── chat.js      ← Proxy API Claude (menyimpan API key dengan aman)
```

## ⚡ Fitur

- 🎭 **Character Maker** — Buat tokoh sendiri (nama, penampilan, sifat, kemampuan spesial)
- ✨ **Story Customization** — Pilih latar, genre, dan konflik cerita
- 🤖 **AI Story Generator** — Cerita dibuat otomatis oleh Claude AI
- 📖 **Reading Mode** — Tampilan baca bersih tanpa distraksi
- ⚔️ **Story Quest** — Kuis pemahaman berbasis AI
- 📊 **Stamina Tracker** — Grafik durasi baca & riwayat cerita
- ⚡ **Level System** — 5 level, cerita makin panjang & soal makin banyak
- 🏆 **Leaderboard** — Papan peringkat antar pemain

## ❓ FAQ

**Q: Apakah gratis?**  
A: Ya! GitHub + Vercel gratis. API Claude berbayar tapi ada free credits untuk percobaan.

**Q: Kalau API key belum ada, apakah website tetap bisa dipakai?**  
A: Ya, website tetap berjalan dengan cerita template (tanpa AI).

**Q: Data siswa tersimpan di mana?**  
A: Di `localStorage` browser masing-masing. Tidak ada database eksternal.
