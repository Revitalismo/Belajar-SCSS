##### Variables
Variable adalah cara untuk menyimpan informasi yang kita ingin gunakan diseluruh stylesheet kita. Kita bisa menyimpan hal-hal seperti colors, font-stacks, atau nilai CSS lainnya yang ingin kita gunakan kembali. SASS menggunakan simbol ```$``` dolar untuk membuat suatu variable. Disini contohnya :
```
$font-base: 'Roboto', sans-serif;
$dark-primary: rgb(26, 26, 26);
$dark-secondary: rgb(44, 44, 44);

.header {
    font-family: $font-base;
}

.title {
    color: $dark-primary;
}

.description {
    color: $dark-secondary;
}
```