#### Instalasi repository ini
1. Pertama ```git clone git@github.com:Revitalismo/Belajar-SCSS.git```.

#### Cara menjalankan
1. Buka folder Belajar Belajar SCSS.
2. Ketikan ```npm run dev```.
3. buka buka alamat localhost di browser.

#### Preprocessing
CSS adalah hal yang menyenangkan(untuk sebagian orang), tapi yang namanya stylesheet lama kelamaan semakin besar, menjadi lebih kompleks, dan sulit di maintenance.
Disinilah dimana sebuah preprocessor bisa membantu kita. Yaitu SASS/SCSS, SASS mempunyai fitur yang CSS tidak miliki, seperti nesting, mixins inheritance, dan fitur keren lainnya yang membantu kita menulis CSS yang kuat(CSS specificity), dan mudah di maintenance.

Tapi SASS tidak bisa langsung digunakan, maka dari itu SASS harus di diproses terlebih dahulu dan kemudian menjadi file CSS murni yang dapat kita gunakan pada website kita.

Kita bisa mengcompile File SASS kita ke CSS menggunakan perintah ```sass```. Dan kita  harus memberi tahu ke compiler file mana yang ingin kita compile, dan dimana kita ingin menamai filenya dan menaruh file hasil compile. Sebagai contoh ```sass style.scss style.css``` ini akan mengcompile file ```style.scss``` dan hasil compilenya ```style.css```

Kita bisa menggunakan keyword ```--watch```. agar kita tak perlu compile secara manual jika kita mengubah lagi isi file ```style.scss``` kita.
```sass --watch style.scss style.css```

#### Fun fact :
SASS mempunyai dua sintaks (.scss) ini yang paling umum dan kita akan menggunakan ini. Ini adalah superset dari CSS, yang mana artinya adalah semua CSS yang valid juga adalah SCSS yang valid. sintaks yang menggunakan indentasi (.sass) dan tidak begitu umum, kalau kita menggunakan .sass maka kita menggunakan indentasi daripada curly braces dan menggunakan baris baru daripada ```;```(titik koma).

#### Instalasi compiler SASS
Kita bisa menginstall compiler SASS dengan bantuan NPM, dengan syarat kita harus mendownload ```NodeJs``` terlebih dahulu.

##### Menginstall compiler SASS :
```npm install sass```

Docs install dengan berbagai macam package manager :
https://sass-lang.com/install

Resource : 
https://sass-lang.com/guide