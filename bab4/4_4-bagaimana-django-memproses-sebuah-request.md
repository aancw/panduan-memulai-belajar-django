## 4.4 Bagaimana Django Memproses Sebuah Request

Pada bagian ini, kita akan mempelajari sekilas tentang bagaimana Django memproses sebuah request yang dikirimkan oleh browser ketika kita mengakses laman tertentu seperti misalnya [http://127.0.0.1/hello](http://127.0.0.1/hello) yang akan menampilkan "Hello World, Welcome to Sinau Development!" . Semua itu berawal dari berkas _settings_ pada sebuah project.

Ketika kita menjalankan perintah `python manage.py runserver` , maka akan mencari berkas `settings.py` yang berada didalam direktori `djangotutorial` yang berlokasi di `djangotutorial/djangotutorial/settings.py`.

Pada berkas ini terdapat konfigurasi inti dari sebuah Django project yang dimana ditulis dengan huruf kapital. Contohnya `BASE_DIR`,`SECRET_KEY`,`ROOT_URLCONF`,`TEMPLATES` dan lain-lain. Nah `ROOT_URLCONF` merupakan hal yang paling penting, karena pada konfigurasi tersebut menyebutkan dimana modul yang dijadikan sebagai site root yang sudah kita bahas pada bagian sebelumnya.

```py
ROOT_URLCONF = 'djangotutorial.urls'
```
Ketika terjadi sebuah request pada Django, sebagai contoh ke `/hello/` maka Django me-load URLConf ke konfigurasi ROOT_URLCONF dan kemudian melakukan cek terhadap semua isi URLpatterns yang terdapat pada URLConf untuk melakukan pembandingan sebuah alamat URL.

Disaat sudah ditemukan yang cocok, maka Django akan memanggil fungsi view yang terkait dengan pattern tersebut. Seperti yang sudah dijelaskan sebelumnya bahwa view memanggil fungsi yang mengembalikan nilai berupa HttpResponse.

Setelah itu, Django akan melakukan konversi Python object menjadi Web Response dengan HTTP headers dan body yang sesuai.