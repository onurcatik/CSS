# Cursor Property

```html
<!DOCTYPE html> <!-- HTML5 belgesi olduğunu belirtir. -->
<html lang="tr"> <!-- Belgenin dilini Türkçe olarak ayarlar. -->
<head>
    <meta charset="UTF-8"> <!-- Karakter kodlamasını UTF-8 olarak ayarlar. -->
    <title>CSS İmleç Örneği</title> <!-- Belgenin başlığını ayarlar. -->
    <link rel="stylesheet" href="styles.css"> <!-- Dış CSS dosyasını bağlar. -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- Viewport ayarlarını yapar. -->
</head>
<body>
    <section>
        <h1>CSS İmleç Özelliği Örneği</h1>
        <div class="default">Varsayılan İmleç</div>
        <div class="pointer">Pointer İmleç</div>
        <div class="text">Metin İmleci</div>
        <div class="move">Hareket İmleci</div>
        <div class="not-allowed">Yasak İmleci</div>
        <div class="custom">Özelleştirilmiş İmleç</div>
    </section>
</body>
</html>
```

### Düzeltilmiş CSS Kodu

```css
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f0f0f0;
    margin: 0;
}

section {
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h1 {
    text-align: center;
    margin-bottom: 20px;
}

div {
    margin: 10px 0;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
}

.default {
    cursor: default;
}

.pointer {
    cursor: pointer;
}

.text {
    cursor: text;
}

.move {
    cursor: move;
}

.not-allowed {
    cursor: not-allowed;
}

.custom {
    cursor: url('custom-cursor.png'), auto;
}
```

### Açıklamalar ve Detaylar

#### HTML Dosyası Açıklamaları

- **`<!DOCTYPE html>`**: HTML5 belgesi olduğunu belirtir.
- **`<html lang="tr">`**: Belgenin dilini Türkçe olarak ayarlar.
- **`<meta charset="UTF-8">`**: Karakter kodlamasını UTF-8 olarak ayarlar.
- **`<title>CSS İmleç Örneği</title>`**: Belgenin başlığını ayarlar.
- **`<link rel="stylesheet" href="styles.css">`**: Dış CSS dosyasını bağlar.
- **`<meta name="viewport" content="width=device-width, initial-scale=1.0">`**: Viewport ayarlarını yapar. Bu, sayfanın mobil cihazlarda düzgün görüntülenmesini sağlar.
- **`<body>`**: Belge gövdesini tanımlar.
- **`<section>`**: İçerik bölümü için semantik bir elemandır.
- **`<h1>`**: Başlık etiketi.
- **`<div>`**: İmleç örnekleri için kapsayıcılar.

#### CSS Dosyası Açıklamaları

- **`body`**: Sayfanın genel stilini belirler (yazı tipi, hizalama, arka plan rengi vb.).
- **`section`**: Kapsayıcı bölümün stilini belirler (arka plan, padding, kenarlık).
- **`h1`**: Başlık stilini belirler (ortalamak ve alt boşluk).
- **`div`**: İçerik kutucuklarının stilini belirler (kenar boşlukları, padding, kenarlık).
- **`cursor`**: Her bir imleç türü için uygun cursor değeri atanmıştır:
  - `.default`: Varsayılan imleç.
  - `.pointer`: Pointer (el) imleci.
  - `.text`: Metin imleci.
  - `.move`: Hareket imleci.
  - `.not-allowed`: Yasak imleci.
  - `.custom`: Özelleştirilmiş imleç.

Bu düzenlemeler ile birlikte kod, semantik ve stil açısından daha tutarlı hale getirilmiştir. Kodunuzu bu haliyle kullanabilirsiniz.