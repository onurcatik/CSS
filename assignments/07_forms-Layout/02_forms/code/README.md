## CSS Form Elements

Bu bölümde, form elemanlarının stilize edilmesiyle ilgili detaylı bir örnek sunacağız. HTML ve CSS kodlarını ayrı dosyalar halinde yazacağız. Ayrıca, `header` , `section` , ve `footer` etiketleri kullanarak sayfanın yapısını oluşturacağız.

### HTML Dosyası (index.html)

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Form Elements</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>CSS Form Elemanları</h1>
    </header>
    <section>
        <h2>Giriş Elemanları</h2>
        <form>
            <label for="fname">Ad:</label><br><br>
            <input type="text" id="fname" name="fname" placeholder="Adınızı girin"><br><br>

            <label for="lname">Soyad:</label><br><br>
            <input type="text" id="lname" name="lname" placeholder="Soyadınızı girin"><br><br>

            <label for="email">Email:</label><br><br>
            <input type="email" id="email" name="email" placeholder="example@example.com"><br><br>

            <label for="options">Seçenekler:</label><br><br>
            <select id="options" name="options">
                <option value="option1">Seçenek 1</option>
                <option value="option2">Seçenek 2</option>
                <option value="option3">Seçenek 3</option>
            </select><br><br>

            <input type="checkbox" id="chk1">
            <label for="chk1">Seçenek 1</label><br><br>

            <input type="radio" id="rad1" name="rad">
            <label for="rad1">Seçenek A</label><br><br>

            <input type="radio" id="rad2" name="rad">
            <label for="rad2">Seçenek B</label><br><br>

            <input type="submit" value="Gönder">
        </form>
    </section>
    <footer>
        <p>&copy; 2024 CSS Form Elemanları Örneği</p>
    </footer>
</body>

</html>
```

### CSS Dosyası (styles.css)

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #4CAF50;
    color: white;
    text-align: center;
    padding: 1em 0;
}

section {
    padding: 2em;
    background-color: #fff;
    margin: 2em auto;
    width: 80%;
    max-width: 600px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h1,
h2 {
    color: #333;
}

label {
    display: block;
    margin-bottom: 0.5em;
    color: #333;
}

input[type="text"],
input[type="email"],
select {
    width: 100%;
    padding: 10px;
    margin-bottom: 1em;
    border: 2px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
}

input[type="text"]:focus,
input[type="email"]:focus,
select:focus {
    border-color: #4CAF50;
    box-shadow: 0 0 5px rgba(76, 175, 80, 0.5);
    outline: none;
}

input::placeholder {
    color: #888;
    font-style: italic;
}

input[type="checkbox"],
input[type="radio"] {
    display: none;
}

input[type="checkbox"]+label,
input[type="radio"]+label {
    position: relative;
    padding-left: 25px;
    cursor: pointer;
    display: inline-block;
    color: #333;
}

input[type="checkbox"]+label:before,
input[type="radio"]+label:before {
    content: "";
    position: absolute;
    left: 0;
    top: 0;
    width: 20px;
    height: 20px;
    border: 2px solid #4CAF50;
    border-radius: 4px;
    background-color: #fff;
}

input[type="radio"]+label:before {
    border-radius: 50%;
}

input[type="checkbox"]:checked+label:before,
input[type="radio"]:checked+label:before {
    background-color: #4CAF50;
}

input[type="checkbox"]:checked+label:after {
    content: "\2713";
    position: absolute;
    left: 5px;
    top: 2px;
    font-size: 16px;
    color: #fff;
}

input[type="radio"]:checked+label:after {
    content: "";
    position: absolute;
    left: 6px;
    top: 6px;
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background-color: #fff;
}

select {
    background-color: #fff;
    appearance: none;
    -webkit-appearance: none;
    -moz-appearance: none;
    background-image: url('data:image/svg+xml;charset=US-ASCII,%3csvg xmlns%3d%22http%3a//www.w3.org/2000/svg%22 width%3d%2229%22 height%3d%2216%22 viewBox%3d%220 0 29 16%22%3e%3cpath fill%3d%22%234CAF50%22 d%3d%22M14.5 16L0 0h29z%22/%3e%3c/svg%3e');
    background-repeat: no-repeat;
    background-position: right 10px top 50%;
}

footer {
    text-align: center;
    padding: 1em 0;
    background-color: #4CAF50;
    color: white;
    position: fixed;
    width: 100%;
    bottom: 0;
}
```

### Açıklama

Bu örnek, form elemanlarını stilize etmek için kullanılan CSS tekniklerini kapsamaktadır. Her bir form elemanının CSS ile nasıl şekillendirileceğini göstermektedir. 

#### HTML Yapısı

* `header`: Sayfa başlığı ve tanıtım kısmı.
* `section`: Form elemanlarını içeren ana içerik bölümü.
* `footer`: Sayfanın alt bilgisi.

#### CSS Özellikleri

* `body`: Genel sayfa stilini belirler, arka plan rengi ve yazı tipi ayarları içerir.
* `header`,  `section`,  `footer`: Sayfa bölümlerinin stilini belirler, renkler ve hizalamalar ayarlanır.
* `input[type="text"]`,  `input[type="email"]`,  `select`: Giriş elemanlarının genel stilini belirler, kenarlıklar, dolgu ve odaklandığında değişen stiller eklenir.
* `input::placeholder`: Yer tutucu metnin stilini belirler.
* `input[type="checkbox"]`,  `input[type="radio"]`: Özel onay kutuları ve radyo düğmelerinin stilini belirler.

Bu yapı ve stil ayarları, kullanıcı deneyimini iyileştirmek ve formun görsel çekiciliğini artırmak için kullanılır. CSS ile form elemanlarının nasıl daha estetik ve kullanıcı dostu hale getirileceğini bu örnekle göstermiş olduk.
