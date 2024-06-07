## CSS Selector

### HTML ve CSS Yapısı

#### HTML Dosyası (`index.html`)

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Gelişmiş Seçiciler</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>CSS Gelişmiş Seçiciler</h1>
    </header>
    <section>
        <article>
            <h2>Element Seçici</h2>
            <p>Element seçici, HTML elemanlarını isimlerine göre seçer.</p>
        </article>
        <article id="uniqueArticle">
            <h2>ID Seçici</h2>
            <p>ID seçici, benzersiz bir ID'ye sahip elementleri seçer.</p>
        </article>
        <article class="exampleClass">
            <h2>Class Seçici</h2>
            <p>Class seçici, belirli bir sınıf özniteliğine sahip elementleri seçer.</p>
        </article>
        <article>
            <h2>Pseudo Sınıf</h2>
            <a href="#">Bir bağlantı</a>
        </article>
        <article>
            <h2>Pseudo Element</h2>
            <p>Bu paragrafın ilk satırı kalın olacak.</p>
        </article>
        <article>
            <h2>Özellik Seçici</h2>
            <input type="text" placeholder="Metin girişi">
        </article>
        <article>
            <h2>Evrensel Seçici</h2>
            <p>Tüm elementlerin margin ve padding değerleri sıfırlanır.</p>
        </article>
        <article>
            <h2>Birleştirici Seçiciler</h2>
            <div>
                <p>Descendant (Alt Eleman) Seçici</p>
                <p>Child (Çocuk) Seçici</p>
                <p>Adjacent Sibling (Bitişik Kardeş) Seçici</p>
                <p>General Sibling (Genel Kardeş) Seçici</p>
            </div>
        </article>
    </section>
    <footer>
        <p>&copy; 2024 CSS Gelişmiş Seçiciler</p>
    </footer>
</body>
</html>
```

#### CSS Dosyası (`styles.css`)

```css
/* Element Seçici */
h1 {
    text-align: center;
    color: navy;
}

/* ID Seçici */
#uniqueArticle {
    background-color: #f9f9f9;
    padding: 20px;
    border: 1px solid #ddd;
}

/* Class Seçici */
.exampleClass {
    font-size: 18px;
    color: #333;
}

/* Pseudo Sınıf */
a:hover {
    color: green;
}

/* Pseudo Element */
p::first-line {
    font-weight: bold;
}

/* Özellik Seçici */
input[type="text"] {
    background-color: yellow;
}

/* Evrensel Seçici */
* {
    margin: 0;
    padding: 0;
}

/* Birleştirici Seçiciler */

/* Descendant (Alt Eleman) Seçici */
div p {
    color: blue;
}

/* Child (Çocuk) Seçici */
div > p {
    background-color: #e3e3e3;
    padding: 10px;
    margin-bottom: 5px;
}

/* Adjacent Sibling (Bitişik Kardeş) Seçici */
h2 + p {
    margin-top: 0;
    font-style: italic;
}

/* General Sibling (Genel Kardeş) Seçici */
h2 ~ p {
    color: red;
}
```

### Açıklamalar

#### HTML Yapısı

- **header**: Başlık bölümünü içerir ve `<h1>` etiketi ile ana başlık belirlenir.
- **section**: İçerik bölümünü içerir ve her bir konu için ayrı `<article>` etiketleri kullanılır.
- **footer**: Alt bilgi bölümünü içerir ve telif hakkı bilgisi içerir.

#### CSS Kuralları

1. **Element Seçici**:
    - `h1` etiketi için yazı rengi ve hizalaması ayarlanır.
    
2. **ID Seçici**:
    - `#uniqueArticle` ID'sine sahip `<article>` elementi için arka plan rengi, padding ve border ayarlanır.

3. **Class Seçici**:
    - `.exampleClass` sınıfına sahip elementler için yazı boyutu ve rengi ayarlanır.

4. **Pseudo Sınıf**:
    - `a:hover` ile bağlantı üzerine fare getirildiğinde yazı rengi değiştirilir.

5. **Pseudo Element**:
    - `p::first-line` ile paragrafın ilk satırı kalın yazı tipi ile stilize edilir.

6. **Özellik Seçici**:
    - `input[type="text"]` ile `type` özniteliği `text` olan giriş alanları için arka plan rengi sarı olarak ayarlanır.

7. **Evrensel Seçici**:
    - `*` ile tüm elementlerin margin ve padding değerleri sıfırlanır.

8. **Birleştirici Seçiciler**:
    - `div p`: `div` elementinin altındaki tüm `p` elementlerinin yazı rengi mavi olarak ayarlanır.
    - `div > p`: `div` elementinin doğrudan çocukları olan `p` elementleri için arka plan rengi, padding ve margin ayarlanır.
    - `h2 + p`: Bir `h2` elementinden hemen sonra gelen `p` elementi için margin-top sıfırlanır ve yazı tipi eğik olur.
    - `h2 ~ p`: Bir `h2` elementinin tüm kardeşleri olan `p` elementleri için yazı rengi kırmızı olarak ayarlanır.

Bu örnek, CSS gelişmiş seçicilerini kullanarak nasıl stil oluşturulacağını ve bu seçicilerin HTML yapısında nasıl uygulanacağını detaylı bir şekilde açıklamaktadır.