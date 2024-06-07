## CSS Grid Container

### HTML Kodu

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Grid Container Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>CSS Grid Layout</h1>
    </header>
    <section class="container">
        <div class="item item1">1</div>
        <div class="item item2">2</div>
        <div class="item item3">3</div>
        <div class="item item4">4</div>
        <div class="item item5">5</div>
        <div class="item item6">6</div>
    </section>
    <footer>
        <p>Bu, bir CSS Grid Layout örneğidir.</p>
    </footer>
</body>
</html>
```

### CSS Kodu

```css
/* styles.css */

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

header, footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1em 0;
}

header {
    flex-shrink: 0;
}

footer {
    flex-shrink: 0;
    margin-top: auto;
}

.container {
    display: grid;
    grid-template-columns: 100px 1fr 1fr;
    grid-template-rows: 100px 100px;
    gap: 10px;
    padding: 10px;
    background-color: #f2f2f2;
    flex-grow: 1;
}

.item {
    background-color: #4CAF50;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 1.5em;
}

.item1 { grid-column: 1; grid-row: 1; }
.item2 { grid-column: 2; grid-row: 1; }
.item3 { grid-column: 3; grid-row: 1; }
.item4 { grid-column: 1; grid-row: 2; }
.item5 { grid-column: 2; grid-row: 2; }
.item6 { grid-column: 3; grid-row: 2; }
```

### Açıklama

Bu örnek, CSS Grid Layout'un temel özelliklerini gösteren basit bir düzen sunmaktadır. HTML ve CSS kodları ayrı dosyalara ayrılmıştır ve her iki dosya da kapsamlı bir şekilde açıklanmıştır.

#### HTML Yapısı

HTML yapısı, başlık (`header`), içerik bölümü (`section`), ve alt bilgi (`footer`) olmak üzere üç ana bölümden oluşur. `section` öğesi, grid konteyner olarak tanımlanmıştır ve altı adet grid öğesi (`item`) içermektedir.

```html
<section class="container">
    <div class="item item1">1</div>
    <div class="item item2">2</div>
    <div class="item item3">3</div>
    <div class="item item4">4</div>
    <div class="item item5">5</div>
    <div class="item item6">6</div>
</section>
```

#### CSS Yapısı

CSS kodunda, önce genel stil kuralları tanımlanmıştır. `body`, `header`, ve `footer` için temel stiller verilmiştir. `container` sınıfı, grid konteyner olarak tanımlanmış ve grid düzeni oluşturulmuştur.

```css
.container {
    display: grid;
    grid-template-columns: 100px 1fr 1fr;
    grid-template-rows: 100px 100px;
    gap: 10px;
    padding: 10px;
    background-color: #f2f2f2;
    flex-grow: 1;
}
```

Bu kısımda, üç sütun ve iki satırdan oluşan bir grid düzeni tanımlanmıştır. İlk sütun 100 piksel genişliğindeyken, diğer iki sütun kalan alanın eşit paylaşımlı kısımlarını temsil etmektedir. Satırlar 100 piksel yüksekliğindedir. `gap` özelliği, grid öğeleri arasındaki boşluğu 10 piksel olarak ayarlamaktadır.

Her bir grid öğesi için özel stiller tanımlanmış ve grid konumları belirlenmiştir:

```css
.item1 { grid-column: 1; grid-row: 1; }
.item2 { grid-column: 2; grid-row: 1; }
.item3 { grid-column: 3; grid-row: 1; }
.item4 { grid-column: 1; grid-row: 2; }
.item5 { grid-column: 2; grid-row: 2; }
.item6 { grid-column: 3; grid-row: 2; }
```

Bu kod parçaları, her bir grid öğesinin hangi sütunda ve satırda yer alacağını belirler.

### Sonuç

Bu örnek, CSS Grid Layout kullanarak basit ama etkili bir web sayfası düzeni oluşturmayı göstermektedir. Grid Layout, karmaşık düzenlerin kolayca yönetilmesini sağlar ve modern web tasarımında güçlü bir araçtır. Bu rehber, CSS Grid Layout'un temellerini anlamanıza ve pratik bir uygulama yapmanıza yardımcı olacaktır.