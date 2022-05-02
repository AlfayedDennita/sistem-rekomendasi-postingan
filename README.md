# Laporan Proyek *Machine Learning* — Muhammad Alfayed Dennita

## 1. Ulasan Proyek (*Project Overview*)

![Times Square New York](https://www.nycgo.com/images/venues/152/tripadvisortimessquare_taggeryanceyiv_5912__large.jpg)
***Times Square New York** (Sumber: nycgo.com)*

Pada saat ini, keberadaan media untuk menuangkan hasil karya atau sekadar memberikan informasi sangatlah beragam. Setiap media memiliki caranya tersendiri dalam menyajikan konten informasinya, seperti melalui teks, gambar, suara, atau video. Macam-macam bentuk media tersebut sering kali kita lihat keberadaannya di dalam kehidupan sehari-hari, baik itu secara luring (*offline*) ataupun secara daring (*online*). Misalnya, ketika di jalan sering kali kita melihat berbagai poster, spanduk, baliho, dan videotron yang masing-masing menampilkan konten informasi yang berbeda. Media-media tersebut merupakan contoh dari media yang dapat ditemukan secara luring. Sedangkan untuk media yang bersifat daring, kita bisa menemukannya melalui perangkat yang terhubung dengan jaringan internet, seperti komputer, laptop, ponsel pintar, tablet, dan lainnya. Di dalam internet akan terbagi lagi berbagai media informasi menurut jenis dan sifatnya, seperti situs web berita yang cenderung bersifat formal, media sosial yang cenderung bersifat nonformal, dan platform video yang khusus menampilkan informasi dalam bentuk video.

![Pengguna Media Digital di Seluruh Dunia pada Januari 2021](https://images.squarespace-cdn.com/content/v1/5b79011d266c077298791201/1612421461051-2IC1IMUOM1833412VYYW/Global+Digital+Overview+January+2021+DataReportal?format=1500w)
***Pengguna Media Digital di Seluruh Dunia pada Januari 2021** (Sumber: datareportal.com)*

Menurut [Hootsuite](https://www.hootsuite.com) yang dikutip oleh [DataReportal](https://datareportal.com), pada awal tahun 2021 jumlah pengguna internet di dunia telah mencapai 4,66 miliar pengguna. Dari keseluruhan populasi dunia (7,83 miliar), lebih dari setengahnya (59,5%) merupakan pengguna internet [[1]](https://datareportal.com/reports/digital-2021-global-overview-report). Jumlah pengguna internet yang sangat banyak tersebut menandakan bahwa saat ini kebutuhan akan internet sangat penting dalam mendapatkan informasi secara cepat dan sangat sulit untuk dihindari.

Banyaknya jumlah pengguna internet tersebut akhirnya dimanfaatkan oleh beberapa pihak untuk mendapatkan keuntungan. Salah satunya adalah dengan membangun media informasi berbasis daring yang dapat diakses oleh setiap orang tanpa adanya batasan jarak. Contoh media yang sudah banyak diterapkan pada saat ini adalah situs web dan aplikasi yang menampilkan berbagai jenis postingan. Media tersebut dapat mencakup berbagai bentuk konten, seperti teks, gambar, suara, dan video. Kemudahan dalam mengaplikasikan berbagai bentuk konten ke dalam satu media merupakan salah satu keunggulan media berbasis daring dibandingkan luring. Hal tersebut menyebabkan banyak pengembang media luring yang melebarkan bisnisnya ke media daring juga. Hal ini dapat dibuktikan dengan jumlah situs web aktif yang ada di internet saat ini. Menurut [Siteefy](https://siteefy.com), saat ini di internet terdapat hampir 200 juta situs web yang aktif [[2]](https://siteefy.com/how-many-websites-are-there). Hal tersebut menandakan banyak pihak yang sudah mengambil peluang dari banyaknya pengguna internet di dunia saat ini.

Namun, dari segala kemudahan dan keuntungan tersebut pastinya terdapat juga tantangan di dalamnya. Banyaknya informasi yang ada di dalam satu media membuat pengguna kesulitan untuk menemukan konten informasi yang relevan dengannya. Oleh karena itu, pengembang media juga harus bisa membangun sebuah sistem yang dapat memberikan konten informasi sesuai dengan preferensi penggunanya. Hal tersebut dilakukan untuk mencegah pengguna meninggalkan media karena sulitnya mencari konten yang menarik baginya. Jika pengguna selalu disuguhkan konten yang diinginkannya, mereka akan senang menghabiskan waktunya di dalam media tersebut sehingga pengembang media juga akan merasa senang karena media informasi miliknya dapat berguna bagi banyak orang serta menghasilkan berbagai keuntungan yang berlimpah dari media tersebut.

---

1. Simon Kemp, ["Digital 2021: Global Overview Report"](https://datareportal.com/reports/digital-2021-global-overview-report), DataReportal, Diakses tanggal 16 Oktober 2021.
2. Nick Huss, ["How Many Websites Are There in the World?"](https://siteefy.com/how-many-websites-are-there), Siteefy, Diakses tanggal 16 Oktober 2021.

## 2. Pemahaman Bisnis (*Business Understanding*)

![Ilustrasi Media Informasi Daring](https://ed.stanford.edu/sites/default/files/news_images/wineburg_getty.jpg)
***Ilustrasi Media Informasi Daring** (Sumber: ed.stanford.edu)*

Sebuah media informasi situs web yang baru saja rilis beberapa bulan menerima laporan bahwa jumlah tayangan postingan di situs web mereka mengalami penurunan yang cukup drastis. Pengguna mereka banyak beralih ke situs web kompetitor yang baru saja rilis beberapa hari. Hal ini tentu menimbulkan pertanyaan, mengapa sebagian pengguna bisa beralih ke situs web yang masih baru tersebut? Apakah situs web tersebut memiliki tampilan yang lebih menarik atau kualitas postingan yang lebih baik?

Setelah dilakukan pengusutan, ternyata penyebab utama dari penurunan jumlah tayangan postingan adalah kurangnya rasa nyaman dan buruknya pengalaman pengguna dalam menjelajahi situs web. Jika dilihat dari interaksi pengguna dengan situs web, pengguna lebih banyak mencari postingan yang ingin dilihatnya melalui kotak pencarian dibandingkan membuka postingan melalui beranda mereka. Hal tersebut menandakan bahwa menampilkan postingan acak di beranda bukanlah suatu ide yang baik, tentunya pengguna menginginkan postingan yang sesuai dengan preferensi dan minatnya.

Oleh karena itu, pengembang harus membuat sebuah fitur atau sistem baru dalam situs web mereka yang dapat memberikan daftar rekomendasi postingan yang diminati oleh penggunanya. Pengembang harus mengubah daftar postingan acak yang ditampilkan pada beranda menjadi daftar postingan yang relevan dengan masing-masing pengguna berdasarkan histori tayangannya. Selain itu, pengembang juga dapat memberikan daftar rekomendasi postingan yang diletakkan di bawah konten postingan agar ketika pengguna telah selesai melihat suatu postingan, pengguna tersebut dapat melihat postingan lainnya yang masih relevan dengan postingan yang telah dilihatnya.

### 2.1 Pernyataan Masalah (*Problem Statements*)

Berdasarkan kondisi permasalahan yang telah dijelaskan sebelumnya, pengembang harus membuat beberapa model sistem rekomendasi postingan yang dapat menjawab semua pertanyaan berikut.

1. Berdasarkan data postingan yang baru saja selesai dilihat pengguna, bagaimana membuat daftar rekomendasi postingan untuk ditempatkan di bawah konten postingan dengan metode pendekatan *content-based filtering*?
2. Berdasarkan data histori tayangan pengguna, bagaimana membuat daftar rekomendasi postingan yang belum pernah dilihat pengguna untuk ditempatkan pada beranda dengan metode pendekatan *collaborative filtering*?

### 2.2 Tujuan (*Goals*)

Dari semua pertanyaan yang telah diajukan maka dapat diketahui tujuan dari pembuatan beberapa model sistem rekomendasi postingan. Berikut adalah tujuan dari pembuatan model sistem rekomendasi postingan. 

1. Menghasilkan daftar rekomendasi postingan berdasarkan postingan yang baru saja selesai dilihat pengguna untuk ditempatkan di bawah konten postingan dengan metode pendekatan *content-based filtering*.
2. Menghasilkan daftar rekomendasi postingan berdasarkan postingan yang sering dilihat pengguna untuk ditempatkan di beranda masing-masing pengguna dengan metode pendekatan *collaborative filtering*.

### 2.3 Pernyataan Solusi (*Solution Statements*)

Berdasarkan permasalahan sebelumnya, dapat diketahui bahwa akan dibuat dua buah model sistem rekomendasi postingan dengan metode pendekatan yang berbeda, yaitu *content-based filtering* dan *collaborative filtering*. Berikut adalah penjelasan dari kedua metode pendekatan tersebut.

#### 2.3.1 *Content-Based Filtering*

*Content-based filtering* adalah suatu metode yang merekomendasikan konten (dalam kasus ini adalah postingan) dengan konten lainnya berdasarkan tingkat kesamaannya. Setiap postingan memiliki karakteristiknya masing-masing yang direpresentasikan melalui berbagai kategori dan jenis postingannya. Kategori dan jenis postingan tersebut akan menjadi acuan apakah suatu postingan relevan dengan postingan lainnya. Apabila suatu postingan memiliki karakteristik (kategori dan jenis) yang sama atau hampir sama dengan suatu postingan lainnya maka kedua postingan tersebut dapat dikatakan mirip, begitu pula dengan hal sebaliknya.

Setiap karakteristik akan direpresentasikan melalui setiap katanya sehingga apabila suatu postingan memiliki banyak kata pada kategori dan jenisnya maka postingan tersebut akan memiliki banyak karakteristik pula. Untuk menentukan kata apa saja yang harus dipertimbangkan dalam menilai tingkat kesamaan di setiap postingan, dibutuhkan suatu teknik penilaian yang dinamakan TF—IDF (Term Frequency—Inverse Document Frequency). TF—IDF akan mengukur seberapa penting suatu kata terhadap kata lainnya dalam suatu kumpulan kata. Singkatnya, TF—IDF akan memilih kata apa saja yang bisa menggambarkan suatu postingan. Penilaian TF—IDF terhadap postingan akan diskalakan dalam nilai 0—1, 0 berarti suatu kata tidak mewakili postingan dan 1 berarti suatu kata sangat mewakili postingan.

Setelah setiap postingan memiliki bobot nilai pada semua kumpulan karakteristik yang ada, langkah selanjutnya adalah menghitung tingkat kesamaan dari setiap postingan dengan metrik kesamaan kosinus (*cosine similarity*). Kesamaan kosinus akan menghitung tingkat kesamaan suatu postingan dengan postingan lainnya dan diskalakan dalam nilai 0—1, 0 berarti suatu postingan tidak memiliki kesamaan dengan postingan lainnya dan 1 berarti suatu postingan sama dengan postingan lainnya.

Daftar rekomendasi postingan akan diberikan berdasarkan tingkat kesamaan kosinus. Suatu postingan akan dicari rekomendasi postingannya berdasarkan postingan dengan tingkat kesamaan yang tinggi dengannya. Semakin banyak dua postingan memiliki kesamaan karakteristik maka akan semakin tinggi pula tingkat kesamaan kosinusnya.

#### 2.3.2 *Collaborative Filtering*

*Collaborative filtering* adalah suatu metode rekomendasi yang membutuhkan interaksi pengguna lainnya dalam menentukan daftar rekomendasi. *Collaborative filtering* dapat dibagi menjadi dua kategori, yaitu *memory based* (berbasis memori) dan *model based* (berbasis model). Dalam kasus ini yang digunakan adalah *collaborative filtering* berbasis model. Hal tersebut dipilih karena *collaborative filtering* berbasis model tetap dapat membuat daftar rekomendasi postingan untuk suatu pengguna walaupun pengguna tersebut tidak ada dalam proses pemodelan.

Model akan dibangun menggunakan teknik *embedding*. Teknik *embedding* akan menghitung kecocokan antara pengguna dengan postingan. Setelah melakukan *embedding*, langkah selanjutnya adalah melakukan perkalian *dot product* antara *embedding* pengguna dan postingan. Selain itu, bias juga akan ditambahkan untuk setiap pengguna dan postingan. Skor kecocokan akan ditentukan dalam skala 0—1 dengan fungsi aktivasi *sigmoid*.

Daftar rekomendasi postingan akan diberikan dengan melihat kecocokan antara pengguna yang satu dengan yang lainnya. Apabila suatu pengguna lebih sering melihat postingan dengan kategori olahraga maka pengguna tersebut akan diberikan daftar rekomendasi postingan yang belum dilihatnya dari pengguna lain yang sering melihat postingan dengan kategori olahraga juga.

## 3. Pemahaman Data (*Data Understanding*)

Untuk membuat model yang dapat merekomendasikan postingan kepada pengguna, tentunya membutuhkan data yang berisi informasi dari setiap postingan dan pengguna tersebut. Selain itu, data tayangan postingan juga dibutuhkan untuk mengetahui pengguna mana saja yang telah melihat suatu postingan dan postingan apa saja yang telah dilihat oleh pengguna.

![Post recommender oleh rohit96](https://drive.google.com/uc?id=1RGPa7G6eBH5Ce-LuVjl2gkcpiM09KWXd)
***Post recommender oleh rohit96** (Sumber: kaggle.com)*

Kumpulan data yang akan digunakan dalam proses pembuatan model kali ini adalah **Post recommender** yang diterbitkan oleh pengguna Kaggle dengan nama pengguna **rohit96**. Untuk melihat informasi data lebih lanjut, dapat mengunjungi tautan berikut: [Post recommender | Kaggle](https://www.kaggle.com/rohit0906/post-recommender).

Kumpulan data **Post recommender** berisi tiga data yang dibutuhkan dalam proses pembuatan model, yaitu `posts.csv` yang berisi data postingan, `users.csv` yang berisi data pengguna, dan `views.csv` yang berisi data tayangan. Berikut adalah masing-masing penjelasan ketiga data tersebut.

### 3.1 Data Postingan (`posts.csv`)

Data postingan memiliki jumlah sampel (baris) sebanyak 493 sampel dan jumlah fitur (kolom) sebanyak 4 fitur. Berikut adalah penjelasan dari masing-masing fitur pada data postingan.

1. `_id` yang diubah menjadi `post_id`, yaitu teks identifikasi unik yang dimiliki setiap postingan. Fitur ini memiliki nilai berupa teks identifikasi unik postingan dengan tipe data `string`.
2. `title`, yaitu judul postingan. Fitur ini memiliki nilai berupa judul postingan dengan tipe data `string`.
3. `category`, yaitu kumpulan kategori yang berkaitan dengan postingan dan setiap kategori dipisahkan oleh simbol pipa (`|`) atau tanda titik koma (`;`). Fitur ini memiliki nilai berupa kumpulan kategori dengan tipe data `string`.
4. `post_type` yang diubah menjadi `type`, yaitu jenis postingan. Fitur ini memiliki nilai berupa jenis postingan dengan tipe data `string`. Nilai unik yang ada pada fitur ini adalah *blog*, *artwork* (karya seni), *project* (proyek), dan *skill* (keahlian).

### 3.2 Data Pengguna (`users.csv`)

Data pengguna memiliki jumlah sampel (baris) sebanyak 118 sampel dan jumlah fitur (kolom) sebanyak 4 fitur. Berikut adalah penjelasan dari masing-masing fitur pada data pengguna.

1. `_id` yang diubah menjadi `user_id`, yaitu teks identifikasi unik yang dimiliki setiap pengguna. Fitur ini memiliki nilai berupa teks identifikasi unik pengguna dengan tipe data `string`.
2. `name`, yaitu nama pengguna. Fitur ini memiliki nilai berupa nama pengguna dengan tipe data `string`.
3. `gender`, yaitu jenis kelamin pengguna. Fitur ini memiliki nilai berupa jenis kelamin pengguna dengan tipe data `string`. Nilai unik yang ada pada fitur ini adalah *male* (laki-laki), *female* (perempuan), dan *undefined* (tidak terdefinisi).
4. `academics`, yaitu tingkat pendidikan pengguna. Fitur ini memiliki nilai berupa tingkat pendidikan pengguna dengan tipe data `string`. Nilai unik yang ada pada fitur ini adalah *undergraduate* (sarjana), *graduate* (pascasarjana), dan *undefined* (tidak terdefinisi).

### 3.3 Data Tayangan (`views.csv`)

Data tayangan memiliki jumlah sampel (baris) sebanyak 1.449 sampel dan jumlah fitur (kolom) sebanyak 3 fitur. Berikut adalah penjelasan dari masing-masing fitur pada data tayangan.

1. `user_id`, yaitu teks identifikasi unik yang dimiliki setiap pengguna. Fitur ini memiliki nilai berupa teks identifikasi unik pengguna dengan tipe data `string`.
2. `post_id`, yaitu teks identifikasi unik yang dimiliki setiap postingan. Fitur ini memiliki nilai berupa teks identifikasi unik postingan dengan tipe data `string`.
3. `timestamp`, yaitu tanggal dan jam pengguna melihat postingan. Fitur ini memiliki nilai berupa tanggal dan jam pengguna melihat postingan dengan tipe data `string` yang diubah ke `datetime`.
 
Dalam proses eksplorasi data, fitur-fitur tersebut dianalisis dan dilakukan perbaikan (bila perlu) agar memiliki nilai yang berguna dalam proses pembuatan model. Proses eksplorasi data yang dilakukan dapat diuraikan sebagai berikut.

1. Mengubah nama dan tipe data pada beberapa fitur untuk memudahkan proses pengodean. Fitur yang dilakukan pengubahan nama dan tipe datanya dapat dilihat pada penjelasan masing-masing fitur.
2. Memperbaiki nilai kosong (*missing value*) dari fitur `category` pada data postingan. Nilai kosong tersebut diisi dengan nilai *Uncategorized*.
3. Analisis dan visualisasi hubungan univariat pada masing-masing data untuk mengetahui informasi dari suatu fitur yang akan diuraikan di bawah.
4. Analisis dan visualisasi hubungan multivariat dari ketiga data untuk mengetahui informasi berbagai fitur yang akan diuraikan di bawah.

Berikut adalah hasil visualisasi hubungan univariat dan multivariat dari berbagai fitur pada setiap data beserta penjelasan analisis singkatnya.

### 3.4 Hubungan Univariat pada Data Postingan

**3.4.1 Visualisasi distribusi dari fitur `type` untuk mengetahui bagaimana persebaran jenis postingan**

![Distribusi Jenis Postingan](https://drive.google.com/uc?id=1C6wQIgjljIOSB44uUoMdNswyZ5GZ-2zH)

**Penjelasan:**

Jenis postingan didominasi oleh *artwork* (karya seni) dengan jumlah postingan sebanyak 241 (48,88%) dan blog dengan jumlah postingan sebanyak 198 (40,16%). Sisanya, jenis postingan *skill* (keahlian) dan *project* (proyek) masing-masing memiliki postingan sebanyak 27 (5,48%). Jadi, data postingan memiliki jumlah postingan yang hampir seimbang antara postingan yang cenderung non-ilmiah (karya seni dan keahlian) dengan postingan yang cenderung ilmiah (blog dan proyek).

### 3.5 Hubungan Univariat pada Data Pengguna

**3.5.1 Visualisasi ditribusi dari fitur `gender` untuk mengetahui bagaimana persebaran jenis kelamin pengguna**

![Distribusi Jenis Kelamin Pengguna](https://drive.google.com/uc?id=1wfhMmIALiwM2JrNbPTI2fm0yISLU99K4)

**Penjelasan:**

Jenis kelamin pengguna didominasi oleh *male* (laki-laki) dengan jumlah pengguna sebanyak 72 (61,02%), sedangkan jumlah pengguna *female* (perempuan) sebanyak 44 (37,29%). Selain itu, terdapat juga 2 (1,69%) pengguna yang tidak mendefinisikan jenis kelaminnya (*undefined*). Jadi, data pengguna yang lebih banyak memiliki pengguna berjenis kelamin laki-laki dibandingkan perempuan memungkinkan daftar postingan yang sering dilihat lebih banyak bersifat laki-laki, seperti tentang teknologi, musik, olahraga, dan lainnya.

**3.5.2 Visualisasi distribusi dari fitur `academics` untuk mengetahui bagaimana persebaran tingkat pendidikan pengguna**

![Distribusi Tingkat Pendidikan Pengguna](https://drive.google.com/uc?id=1_it7KWTXa7UFSAETOw5LFI7glJWIGjua)

**Penjelasan:**

Tingkat pendidikan pengguna memiliki distribusi yang hampir imbang antara *undergraduate* (sarjana) dengan *graduate* (pascasarjana). Jumlah pengguna dengan tingkat pendidikan sarjana adalah 68 (57,63%), sedangkan jumlah pengguna dengan tingkat pendidikan pascasarjana adalah 48 (40,68%). Selain itu, terdapat juga 2 (1,69%) pengguna yang tidak mendefinisikan tingkat pendidikannya (*undefined*). Jadi, data pengguna didominasi oleh pengguna yang sedang/pernah berkuliah sehingga kemungkinan daftar postingan yang sering dilihat dari pengguna berkaitan dengan ilmu-ilmu keilmiahan.

### 3.6 Hubungan Univariat pada Data Tayangan

**3.6.1 Visualisasi perbandingan antara pengguna unik dengan postingan unik untuk mengetahui tingkat ketersediaan postingan untuk pengguna**

![Perbandingan Pengguna Unik dan Postingan Unik](https://drive.google.com/uc?id=1Esnyx03eOYNeK8FQUg5JnHr2fBNAXTG3)

**Penjelasan:**

Perbandingan antara jumlah pengguna unik dengan postingan unik sangat berbeda jauh, hampir lima kali lipat. Jumlah pengguna unik pada data tayangan adalah 118, sedangkan jumlah postingan unik adalah 495. Jadi, ketersediaan postingan untuk pengguna dapat tercukupi karena banyaknya pilihan postingan untuk pengguna.

**3.6.2 Visualisasi jumlah tayangan postingan berdasarkan hari akses untuk mengetahui di hari apa pengguna banyak melihat postingan**

![Jumlah Tayangan Berdasarkan Hari Akses](https://drive.google.com/uc?id=1by11IcRX3zSsxcrS4Cfy4sYUyadLb-sh)

**Penjelasan:**

Jumlah tayangan pada postingan dari hari ke hari cukup bervariasi. Jumlah tayangan terbanyak ada di hari *Friday* (Jumat) sebanyak 263 (18,15%), sedangkan jumlah tayangan terdikit ada di hari *Wednesday* (Rabu) sebanyak 158 (10,90%). Dari jumlah tayangan tersebut dapat diketahui bahwa pengguna lebih banyak melihat postingan di hari Jumat karena hari tersebut adalah hari kerja terakhir yang memungkinkan pengguna melihat postingan setelah mereka bekerja selama hampir seminggu penuh untuk melepaskan penat. Kemudian di hari berikutnya, *Saturday* (Sabtu), intensitas tayangan postingan menjadi lebih sedikit karena pengguna sudah menghabiskan waktunya melihat banyak postingan di hari Jumat.

### 3.7 Hubungan Multivariat pada Semua Data

**3.7.1 Visualisasi pengguna yang paling banyak melihat postingan untuk mengetahui pengguna mana yang paling banyak memberikan informasi pada proses pemodelan dengan metode *collaborative filtering***

![Pengguna yang Paling Banyak Melihat Postingan](https://drive.google.com/uc?id=1l8gvdwHzzjK0Qa4Hwm7jt48Azjtoy6TM)

**Penjelasan:**

Lima pengguna teratas yang paling banyak melihat postingan adalah pengguna dengan jenis kelamin laki-laki dan sebagian besarnya memiliki tingkat pendidikan sarjana. Jadi, pada data tayangan ini laki-laki lebih aktif melihat postingan dibandingkan perempuan dan pengguna dengan tingkat pendidikan sarjana lebih aktif melihat postingan dibandingkan pascasarjana.

**3.7.2 Visualisasi postingan yang paling banyak dilihat pengguna untuk mengetahui postingan mana yang paling banyak memberikan informasi pada proses pemodelan dengan metode *collaborative filtering***

![Postingan yang Paling Banyak Dilihat Pengguna](https://drive.google.com/uc?id=13UhVbzlIPREvQrcuy_G4vD9InM7XHM6V)

**Penjelasan:**

Lima postingan teratas yang paling banyak dilihat pengguna sebagian besar merupakan postingan dengan jenis karya seni. Jadi, pada data tayangan ini pengguna lebih tertarik untuk melihat postingan berjenis karya seni dibandingkan tiga jenis postingan lainnya (blog, keahlian, dan proyek). Berarti, dugaan sebelumnya yang menyatakan pengguna akan sering melihat postingan yang bersifat ilmiah kurang tepat. Walaupun sebagian besar pengguna berada di tingkatan pendidikan tinggi, pengguna lebih banyak melihat postingan untuk mencari hiburan bagi dirinya sendiri dibandingkan untuk mencari informasi ilmu keilmiahan.

## 4. Persiapan Data (*Data Preparation*)

Data yang telah dianalisis dan dilakukan perbaikan selanjutnya akan disesuaikan kembali agar masing-masing model dapat memahami dan mengolah data tersebut. Proses persiapan data pada masing-masing metode dilakukan secara terpisah karena bentuk data yang dibutuhkan pada setiap model dari kedua metode tersebut berbeda.

### 4.1 *Content-Based Filtering*

Berikut adalah tahapan proses persiapan data dari proses pemodelan dengan metode pendekatan *content-based filtering*.

1. Membuat data baru berdasarkan data postingan. Fitur utama yang akan digunakan dalam proses pemodelan ini adalah fitur `category` dan `type` karena kedua fitur tersebut memiliki informasi yang sangat penting untuk menggambarkan karakteristik suatu postingan. Setelah itu, kedua fitur tersebut digabung menjadi fitur `keywords` karena semua kata dari kedua fitur tersebut akan dijadikan kata kunci yang menggambarkan karakteristik suatu postingan.
2. Menghilangkan semua tanda pemisah kategori yang berupa simbol pipa (`|`) dan tanda titik koma (`;`) dari fitur `keywords` yang sebelumnya menjadi tanda pemisah berbagai kategori dari fitur `category`. Hal ini dilakukan agar model dapat menghubungkan kesamaan di antara postingan melalui kata-kata penting dari fitur `keywords`.
3. Mengubah semua kata pada fitur `keywords` menjadi huruf kecil (*lower case*) agar kata yang sama namun berbeda format penulisannya tidak dianggap berbeda oleh model.
4. Menghapus semua *stop word* pada fitur `keywords`. *Stop word* adalah kata-kata umum yang sering muncul dalam jumlah besar pada teks tetapi tidak memiliki makna yang penting, seperti *a*, *the*, *of*, dan lainnya. Karena tidak memiliki makna penting dan sering muncul keberadaannya, *stop word* tidak akan menjadi karakteristik unik dari suatu postingan.
5.  Melakukan normalisasi teks berupa *lemmatization* pada fitur `keywords`. *Lemmatization* adalah proses mengubah suatu kata menjadi bentuk dasar yang bermakna dengan melibatkan konteks, contohnya seperti kata `drawings` menjadi `drawing`. Hal ini dilakukan agar kata kunci yang berbeda penulisannya namun memiliki makna yang sama tidak dianggap  berbeda oleh model.
6.  Memperbaiki kata kunci yang memiliki kesalahan penulisan secara manual dengan bantuan [Grammarly](https://grammarly.com). Grammarly adalah aplikasi pengecek serta perbaikan kata dan kalimat dalam bahasa Inggris secara otomatis sehingga kita dapat memanfaatkan aplikasi tersebut untuk melihat kata kunci apa saja yang memiliki kesalahan penulisan.
7.  Melakukan transformasi fitur `keywords` menjadi bentuk matriks TF–IDF agar nilai pada fitur tersebut dapat diolah oleh model.

### 4.2 *Collaborative Filtering*

Berikut adalah tahapan proses persiapan data dari proses pemodelan dengan metode pendekatan *collaborative filtering*.

1. Membuat data baru berdasarkan data tayangan. Fitur utama yang akan digunakan dalam proses pemodelan ini adalah fitur `user_id` dan `post_id` karena kedua fitur tersebut memberikan informasi berupa pengguna mana yang telah melihat suatu postingan dan postingan apa yang dilihatnya. Pengguna dapat melihat banyak postingan dan postingan dapat dilihat banyak pengguna.
2. Membuat fitur `total_views` yang berisi nilai seberapa banyak pengguna melihat suatu postingan. Nilai dari fitur tersebut didapatkan dari penggabungan sampel yang memiliki nilai `user_id` dan `post_id` yang sama.
3. Melakukan *encoding* pada nilai fitur `user_id` dan `post_id` menjadi nilai angka/numerik agar dapat diolah oleh model saat proses pemodelan. Hasil *encoding* tersebut selanjutnya dipetakan pada fitur baru yang bernama `user` dan `post`. Kedua fitur inilah yang akan digunakan dalam proses pemodelan bersama dengan fitur `total_views` agar model dapat mengolah nilai-nilainya.
4. Mengetahui jumlah pengguna dan postingan untuk dijadikan argumen pada model nanti.
5. Mengacak urutan sampel pada data agar persebaran sampelnya merata dan tidak menumpuk di satu pengguna.
6. Membagi data menjadi data latih dan data validasi dengan fitur `user`, `post`, dan `total_views`. Fitur yang akan menjadi data target adalah fitur `total_views`. Data latih akan diambil 80% dari data keseluruhan dan data validasi akan diambil dari sisa data keseluruhan (20%). Sebelum itu, fitur `total_views` harus dilakukan skala ulang terlebih dahulu pada nilainya menjadi skala 0–1 agar model dapat bekerja lebih baik. Setelah proses pembagian data, didapatkan jumlah data latih sebanyak 1.116 sampel dan jumlah data validasi sebanyak 279 sampel dari 1.395 sampel.

## 5. Pemodelan dan Hasil (*Modeling and Result*)

Berdasarkan pernyataaan solusi sebelumnya, proses pemodelan dibagi menjadi dua metode pendekatan, yaitu metode *content-based filtering* dan metode *collaborative filtering*. Berikut adalah penjelasan dan tahapan dalam proses pemodelan dari masing-masing metode pendekatan.

### 5.1 *Content-Based Filtering*

Pada persiapan data sebelumnya, data untuk proses pemodelan *content-based filtering* telah berhasil disesuaikan agar bisa diolah oleh model. Data tersebut berupa matriks TF–IDF yang berisi bobot semua karakteristik dari setiap postingan atau bobot kata kunci yang berkaitan dengan setiap postingan. Informasi tersebut yang akan menjadi bahan pertimbangan model dalam menentukan daftar rekomendasi postingan berdasarkan tingkat kesamaan postingan.

Pertama, model akan menghitung tingkat kesamaan dari matriks TF–IDF  menggunakan metrik kesamaan kosinus (*cosine similarity*). Semua postingan yang ada pada matriks tersebut akan dinilai kesamaannya satu sama lain berdasarkan penilaian kesamaan kosinus. Kesamaan kosinus akan mengukur kesamaan antara dua vektor dan menentukan apakah vektor tersebut menunjuk ke arah yang sama. Kesamaan kosinus akan menghitung sudut kosinus antara dua vektor, semakin kecil sudut kosinus maka akan semakin besar pula tingkat kesamaannya. Jadi, pada kasus kali ini, kesamaan kosinus akan membandingkan dua postingan berdasarkan bobot setiap kata kuncinya, semakin banyak kedua postingan memiliki kesamaaan dengan kata kunci maka akan semakin besar pula tingkat kesamaannya. Tingkat kesamaaan kosinus berada di skala nilai 0–1, 0 berarti tidak ada kesamaaan dan 1 berarti sama.

Setelah mendapatkan data tingkat kesamaan di setiap postingan dengan kesamaan kosinus, proses berikutnya adalah membuat kelas yang berfungsi untuk menampilkan daftar rekomendasi postingan. Kelas tersebut diberi nama `ContentRecommender` dan memiliki tiga pilihan keluaran, yaitu daftar rekomendasi dalam bentuk bingkai data (*data frame*) yang diakses melalui metode `frame`, daftar rekomendasi dalam bentuk teks laporan yang diakses melalui metode `text`, dan informasi postingan acuan dalam bentuk bingkai data yang diakses melalui metode `base`. Postingan yang akan dijadikan acuan untuk mencari daftar rekomendasi dapat dimasukkan melalui parameter `value` berdasarkan fitur tertentu yang ditentukan dari parameter `by`. Fitur yang diperbolehkan untuk menentukan postingan acuan adalah fitur `post_id` dan `title`. Selain itu, jumlah daftar rekomendasi dapat ditentukan melalui parameter `n` dan tingkat kesamaan kosinus akan ditampilkan atau tidak melalui parameter `metric`.

Setelah model dan kelas sudah berhasil dibuat, sekarang saatnya untuk melakukan pengujian model tersebut dengan kelas `ContentRecommender`. Dalam pengujian kali ini, model akan diuji dengan dua postingan acak yang berbeda. Kedua postingan acuan tersebut akan dicari berdasarkan fitur yang berbeda dan ditampilkan dalam bentuk yang berbeda. Berikut adalah hasil pengujian dari sistem rekomendasi dengan metode *content-based filtering*.

#### 5.1.1 Postingan Acak 1 melalui Fitur `post_id` dalam Bentuk Bingkai Data

Berikut adalah daftar rekomendasi postingan dalam bentuk bingkai data yang ditampilkan melalui metode `frame` milik kelas `ContentRecommender`.

![Daftar Rekomendasi Postingan dengan Metode Content-Based Filtering](https://drive.google.com/uc?id=1ZpJu7l3f46tq-eUiXo5OqPfNYQFJ5KDL)

Berikut adalah postingan acuan yang ditampilkan melalui metode `base` milik kelas `ContentRecommender`.

![Postingan Acuan untuk Menampilkan Daftar Rekomendasi Postingan](https://drive.google.com/uc?id=1lgZ8MC5LBhr-TduZcWF-Cb0T1Wvcyp78)

Dari kedua gambar tersebut dapat diketahui bahwa daftar rekomendasi postingan memiliki tingkat kesamaan yang bervariasi dengan postingan acuannya, mulai dari 1,00 (100%) hingga 0,31 (31%) dalam lima rekomendasi postingan teratas. Nilai rata-rata tingkat kesamaan dalam lima rekomendasi postingan teratas adalah 0,58 (58%). Postingan acuan merupakan postingan berjenis blog dan memiliki kategori pemasaran (*marketing*). Jadi, postingan yang direkomendasikan adalah postingan yang juga berjenis blog dan memiliki kategori pemasaran. Tingkat kesamaan yang bervariasi pada daftar rekomendasi tersebut dikarenakan terdapat beberapa kategori rekomendasi postingan yang tidak ada di postingan acuan sehingga tingkat kesamaannya tidak terlalu besar.

Untuk mengetahui performa model dalam memberikan postingan yang relevan, model dapat dievaluasi menggunakan metrik presisi (*precision*). Metrik tersebut akan melihat seberapa banyak model memberikan rekomendasi yang relevan dibandingkan memberikan rekomendasi yang tidak relevan. Untuk menentukan suatu postingan relevan atau tidak, kita dapat menetapkannya berdasarkan tingkat kesamaannya. Bila tingkat kesamaan suatu rekomendasi postingan di atas atau sama dengan 0,75 (>= 75%) maka postingan tersebut dapat dikatakan relevan dengan postingan acuan, begitu pun sebaliknya. Jadi, dari lima rekomendasi postingan tersebut dapat diketahui bahwa dua postingan teratas merupakan postingan relevan dan tiga sisanya merupakan postingan tidak relevan sehingga nilai presisinya adalah (2 / [2 + 3]) = 0,4 (40%).


#### 5.1.2 Postingan Acak 2 melalui Fitur `title` dalam Bentuk Teks Laporan

Berikut adalah teks laporan yang berisi informasi postingan acuan dan daftar rekomendasi postingan yang ditampilkan melalui metode `text` milik kelas `ContentRecommender`.

![Daftar Rekomendasi Postingan dengan Metode Content-Based Filtering](https://drive.google.com/uc?id=1Gi1tXPyTuJPPq2eMjAK7laQPYHH7PcqF)

Dari gambar tersebut dapat diketahui bahwa semua daftar rekomendasi postingan memiliki tingkat kesamaan 100% dengan postingan acuannya. Postingan acuan merupakan postingan berjenis karya seni (*artwork*) dengan kategori menggambar (*drawings*). Jadi, postingan yang direkomendasikan adalah postingan yang juga berjenis karya seni dengan kategori menggambar. Setiap postingan rekomendasi memiliki kategori yang juga dimiliki oleh postingan acuan sehingga rata-rata tingkat kesamaannya mencapai 100%.

Karena semua rekomendasi postingan merupakan postingan yang relevan (tingkat kesamaannya di atas atau sama dengan 75%), dapat disimpulkan bahwa model dalam memberikan rekomendasi postingan berdasarkan postingan acuan ke-2 memiliki nilai presisi sebesar (5 / [5 + 0]) = 1,0 (100%).

### 5.2 *Collaborative Filtering*

Pada tahap ini, model untuk membuat sistem rekomendasi postingan dengan metode *collaborative filtering* akan dipersiapkan. Model tersebut akan dibuat dengan pustaka Keras dan diberi nama `RecommenderNet`. Model akan menghitung skor kecocokan antara pengguna dengan postingan melalui teknik *embedding*. Pertama, model akan melakukan proses *embedding* terhadap data pengguna dan postingan. Selanjutnya, model akan melakukan operasi perkalian *dot product* antara *embedding* pengguna dan postingan. Terakhir, model akan menambahkan bias untuk setiap pengguna atau postingan. Skor kecocokan akan ditentukan dalam skala 0–1 dengan fungsi aktivasi *sigmoid*.

Setelah selesai mempersiapkan kelas model, langkah selanjutnya adalah melakukan *compile* pada model dengan memberikan argumen berupa jumlah pengguna unik pada data tayangan, jumlah postingan unik pada data tayangan, dan ukuran *embedding*. Metrik yang digunakan untuk mengukur kualitas model adalah metrik RMSE (Root Mean Squared Error).

Berikutnya, model akan dilakukan pelatihan dengan menggunakan *callback*. Model akan berhenti melakukan pelatihan apabila nilai dari metrik RMSE pada data validasi sudah lebih kecil dari 0,1. Nilai kesalahan RMSE tersebut sudah cukup baik untuk memberikan daftar rekomendasi postingan.

Setelah model selesai melakukan pelatihan, langkah selanjutnya hampir sama seperti pada pemodelan dengan teknik *content-based filtering*, yaitu membuat kelas yang berfungsi untuk menampilkan keluaran dalam bentuk bingkai data ataupun teks laporan. Kelas tersebut diberi nama `CollaborativeRecommender` dan memiliki tiga pilihan keluaran, yaitu daftar rekomendasi dalam bentuk bingkai data yang diakses melalui metode `frame`, daftar rekomendasi dalam bentuk teks laporan yang diakses melalui metode `text`, dan daftar postingan yang sering dilihat pengguna dalam bingkai data yang diakses melalui metode `most_viewed`. Pengguna yang akan diberikan daftar rekomendasi dapat dimasukkan melalui nilai dari fitur `user_id` di parameter `user_id` dan jumlah rekomendasi postingan dapat ditentukan melalui parameter `n`.

Setelah model dan kelas sudah berhasil dibuat, langkah berikutnya adalah melakukan evaluasi model dengan melakukan visualisasi nilai metrik RMSE dan melihat daftar rekomendasi postingan berdasarkan postingan yang sering dilihat pengguna. Untuk menguji hasil rekomendasi postingan, model cukup diuji dengan satu sampel saja dengan bentuk keluaran yang berbeda.

Berikut adalah visualisasi dari nilai metrik RMSE pada pelatihan model dalam 22 epoch.

![Visualisasi Nilai Metrik RMSE](https://drive.google.com/uc?id=1rFlp5seeYm2zOqh5Xm_1qXxJEKob2oQb)

Berdasarkan visualisasi tersebut, nilai RMSE dari epoch pertama hingga epoch ke-22 mengalami penurunan yang cukup baik. Nilai RMSE pada data latih di epoch terakhir adalah 0,0602 dan nilai RMSE pada data validasi adalah 0,0981. Nilai dengan angka tersebut menunjukkan bahwa model dapat memberikan daftar rekomendasi dengan kesalahan yang sangat kecil, bahkan tidak lebih 0,1.

Berikut adalah daftar rekomendasi postingan dalam bentuk bingkai data yang ditampilkan melalui metode `frame` milik kelas `CollaborativeRecommender`.

![Daftar Rekomendasi Postingan dengan Metode Collaborative Filtering](https://drive.google.com/uc?id=1G8G1Mcr7pl7SNz0fwMRHHnKG2NSoz9Wc)

Berikut adalah daftar postingan yang sering dilihat pengguna dalam bentuk bingkai data yang ditampilkan melalui metode `most_viewed` milik kelas `CollaborativeRecommender`.

![Daftar Postingan yang Sering Dilihat Pengguna](https://drive.google.com/uc?id=1u_-OKzgbyZgvZzJQ2TaHRS7olFLNWlci)

Berikut adalah daftar rekomendasi postingan beserta daftar postingan yang sering dilihat pengguna dalam bentuk teks laporan yang ditampilkan melalui metode `text` milik kelas `CollaborativeRecommender`.

![Daftar Rekomendasi Postingan dengan Metode Collaborative Filtering](https://drive.google.com/uc?id=1FmtPsEhRSPSVz8mBNiirh4xwPTPDsudE)

Berdasarkan ketiga gambar tersebut, daftar rekomendasi postingan untuk pengguna dibandingkan dengan postingan yang sering dilihatnya memiliki kesamaan yang relevan. Postingan yang sering dilihat pengguna adalah postingan berjenis karya seni dan blog, sedangkan postingan yang direkomendasikan juga postingan berjenis karya seni dan blog. Jadi, dapat diketahui bahwa model telah berhasil memberikan daftar rekomendasi postingan yang cukup relevan kepada pengguna tertentu berdasarkan histori tayangan postingan.

## 6. Evaluasi (*Evaluation*)

Metrik evaluasi yang digunakan pada setiap metode pendekatan berbeda-beda. Model dengan metode *content-based filtering* menggunakan metrik presisi (*precision*) untuk mengetahui seberapa tepat model memberikan daftar rekomendasi yang relevan, sedangkan model dengan metode *collaborative filtering* menggunakan metrik RMSE (Root Mean Squared Error) untuk mengetahui seberapa besar kesalahan model dalam memberikan daftar rekomendasi postingan. Untuk lebih jelasnya, berikut adalah penjelasan dari masing-masing metrik tersebut.

### 6.1 Presisi (*Precision*)

Presisi adalah metrik yang menilai seberapa baik model dalam memberikan prediksi atau rekomendasi yang bersifat positif benar (*true positive*) dibandingkan positif salah (*false positive*). Ketika suatu data diklasifikasikan sebagai positif, metrik ini akan menilai seberapa presisi model dalam memprediksi atau memberi rekomendasi data yang diklasifikasikan positif tersebut.

Kelebihan metrik ini adalah sangat cocok digunakan bila mengharapkan model menghasilkan nilai positif benar dan sangat tidak mengharapkan model menghasilkan positif salah. Namun, kelemahan metrik ini adalah tidak cocok digunakan apabila ingin melakukan evaluasi pada nilai negatif, entah itu negatif benar atau negatif salah.

Pada kasus kali ini, metrik presisi akan menilai model berdasarkan tingkat kesamaan kosinus suatu rekomendasi postingan terhadap postingan acuan. Postingan akan diklasifikasikan sebagai postingan yang relevan (positif benar) bila tingkat kesamaannya lebih besar atau sama dengan 0,75 (>= 75%) terhadap postingan acuan, begitu pun sebaliknya. Persentase dengan nilai di atas 75% tersebut sudah tepat untuk mengklasifikasikan bahwa suatu rekomendasi postingan relevan dengan postingan acuan karena 3/4 karakteristik rekomendasi postingan yang juga dimiliki dengan postingan acuan sudah cukup untuk menggambarkan bahwa kedua postingan serupa. Setelah sudah mengetahui postingan yang relevan dan tidak relevan, kita dapat menghitung nilai presisinya secara manual berdasarkan formula **(Positif Benar / [Positif Benar + Positif Salah])** atau **(Postingan Relevan / [Postingan Relevan + Postingan Tidak Relevan])**.

Dari pengujian model sebelumnya, pada postingan pertama nilai presisi dari model adalah 0,4 (40%) karena model memberikan 2 rekomendasi postingan relevan dan 3 rekomendasi tidak relevan, **(2 / [2 + 3]) = 0,4 (40%)**. Sementara itu, pada postingan kedua nilai presisi dari model adalah 1,0 (100%) karena model memberikan daftar rekomendasi postingan yang semuanya relevan, **(5 / [5 + 0]) = 1,0 (100%)**. Kedua pengujian tersebut menghasilkan nilai presisi yang berbeda dikarenakan berbedanya jumlah karakteristik pada kedua postingan. Postingan pertama memiliki karakteristik yang cukup banyak sehingga sulit untuk menemukan postingan yang serupa dengannya. Karena cukup sulit menemukan postingan yang serupa, model hanya mampu memberikan postingan yang setidaknya hampir relevan walaupun diklasifikasikan tidak relevan. Sementara itu, postingan kedua memiliki karakteristik yang lebih sedikit sehingga model lebih mudah menemukan postingan yang serupa. Selain itu, ketersediaan postingan juga berpengaruh pada performa model. Semakin banyak postingan dengan karakteristik yang beragam maka akan semakin mudah pula model menemukan postingan yang relevan.

Dalam Python, metrik presisi dapat digunakan melalui pustaka scikit-learn bagian *metrics*. Untuk lebih detailnya dapat mengunjungi tautan berikut: [sklearn.metrics.precision_score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.precision_score.html). Namun, pada kasus kali ini model tidak dievaluasi menggunakan pustaka tersebut, model hanya dievaluasi dengan pengamatan manual berdasarkan tingkat kesamaan kosinus.

### 6.2 RMSE (Root Mean Squared Error)

Root Mean Squared Error adalah metrik untuk mengukur seberapa jauh hasil prediksi atau rekomendasi dari yang sebenarnya. Semakin kecil nilai RMSE maka akan semakin kecil pula kesalahan prediksi atau rekomendasi suatu model. RMSE dihitung dengan cara melakukan kuadrat pada kesalahan (selisih antara nilai prediksi dan nilai sebenarnya), kemudian mencari rata-ratanya dengan menjumlahkan kesalahan kuadrat, lalu dibagi dengan jumlah data. Terakhir, dilakukan operasi akar agar satuan dari RMSE sama dengan satuan nilai sebenarnya. Secara matematis, rumus RMSE dapat dituliskan seperti berikut.

![Rumus Root Mean Squared Error](https://media.geeksforgeeks.org/wp-content/uploads/20200622171741/RMSE1.jpg)
***Rumus Root Mean Squared Error** (Sumber: geeksforgeeks.org)*

Metrik RMSE cocok digunakan pada model yang bersifat regresi dan memiliki kemudahan dalam perhitungan serta penggunaannya. Namun, kelemahannya adalah RMSE cenderung menonjolkan deviasi yang besar karena adanya pengkuadratan.

Pada kasus kali ini, RMSE digunakan untuk mengetahui seberapa jauh model dalam memberikan daftar rekomendasi postingan dari yang sebenarnya. Dari hasil visualisasi RMSE sebelumnya, dapat diketahui bahwa nilai RMSE pada data latih adalah 0,0602 dan pada data validasi adalah 0,0981. Nilai RMSE yang sangat kecil tersebut menunjukkan bahwa model dapat memberikan daftar rekomendasi dengan kesalahan yang kecil.

Pada pemodelan sebelumnya, metrik RMSE ditentukan sebelum model melakukan *compile* dengan cara mengisi argumen `metrics` dengan pustaka RMSE yang tersedia melalui Keras. Kunjungi tautan berikut untuk mengetahui lebih lanjut: [tf.keras.metrics.RootMeanSquaredError](https://www.tensorflow.org/api_docs/python/tf/keras/metrics/RootMeanSquaredError).

## 7. Kesimpulan (*Conclusion*)

Dari serangkaian proses yang cukup panjang, akhirnya sistem rekomendasi postingan telah selesai dibuat. Sistem rekomendasi dibuat dalam dua metode pendekatan yang berbeda, yaitu *content-based filtering* dan *collaborative filtering*. Metode *content-based filtering* digunakan untuk mendapatkan daftar rekomendasi postingan berdasarkan karakteristik (kategori dan jenis) suatu postingan. Sementara itu, *collaborative filtering* digunakan untuk mendapatkan daftar rekomendasi postingan berdasarkan histori tayangan pengguna.

Kedua model memiliki kualitas yang cukup baik dalam memberikan daftar rekomendasi sehingga sudah siap untuk digunakan. Untuk mendukung model tersebut dapat bekerja lebih baik ke depannya, diharapkan ketiga data yang ada (postingan, pengguna, dan tayangan) bisa lebih berkembang sehingga memiliki informasi yang lebih banyak lagi dari saat ini. Dengan banyaknya informasi pada data, diharapkan model dapat memberikan daftar rekomendasi yang lebih relevan ke depannya.

Untuk menutup laporan ini, akan disajikan ringkasan pembuatan sistem rekomendasi postingan dari awal hingga selesai dalam bentuk diagram alir berikut.

![Ringkasan Pembuatan Sistem Rekomendasi Postingan](https://drive.google.com/uc?id=13BHnf2QWG2-QU2zY3XW5Lzd6w113g_78)

**——— Akhir Laporan ———**