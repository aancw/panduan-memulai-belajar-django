# 4.0 Membuat Example Hello World Site

Seperti yang sudah dijelaskan sebelumnya bahwa URLConf adalah konfigurasi URL untuk Django, mungkin bila disamakan dengan CodeIgniter merupakan `route` config. Untuk memanggil fungsi view `hello_sinau` yang berada pada views.py kita harus melakukan perubahan pada URLConf dalam bekas urls.py menjadi seperti berikut:

```
from django.conf.urls import include,url
from django.contrib import admin
from djangotutorial.views import hello_sinau

urlpatterns = [
    url(r'^admin/', admin.site.urls),
    url(r'^hello/$', hello_sinau),
]

```

Penjelasan:

- Kita melakukan import untuk hello_sinau views yang ada pada modul djangotutorial/views.py
- Kita menambahkan `url(r'^hello/$', hello_sinau)` ke urlpatterns, fungsi ini ditujukan untuk memberitahu Django tentang URL yang sudah dikonfigurasikan. Argumen pertama merupakan pattern-matching berupa RegExp yang dimulai dengan tanda '^' dan diakhiri dengan '$', dan yang kedua merupakan fungsi view yang kita panggil dari berkas views.py.

Satu lagi yang penting adalah 'r' dimana karakter tersebut memberitahukan bahwa string merupakan 'raw string'. Sila baca disini https://docs.python.org/2.0/ref/strings.html . Untuk RegExp sila baca disini https://docs.python.org/3.4/library/re.html

Ok, coba kita jalankan kembali `python manage.py runserver`, lalu akses http://127.0.0.1:8000/hello . Maka akan tampil seperti berikut:
