### CSS Grid Website-Layout

#### HTML File (index.html)

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Web Sitesi Düzeni</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="header">
        <h1>Web Sitesi Adı</h1>
        <p>Web Sitesi Sloganı</p>
    </div>

    <div class="navbar">
        <a href="#home">Ana Sayfa</a>
        <a href="#news">Haberler</a>
        <a href="#contact">İletişim</a>
        <a href="#about">Hakkında</a>
    </div>

    <div class="row">
        <div class="side">
            <h2>Yan Menü</h2>
            <p>Yan menü içeriği.</p>
        </div>
        <div class="main">
            <h2>Ana İçerik</h2>
            <p>Ana içerik bölümü.</p>
        </div>
    </div>

    <div class="footer">
        <p>Telif Hakkı © 2024 Tüm Hakları Saklıdır.</p>
    </div>
</body>
</html>
```

#### CSS File (styles.css)

```css
/* Genel Stil Ayarları */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Başlık (Header) Stilleri */
.header {
    background-color: #f1f1f1;
    padding: 20px;
    text-align: center;
    font-size: 35px;
}

/* Navigasyon Çubuğu (Navbar) Stilleri */
.navbar {
    overflow: hidden;
    background-color: #333;
}

.navbar a {
    float: left;
    display: block;
    color: #f2f2f2;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
}

.navbar a:hover {
    background-color: #ddd;
    color: black;
}

/* İçerik ve Yan Menü (Content/Side Menu) Stilleri */
.row {
    display: flex;
}

.side {
    flex: 30%;
    background-color: #f1f1f1;
    padding: 20px;
}

.main {
    flex: 70%;
    background-color: #ffffff;
    padding: 20px;
}

/* Altbilgi (Footer) Stilleri */
.footer {
    background-color: #f1f1f1;
    padding: 10px;
    text-align: center;
}
```

### Explanation

#### HTML Yapısı

1. **HTML Doctype ve Temel Yapı**:
   - `<!DOCTYPE html>`: HTML5 doküman tipini belirtir.
   - `<html lang="tr">`: HTML dokümanının dilini belirtir. Bu örnekte Türkçe olarak ayarlandı.
   - `<head>`: Meta bilgiler ve stil dosyasının bağlandığı bölüm.
   - `<link rel="stylesheet" href="styles.css">`: Harici CSS dosyasını bağlar.

2. **Başlık (Header)**:
   - `<div class="header">`: Başlık bölümünü tanımlar.
   - `<h1>` ve `<p>` etiketleri: Başlık ve slogan metinlerini içerir.

3. **Navigasyon Çubuğu (Navbar)**:
   - `<div class="navbar">`: Navigasyon çubuğunu tanımlar.
   - `<a href="#">`: Navigasyon bağlantıları.

4. **İçerik ve Yan Menü (Content/Side Menu)**:
   - `<div class="row">`: Flexbox kullanarak içerik ve yan menü düzenini tanımlar.
   - `<div class="side">` ve `<div class="main">`: Yan menü ve ana içerik bölümleri.

5. **Altbilgi (Footer)**:
   - `<div class="footer">`: Altbilgi bölümünü tanımlar.

#### CSS Stilleri

1. **Genel Stil Ayarları**:
   - `body`: Tüm sayfanın genel stil ayarları.
   - `box-sizing: border-box`: Elemanların toplam genişliğini ve yüksekliğini padding ve border dahil ederek hesaplar.

2. **Başlık (Header) Stilleri**:
   - `background-color`: Arka plan rengini ayarlar.
   - `padding`, `text-align`, `font-size`: İç boşluk, metin hizalama ve yazı boyutu ayarları.

3. **Navigasyon Çubuğu (Navbar) Stilleri**:
   - `overflow: hidden`: Taşan içeriği gizler.
   - `float: left`: Bağlantıları sola hizalar.
   - `display: block`, `color`, `text-align`, `padding`, `text-decoration`: Bağlantıların görünümü ve hizalaması.

4. **İçerik ve Yan Menü (Content/Side Menu) Stilleri**:
   - `display: flex`: İçerik ve yan menü için flexbox düzeni kullanır.
   - `flex`: Alanı yüzde oranında ayarlar.
   - `padding`: İç boşluk ayarları.

5. **Altbilgi (Footer) Stilleri**:
   - `background-color`: Arka plan rengini ayarlar.
   - `padding`, `text-align`: İç boşluk ve metin hizalama ayarları.

### Sonuç

Bu örnek, CSS kullanarak bir web sitesi düzeni oluşturmanın temel adımlarını göstermektedir. HTML ve CSS dosyalarını ayrı tutarak, kodun daha düzenli ve yönetilebilir olmasını sağladık. Bu düzen, modern web tasarım teknikleri ve standartlarına uygun olarak hazırlanmıştır. Bu bilgiler, web geliştirme sürecinde kullanıcı dostu ve estetik bir web sitesi oluşturmak için gereklidir.