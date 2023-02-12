##### Partials
Kita bisa membuat sebagian file SASS(module) yang mengandung beberapa CSS yang mana file tersebut bisa kita pakai di file SASS kita yang lain. Ini adalah cara yang bagus untuk memodulasi CSS kita dan membuat hal-hal lebih mudah di maintain. Sebuah partial SASS file dinamai underscore (_) diawal namanya. Contoh ```_partial.scss```. 

##### Modules
Kita tidak harus menulis semuanya ke dalam satu file SASS. Kita bisa memisahnya dan jika kita ingin menggunakan nya bisa dengan ```rule @use```. Ini akan memuat file SASS lain sebagai sebuah module, yang mana kita bisa menggunakan variabel, mixins, dan function yang ada di dalamnya berdasarkan nama filenya.

```
@use "_base";

.header {
    padding: 20px;
    margin: 3rem auto;
    max-width: 300px;
    font-family: base.$font-base;
    background-color: base.$bg-light;

    display: flex;
    flex-direction: column;
    row-gap: 12px;
    
    .title {
        font-size: 1.125rem;
        font-weight: 500;
        color: base.$dark-primary;
    }
    
    .description {
        color: base.$dark-secondary;
    }

    img {
        height: base.$profile-picture;
        width: base.$profile-picture;
        border-radius: 100%;
        object-fit: base.$object-cover;
    }
}
```