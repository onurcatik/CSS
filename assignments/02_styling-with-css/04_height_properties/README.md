### CSS Height and Properties

Aşağıda, CSS yükseklik ve genişlik özelliklerini kullanarak nasıl çalışabileceğinizi gösteren ayrıntılı bir örnek bulunmaktadır. Bu örnek, HTML ve CSS dosyalarının ayrı ayrı nasıl yapılandırılacağını ve bu özelliklerin nasıl uygulanacağını göstermektedir.

#### HTML Dosyası (index.html)

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Yükseklik ve Genişlik Örnek</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>CSS Yükseklik ve Genişlik Örnek</h1>
    </header>
    <main>
        <section class="container">
            <div class="box fixed-size">Sabit Boyutlu Kutu</div>
            <div class="box percentage-size">Yüzde Boyutlu Kutu</div>
            <div class="box max-width-size">Maksimum Genişlik Kutusu</div>
            <div class="box min-height-size">Minimum Yükseklik Kutusu</div>
            <div class="box responsive-size">Responsive Kutu</div>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 CSS Örnek</p>
    </footer>
</body>

</html>
```

#### CSS Dosyası (styles.css)

```css
/* Genel Stil */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

header {
    background-color: #4CAF50;
    color: white;
    padding: 1em;
    text-align: center;
}

main {
    padding: 1em;
}

footer {
    background-color: #4CAF50;
    color: white;
    text-align: center;
    padding: 0.5em;
    position: fixed;
    width: 100%;
    bottom: 0;
}

/* Kutu Stilleri */
.container {
    display: flex;
    flex-wrap: wrap;
    gap: 1em;
}

.box {
    background-color: #f4f4f4;
    border: 1px solid #ccc;
    padding: 1em;
    text-align: center;
    flex: 1;
}

/* Sabit Boyutlu Kutu */
.fixed-size {
    height: 100px;
    width: 200px;
}

/* Yüzde Boyutlu Kutu */
.percentage-size {
    height: 50px;
    width: 50%;
}

/* Maksimum Genişlik Kutusu */
.max-width-size {
    width: 100%;
    max-width: 300px;
}

/* Minimum Yükseklik Kutusu */
.min-height-size {
    min-height: 150px;
    height: auto;
}

/* Responsive Kutu */
.responsive-size {
    width: 100%;
    height: auto;
}

@media (max-width: 600px) {
    .responsive-size {
        height: 200px;
    }
}
```

### Açıklamalar

1. **HTML Yapısı** :
   - **Header** : Sayfanın başlık kısmını içerir.
   - **Main** : İçeriğin bulunduğu ana bölümü içerir.
   - **Footer** : Sayfanın alt kısmında yer alır ve sabitlenmiştir.
   - **Container** : Flexbox kullanarak kutuların düzenlenmesini sağlar.
   - **Box** : Farklı yükseklik ve genişlik özellikleri ile stilize edilmiş kutuları içerir.

2. **CSS Stilleri** :
   - **Genel Stil** : Tüm sayfa için genel stil ayarları (font, margin, padding vb.) belirlenir.
   - **Header ve Footer** : Başlık ve alt bilgi bölümlerinin arka plan renkleri ve metin hizalamaları ayarlanır.
   - **Container** : Flexbox düzeni kullanılarak kutuların esnek ve duyarlı olması sağlanır.
   - **Box Stilleri** : Her bir kutunun belirli bir yüksekliği ve genişliği nasıl kullanacağını gösteren stiller.

Bu örnek, CSS yükseklik ve genişlik özelliklerinin nasıl kullanılacağını ve farklı birimlerin (piksel, yüzde) ve özelliklerin (max-width, min-height) nasıl uygulanacağını göstermektedir. Responsive tasarım için `@media` sorguları kullanılarak farklı ekran boyutlarına uyum sağlanmıştır.
