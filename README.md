Tugas Akhir Projek STATISTIKA DAN PROBABILITAS

NAMA : KADEK LIA SARI UDAYANI
NIM : 2515101066
PRODI : ILMU KOMPUTER
1. Deskripsi Dataset
- Penejelasan Dataset :
Dataset yang digunakan berisi data startup dengan beberapa variabel, antara lain:
< Pendapatan_Tahunan_Miliar_IDR
< Nilai_Pelanggan_Juta_IDR
< Biaya_Akuisisi_Pelanggan_Juta_IDR
< Tingkat_Churn_Persen
< Kategori_Layanan
- Variabel Yang Digunakan : 
< Variabel Independen (X) : Pendapatan_Tahunan_Miliar_IDR  
< Variabel Dependen (Y)   : Nilai_Pelanggan_Juta_IDR
- Tujuan Analisis :
Tujuan analisis adalah untuk mengetahui karakteristik data startup serta hubungan
antara pendapatan tahunan dan nilai pelanggan.
2. Cara Menjalankan 
- Instruksi instalas Package :
Sebelum menjalankan program, pastikan package sudah terinstal:
< tidyverse
< ggplot2
Jika belum terinstal, jalankan perintah  di RStudio:
install.packages("tidyverse")
- Urutan Menjalankan Script : 
Jalankan script secara berurutan di RStudio caranya sebagai berikut : 
< 01_data_preparation.R  
   → Digunakan untuk memuat library, membaca dataset, dan menyiapkan data bersih.
< 02_analisis_deskriptif.R  
   → Melakukan analisis statistik deskriptif (mean, median, modus, standar deviasi, dan visualisasi).
< 03_uji_asumsi.R  
   → Melakukan uji normalitas menggunakan Q-Q Plot dan uji Shapiro-Wilk.
< 04_analisis_korelasi.R  
   → Menghitung korelasi antara variabel Pendapatan_Tahunan_Miliar_IDR dan Nilai_Pelanggan_Juta_IDR serta menampilkan scatter plot.
< 05_analisis_regresi.R  
   → Melakukan analisis regresi linear sederhana dan menampilkan garis regresi.
3. Hasil Dan Interpretasi 
< Analisis Deskriptif
Ukuran Pemusatan (Mean, Median, Modus):
Berdasarkan hasil analisis statistik deskriptif, diperoleh nilai mean dan median yang relatif berdekatan. Hal ini menunjukkan bahwa data cenderung memiliki distribusi yang cukup seimbang dan tidak terlalu miring ke salah satu sisi.
Ukuran Sebaran (Standar Deviasi, Range, Kuartil):
Nilai standar deviasi menunjukkan bahwa data memiliki tingkat variasi yang cukup besar. Range yang lebar mengindikasikan adanya perbedaan nilai yang cukup signifikan antar observasi.
Visualisasi (Histogram dan Boxplot)
Histogram Pendapatan Tahunan :
![Histogram Pendapatan](results/histogram_Pendapatan_Tahunan_Miliar_IDR.png)
Boxplot Pendapatan Tahunan :
![Boxplot Pendapatan](results/boxplot_Pendapatan_Tahunan_Miliar_IDR.png)
Interpretasi:
Histogram menunjukkan distribusi data yang cenderung tidak simetris, sementara boxplot memperlihatkan adanya kemungkinan outlier pada beberapa nilai pendapatan yang sangat tinggi.
< Uji Normalitas
Hasil Uji Shapiro-Wilk
Nilai p-value yang diperoleh dari uji Shapiro-Wilk menunjukkan bahwa data tidak sepenuhnya berdistribusi normal (p-value < 0.05).
Q-Q Plot :
![QQ Plot](results/qqplot_Pendapatan.png)
Interpretasi:
Pada Q-Q Plot terlihat bahwa sebagian titik tidak sepenuhnya mengikuti garis diagonal, sehingga dapat disimpulkan bahwa distribusi data menyimpang dari distribusi normal.
< Analisis Korelasi
Nilai Koefisien Korelasi
Hasil uji korelasi menunjukkan nilai koefisien korelasi positif, yang menandakan adanya hubungan searah antara Pendapatan Tahunan (dalam Miliar IDR) dan Nilai Pelanggan (dalam Juta IDR).
Visualisasi Scatter Plot :
![Scatter Plot](results/scatterplot_Pendapatan_Tahunan_Miliar_IDR_vs_Nilai.png)
Interpretasi:
Scatter plot menunjukkan pola hubungan yang cenderung meningkat, sehingga dapat disimpulkan bahwa semakin tinggi pendapatan tahunan, maka nilai pelanggan juga cenderung meningkat.
< Analisis Regresi
Model Regresi Linear
Analisis regresi linear sederhana menunjukkan bahwa variabel Pendapatan Tahunan berpengaruh terhadap Nilai Pelanggan.
Plot Regresi :
![Plot Regresi](results/plot_regresi_Pendapatan_Tahunan_Miliar_IDR_vs_Nilai.png)
Interpretasi:
Garis regresi menunjukkan tren positif, yang berarti setiap peningkatan pendapatan tahunan diikuti oleh peningkatan nilai pelanggan. Model ini cukup baik dalam menjelaskan hubungan antara kedua variabel.
4. Kesimpulan
Berdasarkan hasil analisis statistik yang telah dilakukan, dapat disimpulkan bahwa data memiliki variasi yang cukup besar dengan distribusi yang cenderung tidak sepenuhnya normal. Hal ini terlihat dari hasil uji normalitas Shapiro-Wilk dan visualisasi Q-Q Plot yang menunjukkan penyimpangan dari distribusi normal.
Hasil analisis korelasi menunjukkan adanya hubungan positif antara variabel Pendapatan Tahunan (dalam Miliar IDR) dan Nilai Pelanggan (dalam Juta IDR). Hubungan ini mengindikasikan bahwa peningkatan pendapatan tahunan cenderung diikuti oleh peningkatan nilai pelanggan. Selanjutnya, analisis regresi linear sederhana memperkuat hasil korelasi dengan menunjukkan bahwa Pendapatan Tahunan memiliki pengaruh terhadap Nilai Pelanggan. Garis regresi yang terbentuk menunjukkan hubungan searah, sehingga model regresi dapat digunakan untuk menjelaskan hubungan antara kedua variabel tersebut, meskipun tidak seluruh variasi Nilai Pelanggan dapat dijelaskan oleh model.Secara keseluruhan, analisis ini memberikan wawasan bahwa Pendapatan Tahunan merupakan salah satu faktor yang berkontribusi terhadap Nilai Pelanggan, namun masih terdapat faktor lain di luar model yang juga memengaruhi variabel dependen.



















