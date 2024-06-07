### CSS List

Bu bölümde, CSS listeleri ve ilgili özellikleri kullanarak bir web sayfası oluşturacağız. Bu sayfa, HTML ve CSS kodlarını ayrı dosyalarda tutarak yapılandırılmış bir örnek sunacaktır. Örneğimizde, `header` , `section` , ve `footer` elementleri bulunacak ve farklı liste stillerinin nasıl uygulanacağını göstereceğiz.

#### HTML Dosyası (index.html)

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Listeler Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>CSS Listeler Örneği</h1>
    </header>

    <section>
        <h2>Farklı Liste Türleri</h2>

        <h3>Numarasız Liste</h3>
        <ul class="square-list">
            <li>Elma</li>
            <li>Muz</li>
            <li>Çilek</li>
        </ul>

        <h3>Numaralı Liste</h3>
        <ol class="roman-list">
            <li>Birinci</li>
            <li>İkinci</li>
            <li>Üçüncü</li>
        </ol>

        <h3>Görüntü ile Liste</h3>
        <ul class="image-list">
            <li>Bilgisayar</li>
            <li>Telefon</li>
            <li>Tablet</li>
        </ul>

        <h3>İçte ve Dışta İşaretleyici Pozisyonu</h3>
        <ul class="inside-list">
            <li>İçte Pozisyon</li>
            <li>İçte Pozisyon</li>
            <li>İçte Pozisyon</li>
        </ul>
        <ul class="outside-list">
            <li>Dışta Pozisyon</li>
            <li>Dışta Pozisyon</li>
            <li>Dışta Pozisyon</li>
        </ul>
    </section>

    <footer>
        <p>© 2024 CSS Listeler Örneği. Tüm Hakları Saklıdır.</p>
    </footer>
</body>

</html>
```

#### CSS Dosyası (styles.css)

```css
/* Genel Stil */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1em 0;
}

section {
    padding: 2em;
}

footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1em 0;
    position: fixed;
    width: 100%;
    bottom: 0;
}

/* Liste Stilleri */
.square-list {
    list-style-type: square;
}

.roman-list {
    list-style-type: upper-roman;
}

.image-list {
    list-style-image: url('path_to_image.png');
}

.inside-list {
    list-style-position: inside;
}

.outside-list {
    list-style-position: outside;
}
```

### Açıklama

#### HTML Yapısı

* **header** : Sayfanın başlığı için kullanılır. İçerisinde bir başlık (`<h1>`) bulunmaktadır.
* **section** : Ana içerik alanını barındırır. Farklı liste türlerini ve özelliklerini göstermek için kullanılmıştır. İçerisinde alt başlıklar (`<h2>` ve `<h3>`) ve listeler (`<ul>` ve `<ol>`) bulunmaktadır.
* **footer** : Sayfanın alt kısmını içerir. Telif hakkı bilgileri gibi genel bilgiler için kullanılır.

#### CSS Stilleri

* **Genel Stil** : Sayfanın genel stilini belirler. `body`,   `header`,   `section`, ve `footer` elementleri için temel stiller tanımlanmıştır.
* **Liste Stilleri** : Farklı liste türleri ve pozisyonları için özel stiller tanımlanmıştır:
  + `.square-list`: Numarasız liste elemanlarını kare işaretleyici ile gösterir.
  + `.roman-list`: Numaralı liste elemanlarını büyük Roma rakamları ile gösterir.
  + `.image-list`: Liste elemanları için özel bir görüntü işaretleyici kullanır.
  + `.inside-list`: Liste elemanı işaretleyicilerini liste elemanlarının içinde konumlandırır.
  + `.outside-list`: Liste elemanı işaretleyicilerini liste elemanlarının dışında konumlandırır.

Bu örnek, CSS listeleri ve ilgili özelliklerin nasıl uygulanacağını gösterir. HTML ve CSS dosyalarını ayrı tutarak, web sayfasının yapısını ve stilini daha düzenli ve yönetilebilir hale getirir. Bu yöntem, web geliştirme sürecinde profesyonel bir yaklaşımdır ve büyük projelerde düzeni korumak için oldukça faydalıdır.
