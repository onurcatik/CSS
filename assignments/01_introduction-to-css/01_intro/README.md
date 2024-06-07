# HTML ve CSS

## HTML Kısmı (index.html)

Bu örnekte, basit bir web sayfası oluşturacağız. Sayfada bir başlık, paragraf ve bir buton bulunacak. Ayrıca, bu öğelerin stilini belirlemek için ayrı bir CSS dosyası kullanacağız.

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Örnek Web Sayfası</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>Örnek Web Sayfasına Hoşgeldiniz</h1>
    </header>
    <main>
        <p>Bu, basit bir web sayfası örneğidir. Bu paragraf, CSS kullanılarak stilize edilmiştir.</p>
        <button>Butona Tıklayın</button>
    </main>
    <footer>
        <p>&copy; 2024 Örnek Şirket</p>
    </footer>
</body>

</html>
```

## CSS Kısmı (styles.css)

Aşağıda, yukarıdaki HTML dosyasını stilize etmek için kullanılan CSS kuralları yer almaktadır. Bu kurallar, öğelerin rengini, yazı tipi boyutunu, kenar boşluklarını ve daha fazlasını belirler.

```css
/* Genel stil kuralları */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f0f0f0;
    color: #333;
}

/* Başlık stil kuralları */
header {
    background-color: #4CAF50;
    color: white;
    text-align: center;
    padding: 1em 0;
}

header h1 {
    margin: 0;
}

/* Ana içerik stil kuralları */
main {
    padding: 2em;
}

main p {
    font-size: 1.2em;
    line-height: 1.6;
}

/* Buton stil kuralları */
button {
    background-color: #4CAF50;
    color: white;
    border: none;
    padding: 1em 2em;
    cursor: pointer;
    font-size: 1em;
    border-radius: 5px;
}

button:hover {
    background-color: #45a049;
}

/* Alt bilgi stil kuralları */
footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1em 0;
    position: fixed;
    width: 100%;
    bottom: 0;
}
```

## Açıklama

Bu örnek, HTML ve CSS kullanarak bir web sayfasının nasıl oluşturulacağını ve stil verileceğini göstermektedir:

1. **HTML Dosyası (index.html)** :
    - **`<head>` Bölümü** : Sayfanın başlık bilgilerini ve harici CSS dosyasına bağlantıyı içerir.
    - **`<body>` Bölümü** : Sayfanın içerik kısmını içerir. Bu bölümde bir başlık, ana içerik ve alt bilgi bulunur.
    - **`<header>` Etiketi** : Sayfanın başlık bölümünü içerir.
    - **`<main>` Etiketi** : Ana içerik bölümünü içerir.
    - **`<footer>` Etiketi** : Alt bilgi bölümünü içerir.

2. **CSS Dosyası (styles.css)** :
    - **Genel Stil Kuralları** : Tüm sayfa için geçerli olan temel stil kurallarını belirler.
    - **Başlık (Header) Stil Kuralları** : Başlık bölümünün arka plan rengini, metin rengini ve hizalamasını belirler.
    - **Ana İçerik Stil Kuralları** : Ana içerik bölümünün kenar boşluklarını ve paragraf stilini belirler.
    - **Buton Stil Kuralları** : Butonun rengini, boyutunu, kenarlarını ve üzerine gelindiğinde değişen rengini belirler.
    - **Alt Bilgi (Footer) Stil Kuralları** : Alt bilgi bölümünün arka plan rengini, metin rengini ve hizalamasını belirler.

Bu örnek, web geliştirme projelerinizde HTML ve CSS'nin nasıl birlikte kullanılacağını ve her iki dosyanın nasıl yapılandırılacağını göstermektedir. Bu yapıyı kullanarak, daha karmaşık ve stilize web sayfaları oluşturabilirsiniz.
