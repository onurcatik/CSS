# CSS Margin

## HTML Kodu

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Margin Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <div class="container">
        <div class="box" id="box1">Box 1</div>
        <div class="box" id="box2">Box 2</div>
        <div class="box" id="box3">Box 3</div>
    </div>
</body>

</html>
```

## CSS Kodu

```css
/* styles.css */
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.container {
    width: 80%;
    background-color: #fff;
    padding: 20px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.box {
    background-color: #3498db;
    color: white;
    padding: 20px;
    margin-bottom: 20px;
    text-align: center;
    font-size: 1.2em;
}

/* Bireysel kenarlar için margin */
#box1 {
    margin-top: 30px;
    margin-right: 15px;
    margin-bottom: 10px;
    margin-left: 15px;
}

/* Kısayol kullanımı */
#box2 {
    margin: 20px 10px;
}

/* Otomatik hizalama */
#box3 {
    margin: 0 auto;
    width: 50%;
}
```

## Açıklamalar

1. **HTML Yapısı**:
   - HTML dosyamız, üç adet `div` öğesi içeren bir `container` (kapsayıcı) içerir. Bu `div` öğeleri "box" sınıfına sahiptir ve her biri farklı `id` değerleri taşır (`box1`, `box2`, `box3`). Her kutu öğesi, farklı margin özellikleri ile stilize edilmiştir.
   
2. **CSS Yapısı**:
   - **`body`**: Sayfanın genel stilini belirler. `font-family` ile yazı tipini belirler, `background-color` ile arka plan rengini ayarlar. `margin` ve `padding` sıfırlanır. Flexbox kullanarak içeriği hem yatay hem dikey olarak merkezler (`justify-content: center; align-items: center;`) ve tam ekran yüksekliği ayarlanır (`height: 100vh;`).
   
   - **`.container`**: Genişliği %80 olan, beyaz arka planlı ve gölgeli bir kapsayıcıdır. İçerisine 20 piksel padding eklenmiştir ve hafif bir gölge efekti uygulanmıştır (`box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);`).
   
   - **`.box`**: Tüm kutulara uygulanan temel stil. Mavi arka plan, beyaz yazı rengi, padding ve margin içerir. Yazı boyutu 1.2em olarak ayarlanmış ve metin ortalanmıştır.
   
   - **`#box1`**: Bireysel kenarlar için margin ayarları yapılmıştır (`margin-top: 30px; margin-right: 15px; margin-bottom: 10px; margin-left: 15px;`). Bu, her kenar için farklı bir margin değeri belirlememize olanak tanır.
   
   - **`#box2`**: Kısayol kullanımı ile margin ayarları yapılmıştır (`margin: 20px 10px;`). Bu yazımda ilk değer (`20px`) üst ve alt kenarlar için, ikinci değer (`10px`) ise sağ ve sol kenarlar için margin değerini belirtir.
   
   - **`#box3`**: Otomatik hizalama ile kutu yatay olarak ortalanmış ve genişliği %50 olarak belirlenmiştir (`margin: 0 auto; width: 50%;`). `margin: 0 auto;` kullanımı, öğeyi yatay olarak ortalamak için kullanılır.

Bu örnek, CSS margin özelliklerinin çeşitli kullanım durumlarını göstermektedir. Kutu elemanlarının her biri, farklı margin ayarları ile stillendirilmiş ve web sayfasının düzenini nasıl etkilediği gözlemlenebilir. Bu sayede CSS margin özelliklerinin pratik uygulamaları anlaşılabilir.