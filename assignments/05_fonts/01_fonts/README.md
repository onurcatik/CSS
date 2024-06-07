### HTML and CSS Fonts

Bu örnek, yukarıdaki konuları birleştirerek HTML ve CSS ile nasıl uygulanabileceğini göstermektedir.

#### HTML Dosyası (index.html)

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Yazı Tipleri Örneği</title>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>CSS Yazı Tipleri Örneği</h1>
    </header>
    <main>
        <section>
            <h2>Font Family Özelliği</h2>
            <p class="font-family">Bu metin Arial, Helvetica ve sans-serif yedek yazı tipleri kullanılarak gösterilmektedir.</p>
        </section>
        <section>
            <h2>Font Style Özelliği</h2>
            <p class="font-style-normal">Bu metin normal stil ile gösterilmektedir.</p>
            <p class="font-style-italic">Bu metin italik stil ile gösterilmektedir.</p>
            <p class="font-style-oblique">Bu metin eğik (oblique) stil ile gösterilmektedir.</p>
        </section>
        <section>
            <h2>Font Weight Özelliği</h2>
            <p class="font-weight-normal">Bu metin normal ağırlık ile gösterilmektedir.</p>
            <p class="font-weight-bold">Bu metin kalın ağırlık ile gösterilmektedir.</p>
        </section>
        <section>
            <h2>Font Variant Özelliği</h2>
            <p class="font-variant-small-caps">Bu metin küçük büyük harflerle gösterilmektedir.</p>
        </section>
        <section>
            <h2>Font Size Özelliği</h2>
            <p class="font-size-small">Bu metin küçük boyut ile gösterilmektedir.</p>
            <p class="font-size-medium">Bu metin orta boyut ile gösterilmektedir.</p>
            <p class="font-size-large">Bu metin büyük boyut ile gösterilmektedir.</p>
        </section>
    </main>
</body>

</html>
```

#### CSS Dosyası (styles.css)

```css
body {
    font-family: 'Roboto', sans-serif;
    margin: 0;
    padding: 0;
    line-height: 1.6;
}

header {
    background-color: #f4f4f4;
    padding: 20px;
    text-align: center;
}

h1,
h2 {
    font-weight: bold;
}

section {
    margin: 20px;
    padding: 10px;
    border-bottom: 1px solid #ddd;
}

.font-family {
    font-family: "Arial", "Helvetica", sans-serif;
}

.font-style-normal {
    font-style: normal;
}

.font-style-italic {
    font-style: italic;
}

.font-style-oblique {
    font-style: oblique;
}

.font-weight-normal {
    font-weight: 400;
}

.font-weight-bold {
    font-weight: 700;
}

.font-variant-small-caps {
    font-variant: small-caps;
}

.font-size-small {
    font-size: 12px;
}

.font-size-medium {
    font-size: 16px;
}

.font-size-large {
    font-size: 24px;
}
```

Bu örnekte, çeşitli CSS özelliklerini kullanarak yazı tiplerinin nasıl özelleştirileceğini gösterdik. HTML dosyasında farklı CSS sınıfları ile metinlerin stilini belirledik ve CSS dosyasında bu sınıfların stillerini tanımladık. Google Fonts'tan `Roboto` yazı tipini kullanarak genel yazı tipi stilini belirledik ve çeşitli örneklerle diğer CSS özelliklerini uyguladık.
