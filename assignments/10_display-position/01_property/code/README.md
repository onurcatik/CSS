# CSS Display Property

Bu bölümde, CSS'de çeşitli `display` özellik değerlerinin kullanımını gösteren, bir bölüm ve bir altbilgi içeren yapılandırılmış bir düzen içindeki HTML öğelerine uygulanan ayrıntılı bir örnek sunulmaktadır.
## HTML Structure

Bir üstbilgi, çeşitli öğeler içeren bir bölüm ve bir altbilgi ile temel bir HTML yapısı oluşturacağız. Bu, farklı `display` özellik değerlerinin düzeni nasıl etkilediğini göstermeye yardımcı 
olacaktır.

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Display Property Example</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>CSS Display Property Örneği</h1>
    </header>
    <section>
        <h2>Örnekler</h2>
        <div class="inline-example">Bu bir inline elementtir.</div>
        <div class="inline-block-example">Bu bir inline-block elementtir.</div>
        <div class="block-example">Bu bir block elementtir.</div>
        <div class="none-example">Bu element görünmeyecek.</div>
        <div class="hidden-example">Bu element gizlenmiş, ancak hala yer kaplamaktadır.</div>
        <div class="flex-container">
            <div class="flex-item">Flex Item 1</div>
            <div class="flex-item">Flex Item 2</div>
            <div class="flex-item">Flex Item 3</div>
        </div>
        <div class="grid-container">
            <div class="grid-item">Grid Item 1</div>
            <div class="grid-item">Grid Item 2</div>
            <div class="grid-item">Grid Item 3</div>
            <div class="grid-item">Grid Item 4</div>
        </div>
        <div class="table-example">
            <div class="table-row">Satır 1</div>
            <div class="table-row">Satır 2</div>
        </div>
    </section>
    <footer>
        <p>Bu, footer alanıdır.</p>
    </footer>
</body>

</html>
```

## CSS Styling

HTML öğelerini biçimlendirmek ve farklı `display` özellik değerlerini göstermek için CSS kodu aşağıda verilmiştir.

```css
/* styles.css */

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header,
footer {
    background-color: #f8f9fa;
    text-align: center;
    padding: 20px;
}

section {
    padding: 20px;
}

h1,
h2 {
    color: #333;
}

/* Display inline */
.inline-example {
    display: inline;
    background-color: #e7f3fe;
    padding: 10px;
    border: 1px solid #b3d4fc;
}

/* Display inline-block */
.inline-block-example {
    display: inline-block;
    background-color: #dff0d8;
    padding: 10px;
    border: 1px solid #c3e6cb;
    width: 200px;
    height: 100px;
}

/* Display block */
.block-example {
    display: block;
    background-color: #f2dede;
    padding: 10px;
    border: 1px solid #ebccd1;
    width: 100%;
    margin-top: 10px;
}

/* Display none */
.none-example {
    display: none;
}

/* Visibility hidden */
.hidden-example {
    visibility: hidden;
    background-color: #fcf8e3;
    padding: 10px;
    border: 1px solid #faebcc;
    margin-top: 10px;
}

/* Flex container */
.flex-container {
    display: flex;
    background-color: #f5f5f5;
    padding: 10px;
    border: 1px solid #ddd;
    margin-top: 10px;
}

.flex-item {
    background-color: #d9edf7;
    padding: 20px;
    border: 1px solid #bce8f1;
    margin-right: 10px;
}

/* Grid container */
.grid-container {
    display: grid;
    grid-template-columns: auto auto;
    background-color: #f5f5f5;
    padding: 10px;
    border: 1px solid #ddd;
    margin-top: 10px;
}

.grid-item {
    background-color: #dff0d8;
    padding: 20px;
    border: 1px solid #c3e6cb;
    margin: 5px;
}

/* Display table */
.table-example {
    display: table;
    width: 100%;
    background-color: #f9f9f9;
    border: 1px solid #ccc;
    margin-top: 10px;
}

.table-row {
    display: table-row;
    background-color: #e9ecef;
    padding: 10px;
    border: 1px solid #dee2e6;
}
```

## Explanation

### header ve footer

* **header** ve **footer** elementleri, sayfanın başlık ve alt bilgi bölümlerini tanımlar. Bu elementler genellikle sabit içerik barındırır ve tüm sayfa boyunca aynı kalır.
  

### section

* **section** elementi, sayfa içeriğini mantıksal bölümlere ayırır. Her bir bölüm, belirli bir konuya veya işlevselliğe odaklanabilir.

### inline, inline-block ve block

* **inline** : Element satır içi olarak görüntülenir. Yükseklik ve genişlik değerleri etkisizdir.
* **inline-block** : Element satır içi blok olarak görüntülenir. Yükseklik ve genişlik değerleri uygulanabilir.
* **block** : Element blok olarak görüntülenir ve yeni bir satırda başlar, tüm genişliği kaplar.

### none ve visibility: hidden

* **display: none** : Element tamamen kaldırılır ve sayfa düzenini etkilemez.
* **visibility: hidden** : Element gizlenir, ancak hala yer kaplar ve sayfa düzenini etkiler.

### flex ve grid

* **flex** : Esnek konteyner oluşturur. İçindeki çocuk elemanlar esnek kutular olarak düzenlenir.
* **grid** : Grid konteyner oluşturur. İçindeki çocuk elemanlar grid öğeleri olarak düzenlenir.

### table

* **display: table** : Element tablo gibi görüntülenir. İçindeki çocuk elemanlar tablo satırları olarak düzenlenir.

Bu örnekler, CSS display property'nin farklı değerlerinin bir web sayfasının düzenini nasıl etkilediğini net bir şekilde gösterir. Doğru kullanıldığında, bu özellikler web tasarımında büyük esneklik ve kontrol sağlar.
