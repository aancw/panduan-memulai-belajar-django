## 5.2 Apa itu App?

App merupakan bagian dari sebuah project yang kita buat. Tidak seperti Project yang bisa berjalan sendiri, App membutuhkan Project karena memang harus disatukan dengan Project. App dibuat untuk memenuhi fungsi tertentu dalam sebuah Project seperti : App Komentar, App file Uploader dsb. App ini pun bisa dipindah ke project lain ketika dibutuhkan. App bisa saling berhubungan/memerlukan dengan App lainnya dalam sebuah project. Yang dimana berarti relasi antara App dan Project adalah ketergantungan dan tidak bisa berjalan sendiri.

### Struktur Direktori Django Project dan App

```
$ django-admin startapp apptutorial

djangotutorial/
|-- djangotutorial
|   |-- __init__.py
|   |-- apptutorial
|   |   |-- __init__.py
|   |   |-- admin.py
|   |   |-- apps.py
|   |   |-- migrations
|   |   |   `-- __init__.py
|   |   |-- models.py
|   |   |-- tests.py
|   |   `-- views.py
|   |-- settings.py
|   |-- urls.py
|   `-- wsgi.py
`-- manage.py
```

Pada contoh diatas, kita membuat sebuah App yang bernama `apptutorial` didalam sebuah project `djangotutorial`.




