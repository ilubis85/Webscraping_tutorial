Tutorial Web Scrapping dan Teks Mining
================
Muhammad I. Lubis (<ilubis85@gmail.com>)

<!-- README.md is generated from README.Rmd. Please edit that file -->
<!-- badges: start -->
<!-- badges: end -->

## Apa itu web scrapping

Berdasarkan halaman
[Wikipedia](https://en.wikipedia.org/wiki/Web_scraping), web scraping
merujuk pada proses ekstraksi data secara otomatis dari situs web.
Dengan menggunakan beberapa baris *scripts* web scraping memungkinkan
pengguna untuk mengambil dan menguraikan halaman HTML atau data
terstruktur lainnya dari situs web, serta mengekstrak informasi yang
diinginkan. Dengan web scraping, pengguna dapat mengumpulkan data dari
berbagai halaman web, mengubahnya ke dalam format yang lebih
terstruktur, dan kemudian melakukan analisis atau menggunakan data
tersebut untuk berbagai tujuan.

## Apakah web scraping legal?

Pertanyaan yang sering muncul adalah apakah kegiatan web scraping legal
atau tidak. Berdasarkan informasi terbaru dari
[APIFYBlog](https://blog.apify.com/is-web-scraping-legal/#:~:text=can%20scrape%20everything.-,Myth%202%3A%20Web%20scrapers%20operate%20in%20a%20grey%20area%20of,not%20heavily%20regulated%2C%20that's%20true.),
web scraping legal selama informasi yang diakses adalah informasi publik
dan bukan informasi yang bersifat pribadi atau merupakan kekayaan
intelektual. Secara analogi, web scraping bisa diibaratkan seperti
mengambil foto, di mana semua boleh difoto kecuali dokumen rahasia atau
lokasi-lokasi yang dilarang untuk difoto..

<div class="figure" style="text-align: center">

<img src="docs/Webscraping_legal.jpg" alt="Mitos terkait web scraping" width="70%" />
<p class="caption">
Mitos terkait web scraping
</p>

</div>

## Bagaimana melakukan web scrapping

Web scraping dapat dilakukan melalui dua tahap: pertama, mencari dan
mengumpulkan alamat website, dan kedua, melakukan ekstraksi informasi
yang dibutuhkan dengan membangun kode atau skrip. Jika Anda menggunakan
R, Anda dapat menggunakan library **rvest** untuk melakukan ekstraksi
data. Sebagai contoh, kita akan melakukan scraping informasi dari
artikel online terkait konflik antara manusia dan harimau (KMH).

#### Kumpulkan beberapa artikel online untuk di-scraping

Konflik manusia dan harimau (KMH) menunjukkan tren peningkatan dalam
beberapa tahun terakhir, terutama di daerah dengan tingkat tutupan hutan
yang tinggi, seperti di Provinsi Aceh. Saat ini, data terkait sebaran
lokasi konflik antara manusia dan harimau tidak tersedia secara umum,
padahal informasi tersebut sangat penting untuk mitigasi dan
pengendalian konflik guna meminimalkan dampak negatif terhadap manusia
dan satwa liar.

Salah satu sumber informasi publik terkait KMH dapat diakses melalui
berita atau artikel online. Tutorial web scraping ini akan mencoba
mengekstrak informasi konflik melalui media online. Kita akan
menggunakan link berikut ini sebagai contoh

“<https://aceh.tribunnews.com/2020/03/11/teror-harimau-sumatera-belum-mereda-di-subulussalam-giliran-desa-bawan-jadi-sasaran?page=all>”

Untuk melakukan web scraping pada halaman tersebut, kita akan
mengekstraksi informasi yang dibutuhkan, seperti judul artikel, tanggal
publikasi, dan isi artikel.

#### Menggunakan SelectorGadget untuk mengetahui kode lokasi beberapa informasi

SelectorGadget adalah salah satu ekstensi untuk web browser Chrome yang
sangat berguna dalam menentukan kode atau lokasi dari informasi yang
ingin diekstrak. Ini memungkinkan Anda dengan mudah memilih elemen HTML
yang ingin Anda tuju untuk scraping, seperti tanggal publikasi, penulis
artikel, atau isi tulisan. Penting untuk diingat bahwa setiap website,
bahkan setiap halaman dalam satu website, mungkin memiliki kode dan
lokasi yang berbeda-beda.

**Berikut adalah langkah-langkah penggunaan SelectorGadget:**

1.  Buka halaman web yang ingin Anda scrape di browser Chrome.
2.  Install ekstensi SelectorGadget dari Chrome Web Store.
3.  Setelah ekstensi terpasang, klik ikon SelectorGadget di toolbar
    Chrome (ikon berbentuk cangkul).
4.  Saat mode SelectorGadget aktif, elemen yang Anda arahkan dengan
    kursor akan diberi penyorotan.
5.  Klik pada elemen yang ingin Anda pilih. SelectorGadget akan mencoba
    memilih elemen tersebut bersama dengan kode selektornya.
6.  Jika elemen yang dipilih tidak sesuai atau tidak akurat, klik lagi
    pada elemen lain untuk memperbaikinya. Anda dapat mengklik beberapa
    elemen untuk memilih area yang tepat.
7.  Setelah Anda puas dengan pemilihan elemen, Anda dapat melihat kode
    selektor di bagian atas jendela SelectorGadget. Anda dapat menyalin
    dan menggunakan kode tersebut dalam skrip web scraping Anda.
8.  Ulangi langkah-langkah di atas untuk setiap informasi yang ingin
    Anda ekstrak, seperti tanggal, penulis, atau isi tulisan.

Dengan menggunakan SelectorGadget, Anda dapat dengan mudah mengetahui
kode atau lokasi elemen-elemen yang ingin Anda scrape pada halaman web
yang dituju.
