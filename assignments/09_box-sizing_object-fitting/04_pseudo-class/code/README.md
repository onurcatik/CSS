## CSS Pseudo-Class 

Bu bölümde, HTML ve CSS dosyalarını ayrı tutarak CSS pseudo-sınıflarının nasıl kullanıldığını gösteren kapsamlı bir örnek sunacağız. Örneğimizde, `header` , `section` , `footer` elemanlarını kullanarak temel bir sayfa yapısı oluşturacağız ve bu elemanlara pseudo-sınıflar uygulayacağız.

### HTML Kodu

Aşağıdaki HTML dosyasını `index.html` olarak kaydedin:

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Pseudo-sınıfları Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>CSS Pseudo-sınıfları</h1>
        <nav>
            <ul>
                <li><a href="#">Anasayfa</a></li>
                <li><a href="#">Hakkında</a></li>
                <li><a href="#">İletişim</a></li>
            </ul>
        </nav>
    </header>

    <section>
        <h2>Örnek Bölüm</h2>
        <p class="intro">Bu bölümde CSS pseudo-sınıflarını nasıl kullanabileceğinizi göstereceğiz.</p>
        <p>İşte bazı örnekler:</p>
        <ul>
            <li>Birinci öğe</li>
            <li>İkinci öğe</li>
            <li>Üçüncü öğe</li>
        </ul>
        <form>
            <label for="name">Adınız:</label>
            <input type="text" id="name" name="name">
            <br>
            <label for="subscribe">Abone Ol:</label>
            <input type="checkbox" id="subscribe" name="subscribe">
        </form>
    </section>

    <footer>
        <p>&copy; 2024 CSS Pseudo-sınıfları Örneği. Tüm hakları saklıdır.</p>
    </footer>
</body>

</html>
```

### CSS Kodu

Aşağıdaki CSS dosyasını `styles.css` olarak kaydedin:

```css
/* Genel Stil Ayarları */
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 0;
}

/* Header Stili */
header {
    background: #333;
    color: #fff;
    padding: 10px 0;
    text-align: center;
}

header h1 {
    margin: 0;
}

nav ul {
    list-style: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin: 0 10px;
}

nav ul li a {
    color: #fff;
    text-decoration: none;
}

nav ul li a:link {
    color: #ffcc00;
}

nav ul li a:visited {
    color: #cc9900;
}

nav ul li a:hover {
    color: #ff6600;
}

nav ul li a:active {
    color: #ff3300;
}

/* Section Stili */
section {
    padding: 20px;
}

section h2 {
    color: #333;
}

.intro {
    font-style: italic;
    color: #555;
}

/* Liste ve Form Elemanları */
ul li:first-child {
    color: red;
}

ul li:last-child {
    color: blue;
}

ul li:nth-child(2) {
    color: green;
}

form input:focus {
    border-color: blue;
}

form input:enabled {
    background-color: #f9f9f9;
}

form input:disabled {
    background-color: #e9e9e9;
}

form input:checked {
    background-color: #d9d9d9;
}

/* Footer Stili */
footer {
    background: #333;
    color: #fff;
    text-align: center;
    padding: 10px 0;
    position: fixed;
    width: 100%;
    bottom: 0;
}
```

### Açıklamalar

#### HTML Yapısı

* **Header** : `header` elemanı, sayfanın başlık kısmını içerir. Burada bir başlık (`h1`) ve bir navigasyon menüsü (`nav`) bulunur.
* **Section** : `section` elemanı, sayfanın ana içeriğini içerir. Bu bölümde başlık (`h2`), paragraflar (`p`), liste (`ul` ve `li`) ve bir form bulunur.
* **Footer** : `footer` elemanı, sayfanın alt bilgi kısmını içerir.

#### CSS Stilleri

* **Genel Stil Ayarları** : `body` elemanı için genel stil ayarları yapılmıştır.
* **Header Stili** : `header` elemanı için arka plan rengi ve metin rengi ayarlanmıştır. `nav` içindeki `ul` ve `li` elemanlarının stilleri belirlenmiştir. Bağlantılar (`a` elemanları) için dört farklı pseudo-sınıf (`:link`,  `:visited`,  `:hover`,  `:active`) kullanılmıştır.
* **Section Stili** : `section` elemanı için padding eklenmiştir. `h2` başlıkları için renk ayarı yapılmıştır. `intro` sınıfına sahip paragraflar için stil ayarlanmıştır.
* **Liste ve Form Elemanları** : Liste (`ul` ve `li` elemanları) ve form elemanları için pseudo-sınıflar kullanılarak stil ayarları yapılmıştır. `:first-child`,  `:last-child`,  `:nth-child(n)` gibi yapısal pseudo-sınıflar ve `:focus`,  `:enabled`,  `:disabled`,  `:checked` gibi dinamik pseudo-sınıflar kullanılmıştır.
* **Footer Stili** : `footer` elemanı için arka plan rengi, metin rengi ve konumlandırma ayarları yapılmıştır.

Bu örnekle, CSS pseudo-sınıflarının farklı kullanım alanlarını ve stillendirme seçeneklerini kapsamlı bir şekilde öğrenmiş oldunuz. Bu bilgiler, web projelerinizde dinamik ve kullanıcı dostu arayüzler oluşturmanıza yardımcı olacaktır.
