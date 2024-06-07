## CSS 3D Transform

Bu bölümde, CSS 3D dönüşümlerinin nasıl uygulanacağını gösteren kapsamlı bir örnek sunacağız. Örneğimiz, HTML ve CSS dosyalarını ayrı tutarak, iyi bir uygulama yapısını gösterecek. Ayrıca, bir `section` ve `footer` ekleyerek, dönüşümlerle zenginleştirilmiş tam bir web sayfası oluşturacağız.

### HTML Dosyası: `index.html`

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS 3D Dönüşümler</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>CSS 3D Dönüşümler</h1>
    </header>
    <section class="content">
        <div class="cube">
            <div class="face front">Ön</div>
            <div class="face back">Arka</div>
            <div class="face left">Sol</div>
            <div class="face right">Sağ</div>
            <div class="face top">Üst</div>
            <div class="face bottom">Alt</div>
        </div>
    </section>
   
</body>
</html>
```

### CSS Dosyası: `styles.css`

```css
body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    margin: 0;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

header {
    background-color: #333;
    color: #fff;
    padding: 1em;
    text-align: center;
}

.content {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
    perspective: 1000px;
}

.cube {
    position: relative;
    width: 200px;
    transform-style: preserve-3d;
    transform: rotateX(20deg) rotateY(30deg);
    animation: rotateCube 10s infinite linear;
}

@keyframes rotateCube {
    from {
        transform: rotateX(20deg) rotateY(0);
    }
    to {
        transform: rotateX(20deg) rotateY(360deg);
    }
}

.face {
    position: absolute;
    width: 200px;
    height: 200px;
    background-color: rgba(255, 255, 255, 0.9);
    border: 1px solid #ccc;
    line-height: 200px;
    text-align: center;
    font-size: 20px;
    font-weight: bold;
}

.front  { transform: translateZ(100px); }
.back   { transform: rotateY(180deg) translateZ(100px); }
.left   { transform: rotateY(-90deg) translateZ(100px); }
.right  { transform: rotateY(90deg) translateZ(100px); }
.top    { transform: rotateX(90deg) translateZ(100px); }
.bottom { transform: rotateX(-90deg) translateZ(100px); }


```

### Açıklama

Bu örnekte, bir 3D küp oluşturduk ve her yüzeyine farklı bir metin ekledik. Küpün dönüş hareketini `rotateX` ve `rotateY` yöntemlerini kullanarak sağladık. Ayrıca, `perspective` özelliği ile 3D dönüşümün derinlik etkisini belirledik.

- **HTML Yapısı:**
  - `header`: Sayfanın başlık bölümünü içerir.
  - `section`: İçeriği barındıran ana bölüm. Bu bölümde 3D küpümüz bulunur.


- **CSS Yapısı:**
  - `body`: Sayfanın genel stilini tanımlar.
  - `header` ve `footer`: Başlık ve alt bilgi bölümlerinin stillerini belirler.
  - `.content`: 3D dönüşümler için perspektifi tanımlar.
  - `.cube`: Küpün temel dönüşümlerini ve animasyonlarını tanımlar.
  - `.face`: Küpün her bir yüzeyinin stilini tanımlar.

### 3D Dönüşüm Özellikleri

- **perspective:** 3D dönüşümler için derinlik efektini ayarlar.
- **transform-style: preserve-3d;**: Çocuk elemanların 3D dönüşümlerini korur.
- **transform:** Elemanlara dönüşüm uygular.
- **@keyframes:** Animasyonları tanımlar.

Bu örnek, CSS 3D dönüşümlerinin nasıl uygulanabileceğini ve web sayfalarına nasıl dinamik ve etkileşimli özellikler kazandırılabileceğini gösterir. Kod yapısı ve açıklamalarıyla birlikte, bu örnek size kendi projelerinizde kullanabileceğiniz bir temel sağlar.