# CSS  Pagination

Bir web siteniz çok sayıda sayfaya sahipse, her sayfaya bir çeşit sayfa numaralandırma (pagination) eklemek isteyebilirsiniz. Sayfa numaralandırma, kullanıcıların içeriği daha kolay gezinebilmesi için gereklidir ve kullanıcı deneyimini büyük ölçüde artırabilir. Bu eğitimde, CSS kullanarak nasıl etkili bir sayfa numaralandırma oluşturabileceğinizi öğreneceksiniz.

## 1. Sayfa Numaralandırma Nedir?

Sayfa numaralandırma, uzun içeriği daha yönetilebilir parçalara bölmek için kullanılır. Örneğin, bir blogda birden fazla makale olduğunda, kullanıcıların sayfalar arasında gezinmesine olanak tanır. Genellikle, sayfa numaraları, ileri ve geri oklar veya "ilk" ve "son" gibi bağlantılar içerir.

## 2. HTML Yapısı

Öncelikle, temel bir HTML yapısı oluşturmalıyız. Sayfa numaralandırma için genellikle bir liste öğesi kullanılır:

```html
<div class="pagination">
    <a href="#">&laquo;</a>
    <a href="#">1</a>
    <a href="#">2</a>
    <a href="#">3</a>
    <a href="#">4</a>
    <a href="#">5</a>
    <a href="#">&raquo;</a>
</div>
```

Bu yapıda, `&laquo;` ve `&raquo;` karakterleri sırasıyla geri ve ileri gitme simgelerini temsil eder.

## 3. CSS İle Stil Verme

Şimdi, bu HTML yapısını CSS ile nasıl stillendirebileceğimize bakalım:

```css
.pagination {
    display: inline-block;
}

.pagination a {
    color: black;
    float: left;
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
```

Bu CSS kodu, sayfa numaralandırma bağlantılarını yatay olarak hizalar ve fareyle üzerine gelindiğinde veya aktif olduğunda farklı stiller uygular. `transition` özelliği, arka plan renginin yumuşak bir şekilde değişmesini sağlar.

## 4. Örnek Uygulama

Aşağıda, yukarıdaki HTML ve CSS kodlarını birleştirerek oluşturulmuş tam bir örnek bulunmaktadır:

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
.pagination {
    display: inline-block;
}

.pagination a {
    color: black;
    float: left;
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
</style>
</head>
<body>

<h2>CSS Sayfa Numaralandırma Örneği</h2>

<div class="pagination">
  <a href="#">&laquo;</a>
  <a href="#">1</a>
  <a class="active" href="#">2</a>
  <a href="#">3</a>
  <a href="#">4</a>
  <a href="#">5</a>
  <a href="#">&raquo;</a>
</div>

</body>
</html>
```

## 5. İleri Düzey Özelleştirmeler

Sayfa numaralandırmayı daha da özelleştirmek için aşağıdaki gibi ek CSS özelliklerini kullanabilirsiniz:

* **Responsive Tasarım** : Farklı cihazlar için uygun hale getirmek için medya sorguları kullanabilirsiniz.
* **Daha Fazla Stil Seçenekleri** : Farklı arka plan renkleri, kenar boşlukları ve kenarlıklar ekleyebilirsiniz.
* **JavaScript Entegrasyonu** : Daha dinamik bir deneyim için sayfa numaralandırmayı JavaScript ile entegre edebilirsiniz.

Örnek olarak, responsive tasarım için medya sorgusu ekleyelim:

```css
@media screen and (max-width: 600px) {
    .pagination a {
        padding: 8px 12px;
        font-size: 12px;
    }
}
```

Bu medya sorgusu, ekran genişliği 600 pikselden küçük olduğunda sayfa numaralandırma bağlantılarının boyutunu ayarlar.

## Sonuç

CSS ile sayfa numaralandırma oluşturmak, kullanıcı deneyimini artırmak için oldukça etkili bir yöntemdir. Bu eğitimde, temel HTML yapısını ve CSS stillerini öğrendiniz. Kendi projelerinizde bu bilgileri kullanarak daha etkili ve kullanıcı dostu web sayfaları oluşturabilirsiniz. Bu eğitimde ele alınan konular, CSS'nin gücünü ve esnekliğini vurgulamakta olup, modern web geliştirme süreçlerinde sıkça karşılaşılan gereksinimlere yanıt vermektedir.
