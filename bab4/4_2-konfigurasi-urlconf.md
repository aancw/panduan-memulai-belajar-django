## 4.2 Konfigurasi URLConf

Bila kita menjalankan kembali `python manage.py runserver`, kita masih lah akan mendapatkan tampilan pesan "Welcome to Django". Karena kita belum melakukan pendefinisian view yang sudah kita buat sebelumnya.

Nah, kita perlu memberitahukan kepada Django bahwa kita sudah membuat view dengan spesifik URL. Kita akan menggunakan URLConf untuk melakukan pendefinisian view agar bisa diakses melalui URL yang telah didefinisikan. Sebagai contoh kita akan memanggil view `hello_sinau` disaat user mengakses URL `/hello/`.

Untuk memanggil fungsi view `hello_sinau` yang berada pada views.py kita harus melakukan perubahan pada URLConf dalam bekas urls.py menjadi seperti berikut:

```py
from django.conf.urls import include,url
from django.contrib import admin
from djangotutorial.views import hello_sinau

urlpatterns = [
    url(r'^admin/', admin.site.urls),
    url(r'^hello/$', hello_sinau),
]
```

Bila dijabarkan dengan penjelasan akan seperti berikut:

* Pertama, kita melakukan import untuk modul yang kita butuhkan. Pada 2 baris pertama melakukan import modul url dan admin. Dimana modul admin merupakan modul utama untuk default Django admin. Pada baris ketiga melakukan import untuk view `hello_sinau` yang ada pada modul `djangotutorial/views.py`

* Kedua, kita menambahkan `url(r'^hello/$', hello_sinau)` ke urlpatterns, fungsi ini ditujukan untuk memberitahu Django tentang URL yang sudah dikonfigurasikan. Argumen pertama merupakan pattern-matching berupa **RegExp** yang dimulai dengan tanda `^` dan diakhiri dengan `$`, dan yang kedua merupakan fungsi view yang kita panggil dari berkas views.py.

Satu lagi yang penting adalah `r` dimana karakter tersebut memberitahukan bahwa string merupakan `raw string`. Sila baca disini [https://docs.python.org/2.0/ref/strings.html](https://docs.python.org/2.0/ref/strings.html) dan untuk RegExp sila baca disini [https://docs.python.org/3.4/library/re.html  
](https://docs.python.org/3.4/library/re.html)

Mari kita jalankan kembali Django project dengan perintah `python manage.py runserver`. Bila kita akses pada halaman [http://127.0.0.1:8000/hello](http://127.0.0.1:8000/hello) maka akan tampil seperti berikut:

![](/assets/hello-world-django.png)

Wah. Sudah tampil Hello World? Horaaaaaai!
