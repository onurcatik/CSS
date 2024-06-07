### CSS Grid Items Naming 

#### Giriş

Bu bölümde, CSS Grid Layout ile grid öğelerine isim verme konusunu ele alacağız. Detaylı bir örnek üzerinden, HTML ve CSS kodlarını ayrı ayrı göstererek, grid öğelerinin nasıl isimlendirileceğini ve yerleşim düzeninin nasıl oluşturulacağını açıklayacağız. Ek olarak, `<section>` ve `<footer>` etiketlerini kullanarak, grid yerleşimini daha da zenginleştireceğiz.

#### HTML Kodu

Aşağıdaki HTML kodu, grid layout için bir yapı tanımlar ve çeşitli grid öğelerini içerir.

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Grid Öğeleri İsimlendirme</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <header class="header">Başlık</header>
        <section class="main">Ana İçerik</section>
        <aside class="sidebar">Kenar Çubuğu</aside>
        <footer class="footer">Alt Bilgi</footer>
    </div>
</body>
</html>
```

#### CSS Kodu

Aşağıdaki CSS kodu, HTML yapısının grid layout'unu tanımlar ve grid öğelerine isimler atar.

```css
/* styles.css */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

.container {
    display: grid;
    grid-template-areas:
        'header header header'
        'sidebar main main'
        'footer footer footer';
    grid-gap: 10px;
    padding: 10px;
}

.header {
    grid-area: header;
    background-color: #f8b400;
    padding: 20px;
    text-align: center;
    font-size: 24px;
}

.main {
    grid-area: main;
    background-color: #4caf50;
    padding: 20px;
    font-size: 18px;
}

.sidebar {
    grid-area: sidebar;
    background-color: #2196f3;
    padding: 20px;
    font-size: 18px;
}

.footer {
    grid-area: footer;
    background-color: #555;
    color: white;
    padding: 20px;
    text-align: center;
    font-size: 16px;
}
```

#### Açıklama

- **Grid Yapısının Tanımlanması:** `display: grid;` özelliği, `.container` sınıfına sahip div'in bir grid konteyneri olmasını sağlar. `grid-template-areas` özelliği ise grid alanlarının düzenini tanımlar. Bu düzen, `header`, `main`, `sidebar` ve `footer` alanlarını içerir.
  
- **Grid Öğelerine İsim Verme:** Her grid öğesine, `grid-area` özelliği kullanılarak bir isim atanır. Örneğin, `.header` sınıfına sahip öğe `grid-area: header;` ile tanımlanmıştır. Bu isimler, `grid-template-areas` özelliğinde kullanılarak öğelerin yerleşimi belirlenir.

- **Stil Ayarları:** Her bir grid öğesi, farklı arka plan renkleri ve padding değerleri ile stilize edilmiştir. Bu stil ayarları, öğelerin sayfa üzerinde daha belirgin ve anlaşılır olmasını sağlar.

#### Sonuç

Bu kapsamlı örnek, CSS Grid Layout kullanarak grid öğelerine nasıl isim verileceğini ve bu isimlerin grid şablonlarında nasıl kullanılacağını göstermektedir. HTML ve CSS kodlarının ayrı ayrı sunulması, kodun okunabilirliğini ve yönetilebilirliğini artırır. `<section>` ve `<footer>` etiketlerinin kullanılması, sayfanın semantik yapısını zenginleştirir ve daha iyi bir kullanıcı deneyimi sağlar. Bu teknikler, web sayfalarınızda daha esnek ve yönetilebilir düzenler oluşturmanıza yardımcı olacaktır.