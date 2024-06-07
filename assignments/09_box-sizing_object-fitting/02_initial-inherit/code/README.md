### Örnek: HTML, CSS `initial` and`inherit` 

Bu bölümde, `initial` ve `inherit` anahtar kelimelerinin kullanımını içeren kapsamlı bir örnek sunacağız. HTML ve CSS dosyalarını ayrı tutarak, bu anahtar kelimelerin nasıl uygulanacağını ve bunların etkilerini açıklayacağız. Ek olarak, `<section>` etiketini kullanarak, bu anahtar kelimelerin nasıl çalıştığını göstereceğiz.

#### HTML Kodu ( `index.html` )

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS initial ve inherit Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>CSS initial ve inherit Örneği</h1>
    </header>
    <section>
        <div class="parent">
            <p class="child-inherit">Bu paragraf, ebeveynin rengini miras alır.</p>
            <p class="child-initial">Bu paragraf, başlangıç değerine sıfırlanır.</p>
        </div>
    </section>
</body>

</html>
```

#### CSS Kodu ( `styles.css` )

```css
/* Genel stil ayarları */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

/* Header stili */
header {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1em 0;
}

/* Section stili */
section {
    padding: 2em;
    background-color: #f4f4f4;
}

/* Ebeveyn div stili */
.parent {
    color: green;
    /* Ebeveynin rengi */
    border: 2px solid green;
    padding: 1em;
}

/* inherit anahtar kelimesi kullanımı */
.child-inherit {
    color: inherit;
    /* Ebeveynin rengini miras alır */
}

/* initial anahtar kelimesi kullanımı */
.child-initial {
    color: initial;
    /* Varsayılan değere sıfırlanır */
}
```

#### Açıklamalar

1. **HTML Dosyası:** 
   - `<header>` , `<section>` etiketlerini kullanarak sayfanın yapısını belirledik.
   - `<div class="parent">` içinde iki paragraf oluşturduk: biri `inherit` anahtar kelimesini, diğeri `initial` anahtar kelimesini kullanır.

2. **CSS Dosyası:** 
   - Genel stil ayarları, yazı tipini ve kenar boşluklarını belirler.
   - `<header>` , `<section>` , ve `<footer>` için temel stiller uygulanır.
   - `.parent` sınıfı ile ebeveyn divin stilini belirledik, bu stil tüm alt elemanlar tarafından miras alınabilir.
   - `.child-inherit` sınıfı, `inherit` anahtar kelimesi ile ebeveynin rengini miras alır.
   - `.child-initial` sınıfı, `initial` anahtar kelimesi ile rengi varsayılan değere sıfırlar.

#### Detaylı Açıklamalar

* **`inherit` Anahtar Kelimesi:** 
`.child-inherit` sınıfındaki paragraf, `.parent` sınıfındaki divin rengini miras alır ve yeşil olur. Bu, stil tutarlılığını sağlamak için kullanışlıdır ve alt elemanların ebeveyn stillerini miras almasını sağlar.

* **`initial` Anahtar Kelimesi:** 
`.child-initial` sınıfındaki paragraf, tarayıcının varsayılan rengini kullanır. Genellikle bu, siyah veya kullanıcı tarafından belirlenen bir varsayılan renk olabilir. Bu anahtar kelime, belirli bir stil özelliğini sıfırlamak ve tarayıcı varsayılanlarına dönmek için kullanılır.

Bu örnek, `initial` ve `inherit` anahtar kelimelerinin CSS'de nasıl kullanılacağını ve etkilerini göstermektedir. Bu anahtar kelimeler, stil yönetiminde esneklik ve tutarlılık sağlar, böylece web sayfalarının görünümünü ve hissini daha kontrollü bir şekilde yönetebilirsiniz.
