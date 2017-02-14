## 4.3 Sekilas Tentang Site Root

Seperti yang sudah dijelaskan dan praktekkan sebelumnya, bahwa kita akan mendapatkan pesan error '404 Not Found' ketika mengakses `site root` seperti `http://127.0.0.1:8000/`. Dikarenakan Django tidak mendefinisikan secara default untuk site root, maka kita diharuskan untuk melakukan pendefinisian pada URLConf sama seperti yang sudah dilakukan pada pembahasan sebelumnya.

Bila kita sudah membuat view baru untuk site root, maka langkah selanjutnya menambahkan URLpattern yang diawali dengan "^$" sebagai RegExp yang dimana memberitahukan bahwa tidak ada kata setelahnya.

```py
from django.conf.urls import include,url
from django.contrib import admin
from djangotutorial.views import hello_sinau, homepage

urlpatterns = [
    url(r'^admin/', admin.site.urls),
    url(r'^hello/$', hello_sinau),
    url(r'^$', welcome),
]
```
