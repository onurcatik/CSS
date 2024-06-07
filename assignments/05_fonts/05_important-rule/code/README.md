## !important 

Bu örnekte, `!important` kuralının kullanımını göstermek için bir HTML ve CSS dosyası oluşturacağız. Bu örnek, `!important` kuralının nasıl uygulandığını ve etkilerini açıkça gösterecektir.

### HTML Dosyası (index.html)

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>!important Kuralı Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>CSS !important Kuralı Örneği</h1>
    </header>
    <main>
        <section>
            <h2>Örnek İçerik</h2>
            <p class="highlight">Bu paragrafın arka plan rengi önemlidir.</p>
            <p class="highlight">Bu paragrafın yazı rengi önemlidir.</p>
            <p>Bu paragraf standart stil kurallarına sahiptir.</p>
        </section>
    </main>
</body>

</html>
```

### CSS Dosyası (styles.css)

```css
/* Genel stil kuralları */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
    color: #333;
}

header {
    background-color: #4CAF50;
    color: white;
    text-align: center;
    padding: 1em 0;
}

h1 {
    margin: 0;
}

main {
    padding: 2em;
}

section {
    background-color: white;
    padding: 1em;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    margin-bottom: 2em;
}

h2 {
    color: #4CAF50;
}

/* Standart stil kuralları */
.highlight {
    background-color: yellow;
    color: black;
    padding: 10px;
    border: 1px solid #ccc;
}

/* !important kuralı ile stil kuralları */
.highlight {
    background-color: orange !important;
}

.highlight {
    color: red !important;
}
```

### Açıklama

#### HTML Yapısı

* **Başlık ve İçerik:** `header` etiketi içinde sayfa başlığı (`h1`) yer alır. `main` etiketi içinde `section` etiketi ile bir bölüm oluşturulmuştur.
* **Paragraflar:** `section` içinde üç adet `p` etiketi ile paragraflar tanımlanmıştır. İki paragraf `highlight` sınıfına sahiptir, üçüncü paragraf ise standart stil kurallarına sahiptir.

#### CSS Yapısı

* **Genel Stil Kuralları:** `body`,  `header`, `h1`,  `main`, ve `section` etiketleri için genel stil kuralları tanımlanmıştır.
* **Standart Stil Kuralları:** `.highlight` sınıfına sahip paragraflar için arka plan rengi sarı ve yazı rengi siyah olarak tanımlanmıştır.
* **!important Kuralı ile Stil Kuralları:** `.highlight` sınıfı için arka plan rengi ve yazı rengi `!important` kuralı ile yeniden tanımlanmıştır. Bu kurallar, tüm diğer stil kurallarını geçersiz kılar.

#### Çalışma Mantığı

* İlk olarak,  `.highlight` sınıfı için standart stil kuralları tanımlanır.
* Daha sonra, aynı `.highlight` sınıfı için `!important` kuralı kullanılarak arka plan rengi ve yazı rengi yeniden tanımlanır.
* `!important` kuralı, önceki stil kurallarını geçersiz kılar ve `.highlight` sınıfına sahip paragraflar için arka plan rengi turuncu, yazı rengi ise kırmızı olur.

### Sonuç

Bu örnek, `!important` kuralının CSS'deki etkisini ve kullanımını açıkça göstermektedir. `!important` kuralı, belirli stil kurallarının öncelikli olmasını sağlarken, aynı zamanda stil dosyalarının yönetimini zorlaştırabileceği için dikkatli kullanılması gerekir. Bu örnek, `!important` kuralının nasıl çalıştığını ve doğru kullanımını anlamanıza yardımcı olacaktır.
