# 🏨 Web Scraping & Analisis Harga Penginapan: Studi Kasus Traveloka

Proyek ini melakukan **automated web scraping** pada platform Traveloka untuk mengumpulkan data akomodasi (**Villa dan Apartemen**) di wilayah Bandung dan Bali. Data yang dikumpulkan disimpan secara terstruktur ke dalam database **PostgreSQL** untuk kemudian dianalisis guna mendapatkan *insight* harga dan kualitas.

---

## 🛠️ Tools & Teknologi
* **Bahasa Pemrograman:** Python 🐍
* **Library Scraping:** BeautifulSoup & Requests
* **Database:** PostgreSQL 🐘
* **Analisis Data:** SQL Queries & Python DataFrames (Pandas)

---

## 📊 Hasil Web Scraping
Proses scraping berhasil mengumpulkan total **320 entitas data** yang berasal dari **16 URL unik** (masing-masing URL memuat 20 data properti). Data disimpan ke dalam dua tabel utama:

### 1. Tabel `webpages`
Berfungsi untuk menyimpan metadata dari proses scraping.
* **Kolom:** URL yang di-scrap, Lokasi, Tipe Properti, dan Waktu Akses.

<img width="581" alt="Tabel Webpages" src="https://github.com/user-attachments/assets/85204a4e-e79e-43fb-a675-170651479dd7" />

### 2. Tabel `properties`
Berfungsi menyimpan detail informasi fisik dan harga akomodasi.
* **Kolom:** Title (Nama Tempat), Property Type, District, City/Regency, Harga, dan Rating.

<img width="498" alt="Tabel Properties 1" src="https://github.com/user-attachments/assets/e28403d7-c656-4140-8f23-81af391391a9" />
<img width="495" alt="Tabel Properties 2" src="https://github.com/user-attachments/assets/40adf642-0a85-4714-8a5a-4a7911054889" />

---

## 🔍 Analisis Menggunakan Query Python

### 📍 1. Distribusi Harga Villa di Bali
Analisis ini bertujuan untuk melihat sebaran harga khusus untuk kategori **Villa** di area **Bali**.
<img width="496" alt="Distribusi Harga Bali" src="https://github.com/user-attachments/assets/05b8686b-b7ec-468c-909b-4faf4c44991a" />

### ⭐ 2. Akomodasi dengan Rating Tertinggi
Digunakan untuk mengidentifikasi penginapan premium. Data ini sangat berguna bagi segmen pasar yang mengutamakan **kenyamanan dan pelayanan terbaik** berdasarkan pengalaman pengguna sebelumnya.
<img width="500" alt="Rating Tertinggi 1" src="https://github.com/user-attachments/assets/d28ec13e-0285-4fbc-b7d6-fda678e9b256" />
<img width="491" alt="Rating Tertinggi 2" src="
