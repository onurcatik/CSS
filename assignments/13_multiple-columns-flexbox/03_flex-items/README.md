## CSS Flex Items

Bu bölümde, CSS Flexbox düzen modelini kullanarak esnek bir düzen oluşturacağız. Örneğimizde bir header, iki section ve gelişmiş bir footer öğesi içereceğiz. Bu öğeler flex konteyner içinde yer alacak ve çeşitli flex öğesi özellikleri uygulanacaktır. HTML ve CSS dosyalarını ayrı olarak düzenleyeceğiz.

### HTML Kodu

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Flex Öğeleri Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header class="flex-container">
        <div class="flex-item">Logo</div>
        <div class="flex-item">Menü</div>
        <div class="flex-item">Arama</div>
    </header>

    <section class="flex-container">
        <div class="flex-item">Ana İçerik</div>
        <div class="flex-item">Yan İçerik</div>
    </section>

    <footer class="flex-container">
        <div class="flex-item">Alt Bilgi 1</div>
        <div class="flex-item">Alt Bilgi 2</div>
        <div class="flex-item">Alt Bilgi 3</div>
    </footer>
</body>
</html>
```

### CSS Kodu

```css
/* Genel stil */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

/* Flex konteynerler için stil */
.flex-container {
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 10px;
    border: 1px solid #ccc;
    margin: 10px;
}

/* Flex öğeleri için stil */
.flex-item {
    flex: 1;
    padding: 20px;
    text-align: center;
    border: 1px solid #000;
    margin: 5px;
}

/* Header özel stili */
header {
    background-color: #f4f4f4;
}

/* Section özel stili */
section {
    flex-direction: column;
}

section .flex-item {
    flex: 2;
    margin: 10px 0;
}

/* Footer özel stili */
footer {
    background-color: #333;
    color: white;
}

footer .flex-item {
    flex: 1;
}
```

### Açıklamalar (Türkçe)

**Flex Container ve Flex Items (Flex Konteyner ve Flex Öğeleri)**

Flex konteyner, esnek öğeler içeren bir kapsayıcıdır. İçerdiği doğrudan çocuk öğeleri (flex öğeler) üzerinde düzenleme yaparak daha esnek ve uyumlu yerleşimler oluşturabiliriz. Bu örnekte, header, section ve footer öğelerini flex konteyner olarak tanımladık ve içlerindeki öğeleri flex öğeler haline getirdik.

**1. Header (Üst Bilgi)**

Header içinde üç flex öğe bulunmaktadır: Logo, Menü ve Arama. `justify-content: space-around;` özelliği ile öğeler arasında eşit boşluk bırakılır ve `align-items: center;` ile dikey olarak ortalanır.

**2. Section (Bölüm)**

Section içinde iki flex öğe bulunmaktadır: Ana İçerik ve Yan İçerik. Bu öğeler, section içerisinde dikey olarak yerleştirilmiştir (`flex-direction: column;`). `flex: 2;` ile Ana İçerik öğesi, Yan İçerik öğesine göre daha fazla yer kaplar.

**3. Footer (Alt Bilgi)**

Footer içinde üç flex öğe bulunmaktadır: Alt Bilgi 1, Alt Bilgi 2 ve Alt Bilgi 3. `background-color: #333;` ile arka planı koyu renkle, `color: white;` ile metin rengi beyaz olarak belirlenmiştir. Flex özellikleri sayesinde footer öğeleri esnek ve eşit şekilde yerleştirilmiştir.

Bu örnek, CSS Flexbox özelliklerinin kullanımını göstermekte ve esnek düzenler oluştururken size rehberlik etmektedir. Flexbox ile esnek, uyumlu ve kullanıcı dostu web düzenleri oluşturabilirsiniz.