
# Rekomendasi Tanaman Berdasarkan Curah Hujan dan Suhu di Kota-Kota Australia

## 👨‍🌾 Deskripsi Proyek ETL
Proyek ini merupakan sistem ETL (Extract, Transform, Load) yang bertujuan untuk merekomendasikan jenis tanaman berdasarkan kondisi iklim, khususnya suhu dan curah hujan, di berbagai kota di Australia. Proyek ini menggabungkan data cuaca dan data pertanian untuk mendukung pengambilan keputusan di bidang pertanian.

---

## 🎯 Manfaat Data / Use Case
**Tujuan Proyek:**
- Memberikan rekomendasi tanaman berdasarkan suhu dan curah hujan lokal.

**Manfaat:**
- Membantu petani memilih tanaman yang sesuai dengan iklim setempat.
- Mengurangi risiko gagal panen.
- Mendukung analisis keberlanjutan pertanian di masa depan.

---

## 📈 Serving Analisis
**Analisis Data Cuaca:**
- Hitung suhu tertinggi dan terendah per lokasi.
- Hitung curah hujan tertinggi dan terendah.
- Visualisasi: Bar chart suhu dan curah hujan per lokasi.

**Analisis Kebutuhan Nutrisi:**
- Rata-rata kebutuhan NPK per tanaman.
- Visualisasi: Bar chart dan pie chart untuk NPK.

---

## 🤖 Serving Machine Learning
**Metode:**
- K-Means Clustering: Mengelompokkan lokasi berdasarkan iklim.
- KNN: Mencocokkan tanaman dengan lokasi berdasarkan kondisi cuaca.

**Visualisasi:**
- PCA Cluster Plot: Visualisasi klaster lokasi berdasarkan cuaca.
- Elbow Plot: Menentukan jumlah klaster optimal.
- Output: DataFrame rekomendasi tanaman dan lokasi yang cocok.

---

## 🗂️ Extract (Pengambilan Data)
- **Sumber Data:**
  - Cuaca: `lionelbottan/weatheraus`
  - Tanaman: `datasetengineer/smart-farming-data-2024-sf24`
- **Teknik:** Unduh via `kagglehub.dataset_download` dalam format CSV.
- **Penanganan Error:** Validasi nilai `null` dan `duplicated`.

---

## 🔧 Transform (Pembersihan & Transformasi)
- Menghapus nilai null dan duplikasi.
- Menghitung rata-rata suhu dari Min dan MaxTemp.
- Menyesuaikan nama kolom.
- Menyelaraskan fitur tanaman dan cuaca agar bisa digabungkan.

---

## 💾 Load (Pemindahan ke Target)
- **Target:** File CSV
  - `hasil_analisis_suhu_dan_hujan.csv`
  - `analisis_npk_per_tanaman.csv`
- **Validasi Load:**
  - Tidak ada duplikat.
  - Format sesuai dan struktur data terjaga.

---

## 🏗️ Arsitektur / Workflow ETL
- **Tools & Libraries:** 
  - Google Colab
  - Pandas, Seaborn, Matplotlib
  - Sklearn, PyCaret
- **Workflow:**
  1. **Extract:** Unduh data dari Kaggle.
  2. **Transform:** Pembersihan dan penggabungan data.
  3. **Load:** Simpan ke file CSV.
  4. **Serving:** Model clustering dan rekomendasi tanaman.

- **Struktur Modular:**
  - Fungsi: `extract_data()`, `transform_data()`, `load_data()`, `serve_model()`

---

## 🧑‍💻 Kode Program
- Struktur kode modular sesuai tahapan ETL.
- Penamaan variabel deskriptif (`df_cuaca`, `df_tanaman`, dll).
- Komentar disediakan seperlunya.
- Menghindari hardcoding berlebih.

---

## 📚 Dokumentasi
- Penjelasan alur ETL dijabarkan per tahap.
- Penjelasan sumber data dan transformasi dilakukan secara rinci.
- Tools yang digunakan disebutkan lengkap.

---

## 🎤 Presentasi / Demo
- Presentasi dilakukan dalam 10 menit, menjelaskan alur dan hasil proyek.
- Proyek diunggah ke GitHub.

---

## 👥 Kontributor

| Contributor       | GitHub Profile                                  |
|-------------------|------------------------------------------------|
| **Adam Mahabayu Muhibulloh (234311002)**  | [🌐 Profile](https://github.com/adammahabayu) |
| **Afiq Galuh Setya Ramadhani (234311004)**      | [🌐 Profile](https://github.com/afiqgsr)    |
| **Alfonsus William Hamonangan Sinaga (234311005)**  | [🌐 Profile](https://github.com/willidevv) |
| **Fauzan Fathin Zaky (234311014)**      | [🌐 Profile](https://github.com/fauzan123ae)    |

---

