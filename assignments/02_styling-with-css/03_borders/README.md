# CSS Borders 

Bu bölümde, yukarıda açıklanan CSS sınır özelliklerini kullanarak kapsamlı bir örnek oluşturacağız. Örneğimizde HTML ve CSS kodlarını ayrı dosyalar halinde sunacağız. Bu, daha iyi bir yapı ve düzen sağlayarak kodun okunabilirliğini artıracaktır.

## HTML Kodu (index.html)

Aşağıda, CSS sınır özelliklerini göstermek için basit bir HTML belgesi yer almaktadır. Bu belge, çeşitli sınır stilleri, renkleri, genişlikleri ve köşe yuvarlatma özelliklerini içeren birkaç div öğesi içerir.

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Sınır Özellikleri Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <div class="border-style-example">Sınır Stili: Solid</div>
    <div class="border-color-example">Sınır Rengi: Kırmızı</div>
    <div class="border-width-example">Sınır Genişliği: 5px</div>
    <div class="border-radius-example">Köşe Yuvarlatma: 10px</div>
    <div class="complex-border-example">Karmaşık Sınır Örneği</div>
</body>

</html>
```

## CSS Kodu (styles.css)

Aşağıda, yukarıdaki HTML belgesindeki her bir div öğesi için CSS sınır özelliklerini tanımlayan CSS kodu yer almaktadır.

```css
/* Genel stil ayarları */
body {
    font-family: Arial, sans-serif;
    padding: 20px;
}

/* Sınır stili örneği */
.border-style-example {
    border-style: solid;
    border-width: 2px;
    border-color: black;
    padding: 10px;
    margin-bottom: 20px;
}

/* Sınır rengi örneği */
.border-color-example {
    border-style: solid;
    border-width: 2px;
    border-color: red;
    padding: 10px;
    margin-bottom: 20px;
}

/* Sınır genişliği örneği */
.border-width-example {
    border-style: solid;
    border-width: 5px;
    border-color: black;
    padding: 10px;
    margin-bottom: 20px;
}

/* Köşe yuvarlatma örneği */
.border-radius-example {
    border-style: solid;
    border-width: 2px;
    border-color: black;
    border-radius: 10px;
    padding: 10px;
    margin-bottom: 20px;
}

/* Karmaşık sınır örneği */
.complex-border-example {
    border-top-style: solid;
    border-right-style: dashed;
    border-bottom-style: dotted;
    border-left-style: double;
    border-width: 4px;
    border-top-color: blue;
    border-right-color: green;
    border-bottom-color: red;
    border-left-color: yellow;
    border-radius: 15px 30px 45px 60px;
    padding: 10px;
    margin-bottom: 20px;
}
```

## Açıklama

1. **HTML Kodu** :
    - `index.html` dosyası, sayfa başlığı ve karakter seti gibi meta bilgileri içerir.
    - `link` etiketi, harici bir CSS dosyasını (`styles.css`) bağlar.
    - Her bir div öğesi, farklı bir CSS sınır özelliğini göstermek için belirli bir sınıfa (`class`) sahiptir.

2. **CSS Kodu** :
    - `styles.css` dosyası, her bir sınıf için stil kurallarını tanımlar.
    - `.border-style-example` sınıfı, katı bir sınır stili ile tanımlanmıştır.
    - `.border-color-example` sınıfı, kırmızı bir sınır rengi ile tanımlanmıştır.
    - `.border-width-example` sınıfı, 5 piksel genişliğinde bir sınır ile tanımlanmıştır.
    - `.border-radius-example` sınıfı, 10 piksel yarıçapında yuvarlatılmış köşeler ile tanımlanmıştır.
    - `.complex-border-example` sınıfı, farklı stiller, renkler ve genişliklerle dört tarafında farklı sınırlar ve karmaşık köşe yuvarlatma ile tanımlanmıştır.

Bu örnek, CSS sınır özelliklerini kapsamlı bir şekilde anlamanızı sağlayacaktır. Kodun hem HTML hem de CSS bölümlerini ayrı dosyalar halinde tutmak, iyi bir uygulama olup, kodun daha modüler ve yönetilebilir olmasını sağlar.
