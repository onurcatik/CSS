## Örnek Proje: CSS Geçişleri

Bu örnek proje, HTML ve CSS kullanarak geçiş efektlerini nasıl uygulayacağınızı göstermektedir. Projede bir başlık, iki bölüm ve bir alt bilgi (footer) yer almaktadır. Her bölümde geçiş efektleri kullanılarak kullanıcı etkileşimi sağlanacaktır.

### HTML Dosyası (index.html)

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Geçişleri Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>CSS Geçişleri Örneği</h1>
    </header>
    <section id="section1">
        <h2>Geçiş Özellikleri</h2>
        <p>Bu bölümde geçiş özelliklerinin nasıl çalıştığını göreceğiz.</p>
        <div class="box1">Hover Me!</div>
    </section>
    <section id="section2">
        <h2>Geçiş Süresi ve Gecikme</h2>
        <p>Bu bölümde geçiş süresi ve gecikme özelliklerini inceleyeceğiz.</p>
        <div class="box2">Hover Me!</div>
    </section>
    <section id="section3">
        <h2>Geçiş Hız Eğrisi</h2>
        <p>Bu bölümde geçiş hız eğrisi özelliklerini inceleyeceğiz.</p>
        <div class="box3">Hover Me!</div>
    </section>
    <footer>
        <p>&copy; 2024 CSS Geçişleri Örneği. Tüm hakları saklıdır.</p>
    </footer>
</body>
</html>
```

### CSS Dosyası (styles.css)

```css
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 0;
}

header {
    background: #333;
    color: white;
    padding: 10px 0;
    text-align: center;
}

section {
    padding: 20px;
}

#section1 {
    background: #f4f4f4;
}

#section2 {
    background: #e2e2e2;
}

#section3 {
    background: #d3d3d3;
}

.box1, .box2, .box3 {
    width: 200px;
    height: 200px;
    background: #3498db;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 20px 0;
    transition: all 1s ease;
}

.box1:hover {
    background-color: #2ecc71;
}

.box2 {
    transition-property: width;
    transition-duration: 2s;
    transition-delay: 0.5s;
}

.box2:hover {
    width: 300px;
}

.box3 {
    transition-property: transform;
    transition-duration: 1s;
    transition-timing-function: ease-in-out;
}

.box3:hover {
    transform: rotate(45deg);
}

footer {
    background: #333;
    color: white;
    text-align: center;
    padding: 10px 0;
}
```

### Açıklama

#### HTML Yapısı

- **Header**: Projenin başlık kısmını içerir.
- **Section**: Üç bölüm içerir, her biri geçiş efektleriyle donatılmıştır.
- **Footer**: Sayfanın alt bilgisini içerir.

#### CSS Tarafı

- **Genel Stiller**: Temel stil ayarları yapılmıştır (font, margin, padding).
- **Header**: Başlık kısmı için arka plan rengi ve metin rengi ayarlanmıştır.
- **Section**: Bölümler için dolgu (padding) ayarları yapılmıştır.
- **Box**: Her bölümde yer alan kutular için stil ayarları ve geçiş özellikleri tanımlanmıştır.

#### Geçiş Özellikleri

1. **transition-property**: Geçiş efektinin hangi CSS özelliği için geçerli olduğunu belirtir.
   - `box2` örneğinde, geçiş efekti sadece `width` özelliği için geçerlidir.

    ```css
    .box2 {
        transition-property: width;
    }
    ```

2. **transition-duration**: Geçiş efektinin tamamlanmasının ne kadar süreceğini belirtir.
   - `box2` örneğinde, geçiş efekti 2 saniye sürecektir.

    ```css
    .box2 {
        transition-duration: 2s;
    }
    ```

3. **transition-delay**: Geçiş efektinin ne zaman başlayacağını belirtir.
   - `box2` örneğinde, geçiş efekti 0.5 saniye gecikmeyle başlayacaktır.

    ```css
    .box2 {
        transition-delay: 0.5s;
    }
    ```

4. **transition-timing-function**: Geçiş efektinin hız eğrisini belirtir.
   - `box3` örneğinde, geçiş efekti yavaş başlayacak, hızlanacak ve sonra tekrar yavaşlayacaktır (`ease-in-out`).

    ```css
    .box3 {
        transition-timing-function: ease-in-out;
    }
    ```

5. **transition**: Birden fazla geçiş özelliğini tek bir satırda tanımlamak için kullanılır.
   - `box1` örneğinde, `background-color` özelliği için geçiş efekti 1 saniye sürecek ve `ease` hız eğrisi kullanılacaktır.

    ```css
    .box1 {
        transition: all 1s ease;
    }
    ```

### Sonuç

Bu örnek proje, CSS geçişlerinin nasıl uygulanabileceğini ve kullanıcı etkileşimini nasıl artırabileceğini göstermektedir. Her bölümde farklı geçiş efektleri kullanarak, CSS geçişlerinin gücünü ve esnekliğini keşfetmiş olduk. Bu tür geçişler, web sayfalarınızı daha dinamik ve kullanıcı dostu hale getirmek için güçlü araçlardır.