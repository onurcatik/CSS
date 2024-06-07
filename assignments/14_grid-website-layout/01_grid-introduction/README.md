  # CSS Grid Layout Introduction

## Giriş

CSS Grid Layout Modülü, web sayfaları için esnek ve güçlü bir düzen sistemi sunar. Bu modül, satır ve sütunlar kullanarak karmaşık düzenler oluşturmayı kolaylaştırır. Bu bölümde, bir HTML sayfasında CSS Grid kullanarak nasıl bir düzen oluşturabileceğimizi detaylı bir örnekle açıklayacağız.

## HTML ve CSS Ayrı Dosyalarla Örnek

Aşağıda, bir HTML dosyası ve bir CSS dosyası kullanarak bir ızgara düzeni nasıl oluşturabileceğinizi göreceksiniz. Bu örnek, bir başlık, iki bölüm ve bir altbilgi içerir.

### HTML Dosyası (index.html)

```html
<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Grid Layout Örneği</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header class="grid-item header">
    <h1>CSS Grid Layout</h1>
  </header>
  <section class="grid-item section">
    <p>Bu bölümde, CSS Grid Layout'un nasıl kullanılacağını öğreneceksiniz.</p>
  </section>
  <section class="grid-item section">
    <p>Izgara düzeni, web sayfalarında düzeni sağlamak için mükemmel bir yöntemdir.</p>
  </section>
  
</body>
</html>
```

### CSS Dosyası (styles.css)

```css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: auto 1fr 1fr auto;
  gap: 10px;
  min-height: 100vh;
}

.header {
  grid-column: 1 / -1;
  background-color: #4CAF50;
  color: white;
  text-align: center;
  padding: 20px;
}

.section {
  background-color: #f4f4f4;
  padding: 20px;
}


```

## Açıklamalar

### HTML Açıklamaları

- **Header:** Başlık kısmı, `header` etiketi içinde yer alır ve ızgaranın birinci satırında tam genişlik kaplar.
- **Section:** İki bölüm, `section` etiketi içinde yer alır ve ızgaranın ikinci ve üçüncü satırlarını kaplar.


### CSS Açıklamaları

- **Body:** `display: grid;` özelliği ile ızgara konteyneri olarak tanımlanmıştır. `grid-template-columns: repeat(2, 1fr);` iki sütunlu bir ızgara oluşturur. `grid-template-rows: auto 1fr 1fr auto;` ise satırların yüksekliğini ayarlar. `gap: 10px;` satır ve sütunlar arasındaki boşlukları belirler.
- **Header:** `grid-column: 1 / -1;` özelliği, başlık kısmının ızgaranın tam genişlik kaplamasını sağlar. Arka plan rengi ve diğer stil özellikleri belirlenmiştir.
- **Section:** Bölümler, arka plan rengi ve iç dolgu (padding) ile stillendirilmiştir.
- **Footer:** Altbilgi kısmı da tam genişlik kaplayacak şekilde ayarlanmıştır ve benzer şekilde stillendirilmiştir.

## Sonuç

Bu örnek, CSS Grid Layout kullanarak basit ve esnek bir web sayfası düzeni oluşturmayı göstermektedir. Izgara düzeni, web sayfalarında içerikleri düzenlemek ve düzeni sağlamak için güçlü bir araçtır. Bu teknik, özellikle karmaşık düzenler ve farklı cihazlarda uyumlu tasarımlar oluşturmak için idealdir.