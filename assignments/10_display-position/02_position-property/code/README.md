### Örnek: CSS Konumlandırma Özelliklerinin Kullanımı

Bu örnekte, HTML ve CSS kullanarak bir web sayfasının üst bilgi (header), ana içerik (section), ve alt bilgi (footer) bölümlerinin nasıl konumlandırıldığını göstereceğiz. Ayrıca, her bir konumlandırma türünün nasıl çalıştığını açıklayacağız.

#### HTML Dosyası ( `index.html` )

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Position Property Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header class="header">Üst Bilgi (Header)</header>
    <section class="content">
        <div class="static">Static Pozisyon</div>
        <div class="relative">Relative Pozisyon</div>
        <div class="fixed">Fixed Pozisyon</div>
        <div class="absolute">Absolute Pozisyon</div>
        <div class="sticky">Sticky Pozisyon</div>
    </section>
</body>

</html>
```

#### CSS Dosyası ( `styles.css` )

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.header,
.footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 20px 0;
}

.header {
    position: fixed;
    top: 0;
    width: 100%;
}

.content {
    padding: 100px 20px;
}

.static {
    position: static;
    background-color: #f4f4f4;
    padding: 20px;
    margin: 10px 0;
}

.relative {
    position: relative;
    top: 20px;
    left: 20px;
    background-color: #cce7ff;
    padding: 20px;
    margin: 10px 0;
}

.fixed {
    position: fixed;
    top: 80px;
    right: 20px;
    width: 200px;
    background-color: #ffcccb;
    padding: 20px;
}

.absolute {
    position: absolute;
    top: 50px;
    left: 50px;
    background-color: #d4ffcc;
    padding: 20px;
}

.sticky {
    position: -webkit-sticky;
    /* Safari */
    position: sticky;
    top: 0;
    background-color: #ffeb3b;
    padding: 20px;
    margin: 10px 0;
}
```

### Açıklamalar

#### HTML Yapısı

* **Header** : Sayfanın en üstünde yer alır ve sabit bir konumda kalır.
* **Section** : Ana içeriği barındırır ve konumlandırma özelliklerinin farklı kullanım örneklerini içerir.
* **Footer** : Sayfanın altında yer alır ve normal akışa göre yerleştirilir.

#### CSS Açıklamaları

1. **Genel Ayarlar** : 
   - `body` etiketine genel stil ayarları uygulanır.
   - `box-sizing: border-box;` tüm elemanların içerik, dolgu (padding) ve kenarları (border) dahil olmak üzere tam genişlik ve yükseklik almasını sağlar.

2. **Üst Bilgi (Header) ve Alt Bilgi (Footer)** :
   - `.header` : Sabitlenmiş konumda ( `position: fixed;` ) ve ekranın üst kısmına yerleştirilmiştir.
   

3. **Ana İçerik (Section)** :
   - `.static` : Statik konumda ( `position: static;` ) ve sayfanın normal akışına göre yerleştirilmiştir.
   - `.relative` : Göreceli konumda ( `position: relative;` ) ve normal konumundan 20 piksel aşağı ve 20 piksel sağa kaydırılmıştır.
   - `.fixed` : Sabitlenmiş konumda ( `position: fixed;` ) ve ekranın sağ üst köşesine yerleştirilmiştir.
   - `.absolute` : Mutlak konumda ( `position: absolute;` ) ve en yakın konumlandırılmış ata elemanına göre yerleştirilmiştir.
   - `.sticky` : Kaydırma pozisyonuna göre yapışkan konumda ( `position: sticky;` ) ve ekranın üst kısmına sabitlenmiştir.

### Sonuç

Bu örnek, CSS konumlandırma özelliklerinin nasıl çalıştığını ve farklı durumlarda nasıl kullanılabileceğini göstermektedir. Her bir konumlandırma türünün kendine özgü davranışları vardır ve doğru kullanıldığında web sayfalarının düzenini ve kullanıcı deneyimini iyileştirir. Bu bilgilerin doğru ve etkili bir şekilde uygulanması, gelişmiş ve profesyonel web sitelerinin oluşturulmasında kritik öneme sahiptir.
