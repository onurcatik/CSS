### HTML and CSS Text Transformation

Aşağıda, `text-transform` özelliğini çeşitli şekillerde kullanarak metin dönüştürme işlemlerini gösteren kapsamlı bir örnek bulunmaktadır. Bu örnek, HTML ve CSS kodlarının ayrı dosyalarda tutulmasını içermektedir.

#### HTML Dosyası (index.html)

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Metin Dönüştürme Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <h1>CSS Metin Dönüştürme Özellikleri</h1>

    <section>
        <h2>uppercase Örneği</h2>
        <p class="uppercase">Bu metin tamamen büyük harfe dönüştürülecek.</p>
    </section>

    <section>
        <h2>lowercase Örneği</h2>
        <p class="lowercase">Bu Metin Tamamen Küçük Harfe Dönüştürülecek.</p>
    </section>

    <section>
        <h2>capitalize Örneği</h2>
        <p class="capitalize">bu metin her kelimenin ilk harfi büyük olacak şekilde dönüştürülecek.</p>
    </section>

    <section>
        <h2>none Örneği</h2>
        <p class="none">Bu Metin Üzerinde Herhangi Bir Dönüştürme Uygulanmayacak.</p>
    </section>
</body>

</html>
```

#### CSS Dosyası (styles.css)

```css
/* Genel Stil Ayarları */
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 20px;
    background-color: #f4f4f4;
}

h1 {
    text-align: center;
    margin-bottom: 20px;
}

section {
    background-color: #fff;
    padding: 15px;
    margin-bottom: 20px;
    border: 1px solid #ddd;
    border-radius: 5px;
}

h2 {
    color: #333;
    margin-bottom: 10px;
}

/* Metin Dönüştürme Stilleri */
.uppercase {
    text-transform: uppercase;
}

.lowercase {
    text-transform: lowercase;
}

.capitalize {
    text-transform: capitalize;
}

.none {
    text-transform: none;
}
```

#### Örnek Açıklamaları

* **HTML Dosyası (index.html):** Bu dosya, web sayfasının yapısını ve içeriğini tanımlar. Her bir `section` etiketi içinde, farklı `text-transform` özelliklerini göstermek için örnek metinler bulunmaktadır.
* **CSS Dosyası (styles.css):** Bu dosya, HTML dosyasındaki elemanların stilini tanımlar. `text-transform` özelliğinin yanı sıra genel stil ayarları da içerir.

#### Uygulama Sonuçları

Bu örneği bir web tarayıcısında görüntülediğinizde, aşağıdaki gibi bir çıktı elde edersiniz:

1. **uppercase Örneği:** Metin tamamen büyük harfe dönüştürülür.
   - Çıktı: "BU METİN TAMAMEN BÜYÜK HARFE DÖNÜŞTÜRÜLECEK."
2. **lowercase Örneği:** Metin tamamen küçük harfe dönüştürülür.
   - Çıktı: "bu metin tamamen küçük harfe dönüştürülecek."
3. **capitalize Örneği:** Her kelimenin ilk harfi büyük olacak şekilde dönüştürülür.
   - Çıktı: "Bu Metin Her Kelimenin İlk Harfi Büyük Olacak Şekilde Dönüştürülecek."
4. **none Örneği:** Metin üzerinde herhangi bir dönüştürme uygulanmaz.
   - Çıktı: "Bu Metin Üzerinde Herhangi Bir Dönüştürme Uygulanmayacak."

Bu örnekler, `text-transform` özelliğinin kullanımını ve etkilerini açıkça göstermektedir. Metin dönüştürme özellikleri, web sayfalarının stilini ve okunabilirliğini artırmak için etkili bir şekilde kullanılabilir.
