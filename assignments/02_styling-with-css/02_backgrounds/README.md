### CSS Backgrounds

Bu örnek, HTML ve CSS kullanarak bir web sayfasında çeşitli arka plan özelliklerini nasıl kullanacağınızı göstermektedir. HTML ve CSS dosyaları ayrı tutulacak ve her bir özellik detaylı olarak ele alınacaktır.

#### HTML (index.html)

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Arka Plan Özellikleri</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header class="header">
        <h1>CSS Arka Plan Özellikleri Örneği</h1>
    </header>
    <section class="content">
        <div class="box box1">
            <p>Bu kutu, sabit bir arka plan resmine sahiptir.</p>
        </div>
        <div class="box box2">
            <p>Bu kutu, tekrar etmeyen bir arka plan resmine sahiptir.</p>
        </div>
        <div class="box box3">
            <p>Bu kutu, merkezde konumlandırılmış bir arka plan resmine sahiptir.</p>
        </div>
        <div class="box box4">
            <p>Bu kutu, %50 yatay ve dikey pozisyonda konumlandırılmış bir arka plan resmine sahiptir.</p>
        </div>
    </section>
</body>

</html>
```

#### CSS (styles.css)

```css
/* Genel Stiller */
body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
}

header {
    background-color: #333;
    color: #fff;
    padding: 20px;
    width: 100%;
    text-align: center;
}

.content {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
    margin: 20px 0;
}

.box {
    width: 200px;
    height: 200px;
    border: 1px solid #ccc;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    color: #333;
    padding: 10px;
    box-sizing: border-box;
}

/* Arka Plan Özellikleri */
.box1 {
    background-image: url('fixed-background.jpg');
    background-attachment: fixed;
}

.box2 {
    background-image: url('no-repeat-background.jpg');
    background-repeat: no-repeat;
    background-size: cover;
}

.box3 {
    background-image: url('center-background.jpg');
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
}

.box4 {
    background-image: url('position-background.jpg');
    background-position: 50% 50%;
    background-repeat: no-repeat;
    background-size: cover;
}
```

### Açıklamalar

* **Genel Stiller:** `body` elementinin arka plan rengi ve temel stil özellikleri belirlenmiştir. `header` ve `.content` elementleri için de stil ayarları yapılmıştır.
* **Arka Plan Özellikleri:** 
  + `.box1`: Sabit arka plan resmine sahiptir. Kullanıcı sayfayı kaydırdığında arka plan resmi sabit kalır.
  + `.box2`: Arka plan resmi tekrar etmez ve kutuyu tamamen kaplar.
  + `.box3`: Arka plan resmi merkezde konumlandırılmıştır ve tekrar etmez.
  + `.box4`: Arka plan resmi, %50 yatay ve dikey pozisyonda konumlandırılmıştır ve tekrar etmez.

Bu örnek, CSS arka plan özelliklerinin nasıl kullanılacağını göstermektedir. Arka plan resimlerinin etkili kullanımı, web sayfalarının estetik ve fonksiyonel olmasını sağlar. Bu örneklerde kullanılan resimler, ilgili dosyalarla aynı dizinde yer almalıdır.
