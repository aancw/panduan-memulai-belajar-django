# 1.0 Apa itu Django?

Django merupakan Free dan Open Source Web Framework yang dibangun menggunakan bahasa Python. Sebuah web framework yang didalamnya sudah terdapat komponen untuk lebih mempercepat dan memudahkan web development. Arsitektur yang digunakan oleh Django adalah model-template-view\(MTV\).

* Model adalah lapisan akses data. Pada lapisan ini terdapat tentang apa saja sebuah data itu: bagaimana cara akses, bagaimana cara validasi dan lain-lain.

* Template adalah lapisan representasi. Pada lapisan ini terdapat presentasi tentang bagaimana seharusnya web tersebut ditampilan.

* View adalah lapisan yang berurusan dengan logika. Pada lapisan ini terdapat logika yang dapat mengakses model dan juga template. Bisa juga disebut sebagai jembatan antara model dan template.

# 1.1 Kenapa Django?

* **Rapidly**

Django telah dirancang untuk membantu developer membuat aplikasi dari konsep sampai selesai secepat mungkin.

* **Flexible**

Django cocok digunakan untuk skala project kecil hingga skala project besar.

* **Fully Loaded**

Django menyediakan banyak komponen yang dibutuhkan untuk development aplikasi web atau pun mobile. Django itu sendiri lebih lengkap dibandingkan dengan framework python lain nya.

* **Cross-Plaftorm**

Karena Django ini menggunakan Python, dan kita tahu bahwa python ini bisa berjalan pada platform apapun yang sudah terpasang python.

* **Django menggunakan prinsip D.R.Y: Don’t Repeat Yourself**

![](/assets/dont-repeat-yourself.jpg)

* **Good Documentation**

Django memiliki web dengan dokumentasi yang sangat lengkap dan terstruktur. Sangat cocok untuk yang sedang belajar untuk tahap awal. Juga disediakan code examples sebagai bahan belajar.

* **Secure**

Sebenarnya Secure ini relatif dan tidak mutlak karena tidak ada sistem yang aman. Namun, Django sudah include pengamanan untuk serangan umum seperti : SQL Injection, XSS, CSRF dan clickjacking. Bisa juga menggunakan Middleware Django untuk membantu Securing Django Project seperti pada repo berikut: [https://github.com/sdelements/django-security](https://github.com/sdelements/django-security)

