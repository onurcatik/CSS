### CSS Opacity - Transparency

Aşağıda, HTML ve CSS kullanarak opaklık ve şeffaflık özelliklerinin nasıl uygulanacağını gösteren kapsamlı bir örnek yer almaktadır. Bu örnek, iki bölüme ayrılmıştır: HTML ve CSS. Her bölüm, ilgili kod parçalarını ve açıklamalarını içermektedir.

#### HTML Kodu

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Opaklık ve Şeffaflık Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Opaklık ve Şeffaflık Örneği</h1>
        <div class="example">
            <div class="opaque">Opak Element</div>
            <div class="semi-transparent">Yarı Saydam Element</div>
            <div class="transparent">Tamamen Şeffaf Element</div>
        </div>
        <div class="example">
            <div class="rgba-bg">RGBA Arka Plan</div>
            <div class="hsla-bg">HSLA Arka Plan</div>
        </div>
    </div>
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
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f0f0f0;
}

.container {
    text-align: center;
}

.example {
    margin: 20px 0;
}

.opaque {
    background-color: #007BFF;
    color: white;
    padding: 20px;
    margin: 10px;
    opacity: 1.0;
}

.semi-transparent {
    background-color: #28A745;
    color: white;
    padding: 20px;
    margin: 10px;
    opacity: 0.5;
}

.transparent {
    background-color: #DC3545;
    color: white;
    padding: 20px;
    margin: 10px;
    opacity: 0.0;
}

.rgba-bg {
    background-color: rgba(255, 0, 0, 0.5);
    color: white;
    padding: 20px;
    margin: 10px;
}

.hsla-bg {
    background-color: hsla(120, 100%, 50%, 0.3);
    color: black;
    padding: 20px;
    margin: 10px;
}
```

### Açıklama

Bu örnek, HTML ve CSS dosyalarının ayrı tutulduğu bir yapıya sahiptir. HTML dosyası, sayfa yapısını ve içerik düzenini sağlar. CSS dosyası ise stil tanımlamalarını içerir.

#### HTML Açıklaması

HTML dosyasında, iki adet `div` öğesi bulunmaktadır. İlk `div` öğesi, üç farklı opaklık seviyesini gösteren üç alt `div` içerir:
- `.opaque`: Tamamen opak bir öğe.
- `.semi-transparent`: Yarı saydam bir öğe.
- `.transparent`: Tamamen şeffaf bir öğe.

İkinci `div` öğesi, RGBA ve HSLA renk modelleriyle arka plan şeffaflığı uygulanan iki alt `div` içerir:
- `.rgba-bg`: RGBA ile yarı saydam arka plan.
- `.hsla-bg`: HSLA ile yarı saydam arka plan.

#### CSS Açıklaması

CSS dosyasında, her sınıf için stil tanımlamaları yapılmıştır:
- `.opaque`, `.semi-transparent`, `.transparent`: Bu sınıflar, opaklık seviyelerini belirlemek için `opacity` özelliğini kullanır.
- `.rgba-bg`: RGBA renk modeli ile arka plan rengi tanımlanmıştır.
- `.hsla-bg`: HSLA renk modeli ile arka plan rengi tanımlanmıştır.

### Sonuç

Bu örnek, opaklık ve şeffaflık özelliklerinin HTML ve CSS kullanılarak nasıl uygulanabileceğini göstermektedir. Opaklık özelliği, öğelerin görünürlüğünü ayarlamak için kullanılırken, RGBA ve HSLA renk modelleri, arka plan renklerinin saydamlığını belirlemek için kullanılabilir. Bu teknikler, web tasarımında estetik ve işlevsellik açısından önemli araçlardır.