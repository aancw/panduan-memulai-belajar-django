## 4.1 Membuat View

Untuk pembuatan _view_ kita perlu membuat berkas kosong terlebih dahulu bernama `views.py` pada direktori inti sebuah project yang sudah dijelaskan sebelumnya( _djangotutorial/djangotutorial/views.py_ ) seperti berikut:

```py
from django.http import HttpResponse

def hello_sinau(request):
  return HttpResponse("Hello World, Welcome to Sinau Development!")
```

Bila dijabarkan dengan penjelasan akan seperti berikut:

* Pertama, kita melakukan import class `HttpResponse` yang berada pada modul `django.http`, kita perlu melakukan import class tersebut karena kita akan menggunakan fungsi yang ada didalamnya pada contoh kali ini.

* Kedua, kita melakukan pendefinisian terhadap fungsi yang bernama `hello_sinau` dengan parameter berupa `request`. Setiap views dibutuhkan setidaknya 1 parameter. Nah, kita disini menggunakan request sebagai parameter dikarenakan `request` merupakan sebuah object yang menyimpan informasi tentang Web Request. Pada kasus ini kita tidak akan melakukan apapun terhadap request karena masih belum dibutuhkan.

* Ketiga, kita mengembalikan nilai berupa `HttpResponse` yang berisi `Hello World, Welcome to Sinau Development!`
    
Agar views yang kita buat dapat berjalan, kita perlu melakukan konfigurasi pada URLConf. Bila kita menjalankan perintah `python manage.py runserver` maka yang akan tampil masihlah tampilan dari **Welcome Django**.
