# HTML and CSS Text

Bu bölümde, yukarıda bahsedilen CSS metin özelliklerini kullanarak bir HTML sayfası ve ona bağlı CSS dosyasını oluşturacağız. Bu örnek, özelliklerin nasıl kullanılacağını ve birbirleriyle nasıl etkileşimde bulunacağını gösterecektir.

## HTML Dosyası (index.html)

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Metin Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>CSS Metin Özellikleri</h1>
    </header>
    <main>
        <section>
            <h2>Metin Rengi ve Arka Plan Rengi</h2>
            <p class="text-color">Bu metin mavi renkte ve sarı arka planda görünecektir.</p>
        </section>
        <section>
            <h2>Metin Hizalama</h2>
            <p class="left">Bu metin sola hizalanmıştır.</p>
            <p class="right">Bu metin sağa hizalanmıştır.</p>
            <p class="center">Bu metin ortalanmıştır.</p>
            <p class="justify">Bu metin iki yana yaslanmıştır ve satırlar arasındaki boşluklar eşitlenmiştir. Metnin düzeni daha düzenli görünür.</p>
        </section>
        <section>
            <h2>Son Satırın Hizalanması</h2>
            <p class="justify-last">Bu metin iki yana yaslanmış, ancak son satır sağa hizalanmıştır.</p>
        </section>
        <section>
            <h2>Dikey Hizalama</h2>
            <div class="vertical-align-example">
                <span class="vertical-align-middle">Orta</span>
                <span class="vertical-align-top">Üst</span>
                <span class="vertical-align-bottom">Alt</span>
            </div>
        </section>
        <section>
            <h2>Metin Dönüşümü ve Dekorasyonu</h2>
            <p class="uppercase">Bu metin tamamen büyük harflerle yazılmıştır.</p>
            <p class="lowercase">BU METİN TAMAMEN KÜÇÜK HARFLERLE YAZILMIŞTIR.</p>
            <p class="capitalize">bu metin her kelimenin ilk harfi büyük olacak şekilde yazılmıştır.</p>
            <p class="underline">Bu metnin altı çizilidir.</p>
            <p class="overline">Bu metnin üstü çizilidir.</p>
            <p class="line-through">Bu metnin üstü çizilidir.</p>
        </section>
        <section>
            <h2>Harf ve Kelime Aralığı</h2>
            <p class="letter-spacing">Bu metnin harfleri arasındaki boşluk artırılmıştır.</p>
            <p class="word-spacing">Bu metnin kelimeleri arasındaki boşluk artırılmıştır.</p>
        </section>
        <section>
            <h2>Satır Yüksekliği</h2>
            <p class="line-height">Bu metnin satır yüksekliği artırılmıştır. Bu, metnin daha okunabilir olmasını sağlar.</p>
        </section>
    </main>
    <footer>
        <p>Bu sayfa, CSS metin özelliklerinin nasıl kullanılacağını göstermek amacıyla oluşturulmuştur.</p>
    </footer>
</body>

</html>
```

## CSS Dosyası (styles.css)

```css
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header,
footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 1em 0;
}

header h1,
footer p {
    margin: 0;
}

main {
    padding: 20px;
}

section {
    margin-bottom: 20px;
    padding: 20px;
    background: #fff;
    border: 1px solid #ddd;
    border-radius: 8px;
}

h2 {
    color: #333;
    border-bottom: 2px solid #ddd;
    padding-bottom: 10px;
}

.text-color {
    color: blue;
    background-color: yellow;
    padding: 10px;
}

.left {
    text-align: left;
}

.right {
    text-align: right;
}

.center {
    text-align: center;
}

.justify {
    text-align: justify;
}

.justify-last {
    text-align: justify;
    text-align-last: right;
}

.vertical-align-example {
    display: flex;
    align-items: baseline;
    justify-content: space-around;
    border: 1px solid #ddd;
    padding: 10px;
}

.vertical-align-middle {
    vertical-align: middle;
}

.vertical-align-top {
    vertical-align: top;
}

.vertical-align-bottom {
    vertical-align: bottom;
}

.uppercase {
    text-transform: uppercase;
}

.lowercase {
    text-transform: lowercase;
}

.capitalize {
    text-transform: capitalize;
}

.underline {
    text-decoration: underline;
}

.overline {
    text-decoration: overline;
}

.line-through {
    text-decoration: line-through;
}

.letter-spacing {
    letter-spacing: 2px;
}

.word-spacing {
    word-spacing: 4px;
}

.line-height {
    line-height: 1.8;
}
```

Bu örnek, CSS'in metin biçimlendirme özelliklerini gösteren kapsamlı ve detaylı bir HTML ve CSS uygulamasıdır. HTML dosyasında çeşitli metin biçimlendirme örnekleri bulunmakta ve her bir örnek CSS dosyasındaki ilgili stil tanımlarıyla şekillendirilmektedir. Bu yapı, web sayfalarınızda CSS metin özelliklerini nasıl kullanabileceğinizi ve farklı özelliklerin birbirleriyle nasıl etkileşimde bulunabileceğini görmenizi sağlar.
