### CSS Görsel Spriteleri: Kapsamlı Örnek

Bu bölümde, CSS görsel spritelerini kullanarak bir web sayfası oluşturacağız. Örneğimizde bir HTML dosyası ve bir CSS dosyası ayrı olarak yapılandırılacaktır. Ayrıca, `<section>` ve `<footer>` etiketlerini de ekleyeceğiz.

#### HTML Dosyası (`index.html`)

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Görsel Spriteleri Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>CSS Görsel Spriteleri</h1>
    </header>
    
    <section>
        <h2>İkonlar</h2>
        <div class="icon-container">
            <div class="icon icon1"></div>
            <div class="icon icon2"></div>
            <div class="icon icon3"></div>
            <div class="icon icon4"></div>
        </div>
    </section>
    
    <footer>
        <p>&copy; 2024 CSS Görsel Spriteleri Örneği</p>
    </footer>
</body>
</html>
```

#### CSS Dosyası (`styles.css`)

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: #fff;
    padding: 10px 0;
    text-align: center;
}

header h1 {
    margin: 0;
}

section {
    padding: 20px;
    text-align: center;
}

section h2 {
    margin-bottom: 20px;
}

.icon-container {
    display: flex;
    justify-content: center;
    gap: 10px;
}

.icon {
    background-image: url('sprite_example.png');
    background-repeat: no-repeat;
    display: inline-block;
}

.icon1 {
    width: 50px;
    height: 50px;
    background-position: 0 0; /* İlk ikon */
}

.icon2 {
    width: 50px;
    height: 50px;
    background-position: -50px 0; /* İkinci ikon */
}

.icon3 {
    width: 50px;
    height: 50px;
    background-position: -100px 0; /* Üçüncü ikon */
}

.icon4 {
    width: 50px;
    height: 50px;
    background-position: -150px 0; /* Dördüncü ikon */
}

footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 10px 0;
    position: fixed;
    width: 100%;
    bottom: 0;
}
```

#### Açıklama

Bu örnekte, bir web sayfasında görsel spritelerin nasıl kullanılacağını gösteriyoruz. 

1. **HTML Dosyası:**
    - Başlık ve meta etiketleri ile temel HTML yapısı oluşturulmuştur.
    - `header` etiketinde sayfa başlığı yer almaktadır.
    - `section` etiketi altında, dört farklı ikon içeren bir `icon-container` div'i bulunmaktadır.
    - `footer` etiketi ile sayfa alt kısmında bir telif hakkı bilgisi gösterilmektedir.

2. **CSS Dosyası:**
    - Temel stil kuralları belirlenmiştir.
    - `icon` sınıfı, sprite görüntüsünün arka plan olarak ayarlandığı temel bir sınıftır.
    - `icon1`, `icon2`, `icon3`, ve `icon4` sınıfları, sprite görüntüsünün farklı bölümlerini gösterecek şekilde ayarlanmıştır.
    - `footer` etiketi, sayfanın alt kısmında sabit bir konumda olacak şekilde stilize edilmiştir.

Bu örnek, CSS görsel spritelerinin nasıl kullanılacağını ve HTML ile CSS dosyalarının nasıl organize edileceğini göstermektedir. Spriteler, HTTP isteklerini azaltarak sayfa performansını artırır ve bakım sürecini kolaylaştırır. Bu teknik, özellikle birçok küçük simgenin kullanıldığı projelerde büyük fayda sağlar.