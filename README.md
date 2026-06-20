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
 Dimensi data: (5000, 14)
   ID  Age  Experience  Income  ZIP Code  Family  CCAvg  Education  Mortgage  \
0   1   25           1      49     91107       4    1.6          1         0   
1   2   45          19      34     90089       3    1.5          1         0   
2   3   39          15      11     94720       1    1.0          1         0   
3   4   35           9     100     94112       1    2.7          2         0   
4   5   35           8      45     91330       4    1.0          2         0   

   Personal Loan  Securities Account  CD Account  Online  CreditCard  
0              0                   1           0       0           0  
1              0                   1           0       0           0  
2              0                   0           0       0           0  
3              0                   0           0       0           0  
4              0                   0           0       0           1  

Missing values:
 ID                    0
Age                   0
Experience            0
Income                0
ZIP Code              0
Family                0
CCAvg                 0
Education             0
Mortgage              0
Personal Loan         0
Securities Account    0
CD Account            0
Online                0
CreditCard            0
dtype: int64

Statistik Deskriptif:
         Income     CCAvg    Family
count  5000.000  5000.000  5000.000
mean     73.774     1.938     2.396
std      46.034     1.748     1.148
min       8.000     0.000     1.000
25%      39.000     0.700     1.000
50%      64.000     1.500     2.000
75%      98.000     2.500     3.000
max     224.000    10.000     4.000

Distribusi Pendidikan:
 Education
1    2096
3    1501
2    1403
Name: count, dtype: int64

Proporsi Target:
 Personal Loan
0    0.904
1    0.096
Name: proportion, dtype: float64
Optimization terminated successfully.
         Current function value: 0.133478
         Iterations 9
                           Logit Regression Results                           
==============================================================================
Dep. Variable:          Personal Loan   No. Observations:                 5000
Model:                          Logit   Df Residuals:                     4994
Method:                           MLE   Df Model:                            5
Date:                Sat, 20 Jun 2026   Pseudo R-squ.:                  0.5779
Time:                        20:08:56   Log-Likelihood:                -667.39
converged:                       True   LL-Null:                       -1581.0
Covariance Type:            nonrobust   LLR p-value:                     0.000
===============================================================================
                  coef    std err          z      P>|z|      [0.025      0.975]
-------------------------------------------------------------------------------
const         -13.1779      0.518    -25.451      0.000     -14.193     -12.163
Income          0.0598      0.003     22.254      0.000       0.055       0.065
CCAvg           0.1627      0.041      4.017      0.000       0.083       0.242
Family          0.5871      0.071      8.237      0.000       0.447       0.727
Education_2     3.9106      0.251     15.578      0.000       3.419       4.403
Education_3     3.9332      0.244     16.098      0.000       3.454       4.412
===============================================================================

Odds Ratio:
                 2.5%    97.5%       OR
const         0.0000   0.0000   0.0000
Income        1.0560   1.0672   1.0616
CCAvg         1.0869   1.2739   1.1767
Family        1.5642   2.0684   1.7987
Education_2  30.5269  81.6680  49.9307
Education_3  31.6366  82.4400  51.0697

Confusion Matrix:
 [[889  15]
 [ 28  68]]
Accuracy  : 0.9570
Precision : 0.8193
Recall    : 0.7083
F1-Score  : 0.7598
AUC       : 0.9540
<img width="1166" height="490" alt="image" src="https://github.com/user-attachments/assets/5106e01f-f1f8-4957-847b-0c1fd6033a86" />

=== KEBAIKAN MODEL ===
Pseudo R² (McFadden) : 0.5779
Log-Likelihood       : -667.3904
LL-Null              : -1581.0206
LLR p-value          : 0.0000e+00
AIC                  : 1346.7807
BIC                  : 1385.8839

## Dataset
Bank Personal Loan Modelling – Universal Bank (5.000 nasabah)
