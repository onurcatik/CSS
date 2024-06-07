## CSS Shadow Effects

Bu bölümde, CSS `text-shadow` ve `box-shadow` özelliklerinin nasıl kullanılacağını gösteren kapsamlı bir örnek oluşturacağız. HTML ve CSS kodlarını ayrı dosyalarda tutarak daha düzenli ve modüler bir yapı elde edeceğiz.

### HTML Dosyası ( `index.html` )

Öncelikle, HTML dosyamızı oluşturacağız. Bu dosya, örnek metin ve kutu öğeleri içerecek.

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Gölge Efektleri Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <section>
        <h1>Metin Gölge Efekti</h1>
        <p class="text-shadow-example">Bu, bir metin gölge efekti örneğidir.</p>
    </section>
    <section>
        <h1>Kutu Gölge Efekti</h1>
        <div class="box-shadow-example">Bu, bir kutu gölge efekti örneğidir.</div>
        <div class="box-shadow-inset-example">Bu, bir iç kutu gölge efekti örneğidir.</div>
    </section>
</body>

</html>
```

### CSS Dosyası ( `styles.css` )

Şimdi, gölge efektlerini uygulayacağımız CSS dosyasını oluşturacağız. Bu dosya, HTML öğelerine stil eklemek için kullanılacaktır.

```css
/* Genel Stil Ayarları */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 20px;
    background-color: #f0f0f0;
}

/* Bölüm Başlıkları */
h1 {
    color: #333;
    text-align: center;
    margin-bottom: 20px;
}

/* Metin Gölge Efekti */
.text-shadow-example {
    font-size: 24px;
    color: #333;
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
    text-align: center;
    margin-bottom: 40px;
}

/* Kutu Gölge Efekti */
.box-shadow-example {
    width: 300px;
    height: 100px;
    margin: 0 auto 40px;
    background-color: #fff;
    box-shadow: 3px 3px 10px rgba(0, 0, 0, 0.5);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 18px;
    color: #333;
}

/* İç Kutu Gölge Efekti */
.box-shadow-inset-example {
    width: 300px;
    height: 100px;
    margin: 0 auto;
    background-color: #fff;
    box-shadow: inset 3px 3px 10px rgba(0, 0, 0, 0.5);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 18px;
    color: #333;
}
```

### Açıklama

#### HTML Yapısı

HTML dosyamız iki ana bölüm ( `section` ) içerir:
1. `Metin Gölge Efekti`: Bu bölüm,  `text-shadow` özelliğini göstermek için bir başlık (`h1`) ve bir paragraf (`p`) içerir.
2. `Kutu Gölge Efekti`: Bu bölüm,  `box-shadow` özelliğini göstermek için iki kutu (`div`) içerir. İlk kutu dış gölge, ikinci kutu ise iç gölge efektine sahiptir.

#### CSS Stilleri

1. **Genel Stil Ayarları** :
    - `body` etiketi için genel yazı tipi, kenar boşlukları ve arka plan rengi ayarlandı.
    - `h1` etiketi için yazı rengi, hizalama ve alt kenar boşluğu ayarlandı.

2. **Metin Gölge Efekti** :
    - `.text-shadow-example` sınıfı, `text-shadow` özelliği ile metne gölge uyguladı.
    - Bu özellik, metnin daha belirgin ve derinlikli görünmesini sağlar.

3. **Kutu Gölge Efekti** :
    - `.box-shadow-example` sınıfı, `box-shadow` özelliği ile kutuya dış gölge uyguladı.
    - `.box-shadow-inset-example` sınıfı ise `inset` anahtar kelimesi kullanarak iç gölge uyguladı.
    - Her iki sınıf da kutuların ortalanmasını ve içeriğin merkezde hizalanmasını sağladı.

Bu örnek, `text-shadow` ve `box-shadow` özelliklerinin temel ve ileri düzey kullanımını göstermektedir. Her iki özellik de metinler ve öğeler üzerinde görsel derinlik oluşturmak için etkili araçlardır. Bu tür gölge efektleri, tasarımlarınıza estetik bir katkı sağlar ve kullanıcı deneyimini zenginleştirir.
