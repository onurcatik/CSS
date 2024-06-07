### CSS İcon

Bu bölümde, Font Awesome ikonlarını kullanarak bir HTML sayfası oluşturacağız. CSS ve HTML kodlarını ayrı dosyalarda tutacağız. Bu uygulama, Font Awesome ikonlarını nasıl entegre edeceğinizi ve özelleştireceğinizi gösterecektir.

#### 1. HTML Dosyası ( `index.html` )

Öncelikle, HTML dosyanızı oluşturun ve Font Awesome CDN kodunu `<head>` bölümüne ekleyin. Ardından, ikonları `<body>` bölümünde kullanın.

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Font Awesome İkonları Örneği</title>
    <!-- Font Awesome CDN Kodu -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- CSS Dosyasını Ekleyin -->
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <h1>Font Awesome İkonları Örneği</h1>
    <div class="icon-container">
        <i class="fas fa-heart"></i> <!-- Solid kalp ikonu -->
        <i class="far fa-heart"></i> <!-- Regular kalp ikonu -->
        <i class="fab fa-twitter"></i> <!-- Twitter marka ikonu -->
    </div>
</body>

</html>
```

#### 2. CSS Dosyası ( `styles.css` )

Şimdi, ikonları özelleştirmek için CSS dosyanızı oluşturun.

```css
/* styles.css */
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    text-align: center;
    margin: 0;
    padding: 0;
}

h1 {
    color: #333;
    margin-top: 20px;
}

.icon-container {
    margin-top: 50px;
}

.icon-container i {
    margin: 20px;
    font-size: 50px;
    transition: color 0.3s ease, transform 0.3s ease;
}

.icon-container i:hover {
    color: #ff6347;
    /* Hover sırasında ikon rengi */
    transform: scale(1.2);
    /* Hover sırasında ikon büyütme */
}
```

### Sonuç

Bu örnekte, HTML ve CSS dosyalarını ayırarak Font Awesome ikonlarını nasıl entegre edeceğinizi ve özelleştireceğinizi gösterdik. HTML dosyasında ikonları yerleştirip, CSS dosyasında ikonların stilini belirledik. İkonların üzerine gelindiğinde renk ve boyut değişiklikleri yaparak, kullanıcı etkileşimini artırdık. Bu yöntemi kullanarak, web projelerinizde estetik ve işlevsel ikonlar ekleyebilir, sayfalarınızın görsel çekiciliğini ve kullanıcı deneyimini geliştirebilirsiniz.
