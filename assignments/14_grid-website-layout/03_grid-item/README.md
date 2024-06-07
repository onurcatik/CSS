### CSS Grid Items

Bu bölümde, CSS Grid ile grid itemların yönetimini gösteren kapsamlı bir örnek sunacağız. Bu örnek, HTML ve CSS kodlarını ayrı ayrı ele alacak ve bir web sayfasının nasıl yapılandırılacağını adım adım açıklayacaktır.

#### HTML Kodu
```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Grid Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>CSS Grid Layout</h1>
    </header>
    <section class="grid-container">
        <div class="item header">Header</div>
        <div class="item sidebar">Sidebar</div>
        <div class="item content">Main Content</div>
        <div class="item footer">Footer</div>
    </section>
    <footer>
        <p>&copy; 2024 Web Development Tutorial</p>
    </footer>
</body>
</html>
```

#### CSS Kodu
```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

header, footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1em 0;
}

.grid-container {
    display: grid;
    grid-template-columns: 1fr 3fr;
    grid-template-rows: auto 1fr auto;
    grid-template-areas: 
        "header header"
        "sidebar content"
        "footer footer";
    gap: 10px;
    flex: 1;
}

.item {
    padding: 20px;
    background-color: #f0f0f0;
    border: 1px solid #ccc;
}

.header {
    grid-area: header;
}

.sidebar {
    grid-area: sidebar;
}

.content {
    grid-area: content;
}

.footer {
    grid-area: footer;
}

footer {
    margin-top: auto;
}
```

### Açıklama

#### HTML Yapısı
- **Header:** Web sayfasının üst kısmında yer alır ve genellikle başlık veya logo içerir.
- **Section:** Ana içerik bölümünü kapsayan kısım. Bu bölümde grid layout kullanılarak farklı bölümler (header, sidebar, content, footer) oluşturulmuştur.
- **Footer:** Web sayfasının alt kısmında yer alır ve genellikle telif hakkı bilgileri veya iletişim bilgilerini içerir.

#### CSS Yapısı
- **Genel Stil Ayarları:** Tüm sayfa için temel stil ayarları yapılmıştır (font, margin, padding).
- **Grid Konteyneri:** `grid-container` sınıfı, CSS Grid layout özelliklerini içerir. Bu sınıf içinde grid düzeni tanımlanmıştır:
  - `grid-template-columns`: İki sütunlu bir düzen tanımlanmıştır. İlk sütun 1 birim, ikinci sütun 3 birim genişliğindedir.
  - `grid-template-rows`: Otomatik yükseklikli satırlar ve bir ana içerik satırı tanımlanmıştır.
  - `grid-template-areas`: Grid alanları adlandırılarak düzen belirlenmiştir.
  - `gap`: Grid itemlar arasındaki boşluk belirlenmiştir.
- **Grid Itemlar:** `item` sınıfı, tüm grid itemları için ortak stil özelliklerini içerir. Belirli itemlar için (header, sidebar, content, footer) özel alanlar tanımlanmıştır.
- **Header ve Footer:** Header ve footer bölümleri için stil özellikleri tanımlanmıştır.

Bu örnek, CSS Grid kullanarak bir web sayfasının ana yapısını oluşturmayı göstermektedir. Grid itemların konumlandırılması, grid layout özellikleri kullanılarak belirlenmiştir. Bu teknik, modern web tasarımında esnek ve düzenli bir yapı sağlar.