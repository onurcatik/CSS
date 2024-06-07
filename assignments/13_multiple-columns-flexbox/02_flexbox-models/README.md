## CSS Flex Box

Bu bölümde, HTML ve CSS dosyalarını ayrı tutarak, Flexbox modelinin kullanıldığı detaylı bir web sayfası örneği sunacağız. Bu örnekte bir başlık (header), içerik (section), ve alt bilgi (footer) elemanları yer alacak. Flexbox özelliklerinin nasıl uygulandığını ve bu özelliklerin her birinin ne işe yaradığını adım adım açıklayacağız.

### HTML Kodu

HTML dosyasını `index.html` olarak adlandıralım.

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Flexbox Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header class="flex-container header">
        <div class="logo">Logo</div>
        <nav class="nav">
            <ul class="flex-container">
                <li><a href="#">Anasayfa</a></li>
                <li><a href="#">Hakkında</a></li>
                <li><a href="#">İletişim</a></li>
            </ul>
        </nav>
    </header>
    <section class="flex-container main-content">
        <article class="flex-item">Makale 1</article>
        <article class="flex-item">Makale 2</article>
        <article class="flex-item">Makale 3</article>
    </section>
    <footer class="flex-container footer">
        <div class="footer-item">© 2024 Şirket Adı</div>
        <div class="footer-item">Gizlilik Politikası</div>
        <div class="footer-item">Kullanım Koşulları</div>
    </footer>
</body>
</html>
```

### CSS Kodu

CSS dosyasını `styles.css` olarak adlandıralım.

```css
/* Genel stil tanımlamaları */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Flex container ve flex item genel stili */
.flex-container {
    display: flex;
}

.flex-item {
    padding: 20px;
    margin: 10px;
    background-color: #f0f0f0;
    border: 1px solid #ccc;
}

/* Başlık (header) stil tanımlamaları */
.header {
    justify-content: space-between;
    align-items: center;
    background-color: #333;
    color: #fff;
    padding: 10px 20px;
}

.header .nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    display: flex;
}

.header .nav li {
    margin: 0 10px;
}

.header .nav a {
    color: #fff;
    text-decoration: none;
}

/* Ana içerik (section) stil tanımlamaları */
.main-content {
    flex-direction: column;
    align-items: center;
    padding: 20px;
}

.main-content .flex-item {
    width: 100%;
    max-width: 600px;
}

/* Alt bilgi (footer) stil tanımlamaları */
.footer {
    justify-content: space-around;
    background-color: #333;
    color: #fff;
    padding: 10px 20px;
}

.footer .footer-item {
    flex: 1;
    text-align: center;
}
```

### Açıklamalar

#### Flex Container ve Flex Item

Flexbox modelinin temelinde, bir flex container ve bu container içerisinde yer alan flex item'lar bulunur. Flex container, `display: flex;` özelliği ile tanımlanır. Bu örnekte, `header`, `main-content`  elementleri flex container olarak tanımlanmıştır.

#### `justify-content` Özelliği

Bu özellik, flex item'ların ana eksen (main axis) boyunca nasıl hizalanacağını belirler. Örneğin, `header` elementinde `justify-content: space-between;` kullanılmıştır. Bu, flex item'ların (logo ve navigasyon menüsü) container içinde başlangıç ve bitiş noktalarına hizalanıp aralarında boşluk bırakılmasını sağlar.

#### `align-items` Özelliği

Bu özellik, flex item'ların çapraz eksen (cross axis) boyunca nasıl hizalanacağını belirler. `header` elementinde `align-items: center;` kullanılmıştır. Bu, flex item'ların container'ın ortasında dikey olarak hizalanmasını sağlar.

#### `flex-direction` Özelliği

Bu özellik, flex item'ların hangi yönde dizileceğini belirler. `main-content` elementinde `flex-direction: column;` kullanılmıştır. Bu, flex item'ların (makaleler) dikey olarak dizilmesini sağlar.

#### `flex-wrap` Özelliği

Bu özellik, flex item'ların container'ı aşıp aşmadığını kontrol eder. Bu örnekte `flex-wrap` kullanılmamıştır, ancak `flex-wrap: wrap;` olarak ayarlandığında, item'lar container genişliğini aştığında bir sonraki satıra geçerler.

#### `align-content` Özelliği

Bu özellik, flex hatlarının (flex lines) nasıl hizalanacağını belirler. Örneğin, `footer` elementinde `justify-content: space-around;` kullanılmıştır. Bu, flex item'ların (alt bilgi öğeleri) container içinde eşit aralıklarla hizalanmasını sağlar.

### Sonuç

Bu örnekle, Flexbox modelinin temel özelliklerini ve bu özelliklerin nasıl uygulanacağını gördük. Flexbox, modern web tasarımında esnek ve duyarlı düzenler oluşturmak için güçlü bir araçtır. Bu bilgilerle, daha esnek ve kullanıcı dostu web sayfaları tasarlayabilirsiniz.