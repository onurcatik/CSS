# CSS Box Sizing Example

CSS `box-sizing` özelliğini açıklamak ve uygulamalı bir örnek sunmak için aşağıda ayrıntılı bir HTML ve CSS örneği verilmiştir. Bu örnek, `box-sizing` özelliğinin nasıl çalıştığını, farklı değerlerin (content-box ve border-box) öğe boyutlarını nasıl etkilediğini gösterecek ve bir `section` ve `footer` öğeleri içerecektir.

## HTML Kodu

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Box Sizing Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>CSS Box Sizing Örneği</h1>
    </header>
    <section>
        <h2>Content-Box Örneği</h2>
        <div class="content-box-example">
            <p>Bu kutu content-box kullanılarak boyutlandırılmıştır.</p>
        </div>
    </section>
    <section>
        <h2>Border-Box Örneği</h2>
        <div class="border-box-example">
            <p>Bu kutu border-box kullanılarak boyutlandırılmıştır.</p>
        </div>
    </section>
    <footer>
        <p>&copy; 2024 CSS Box Sizing Örneği. Tüm hakları saklıdır.</p>
    </footer>
</body>

</html>
```

## CSS Kodu

```css
*,
*::before,
*::after {
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1rem 0;
}

section {
    margin: 2rem;
    padding: 1rem;
    background-color: white;
    border: 1px solid #ddd;
    border-radius: 5px;
}

h2 {
    border-bottom: 2px solid #333;
    padding-bottom: 0.5rem;
    margin-bottom: 1rem;
}

.content-box-example {
    width: 300px;
    height: 200px;
    padding: 20px;
    border: 10px solid black;
    box-sizing: content-box;
    /* Varsayılan değeri belirtmek için */
    background-color: #e0e0e0;
    margin-bottom: 2rem;
}

.border-box-example {
    width: 300px;
    height: 200px;
    padding: 20px;
    border: 10px solid black;
    box-sizing: border-box;
    background-color: #d0d0d0;
}

footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1rem 0;
    position: absolute;
    width: 100%;
    bottom: 0;
}
```

## Açıklamalar

### HTML Açıklamaları

* **`<header>`** : Sayfanın başlığını içerir. `h1` etiketi ile sayfa başlığı belirtilmiştir.
* **`<section>`** : İçerik bölümlerini gruplamak için kullanılmıştır. Her `section` içinde bir başlık (`h2`) ve içerik kutusu (`div`) bulunmaktadır.
* **`<footer>`** : Sayfanın alt bilgisini içerir. Telif hakkı bilgilerini içerir.

### CSS Açıklamaları

* **Genel Seçici** : `*`,  `*::before`,  `*::after` seçicileri ile tüm öğeler ve onların pseudo-elementleri için `box-sizing` özelliği `border-box` olarak ayarlanmıştır. Bu, tüm öğelerin aynı kutu boyutlandırma modelini kullanmasını sağlar.
* **Gövde (body)** : Sayfa genelinde kullanılan yazı tipi, margin, padding ve arka plan rengi ayarlanmıştır.
* **Başlık (header)** : Başlığın arka plan rengi, metin rengi, hizalama ve padding değerleri belirlenmiştir.
* **Bölüm (section)** : Bölümlerin margin, padding, arka plan rengi, kenarlık ve kenarlık yuvarlama özellikleri ayarlanmıştır.
* **Başlık 2 (h2)** : Başlıkların alt çizgisi, padding ve margin değerleri belirlenmiştir.
* **Content-Box ve Border-Box Örnekleri** : İki farklı kutu örneği için boyutlar, padding, kenarlık, arka plan rengi ve `box-sizing` değerleri ayarlanmıştır. `content-box` varsayılan değeriyle toplam boyuta padding ve kenarlık dahil edilmezken,  `border-box` ile dahil edilmiştir.
* **Alt Bilgi (footer)** : Alt bilginin arka plan rengi, metin rengi, hizalama ve padding değerleri belirlenmiştir.

### Sonuç

Bu örnek, `box-sizing` özelliğinin farklı değerlerinin nasıl çalıştığını ve öğe boyutlarını nasıl etkilediğini göstermektedir. `content-box` ve `border-box` değerleri, özellikle karmaşık düzenler oluştururken ve tarayıcılar arası tutarlılığı sağlamak için çok yararlıdır. Bu özelliği doğru kullanarak, daha esnek ve yönetilebilir tasarımlar oluşturabilirsiniz.
