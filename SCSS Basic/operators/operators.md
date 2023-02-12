##### Operators
Melakukan math di CSS kita sangatlah membantu. SASS memiliki standard math operators untuk melakukan operasi seperti pengurangan, pertambahan, perkalian, pembagian, ```(-, +, *, math.div(), %)```. Dalam contoh ini kita akan melakukan operasi matematikan sederhana untuk kalkulasi ```font-size``` dan ```font-weight``` untuk ```.title```.

```
// operators.scss
@use "base";
@use "sass:math";

.card-default {
    @extend %card;

    font-family: base.$font-base;
    @include base.theme(base.$bg-light, base.$color-dark);

    .title {
        font-size: math.div(18rem,16rem) + 0rem;
        font-weight: 100 + 400;
    }

    img {
        @extend %profile-picture;
    }
}

```
Catatan: Sebelum kita menggunakan standard operator di SCSS kita harus terlebih dahulu mengimpor module math, caranya ```@use "sass:math";```.