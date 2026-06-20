# Analisis Regresi Logistik Biner: Prediksi Penerimaan Personal Loan

## Deskripsi
Proyek ini membangun model regresi logistik biner untuk memprediksi
peluang nasabah Universal Bank menerima tawaran produk pinjaman pribadi
(*personal loan*), berdasarkan variabel Income, CCAvg, Family, dan Education.

## Hasil Utama
| Metrik | Nilai |
|---|---|
| Pseudo R² (McFadden) | 0.578 |
| Accuracy | 95.7% |
| AUC | 0.954 |
| F1-Score | 76.0% |

## Cara Menjalankan
```bash
git clone https://github.com/aufaazakki577-sketch/personal-loan-logistic-regression
cd personal-loan-logistic-regression
pip install -r requirements.txt

# Letakkan file Excel di folder data/, lalu:
python analysis.py
```

## Output
![Evaluasi Model](output/evaluasi_model.png)

## Dataset
Bank Personal Loan Modelling – Universal Bank (5.000 nasabah)
