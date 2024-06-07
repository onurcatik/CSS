### CSS Tooltip 

CSS tooltipler, kullanıcıların fare imlecini bir öğenin üzerine getirdiğinde ek bilgi görüntülemelerini sağlayan önemli bir kullanıcı arayüzü bileşenidir. Bu bölümde, kapsamlı ve detaylı bir örnek sunarak, tooltiplerin nasıl oluşturulacağını ve stil verileceğini göstereceğiz. HTML ve CSS dosyalarını ayrı tutarak, kodun daha düzenli ve yönetilebilir olmasını sağlayacağız. Ayrıca, HTML'de `section` ve `footer` etiketlerini de kullanacağız.

#### HTML Dosyası (index.html)

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Tooltip Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>CSS Tooltip Örneği</h1>
    </header>

    <section>
        <h2>Temel Tooltip</h2>
        <div class="tooltip">Üzerine gelin
            <span class="tooltiptext">Temel Tooltip Metni</span>
        </div>

        <h2>Gelişmiş Tooltip</h2>
        <div class="tooltip-advanced">Üzerine gelin
            <span class="tooltiptext-advanced">Gelişmiş Tooltip Metni</span>
        </div>

        <h2>Farklı Konumlandırmalar</h2>
        <div class="tooltip tooltip-right">Sağda
            <span class="tooltiptext">Sağ Tooltip</span>
        </div>
        <div class="tooltip tooltip-bottom">Altta
            <span class="tooltiptext">Alt Tooltip</span>
        </div>
        <div class="tooltip tooltip-left">Solda
            <span class="tooltiptext">Sol Tooltip</span>
        </div>
    </section>

    <footer>
        <p>Bu örnek, kullanıcı deneyimini artırmak için CSS kullanarak nasıl tooltip oluşturulacağını göstermektedir.</p>
    </footer>
</body>

</html>
```

#### CSS Dosyası (styles.css)

```css
/* Genel Stiller */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: #fff;
    width: 100%;
    padding: 10px 0;
    text-align: center;
}

section {
    margin: 20px;
    width: 80%;
}

footer {
    background-color: #333;
    color: #fff;
    width: 100%;
    padding: 10px 0;
    text-align: center;
    position: fixed;
    bottom: 0;
}

/* Tooltip Stilleri */
.tooltip,
.tooltip-advanced {
    position: relative;
    display: inline-block;
    cursor: pointer;
    margin: 10px;
}

.tooltip .tooltiptext,
.tooltip-advanced .tooltiptext-advanced {
    visibility: hidden;
    width: 140px;
    background-color: black;
    color: #fff;
    text-align: center;
    border-radius: 6px;
    padding: 5px 0;
    position: absolute;
    z-index: 1;
    opacity: 0;
    transition: opacity 0.6s, transform 0.6s;
}

/* Temel Tooltip Stilleri */
.tooltip .tooltiptext {
    bottom: 125%;
    left: 50%;
    margin-left: -70px;
    transform: translateY(-10px);
}

.tooltip:hover .tooltiptext {
    visibility: visible;
    opacity: 1;
    transform: translateY(0);
}

/* Gelişmiş Tooltip Stilleri */
.tooltip-advanced .tooltiptext-advanced {
    bottom: 125%;
    left: 50%;
    margin-left: -70px;
    transform: translateY(-10px);
    background-color: darkblue;
    padding: 10px;
}

.tooltip-advanced:hover .tooltiptext-advanced {
    visibility: visible;
    opacity: 1;
    transform: translateY(0);
}

/* Farklı Konumlandırmalar */
.tooltip-right .tooltiptext {
    bottom: auto;
    top: 50%;
    left: 125%;
    margin-left: 0;
    margin-top: -30px;
}

.tooltip-bottom .tooltiptext {
    top: 125%;
    bottom: auto;
    left: 50%;
    margin-left: -60px;
}

.tooltip-left .tooltiptext {
    top: 50%;
    bottom: auto;
    right: 125%;
    left: auto;
    margin-top: -30px;
}
```

### Açıklama

#### HTML Yapısı

* **header** : Sayfanın başlığı ve tanıtım metni için kullanılır.
* **section** : Sayfanın ana içeriği bu bölümde yer alır. Tooltiplerin çeşitli örnekleri ve konumlandırmaları burada gösterilmiştir.
* **footer** : Sayfanın alt bilgisi, kısa bir açıklama içerir.

#### CSS Stilleri

* **Genel Stiller** : Sayfa düzeni ve temel stiller tanımlanmıştır. `body`,  `header`,  `section`, ve `footer` için genel düzen ve renk ayarları yapılmıştır.
* **Tooltip Stilleri** : Tooltiplerin temel ve gelişmiş stilleri tanımlanmıştır. `visibility`,  `opacity`, ve `transition` kullanılarak tooltiplerin animasyonları sağlanmıştır.
* **Farklı Konumlandırmalar** : Tooltiplerin farklı konumlarda gösterilmesi için özel sınıflar (`.tooltip-right`,  `.tooltip-bottom`,  `.tooltip-left`) tanımlanmıştır.

Bu kapsamlı örnek, tooltiplerin nasıl oluşturulacağını, stil verileceğini ve konumlandırılacağını gösterir. HTML ve CSS dosyalarının ayrılması, kodun daha düzenli ve anlaşılır olmasını sağlar. Ayrıca, erişilebilirlik standartlarına uygun şekilde tooltiplerin oluşturulması, kullanıcı deneyimini önemli ölçüde artırır.
