Web Scraping & Analisis Harga Penginapan: Studi Kasus Traveloka
Proyek ini melakukan automated web scraping pada platform Traveloka untuk mengumpulkan data akomodasi (Villa dan Apartemen) di wilayah Bandung dan Bali. Data yang dikumpulkan disimpan secara terstruktur ke dalam database PostgreSQL untuk kemudian dianalisis.

🛠️ Tools & Teknologi
Bahasa Pemrograman: Python

Library Scraping: BeautifulSoup

Database: PostgreSQL

Analisis Data: SQL Queries & Python DataFrames

📊 Hasil Web Scraping
Proses scraping berhasil mengumpulkan total 320 entitas data yang berasal dari 16 URL unik (masing-masing URL memuat 20 data properti). Data disimpan ke dalam dua tabel utama:

1. Tabel webpages
Berfungsi untuk menyimpan metadata dari proses scraping.

Kolom: URL yang di-scrap, Lokasi, Tipe Properti, dan Waktu Akses.

<img width="581" alt="Tabel Webpages" src="https://github.com/user-attachments/assets/85204a4e-e79e-43fb-a675-170651479dd7" />

2. Tabel properties
Berfungsi menyimpan detail informasi fisik dan harga akomodasi.

Kolom: Title (Nama Tempat), Property Type, District, City/Regency, Harga, dan Rating.

<img width="498" alt="Tabel Properties 1" src="https://github.com/user-attachments/assets/e28403d7-c656-4140-8f23-81af391391a9" /> <img width="495" alt="Tabel Properties 2" src="https://github.com/user-attachments/assets/40adf642-0a85-4714-8a5a-4a7911054889" />

🔍 Analisis Menggunakan Query Python
1. Distribusi Harga Villa di Bali
Analisis ini bertujuan untuk melihat sebaran harga khusus untuk kategori Villa di area Bali. <img width="496" alt="Distribusi Harga Bali" src="https://github.com/user-attachments/assets/05b8686b-b7ec-468c-909b-4faf4c44991a" />

2. Akomodasi dengan Rating Tertinggi
Digunakan untuk mengidentifikasi penginapan premium. Data ini sangat berguna bagi segmen pasar yang mengutamakan kenyamanan dan pelayanan terbaik berdasarkan pengalaman pengguna sebelumnya. <img width="500" alt="Rating Tertinggi 1" src="https://github.com/user-attachments/assets/d28ec13e-0285-4fbc-b7d6-fda678e9b256" /> <img width="491" alt="Rating Tertinggi 2" src="https://github.com/user-attachments/assets/00623def-3b2d-4b4b-a55a-77d6383b8429" />

3. Akomodasi dengan Harga di Bawah Rata-Rata
Filter ini menampilkan properti yang lebih ekonomis dibandingkan rata-rata harga pasar di Bali dan Bandung.

Temuan: Terdapat 52 properti yang masuk kategori budget-friendly.

<img width="461" alt="Dibawah Rata-rata 1" src="https://github.com/user-attachments/assets/189ac6d2-1dd6-4769-9ae1-20b545abbd6a" /> <img width="372" alt="Dibawah Rata-rata 2" src="https://github.com/user-attachments/assets/72d05bd0-f1e3-493b-b6eb-e563be717a09" />

🐘 Analisis Menggunakan Query PostgreSQL
Perbandingan Harga vs Rating
Ditemukan adanya 1 properti yang memiliki harga di atas rata-rata namun dengan rating rendah (di bawah 8). Analisis ini membantu user untuk menghindari penginapan yang kurang worth it secara nilai ekonomi. <img width="515" alt="Analisis Harga vs Rating" src="https://github.com/user-attachments/assets/53d4e3be-280c-45d3-853b-67660c7e0bf2" />

Perbandingan Tipe Properti: Villa vs Apartment
Berdasarkan data agregasi:

Villa: Memiliki harga rata-rata, harga maksimal, dan harga minimal yang lebih tinggi.

Apartemen: Cenderung lebih terjangkau di semua lini harga.

Kesimpulan: Apartemen adalah pilihan terbaik bagi pencari penginapan dengan budget terbatas.

<img width="521" alt="Analisis Tipe Properti" src="https://github.com/user-attachments/assets/b186f211-0a49-48ea-859f-83b0e073b8b7" />
