# 🎬 RegionalSearch — Premium Movie Discovery

![Vercel Deployment](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![TMDB API](https://img.shields.io/badge/TMDB-01b4e4?style=for-the-badge&logo=the-movie-database&logoColor=white)
![JavaScript](https://img.shields.io/badge/Vanilla_JS-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

**RegionalSearch** (formerly StreamFinder Pro) adalah platform penemuan film dan acara TV modern yang dirancang dengan estetika *Dark Mode* dan *Glassmorphism*. Dilengkapi dengan fitur pelacakan ketersediaan layanan streaming berdasarkan wilayah geografis secara real-time.

[🚀 Lihat Demo Langsung](https://regional-search.vercel.app)

---

## ✨ Fitur Unggulan

* **⚡ Instant Navigation Search**: Cari judul favorit Anda dari halaman mana pun tanpa perlu memuat ulang halaman.
* **🌍 Regional Streaming Data**: Mengetahui di mana sebuah film tersedia untuk ditonton (Netflix, Disney+, HBO, dll) berdasarkan negara.
* **📱 Fully Responsive Design**: Antarmuka yang optimal untuk Desktop hingga Mobile dengan *Hamburger Menu* yang interaktif.
* **📂 Structured Explorer**: Halaman khusus untuk **Movies** dan **TV Shows** dengan pagination yang lancar.
* **💾 Personal Watchlist**: Simpan koleksi film favorit Anda langsung di browser menggunakan LocalStorage.
* **🔗 Clean URL Architecture**: Navigasi yang ramah pengguna dengan format `/movies/:id` (via Vercel Rewrites).

---

## 🛠️ Teknologi yang Digunakan

* **Frontend**: HTML5, CSS3 (Custom Variables, Flexbox, Grid), Vanilla JavaScript (ES6+).
* **API**: [The Movie Database (TMDB)](https://www.themoviedb.org/documentation/api).
* **Deployment**: Vercel dengan konfigurasi `vercel.json` untuk *Server-side rewrites*.
* **Design Concept**: Glassmorphism & High-Contrast Dark Theme.

---

## 📸 Tampilan Antarmuka

| Desktop View | Mobile Menu |
|---|---|
| <img src="https://via.placeholder.com/800x450/050508/FFFFFF?text=Desktop+Preview" width="400"> | <img src="https://via.placeholder.com/300x600/050508/FFFFFF?text=Mobile+Preview" width="150"> |

---

## ⚙️ Cara Menjalankan Lokal

1.  **Clone repositori ini:**
    ```bash
    git clone [https://github.com/username/regional-search.git](https://github.com/username/regional-search.git)
    ```
2.  **Dapatkan API Key:**
    Daftar di [TMDB](https://www.themoviedb.org/) untuk mendapatkan API Key.
3.  **Konfigurasi:**
    Masukkan API Key Anda ke dalam variabel `API_KEY` di setiap file `.html`.
4.  **Buka file:**
    Cukup buka `index.html` di browser Anda atau gunakan ekstensi *Live Server* di VS Code.

---

## 🚀 Konfigurasi Deployment (Vercel)

Proyek ini menggunakan `vercel.json` untuk menangani navigasi URL yang bersih:

```json
{
  "cleanUrls": true,
  "rewrites": [
    { "source": "/movies/:id", "destination": "/detail.html?id=:id&type=movie" },
    { "source": "/tv/:id", "destination": "/detail.html?id=:id&type=tv" }
  ]
}
