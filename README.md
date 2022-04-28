# CrashCourse

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 13.3.3.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.

## Pengenalan Angular
Basis dari Angular yaitu component driven, dimana komponen adalah potongan UI yang termasuk template html, logic, dan styling. Sifatnya dapat digunakan kembali (reusable) dan bisa diembed ke template html lainnya dengan tag XML.
Contoh dasarnya seperti ini,
![image](https://user-images.githubusercontent.com/45738683/165676945-12e3f099-b734-487a-ba4c-4768c197c60b.png)
![image](https://user-images.githubusercontent.com/45738683/165676962-f4723c68-dc8a-4007-b3b6-d3386c43f3e7.png)
![image](https://user-images.githubusercontent.com/45738683/165676969-5a4c8365-cb59-475c-98e6-97e09671c301.png)

Bisa menggunakan tag yang diinject maupun javascript expression ke dalam html template.
![image](https://user-images.githubusercontent.com/45738683/165676994-92ff1e80-cdf3-4a8c-ad82-5631eab1939c.png)

[] untuk melakukan directive property (mirip seperti di react), () untuk melakukan event handling.
![image](https://user-images.githubusercontent.com/45738683/165677021-6622bb4d-7a84-4b74-8945-1307b6fd3d90.png)

Pakai Input untuk menerima data props dan meneruskan ke class, Output berfungsi sebagai output emitter.
![image](https://user-images.githubusercontent.com/45738683/165677044-ec6a5c0c-4f88-4531-8064-ed12b9d3bd8d.png)
![image](https://user-images.githubusercontent.com/45738683/165677053-289dc640-c310-4620-95a7-c180f398aee6.png)

Output Emitter memungkinkan untuk memanggil method dari kelas parent yang mengembed component tersebut.
![image](https://user-images.githubusercontent.com/45738683/165677082-04770ff9-e99d-4e0d-9aea-6bc587b309bc.png)
![image](https://user-images.githubusercontent.com/45738683/165677088-746e1293-0124-4940-903b-7ff6e325aea2.png)
![image](https://user-images.githubusercontent.com/45738683/165677097-73c157ab-d358-4900-af03-aad693542561.png)

Two-ways data binding, dimana [] untuk menerima input data, dan () untuk output atau menjalankan suatu function. Karena sifat binding tersebut, sehingga secara realtime data yang ditampilkan akan sesuai dengan apa yang di-inputkan.
![image](https://user-images.githubusercontent.com/45738683/165677128-1d86a9f8-3dda-40b2-b370-3c7c774838b9.png)
![image](https://user-images.githubusercontent.com/45738683/165677120-4265ffef-ea31-4fc9-a8df-0aa9f354eb9a.png)

Sebenarnya, kita bisa melakukan output emitter ke parent apabila event yang diperlukan hanya untuk satu handler. Apabila ingin beberapa komponen untuk bereaksi pada suatu perubahan event, diperlukan Subject, Subscription, dan Observable. Nantinya akan dibuat suatu layer service baru dengan nama UIService yang bertanggung jawab atas presentasi yang ada.
![image](https://user-images.githubusercontent.com/45738683/165677150-bff412b1-5184-4870-a02b-c167f69ef174.png)
![image](https://user-images.githubusercontent.com/45738683/165677158-9965ca98-6113-4e40-b2ed-d842738f3f49.png)
![image](https://user-images.githubusercontent.com/45738683/165677168-05f2ad8f-c5c8-4291-8b94-10b167d02de4.png)

Sedangkan untuk routing, silahkan melakukan penambahan routing pada app.module.ts, bisa dilakukan konfigurasi seperti kebutuhan debug / enableTracing. Lalu ganti tag pada template,
![image](https://user-images.githubusercontent.com/45738683/165677194-acbccc20-9cb9-451c-adda-f09396d4f696.png)
![image](https://user-images.githubusercontent.com/45738683/165677215-b552bb41-a848-4a52-98a8-16b7ffc5c62d.png)

Selanjutnya yaitu buat komponen baru seperti About, dan buat navigasi sederhana dengan RouterLink. Kenapa tidak menggunakan href, karena itu akan refresh page secara seutuhnya, RouterLink bisa membantu agar input data tetap tersedia dan tidak hilang.
![image](https://user-images.githubusercontent.com/45738683/165677236-0bdbf0d5-9a81-4eec-8e20-db9bdd7b0805.png)
![image](https://user-images.githubusercontent.com/45738683/165677244-c8a1af69-68e3-4445-b112-aca41f2a650b.png)

Angular memiliki struktur sebagai berikut:
-	Component
-	Module
Di dalam component, terdapat beberapa parameter yaitu selector, templateUrl, dan styleUrls.
![image](https://user-images.githubusercontent.com/45738683/165677278-efe33440-a242-42cf-bba5-dcc17513e03b.png)

Component yang telah dideklarasikan akan diinject ke dalam templateUrl bersamaan dengan styleUrls yang ada.
![image](https://user-images.githubusercontent.com/45738683/165677299-6267083d-641c-4f64-a5b1-4911aeb5db80.png)

Module adalah file yang utama dalam angular, dimana semuanya diatur dan dideklarasikan apabila ingin ditambahkan suatu halaman baru ke dalam aplikasi.
![image](https://user-images.githubusercontent.com/45738683/165677344-2c5f6772-6b10-4a49-822d-eedce7b89c4a.png)

Sekian dari materi summary pembelajaran Angular.
