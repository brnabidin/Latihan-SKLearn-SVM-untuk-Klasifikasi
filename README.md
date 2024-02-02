# Latihan-SKLearn-SVM-untuk-Klasifikasi

**Tahapan Latihan**

Dataset berisi 8 kolom atribut dan 1 kolom label yang berisi 2 kelas yaitu 1 dan 0. Angka 1 menandakan bahwa orang tersebut positif diabetes dan 0 menandakan sebaliknya. Terdapat 768 sampel yang merupakan 768 pasien perempuan keturunan suku Indian Pima.

Model machine learning yang akan kita buat bertujuan untuk mengklasifikasikan apakah seorang pasien positif diabetes atau tidak.

**Tahapan latihan kali ini adalah:**

- Ubah data ke dalam Dataframe.

- Bagi dataset.

- Lakukan standarisasi.

- Buat dan latih model.

- Evaluasi model.


# Codelab

Tahap pertama yang perlu kita lakukan adalah mengunduh dataset Pima Indian Diabetes dari tautan "https://www.kaggle.com/uciml/pima-indians-diabetes-database" berikut. Setelah mengunduh dataset, jangan lupa masukkan dataset ke dalam Google Colab. 

Pada tahap selanjutnya kita akan mengimpor library pandas dan mengubah dataset menjadi sebuah dataframe.

Jika Anda menggunakan Colaboratory, dataset yang telah berhasil diunggah ke Colab akan tampil sebagai berikut.

<img width="289" alt="20200430215018bf3f7541959b7e2e5744f87170d17302" src="https://github.com/brnabidin/Latihan-SKLearn-SVM-untuk-Klasifikasi/assets/67081096/8bdae3b7-52e4-453d-b574-27ce73a435fa">

Kemudian, impor library pandas dan ubah file csv menjadi dataframe dengan code berikut.

![1](https://github.com/brnabidin/Latihan-SKLearn-SVM-untuk-Klasifikasi/assets/67081096/a1c6663a-0090-4238-8520-856766406dcc)

Lalu kita tampilkan 5 baris teratas dari dataframe untuk melihat isi dari dataset. Untuk melakukannya kita dapat menjalankan kode df.head() seperti di bawah.

![2](https://github.com/brnabidin/Latihan-SKLearn-SVM-untuk-Klasifikasi/assets/67081096/32be3f7b-6ecc-44d0-bd92-e78e3ec261b3)

<img width="397" alt="202004302153042e9a31f72bc888ba288b079bda6f3663" src="https://github.com/brnabidin/Latihan-SKLearn-SVM-untuk-Klasifikasi/assets/67081096/4939a4d8-fcf4-4f21-861c-58f7b789f012">

Hal paling penting selanjutnya adalah kita perlu mengecek apakah terdapat nilai-nilai yang hilang pada dataset serta apakah ada atribut yang bukan berisi bilangan numerik. Kita bisa melakukan ini dengan memanggil fungsi .info() pada dataframe.

![3](https://github.com/brnabidin/Latihan-SKLearn-SVM-untuk-Klasifikasi/assets/67081096/5dcf4502-6118-48d8-8aee-cd7c593039dd)

<img width="397" alt="2020043021540468d55498f34c239c16e337cb9d7b3bdd" src="https://github.com/brnabidin/Latihan-SKLearn-SVM-untuk-Klasifikasi/assets/67081096/0c68c433-97e8-4d41-874c-afbcc53814f1">

Output dari fungsi info() menunjukkan bahwa semua atribut nilainya lengkap, dan juga nilai-nilai dari tiap kolom memiliki tipe data numerik yaitu int64 dan float64.

Pada tahap ini data sudah bisa dipakai untuk pelatihan model.

Kita lalu memisahkan antara atribut dan label pada dataframe. Untuk memisahkan kolom-kolom pada dataframe kamu bisa melihat dokumentasinya pada tautan "https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html" ini.

![4](https://github.com/brnabidin/Latihan-SKLearn-SVM-untuk-Klasifikasi/assets/67081096/b1918670-e9d6-4fcc-b32b-64831c7f8f35)

Jika kita lihat, nilai-nilai pada dataset memiliki skala yang berbeda. Contohnya pada kolom Glucose dan kolom Diabetes Pedigree Function. Kita perlu mengubah nilai-nilai dari setiap atribut berada pada skala yang sama. Kita dapat mencoba menggunakan standarisasi dengan fungsi StandardScaler() dari SKLearn.

![5](https://github.com/brnabidin/Latihan-SKLearn-SVM-untuk-Klasifikasi/assets/67081096/436453d7-7e0b-4345-915f-b520aa066d8d)

Setelah atribut dan label dipisah, kita bisa memisahkan data untuk training dan testing menggunakan fungsi .train_test_split().

![6](https://github.com/brnabidin/Latihan-SKLearn-SVM-untuk-Klasifikasi/assets/67081096/c018993e-691e-480d-bc6c-5f71d68e2fc7)

Kita kemudian membuat objek Support Vector Classifier dan menampungnya pada variabel clf. Akhirnya kita sampai pada tahapan yang kita tunggu-tunggu, kita memanggil fungsi fit untuk melatih model.

![7](https://github.com/brnabidin/Latihan-SKLearn-SVM-untuk-Klasifikasi/assets/67081096/3ec9f6ac-e74d-41e2-9a88-43a81b57040f)

Terakhir, kita bisa melihat bagaimana akurasi prediksi dari model yang kita latih terhadap data testing.

![8](https://github.com/brnabidin/Latihan-SKLearn-SVM-untuk-Klasifikasi/assets/67081096/33c9a13e-0a44-4644-b843-510440839028)

![20200430220814d41d434f0c8262bf11d287dc3f2daee4](https://github.com/brnabidin/Latihan-SKLearn-SVM-untuk-Klasifikasi/assets/67081096/902e93d8-6cbd-43ed-81d8-c7216d961310)

Selamat, Anda telah berhasil mengembangkan sebuah model Support Vector Classifier untuk mendeteksi diabetes.
