# Dry Bean Classification Project

## Isi folder
- `ProjectAkhirDS.ipynb`: notebook utama yang berisi seluruh tahapan dan penjelasan Markdown.

## Dataset
Dataset menggunakan Dry Bean dari UCI Machine Learning Repository:
https://archive.ics.uci.edu/dataset/602/dry+bean+dataset

DOI: https://doi.org/10.24432/C50S4B  
Lisensi: CC BY 4.0.

Notebook akan mencari `data/Dry_Bean_Dataset.xlsx` atau `Dry_Bean_Dataset.xlsx`. Jika file Excel tidak ditemukan, notebook mengambil dataset dari UCI menggunakan `ucimlrepo` (membutuhkan koneksi internet). Salinan CSV mentah dan data bersih disimpan ke folder `data/`.

## Cara menjalankan

1. Buka folder proyek di VS Code, Jupyter Notebook, atau Google Colab.
2. Instal dependencies

3. Buka dan jalankan `ProjectAkhirDS.ipynb` dari sel paling atas sampai paling bawah.
4. Setelah berhasil, periksa file CSV yang dihasilkan dan lengkapi bagian konklusi berdasarkan hasil aktual.

## Alur analisis
Business Understanding → Data Gathering → EDA → Cleaning → Preprocessing → Feature Selection → SVM & Random Forest → Evaluasi → Konklusi.

## Catatan pengerjaan
- Dataset UCI asli dinyatakan tidak memiliki missing value. Notebook tetap memeriksanya dan tidak membuat nilai kosong buatan.
- Duplikat identik dihapus jika ditemukan.
- Outlier IQR hanya ditandai sebagai kandidat dan tidak otomatis dihapus.
- Feature selection dihitung dari data training saja.
- Scaling dilakukan dalam Pipeline SVM untuk mencegah data leakage. Random Forest tidak menggunakan scaling.
- Nilai evaluasi tidak ditulis terlebih dahulu; seluruh hasil dihitung saat notebook dijalankan.
