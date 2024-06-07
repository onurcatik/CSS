# CSS Specifiy

CSS özgüllük, web sayfasındaki bir elemente uygulanacak stil kurallarının belirlenmesinde kritik bir rol oynar. Bu bölümde, özgüllük kavramını detaylı bir şekilde inceleyecek ve pratik bir örnek ile konuyu pekiştireceğiz.

## Özgüllük Hesaplaması ve Öncelik Sıralaması

Özgüllük hesaplaması, belirli bir seçicinin diğer seçicilere göre önceliğini belirler. Aşağıda, CSS seçicilerinin özgüllük seviyelerini ve hesaplama yöntemlerini tekrar gözden geçirelim:

1. **Satır İçi Stiller (Inline Styles)**: Örnek: `<h1 style="color: pink;">`
2. **ID Seçicileri**: Örnek: `#navbar`
3. **Sınıflar, Pseudo-sınıflar, Özellik Seçicileri**: Örnek: `.test`, `:hover`, `[href]`
4. **Elementler ve Pseudo-elementler**: Örnek: `h1`, `:before`

### Özgüllük Hesaplama Yöntemi

- Her bir ID değeri için 100 eklenir.
- Her bir sınıf değeri (veya pseudo-sınıf veya özellik seçici) için 10 eklenir.
- Her bir element seçici veya pseudo-element için 1 eklenir.

Şimdi bu bilgileri kullanarak, HTML ve CSS kodlarıyla örnek bir proje yapalım.

## Örnek Proje: Özgüllük Uygulaması

### HTML Kodu

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Özgüllük Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1 id="main-title" class="title">CSS Özgüllük Örneği</h1>
    </header>
    <section>
        <h2 class="subtitle">Örnek İçerik</h2>
        <p id="intro" class="text">Bu, CSS özgüllük kavramını açıklayan örnek bir paragraftır.</p>
        <p class="text">Bu paragraf da aynı sınıfa sahiptir, ancak ID kullanımı ile farklı bir stil uygulanabilir.</p>
    </section>
    <footer>
        <p class="footer-text">Bu, footer kısmındaki örnek bir metindir.</p>
    </footer>
</body>
</html>
```

### CSS Kodu

```css
/* styles.css */

body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px 0;
}

#main-title {
    color: blue;
}

.title {
    color: red; /* Bu stil ID'ye göre geçersiz kılınır */
}

section {
    padding: 20px;
}

.subtitle {
    color: green;
}

.text {
    color: black;
}

#intro {
    color: orange; /* Bu stil class'a göre geçersiz kılınır */
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

.footer-text {
    font-size: 12px;
}
```

### Açıklama

Bu örnekte, HTML ve CSS kodlarını ayrı dosyalarda düzenledik. HTML dosyasında başlık, içerik bölümü ve footer kısımlarını tanımladık. CSS dosyasında ise bu elementlere stil uyguladık. İşte bazı kritik noktalar:

- `#main-title` ID seçicisi, `color: blue;` stili ile diğer tüm seçicileri geçersiz kılar.
- `.title` sınıf seçicisi, `color: red;` stili ile ID seçicisine karşı kaybeder.
- `#intro` ID seçicisi, `color: orange;` stili ile aynı elemente uygulanan `.text` sınıf seçicisini geçersiz kılar.

Bu örnek, CSS özgüllüğünün nasıl çalıştığını ve belirli stillerin diğerlerine göre nasıl önceliklendirildiğini açıkça göstermektedir. Her seçicinin özgüllüğünü doğru bir şekilde hesaplayarak ve anlayarak, web sayfalarınızın beklediğiniz gibi görünmesini sağlayabilirsiniz.