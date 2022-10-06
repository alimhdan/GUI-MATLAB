# PANDUAN PENGGUNAAN APLIKASI GUI MATLAB

GUI MATLAB UNTUK CLUSTERING KEMISKINAN DI PROVINSI JAWA TENGAH MENGGUNAKAN HIERARCHICAL AGGLOMERATIVE CLUSTERING DAN OPTIMASI CALINSKI-HARABSZ PSEUDO F-STATISTICS

Deskripsi Aplikasi
GUI MATLAB untuk Clustering Kemiskinan di Provinsi Jawa Tengah Menggunakan Hierarchical Agglomerative Clustering dan Optimasi Calinski-Harabsz Pseudo F-Statistics merupakan aplikasi GUI MATLAB yang disusun untuk membantu penelitian dalam pengelompokan kabupaten/kota di Provinsi Jawa Tengah berdasarkan indikator kemiskinan menggunakan metode Hierarchical Agglomerative Clustering. Adapaun data yang digunakan dalam penelitian ini adalah data indikator kemiskinan hasil Survei Sosial Ekonomi Nasional (SUSENAS) tahun 2020 di Provinsi Jawa Tengah per kabupaten/kota (Mustafidah, 2017). Berikut disajikan rincian variabel yang digunakan dalam penelitian ini:

− Persentase rumah tangga yang dinding bangunan tempat tinggal terluasnya terbuat dari kayu (X1)

− Persentase rumah tangga yang jenis lantai bangunan tempat tinggalnya terbuat dari tanah (X2)

− Persentase rumah tangga yang luas lantai bangunan tempat tinggalnya ≤ 7,2 m2 (X3)

− Persentase rumah tangga yang sumber air minumnya dari sumur tak terlindung/mata air terlindungi/tak terlindungi (X4)

− Persentase rumah tangga tidak mempunyai fasilitas tempat buang air besar/bersifat umum (X5)

− Persentase rumah tangga yang sumber penerangan utamanya bukan listrik (X6)

− Persentase rumah tangga yang jenis atap terluasnya ijuk/daun/lainnya (X7)

− Persentase pengeluaran per kapita per bulan rumah tangga miskin untuk komoditi makanan (X8)

− Persentase penduduk miskin usia 15 tahun ke atas menurut kabupaten/kota yang belum/tidak tamat SD (X9)

Aplikasi ini dilengkapi dengan beberapa metode pengukuran jarak seperti Single Linkage, Complete Linkage, Average Linkage, Centroid, dan Ward yang dapat digunakan sebagai pemilihan metode pengukuran jarak terdekat pada saat melakukan clustering. Aplikasi ini juga mampu melakukan pemilihan jumlah cluster optimal dengan menggunakan nilai Pseudo F-Statistics. Nilai Pseudo F-Statistics tersebut berasal dari perhitungan sebuah metode yang disebut sebagai metode Calinski-Harabsz Pseudo F-Statistics. Metode Calinski-Harabsz Pseudo F-Statistics mampu menemukan jumlah cluster optimal yang merupakan cluster dengan
tingkat homogenitas yang tinggi antar anggota dalam cluster tersebut dan heterogenitas yang tinggi antar cluster yang terbentuk.
Langkah Pendahuluan Sebelum Menggunakan Aplikasi
Berikut merupakan langkah pendahuluan yang harus dilakukan sebelum menggunakan aplikasi ini:
1. Memasang software MATLAB
Pembuatan GUI MATLAB ini menggunakan software MATLAB 2009a sehingga diharapkan pengguna lain melakukan running program menggunakan versi yang sama agar tidak terjadi error pada beberapa kode yang telah dibuat.
2. Persiapan data
Data yang perlu dipersiapkan adalah data indikator dan wilayah (opsional) dalam format excel ‘.xlsx’.

Langkah-Langkah Penggunaan Aplikasi
1. Persiapkan data variabel yang akan digunakan dalam bentuk ‘.xlsx’. Isikan data tanpa nama variabel seperti contoh ilustrasi berikut (data penelitian yang digunakan di sini disimpan dengan nama HIBAHFSM). Gunakan 2 sheet dengan sheet 1 berisi data indikator dan sheet 2 lembar kosong (tidak ada tulisan apa-apa).

![image](https://user-images.githubusercontent.com/102334577/194223020-6efe7a45-8630-403e-a054-1d81e25e0121.png)

2. Buka aplikasi GUI MATLAB lalu jalankan aplikasi tersebut.

![image](https://user-images.githubusercontent.com/102334577/194222145-c34c6639-05c3-40b4-bbc5-245ea9b994d0.png)

3. Jalankan aplikasi tersebut dengan cara klik ‘Run Figure’.

![image](https://user-images.githubusercontent.com/102334577/194222961-25992b2d-a48e-4dda-8637-423f0aa5aaf7.png)

4. Berikut merupakan tampilan awal dari aplikasi GUI MATLAB-nya.

![image](https://user-images.githubusercontent.com/102334577/194222941-b6c64e44-1e4e-430b-a2a0-6c07338d0476.png)

5. Lakukan input variabel dengan cara klik ‘Variabel’. Lalu pilih data variabel yang digunakan. Setelah data terinput maka data akan ditampilkan pada Tabel Tampilan Data:

![image](https://user-images.githubusercontent.com/102334577/194222920-d22a9cd8-5c10-4ad8-9102-dfd0f4a87065.png)

6. Lakukan standardisasi data jika data memiliki satuan yang berbeda (Pada penelitian ini data yang digunakan memiliki satuan yang sama sehingga tidak dilakukan standardisasi).

![image](https://user-images.githubusercontent.com/102334577/194222890-0bfec7f2-7245-4137-a855-2d751449ab67.png)

7. Lakukan uji asumsi terhadap data yang digunakan dengan cara klik ‘Cek Asumsi’ maka akan muncul hasil dari uji asumsi seperti ilustrasi di bawah ini:

![image](https://user-images.githubusercontent.com/102334577/194222862-347766b3-a589-4e09-aa88-225310af6374.png)

8. Setelah semua asumsi terpenuhi maka dapat dilakukan clustering dengan cara sebagai berikut:
a) Pilih metode penentuan jarak terdekat yang diinginkan (Metode yang dapat dipilih adalah Single Linkage, Complete Linkage, Average Linkage, Centroid, dan Ward).

![image](https://user-images.githubusercontent.com/102334577/194222793-3d9d1f43-8fb0-4efb-b1a0-9d67ae3dcc99.png)

b) Isikan jumlah cluster yang ingin dibentuk, lalu klik ‘Cek Hasil’.

![image](https://user-images.githubusercontent.com/102334577/194222756-a6e27897-a82a-46cf-a954-b26ae9f531ff.png)

   Berikut merupakan hasil clustering yang telah terbentuk:

![image](https://user-images.githubusercontent.com/102334577/194222718-9ec242fb-8e15-400f-85d3-dba40eeac4fd.png)

   Hasil yang ditunjukkan pada GUI MATLAB ini meliputi dendogram, nilai Pseudo F-Statistics, dan hasil clustering.
9. Lakukan beberapa kali pengujian dengan menggunakan jumlah cluster yang berbeda. Kemudian bandingan nilai Pseudo F-Statistic-nya. Jumlah cluster optimal yang dipilih adalah cluster yang memiliki nilai Pseudo F-Statistic tertinggi.
10. Hasil clustering yang telah diolah menggunakan GUI MATLAB telah di-setting secara otomatis tersimpan dalam file excel (HIBAHFSM.xlsx).
Hasil clustering akan tersimpan di kolom K dalam sheet 1 (jika data tanpa standardisasi).

![image](https://user-images.githubusercontent.com/102334577/194222645-8b3bb4fe-17bf-4387-b3eb-3259e53a6482.png)

Hasil clustering akan tersimpan di kolom J dalam sheet 2 (jika data distandardisasi). Selain itu, dalam sheet 2 juga otomatis menyimpan data standardisasi dari masing-masing variabel yang disimpan pada kolom A-I.

![image](https://user-images.githubusercontent.com/102334577/194222669-dac31072-7bd9-4194-a1d9-fad7b616dee8.png)

11. Berikut disajikan ilustrasi tampilan keseluruhan dari hasil pengolahan menggunakan GUI MATLAB.

![image](https://user-images.githubusercontent.com/102334577/194222608-2e58a149-401b-4dd6-9840-ea3db82b0186.png)

12. Tutup aplikasi GUI MATLAB dengan cara klik ‘Close’ pada tanda silang seperti ilustrasi di bawah ini:

![image](https://user-images.githubusercontent.com/102334577/194222577-79ab6f2f-b82b-473c-ab8c-a1fef72f0bbd.png)
