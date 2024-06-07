### CSS Gradyan

Bu örnekte, CSS gradyanları kullanarak bir web sayfası oluşturacağız. Web sayfamızın HTML ve CSS kodlarını ayrı dosyalara koyacağız ve bir header, main, section ve footer bileşenlerinden oluşan tam bir sayfa yapısı oluşturacağız.

#### HTML Kodu

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Gradyanları Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>CSS Gradyanlarıyla Tasarım</h1>
    </header>
    <main>
        <section class="linear-gradient">
            <h2>Lineer Gradyan</h2>
            <p>Bu bölümde, sağa doğru giden bir lineer gradyan örneği gösterilmektedir.</p>
        </section>
        <section class="radial-gradient">
            <h2>Radyal Gradyan</h2>
            <p>Bu bölümde, merkezden yayılan bir radyal gradyan örneği gösterilmektedir.</p>
        </section>
        <section class="conic-gradient">
            <h2>Konik Gradyan</h2>
            <p>Bu bölümde, saat yönünde dönen bir konik gradyan örneği gösterilmektedir.</p>
        </section>
    </main>
    <footer>
        <p>© 2024 CSS Gradyanları Örneği. Tüm Hakları Saklıdır.</p>
    </footer>
</body>

</html>
```

#### CSS Kodu

```css
/* styles.css */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background: #f0f0f0;
    color: #333;
}

header {
    background: linear-gradient(to right, #4a90e2, #9013fe);
    color: white;
    padding: 20px;
    text-align: center;
}

main {
    padding: 20px;
}

section {
    margin: 20px 0;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.linear-gradient {
    background: linear-gradient(to right, #ff7e5f, #feb47b);
}

.radial-gradient {
    background: radial-gradient(circle, #ff7e5f, #feb47b);
}

.conic-gradient {
    background: conic-gradient(from 0deg, #ff7e5f, #feb47b, #ff7e5f);
}

footer {
    background: linear-gradient(to right, #4a90e2, #9013fe);
    color: white;
    text-align: center;
    padding: 10px;
    position: fixed;
    bottom: 0;
    width: 100%;
}
```

### Açıklama

#### HTML Kodu

HTML belgemiz, web sayfamızın yapısını tanımlar. `header` , `main` , `section` ve `footer` etiketlerini kullanarak sayfamızı bölümlere ayırıyoruz. Her `section` etiketine, CSS'de belirlediğimiz sınıf adlarını ( `linear-gradient` , `radial-gradient` , `conic-gradient` ) atıyoruz.

* **header** : Sayfanın başlık kısmını içerir. Lineer gradyan arka plan rengi uygulanmıştır.
* **main** : Sayfanın ana içeriğini içerir. Üç farklı bölüm (`section`) içerir.
    - **section (linear-gradient)** : Sağdan sola doğru lineer bir gradyan arka planı kullanır.
    - **section (radial-gradient)** : Dairesel bir radyal gradyan arka planı kullanır.
    - **section (conic-gradient)** : Saat yönünde dönen bir konik gradyan arka planı kullanır.
* **footer** : Sayfanın altbilgi kısmını içerir. Lineer gradyan arka plan rengi uygulanmıştır.

#### CSS Kodu

CSS belgemiz, HTML yapımızın stilini tanımlar.

* **body** : Tüm sayfa için genel stil ayarları (font, arka plan rengi, metin rengi) yapılır.
* **header** : Başlık kısmı için lineer gradyan arka planı ve metin stil ayarları yapılır.
* **main** : Ana içerik bölümü için padding ayarı yapılır.
* **section** : Her bölüm için margin, padding, border-radius ve box-shadow ayarları yapılır.
    - **.linear-gradient** : Sağdan sola doğru lineer gradyan arka planı uygulanır.
    - **.radial-gradient** : Dairesel radyal gradyan arka planı uygulanır.
    - **.conic-gradient** : Konik gradyan arka planı uygulanır.
* **footer** : Altbilgi kısmı için lineer gradyan arka planı ve metin stil ayarları yapılır.

Bu örnek, CSS gradyanlarının nasıl kullanılacağını ve HTML ile CSS kodlarının nasıl ayrı dosyalarda düzenleneceğini göstermektedir. Gradyanlar, web sayfalarınıza estetik ve modern bir görünüm kazandırmak için etkili bir yöntemdir.
