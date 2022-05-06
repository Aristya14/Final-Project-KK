# Laravel Tutorial Controller
# Daftar Isi
1. [Pengertian](https://github.com/Aristya14/coba/blob/main/Laravel-Controller.md#pengertian)
2. [Langkah-Langkah](https://github.com/Aristya14/coba/blob/main/Laravel-Controller.md#Langkah-langkah)
3. [Konsep](https://github.com/Aristya14/coba/blob/main/Laravel-Controller.md#Konsep)

# Pengertian
Laravel Controller merupakan salah satu bagian dimana seluruh fungsional web dibuat. Pada Controller dilakukan pengaturan untuk mengakses Model terkait dengan Database dan juga bagaimana mengirimkan datanya ke View. Berbagai pemrosesan juga dilakukan di dalam Controller. Controller adalah salah satu komponen inti dari MVC yang berfungsi sebagai penghubung antara request user (View) ke model yang nantinya akan di kembalikan lagi ke View dalam bentuk response. Controller ini akan banyak berisi logika – logika dalam menyusun suatu fungsi tertentu. Contohnya adalah aktivitas CRUD (Create, Read, Update, Delete) yang prosesnya berjalan di dalam Controller.

# Konsep
Salah satu contoh aktivitas pada controller adalah aktivitas CRUD (Create, Read, Update, Delete).

# Langkah-Langkah
## Langkah Pertama : Membuat file Controller
Ada 2 cara dalam membuat controller pada laravel. Yang pertama, dengan cara membuat langsung file controller barunya di dalam folder app/Http/Controllers. Sedangkan cara yang kedua, dengan menggunakan perintah php artisan dari laravel.
### Cara Pertama : membuat file secara manual di dalam folder app/Http/Controllers
Kita langsung membuat file controller baru pada laravel dengan membuat langsung filenya di dalam folder controllers. Di sini kita akan mengikuti format penulisan pada laravel, jadi nama file controllernya dibuat dengan huruf besar di awal Controllernya. Misalnya kita akan membuat controller dosen, buat file baru dengan nama DosenController.php dalam folder controllers. Berikut adalah lokasi directorinya pada kasus ini : laravel-tutorial/app/Http/Controllers/DosenController.php
### Cara Kedua : membuat file dengan php artisan
Cara kedua, kita dapat membuat file controller baru seperti pada cara pertama dengan cara yang lebih mudah. Caranya dengan memanfaatkan php artisan yang terdapat pada laravel. Dengan fitur ini kita dapat membuat serta mengontrol project kita. php artisan adalah fitur unggulan yang ada pada laravel, yang dibuat untuk memudahkan kita dalam pengembangan menggunakan laravel. php artisan untuk membuat file controller baru dapat dibuat dengan syntax berikut yang diketik melalui terminal atau command prompt (CMD)
``` bash php
php artisan make:controller MahasiswaController
```
Perintah make:controller di atas adalah perintah dari php artisan untuk membuat controller baru sesuai nama yang diinginkan. Pada kasus ini file controller tersebut bernama MahasiswaController. Maka file controller MahasiswaController.php akan dibuat secara otomatis. Selain itu, dengan memanfaatkan php artisan make:controller ini kita dapat langsung menulis kode sesuai template Resource Controller pada dalam controller dengan menambahkan --resource setelah nama file controller :
``` bash
php artisan make:controller MahasiswaController --resource
```

Berikut adalah DosenController jika dibuat dengan resource :
``` bash
<?php

namespace App\Http\Controllers;

use Illuminate\Http\Request;

class MahasiswaController extends Controller
{
    /**
     * Display a listing of the resource.
     *
     * @return \Illuminate\Http\Response
     */
    public function index()
    {
        //
    }

    /**
     * Show the form for creating a new resource.
     *
     * @return \Illuminate\Http\Response
     */
    public function create()
    {
        //
    }

    /**
     * Store a newly created resource in storage.
     *
     * @param  \Illuminate\Http\Request  $request
     * @return \Illuminate\Http\Response
     */
    public function store(Request $request)
    {
        //
    }

    /**
     * Display the specified resource.
     *
     * @param  int  $id
     * @return \Illuminate\Http\Response
     */
    public function show($id)
    {
        //
    }

    /**
     * Show the form for editing the specified resource.
     *
     * @param  int  $id
     * @return \Illuminate\Http\Response
     */
    public function edit($id)
    {
        //
    }

    /**
     * Update the specified resource in storage.
     *
     * @param  \Illuminate\Http\Request  $request
     * @param  int  $id
     * @return \Illuminate\Http\Response
     */
    public function update(Request $request, $id)
    {
        //
    }

    /**
     * Remove the specified resource from storage.
     *
     * @param  int  $id
     * @return \Illuminate\Http\Response
     */
    public function destroy($id)
    {
        //
    }
}

```
