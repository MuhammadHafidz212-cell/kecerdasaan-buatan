# UAS Kecerdasan Buatan (SIF210) - Penjadwalan Otomatis Mata Kuliah Menggunakan Algoritma Genetika

**Nama:** Muhammad Hafis  
**NIM:** 24146028  
**Mata Kuliah:** Kecerdasan Buatan (SIF210)  


---

## Deskripsi Proyek

Proyek ini mengimplementasikan **Algoritma Genetika** untuk menyelesaikan masalah **Penjadwalan Otomatis Mata Kuliah**. Tujuannya adalah mengalokasikan 24 mata kuliah ke dalam 4 ruangan dan 12 slot waktu (Senin–Kamis, 3 slot per hari) dengan meminimalkan tiga jenis konflik:

1. **Konflik Ruang** – Dua mata kuliah menggunakan ruang dan slot waktu yang sama.
2. **Konflik Dosen-Waktu** – Dosen yang sama mengajar lebih dari satu mata kuliah pada slot waktu yang sama.
3. **Konflik Dosen-Hari** – Dosen yang sama mengajar lebih dari satu kali pada hari yang sama.

## Parameter Algoritma Genetika

| Parameter          | Nilai  |
|--------------------|--------|
| Populasi Awal      | 60     |
| Maksimum Generasi  | 100    |
| Crossover Rate     | 85%    |
| Mutation Rate      | 20%    |
| Struktur Kromosom  | 24 gen (ruang, slot waktu) per individu |
| Seleksi            | Tournament Selection (size=3) |
| Fitness Function   | 100 / (1 + total_konflik) |

## Cara Menjalankan

### Prasyarat

Pastikan Python 3.x dan pustaka berikut terinstal:

```bash
pip install jupyter matplotlib numpy pandas
```

### Menjalankan Notebook

1. Buka terminal di direktori proyek ini.
2. Jalankan Jupyter Notebook:

```bash
jupyter notebook UAS_Penjadwalan_GA.ipynb
```

3. Pilih menu **Cell > Run All** untuk mengeksekusi seluruh sel.
4. Atau jalankan langsung dengan `nbconvert`:

```bash
jupyter nbconvert --to script --execute UAS_Penjadwalan_GA.ipynb --output hasil
python hasil.txt
```

## Struktur File

```
├── UAS_Penjadwalan_GA.ipynb   # Notebook utama implementasi GA
├── README.md                   # Dokumentasi proyek
├── grafik_fitness.png          # Grafik hasil evolusi (generated)
└── Laporan_UAS.pdf             # Laporan lengkap (PDF)
```

## Hasil Ringkasan

- **Fitness Terbaik:** ~25.0000 (setara 3 konflik)
- **Fitness Rata-rata Akhir:** ~8.73
- **Konflik Tersisa:** 3

> **Catatan:** Hasil dapat bervariasi setiap kali run karena sifat stokastik Algoritma Genetika.
