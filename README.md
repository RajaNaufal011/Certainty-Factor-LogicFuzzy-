# 💡 Certainty Factor & Fuzzy Logic: Diagnosa & Pengendalian

Proyek ini berisi implementasi logika **Certainty Factor (CF)** dan **Logika Fuzzy** untuk menganalisis gejala dalam diagnosa penyakit (misalnya Flu) serta mengontrol kecepatan kipas AC berdasarkan suhu, kelembaban, dan aktivitas.

## 🔧 Teknologi yang Digunakan
- Python 3.x
- [scikit-fuzzy (skfuzzy)](https://pypi.org/project/scikit-fuzzy/)
- NumPy
- Matplotlib

---

## 📁 Struktur Folder/Isi
| File/Folder            | Deskripsi                                                  |
|------------------------|------------------------------------------------------------|
| `cf_diagnosa.py`       | Implementasi logika Certainty Factor untuk diagnosa penyakit |
| `fuzzy_ac_control.py`  | Sistem fuzzy untuk pengaturan kecepatan kipas AC            |
| `README.md`            | Dokumentasi proyek                                          |
| `images/` *(opsional)* | Gambar visualisasi grafik dan diagram                      |

---

## 📌 1. Certainty Factor (CF)
Certainty Factor digunakan untuk menghitung **tingkat keyakinan diagnosa** berdasarkan kombinasi gejala.

### ✅ Fitur:
- Memungkinkan gejala memiliki **bobot pakar (bobot kepercayaan)**.
- Menghitung akumulasi CF dari beberapa gejala.
- Menunjukkan bagaimana **perubahan nilai gejala memengaruhi hasil akhir**.

### 🔍 Contoh:
Jika gejala `demam` berubah dari 0.7 menjadi 0.2 dan bobot pakar 0.8, maka keyakinan terhadap diagnosa **turun drastis**.

---

## 📌 2. Fuzzy Logic - Kontrol Kipas AC
Logika fuzzy digunakan untuk mengatur **kecepatan kipas** berdasarkan:
- Suhu (`temperature`)
- Kelembaban (`humidity`)
- Aktivitas (`aktivitas`) ← variabel tambahan

### ✅ Fitur:
- Menggunakan **fuzzy membership functions** (trapesium dan segitiga).
- Menyediakan **aturan fuzzy (rule base)** untuk pengambilan keputusan.
- Visualisasi grafik keanggotaan dan output.

### 🔍 Contoh Aturan:
```text
Jika suhu panas dan kelembaban lembab → kecepatan kipas maksimal
Jika aktivitas tinggi dan suhu normal → kecepatan kipas tinggi
Jika suhu dingin dan aktivitas rendah → kipas mati
