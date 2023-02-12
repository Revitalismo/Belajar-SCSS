##### Inheritance/extends
Menggunakan ```@extend``` memungkinkan kita untuk berbagi sekumpulan property-property CSS from satu selector ke yang lainnya. Pada penjelasan kali ini card sederhana.

```
// _base.scss

%card {
    padding: 20px;
    margin: 3rem auto;
    max-width: 300px;
    
    display: flex;
    flex-direction: column;
    row-gap: 12px;
}

%profile-picture {
    height: base.$profile-picture;
    width: base.$profile-picture;
    border-radius: 100%;
    object-fit: base.$object-cover;
}
```

```
// inheritance.scss

.card-primary {
    @extend %card;

    font-family: base.$font-base;
    @include base.theme;
    
    .title {
        font-size: 1.125rem;
        font-weight: 500;
    }

    img {
        height: base.$profile-picture;
        width: base.$profile-picture;
        border-radius: 100%;
        object-fit: base.$object-cover;
    }
}
```

Pada kode program di atas ```.card-primary``` berperilaku(property nya) seperti %card, yang mana artinya ```.card-primary``` mewarisi properti ```%card```. 
Ke ajaiban terjadi di CSS yang di generated, setiap class akan mendapat property CSS yang sama seperti %card. Ini membantu kita untuk menghindari menulis banyak class pada HTML.

```
// generated css
.card-primary, .card-secondary {
  padding: 20px;
  margin: 3rem auto;
  max-width: 300px;
  display: flex;
  flex-direction: column;
  row-gap: 12px;
}
```
Catatan: Properties CSS di ```%profile-picture``` tidak di generated, karena ```%profile-picture``` tidak pernah di extend.