### HTML and CSS Color

Bu örnek, CSS renklerinin farklı yöntemlerle nasıl kullanılacağını gösteren kapsamlı bir örnek sunmaktadır. HTML ve CSS dosyalarını ayrı tutarak temiz ve düzenli bir yapı oluşturacağız.

#### HTML (index.html)

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Renk Örnekleri</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <div class="color-example color-name">Önceden Tanımlanmış Renk İsmi: Blue</div>
    <div class="color-example color-rgb">RGB Renk: rgb(255, 0, 0)</div>
    <div class="color-example color-hex">HEX Renk: #00FF00</div>
    <div class="color-example color-hsl">HSL Renk: hsl(240, 100%, 50%)</div>
    <div class="color-example color-rgba">RGBA Renk: rgba(255, 165, 0, 0.5)</div>
</body>

</html>
```

#### CSS (styles.css)

```css
body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    padding: 20px;
}

.color-example {
    padding: 20px;
    margin: 10px 0;
    border-radius: 5px;
    color: #ffffff;
    font-size: 16px;
    text-align: center;
}

/* Önceden Tanımlanmış Renk İsmi */
.color-name {
    background-color: blue;
    /* Önceden tanımlanmış renk ismi */
}

/* RGB Renk */
.color-rgb {
    background-color: rgb(255, 0, 0);
    /* RGB renk değeri */
}

/* HEX Renk */
.color-hex {
    background-color: #00FF00;
    /* HEX renk değeri */
}

/* HSL Renk */
.color-hsl {
    background-color: hsl(240, 100%, 50%);
    /* HSL renk değeri */
}

/* RGBA Renk */
.color-rgba {
    background-color: rgba(255, 165, 0, 0.5);
    /* RGBA renk değeri */
}
```

### Açıklamalar:

* **HTML Dosyası (index.html):** Bu dosya, sayfa yapısını içerir ve her bir renk türü için `div` elemanları kullanılarak renk örnekleri sunar. Her `div` elemanına belirli bir sınıf atanmıştır (`color-name`,  `color-rgb`,  `color-hex`,  `color-hsl`,  `color-rgba`).
* **CSS Dosyası (styles.css):** Bu dosya, her bir renk türü için stilleri tanımlar. `background-color` özelliği kullanılarak her `div` elemanına farklı bir renk atanmıştır.
  + `.color-name`: `background-color: blue;` kullanılarak önceden tanımlanmış bir renk atanmıştır.
  + `.color-rgb`: `background-color: rgb(255, 0, 0);` kullanılarak RGB renk değeri atanmıştır.
  + `.color-hex`: `background-color: #00FF00;` kullanılarak HEX renk değeri atanmıştır.
  + `.color-hsl`: `background-color: hsl(240, 100%, 50%);` kullanılarak HSL renk değeri atanmıştır.
  + `.color-rgba`: `background-color: rgba(255, 165, 0, 0.5);` kullanılarak RGBA renk değeri atanmıştır.

Bu örnek, CSS'de renklerin farklı yöntemlerle nasıl belirtileceğini açıkça göstermektedir. Her renk yöntemi için ayrı bir `div` elemanı oluşturulmuş ve her biri farklı bir arka plan rengi ile renklendirilmiştir. Bu sayede, her yöntem arasındaki farklar ve kullanım biçimleri net bir şekilde anlaşılabilir.
