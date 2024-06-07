### CSS Z-index Property

CSS'nin z-index özelliği, bir HTML belgesindeki elemanların yığılma sırasını belirlemeye yarar. Bu özellik, özellikle üst üste binen elemanların görsel hiyerarşisini kontrol etmek için kullanılır. Aşağıda, z-index özelliğini kapsamlı bir şekilde ele alan bir örnek yer almaktadır. Bu örnekte, HTML ve CSS dosyaları ayrı olarak düzenlenmiştir ve section ile footer elementleri eklenmiştir.

#### HTML Dosyası ( `index.html` )

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Z-index Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>Z-index Örneği</h1>
    </header>

    <section>
        <div class="container">
            <div class="box box1">Box 1</div>
            <div class="box box2">Box 2</div>
            <div class="box box3">Box 3</div>
        </div>
    </section>

    <footer>
        <p>&copy; 2024 Z-index Örneği</p>
    </footer>
</body>

</html>
```

#### CSS Dosyası ( `styles.css` )

```css
/* Genel Stiller */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

header {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1em 0;
}

section {
    padding: 2em;
    text-align: center;
}

/* Kutu Stilleri */
.container {
    position: relative;
    width: 300px;
    height: 300px;
    margin: 0 auto;
    border: 1px solid #ccc;
}

.box {
    position: absolute;
    width: 100px;
    height: 100px;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
}

.box1 {
    background-color: red;
    top: 20px;
    left: 20px;
    z-index: 2;
    /* Üstte Görünecek */
}

.box2 {
    background-color: blue;
    top: 50px;
    left: 50px;
    z-index: 1;
    /* Ortada Görünecek */
}

.box3 {
    background-color: green;
    top: 80px;
    left: 80px;
    z-index: 0;
    /* Altta Görünecek */
}
```

#### Açıklama

Bu örnekte, HTML ve CSS dosyaları ayrılmıştır. HTML dosyası, sayfanın yapısını ve içeriğini tanımlar; CSS dosyası ise görsel stil ve düzeni belirler.

* **HTML Yapısı:** 
  + `<header>`: Sayfanın başlığı.
  + `<section>`: İçeriği barındıran bölüm. Üç adet kutu (`.box`) içerir.

* **CSS Stilleri:** 
  + **Genel Stiller:** Sayfanın genel görünümünü düzenler, kenar boşluklarını sıfırlar ve kutu modelini uygular.
  + **Header ve Footer:** Arka plan rengini, yazı rengini ve hizalamayı ayarlar.
  + **Section:** Bölümün içeriğini ortalar ve padding ekler.
  + **Container:** Kutuları içeren kapsayıcı. Relative pozisyonlanır ve belirli bir genişlik ve yükseklik verilir.
  + **Box Stilleri:** Kutuların mutlak pozisyonlarını, renklerini ve içlerindeki yazıyı merkezler. Her bir kutu için farklı z-index değerleri atanmıştır:
    - `.box1`: z-index 2 ile en üstte yer alır.
    - `.box2`: z-index 1 ile ortada yer alır.
    - `.box3`: z-index 0 ile en altta yer alır.

Bu düzenleme, z-index değerlerinin kutuların yığılma sırasını nasıl etkilediğini açıkça gösterir. Kırmızı kutu (Box 1) en üstte, mavi kutu (Box 2) ortada ve yeşil kutu (Box 3) en altta yer almaktadır. Bu şekilde, z-index özelliğinin nasıl kullanıldığını ve elemanların yığılma sırasını nasıl etkilediğini anlamış olduk.
