# 3.0 Membuat Project Pertama Django

Setelah semua nya telah berhasil terpasang dan berjalan lancar. Tahap pertama yang akan kita lakukan adalah membuat project pertama Django kita. Caranya? Cukup ketikkan perintah:

```
django-admin startproject djangotutorial
```

Maka akan terbuat direktori _djangotutorial_ seperti berikut:

    djangotutorial/
    |-- djangotutorial
    |   |-- __init__.py
    |   |-- settings.py
    |   |-- urls.py
    |   `-- wsgi.py
    `-- manage.py

Yang dimana masing-masing tersebut adalah:

* **djangotutorial/ **adalah direktori inti yang memuat sebuah project. Perlu diketahui bahwa nama tersebut tidak berpengaruh sama sekali dengan Django, jadi bisa ubah sesuka hati
* **manage.py **sebuah utilitas yang digunakan untuk melakukan interaksi terhadap project Django dengan berbagai cara. Untuk lebih lengkapnya silahkan membaca [https://docs.djangoproject.com/en/1.10/ref/django-admin/](https://docs.djangoproject.com/en/1.10/ref/django-admin/)
* Direktori **djangotutorial/** kedua adalah Python package untuk project yang kita buat. Nama tersebut yang akan digunakan ketika melakukan import package \(cont: djangotutorial.urls\)
* **djangotutorial/\_\_init\_\_.py **adalah sebuah berkas kosong yang memberitahukan bahwa direktori tersebut merupakan Python package.
* **djangotutorial/settings.py **merupakan pengaturan atau konfigurasi untuk project Django itu sendiri. Lebih lengkap nya silahkan baca disini [https://docs.djangoproject.com/en/1.10/topics/settings/](https://docs.djangoproject.com/en/1.10/topics/settings/)
* **djangotutorial/urls.py** merupakan deklarasi URL untuk project Django; Berisi konfigurasi URL pada project yang kita buat. Akan kita bahas pada kesempatan selanjutnya untuk URL Dispatcher dan URLConf. Isi berkas urls.py:

  ```
  """djangotutorial URL Configuration
  The urlpatterns list routes URLs to views. For more information please see:
      
  https://docs.djangoproject.com/en/1.10/topics/http/urls/

    Examples:
    Function views
        1. Add an import:  from my_app import views
        2. Add a URL to urlpatterns:  url(r'^$', views.home, name='home')
    Class-based views
        1. Add an import:  from other_app.views import Home
        2. Add a URL to urlpatterns:  url(r'^$', Home.as_view(), name='home')
    Including another URLconf
        1. Import the include() function: from django.conf.urls import url, include
        2. Add a URL to urlpatterns:  url(r'^blog/', include('blog.urls'))
    """
    from django.conf.urls import include,url
    from django.contrib import admin
  urlpatterns = [
        url(r'^admin/', admin.site.urls),
    ]

  ```

* **djangotutorial/wsgi.py **merupakan dukungan kompatibilitas **WSGI** dengan web server untuk menjalankan project Django. Nantinya bisa diintegrasikan dengan menggunakan web server pada umumnya seperti apache, nginx dan lain-lain.

Django itu sendiri sudah menyediakan web server yang dibuat dengan Python untuk melakukan testing dalam masa development. Jadi memudahkan kita untuk development sebelum masuk kedalam server production. Perlu diingat bahwa web server yang disediakan tidak dianjurkan untuk digunakan pada masa production. Pada kesempatan selanjutnya akan membahas tentang integrasi antara WSGI dan web server.

Ok. Sekarang kita lakukan pengecekan untuk memastikan bahwa project Django kita berjalan dengan lancar. Lakukan perintah berikut di direktori utama yang sudah disebutkan diatas:

```
python manage.py runserver
```

Maka akan menampilkan pesan seperti berikut:

```
Performing system checks...

System check identified no issues (0 silenced).

You have 13 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.

November 30, 2016 - 01:06:48
Django version 1.10.3, using settings 'djangotutorial.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.
```

Abaikan peringatan yang menyebutkan bahwa ada beberapa bagian yang belum dimigrasi, karena memang kita belum saatnya melakukan itu. Pesan tersebut menyatakan bahwa project Django berjalan lancar dan bisa diakses melalui [http://127.0.0.1:8000](http://127.0.0.1:8000). Akan tampil seperti gambar berikut:

![](/assets/Django-first-app.png)

