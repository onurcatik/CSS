# CSS Resize Property 

## Giriş

Bu belge, CSS `resize` özelliği hakkında kapsamlı ve detaylı bir rehber sunar. Rehberde `resize` özelliğinin ne olduğu, nasıl kullanıldığı ve kullanım örnekleri üzerinde durulacaktır. Örnekler, HTML ve CSS dosyaları ile ayrı ayrı sunulacaktır. Ayrıca bir web sayfası oluşturularak bu özellik üzerine odaklanılacaktır.

## Genel Bakış

`resize` özelliği, bir öğenin kullanıcı tarafından yeniden boyutlandırılabilir olup olmadığını ve nasıl boyutlandırılacağını belirler. Bu özellik, özellikle metin alanları ve div öğeleri gibi öğelerde kullanışlıdır.

### Uygulama Koşulları

* `resize` özelliği, yalnızca `overflow` özelliği "scroll", "auto" veya "hidden" olarak ayarlandığında geçerlidir. `overflow` özelliği "visible" olarak ayarlandığında `resize` özelliği çalışmaz.
* `resize` özelliği, satır içi (inline) öğelerde uygulanamaz.

### Değerler

* `none`: Öğenin yeniden boyutlandırılamayacağını belirtir.
* `both`: Öğenin hem yatay hem de dikey olarak yeniden boyutlandırılabileceğini belirtir.
* `horizontal`: Öğenin yalnızca yatay olarak yeniden boyutlandırılabileceğini belirtir.
* `vertical`: Öğenin yalnızca dikey olarak yeniden boyutlandırılabileceğini belirtir.

### HTML ve CSS ile Örnek Uygulama

Aşağıda, `resize` özelliğinin nasıl kullanılacağını gösteren bir örnek bulunmaktadır. Bu örnek, bir web sayfası oluşturacak ve bu sayfada `resize` özelliğini uygulayacaktır.

#### HTML Kodu (index.html)

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Resize Property Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>CSS Resize Property Örneği</h1>
    </header>
    <section>
        <h2>Yeniden Boyutlandırılabilir Alanlar</h2>
        <div class="resizable both">
            Bu div hem yatay hem de dikey olarak yeniden boyutlandırılabilir.
        </div>
        <div class="resizable horizontal">
            Bu div sadece yatay olarak yeniden boyutlandırılabilir.
        </div>
        <div class="resizable vertical">
            Bu div sadece dikey olarak yeniden boyutlandırılabilir.
        </div>
    </section>
    <footer>
        <p>© 2024 Web Geliştirme Eğitimi</p>
    </footer>
</body>

</html>
```

#### CSS Kodu (styles.css)

```css
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

header,
footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1rem;
}

section {
    padding: 1rem;
}

h1,
h2 {
    margin: 0 0 1rem 0;
}

.resizable {
    padding: 1rem;
    border: 1px solid #333;
    margin-bottom: 1rem;
    overflow: auto;
    width: 300px;
    height: 150px;
}

.both {
    resize: both;
}

.horizontal {
    resize: horizontal;
}

.vertical {
    resize: vertical;
}
```

### Örnek Açıklaması

* **Header ve Footer** : Sayfanın başında ve sonunda yer alan `header` ve `footer` öğeleri, sabit içerik alanlarını temsil eder. Bu alanlar, genellikle sayfanın başlığı ve alt bilgi (footer) içerir.
* **Section** : Bu bölümde, yeniden boyutlandırılabilir alanlar yer alır. Her `div` öğesi,  `resizable` sınıfını kullanarak stil alır ve belirli `resize` değerleri ile farklı boyutlandırma seçenekleri sunar.
* **CSS Özellikleri** :
  + `resize: both;`: Öğenin hem yatay hem de dikey olarak yeniden boyutlandırılmasına izin verir.
  + `resize: horizontal;`: Öğenin yalnızca yatay olarak yeniden boyutlandırılmasına izin verir.
  + `resize: vertical;`: Öğenin yalnızca dikey olarak yeniden boyutlandırılmasına izin verir.
  + `overflow: auto;`: `resize` özelliğinin çalışması için gerekli olan `overflow` ayarını yapar.

Bu örnek, `resize` özelliğinin nasıl kullanılacağını ve farklı değerlerin nasıl etkili olduğunu gösterir. HTML ve CSS kodları ayrı dosyalarda saklanarak, kodun daha düzenli ve yönetilebilir olmasını sağlar. Bu rehberi kullanarak, web projelerinizde `resize` özelliğini etkili bir şekilde uygulayabilirsiniz.
