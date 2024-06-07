# Viewport

Bu bölümde, görünüm alanı ayarlarının HTML ve CSS kullanılarak nasıl yapılandırılacağını ayrıntılı bir örnekle göstereceğiz. Bu örnek, duyarlı tasarım ilkelerini uygulayarak bir web sayfası oluşturmayı amaçlamaktadır. Örnek ayrıca `section` ve `footer` etiketlerini de içerecektir.

## HTML ve CSS ile Görünüm Alanı Ayarları

### HTML Dosyası (index.html)

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Görünüm Alanı Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Görünüm Alanı (Viewport) Ayarları</h1>
    </header>
    <section>
        <article>
            <h2>Görünüm Alanı Nedir?</h2>
            <p>Görünüm alanı, kullanıcının bir web sayfasında görebildiği alanı ifade eder ve cihazın ekran boyutuna göre değişir.</p>
        </article>
        <article>
            <h2>Mobil Görünüm ve Ölçeklendirme</h2>
            <p>Mobil cihazlarda, görünüm alanı ayarları sayfanın cihaz ekranına uygun şekilde görüntülenmesini sağlar.</p>
        </article>
    </section>
    <footer>
        <p>&copy; 2024 Görünüm Alanı Ayarları Örneği</p>
    </footer>
</body>
</html>
```

### CSS Dosyası (styles.css)

```css
/* Genel Stil Ayarları */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Başlık Stilleri */
header {
    background-color: #4CAF50;
    color: white;
    text-align: center;
    padding: 1em 0;
}

/* Bölüm ve Makale Stilleri */
section {
    padding: 2em;
    background-color: #f4f4f4;
}

article {
    margin-bottom: 2em;
    padding: 1em;
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h2 {
    color: #4CAF50;
}

/* Altbilgi Stilleri */
footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1em 0;
    position: fixed;
    width: 100%;
    bottom: 0;
}
```

### Açıklamalar

#### HTML Dosyası

1. **Meta Etiketi ile Görünüm Alanı Ayarları**
    ```html
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    ```
    Bu meta etiketi, sayfanın genişliğini cihazın ekran genişliğine göre ayarlar ve başlangıç ölçeklendirmesini 1.0 olarak belirler.

2. **Temel Yapı**
    - `header`: Sayfanın başlığını içerir.
    - `section`: Sayfanın ana içeriğini iki makale (article) ile birlikte barındırır.
    - `footer`: Sayfanın alt bilgisini içerir.

#### CSS Dosyası

1. **Genel Stil Ayarları**
    ```css
    body {
        font-family: Arial, sans-serif;
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    ```
    Bu ayarlar, sayfanın temel stilini belirler ve tüm elemanların kutu modelini sınır kutusu ile ayarlar.

2. **Başlık Stilleri**
    ```css
    header {
        background-color: #4CAF50;
        color: white;
        text-align: center;
        padding: 1em 0;
    }
    ```
    Başlık bölümünün arka plan rengini, metin rengini ve hizalamasını ayarlar.

3. **Bölüm ve Makale Stilleri**
    ```css
    section {
        padding: 2em;
        background-color: #f4f4f4;
    }

    article {
        margin-bottom: 2em;
        padding: 1em;
        background-color: white;
        border-radius: 8px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }

    h2 {
        color: #4CAF50;
    }
    ```
    Bölüm ve makalelerin stilini, arka plan rengini, kenar boşluklarını ve gölgelerini belirler. Makale başlıklarının rengini ayarlar.

4. **Altbilgi Stilleri**
    ```css
    footer {
        background-color: #333;
        color: white;
        text-align: center;
        padding: 1em 0;
        position: fixed;
        width: 100%;
        bottom: 0;
    }
    ```
    Altbilginin arka plan rengini, metin rengini ve hizalamasını ayarlar. Ayrıca, altbilginin sayfanın altına sabitlenmesini sağlar.

### Sonuç

Bu örnek, görünüm alanı ayarlarının HTML ve CSS kullanılarak nasıl yapılandırılacağını ve duyarlı tasarım ilkelerinin nasıl uygulanacağını göstermektedir. Görünüm alanı ayarları, web sayfalarının farklı cihazlarda tutarlı ve kullanıcı dostu bir şekilde görüntülenmesi için kritik öneme sahiptir. Bu örnekle, görünüm alanı ayarlarının temel ilkeleri ve uygulanabilir yöntemleri hakkında kapsamlı bir anlayış kazanabilirsiniz.