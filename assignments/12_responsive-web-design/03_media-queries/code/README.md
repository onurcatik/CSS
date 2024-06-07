### Media Queries

Bu bölümde, medya sorgularını kullanarak duyarlı bir web sayfası oluşturacağız. Bu örnekte, bir başlık, içerik bölümü ve alt bilgi (footer) bulunan basit bir sayfa oluşturacağız. HTML ve CSS kodlarını ayrı dosyalar halinde tutacağız ve medya sorgularının bu yapıyı nasıl etkilediğini inceleyeceğiz.

#### HTML Dosyası (index.html)

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Duyarlı Web Sayfası</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Başlık</h1>
    </header>
    <section>
        <p>Bu, medya sorgularını kullanarak duyarlı hale getirilmiş bir web sayfasıdır.</p>
        <img src="https://via.placeholder.com/800x400" alt="Örnek Görsel">
    </section>
    <footer>
        <p>Bu, alt bilgi bölümüdür.</p>
    </footer>
</body>
</html>
```

#### CSS Dosyası (styles.css)

```css
/* Temel Stil Kuralları */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header, section, footer {
    padding: 20px;
    text-align: center;
}

header {
    background-color: #4CAF50;
    color: white;
}

section {
    background-color: #f2f2f2;
    color: #333;
}

footer {
    background-color: #333;
    color: white;
}

/* Görsellerin Duyarlı Hale Getirilmesi */
img {
    max-width: 100%;
    height: auto;
}

/* Medya Sorguları */
@media only screen and (max-width: 768px) {
    header, section, footer {
        padding: 10px;
    }

    section p {
        font-size: 14px;
    }
}

@media only screen and (max-width: 480px) {
    header h1 {
        font-size: 18px;
    }

    section p {
        font-size: 12px;
    }

    footer p {
        font-size: 12px;
    }
}
```

### Açıklama

Bu örnekte, HTML ve CSS kodlarımızı ayrı dosyalara ayırdık ve medya sorgularını kullanarak sayfamızı duyarlı hale getirdik. 

#### HTML Dosyasının İncelenmesi

HTML dosyasında, temel bir yapı oluşturduk. Başlık (`header`), içerik bölümü (`section`) ve alt bilgi (`footer`) bölümlerini ekledik. Görsel ve metin içeriklerini de bu bölümlere yerleştirdik.

#### CSS Dosyasının İncelenmesi

CSS dosyasında, önce temel stil kurallarını tanımladık:

- `body`: Tüm sayfa için genel stil kuralları.
- `header`, `section`, `footer`: Bu bölümler için ortak stil kuralları.

Daha sonra, görselleri duyarlı hale getirmek için `img` etiketi için bir stil kuralı ekledik. `max-width: 100%;` ve `height: auto;` ayarları ile görsellerin ekran boyutuna göre ölçeklenmesini sağladık.

#### Medya Sorguları

Medya sorgularını kullanarak, farklı ekran boyutlarına göre stil kurallarını uyarladık:

1. **768 piksel genişliğe kadar olan ekranlar için**:
    - `header`, `section`, `footer` bölümlerinin iç dolgusunu (`padding`) küçülttük.
    - `section p` elementi için yazı tipini küçülttük.

2. **480 piksel genişliğe kadar olan ekranlar için**:
    - `header h1`, `section p` ve `footer p` elementlerinin yazı tiplerini daha da küçülttük.

Bu medya sorguları sayesinde, sayfamızın farklı ekran boyutlarında kullanıcı dostu ve okunabilir olmasını sağladık.

### Sonuç

Bu örnek, medya sorgularının nasıl kullanılacağını ve web sayfalarının nasıl duyarlı hale getirileceğini göstermektedir. Medya sorguları, farklı cihazlarda ve ekran boyutlarında tutarlı bir kullanıcı deneyimi sağlamak için kritik bir araçtır. Bu doküman ve örnek, medya sorgularını kullanarak profesyonel ve kullanıcı dostu web siteleri geliştirme konusunda kapsamlı bir rehber sunar.