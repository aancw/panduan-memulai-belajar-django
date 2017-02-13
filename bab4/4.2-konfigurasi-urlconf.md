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



