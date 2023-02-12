##### Mixins
Sesuatu di CSS terkadang membosankan untuk ditulis, khususnya dengan CSS3 dan banyak vendor prefixes yang ada. Sebuah mixins memungkinkan kita untuk membuat sekumpulan deklarasi dari CSS yang kita ingin gunakan untuk digunakan kembali diseluruh website kita. Ini membantu SASS kita tetap DRY(don't repeat yourself). Bahkan kita bisa memasukan nilai-nilai untuk membuat mixin lebih flexible. Ini adalah contoh dari mixin ```theme```.

```
// _base.scss

@mixin theme($bg: $bg-blue, $color: $color-light) {
    background-color: $bg;
    color: $color;
    border-radius: 10px;
    
    -webkit-box-shadow: 0px 10px 25px 0px rgba(115,115,115,0.34);
    -moz-box-shadow: 0px 10px 25px 0px rgba(115,115,115,0.34);
    box-shadow: 0px 10px 25px 0px rgba(115,115,115,0.34);
}
```

##### Membuat mixin
Untuk membuat sebuah Mixin kita bisa menggunakan directive ```@mixin``` dan memberinya nama. Kita menamai mixin kita ```theme```. Kita juga bisa menggunakan variable ```$bg-blue``` dan ```$color-light``` di dalam kurung nya, jadi dengan ini kita bisa memasukan sebuah ```theme``` apapun yang kita mau. 

Setelah kita membuat mixin, dan kemudian kita bisa menggunakannya sebagai sebuah deklarasi CSS di mulai dengan ```@include``` diikuti dengan nama mixin nya.
