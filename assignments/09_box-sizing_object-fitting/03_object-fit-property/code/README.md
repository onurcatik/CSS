### CSS Object Fit Property Example

Aşağıda, `object-fit` ve `object-position` özelliklerinin kullanıldığı kapsamlı bir örnek sunulmuştur. Örnek, HTML ve CSS dosyalarının ayrı ayrı yazılmasıyla oluşturulmuştur. Ayrıca bir `section` ve `footer` elementi eklenmiştir. 

#### HTML Dosyası (index.html)

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Object-Fit ve Object-Position Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>CSS Object-Fit ve Object-Position Örneği</h1>
    </header>

    <section>
        <h2>Object-Fit: Contain</h2>
        <div class="image-container">
            <img src="example1.jpg" class="fit-contain" alt="Example Image">
        </div>

        <h2>Object-Fit: Cover ve Object-Position: Top Right</h2>
        <div class="image-container">
            <img src="example2.jpg" class="fit-cover-top-right" alt="Example Image">
        </div>
    </section>

</body>

</html>
```

#### CSS Dosyası (styles.css)

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: white;
    padding: 1rem;
    text-align: center;
}

section {
    padding: 2rem;
}

.image-container {
    margin: 1rem 0;
    border: 1px solid #ddd;
    padding: 1rem;
    background-color: white;
}

img {
    width: 100%;
    height: 300px;
    display: block;
    margin: 0 auto;
}

.fit-contain {
    object-fit: contain;
}

.fit-cover-top-right {
    object-fit: cover;
    object-position: top right;
}
```

#### Açıklamalar

##### HTML Yapısı

1. **Başlık (Header)** 
    - `header` etiketi, sayfanın başlığını içerir ve genellikle ana başlık veya logo gibi önemli bilgileri barındırır.

2. **Bölüm (Section)** 
    - `section` etiketi, sayfanın ana içeriğini içerir. Burada iki farklı `object-fit` değeri (`contain` ve `cover`) ve `object-position` değeri (`top right`) ile ilgili örnekler bulunmaktadır.
    - Her bir örnek, `div` etiketi içinde yer almakta ve uygun CSS sınıflarıyla stilize edilmektedir.

##### CSS Yapısı

1. **Genel Stil** 
    - `body` etiketi için temel stil ayarları yapılmıştır. Yazı tipi, kenar boşlukları ve arka plan rengi belirlenmiştir.
    - `header`  için arka plan renkleri, metin renkleri ve hizalama ayarları yapılmıştır.
    - `section` etiketi için iç kenar boşlukları belirlenmiştir.

2. **Görsel Konteyner** 
    - `image-container` sınıfı, her bir görselin etrafında bir çerçeve oluşturmak için kullanılmıştır. Kenar boşlukları, dolgu ve arka plan rengi ayarları yapılmıştır.

3. **Görsellerin Stili** 
    - `img` etiketi için genişlik, yükseklik ve hizalama ayarları yapılmıştır.
    - `fit-contain` sınıfı, `object-fit: contain` değeriyle görselin konteynere en boy oranını koruyarak sığmasını sağlar.
    - `fit-cover-top-right` sınıfı, `object-fit: cover` ve `object-position: top right` değerleriyle görselin konteyneri tamamen doldurmasını ve içeriğin sağ üst köşede konumlanmasını sağlar.

Bu örnek, `object-fit` ve `object-position` özelliklerinin nasıl kullanılacağını açıkça göstermektedir. Her iki özellik de, görsellerin ve videoların bir web sayfasında esnek ve duyarlı bir şekilde nasıl yerleştirileceğini kontrol etmek için kritik öneme sahiptir. Bu tür özelliklerin doğru kullanımı, kullanıcı deneyimini önemli ölçüde artırabilir.
