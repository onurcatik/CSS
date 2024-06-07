### HTML and CSS Syntax

Aşağıda, CSS sözdizimini doğru ve etkili bir şekilde kullanarak basit bir web sayfası oluşturacağız. HTML ve CSS dosyalarını ayrı tutacağız. 

#### HTML (index.html)

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Örnek CSS Uygulaması</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>Web Geliştirme</h1>
        <nav>
            <ul>
                <li><a href="#home">Ana Sayfa</a></li>
                <li><a href="#about">Hakkında</a></li>
                <li><a href="#contact">İletişim</a></li>
            </ul>
        </nav>
    </header>
    <section id="home">
        <h2>Ana Sayfa</h2>
        <p class="intro">Bu, web geliştirme hakkında bir örnek web sayfasıdır.</p>
    </section>
    <section id="about">
        <h2>Hakkında</h2>
        <p>Bu bölüm, projenin detaylarını içerir.</p>
    </section>
    <section id="contact">
        <h2>İletişim</h2>
        <p>Bize <a href="mailto:info@ornek.com">info@ornek.com</a> adresinden ulaşabilirsiniz.</p>
    </section>
    <footer>
        <p>&copy; 2024 Web Geliştirme. Tüm hakları saklıdır.</p>
    </footer>
</body>

</html>
```

#### CSS (styles.css)

```css
/* Evrensel Seçici */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Tür Seçici */
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    background-color: #f4f4f4;
    padding: 20px;
}

/* ID Seçici */
#home,
#about,
#contact {
    margin-bottom: 20px;
    padding: 20px;
    background: #fff;
    border: 1px solid #ddd;
    border-radius: 5px;
}

/* Sınıf Seçici */
.intro {
    font-size: 1.2em;
    color: #333;
}

/* Tür ve Sınıf Seçici */
p.intro {
    margin-top: 10px;
}

/* Etiket Seçiciler */
header {
    background: #333;
    color: #fff;
    padding: 10px 0;
}

header h1 {
    text-align: center;
}

header nav ul {
    list-style: none;
    display: flex;
    justify-content: center;
}

header nav ul li {
    margin: 0 10px;
}

header nav ul li a {
    color: #fff;
    text-decoration: none;
}

header nav ul li a:hover {
    text-decoration: underline;
}

/* Altbilgi Seçici */
footer {
    text-align: center;
    margin-top: 20px;
}
```

### Açıklamalar:

1. **Evrensel Seçici** : Tüm öğeler için varsayılan marj ve dolguyu sıfırlayıp,  `box-sizing` özelliğini `border-box` olarak ayarlayarak, kutu modelinin daha öngörülebilir olmasını sağlar.
2. **Tür Seçici** : `body` öğesi için temel stil tanımlar. Bu, sayfanın genel font ailesini, satır yüksekliğini ve arka plan rengini ayarlar.
3. **ID Seçici** : Belirli bölümlerin (`#home`, `#about`, `#contact`) stilini belirler. Her bölüm için kenar boşlukları, dolgu, arka plan rengi ve sınır tanımlanmıştır.
4. **Sınıf Seçici** : `.intro` sınıfı, belirli paragraflar için font boyutu ve renk ayarlarını içerir.
5. **Tür ve Sınıf Seçici** : `p.intro`, yalnızca `p` etiketleri içinde `.intro` sınıfına sahip olanları hedefler ve üst marjı ayarlar.
6. **Etiket Seçiciler** : `header` ve `footer` etiketleri için stil tanımlar. Başlık içindeki `nav` öğesi için stil, menünün yatay olarak hizalanmasını sağlar.
7. **Altbilgi Seçici** : `footer` etiketine merkezde hizalama ve üst marj ekler.

Bu örnek, temel CSS sözdizimini ve seçici türlerini kullanarak profesyonel ve tutarlı bir web sayfası oluşturmayı gösterir. Her bir stil tanımının sayfanın görünümüne ve yapısına nasıl katkıda bulunduğunu ayrıntılı bir şekilde ele aldık.
