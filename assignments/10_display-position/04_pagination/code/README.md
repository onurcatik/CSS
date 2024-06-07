## CSS Pagination 

Bir web siteniz çok sayıda sayfaya sahipse, her sayfaya bir çeşit sayfa numaralandırma (pagination) eklemek isteyebilirsiniz. Sayfa numaralandırma, kullanıcıların içeriği daha kolay gezinebilmesi için gereklidir ve kullanıcı deneyimini büyük ölçüde artırabilir. Bu eğitimde, CSS kullanarak nasıl etkili bir sayfa numaralandırma oluşturabileceğinizi öğreneceksiniz.

### 1. Sayfa Numaralandırma Nedir?

Sayfa numaralandırma, uzun içeriği daha yönetilebilir parçalara bölmek için kullanılır. Örneğin, bir blogda birden fazla makale olduğunda, kullanıcıların sayfalar arasında gezinmesine olanak tanır. Genellikle, sayfa numaraları, ileri ve geri oklar veya "ilk" ve "son" gibi bağlantılar içerir.

### 2. HTML Yapısı

Öncelikle, temel bir HTML yapısı oluşturmalıyız. Sayfa numaralandırma için genellikle bir liste öğesi kullanılır. Ayrıca, eğitimde `<section>` ve `<footer>` etiketlerini de kullanarak daha anlamlı bir yapı oluşturacağız:

#### HTML Dosyası (`index.html`)

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Sayfa Numaralandırma Örneği</title>
</head>
<body>

<header>
    <h1>Sayfa Numaralandırma (Pagination) Örneği</h1>
</header>

<section>
    <h2>Makale Başlığı</h2>
    <p>Bu bölüm, makalenin içeriğini içerir. Burada makale ile ilgili bilgileri bulabilirsiniz. Uzun bir içerik olduğunda, sayfa numaralandırma kullanarak kullanıcıların içeriği daha kolay gezmesine olanak tanıyabilirsiniz.</p>
</section>

<section class="pagination">
    <a href="#">&laquo;</a>
    <a href="#">1</a>
    <a href="#">2</a>
    <a href="#">3</a>
    <a href="#">4</a>
    <a href="#">5</a>
    <a href="#">&raquo;</a>
</section>

<footer>
    <p>&copy; 2024 Tüm Hakları Saklıdır.</p>
</footer>

</body>
</html>
```

### 3. CSS İle Stil Verme

Şimdi, bu HTML yapısını CSS ile nasıl stillendirebileceğimize bakalım. CSS kodlarını ayrı bir dosyada tutarak daha temiz bir yapı oluşturabiliriz.

#### CSS Dosyası (`styles.css`)

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f9f9f9;
}

header {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1em 0;
}

section {
    margin: 20px;
    padding: 20px;
    background-color: white;
    border: 1px solid #ddd;
    border-radius: 5px;
}

.pagination {
    display: inline-block;
    text-align: center;
    width: 100%;
    margin-top: 20px;
}

.pagination a {
    color: black;
    float: none; /* List item is centered instead of floating left */
    display: inline-block;
    padding: 8px 16px;
    text-decoration: none;
    transition: background-color .3s;
}

.pagination a.active {
    background-color: #4CAF50;
    color: white;
    border-radius: 5px;
}

.pagination a:hover:not(.active) {
    background-color: #ddd;
    border-radius: 5px;
}

@media screen and (max-width: 600px) {
    .pagination a {
        padding: 8px 12px;
        font-size: 12px;
    }
}
```

### 4. Örnek Uygulama Açıklaması

Yukarıda verdiğimiz HTML ve CSS kodları, basit ama etkili bir sayfa numaralandırma yapısı oluşturur. Bu yapı, kullanıcıların sayfalar arasında kolayca gezinmesini sağlar. 

- **HTML Yapısı**:
  - `header`: Sayfa başlığını içerir.
  - `section`: İçeriği ve sayfa numaralandırmayı barındırır.
  

- **CSS Stilleri**:
  - Genel stil özellikleri (yazı tipi, arka plan rengi vb.) `body` ve diğer ana yapılar için belirlenmiştir.
  - `.pagination` sınıfı, sayfa numaralandırmanın stilini tanımlar.
  - `a.active` sınıfı, aktif sayfa numarasını belirler ve `.pagination a:hover:not(.active)` sınıfı, fareyle üzerine gelindiğinde uygulanacak stili tanımlar.
  - Medya sorguları ile, sayfa numaralandırma küçük ekranlar için optimize edilmiştir.

### Sonuç

CSS ile sayfa numaralandırma oluşturmak, kullanıcı deneyimini artırmak için oldukça etkili bir yöntemdir. Bu eğitimde, temel HTML yapısını ve CSS stillerini öğrendiniz. Kendi projelerinizde bu bilgileri kullanarak daha etkili ve kullanıcı dostu web sayfaları oluşturabilirsiniz.

Bu eğitimde ele alınan konular, CSS'nin gücünü ve esnekliğini vurgulamakta olup, modern web geliştirme süreçlerinde sıkça karşılaşılan gereksinimlere yanıt vermektedir.

