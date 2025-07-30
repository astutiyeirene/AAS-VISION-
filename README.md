
# OCR Evaluation Tool – UAS Astuti Yeirene Panggabean

## 📁 Struktur Proyek

```
uas_astuti/
├── generate_ground_truth_csv.py   # Script untuk menghasilkan ground_truth.csv dari label .txt
├── ocr_eval.py                    # Script evaluasi OCR hasil terhadap ground truth
├── log.txt                        # Log hasil evaluasi
├── results.csv                    # Output evaluasi dalam bentuk CSV
├── test/
│   ├── ground_truth.csv          # File CSV hasil gabungan label ground truth
│   ├── testXXX_X.jpg             # Gambar uji
│   └── testXXX_X.txt             # Label ground truth dalam file teks
```

## 📝 Deskripsi Proyek

Proyek ini bertujuan untuk mengevaluasi hasil Optical Character Recognition (OCR) berdasarkan gambar-gambar uji dan file ground truth yang sesuai.

### 1. `generate_ground_truth_csv.py`
- Script ini membaca file `.txt` yang menyertai setiap gambar dalam folder `test/` dan menggabungkannya ke dalam satu file `ground_truth.csv`.
- Format CSV: `filename`, `label`

### 2. `ocr_eval.py`
- Script ini digunakan untuk membandingkan hasil OCR dengan `ground_truth.csv`.
- Output evaluasi disimpan dalam `results.csv` dan detailnya di `log.txt`.

## ▶️ Cara Menjalankan

1. **Generate ground truth**:
   ```bash
   python generate_ground_truth_csv.py
   ```

2. **Jalankan evaluasi OCR**:
   ```bash
   python ocr_eval.py
   ```

> Pastikan semua file gambar dan label `.txt` ada di dalam folder `test/`.

## 📦 Dependencies

- Python 3.x
- Pandas
- (Tambahkan library lain jika digunakan, misalnya pytesseract, opencv, dll.)

## 📌 Catatan

- File gambar seperti `test001_1.jpg` memiliki pasangan label `test001_1.txt`.
- `ground_truth.csv` dibuat otomatis dari file `.txt`.
