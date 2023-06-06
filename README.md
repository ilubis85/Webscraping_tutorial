Tutorial Web Scrapping dan Teks Mining
================
Muhammad I. Lubis (<ilubis85@gmail.com>)

<!-- README.md is generated from README.Rmd. Please edit that file -->
<!-- badges: start -->
<!-- badges: end -->

## Apa itu web scrapping

Berdasarkan halaman Wikipedia, Web scraping merujuk pada proses
ekstraksi data dari websites secara otomatis. Web scraping dapat
dilakukan dengan menuliskan beberapa baris *scripts* untuk mendapatkan
dan menguraikan halaman HTML atau data terstruktur lainnya dari halaman
web dan mengextrak informasi yang diinginkan. Web scraping memungkinkan
pengguna untuk mengumpulkan data dari beberapa halaman web, mengubahnya
ke dalam format yang lebih terstruktur, lalu melakukan analisis atau
menggunakannya untuk berbagai tujuan.

## Legalkah web scrapping

Pertanyaan yang sering muncul di kepala pengguna web scraping adalah
apakah kegiatan web scraping itu legal atau tidak.

## Bagaimana melakukan web scrapping

Web scraping dapat dilakukan melalui dua tahap, mencari dan mengumpulkan
alamat website lalu melakukan ekstraksi informasi yang dibutuhkan.

### Kumpulkan beberapa artikel online untuk di scraping

Konflik manusia dan harimau (KMH) menunjukkan trend peningkatan beberapa
tahun terakhir ini, khususnya di sekitar daerah yang memiliki tutupan
hutan yang tinggi seperti di Provinsi Aceh. Saat ini, data terkait
sebaran lokasi konflik antara manusia dan harimau tidak tersedia secara
umum, sementara informasi terkait ini sangat diperlukan untuk mitigasi
dan pengendalian konflik untuk meminimalisisr dampak negatif terhadap
manusia dan satwa liar.

Salah satu sumber informasi publik terkait KMH dapat di akses melalui
berita atau artikel online. Tutorial web scraping kali ini akan mencoba
mengekstrak informasi konflik melalui media online. Beberapa websites
yang berisi informasi konflik di Provinsi Riau dikumpulkan seperti yang
terlihat pada tabel berikut. misalnya klik website berikut:

“<https://aceh.tribunnews.com/2020/03/11/teror-harimau-sumatera-belum-mereda-di-subulussalam-giliran-desa-bawan-jadi-sasaran?page=all>”

<table class="table" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>
Beberapa artikel terkait konflik mansia dan harimau (KMH) di Aceh
</caption>
<thead>
<tr>
<th style="text-align:left;">
Website
</th>
<th style="text-align:left;">
alamat_website
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
TribunNews
</td>
<td style="text-align:left;">
aku/sudah/ngantuk
</td>
</tr>
<tr>
<td style="text-align:left;">
TribunNews
</td>
<td style="text-align:left;">
aku sudah ngantuk
</td>
</tr>
<tr>
<td style="text-align:left;">
TribunNews
</td>
<td style="text-align:left;">
aku sudah ngantuk
</td>
</tr>
<tr>
<td style="text-align:left;">
KompasNews
</td>
<td style="text-align:left;">
aku sudah ngantuk
</td>
</tr>
<tr>
<td style="text-align:left;">
KompasNews
</td>
<td style="text-align:left;">
aku sudah ngantuk
</td>
</tr>
</tbody>
</table>

### Gunakan selector gadget untuk mengetahui kode lokasibeberapa informasi

Selector gadget merupan salah satu ekstensi dari web browser Chrome yang
dapat digunakan untuk mengetahui lokasi atau kode dimana informasi
tertentu seperti tanggal artikel terbit, penulis artikel, atau isi
tulisan disimpan. Kode dan lokasi informasi tersebut akan berbeda antara
satu website dengan website lainnya, bahkan antar webpage yang masih di
dalam satu website.

Dengan menggunakan alat selector gadget, kita akan mengekstrak informasi
tanggal artikel terbit, penulis artikel, dan isi artikel dari kelima
website diatas.
