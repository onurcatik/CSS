### CSS 2D Dönüşümler: Ayrıntılı Örnek

Bu örnek, HTML ve CSS kullanarak CSS 2D dönüşüm metodlarını uygulayan bir web sayfası oluşturacaktır. Örnek, her dönüşüm metodunu içeren bir bölüm (`section`) ve alt bilgi (`footer`) içerecektir.

#### HTML Kodu

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS 2D Dönüşümler</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>CSS 2D Dönüşümler</h1>
    </header>
    <section>
        <h2>translate() Metodu</h2>
        <div class="translate">Bu kutu translate() ile taşındı.</div>
        
        <h2>rotate() Metodu</h2>
        <div class="rotate">Bu kutu rotate() ile döndürüldü.</div>
        
        <h2>scale() Metodu</h2>
        <div class="scale">Bu kutu scale() ile ölçeklendirildi.</div>
        
        <h2>skewX() Metodu</h2>
        <div class="skewX">Bu kutu skewX() ile eğildi.</div>
        
        <h2>skewY() Metodu</h2>
        <div class="skewY">Bu kutu skewY() ile eğildi.</div>
        
        <h2>matrix() Metodu</h2>
        <div class="matrix">Bu kutu matrix() ile dönüşüm uygulandı.</div>
    </section>
    <footer>
        <p>Bu örnek, CSS 2D dönüşümlerini göstermek amacıyla hazırlanmıştır.</p>
    </footer>
</body>
</html>
```

#### CSS Kodu

```css
/* styles.css */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: white;
    padding: 10px 0;
    text-align: center;
}

section {
    margin: 20px;
    padding: 20px;
    background-color: white;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

section div {
    margin: 20px 0;
    padding: 20px;
    background-color: #eaeaea;
    text-align: center;
    transition: transform 0.5s;
}

footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px 0;
    position: fixed;
    width: 100%;
    bottom: 0;
}

/* Transformations */
.translate {
    transform: translate(50px, 100px);
}

.rotate {
    transform: rotate(45deg);
}

.scale {
    transform: scale(1.5, 1.5);
}

.skewX {
    transform: skewX(30deg);
}

.skewY {
    transform: skewY(30deg);
}

.matrix {
    transform: matrix(1, 0.5, -0.5, 1, 30, 30);
}
```

### Açıklama

#### HTML Yapısı
- **header**: Sayfa başlığını içerir.
- **section**: Farklı CSS 2D dönüşüm metodlarının her birini göstermek için ayrı bölümler içerir.
- **footer**: Sayfanın alt kısmında yer alır ve örneğin amacını belirtir.

#### CSS Yapısı
- **Genel Stiller**: Sayfa genelinde kullanılan font, renk, margin ve padding ayarları yapılmıştır.
- **header** ve **footer**: Arka plan renkleri ve metin hizalamaları ayarlanmıştır.
- **section**: Her bir dönüşüm metodunu gösteren `div` elementleri stilize edilmiştir.
- **Dönüşümler**: Her dönüşüm metodu için ayrı ayrı `transform` özellikleri kullanılarak örnekler oluşturulmuştur.

Bu örnek, CSS 2D dönüşüm metodlarının nasıl kullanıldığını göstermektedir. Her metodun kullanımı ve etkisi, farklı renk ve stil özellikleri ile vurgulanmıştır. Bu yapıyı kendi projelerinizde kullanarak öğelerinizi dinamik hale getirebilirsiniz.