# 📂 Scripting With Python For GIS Environment  

Kumpulan script Python untuk mendukung pekerjaan di bidang **Geospatial Information System (GIS)**, khususnya dalam **otomatisasi manajemen foto, metadata, CSV, dan shapefile**.  
Script ini dikembangkan untuk mempermudah sinkronisasi data spasial dan memastikan konsistensi antara atribut, foto lapangan, serta database.  

---

## 📌 Daftar Script  

### 1. Update Kolom PATH di CSV  
- **Fungsi**: Mengupdate kolom `PATH` di file CSV agar sesuai dengan lokasi direktori foto terbaru.  
- **Kasus penggunaan**: Folder foto dipindahkan, script ini otomatis menyesuaikan path di CSV tanpa input manual.  

---

### 2. Rename Foto Berdasarkan Atribut Shapefile  
- **Fungsi**: Melakukan *batch renaming* foto berdasarkan kolom atribut shapefile (misalnya `Photo`).  
- **Fitur tambahan**: Menangani duplikasi nama file dengan menambahkan suffix otomatis (`_1`, `_2`, dst.).  
- **Output**: Shapefile diperbarui dengan nama file baru, dan log CSV dicatat.  

---

### 3. Rename Foto Berdasarkan GPS Metadata (EXIF)  
- **Fungsi**: Mengekstrak koordinat GPS dari metadata EXIF foto, kemudian mencocokkannya dengan fitur spasial terdekat di shapefile.  
- **Hasil**: Foto di-rename mengikuti atribut tertentu (misalnya `Alamat`), dan proses rename dicatat di log.  

---

### 4. Inject GPS ke Metadata Foto Menggunakan CSV  
- **Fungsi**: Membaca data koordinat dari file CSV (`LATITUDE`, `LONGITUDE`) lalu menulisnya ke metadata EXIF foto.  
- **Library**: Menggunakan `exifread` dan `geopy` untuk ekstraksi & pencocokan.  
- **Kegunaan**: Foto yang awalnya tidak memiliki informasi koordinat bisa langsung dipetakan di GIS.  

---

### 5. Inject GPS ke Metadata Foto Menggunakan ExifTool  
- **Fungsi**: Alternatif yang lebih cepat dan stabil untuk menulis koordinat GPS ke metadata foto.  
- **Cara kerja**: Menggunakan `subprocess` untuk memanggil **ExifTool** langsung dari Python.  
- **Fitur**: Mendukung format `N/S` untuk latitude dan `E/W` untuk longitude.  
- **Kelebihan**: Lebih powerful dan minim error dibanding manipulasi manual metadata.  

---

## ⚡ Manfaat ## 
Dengan script-script ini, pekerjaan repetitif dalam GIS dapat diotomatisasi sehingga:  
✅ Sinkronisasi CSV ↔ Foto lebih cepat  
✅ Rename foto sesuai atribut shapefile tanpa manual  
✅ Injeksi koordinat GPS otomatis ke metadata foto  
✅ Konsistensi data lebih terjamin, hemat waktu, dan minim error  

---

## 🛠️ Teknologi yang Digunakan  
- Python 3.x  
- Pandas  
- GeoPandas  
- Shapely  
- ExifRead  
- Geopy  
- ExifTool  

---

## 🚀 Cara Menggunakan  
1. Clone repository ini.  
2. Sesuaikan **path folder foto, CSV, dan shapefile** di masing-masing script.  
3. Jalankan script sesuai kebutuhan (update PATH, rename foto, atau inject GPS).  
4. Hasil akhir berupa CSV baru, shapefile update, atau foto yang sudah diberi koordinat GPS.  

---

## 👨‍💻 Author  

Semua script dalam repository ini dikembangkan oleh **Septa Mulya Prakarsa**,  
sebagai bagian dari workflow GIS untuk otomasi pengolahan data spasial & foto lapangan.  

💼 Bidang: Geospatial Information System (GIS), Survey & Pemetaan, Data Management  
📌 Fokus: Automasi manajemen foto lapangan, metadata, CSV, dan shapefile dengan Python  

