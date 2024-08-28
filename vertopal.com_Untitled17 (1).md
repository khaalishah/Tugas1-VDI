---
jupyter:
  colab:
  kernelspec:
    display_name: Python 3
    name: python3
  language_info:
    name: python
  nbformat: 4
  nbformat_minor: 0
---

::: {.cell .markdown id="WS_R8-pcfcUL"}
**Tugas 1 Visualisasi Data dan Informasi**

> > Nama : Khaalishah Zuhrah Alyaa V.
> >
> > NIM : 122450034
:::

::: {.cell .markdown id="dXAlCxUlX9GX"}
# **Membuat visualisasi data menjadi lebih efisien dan efektif**
:::

::: {.cell .markdown id="SZiw3EHqXzFa"}
Visualisasi data, yang mengubah data abstrak menjadi visi fisik
(misalnya, panjang, posisi, bentuk, warna, dan dan sebagainya), adalah
cara yang ampuh untuk menyajikan cerita yang menarik dari yang menarik
dari data kepada manusia yang lebih berorientasi pada visual. Saat ini,
semua organisasi memiliki lebih banyak data daripada sebelumnya.
Akibatnya, semakin banyak organisasi yang menggunakan data dan analitik
tingkat lanjut untuk menginformasikan keputusan strategis dan
operasional. Visualisasi data sangat cocok untuk memberikan gambaran
yang baik gambaran umum yang baik tentang data yang sangat besar, dan
membuatnya lebih mudah untuk ditafsirkan.
:::

::: {.cell .markdown id="kozTPS6nXTj0"}
Perkembangan Visualisasi Data Tidak diragukan lagi, visualisasi data
telah membuat langkah besar di banyak bidang, yang dikontribusikan oleh
banyak komunitas. Komunitas grafik komputer telah secara signifikan
memajukan teknologi rendering visualisasi yang indah namun dapat
ditafsirkan sendiri menggunakan, misalnya, D3. Komunitas visualisasi
memudahkan pengguna untuk menentukan dan berinteraksi dengan
visualisasi, seperti D3, VegaLite, VizQL, Tableau, dan Microsoft Power
BI.
:::

::: {.cell .markdown id="GPeCcZBpYRCf"}
1.  Impor data: mengambil data yang diperlukan dari sumber data yang
    diinginkan sumber data yang diinginkan.
2.  Persiapan data: mempersiapkan data yang diimpor untuk visualisasi,
    misalnya, menormalkan nilai, mengoreksi entri yang salah, dan
    menginterpolasi nilai yang hilang.
3.  Manipulasi data: memilih data yang akan divisualisasikan (alias
    penyaringan dari komunitas visualisasi) dan mungkin dengan operasi
    umum lainnya seperti penggabungan dan pengelompokan.
4.  Pemetaan: memetakan data yang diperoleh dari proses di atas proses
    di atas ke primitif geometris (misalnya, titik dan garis), bersama
    dengan atributnya (misalnya, warna, posisi, dan ukuran).
5.  Rendering: mengubah data geometris di atas menjadi representasi
    visual. Berdasarkan pipeline tersebut, kami telah mengidentifikasi
    tiga arah yang membuat visualisasi data lebih efisien dan efektif,
    namun relevan bagi para peneliti basis data.

\(1\) Spesifikasi Visualisasi Spesifikasi visualisasi menyediakan
berbagai cara agar pengguna dapat menentukan apa yang mereka inginkan.
Ada banyak sekali penelitian dari komunitas visualisasi dan database
tentang spesifikasi visualisasi. Kami memasukkannya dalam survei ini
untuk dua alasan:

-   Kelengkapan diri: Penting bagi pembaca untuk mengetahui cara
    menghasilkan visualisasi data.
-   Perspektif desain bahasa: Hal ini terutama melayani komponen
    "Pemetaan" dari pipeline.

\(2\) Pendekatan yang Efisien untuk Visualisasi Data

Untuk melibatkan pengguna secara efektif
:::

::: {.cell .markdown id="GM5C2cZNYtfm"}
# **2. Spesifikasi visualisasi** {#2-spesifikasi-visualisasi}

> > **2.1 Spesifikasi visualisasi data**
> >
> > Secara umum, bahasa visualisasi data terdiri dari tiga bagian: data,
> > tanda (atau isyarat visual), dan pemetaan pemetaan di antara mereka.

-   Data
-   Catatan: data yang perlu divisualisasikan.
-   Transformasi: operasi-operasi-seperti group, bin, filter, dan
    sortir-digunakan untuk mengubah catatan data.
-   Tanda (atau petunjuk visual)
-   Jenis: representasi visual untuk catatan data, seperti seperti
    batang, garis, atau titik.
-   Ukuran: lebar, tinggi visualisasi.
-   Legenda: informasi legenda.
-   Lain-lain: properti lain, seperti lebar dan warna batang.
-   Pemetaan: memetakan data ke tanda yang sesuai. Operasi visual
    berbasis GUI biasanya diterjemahkan ke dalam bahasa visualisasi data

**2.2 Kategorisasi bahasa visualisasi data**

> > Strategi yang umum digunakan untuk mengkategorikan visualisasi data
> > visualisasi data didasarkan pada ekspresifitasnya,
> >
> > **Bahasa Tingkat Rendah** Kami mengacu pada bahasa tingkat rendah
> > sebagai bahasa yang dibutuhkan pengguna untuk menentukan semua
> > elemen pemetaan
> >
> > **Bahasa Tingkat Tinggi** Bahasa tingkat tinggi merangkum detail
> > konstruksi visualisasi, seperti fungsi pemetaan, serta beberapa
> > properti untuk tanda seperti ukuran kanvas, legenda, dan properti
> > lainnya.
> >
> > **2.3 Operasi visual berbasis GUI**
> >
> > Dibandingkan dengan menggunakan bahasa visualisasi deklaratif untuk
> > menentukan visualisasi seperti yang dibahas di Bagian 2.2, cara yang
> > lebih mudah digunakan untuk menyediakan spesifikasi
:::

::: {.cell .markdown id="7nJh1RKgZmGT"}
\#**3. Pendekatan yang efisien untuk visualisasi data**

**3.1 Visualisasi data yang tepat**

> > Banyak sistem visualisasi data membaca data dari basis data. Mereka
> > juga dapat memanipulasi data dengan pernyataan SQL dan kemudian
> > menggunakan alat visualisasi untuk membuat visualisasi.
> >
> > Terjemahan Kueri Cara alami untuk menggunakan kembali banyak sistem
> > (DBMS) adalah menerjemahkan kueri visualisasi ke pertanyaan yang
> > diterima oleh sistem tersebut.
> >
> > **Mengintegrasikan Sistem Visualisasi dengan DBMS** Meskipun
> > Meskipun menggunakan terjemahan kueri adalah hal yang alami, ada
> > beberapa kelemahan.
> >
> > **Penyimpanan Kolom** Dalam manajemen data, kinerja utama faktor
> > adalah tata letak data, misalnya, berbasis baris dan berbasis kolom
> > tata letak, yang mungkin memiliki perbedaan kinerja yang sangat
> > besar untuk Aplikasi OLAP.
> >
> > **Indeks** Indeks banyak digunakan untuk meningkatkan kinerja
> > pencarian dengan cara mengurangi jumlah record/baris dalam tabel
> > yang perlu diperiksa.
> >
> > **Komputasi Paralel** Komputasi paralel juga telah banyak digunakan
> > untuk pemrosesan kueri dalam sistem visualisasi data. Kueri agregasi
> > pada ubin data di imMens diparalelkan menggunakan representasi
> > indeks padat dari ubin data.
> >
> > **Prediksi dan Pengambilan Awal** Salah satu langkah penting dalam
> > visualisasi data visualisasi data adalah eksplorasi data-pengguna
> > terus menelusuri visualisasi yang mereka minati untuk mendapatkan
> > gambaran tentang apa yang akan divisualisasikan.

**3.2 Perkiraan visualisasi data**

> > Ketika volume data tumbuh secara eksponensial, modul pemrosesan
> > tradisional tidak dapat memberikan hasil pemrosesan interaktif yang
> > cepat.
:::

::: {.cell .markdown id="rP9d2QxFbFMq"}
\#**4. Rekomendasi visualisasi**

> > proses visualisasi data bersifat berulang, dan titik sakit utama
> > praktisi adalah bahwa mereka harus terlibat dalam setiap langkah
> > untuk membuat beberapa modifikasi
> >
> > **Tinjauan Solusi** Secara umum, untuk menyelesaikan semua masalah
> > masalah di atas, sistem rekomendasi visualisasi pertama-tama perlu
> > menghitung semua kemungkinan visualisasi dan kemudian
> > merekomendasikan visualisasi dengan peringkat teratas.
> >
> > **Memangkas Visualisasi yang Tidak Berarti** Untungnya, ada banyak
> > sinyal (atau kendala) - baik dari pengguna atau dari kebijaksanaan
> > tradisional - yang dapat digunakan untuk memangkas visualisasi yang
> > "buruk".
> >
> > **4.1 Rekomendasi berbasis spesifikasi**
> >
> > **4.1.1 Spesifikasi yang tidak lengkap**
> >
> > Sistem rekomendasi visualisasi dengan spesifikasi kosong tidak
> > memerlukan masukan dari pengguna.
> >
> > **Pemeringkatan visualisasi berbasis aturan** Sebagian besar karya
> > sebelumnya (APT, SAGE, BOZ) pada rekomendasi visualisasi berbasis
> > aturan, yang yang terinspirasi oleh karya-karya tersebut. Sistem
> > rekomendasi berbasis aturan memberi peringkat pada kandidat
> > visualisasi berdasarkan aturan yang telah ditetapkan, yang biasanya
> > merupakan metrik efektivitas persepsi manusia, yang diukur sebagai
> > efektivitas skor dengan mempertimbangkan jenis data, informasi
> > statistik, manusia manusia, preferensi visual, dll.
> >
> > **Aturan Statistik** Kerangka kerja peringkat per fitur adalah
> > sistem rekomendasi berbasis aturan statistik. Ini dapat memberi
> > peringkat 1D atau Visualisasi proyeksi paralel sumbu 2D (histogram,
> > plot kotak, dan plot sebar) kepada pengguna dengan peringkat
> > statistik yang berbeda metrik.
> >
> > **Aturan Persepsi**

**Linear Model** VizDeck memberikan hasil rekomendasi visualisasi yang
dipersonalisasi dengan melatih model linier untuk untuk setiap pengguna
menggunakan perilaku historis mereka.

> > \*\*Selain melatih model untuk setiap pengguna, ada banyak teknik
> > lain dalam sistem rekomendasi yang dipersonalisasi.
:::

::: {.cell .markdown id="TyImBIb7cydZ"}
\#**5. Arah penelitian lainnya**

> > **5.1 Persiapan data untuk visualisasi data**
> >
> > Data kehidupan nyata biasanya kotor, dan memvisualisasikan data yang
> > kotor dapat menyesatkan pengguna. Fenomena ini telah dikenal sejak
> > lama sebagai lama sebagai salah satu jenis visualisasi yang bias
> > dari komunitas visualisasi data. Misalnya, kumpulan data yang
> > diintegrasikan dari berbagai sumber mungkin mengandung duplikat.
> > Secara alami, data yang divisualisasikan harus dibersihkan, seperti
> > seperti normalisasi nilai, deduplikasi, imputasi nilai yang hilang,
> > dan deteksi pencilan.
> >
> > **5.2 Tolak ukur visualisasi data**

Seperti ImageNet atau tolok ukur TPC klasik, penting penting untuk
mengembangkan tolok ukur untuk kinerja dan rekomendasi. Tolok ukur harus
sesuai dengan analisis visual tugas-tugas analisis visual, menyediakan
jejak dan data yang dapat digunakan kembali, dan dalam hal rekomendasi,
memiliki cakupan dan kualitas label yang tinggi. Ada fokus yang muncul
pada pengembangan tolok ukur untuk ukuran kinerja.

> > **5.3 Visualisasi data untuk aplikasi yang berhubungan dengan basis
> > data**
> >
> > Seperti yang telah disebutkan sebelumnya di Bagian 1, visualisasi
> > data juga memainkan peran penting dalam aplikasi yang berhubungan
> > dengan basis data, seperti Excel, Google Spreadsheet, Visualisasi
> > Data Oracle Desktop, IBM Db2, Amazon Quicksight, Microsoft Power BI,
> > dan masih banyak lagi.
:::

::: {.cell .markdown id="ZmZ-EvZBdWBb"}
\#**6. Kesimpulan**

> > Visualisasi data adalah bidang yang berkembang pesat dengan banyak
> > hasil penelitian baru dan sistem baru yang dikembangkan baru-baru
> > ini. Penelitian dan praktisi dari berbagai bidang telah
> > berkontribusi untuk keberhasilan visualisasi data yang luar biasa,
> > yang didorong oleh sebagian besar (jika tidak semua) domain dan
> > aplikasi. Artikel ini terutama mensurvei visualisasi data terbaru
> > terbaru, dari perspektif manajemen data. Secara khusus, kami telah
> > secara komprehensif menggambarkan karya-karya dalam visualisasi
> > spesifikasi, metode yang efisien untuk visualisasi data, dan
> > rekomendasi visualisasi. Seperti yang telah disebutkan sebelumnya,
> > sebagian besar sistem visualisasi data komersial memiliki kemudahan
> > penggunaan yang baik dalam hal spesifikasi visualisasi data. Namun,
> > banyak praktisi masih mengalami masalah efisiensi dan masalah
> > rekomendasi dari sistem ini. Oleh karena itu, kami juga membahas
> > beberapa masalah terbuka yang dapat diselesaikan oleh para peneliti
> > database dapat memberikan kontribusi yang signifikan untuk memajukan
> > bidang data visualisasi.
:::

::: {.cell .markdown id="WrHs_I_gddvT"}
:::
