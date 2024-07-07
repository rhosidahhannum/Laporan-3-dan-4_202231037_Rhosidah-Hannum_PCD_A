
# Deteksi Tepi dan Garis, Ekstraksi Fitur
Deteksi tepi dan garis adalah teknik-teknik penting dalam pengolahan citra digital yang bertujuan untuk mengidentifikasi dan menyoroti fitur-fitur penting dalam gambar. Kedua teknik ini digunakan dalam berbagai aplikasi seperti pengenalan objek, segmentasi citra, dan analisis medis.
### Deteksi Tepi
Tepi adalah tempat perubahan intensitas yang tajam dalam citra, biasanya terjadi pada perbatasan antara objek yang berbeda. Deteksi tepi berguna untuk menyoroti fitur-fitur penting dalam citra dan membantu dalam pengenalan serta analisis lebih lanjut.

Proses deteksi tepi biasanya melibatkan beberapa langkah berikut:

- Pengurangan Noise: Menggunakan filter untuk mengurangi noise atau gangguan dalam citra yang dapat mempengaruhi deteksi tepi.

- Kalkulasi Gradien: Menghitung gradien intensitas citra untuk mengidentifikasi area dengan perubahan intensitas yang tajam.

- Penentuan Tepi: Menggunakan thresholding untuk menentukan piksel mana yang dianggap sebagai tepi berdasarkan nilai gradiennya.

- Penghilangan Tepi Palsu: Menyaring hasil untuk menghilangkan garis tepi yang tidak signifikan atau disebabkan oleh noise.

Berikut adalah beberapa metode umum yang digunakan dalam deteksi tepi:

- **Operator Sobel**: Menggunakan kernel untuk menghitung gradien intensitas dalam arah horizontal dan vertikal. Operator ini menghasilkan citra tepi dengan ketebalan tertentu.

- **Operator Prewitt**: Mirip dengan operator Sobel, tetapi menggunakan kernel yang sedikit berbeda. Operator Prewitt juga menghitung gradien dalam arah horizontal dan vertikal.

- **Operator Roberts**: Menggunakan kernel kecil untuk menghitung gradien diagonal dalam citra. Operator ini sensitif terhadap noise tetapi menghasilkan tepi yang lebih tajam.

- **Operator Canny**: Merupakan salah satu metode deteksi tepi yang paling populer. Operator Canny melibatkan beberapa langkah, termasuk pengurangan noise, kalkulasi gradien, non-maximum suppression, dan double thresholding untuk menghasilkan tepi yang jelas dan tipis.

- **Operator Laplacian of Gaussian (LoG)**: Menggabungkan penghalusan Gaussian dengan operator Laplacian untuk mendeteksi tepi. Metode ini memperhitungkan perubahan kedua dari intensitas citra.

Deteksi tepi digunakan dalam berbagai aplikasi, antara lain:

- **Pengenalan Objek**: Membantu dalam mengidentifikasi dan mengisolasi objek dalam citra.
- **Segmentasi Citra**: Membagi citra menjadi bagian-bagian yang berbeda berdasarkan tepi objek.
- **Analisis Citra Medis**: Membantu dokter dalam menganalisis citra medis seperti MRI dan CT scan.
- **Visi Komputer**: Digunakan dalam sistem pengenalan wajah, sistem pemantauan lalu lintas, dan robotika.

Beberapa tantangan yang dihadapi dalam deteksi tepi antara lain:
- **Noise**: Noise dalam citra dapat menghasilkan tepi palsu yang mengganggu deteksi tepi yang sebenarnya.
- **Konsistensi Tepi**: Memastikan bahwa garis tepi yang terdeteksi konsisten dan tidak terputus.
- **Pengaturan Parameter**: Memilih parameter yang tepat seperti threshold untuk menghasilkan hasil yang optimal.

### Deteksi Garis
Garis adalah bentuk geometris yang bisa dilihat sebagai rangkaian piksel dengan intensitas yang konsisten dalam satu arah. Deteksi garis bertujuan untuk mengidentifikasi struktur garis dalam citra.

Proses deteksi garis biasanya melibatkan langkah-langkah berikut:
- **Pengurangan Noise**: Menggunakan filter untuk mengurangi noise dalam citra yang dapat mengganggu deteksi garis.
- **Kalkulasi Gradien**: Menghitung gradien intensitas untuk mengidentifikasi perubahan konsisten dalam satu arah.
- **Thresholding**: Menggunakan thresholding untuk menentukan piksel mana yang dianggap sebagai garis berdasarkan nilai gradiennya.
- **Transformasi Hough**: Mengubah ruang gambar ke ruang parameter dan mencari akumulasi untuk mengidentifikasi garis.

Berikut adalah beberapa metode umum yang digunakan untuk deteksi garis:

- **Transformasi Hough (Hough Transform)**: Metode ini sangat efektif untuk mendeteksi garis lurus dalam citra. Transformasi Hough mengubah ruang gambar menjadi ruang parameter, di mana setiap garis dalam gambar direpresentasikan sebagai titik dalam ruang parameter. Dengan mencari akumulasi di ruang parameter, kita dapat mengidentifikasi garis-garis yang ada dalam citra.
**Operator Deteksi Garis**:

**Operator Kirsch**: Menggunakan kernel untuk mendeteksi arah garis dalam delapan arah berbeda.

**Operator Compass**: Menggunakan serangkaian kernel untuk mendeteksi garis dalam berbagai arah.
- **Metode Berbasis Gradien**: Deteksi garis juga bisa dilakukan dengan mengidentifikasi puncak-puncak dalam peta gradien, yang menunjukkan kehadiran garis.

Deteksi garis digunakan dalam berbagai aplikasi, antara lain:

- **Pemetaan Jalan**: Mengidentifikasi garis marka jalan dalam sistem pengemudian otomatis.
- **Analisis Struktur**: Memeriksa struktur bangunan dalam citra satelit atau citra medis.
- **Pengenalan Karakter**: Membantu dalam pengenalan teks dalam citra (OCR).
- **Visi Komputer**: Digunakan dalam robotika dan sistem pengenalan visual untuk mendeteksi dan melacak garis.

### Ekstraksi Fitur
Ekstraksi fitur adalah proses untuk mengidentifikasi dan menyoroti informasi penting dari citra digital. Fitur-fitur ini dapat digunakan untuk berbagai aplikasi seperti pengenalan objek, klasifikasi citra, dan analisis medis. Proses ini melibatkan beberapa teknik yang bertujuan untuk mengubah data citra menjadi bentuk yang lebih sederhana dan lebih mudah diinterpretasikan.

Fitur dalam citra adalah karakteristik atau atribut yang dapat digunakan untuk mendeskripsikan konten citra. Fitur-fitur ini dapat berupa tepi, sudut, tekstur, atau pola tertentu. Ekstraksi fitur adalah langkah penting dalam banyak aplikasi pengolahan citra karena membantu mengurangi data yang harus diproses tanpa kehilangan informasi yang relevan.

Proses ekstraksi fitur biasanya melibatkan beberapa langkah berikut:

- **Pra-Pemrosesan**: Menggunakan teknik-teknik untuk membersihkan dan meningkatkan kualitas citra sebelum ekstraksi fitur dilakukan.
- **Deteksi Fitur**: Menggunakan algoritma untuk mengidentifikasi fitur-fitur penting dalam citra.
- **Deskripsi Fitur**: Menggunakan metode untuk mendeskripsikan fitur yang telah dideteksi dalam bentuk yang dapat digunakan oleh sistem pengolahan lebih lanjut.
- **Pengurangan Dimensi**: Menggunakan teknik untuk mengurangi jumlah fitur yang diproses tanpa kehilangan informasi penting.

Berikut adalah beberapa metode umum yang digunakan dalam ekstraksi fitur:

**Deteksi Tepi**:

- **Operator Sobel**: Menghitung gradien intensitas untuk mendeteksi tepi dalam citra.
- **Operator Canny**: Metode deteksi tepi yang kompleks yang melibatkan pengurangan noise, kalkulasi gradien, dan thresholding ganda.
**Deteksi Sudut**:

- **Detektor Harris**: Mengidentifikasi sudut dengan menghitung matriks gradien lokal dan mengevaluasi respon sudut.
- **FAST (Features from Accelerated Segment Test)**: Algoritma deteksi sudut yang cepat dan efisien.
**Deskripsi Fitur**:

- **Histogram of Oriented Gradients (HOG)**: Mendeskrepsikan citra berdasarkan distribusi gradien intensitas.
- **Scale-Invariant Feature Transform (SIFT)**: Mengidentifikasi dan mendeskripsikan fitur yang tahan terhadap skala dan rotasi.
Speeded-Up Robust Features (SURF): Alternatif lebih cepat dari SIFT untuk mendeskripsikan fitur lokal.
**Ekstraksi Tekstur**:

- **Gray-Level Co-Occurrence Matrix (GLCM)**: Menghitung statistik berdasarkan distribusi intensitas piksel tetangga.
- **Local Binary Patterns (LBP)**: Metode deskripsi tekstur yang menghitung pola biner lokal berdasarkan intensitas piksel.
**Transformasi Citra**:

- **Fourier Transform**: Menganalisis citra dalam domain frekuensi untuk mendeteksi pola periodik.
- **Wavelet Transform**: Menguraikan citra menjadi komponen yang berbeda berdasarkan skala dan lokasi.

Ekstraksi fitur digunakan dalam berbagai aplikasi, antara lain:

- **Pengenalan Wajah**: Mengidentifikasi individu berdasarkan fitur wajah yang diekstraksi dari citra.
- **Klasifikasi Citra**: Mengkategorikan citra ke dalam kelas-kelas yang berbeda berdasarkan fitur yang diekstraksi.
- **Analisis Citra Medis**: Membantu dokter dalam mendeteksi dan menganalisis kelainan dalam citra medis.
- **Visi Komputer**: Digunakan dalam robotika, sistem pengawasan, dan kendaraan otonom untuk mendeteksi dan mengenali objek.




