### CSS Functions

Bu bölümde, HTML ve CSS dosyalarının ayrı olduğu kapsamlı bir örnek üzerinden CSS fonksiyonlarının kullanımını ele alacağız. Bu örnekte, var(), linear-gradient() ve radial-gradient() fonksiyonlarını kullanarak bir web sayfası oluşturacağız.

#### HTML Dosyası (index.html)

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Fonksiyonları Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>CSS Fonksiyonları ile Stil Örneği</h1>
    </header>
    <section>
        <h2>var() Fonksiyonu Kullanımı</h2>
        <p class="primary-text">Bu metin, var() fonksiyonu kullanılarak tanımlanan bir renk ile renklendirildi.</p>
    </section>
    <section>
        <h2>linear-gradient() Fonksiyonu Kullanımı</h2>
        <div class="linear-gradient-box"></div>
    </section>
    <section>
        <h2>radial-gradient() Fonksiyonu Kullanımı</h2>
        <div class="radial-gradient-box"></div>
    </section>
    <footer>
        <p>&copy; 2024 CSS Fonksiyonları Eğitimi</p>
    </footer>
</body>

</html>
```

#### CSS Dosyası (styles.css)

```css
:root {
    --primary-color: #3498db;
    --secondary-color: #2ecc71;
}

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
    color: #333;
}

header {
    background-color: var(--primary-color);
    color: white;
    padding: 20px 0;
    text-align: center;
}

section {
    padding: 20px;
    margin: 20px;
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h2 {
    color: var(--primary-color);
}

.primary-text {
    color: var(--primary-color);
}

.linear-gradient-box {
    width: 100%;
    height: 200px;
    background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
    border-radius: 8px;
    margin-top: 10px;
}

.radial-gradient-box {
    width: 100%;
    height: 200px;
    background: radial-gradient(circle, var(--primary-color), var(--secondary-color));
    border-radius: 8px;
    margin-top: 10px;
}

footer {
    background-color: var(--primary-color);
    color: white;
    text-align: center;
    padding: 10px 0;
    position: fixed;
    width: 100%;
    bottom: 0;
}
```

### Açıklama

Bu örnekte, HTML ve CSS dosyaları ayrı olarak düzenlenmiştir. Örnek, header, section ve footer elemanlarını içermektedir. Her section, farklı bir CSS fonksiyonunun kullanımını göstermektedir:

1. **var() Fonksiyonu Kullanımı:** 
   - `:root` seçicisi altında `--primary-color` ve `--secondary-color` değişkenleri tanımlanmıştır.
   - Bu değişkenler, sayfanın farklı yerlerinde renk değerleri olarak kullanılmıştır.
   - Örneğin, `header` ve `h2` elemanlarının arka plan ve metin renkleri `var()` fonksiyonu ile atanmıştır.

2. **linear-gradient() Fonksiyonu Kullanımı:** 
   - `linear-gradient-box` sınıfı, iki renk arasında doğrusal bir geçiş oluşturmak için `linear-gradient()` fonksiyonunu kullanır.
   - Bu kutu, `var(--primary-color)` ve `var(--secondary-color)` renkleri arasında yatay bir geçişe sahiptir.

3. **radial-gradient() Fonksiyonu Kullanımı:** 
   - `radial-gradient-box` sınıfı, iki renk arasında radyal bir geçiş oluşturmak için `radial-gradient()` fonksiyonunu kullanır.
   - Bu kutu, `var(--primary-color)` ve `var(--secondary-color)` renkleri arasında dairesel bir geçişe sahiptir.

### Sonuç

Bu örnek, CSS fonksiyonlarının nasıl kullanılacağını gösteren kapsamlı bir uygulama sunmaktadır. `var()` , `linear-gradient()` ve `radial-gradient()` fonksiyonları, web sayfalarının stil ve düzenlemelerinde dinamik ve esnek çözümler sunar. Her bir fonksiyonun kullanımı ve avantajları, bu örnek ile net bir şekilde anlaşılabilir.
