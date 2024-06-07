###  CSS Filter Property

#### HTML Kodu

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Filter Property Example</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <section class="filter-examples">
        <h1>CSS Filter Property Örnekleri</h1>
        <div class="example">
            <h2>Bulanıklık (Blur)</h2>
            <img src="example.jpg" alt="Example Image" class="blur-example">
        </div>
        <div class="example">
            <h2>Doygunluk (Saturate)</h2>
            <img src="example.jpg" alt="Example Image" class="saturate-example">
        </div>
        <div class="example">
            <h2>Siyah-Beyaz (Grayscale)</h2>
            <img src="example.jpg" alt="Example Image" class="grayscale-example">
        </div>
        <div class="example">
            <h2>Sepya (Sepia)</h2>
            <img src="example.jpg" alt="Example Image" class="sepia-example">
        </div>
        <div class="example">
            <h2>Parlaklık (Brightness)</h2>
            <img src="example.jpg" alt="Example Image" class="brightness-example">
        </div>
        <div class="example">
            <h2>Kontrast (Contrast)</h2>
            <img src="example.jpg" alt="Example Image" class="contrast-example">
        </div>
        <div class="example">
            <h2>Tersine Çevirme (Invert)</h2>
            <img src="example.jpg" alt="Example Image" class="invert-example">
        </div>
    </section>
</body>
</html>
```

#### CSS Kodu

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
    color: #333;
}

.filter-examples {
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
    background-color: #fff;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
}

.filter-examples h1 {
    text-align: center;
    margin-bottom: 40px;
}

.example {
    margin-bottom: 20px;
    text-align: center;
}

.example h2 {
    margin-bottom: 10px;
}

.example img {
    max-width: 100%;
    height: auto;
}

/* Filter Effects */
.blur-example {
    filter: blur(5px);
}

.saturate-example {
    filter: saturate(150%);
}

.grayscale-example {
    filter: grayscale(100%);
}

.sepia-example {
    filter: sepia(100%);
}

.brightness-example {
    filter: brightness(50%);
}

.contrast-example {
    filter: contrast(200%);
}

.invert-example {
    filter: invert(100%);
}
```

#### Açıklamalar

1. **HTML Yapısı**:
    - HTML dosyasında `section` etiketi içinde çeşitli örnekler sunulmaktadır.
    - Her örnek `div` etiketi içinde başlık (`h2`) ve bir resim (`img`) içermektedir.
    - `link` etiketi ile harici bir CSS dosyası (`styles.css`) bağlanmıştır.

2. **CSS Stilleri**:
    - `body` etiketi için genel stiller tanımlanmıştır (font, arka plan rengi, kenar boşlukları vb.).
    - `filter-examples` sınıfı, örneklerin içinde bulunduğu bölümün stilini belirler.
    - Her örnek `example` sınıfı ile stilize edilmiştir.
    - `img` etiketlerine uygulanan filtre efektleri, ilgili sınıflar (`blur-example`, `saturate-example` vb.) ile tanımlanmıştır.

3. **Filter Efektleri**:
    - **Bulanıklık (Blur)**: `blur(5px)` kullanılarak 5 piksel bulanıklık uygulanmıştır.
    - **Doygunluk (Saturate)**: `saturate(150%)` kullanılarak renk doygunluğu %150 artırılmıştır.
    - **Siyah-Beyaz (Grayscale)**: `grayscale(100%)` kullanılarak resim tamamen siyah-beyaz yapılmıştır.
    - **Sepya (Sepia)**: `sepia(100%)` kullanılarak resme sepya tonu eklenmiştir.
    - **Parlaklık (Brightness)**: `brightness(50%)` kullanılarak resmin parlaklığı %50 azaltılmıştır.
    - **Kontrast (Contrast)**: `contrast(200%)` kullanılarak resmin kontrastı %200 artırılmıştır.
    - **Tersine Çevirme (Invert)**: `invert(100%)` kullanılarak resmin renkleri tersine çevrilmiştir.

Bu örnekler, CSS `filter` özelliğinin nasıl kullanılacağını ve her bir fonksiyonun etkisini anlamak için pratik bir yol sunmaktadır. Bu şekilde, web geliştirme projelerinde görsel efektler eklemek için gerekli bilgiyi sağlamış olursunuz.