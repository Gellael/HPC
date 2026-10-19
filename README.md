# HPC Local Impact

Dasbor interaktif untuk belajar bagaimana komputasi performa tinggi (*high-performance computing*, HPC) bisa membantu menjawab masalah di tingkat lokal, mulai dari banjir, hutan, sampai energi.

Proyek ini murni demo edukasi. Semua angka di dalamnya adalah data sintetis.

## Apa yang bisa dicoba

- **Pilih tantangan lokal**: pemodelan banjir, pemantauan hutan, atau perencanaan energi. Deskripsi, tag, dan grafik ikut berubah.
- **Simulator beban kerja**: geser jumlah node (1-64) dan pilih ukuran data (120 GB, 480 GB, atau 1,2 TB) untuk melihat estimasi waktu selesai, speedup, dan penghematan waktu.
- **Dua grafik**: perbandingan waktu proses workstation biasa vs klaster HPC, dan kurva skala waktu terhadap jumlah node.
- **Mode gelap**, navigasi samping yang bisa dibuka di layar kecil, dan tampilan responsif.

## Teknologi

HTML, CSS, dan JavaScript murni tanpa build step. Grafik memakai [Chart.js](https://www.chartjs.org/). Font: Bricolage Grotesque dan IBM Plex Sans dari Google Fonts.

## Menjalankan di komputer

1. Unduh atau clone repositori ini.
2. Buka `index.html` di browser (atau pakai ekstensi Live Server di VS Code).
3. Pastikan terhubung ke internet, karena Chart.js dan font dimuat lewat CDN.

## Publikasi lewat GitHub Pages

1. Buat repositori baru, lalu unggah `index.html`, `style.css`, `script.js`, dan `README.md` ke folder root.
2. Buka **Settings → Pages**.
3. Di **Build and deployment**, pilih **Deploy from a branch**.
4. Pilih branch `main` dan folder `/ (root)`, lalu simpan.
5. Tunggu beberapa menit sampai situs aktif.

## Cara kerja simulator

Simulator memakai model sederhana (mirip hukum Amdahl): sebagian kecil pekerjaan (8%) harus berjalan berurutan, sisanya dibagi ke semua node dengan efisiensi paralel tertentu (76-84% tergantung skenario). Dari situ dihitung speedup dan waktu proses.

Performa HPC sungguhan dipengaruhi arsitektur prosesor, memori, jaringan antar-node, penyimpanan, seberapa paralel algoritmanya, dan perpindahan data. Model ini tidak menangkap semua itu.

## Catatan penting

Dasbor ini tidak terhubung ke klaster HPC, tidak menjalankan model ilmiah, dan tidak memproses data satelit. Hasilnya bukan prediksi banjir, hutan, atau energi yang nyata, dan bukan benchmark.