# Alat-Analisis-Phishing
Perkenalan

Di ruangan ini, kita akan melihat berbagai alat yang akan membantu kita dalam menganalisis email phishing . Kita akan: 

Perhatikan alat-alat yang dapat membantu kita dalam memeriksa informasi header email.
Pelajari teknik untuk mendapatkan hyperlink dalam email, dan lengkapi URL jika URL tersebut dipersingkat.
Cari alat yang dapat memberi kita informasi tentang tautan yang berpotensi berbahaya tanpa harus berinteraksi langsung dengan tautan berbahaya tersebut.
Mempelajari teknik untuk mendapatkan lampiran berbahaya dari email phishing dan menggunakan sandbox malware untuk menguji lampiran tersebut guna memahami lebih lanjut apa yang dirancang untuk dilakukan oleh lampiran tersebut.
Peringatan : Contoh-contoh di ruangan ini berisi informasi dari email spam dan/atau phishing yang sebenarnya . Berhati-hatilah jika Anda mencoba berinteraksi dengan IP, domain, lampiran, dan lain sebagainya.

# Informasi apa yang harus kami kumpulkan?
Dalam tugas ini, kita akan menguraikan langkah-langkah yang dilakukan saat menganalisis email yang mencurigakan atau berbahaya. 

Berikut adalah daftar periksa informasi penting yang perlu dikumpulkan oleh seorang analis (Anda) dari header email:

Alamat email pengirim
Alamat IP pengirim
Pencarian terbalik alamat IP pengirim
Judul subjek email
Alamat email penerima (informasi ini mungkin ada di kolom CC/BCC)
Alamat email balasan (jika ada)
Tanggal/waktu
Setelah itu, kita akan memperhatikan isi email dan lampiran (jika ada).

Berikut adalah daftar periksa artefak yang perlu dikumpulkan oleh seorang analis (Anda) dari isi email:

Semua tautan URL (jika menggunakan layanan pemendek URL, maka kami perlu mendapatkan tautan URL yang sebenarnya)

# Analisis header email
Beberapa informasi penting yang perlu kita kumpulkan dapat diperoleh secara visual dari klien email atau klien web (seperti Gmail, Yahoo!, dll.). Namun, beberapa informasi, seperti alamat IP pengirim dan informasi balasan, hanya dapat diperoleh melalui header email.

Pada Email Phishing 1 , kita telah melihat bagaimana cara mendapatkan informasi ini secara manual dengan menelusuri kode sumber email.

Di bawah ini kita akan melihat beberapa alat yang akan membantu kita mendapatkan informasi ini.

Yang pertama akan kita bahas adalah alat dari Google yang dapat membantu kita menganalisis header email, yaitu Messageheader dari Google Admin Toolbox. 

Menurut situs tersebut , " Messageheader menganalisis header pesan SMTP , yang membantu mengidentifikasi akar penyebab keterlambatan pengiriman. Anda dapat mendeteksi server yang salah konfigurasi dan masalah perutean email ".

Cara penggunaan : Salin dan tempel seluruh header email lalu jalankan alat analisisnya. 

Header pesan :  https://toolbox.googleapps.com/apps/messageheader/analyzeheader
Nama lampiran
Nilai hash dari lampiran (tipe hash MD5 atau SHA256, lebih disukai yang terakhir)
Peringatan : Berhati-hatilah agar tidak mengklik tautan atau lampiran apa pun di dalam email secara tidak sengaja.

Alat lain disebut Message Header Analyzer . 

Penganalisis Header Pesan :  https://mha.azurewebsites.net/
<img width="974" height="760" alt="image" src="https://github.com/user-attachments/assets/65f81c11-89a2-4dcd-bfb9-2e17fd570751" />

Terakhir, Anda juga dapat menggunakan mailheader.org .

<img width="724" height="763" alt="image" src="https://github.com/user-attachments/assets/a3806d23-488d-4465-a954-5898a4b34f3a" />

Meskipun tidak dibahas di ruang Phishing sebelumnya , Message Transfer Agent ( MTA ) adalah perangkat lunak yang mentransfer email antara pengirim dan penerima. Baca selengkapnya tentang MTA di sini . Karena kita sedang membahas topik ini, baca tentang MUA (Mail User Agent) di sini . 

Catatan : Pilihan alat mana yang akan digunakan pada akhirnya bergantung pada Anda. Sebaiknya memiliki beberapa sumber referensi karena setiap alat mungkin mengungkapkan informasi yang mungkin tidak diungkapkan oleh alat lain. 

Alat-alat di bawah ini dapat membantu Anda menganalisis informasi tentang alamat IP pengirim:

IPinfo.io:  https://ipinfo.io/
Menurut situs tersebut , " Dengan IPinfo, Anda dapat menentukan lokasi pengguna Anda, menyesuaikan pengalaman mereka, mencegah penipuan, memastikan kepatuhan, dan masih banyak lagi ".

<img width="1191" height="562" alt="image" src="https://github.com/user-attachments/assets/ceffbc60-588f-4486-9242-242565eb0bba" />
URLScan.io:  https://urlscan.io/
Menurut situs tersebut , " urlscan.io adalah layanan gratis untuk memindai dan menganalisis situs web. Ketika sebuah URL dikirimkan ke urlscan.io, proses otomatis akan menelusuri URL tersebut seperti pengguna biasa dan merekam aktivitas yang dihasilkan oleh navigasi halaman ini. Ini termasuk domain dan IP yang dihubungi, sumber daya (JavaScript, CSS, dll.) yang diminta dari domain tersebut, serta informasi tambahan tentang halaman itu sendiri. urlscan.io akan mengambil tangkapan layar halaman, merekam konten DOM, variabel global JavaScript, cookie yang dibuat oleh halaman, dan berbagai pengamatan lainnya. Jika situs tersebut menargetkan pengguna dari lebih dari 400 merek yang dilacak oleh urlscan.io, situs tersebut akan disorot sebagai berpotensi berbahaya dalam hasil pemindaian ".

<img width="1197" height="765" alt="image" src="https://github.com/user-attachments/assets/067739e0-f877-4539-96b8-fcce245aa686" />
Perhatikan bahwa urlscan.io menyediakan tangkapan layar URL tersebut. Tangkapan layar ini disediakan agar Anda tidak perlu menavigasi ke URL yang dimaksud secara eksplisit.

Anda dapat menggunakan alat lain yang menyediakan fungsi yang sama dan lebih banyak lagi, seperti  URL2PNG dan Wannabrowser .

Pusat Reputasi Talos:  https://talosintelligence.com/reputation
<img width="1273" height="741" alt="image" src="https://github.com/user-attachments/assets/02eb0ebe-b437-425e-b1d4-6d3419a874cd" />
Jawablah pertanyaan-pertanyaan di bawah ini.
Apa nama situs resmi bank yang coba ditiru oleh capitai-one.com?

capitalone.com

Analisis isi email
Sekarang saatnya memfokuskan perhatian Anda pada isi email. Di sinilah muatan berbahaya dapat dikirimkan ke penerima, baik sebagai tautan maupun lampiran. 

Tautan dapat diekstrak secara manual, baik langsung dari email berformat HTML atau dengan menelusuri header email mentah.

Berikut adalah contoh cara mendapatkan tautan secara manual dari email dengan mengklik kanan tautan dan memilih Salin Lokasi Tautan . 
Hal yang sama dapat dicapai dengan bantuan sebuah alat. Salah satu alat yang dapat membantu kita dalam tugas ini adalah URL Extractor. 

Ekstraktor URL:  https://www.convertcsv.com/url-extractor.htm
Anda dapat menyalin dan menempelkan header mentah ke dalam kotak teks untuk Langkah 1: Pilih input Anda . 
URL yang diekstrak dapat dilihat pada Langkah 3 . 

<img width="1104" height="377" alt="image" src="https://github.com/user-attachments/assets/68a7655f-d2cd-4640-8fa0-de6ee8cd14ef" />
Anda juga dapat menggunakan CyberChef untuk mengekstrak URL dengan resep Ekstrak URL
<img width="326" height="265" alt="image" src="https://github.com/user-attachments/assets/dff6a695-2e59-44a6-8519-948141e12ae6" />
Tip : Penting untuk mencatat domain akar dari URL yang diekstrak. Anda juga perlu melakukan analisis pada domain akar tersebut. 

Setelah mengekstrak URL, langkah selanjutnya adalah memeriksa reputasi URL dan domain utama. Anda dapat menggunakan salah satu alat yang disebutkan pada tugas sebelumnya untuk membantu Anda dalam hal ini. 

Jika email tersebut memiliki lampiran, Anda perlu mendapatkan lampiran tersebut dengan aman. Melakukan hal ini mudah di Thunderbird dengan menggunakan tombol Simpan.

<img width="869" height="44" alt="image" src="https://github.com/user-attachments/assets/b5e39143-bec6-4732-a6b5-3dd3486cd72b" />
Setelah Anda mendapatkan lampiran tersebut, Anda kemudian dapat memperoleh hash-nya. Anda dapat memeriksa reputasi file tersebut dengan hash untuk melihat apakah itu dokumen berbahaya yang dikenal.

Dapatkan hash SHA256 dari file tersebut.
user@machine$ sha256sum Double\ Jackpot\ Slots\ Las\ Vegas.dot
c650f397a9193db6a2e1a273577d8d84c5668d03c06ba99b17e4f6617af4ee83  Double Jackpot Slots Las Vegas.dot
Ada banyak alat yang tersedia untuk membantu kita dalam hal ini, tetapi kita akan fokus pada dua alat utama; alat-alat tersebut tercantum di bawah ini:

Reputasi File Talos:  https://talosintelligence.com/talos_file_reputation
Menurut  situs tersebut , " Cisco Talos Intelligence Group memelihara disposisi reputasi pada miliaran file. Sistem reputasi ini dimasukkan ke dalam lini produk AMP, FirePower, ClamAV, dan Snort sumber terbuka. Alat di bawah ini memungkinkan Anda untuk melakukan pencarian biasa terhadap sistem Reputasi File Talos. Sistem ini membatasi Anda untuk melakukan satu pencarian dalam satu waktu, dan hanya terbatas pada pencocokan hash. Pencarian ini tidak mencerminkan kemampuan penuh dari sistem Advanced Malware Protection (AMP) ".
<img width="832" height="620" alt="image" src="https://github.com/user-attachments/assets/cf2cec1a-3785-4acd-8130-626cc5f64457" />
<img width="1286" height="673" alt="image" src="https://github.com/user-attachments/assets/de672361-88cf-465c-949d-fa53313e9441" />

VirusTotal :  https://www.virustotal.com/gui/​
Menurut situs tersebut , "Analisis file dan URL yang mencurigakan untuk mendeteksi jenis malware, dan bagikan secara otomatis dengan komunitas keamanan."
<img width="756" height="639" alt="image" src="https://github.com/user-attachments/assets/4d4a6497-b0a0-4225-af0f-9aea3f930746" />
<img width="1417" height="780" alt="image" src="https://github.com/user-attachments/assets/19d39d83-5daa-4549-8b71-9b156c20b085" />
Alat/perusahaan lain yang patut disebutkan adalah Reversing Labs , yang juga memiliki layanan reputasi file . 

Jawablah pertanyaan-pertanyaan di bawah ini.
Bagaimana cara mendapatkan lokasi hyperlink secara manual?
Copy Link Location

Kotak Pasir Malware
Untungnya, sebagai Defender, kita tidak perlu memiliki keterampilan analisis malware untuk membedah dan merekayasa balik lampiran berbahaya guna memahami malware dengan lebih baik. 

Terdapat alat dan layanan daring tempat file berbahaya dapat diunggah dan dianalisis untuk lebih memahami apa yang diprogramkan oleh malware tersebut. Layanan ini dikenal sebagai sandbox malware. 

Sebagai contoh, kita dapat mengunggah lampiran yang kita peroleh dari email yang berpotensi berbahaya dan melihat URL apa yang coba dihubungi, muatan tambahan apa yang diunduh ke titik akhir, mekanisme persistensi , Indikator Kompromi (IOC), dan lain sebagainya. 

Beberapa sandbox malware online tersebut tercantum di bawah ini.

Any.Run:  https://app.any.run/
Menurut situs tersebut , " Analisis aktivitas jaringan, file, modul, dan registri. Berinteraksi langsung dengan sistem operasi dari peramban. Lihat umpan balik dari tindakan Anda secara instan ".



Analisis Hibrida:  https://www.hybrid-analysis.com/
Menurut situs tersebut,  "Ini adalah layanan analisis malware gratis untuk masyarakat yang mendeteksi dan menganalisis ancaman yang tidak dikenal menggunakan teknologi Analisis Hibrida yang unik ."



https://www.joesecurity.org/
Menurut situs tersebut, " Joe Sandbox memberdayakan analis dengan berbagai fitur produk. Di antaranya: Interaksi Langsung, Analisis URL & Deteksi Phishing berbasis AI , dukungan aturan Yara dan Sigma, matriks MITRE ATT&CK, deteksi malware berbasis AI , Pemantau Email, Perburuan Ancaman & Intelijen, Perilaku Pengguna Otomatis, instrumentasi VBA/JS/ JAR Dinamis , Grafik Eksekusi, Anonimisasi Internet Lokal, dan masih banyak lagi ".


# PhishTool
Salah satu alat yang dapat membantu analisis phishing otomatis adalah  PhishTool .

Ya, saya menyimpannya untuk terakhir! Apa itu PhishTool?

Menurut situs tersebut, " Baik Anda seorang peneliti keamanan yang menyelidiki perangkat phishing baru, seorang analis SOC yang menanggapi laporan phishing dari pengguna , seorang analis intelijen ancaman yang mengumpulkan IoC phishing , atau seorang penyelidik yang menangani penipuan melalui email."

PhishTool menggabungkan intelijen ancaman, OSINT , metadata email, dan jalur analisis otomatis yang telah teruji ke dalam satu platform respons phishing yang ampuh . Hal ini menjadikan Anda dan organisasi Anda sebagai lawan yang tangguh - kebal terhadap kampanye phishing yang biasanya menimpa mereka yang memiliki kemampuan keamanan email yang lebih rendah .

Catatan : Tersedia edisi komunitas gratis yang dapat Anda unduh dan gunakan. :)

Saya mengunggah email berbahaya ke PhishTool dan menghubungkan VirusTotal ke akun saya menggunakan kunci  API edisi komunitas saya.

Berikut beberapa tangkapan layar dari email berbahaya dan antarmuka PhishTool.  . 
<img width="1050" height="747" alt="image" src="https://github.com/user-attachments/assets/915a76b1-f4d7-4839-b6a8-185fa6041c04" />

Dari gambar di atas, Anda dapat melihat bahwa PhishTool dengan mudah mengambil semua informasi penting yang kita perlukan terkait email tersebut.

Pengirim email
Penerima email (dalam hal ini, daftar panjang alamat email yang di-CC)
Cap waktu
IP asal dan pencarian DNS terbalik
Kita dapat memperoleh informasi tentang relay SMTP , informasi header X spesifik, dan informasi IP.
<img width="1218" height="123" alt="image" src="https://github.com/user-attachments/assets/961f0e65-04bd-4531-a55f-3832f7707f5f" />
Berikut adalah cuplikan Hop 1 dari 6 ( relay SMTP ).
<img width="724" height="266" alt="image" src="https://github.com/user-attachments/assets/880c3cb3-23e9-4038-98ba-bbc926683e68" />

Perhatikan bahwa alat tersebut memberi tahu kita bahwa ' Reply-To tidak ada ' meskipun alat tersebut menyediakan informasi header alternatif,  Return-Path .

Di sebelah kanan dasbor PhishTool, kita dapat melihat isi email. Terdapat dua tab di bagian atas yang dapat kita alihkan untuk melihat email dalam format teks atau kode sumber HTML-nya. 

Tampilan teks:

<img width="937" height="421" alt="image" src="https://github.com/user-attachments/assets/d7cd22ce-8b27-4389-acdf-d6d48308dfed" />
Tampilan HTML:
<img width="1020" height="392" alt="image" src="https://github.com/user-attachments/assets/97c4336b-1e33-4571-b137-7b8f2d324f37" />
Dua panel bagian bawah akan menampilkan informasi tentang lampiran dan URL.

Panel sebelah kanan akan menunjukkan apakah ada URL yang ditemukan dalam email tersebut. Dalam kasus ini, tidak ada email yang ditemukan.
<img width="587" height="334" alt="image" src="https://github.com/user-attachments/assets/5722431b-cc36-4874-b455-9e1cd3cd9312" />
Panel sebelah kiri akan menampilkan informasi tentang lampiran. Email berbahaya ini memiliki file zip.
<img width="1025" height="175" alt="image" src="https://github.com/user-attachments/assets/a93fce2f-68a0-4f08-a5ef-2fecc1b261b5" />

Kita bisa mendapatkan umpan balik dari VirusTotal secara otomatis karena kunci API edisi komunitas kita sudah terhubung.

Di sini kita bisa mendapatkan nama file zip dan hash-nya tanpa perlu berinteraksi langsung dengan email berbahaya tersebut.

 Terdapat elipsis di paling kanan gambar di atas. Jika diklik, kita akan diberikan tindakan tambahan yang dapat kita lakukan dengan lampiran tersebut.

Berikut adalah tangkapan layar sub-menu opsi tambahan.

<img width="489" height="199" alt="image" src="https://github.com/user-attachments/assets/e910c725-7256-4bd0-bcd5-a0d59635326f" />
Mari kita lihat output Strings.
<img width="459" height="312" alt="image" src="https://github.com/user-attachments/assets/a989e868-bf37-4106-92ad-a86c507ef9da" />

Selanjutnya, mari kita lihat informasi dari VirusTotal.
Karena kunci API VirusTotal adalah edisi komunitas gratis, seorang analis dapat secara manual mengakses VirusTotal dan melakukan pencarian hash file untuk melihat informasi lebih lanjut tentang lampiran ini. 

Terakhir, setiap kiriman yang Anda unggah ke PhishTool, dapat Anda tandai sebagai berbahaya dan diselesaikan dengan catatan. Mirip dengan cara Anda bekerja sebagai Analis SOC .
Nama file lampiran dan hash file akan ditandai sebagai berbahaya. Selanjutnya, klik Atasi .

<img width="347" height="93" alt="image" src="https://github.com/user-attachments/assets/12e52d01-d4b9-40bf-90ca-5f7cc5e4fa52" />
Pada layar berikutnya, seorang analis dapat menandai email berdasarkan pilihan dari menu tarik-turun. Lihat GIF di bawah ini.

<img width="809" height="540" alt="image" src="https://github.com/user-attachments/assets/937e395c-20b1-432e-baa4-ac2abe944d9e" />

Catatan : Saya tidak melakukan analisis lebih lanjut pada nama domain atau alamat IP. Saya juga tidak melakukan riset apa pun mengenai domain utama tempat email tersebut berasal. Lampiran tersebut dapat dianalisis lebih lanjut dengan mengunggahnya ke sandbox malware untuk melihat apa sebenarnya yang dilakukannya, yang tidak saya lakukan. Karena itulah artefak Flag dan kode Klasifikasi tambahan tidak dipilih untuk email berbahaya ini. :) 

Untuk menjelaskan lebih lanjut tentang kode klasifikasi secara singkat, tidak semua email phishing dapat dikategorikan sama. Kode klasifikasi memungkinkan kita untuk menandai suatu kasus dengan kode spesifik, seperti Whaling (target bernilai tinggi). Tidak semua email phishing akan menargetkan target bernilai tinggi, seperti Chief Financial Officer (CFO). 

Jawablah pertanyaan-pertanyaan di bawah ini.
Perhatikan output Strings. Apa nama file EXE tersebut?
#454326_PDF.exe

Kasus Phishing 1

Nyalakan Mesin
Skenario : Anda adalah Analis SOC Level 1. Beberapa email mencurigakan telah diteruskan kepada Anda dari rekan kerja lain. Anda harus mendapatkan detail dari setiap email agar tim Anda dapat menerapkan aturan yang sesuai untuk mencegah rekan kerja menerima email  spam/ phishing tambahan.

Tugas : Gunakan alat-alat yang telah dibahas di ruangan ini (atau gunakan sumber daya Anda sendiri) untuk membantu Anda menganalisis setiap header email dan isi email. 

Aktifkan mesin yang terhubung dengan tugas ini; mesin tersebut akan terlihat di  tampilan layar terpisah  setelah siap.

Jika Anda tidak melihat mesin virtual dimuat, klik  tombol Tampilkan Tampilan Terpisah  .



# Jawablah pertanyaan-pertanyaan di bawah ini.
Email ini dirancang untuk meniru merek apa?

Netflix


Apa alamat email pengirimnya?

NetfIix<JGQ47wazXe1xYVBrkeDg-JOg7ODDQwWdR@JOg7ODDQwWdR-yVkCaBkTNp.gogolecloud.com>________.___________.______


Apa alamat IP asalnya? Hilangkan sanggahan pada alamat IP tersebut. ? 
buka contoh file yang akan di analyst di thunderbid  - setelah ketemu - jangan di klik dulu - cari more - view source - lihat isi header email 
buka web https://mha.azurewebsites.net/ dan copy paste kan seluruh isi header email tsb din web - lihat apa yang ingin di cari - hasil 
jawaban : 209[.]85[.]167[.]226



Dari apa yang dapat Anda simpulkan, menurut Anda apa yang akan menjadi bidang yang menarik? Hilangkan belenggu pada bidang tersebut.

etekno[.]xyz



Apa URL yang dipersingkat? Hilangkan efek angker pada URL tersebut.?
lihat halamanm email utaman yang mencurigakan - klik kanan pada kotak email yang mecurigakan - copy link email tsb - copy link location - setelah mendapatkan nya misal : https://t.co/yuxfZm8KPg?amp=1
salin dan tempel di - web cyber cheff link tadi - opration pilih defang url -  recipe defang url - kemudian paste link yang sudah di copy tadi - lihat outputnya - outputnya : hxxps[://]t[.]co/yuxfZm8KPg?amp=1

jawaban : hxxps[://]t[.]co/yuxfZm8KPg?amp==1



