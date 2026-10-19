# uts-machine-learning-241011401418

# Identitas 
**Nama  : Novri Faudzan Pratama**

**NIM   : 241011401418**

**Kelas : 05TPLE005**

**Reg   : Reg C(Sabtu**

**Matkul: Machine Learning**

## RINGKASAN
A. Linear Regression

Dataset yang digunakan adalah Ads_Data.csv, dengan total 40 data. Sebanyak 32 data digunakan untuk training dan 8 data untuk testing.
Persamaan regresi yang diperoleh:
ŷ = 29.3242 + 9.0051X

Hasil evaluasi model:

<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Data</th>
      <th>MAE</th>
      <th>MSE</th>
      <th>RMSE</th>
      <th>R2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Training</td>
      <td>4.0424</td>
      <td>31.9135</td>
      <td>5.6492</td>
      <td>0.9556</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Testing</td>
      <td>6.3949</td>
      <td>54.5504</td>
      <td>7.3858</td>
      <td>0.8152</td>
    </tr>
  </tbody>
</table>
</div>

Kesimpulan: Model memperoleh nilai R² sebesar 0.8152 pada data testing. Artinya, model dapat menjelaskan sekitar 81,52% variasi penjualan pada data testing. Koefisien regresi yang positif nunjukin kalo kenaikan biaya iklan berkaitan dengan peningkatan penjualan berdasarkan model.

B. Logistic Regression

Dataset yang digunakan adalah Email_Data.csv, dengan total 60 data. Sebanyak 45 data digunakan untuk training dan 15 data untuk testing.

Hasil evaluasi pada threshold 0.5:

<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Metrik</th>
      <th>Hasil</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Accuracy</td>
      <td>100%</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Precision</td>
      <td>100%</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Recall</td>
      <td>100%</td>
    </tr>
    <tr>
      <th>4</th>
      <td>F1-score</td>
      <td>100%</td>
    </tr>
  </tbody>
</table>
</div>

<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Metrik</th>
      <th>Hasil</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>True Negative (TN)</td>
      <td>11</td>
    </tr>
    <tr>
      <th>2</th>
      <td>False Positive (FP)</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>False Negative (FN)</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>True Positive (TP)</td>
      <td>4</td>
    </tr>
  </tbody>
</table>
</div>

Kesimpulan: Model berhasil mengklasifikasikan seluruh 15 data testing dengan benar. Namun, hasil ini perlu ditafsirkan dengan hati-hati karena jumlah data testing masih terbatas dan belum menjamin performa yang sama pada data baru.

C. Eksperimen Threshold
Pengujian dilakukan menggunakan threshold 0.3, 0.5, dan 0.7.
  - Threshold 0.3: Accuracy, precision, dan recall mencapai 100%.
  - Threshold 0.5: Accuracy, precision, dan recall mencapai 100%.
  - Threshold 0.7: Precision 100%, tetapi recall turun menjadi 50% karena terdapat dua email spam yang tidak terdeteksi.
Threshold 0.5 dipilih karena memberikan hasil yang seimbang pada data testing tersebut.

D. Perbandingan dengan Scikit-Learn
  - Linear Regression: Koefisien dan nilai R² dari implementasi manual hampir sama dengan scikit-learn.
  - Logistic Regression: Kedua model memperoleh accuracy 100% pada data testing, tetapi nilai koefisien berbeda karena metode optimasi dan regularisasi yang digunakan berbeda.
