🗺️ Scripting With Python For GIS Environment

Deskripsi
Repository ini berisi kumpulan skrip Python yang dikembangkan untuk mendukung berbagai kebutuhan di lingkungan Geographic Information System (GIS), khususnya dalam pengelolaan data spasial dan dokumentasi lapangan.

Fokus utama skrip dalam repository ini adalah otomasi alur kerja GIS yang sering ditemui di lapangan maupun di tahap pengolahan data, seperti:

📷 Manajemen Foto Lapangan

Ekstraksi koordinat GPS dari metadata EXIF.

Rename foto berdasarkan atribut shapefile (misalnya alamat atau ID).

Logging aktivitas rename ke dalam CSV agar proses dapat ditelusuri.

📍 Integrasi Foto dengan Data Spasial

Pencocokan koordinat foto dengan titik terdekat pada shapefile.

Update kolom PATH atau FILENAME di CSV agar sinkron dengan lokasi folder terbaru.

Pembuatan CSV baru yang menghubungkan foto dengan data spasial.

🗂️ Otomasi dan Tracking Data

Penyimpanan riwayat pemrosesan (rename log, update path) untuk keperluan audit.

Dukungan format shapefile dan CSV sebagai format utama GIS.

Dengan adanya skrip ini, pengguna GIS dapat menghemat waktu dalam mengelola ribuan data foto, meminimalisir kesalahan manual, serta menjaga konsistensi antara foto lapangan dengan data spasialnya.
