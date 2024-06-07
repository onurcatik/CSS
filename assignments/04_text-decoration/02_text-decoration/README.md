### HTML and CSS Text Decoration Example

Aşağıda, HTML ve CSS kullanarak metin süsleme özelliklerinin nasıl uygulanacağını gösteren kapsamlı ve detaylı bir örnek bulunmaktadır. Bu örnekte, çeşitli `text-decoration` özelliklerini kullanarak metinlerin nasıl süsleneceği gösterilecektir.

#### HTML Kodu (index.html)

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Metin Süsleme Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>CSS Metin Süsleme Özellikleri</h1>
    </header>
    <main>
        <section>
            <h2>text-decoration-line Örneği</h2>
            <p class="underline">Bu metnin altı çizili.</p>
            <p class="overline">Bu metnin üstü çizili.</p>
            <p class="line-through">Bu metnin ortasından bir çizgi geçiyor.</p>
        </section>
        <section>
            <h2>text-decoration-color Örneği</h2>
            <p class="underline-red">Bu metnin altı kırmızı çizili.</p>
        </section>
        <section>
            <h2>text-decoration-style Örneği</h2>
            <p class="underline-wavy">Bu metnin altı dalgalı çizili.</p>
            <p class="underline-dotted">Bu metnin altı noktalı çizili.</p>
            <p class="underline-dashed">Bu metnin altı kesik çizili.</p>
        </section>
        <section>
            <h2>text-decoration-thickness Örneği</h2>
            <p class="underline-thick">Bu metnin altı 4 piksel kalınlığında çizili.</p>
        </section>
        <section>
            <h2>text-decoration Birleşik Örneği</h2>
            <p class="combined-decoration">Bu metnin altı dalgalı, kırmızı ve 2 piksel kalınlığında çizili.</p>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 CSS Metin Süsleme Örneği</p>
    </footer>
</body>

</html>
```

#### CSS Kodu (styles.css)

```css
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 0;
}

header {
    background-color: #4CAF50;
    color: white;
    padding: 1em 0;
    text-align: center;
}

main {
    padding: 2em;
}

section {
    margin-bottom: 2em;
}

h2 {
    border-bottom: 2px solid #4CAF50;
    padding-bottom: 0.5em;
}

p {
    margin: 0.5em 0;
}

/* text-decoration-line örnekleri */
.underline {
    text-decoration-line: underline;
}

.overline {
    text-decoration-line: overline;
}

.line-through {
    text-decoration-line: line-through;
}

/* text-decoration-color örneği */
.underline-red {
    text-decoration-line: underline;
    text-decoration-color: red;
}

/* text-decoration-style örnekleri */
.underline-wavy {
    text-decoration-line: underline;
    text-decoration-style: wavy;
}

.underline-dotted {
    text-decoration-line: underline;
    text-decoration-style: dotted;
}

.underline-dashed {
    text-decoration-line: underline;
    text-decoration-style: dashed;
}

/* text-decoration-thickness örneği */
.underline-thick {
    text-decoration-line: underline;
    text-decoration-thickness: 4px;
}

/* text-decoration birleşik örneği */
.combined-decoration {
    text-decoration: underline wavy red 2px;
}

footer {
    background-color: #4CAF50;
    color: white;
    text-align: center;
    padding: 1em 0;
    position: fixed;
    width: 100%;
    bottom: 0;
}
```

### Açıklama

Bu örnekte, HTML ve CSS kullanarak çeşitli `text-decoration` özelliklerini uyguladık:

* **text-decoration-line** : Metne alt çizgi, üst çizgi ve ortadan çizgi ekledik.
* **text-decoration-color** : Süsleme çizgisinin rengini kırmızı yaptık.
* **text-decoration-style** : Süsleme çizgisinin stilini dalgalı, noktalı ve kesik çizgi olarak ayarladık.
* **text-decoration-thickness** : Süsleme çizgisinin kalınlığını 4 piksel yaptık.
* **text-decoration** : Birleşik olarak dalgalı, kırmızı ve 2 piksel kalınlığında alt çizgi ekledik.

Footer bölümü, sayfanın alt kısmında sabit bir şekilde duracak şekilde tasarlanmıştır. Bu, kullanıcı deneyimini artırmak için yaygın bir uygulamadır.
