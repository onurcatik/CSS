## CSS Links

Aşağıda CSS bağlantılarıyla ilgili tartışılan kavramların nasıl uygulanacağını gösteren kapsamlı bir örnek bulacaksınız. Örnek iki bölüme ayrılmıştır: ayrı dosyalara yerleştirilen HTML ve CSS.

### HTML (index.html)

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Links Example</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <h1>CSS Bağlantı Örnekleri</h1>

    <h2>Bağlantı Durumları</h2>
    <p><a href="#" class="example-link">Normal, ziyaret edilmemiş bağlantı (a:link)</a></p>
    <p><a href="#" class="example-link visited">Ziyaret edilmiş bağlantı (a:visited)</a></p>
    <p><a href="#" class="example-link hover">Fareyle üzerine gelinmiş bağlantı (a:hover)</a></p>
    <p><a href="#" class="example-link active">Tıklanmış bağlantı (a:active)</a></p>

    <h2>Metin Dekorasyonu</h2>
    <p><a href="#" class="no-decoration">Alt çizgisiz bağlantı (text-decoration: none)</a></p>
    <p><a href="#" class="underline">Alt çizgili bağlantı (text-decoration: underline)</a></p>

    <h2>Arka Plan Rengi</h2>
    <p><a href="#" class="background-color">Arka plan renkli bağlantı (background-color)</a></p>

    <h2>Bağlantı Düğmeleri</h2>
    <p><a href="#" class="button">Bağlantı Düğmesi</a></p>
</body>

</html>
```

### CSS (styles.css)

```css
/* Genel Bağlantı Stilleri */
a.example-link {
    color: blue;
    /* Normal, ziyaret edilmemiş bağlantı */
    text-decoration: none;
}

a.example-link.visited {
    color: purple;
    /* Ziyaret edilmiş bağlantı */
}

a.example-link:hover {
    color: red;
    /* Fareyle üzerine gelinmiş bağlantı */
}

a.example-link:active {
    color: yellow;
    /* Tıklanmış bağlantı */
}

/* Metin Dekorasyonu */
a.no-decoration {
    text-decoration: none;
    color: green;
}

a.underline {
    text-decoration: underline;
    color: green;
}

/* Arka Plan Rengi */
a.background-color {
    background-color: yellow;
    color: black;
    padding: 5px;
    text-decoration: none;
}

/* Bağlantı Düğmeleri */
a.button {
    display: inline-block;
    padding: 10px 20px;
    font-size: 16px;
    background-color: blue;
    color: white;
    text-decoration: none;
    border-radius: 5px;
    transition: background-color 0.3s ease;
}

a.button:hover {
    background-color: darkblue;
}
```

### Açıklama

#### HTML

* `index.html` dosyasında bağlantı durumlarını, metin dekorasyonunu, arka plan rengini ve bağlantı düğmelerini temsil eden farklı `<a>` etiketleri bulunmaktadır.
* Her bağlantı, ilgili CSS sınıfına sahiptir (`example-link`,  `no-decoration`,  `underline`,  `background-color`,  `button`).

#### CSS

* `styles.css` dosyasında her bağlantı türü için stil tanımlamaları yapılmıştır.
* `a.example-link` sınıfı, normal, ziyaret edilmemiş bağlantı için temel stil ayarlarını içerir.
* `a.example-link.visited`,  `a.example-link:hover`, ve `a.example-link:active` sınıfları, ziyaret edilmiş, fareyle üzerine gelinmiş ve tıklanmış bağlantılar için stilleri tanımlar.
* `a.no-decoration` ve `a.underline` sınıfları, metin dekorasyonu özelliklerini gösterir.
* `a.background-color` sınıfı, bağlantılara arka plan rengi ekler.
* `a.button` sınıfı, bağlantıları düğme gibi görüntüler ve fareyle üzerine gelindiğinde arka plan rengini değiştiren bir geçiş efekti ekler.

Bu örnek, CSS kullanarak bağlantıları nasıl özelleştireceğinizi detaylı bir şekilde gösterir. Her HTML etiketi, ilgili CSS sınıflarıyla stil verilmiş ve görsel olarak farklı bağlantı durumlarını, metin dekorasyonlarını ve arka plan renklerini sergiler. Bu, web sayfalarınızda bağlantıların görünümünü ve etkileşimini kontrol etmek için güçlü bir yöntem sağlar.
