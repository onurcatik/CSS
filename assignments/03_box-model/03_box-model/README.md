# HTML ve CSS Box Model

Bu örnekte, HTML ve CSS kullanarak kutu modelini nasıl uygulayabileceğinizi gösteren kapsamlı bir örnek sunulmaktadır. Örneğimizde bir web sayfasının farklı bölümleri (başlık, ana içerik ve alt bilgi) tanımlanmış ve her bölümün kutu modeli bileşenleri ayrıntılı bir şekilde belirtilmiştir.

## HTML Dosyası (index.html)

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kutu Modeli Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>Web Sayfası Başlığı</h1>
    </header>
    <main>
        <section>
            <h2>Ana İçerik</h2>
            <p>Bu bölüm, sayfanın ana içeriğini içerir. İçerik, dolgu, kenarlık ve kenar boşluğu ile çevrilidir.</p>
        </section>
        <aside>
            <h2>Kenar Çubuğu</h2>
            <p>Bu bölüm, ek bilgileri ve bağlantıları içerir.</p>
        </aside>
    </main>
    <footer>
        <p>© 2024 Web Sayfası. Tüm hakları saklıdır.</p>
    </footer>
</body>

</html>
```

## CSS Dosyası (styles.css)

```css
/* Genel Stil Ayarları */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Kutu Modeli Ayarları */
header,
main,
footer {
    width: 80%;
    margin: 0 auto;
    padding: 20px;
    border: 2px solid #000;
    margin-bottom: 20px;
}

/* Başlık Stilleri */
header {
    background-color: #f2f2f2;
    text-align: center;
}

/* Ana İçerik Stilleri */
main {
    display: flex;
    justify-content: space-between;
}

/* Ana Bölüm ve Kenar Çubuğu Stilleri */
main section,
main aside {
    width: 45%;
    padding: 15px;
    border: 1px solid #ccc;
}

/* Alt Bilgi Stilleri */
footer {
    background-color: #f2f2f2;
    text-align: center;
}
```

## Açıklamalar ve Detaylar

1. **HTML Dosyası**:
    - HTML yapısında `header`, `main`, ve `footer` etiketleri kullanılarak sayfanın ana bölümleri tanımlanmıştır.
    - `main` etiketi içinde `section` ve `aside` etiketleri ile ana içerik ve kenar çubuğu ayrılmıştır.

2. **CSS Dosyası**:
    - **Genel Stil Ayarları**: 
        - Tüm elemanlar için `box-sizing: border-box` kullanılarak, elemanların genişlik ve yükseklik hesaplamaları kolaylaştırılmıştır. Bu ayar, dolgu ve kenarlıkların elemanın toplam genişlik ve yüksekliğine dahil edilmesini sağlar.
    - **Kutu Modeli Ayarları**:
        - `header`, `main`, ve `footer` elemanlarının genişliği `%80` olarak ayarlanmış ve ortalanmaları için `margin: 0 auto` kullanılmıştır.
        - Bu elemanlara ayrıca `padding: 20px`, `border: 2px solid #000` ve `margin-bottom: 20px` eklenmiştir.
    - **Başlık Stilleri**:
        - `header` elemanına açık gri bir arka plan rengi (`#f2f2f2`) verilmiş ve metin ortalanmıştır (`text-align: center`).
    - **Ana İçerik Stilleri**:
        - `main` elemanı, esnek kutu düzeni (flexbox) kullanılarak düzenlenmiş ve `justify-content: space-between` ile içindeki elemanların eşit şekilde yerleştirilmesi sağlanmıştır.
    - **Ana Bölüm ve Kenar Çubuğu Stilleri**:
        - `section` ve `aside` elemanlarının genişliği `%45` olarak ayarlanmış, içlerine `padding: 15px` eklenmiş ve kenarları `border: 1px solid #ccc` ile belirlenmiştir.
    - **Alt Bilgi Stilleri**:
        - `footer` elemanına, başlıkla aynı olacak şekilde açık gri arka plan rengi verilmiş ve metin ortalanmıştır.

Bu örnek, CSS kutu modelinin nasıl kullanılacağını ve elemanların stilize edilerek sayfa düzeninin nasıl oluşturulacağını göstermektedir. Her bir bölümün stil ayarları, kutu modeli bileşenlerini (içerik, dolgu, kenarlık ve kenar boşluğu) içermekte olup, bu da elemanların sayfa üzerindeki konum ve görünümlerini yönetmede önemlidir.