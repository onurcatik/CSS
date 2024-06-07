# CSS Website Layout

## Giriş

Web siteleri genellikle başlıklar, menüler, içerikler ve altbilgiler olarak bölümlere ayrılır. Bu bölümler, web sitesinin kullanıcı dostu ve düzenli olmasını sağlar. CSS (Cascading Style Sheets), bu bölümlerin stilini ve yerleşimini kontrol etmek için kullanılır. Bu tutorial, CSS kullanarak bir web sitesi düzeninin nasıl oluşturulacağını detaylı bir şekilde açıklamaktadır.

## Başlık (Header)

Başlık genellikle web sitesinin en üstünde yer alır (veya bir üst navigasyon menüsünün hemen altında). Çoğunlukla bir logo veya web sitesi adını içerir.

## Örnek Kod

```html
<!DOCTYPE html>
<html>
<head>
<style>
.header {
    background-color: #f1f1f1;
    padding: 20px;
    text-align: center;
    font-size: 35px;
}
</style>
</head>
<body>

<div class="header">
  <h1>Web Sitesi Adı</h1>
  <p>Web Sitesi Sloganı</p>
</div>

</body>
</html>
```

## Navigasyon Çubuğu (Navigation Bar)

Navigasyon çubuğu, ziyaretçilerin web sitenizde gezinebilmesi için bağlantılar listesi içerir.

## Örnek Kod

```html
<!DOCTYPE html>
<html>
<head>
<style>
.navbar {
    overflow: hidden;
    background-color: #333;
}

.navbar a {
    float: left;
    display: block;
    color: #f2f2f2;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
}

.navbar a:hover {
    background-color: #ddd;
    color: black;
}
</style>
</head>
<body>

<div class="navbar">
  <a href="#home">Ana Sayfa</a>
  <a href="#news">Haberler</a>
  <a href="#contact">İletişim</a>
  <a href="#about">Hakkında</a>
</div>

</body>
</html>
```

## İçerik/Kolonlar (Content/Columns)

Ana içerik, web sitenizin en büyük ve en önemli kısmıdır. Bu bölüm genellikle birden fazla sütundan oluşur.

## Örnek Kod

```html
<!DOCTYPE html>
<html>
<head>
<style>
.row {
  display: flex;
}

.side {
  flex: 30%;
  background-color: #f1f1f1;
  padding: 20px;
}

.main {
  flex: 70%;
  background-color: #ffffff;
  padding: 20px;
}
</style>
</head>
<body>

<div class="row">
  <div class="side">
    <h2>Yan Menü</h2>
    <p>Yan menü içeriği.</p>
  </div>
  <div class="main">
    <h2>Ana İçerik</h2>
    <p>Ana içerik bölümü.</p>
  </div>
</div>

</body>
</html>
```

## Altbilgi (Footer)

Altbilgi, sayfanızın en altında yer alır. Genellikle telif hakkı ve iletişim bilgileri gibi bilgiler içerir.

## Örnek Kod

```html
<!DOCTYPE html>
<html>
<head>
<style>
.footer {
    background-color: #f1f1f1;
    padding: 10px;
    text-align: center;
}
</style>
</head>
<body>

<div class="footer">
  <p>Telif Hakkı © 2024 Tüm Hakları Saklıdır.</p>
</div>

</body>
</html>
```

## CSS ile Web Sitesi Düzeni Oluşturma

CSS, HTML öğelerinin düzenini kontrol etmek için kullanılır. Bu örnekler, temel bir web sitesi düzeni oluşturmak için gereken adımları göstermektedir. Bu düzen, çeşitli cihaz ve ekran boyutlarına uyacak şekilde daha da geliştirilebilir.

## Kritik İnceleme ve Düzeltmeler

Belgede belirtilen düzenleme yapısında bazı iyileştirmeler ve düzeltmeler yapılabilir. Örneğin, esnek düzen (flex layout) ve ızgara düzeni (grid layout) kullanarak daha modern ve duyarlı tasarımlar oluşturulabilir. Ayrıca, erişilebilirlik ve SEO (Arama Motoru Optimizasyonu) dikkate alınarak HTML yapısı daha semantik hale getirilebilir.

## Flexbox ve Grid Kullanımı

```css
/* Flexbox ile yan yana dizilim */
.row {
  display: flex;
}

/* Grid ile düzenleme */
.container {
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 10px;
}
```

Flexbox ve Grid kullanarak daha karmaşık ve esnek düzenler oluşturabilirsiniz. Bu teknikler, web tasarımında modern yaklaşımları temsil eder ve çeşitli cihazlarda tutarlı bir kullanıcı deneyimi sağlar.

## Sonuç

Bu tutorial, temel bir web sitesi düzeni oluşturmak için CSS kullanımı hakkında kapsamlı ve detaylı bilgiler sunmuştur. CSS'in gücünü kullanarak, web sitenizi daha kullanıcı dostu ve estetik hale getirebilirsiniz. Bu bilgiler, web tasarımı ve geliştirme konusundaki profesyonel standartları yansıtacak şekilde hazırlanmıştır.
