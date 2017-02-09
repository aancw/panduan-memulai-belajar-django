# 2.0 Pemasangan Django

Karena Django ini menggunakan Python sebagai bahasa yang digunakan untuk membuat framework. Maka, pastikan terlebih dahulu bahwa kamu sudah memasang python. Kalau belum, silahkan unduh dan pasang sesuai distro masing-masing.

```
$ python
Python 3.5.2 (default, Nov  7 2016, 11:31:36)
[GCC 6.2.1 20160830] on linux
Type "help", "copyright", "credits" or "license" for more information.
```

Lalu pasang Django dengan menggunakan pip, karena itu merupakan cara termudah yang disediakan:

```
pip install django
```

Pada tulisan ini akan menggunakan Django 1.10 dengan menggunakan Python 3.5, lakukan pengecekan terlebih dahulu dengan menggunakan:

```
$ python
Python 3.5.2 (default, Nov  7 2016, 11:31:36)
[GCC 6.2.1 20160830] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import django
>>> print(django.get_version())
1.10.3
```

Bila versi Django yang terpasang versi nya kurang dari 1.10, lakukan upgrade python menjadi versi 3.x bila kamu menggunakan python versi 2.x. Untuk Arch Linux dengan python versi 2.x sudah mendapatkan Django versi 1.10.

```
$ python2
Python 2.7.12 (default, Nov  7 2016, 11:55:55)
[GCC 6.2.1 20160830] on linux2
Type "help", "copyright", "credits" or "license" for more information.
>>> import django
>>> print(django.get_version())
1.10.3
```

Atau bisa juga cek dengan menggunakan perintah:

```
python -m django --version
python2 -m django --version
```

Yey! Sekarang kita sudah berhasil memasang Django.

