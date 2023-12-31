# Tugas - Membuat Inventory Website
Nama  : Syarna Savitri <br>
NPM   : 2206083565 <br>
Kelas : PBP B <br>
Asdos : EDA <br>

## Hasil Website
Website dapat diakses melalui [link ini](https://inventorywebsite-pbp.adaptable.app).

# Penjelasan Cara Penyelesaian Tugas 6
Cara pengimplementasian *checklist* untuk menyelesaikan Tugas 6: <br>
   Setelah mempelajari [Tutorial 5](https://pbp-fasilkom-ui.github.io/ganjil-2024/docs/tutorial-5), saya menyelesaikan Tugas 5 dengan mempelajari dari banyak sumber.<br>
   Berikut adalah *step-by-step* yang saya buat dengan menyesuaikan *checklist* yang ada pada berkas soal:
      
   - [x] Membuat fungsi untuk mengembalikan data JSON
   - [x] Membuat fungsi untuk menambahkan produk dengan AJAX
   - [x] Menambahkan fungsi untuk routing `get_product_json` dan `get_product_ajax`
   - [x] Menampilkan data produk dengan `Fetch()` API
   - [x] Membuat modal sebagai Form untuk menambahkan produk
   - [x] Menambahkan data produk dengan AJAX

## perbedaan antara asynchronous programming dengan synchronous programming.
Pada proses synchronous setiap fungsi dijalankan berurutan, untuk dapat menjalankan fungsi berikutnya maka kita harus menunggu fungsi sebelumnya selesai (blocking). Berbeda dengan proses asynchronous dimana kita tidak perlu menunggu suatu fungsi selesai dijalankan untuk menjalankan fungsi lainnya (non-blocking).
Dari segi lama waktu eksekusi suatu program, proses asynchronous cenderung lebih cepat dibandingkan dengan proses synchronous. Dapat dilihat pada ilustrasi di bawah, proses synchronous membutuhkan waktu yg lebih lama dibandingkan proses asynchronous karena pada proses synchronous kita harus menunggu setiap fungsi selesai dijalankan.
Meskipun proses asynchronous terlihat banyak memiliki kelebihan dibandingkan dengan proses synchronous, namun ada beberapa hal yang perlu diperhatikan sebelum menggunakan proses asynchronous.
1. Keterkaitan antar fungsi
Setiap fungsi pada proses asynchronous berjalan secara indepeden atau tidak saling mempengaruhi satu sama lain, jika hasil dari suatu fungsi akan digunakan pada fungsi berikutnya maka prosesnya harus berjalan secara berurutan. Oleh karena itu jika suatu fungsi saling berkaitan dengan fungsi lainnya, maka penggunaan proses asynchronous menjadi tidak tepat.
2. Lama waktu eksekusi
Berapa lamakah waktu yang dibutuhkan untuk menjalankan setiap fungsi?. Jika rata-rata waktu yang dibutuhkan untuk setiap fungsi relatif cepat dan tidak membutuhkan proses yang kompleks, penggunaan proses asynchronous tidak akan berdampak besar pada jalannya sebuah program.
3. Kompleksitas
Penerapan proses asynchronous pada suatu program cukuplah rumit, maka dari itu jika program yang akan dibuat masih tergolong simple dan tidak membutuhkan banyak proses, penggunaan asynchronous justru akan membuat program yang sederhana terlihat begitu kompleks

## Dalam penerapan JavaScript dan AJAX, terdapat penerapan paradigma event-driven programming. Jelaskan maksud dari paradigma tersebut dan sebutkan salah satu contoh penerapannya
Paradigma "event-driven programming" adalah suatu pendekatan dalam pemrograman di mana program merespons peristiwa atau "event" yang terjadi, seperti interaksi pengguna dengan antarmuka pengguna (UI) atau perubahan status dalam sistem. Dalam konteks JavaScript dan AJAX, paradigma ini sangat penting karena memungkinkan pengembang untuk membuat aplikasi yang responsif, interaktif, dan dinamis. Pada dasarnya, program yang ditulis dengan paradigma ini bekerja dengan cara mendengarkan peristiwa, menentukan tindakan yang akan diambil saat peristiwa tersebut terjadi, dan merespons peristiwa tersebut dengan menjalankan fungsi atau kode tertentu.

Salah satu contoh penerapan paradigma event-driven programming dalam JavaScript adalah penanganan peristiwa (event handling) di antarmuka pengguna web. Misalnya, ketika seorang pengguna mengklik tombol pada halaman web, ini menciptakan peristiwa klik (click event). Pengembang dapat menentukan bagaimana halaman web harus merespons peristiwa ini dengan menambahkan "event listener" ke elemen tombol tersebut.

```bash
document.getElementById("button_add").onclick = addProduct;
```

## penerapan asynchronous programming pada AJAX
Umumnya dalam dunia programing, kode yang kita tuliskan berjalan secara synchronous, begitu pula pada Javascript. Synchronous ini membuat kode yang kita tuliskan dijalankan secara berurutan. Hal ini sangat lemah ketika kita gunakan untuk melakukan sebuah pekerjaan yang berat, atau pekerjaan yang membutuhkan waktu yang belum dapat kita pastikan kapan pekerjaan itu selesai.

Jika kita melakukan pekerjaan tersebut secara synchronous, proses runtime akan terblokade hingga pekerjaan tersebut selesai dijalankan. Yang paling menakutkan adalah pengguna akan terganggu dengan adanya blocking tersebut.

Kode yang dituliskan secara asynchronous akan dieksekusi di belakang thread utama atau biasa disebut main thread. Hal tersebut tidak akan membloking proses runtime atau menunggu hingga proses selesai dilakukan. Sembari menunggu proses tersebut selesai, compiler akan mengeksekusi perintah kode selanjutnya.

Pada Javascript, Asynchronous JavaScript and XMLHTTP atau biasa disebut AJAX merupakan salah satu konsep yang menerapkan metode asynchronous dalam menjalankan pekerjaannya. Biasa nya AJAX digunakan untuk melakukan permintaan data (request) dan menangani sebuah tanggapan (handling response), baik response dalam bentuk XML, Javascript ataupun JSON dari sebuah Rest API.

## penerapan AJAX dilakukan dengan menggunakan Fetch API daripada library jQuery. Bandingkanlah kedua teknologi tersebut dan tuliskan pendapat kamu teknologi manakah yang lebih baik untuk digunakan.
Fetch API dan jQuery adalah dua teknologi yang digunakan untuk melakukan AJAX (Asynchronous JavaScript and XML) dalam pengembangan web. Masing-masing memiliki karakteristik dan kelebihan sendiri. Pendapat tentang teknologi mana yang lebih baik dapat bergantung pada kebutuhan proyek dan preferensi pengembang, tetapi di bawah ini saya akan membandingkan keduanya dari beberapa aspek:

1. **Fetch API**:
   - **Native JavaScript**: Fetch API adalah bagian dari JavaScript, yang berarti tidak memerlukan pustaka eksternal untuk digunakan. Ini adalah bagian dari standar ECMAScript yang modern.
   - **Promise-based**: Fetch API menggunakan Promise untuk mengelola permintaan dan respons, sehingga memungkinkan penanganan peristiwa yang lebih baik dan lebih mudah dibaca.
   - **Lebih Ringan**: Karena itu adalah bagian dari JavaScript inti, Fetch API biasanya lebih ringan daripada jQuery, yang merupakan pustaka yang lebih besar dan memiliki lebih banyak fitur.

2. **jQuery**:
   - **Cross-Browser Compatibility**: jQuery diciptakan untuk mengatasi masalah kompatibilitas lintas peramban (cross-browser compatibility), sehingga Anda tidak perlu khawatir tentang perbedaan implementasi peramban saat menggunakan jQuery.
   - **Abstraction of Complexity**: jQuery menyediakan abstraksi yang kuat atas banyak operasi JavaScript yang umum digunakan. Hal ini membuat pengembangan lebih cepat dan lebih mudah, terutama jika Anda tidak terlalu familiar dengan JavaScript murni.
   - **Plugin Ecosystem**: jQuery memiliki ekosistem plugin yang kaya, yang memungkinkan Anda dengan mudah menambahkan fitur tambahan ke situs web Anda.

Pilihan antara Fetch API dan jQuery sangat tergantung pada konteks proyek dan preferensi pribadi. Beberapa pertimbangan yang mungkin membantu Anda memutuskan antara keduanya adalah:

- **Kebutuhan Kompatibilitas**: Jika Anda perlu mendukung peramban lama dan beragam, jQuery mungkin lebih sesuai karena abstraksi kompatibilitas yang kuat.
- **Kemahiran dan Pengalaman**: Jika Anda sudah terbiasa dengan JavaScript dan ingin menghindari dependensi tambahan, Fetch API mungkin menjadi pilihan yang baik.
- **Kinerja dan Kekelompokan**: Jika Anda ingin menjaga situs Anda tetap ringan dan tidak perlu semua fitur jQuery, Fetch API dapat menjadi solusi yang lebih efisien.

# Penjelasan Cara Penyelesaian Tugas 5
Cara pengimplementasian *checklist* untuk menyelesaikan Tugas 5: <br>
   Setelah mempelajari [Tutorial 4](https://pbp-fasilkom-ui.github.io/ganjil-2024/docs/tutorial-4), saya menyelesaikan Tugas 4 dengan mempelajari dari banyak sumber.<br>
   Berikut adalah *step-by-step* yang saya buat dengan menyesuaikan *checklist* yang ada pada berkas soal:
      
   - [x] Menambahkan bootstrap ke dalam website.
   - [x] Menambahkan navbar pada website.
   - [x] Menambahkan fitur `Edit` pada website.
   - [x] Membuat fungsi untuk menghapus produk.

## Manfaat dari setiap elemen selector dan kapan waktu yang tepat untuk menggunakannya
Selector yang berfungsi untuk mengatur bagaimana pada sebuah halaman HTML untuk di berikan style atau diberikan rules untuk di design.

1. Element Selector `(element)`: <br>
   Selector ini memilih semua elemen HTML dengan tag yang cocok.
   Contoh: `p` akan memilih semua elemen `<p>` dalam dokumen HTML.
   Waktu yang tepat: digunakan ketika ingin menerapkan gaya ke semua elemen dengan tag yang sama.
   
2. ID Selector `(#id)`: <br>
   Selector ini memilih elemen dengan atribut id tertentu. <br>
   Contoh: `#header` akan memilih elemen dengan `id="header"`. <br>
   Waktu yang tepat: digunakan ketika ingin menerapkan gaya ke elemen tertentu dengan ID unik. <br>

3. Class Selector `(.class)`: <br>
   Selector ini memilih elemen dengan atribut class tertentu. <br>
   Contoh: `.button` akan memilih semua elemen dengan `class="button"`. <br>
   Waktu yang tepat: digunakan ketika Anda ingin menerapkan gaya ke beberapa elemen dengan class yang sama. <br>
   
4. Universal Selector `(*)`: <br>
   Selector ini memilih semua elemen dalam dokumen. <br>
   Contoh: `*` akan memilih semua elemen HTML dalam dokumen. <br>
   Waktu yang tepat: digunakan dengan hati-hati karena dapat mempengaruhi semua elemen dalam dokumen. <br>

5. Attribute Selector `([attribute])`: <br>
   Selector ini memilih elemen dengan atribut yang ditentukan, tanpa memperhatikan nilainya. <br>
   Contoh: `[target]` akan memilih semua elemen dengan atribut target, seperti `<a target="_blank">`. <br>
   Waktu yang tepat: digunakan ketika ingin menerapkan gaya kepada elemen dengan atribut tertentu, terlepas dari nilainya. <br>

## HTML5 Tag yang digunakan pada tugas 5.

|    Nama Tag      |              Keterangan/Kegunaan            |
|------------------|---------------------------------------------|
| `<!DOCTYPE>`     | Tag untuk menentukan tipe dokumen           |
| `<html>`         | Tag untuk membuat sebuah dokumen HTML       |   
| `<title>`        | Tag untuk membuat judul dari sebuah halaman |
| `<body>`         | Tag untuk membuat tubuh dari sebuah halaman |
| `<h1> to <h6>`   | Tag untuk membuat heading                   |
| `<br>`	          | Memasukan satu baris putus                  |
| `<!--...-->`	    | Tag untuk membuat komentar                  | 

## Perbedaan antara margin dan padding
Pada dasarnya, margin adalah ruang di sekitar elemen dan padding mengacu pada ruang antara elemen dan konten di dalamnya. <br>

![image](https://github.com/syarna/Inventory_PBP/assets/112332315/17fc2c38-c645-440f-bd12-a1a22e1005e9)

Bisa kita lihat pada gambar diatas, Margin berada di luar dua elemen yang berdekatan. Setiap sisi elemen memiliki ukuran margin yang dapat kamu ubah satu per satu. Dalam menciptakan celah, margin mendorong elemen yang berdekatan menjauh.<br>
Di sisi lain, padding ditempatkan di dalam batas elemen. Untuk membuat celah tersebut, padding dapat memperbesar ukuran elemen atau memperkecil konten di dalamnya. Secara default, ukuran elemen meningkat.<br>
Jadi, ada 2 buah kotak yang didalamnya terdapat teks, nah jika kamu ingin memberikan jarak antara teks dengan kotak nya, sehingga terdapat ruang didalam kotak, itulah Padding. Jika kamu ingin memberikan jarak antara kedua buah kotak tersebut, sehingga tidak berdempetan, itulah Margin.<br>
Berikut Contoh nya :

![image](https://github.com/syarna/Inventory_PBP/assets/112332315/63d244c6-0129-4f72-b2cd-296b7bc0f6bd)

## Perbedaan antara framework CSS Tailwind dan Bootstrap. Kapan sebaiknya kita menggunakan Bootstrap daripada Tailwind, dan sebaliknya

- DESAIN
  - Bootstrap menawarkan set class CSS dan komponen yang telah dirancang sebelumnya dengan tampilan yang cukup terstruktur dan konsisten. Ini cocok untuk proyek dengan desain tradisional yang membutuhkan kerangka kerja yang stabil dan mudah digunakan.
  - Tailwind menganut pendekatan yang lebih "utility-first", di mana kita membangun antarmuka dengan menggabungkan class utilitas yang lebih kecil. Ini memberikan kebebasan kreatif yang lebih besar dan memungkinkan penggunaan class yang sangat spesifik.

- FLEKSIBILITAS
  - Bootstrap menawarkan kerangka kerja yang relatif terstruktur dengan banyak komponen yang telah dirancang sebelumnya. Ini memberikan stabilitas dan kemudahan penggunaan, tetapi mungkin memiliki batasan dalam hal fleksibilitas desain yang unik.
  - Tailwind memberikan fleksibilitas yang lebih besar dengan pendekatan "utility-first" yang memungkinkan kita membangun desain yang sangat kustom sesuai kebutuhan. kita memiliki kendali penuh atas gaya dan tata letak dengan kombinasi class utilitas yang spesifik.

- UKURAN FILE
  - Bootstrap adalah kerangka kerja yang lebih besar dalam hal ukuran file karena menyediakan banyak fitur dan komponen yang siap pakai. Ini mungkin berdampak pada kecepatan pengunduhan dan performa halaman web.
  - Tailwind dirancang untuk lebih ringan dalam hal ukuran file. Namun, ketika kita menggunakan banyak class utilitas dalam kode, ukuran file CSS dapat meningkat.

- EKOSISTEM PENGEMBANGAN
  - Bootstrap memiliki ekosistem yang sangat kuat dengan dokumentasi yang kaya, banyak tema dan template yang tersedia, serta dukungan komunitas yang luas. Ini membuatnya mudah untuk memulai dan mendapatkan sumber daya yang diperlukan.
  - Tailwind juga memiliki ekosistem yang berkembang pesat dengan dokumentasi yang baik dan komunitas yang aktif, kita dapat menemukan banyak sumber daya, plugin, dan integrasi dengan kerangka kerja JavaScript seperti React atau Vue.

# Penjelasan Cara Penyelesaian Tugas 4
Cara pengimplementasian *checklist* untuk menyelesaikan Tugas 4: <br>
   Setelah mempelajari [Tutorial 3](https://pbp-fasilkom-ui.github.io/ganjil-2024/docs/tutorial-3), saya menyelesaikan Tugas 4 dengan mempelajari dari banyak sumber.<br>
   Berikut adalah *step-by-step* yang saya buat dengan menyesuaikan *checklist* yang ada pada berkas soal:
      
   - [x] Membuat fungsi dan form registrasi.
   - [x] Membuat fungsi login dan logout.
   - [x] Merestriksi akses halaman main.
   - [x] Menggunakan data dari cookies
   - [x] Menghubungkan model Product dengan User

##  Apa itu Django UserCreationForm, dan jelaskan apa kelebihan dan kekurangannya?
Django UserCreationForm adalah salah satu bentuk formulir bawaan yang disediakan oleh Django, sebuah framework web Python yang populer, untuk memudahkan proses pembuatan dan pendaftaran pengguna (user) di aplikasi web. Formulir ini secara khusus dirancang untuk membuat pengguna baru dengan informasi yang diperlukan, seperti nama pengguna (username), kata sandi (password), dan konfirmasi kata sandi. UserCreationForm biasanya digunakan bersama dengan Django's authentication system, yang mengelola otentikasi pengguna dan otomatisasi tugas-tugas terkait keamanan seperti penyimpanan kata sandi dalam bentuk terenkripsi.

Kelebihannya yaitu mudah digunakan, validasi formulir secara otomatis, memiliki langkah-langkah keamanan yang kuat yang terkait dengan otentikasi pengguna, dan costumizeable.
Kekurangannya yaitu keterbatasan desain, memerlukan lebih banyak fitur otentikasi kustom yang tidak dapat diakses melalui UserCreationForm, dan perawatan manual.


## Apa perbedaan antara autentikasi dan otorisasi dalam konteks Django, dan mengapa keduanya penting?
**Autentikasi** adalah proses untuk memverifikasi identitas pengguna. Ini digunakan untuk memastikan bahwa seseorang adalah pengguna yang dia klaim sebagai, biasanya dengan menggunakan kombinasi nama pengguna (username) dan kata sandi (password).Autentikasi digunakan untuk mengidentifikasi pengguna dan memastikan bahwa mereka memiliki hak akses ke sistem atau aplikasi.Django memiliki sistem autentikasi bawaan yang mengelola pendaftaran pengguna, masuk (login), dan keluar (logout) dari sistem. Ini memungkinkan pengguna untuk mengidentifikasi diri mereka sendiri dengan akun mereka.

**Otorisasi** adalah proses untuk mengontrol akses pengguna terhadap sumber daya atau tindakan tertentu setelah mereka berhasil diautentikasi. Ini menentukan apa yang dapat dilakukan atau diakses oleh pengguna yang terautentikasi.Otorisasi digunakan untuk memutuskan hak akses pengguna terhadap fitur atau data aplikasi. Ini menjawab pertanyaan seperti "Apakah pengguna ini memiliki izin untuk melakukan tindakan tertentu?". Django memiliki sistem otorisasi yang memungkinkan Anda untuk menentukan izin (permissions) yang diberikan kepada pengguna, baik secara individu maupun melalui grup. Anda dapat mengontrol akses pengguna ke tampilan (views), objek model, atau bagian-bagian lain dari aplikasi Anda.

Keduanya sangatlah penting karena Autentikasi membantu melindungi aplikasi dari akses tidak sah, sementara otorisasi memastikan bahwa pengguna hanya dapat mengakses sumber daya yang sesuai dengan peran atau izin mereka. Otorisasi memungkinkan pengembang untuk mengendalikan tingkat akses yang berbeda untuk pengguna yang berbeda. Ini penting ketika Anda memiliki pengguna dengan peran yang berbeda, seperti pengguna biasa dan administrator. Kombinasi autentikasi dan otorisasi membantu memastikan kepatuhan dengan aturan keamanan dan privasi yang berlaku, serta mencegah pengguna yang tidak sah mengakses atau memanipulasi data.

## Apa itu cookies dalam konteks aplikasi web, dan bagaimana Django menggunakan cookies untuk mengelola data sesi pengguna?
Cookies adalah file teks kecil yang disimpan di komputer atau perangkat pengguna ketika mereka berinteraksi dengan situs web. Cookies digunakan oleh server web untuk menyimpan informasi di sisi klien, yang dapat digunakan kembali saat pengguna mengunjungi situs web tersebut nanti. Cookies digunakan untuk berbagai tujuan dalam aplikasi web, seperti mengidentifikasi pengguna yang telah masuk (login), menyimpan preferensi pengguna, melacak sesi pengguna, dan menganalisis perilaku pengguna.

Cara Django menggunakan cookies yaitu Django menyediakan pustaka Python yang memudahkan penggunaan cookies. Anda dapat menggunakan modul django.http.HttpResponse untuk menetapkan, mengambil, atau menghapus cookies. Saat pengguna berhasil masuk, Anda dapat mengatur cookie sesi dengan menggunakan request.session dalam view Django. Misalnya, Anda dapat menggunakan request.session['nama_kunci'] = 'nilai' untuk menyimpan data sesi. Django juga secara otomatis menyediakan sistem untuk mengelola cookie autentikasi. Setelah pengguna masuk, cookie autentikasi akan digunakan untuk mempertahankan sesi login mereka.

## Apakah penggunaan cookies aman secara default dalam pengembangan web, atau apakah ada risiko potensial yang harus diwaspadai?
Penggunaan cookies dalam pengembangan web dapat menjadi alat yang aman jika digunakan dengan benar, tetapi juga memiliki risiko potensial yang harus diwaspadai seperti resiko keamanan, privasi pengguna, kekuatan enkripsi, kelemahan browser dan management cookies yang buruk.

# Penjelasan Cara Penyelesaian Tugas 3
Cara pengimplementasian *checklist* untuk menyelesaikan Tugas 3: <br>
   Setelah mempelajari [Tutorial 2](https://pbp-fasilkom-ui.github.io/ganjil-2024/docs/tutorial-2), saya menyelesaikan Tugas 3 dengan mempelajari dari banyak sumber.<br>
   Berikut adalah *step-by-step* yang saya buat dengan menyesuaikan *checklist* yang ada pada berkas soal:
   
   - [x] Buat berkas baru pada direktori `main` dengan nama `forms.py` untuk membuat struktur form yang dapat menerima data produk baru.
   - [x] Mengubah fungsi `show_main` yang sudah ada pada berkas `views.py`.
   - [x] Membuat sebuah fungsi yang menerima parameter request dengan nama `show_xml`, `show_json`,`show_xml_by_id` dan `show_json_by_id`.
   - [x] Mengatur routing pada masing-masing views.
  
## Perbedaan antara `POST` dan `GET` dalam django
1. Metode Pengiriman Data: <br>
   - **GET**:<br>
     Ketika Anda menggunakan metode GET, data formulir disertakan dalam URL sebagai query string. Ini berarti bahwa data formulir akan terlihat langsung di URL dan dapat dengan mudah diakses oleh pengguna atau oleh siapa pun yang melihat URL tersebut. Metode ini cocok untuk permintaan yang bersifat idempoten (artinya, permintaan dapat diulang tanpa efek samping) dan ketika Anda ingin mengirimkan data ke server untuk pencarian atau pengambilan sederhana.<br> Contoh URL dengan metode GET:<br>
   ```bash
   https://example.com/search/?q=query&category=books
   ```
   - **POST**:<br>
     Ketika Anda menggunakan metode POST, data formulir disertakan dalam badan permintaan HTTP, dan tidak terlihat langsung di URL. Oleh karena itu, data ini tidak mudah terlihat oleh pengguna atau siapa pun yang melihat URL. Metode ini lebih cocok untuk pengiriman data yang bersifat sensitif atau ketika Anda ingin mengirim data ke server untuk membuat, memperbarui, atau menghapus entitas di server.<br>

2. Jumlah Data yang Dapat Dikirim:
   - **GET**:<br>
     Metode GET memiliki batasan pada jumlah data yang dapat dikirim, karena data dikirim melalui URL. Banyak server web dan browser memiliki batasan panjang URL, dan jika data formulir terlalu besar, Anda mungkin mengalami masalah.
   - **POST**:<br>
     Metode POST tidak memiliki batasan pada jumlah data yang dapat dikirim, karena data dikirim dalam badan permintaan HTTP yang terpisah dari URL.

3. Keamanan:
   - **GET**:<br>
     Data formulir dalam metode GET terlihat di URL, yang berarti data tersebut kurang aman dan dapat dengan mudah diakses oleh pengguna atau pihak ketiga. Oleh karena itu, metode GET tidak cocok untuk mengirim data sensitif seperti kata sandi.
   - **POST**:<br>
     Data formulir dalam metode POST tidak terlihat di URL, sehingga lebih aman daripada GET untuk mengirim data sensitif. Namun, ini bukan jaminan keamanan lengkap, dan Anda harus selalu mengimplementasikan langkah-langkah keamanan tambahan seperti penggunaan HTTPS.

## Perbedaan utama antara XML, JSON, dan HTML dalam konteks pengiriman data
XML *(Extensible Markup Language)*, JSON *(JavaScript Object Notation)*, dan HTML *(Hypertext Markup Language)* adalah tiga format yang berbeda untuk mengirim data dalam konteks yang berbeda. Berikut adalah perbedaan utama antara ketiganya dalam konteks pengiriman data:

1. Tujuan Utama:
   - **XML**:<br>
     XML digunakan terutama untuk pertukaran data yang struktural dan semantik, terutama antara aplikasi atau sistem yang berbeda. Ini adalah format yang serbaguna dan dapat digunakan untuk menggambarkan data dengan hierarki yang kompleks dan semantik yang kuat. XML juga sering digunakan dalam konfigurasi dan penyimpanan data.
   - **JSON**:<br>
     JSON awalnya dikembangkan untuk pertukaran data di antara aplikasi web dan server, khususnya dalam konteks JavaScript. Ini adalah format yang ringkas dan mudah dibaca/ditulis oleh manusia, yang membuatnya cocok untuk pertukaran data antara aplikasi web. JSON juga digunakan secara luas untuk penyimpanan data di berbagai aplikasi.
   - **HTML**:<br>
     HTML adalah bahasa markah yang digunakan untuk menggambarkan struktur dan tampilan konten web. HTML tidak digunakan secara eksplisit untuk pertukaran data terstruktur, meskipun data dapat dimasukkan dalam elemen HTML dengan atribut seperti data-*.

2. Struktur Data:
   - **XML**:<br>
     XML memiliki struktur yang sangat fleksibel dan kuat. Data dalam XML dijelaskan oleh dokumen yang dapat memiliki elemen-elemen bersarang dengan atribut dan teks.
   - **JSON**:<br>
     JSON memiliki struktur yang lebih sederhana dibandingkan XML. Data dalam JSON direpresentasikan dalam bentuk pasangan "kunci-nilai" (key-value) dalam bentuk objek atau dalam bentuk array. Ini membuat JSON lebih sederhana untuk diuraikan dan digunakan oleh aplikasi.
   - **HTML**:<br>
     HTML memiliki struktur yang ditentukan oleh elemen-elemen HTML, seperti `<p>`, `<div>`,`<table>`, dan lainnya, yang digunakan untuk mengatur tampilan dan konten halaman web.

3. Penggunaan Khusus:
   - **XML**:<br>
     XML digunakan dalam berbagai konteks, termasuk pertukaran data lintas platform, konfigurasi aplikasi, penyimpanan data berstruktur, dan banyak lagi.
   - **JSON**:<br>
     JSON adalah format yang sangat umum digunakan dalam pengembangan web modern. Ini digunakan untuk pertukaran data antara server dan aplikasi web, penyimpanan data di database NoSQL seperti MongoDB, dan banyak lagi.
   - **HTML**:<br>
     HTML digunakan secara khusus untuk menggambarkan struktur dan tampilan halaman web. Ini adalah bahasa yang digunakan oleh browser web untuk merender halaman web.

4. Contoh Representasi:
   - **XML**:
      ```bash
       <person>
        <name>John Doe</name>
        <age>30</age>
      </person>
      ```
   - **JSON**:
      ```bash
       {
        "person": {
         "name": "John Doe",
          "age": 30
        }
      }
     ```
   - **HTML**:
     ```bash
     <p>Hello, World!</p>
     ```

## Mengapa JSON sering digunakan dalam pertukaran data antara aplikasi web modern?
1. Ringkas dan Mudah Dibaca: <br>
   Memiliki sintaks yang sederhana dan mudah dipahami oleh manusia. Data dalam JSONdirepresentasikan dalam bentuk pasangan "kunci-nilai" (key-value), yang membuatnya lebih mudah dibaca dan ditulis dibandingkan dengan format lain yang lebih kompleks seperti XML. Ini memungkinkan pengembang untuk dengan cepat memahami struktur data yang dikirim dan diterima.
   
2. Ringan:<br>
   Format data yang ringan dalam hal ukuran. Ini menghasilkan payload yang lebih kecil daripada format lain seperti XML, yang mengurangi penggunaan bandwidth dan meningkatkan kinerja transfer data, khususnya dalam lingkungan web dengan koneksi yang terbatas atau lambat.

3. Dukungan untuk Struktur Bersarang:<br>
   Memungkinkan untuk merepresentasikan data yang kompleks dengan cara yang terorganisir. 
   
5. Dukungan untuk Tipe Data Umum:<br>
   Tipe data umum seperti string, angka, boolean, array, dan objek. Ini memungkinkan untuk merepresentasikan berbagai jenis data dengan mudah. Selain itu, JSON memiliki dukungan yang baik untuk nilai-nilai null.
   
6. Kemampuan untuk Diproses di Sisi Klien:<br>
   JSON cocok dengan baik dengan bahasa pemrograman JavaScript, yang digunakan secara luas di sisi klien (browser web). Oleh karena itu, data JSON dapat dengan mudah diproses oleh JavaScript di dalam browser, membuatnya sangat sesuai untuk aplikasi web yang berinteraksi dengan server.

7. Dukungan di Banyak Bahasa Pemrograman:<br>
   Selain JavaScript, hampir semua bahasa pemrograman modern memiliki dukungan JSON yang baik. Ini membuatnya mudah untuk mengirim dan menerima data JSON di berbagai platform dan teknologi.

8. Standar Industri:<br>
   JSON telah menjadi standar de facto dalam pertukaran data di lingkungan web. Banyak API web dan layanan daring menggunakan JSON sebagai format data standar, sehingga memudahkan integrasi dan interoperabilitas antara berbagai sistem.
   
9. Sistem yang Mudah Dikelola:<br>
   JSON adalah format data yang mudah dikelola, baik dalam hal pembuatan, pemrosesan, atau pemecahan masalah. Ini membuatnya cocok untuk pengembangan dan pemeliharaan aplikasi web. Karena kombinasi dari keunggulan-keunggulan ini, JSON telah menjadi pilihan yang populer dan dominan dalam pertukaran data antara aplikasi web modern, baik dalam konteks API web, pertukaran data antara server dan klien, maupun penyimpanan data di database NoSQL seperti MongoDB.

## Screenshoot Hasil Akses URL pada Postman:
<img width="1440" alt="Screenshot 2023-09-20 at 10 28 19" src="https://github.com/syarna/Inventory_PBP/assets/112332315/e1bbb1f7-196b-4644-886d-2bbf91c789c2">
<img width="1440" alt="Screenshot 2023-09-20 at 10 28 02" src="https://github.com/syarna/Inventory_PBP/assets/112332315/5b991b5a-8739-4963-8b22-9add1a726dff">
<img width="1440" alt="Screenshot 2023-09-20 at 10 27 49" src="https://github.com/syarna/Inventory_PBP/assets/112332315/e33df3c8-b931-412a-821f-1b9ea40e9db7">
<img width="1440" alt="Screenshot 2023-09-20 at 10 27 31" src="https://github.com/syarna/Inventory_PBP/assets/112332315/c8876bfc-2dd6-4166-90aa-923accf6ad20">
<img width="1440" alt="Screenshot 2023-09-20 at 10 27 21" src="https://github.com/syarna/Inventory_PBP/assets/112332315/bb0067d7-8a6b-461d-86ff-a7faafd563f8">

# Penjelasan Cara Penyelesaian Tugas 2
Cara pengimplementasian *checklist* untuk menyelesaikan Tugas 2: <br>
   Setelah mempelajari [Tutorial 0](https://pbp-fasilkom-ui.github.io/ganjil-2024/docs/tutorial-0) dan [Tutorial 1](https://pbp-fasilkom-ui.github.io/ganjil-2024/docs/tutorial-1), saya menyelesaikan Tugas 2 dengan mempelajari dari banyak sumber.<br>
   Berikut adalah *step-by-step* yang saya buat dengan menyesuaikan *checklist* yang ada pada berkas soal:
   - [x] Mengaktifkan *virtual environtment* untuk mengisolasi package serta dependencies dari aplikasi sehingga tidak bertabrakan dengan versi lain yang ada pada komputer.
   - [x] Membuat proyek Django baru untuk menciptakan situs web.
   - [x] Membuat aplikasi `main` agar aplikasi dapat memiliki model, tampilan, template, dan URL yang terkait dengannya. Aplikasi memungkinkan kita untuk membagi fungsionalitas proyek menjadi bagian-bagian terpisah yang dapat dikelola secara independen.
   - [x] Membuat atribut wajib seperti `name`,`amount` dan `description` sesuai dengan tipe *field* yang telah ditentukan.
   - [x] Mengatur routing URL agar aplikasi `main` dapat diakses melalui peramban web.
   - [x] Menjalankan server untuk mengecek apakah hasil website sudah sesuai dengan ketentuan.
   - [x] Melakukan deploy ke [Adaptable](https://adaptable.io) untuk meng-*hosting* website.
   
## Bagan yang berisi request client ke web aplikasi berbasis Django beserta responnya:
![Bagan Django](https://github.com/syarna/Inventory_PBP/assets/112332315/0a3442b5-4152-4171-9dac-3d7ea3f3b9f7)<br>

Setiap request yang datang dari client (browser) akan dipetakan oleh URLS dan akan diteruskan ke View yang mana View akan memroses request tersebut. View akan memanggil Model untuk melakukan proses membaca atau menulis data ke Database. Setelah itu View akan memanggil template untuk merender data dalam format tertentu(html, xml, json) dan mengirimkan kembali hasilnya dalam bentuk HTTP Response ke client.
   
## Alasan untuk menggunakan ***vitual environment***:
Untuk menjaga ruang terpisah untuk sebuah proyek dengan pustaka dan dependensi di satu tempat. Environment ini spesifik ke proyek tertentu dan tidak berinterfer dengan dependensi proyek lainnya.

## Apakah itu MVC, MVT, MVVM dan perbedaan dari ketiganya?
* **MVC** atau yang biasa disebut **Model-View-Controller** adalah suatu model yang seringkali digunakan oleh para pengembang software. Komponen-komponen di dalam arsiteuktur ini yaitu sebagai berikut.
  * Model: Di dalam komponen ini berisi tentang logika bisnis dan status data yang ada di dalam aplikasi. Kompnen ini bertugas untuk mendapatkan dan memanipulasi data, berkomunikasi dengan controller, berinteraksi dengan database, terkadang memperbarui tampilan dari aplikasi yang dikembangkan.
    Di dalam komponen ini berisi tentang logika bisnis dan status data yang ada di dalam aplikasi. Kompnen ini bertugas untuk mendapatkan dan memanipulasi data, berkomunikasi dengan controller, berinteraksi dengan database, terkadang memperbarui tampilan dari aplikasi yang dikembangkan.

  * View: Komponen ini berhubungan dengan antarmuka pengguna yang terdiri dari HTML/CSS.XML. Komponen ini berkomunikasi dengan pengontrol dan terkadang berinteraksi dengan model. View berkerja sama dengan controller untuk menciptakan tampilan dinamis pada aplikasi yang dikembangkan. Selain bertugas untuk menangani antarmuka dan interaksi pengguna, komponen view juga memiliki tugas untuk menyajikan data yang sesuai untuk pengguna.
    
  * Controller: Controller adalah suatu aktivitas/fragmen yang berfungsi sebagai komunikator antara view dan model. Komponen ini membutuhkan suatu input pengguna dari layanan view/REST. Lalu Permintaan “Get Data” diproses dari model dan diteruskan ke view untuk ditampilkan ke pengguna.

  * Kelebihan **MVC**:<br>
    + MVC membuat logika bisnis terpisah dalam Model.
    + Mendukung teknik asynchronous.
    + Jika terjadi suatu modifikasi, maka tidak akan mempengaruhi keseluruhan Model.
    + Proses pengembangan aplikasi yang dilakukan dapat lebih cepat.

  * Kekurangan **MVC**: <br>
    - Arsitektur ini dapat meningkatkan kompleksitas.
    - Pengujian unit terhalang.
    - Controller kode yang besar yang membuat pengembang tidak bisa mengelolahnya.

* **MVT** adalah singkatan dari **Model-View-Template** adalah sebuah konsep arsitektur yang digunakan dalam pengembangan web untuk memisahkan komponen-komponen utama dari sebuah aplikasi. Konsep ini memungkinkan pengembang web untuk mengorganisasi dan mengelola kode dengan lebih terstruktur.
  * **Model**: komponen dalam konsep MVT yang bertanggung jawab untuk mengatur dan mengelola data dari aplikasi. Model mewakili struktur data dan logika aplikasi yang berada di belakang tampilan. Model menghubungkan aplikasi dengan basis data dan mengatur interaksi dengan data tersebut.
    
  * **View**: komponen yang menangani logika presentasi dalam konsep MVT. View mengontrol bagaimana data yang dikelola oleh model akan ditampilkan kepada pengguna. Dalam konteks MVT, view berperan sebagai pengatur tampilan dan mengambil data dari model untuk disajikan kepada pengguna.

  * **Template**: komponen yang berfungsi untuk mengatur tampilan atau antarmuka pengguna. Template memisahkan kode HTML dari logika aplikasi. Dalam MVT, template digunakan untuk merancang tampilan yang akhirnya akan diisi dengan data dari model melalui view.

  * Kelebihan **MVT**:
    + Memisahkan tugas antara logika aplikasi, tampilan, dan data, sehingga memungkinkan pengembang untuk bekerja pada setiap komponen secara terpisah.
    + Kode yang Mudah Dikelola
    + Kode dapat digunakan kembali dalam berbagai bagian aplikasi yang berbeda.
    + Struktur MVT mendukung skalabilitas dengan memungkinkan pengembangan paralel pada setiap komponen.

* **MVVM** atau **Model-View-ViewModel** yang merupakan gabungan dari MVC dan MVP. MVVM awalnya digunakan di dalam Windows Presentation Foundation (WPF) dan Silverlight, yang secara resmi diumumkan pada tahun 2005 oleh John Grossman dalam sebuah posting blog tentang Avalon. Pola yang digunakan berdasarkan gabungan dari MVC dan MVP mencoba untuk lebih jelas dalam memisahkan pengembangan UI dari logika bisnis dan perilaku dalam aplikasi.

  * Model: digunakan untuk MVVM mirip dengan model yang digunakan MVC, dimana model tersebut terdiri dari data dasar yang digunakan untuk menjalankan perangkat lunak.

  * View: digunakan sebagai antarmuka grafis antara pengguna dan pola desain, serta menampilkan output dari data yang telah diproses. View yang digunakan MVVM mirip dengan View yang digunakan dalam MVC.

  * ViewModel: di satu sisi adalah abstraksi dari View, lalu di sisi yang lain, sebagai penyedia pembungkus data model untuk ditautkan. ViewModel terdiri dair Model yang diubah menjadi View, dan berisi perintah yang dapat digunakan oleh View untuk mempengaruhi Model.

  * Kelebihan **MVVP**:
    + Tidak memiliki hubungan (ketergantungan) antara View dan ViewModel.
    + Tidak ada antarmuka antara View dan Model.
    + Pengujian unit yang mudah dan kode yang digerakkan oleh peristiwa (event-driven).
      
  * Kekurangan **MVVP**:
    - Pengembang harus membuat suatu kuantitas yang dapat diukur di setiap komponen UI.
    - Ukuran kode yang terlalu besar.
