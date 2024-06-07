# CSS Pseudo-Element

Bu bölümde, CSS Pseudo-Elementlerin nasıl kullanılacağını gösteren kapsamlı bir örnek sunacağız. HTML ve CSS kodlarını ayrı dosyalarda tutarak daha düzenli ve anlaşılır hale getireceğiz. Örneğimizde `::first-letter` , `::before` , `::after` , ve `::selection` pseudo-elementlerini kullanacağız. Ayrıca, `section` ve `footer` etiketlerini de dahil edeceğiz.

## HTML Kodu

Öncelikle, HTML dosyamızı oluşturalım. Bu dosyada bir başlık, iki bölüm ( `section` ) ve bir alt bilgi ( `footer` ) yer alacak.

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>CSS Pseudo-Elementler Örneği</title>
</head>

<body>
    <header>
        <h1>CSS Pseudo-Elementler</h1>
    </header>
    <section class="intro">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. <span class="highlight">Curabitur nec diam nec lorem</span> tincidunt facilisis.</p>
    </section>
    <section class="content">
        <p>Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae;</p>
    </section>
    <footer>
        <p>&copy; 2024 Web Geliştirme Eğitimleri</p>
    </footer>
</body>

</html>
```

## CSS Kodu

Şimdi, CSS dosyamızı oluşturalım. Bu dosyada pseudo-elementlerin nasıl stilize edileceğini belirteceğiz.

```css
/* Genel stil ayarları */
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 0;
}

/* Başlık stili */
header h1 {
    background-color: #4CAF50;
    color: white;
    padding: 10px;
    text-align: center;
}

/* Paragraf ilk harfi stili */
p::first-letter {
    font-size: 200%;
    font-weight: bold;
    color: #333;
}

/* Before pseudo-elementi */
.intro::before {
    content: "Giriş: ";
    font-weight: bold;
    color: red;
}

/* After pseudo-elementi */
.content::after {
    content: " - Bu önemli bir noktadır.";
    font-weight: bold;
    color: blue;
}

/* Seçilen metin stili */
::selection {
    background: yellow;
    color: black;
}

/* Footer stili */
footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px;
    position: fixed;
    width: 100%;
    bottom: 0;
}
```

## Detaylı Açıklama

### HTML Dosyası

HTML dosyamızda, temel yapıyı oluşturduk. Bu yapı, `header` , iki `section` içermektedir. `header` kısmında sayfa başlığı bulunmaktadır. İki `section` kısmı, örnek içeriklerimizi barındırmaktadır. 

### CSS Dosyası

CSS dosyamızda, çeşitli pseudo-elementleri kullanarak sayfamızı stilize ettik.

1. **Genel Stil Ayarları:** Tüm sayfa için temel yazı tipi, satır yüksekliği, kenar boşlukları ve dolguları ayarladık.

2. **Başlık Stili:** `header` kısmındaki başlık (`h1`) için arka plan rengi, metin rengi ve hizalama ayarlarını yaptık.

3. **`::first-letter` Pseudo-Elementi:** Paragrafların ilk harfini büyük, kalın ve koyu gri renkte göstermek için kullandık.

4. **`::before` Pseudo-Elementi:** `.intro` sınıfına sahip `section` öğesinin içeriğinden önce "Giriş: " metnini eklemek için kullandık. Bu metni kırmızı ve kalın yaptık.

5. **`::after` Pseudo-Elementi:** `.content` sınıfına sahip `section` öğesinin içeriğinden sonra " - Bu önemli bir noktadır." metnini eklemek için kullandık. Bu metni mavi ve kalın yaptık.

6. **`::selection` Pseudo-Elementi:** Kullanıcı tarafından seçilen metnin arka planını sarı, metin rengini ise siyah yaparak stilize ettik.

## Sonuç

Bu kapsamlı örnek, CSS Pseudo-Elementlerin nasıl kullanıldığını ve stilize edildiğini göstermektedir. Pseudo-Elementler, web sayfalarınızı daha estetik ve fonksiyonel hale getirmek için güçlü araçlardır. Bu örnekte, `::first-letter` , `::before` , `::after` , ve `::selection` pseudo-elementlerini kullanarak farklı içerik bölümlerini nasıl stilize edebileceğinizi öğrendiniz. Bu bilgileri, kendi projelerinizde de uygulayarak kullanıcı deneyimini zenginleştirebilirsiniz.
