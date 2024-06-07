# CSS Variable

Bu bölümde, CSS değişkenlerinin HTML ve CSS'de nasıl kullanılacağını gösteren kapsamlı bir örnek oluşturacağız. Örneğimizde, `header` , `section` elementlerini stilize edeceğiz ve bu elementlerin stilizasyonunda CSS değişkenlerini kullanacağız.

## HTML Kodu

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Değişkenleri Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>CSS Değişkenleri ile Web Sayfası</h1>
    </header>
    <section>
        <h2>Örnek Bölüm</h2>
        <p>Bu bölümde, CSS değişkenlerinin nasıl kullanılacağını gösteren bir örnek bulunmaktadır.</p>
    </section>
  
</body>

</html>
```

Bu HTML yapısında, bir `header` , bir `section` bulunmaktadır. Bu yapı, sayfanın üst kısmında bir başlık, ortada bir bölüm ve en altta bir alt bilgi içermektedir.

## CSS Kodu

```css
:root {
    --primary-color: #3498db;
    --secondary-color: #2ecc71;
    --background-color: #ecf0f1;
    --font-color: #2c3e50;
    --header-height: 60px;
    --footer-height: 40px;
    --padding: 20px;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background-color: var(--background-color);
    color: var(--font-color);
    font-family: Arial, sans-serif;
    line-height: 1.6;
}

header {
    background-color: var(--primary-color);
    color: white;
    height: var(--header-height);
    display: flex;
    align-items: center;
    justify-content: center;
    padding: var(--padding);
}

header h1 {
    font-size: 1.5em;
}

section {
    padding: var(--padding);
    background-color: white;
    margin: var(--padding);
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

section h2 {
    color: var(--secondary-color);
    margin-bottom: 10px;
}

section p {
    margin-bottom: 10px;
}


```

### Açıklamalar

* `:root` seçicisinde, sayfamızda kullanacağımız tüm CSS değişkenlerini tanımladık. Bu değişkenler, renkleri, yükseklikleri ve boşlukları içerir.
* Tüm elementlerin varsayılan margin ve padding değerlerini sıfırladık ve `box-sizing: border-box` ayarını kullanarak kutu modelini daha öngörülebilir hale getirdik.
* `body` elementinde, arka plan rengini ve yazı rengini değişkenlerden alarak ayarladık. Ayrıca, genel yazı tipi ailesini ve satır yüksekliğini belirledik.
* `header` elementinde, arka plan rengini `--primary-color` değişkeninden aldık ve yüksekliğini `--header-height` değişkeni ile ayarladık. Başlık ortalanmış ve belirli bir dolgu ile stilize edilmiştir.
* `section` elementinde, içeriği belirli bir dolgu ile ayarladık, arka plan rengini beyaz olarak belirledik ve gölge ekledik. Başlık rengini `--secondary-color` değişkeninden aldık.
  

Bu örnek, CSS değişkenlerinin stil yönetimini nasıl daha esnek ve sürdürülebilir hale getirdiğini göstermektedir. Değişkenler sayesinde, tek bir merkezi konumdan tüm stil değerlerini kontrol edebilir ve gerektiğinde kolayca güncelleyebilirsiniz.
