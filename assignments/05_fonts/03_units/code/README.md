### CSS Units

Bu örnekte, HTML ve CSS dosyalarını ayırarak farklı CSS uzunluk birimlerinin kullanımını göstereceğiz.

#### HTML (index.html)
```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Uzunluk Birimleri Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>CSS Uzunluk Birimleri</h1>
    </header>
    <main>
        <section class="absolute-units">
            <h2>Mutlak Uzunluk Birimleri</h2>
            <p>Bu bölümde, mutlak uzunluk birimlerinin nasıl kullanılacağını gösteriyoruz.</p>
            <div class="absolute-example">Bu kutu 1cm kenar boşluğuna ve 10px dolguya sahiptir.</div>
        </section>
        <section class="relative-units">
            <h2>Göreli Uzunluk Birimleri</h2>
            <p>Bu bölümde, göreli uzunluk birimlerinin nasıl kullanılacağını gösteriyoruz.</p>
            <div class="relative-example">Bu kutu, yazı tipi boyutuna göre ölçeklenir.</div>
        </section>
        <section class="viewport-units">
            <h2>Viewport Uzunluk Birimleri</h2>
            <p>Bu bölümde, viewport uzunluk birimlerinin nasıl kullanılacağını gösteriyoruz.</p>
            <div class="viewport-example">Bu kutu, viewport boyutuna göre ölçeklenir.</div>
        </section>
    </main>
</body>
</html>
```

#### CSS (styles.css)
```css
/* Temel stil */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f0f0f0;
}

header {
    background-color: #333;
    color: #fff;
    padding: 20px;
    text-align: center;
}

main {
    padding: 20px;
}

h1, h2 {
    color: #333;
}

/* Mutlak Uzunluk Birimleri */
.absolute-units .absolute-example {
    width: 5cm;
    height: 2cm;
    margin: 1cm;
    padding: 10px;
    background-color: #4CAF50;
    color: #fff;
    text-align: center;
}

/* Göreli Uzunluk Birimleri */
.relative-units {
    font-size: 16px;
}

.relative-units .relative-example {
    width: 20em;
    height: 10em;
    margin: 2em;
    padding: 1em;
    background-color: #2196F3;
    color: #fff;
    text-align: center;
}

/* Viewport Uzunluk Birimleri */
.viewport-units .viewport-example {
    width: 50vw;
    height: 30vh;
    margin: 5vh;
    padding: 2vw;
    background-color: #FF5722;
    color: #fff;
    text-align: center;
}
```

### Açıklama

#### HTML Dosyası (index.html)

- `<!DOCTYPE html>`: HTML5 belgesi olarak tanımlar.
- `<html lang="tr">`: Belgenin dilini Türkçe olarak ayarlar.
- `<meta charset="UTF-8">`: Belgenin karakter kodlamasını belirtir.
- `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Mobil cihazlar için ölçekleme ayarlarını yapar.
- `<link rel="stylesheet" href="styles.css">`: CSS dosyasını belgeye dahil eder.

Belgenin ana yapısı üç ana bölümden oluşur: `header`, `main`, ve `section` etiketleri kullanılarak CSS uzunluk birimlerinin farklı türleri gösterilir.

#### CSS Dosyası (styles.css)

- Temel stil kuralları, tüm belge için uygulanır.
- `absolute-units` sınıfında mutlak uzunluk birimleri kullanılır.
- `relative-units` sınıfında göreli uzunluk birimleri kullanılır.
- `viewport-units` sınıfında viewport uzunluk birimleri kullanılır.

Bu örnek, CSS uzunluk birimlerinin nasıl çalıştığını ve farklı birimlerin nasıl kullanılacağını açıkça göstermektedir. Her birim türü için ayrı bölümler ve örnekler sağlanarak, kavramların daha iyi anlaşılması hedeflenmiştir.