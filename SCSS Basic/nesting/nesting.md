##### Nesting
Ketika kita menulis HTML kita mungkin tahu bahwa kita menulisnya secara bersarang dan rapih. Namun di CSS tidak bisa.

Dengan SASS memungkinkan membuat css selector bersarang dengan cara mengikuti penulisan HTML kita. Tapi berhati-hatilah dalam membuat css bersarang karena akan membuat specificity nya sangat tinggi dan sulit di maintenance dan pada umumnya ini adalah bad pratice.

Dibawah ini adalah contoh styles nested untuk header :
```
$font-base: 'Roboto', sans-serif;
$dark-primary: rgb(26, 26, 26);
$dark-secondary: rgb(44, 44, 44);

.header {
    margin: 3rem auto;
    max-width: 300px;
    font-family: $font-base;

    display: flex;
    flex-direction: column;
    row-gap: 12px;
    
    .title {
        font-size: 1.125rem;
        font-weight: 500;
        color: $dark-primary;
    }
    
    .description {
        color: $dark-secondary;
    }
}
```