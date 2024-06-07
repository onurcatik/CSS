# CSS Form Elements

CSS (Cascading Style Sheets), HTML (Hypertext Markup Language) ile birlikte, web sayfalarının stilini belirlemede temel bir rol oynar. CSS formları, kullanıcı girdilerini toplamak ve genellikle bir sunucuya işlenmek üzere göndermek için kullanılır. Bu eğitim, CSS kullanarak form elemanlarının nasıl stilize edileceğini ayrıntılı bir şekilde açıklamaktadır.

## 1. Bordered Inputs (Kenarlıklı Girdiler)

CSS kullanarak, giriş elemanlarının (input) kenarlıklarını değiştirebilir, boyutlarını ve renklerini ayarlayabilir ve yuvarlatılmış köşeler ekleyebilirsiniz. Bu, kullanıcı deneyimini iyileştirmek ve formların görsel çekiciliğini artırmak için önemlidir.

### Örnek 1:

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bordered Input</title>
    <style>
        input {
            border: 2px solid #4CAF50;
            border-radius: 4px;
            padding: 10px;
            width: 300px;
        }
    </style>
</head>

<body>
    <form>
        <label for="fname">Ad:</label><br><br>
        <input type="text" id="fname" name="fname"><br><br>
        <input type="submit" value="Gönder">
    </form>
</body>

</html>
```

Yukarıdaki kodda, `input` elemanlarına 2 piksel genişliğinde ve yeşil renkte bir kenarlık eklenmiştir. Ayrıca, köşeler 4 piksel yarıçapında yuvarlatılmıştır.

## 2. Focused Inputs (Odaklanmış Girdiler)

Odaklandığında stilini değiştiren giriş alanları, kullanıcıların hangi alanın aktif olduğunu anlamasına yardımcı olur.

### Örnek 2:

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Focused Input</title>
    <style>
        input {
            border: 2px solid #ccc;
            border-radius: 4px;
            padding: 10px;
            width: 300px;
        }

        input:focus {
            border-color: #4CAF50;
            box-shadow: 0 0 5px rgba(76, 175, 80, 0.5);
            outline: none;
        }
    </style>
</head>

<body>
    <form>
        <label for="lname">Soyad:</label><br><br>
        <input type="text" id="lname" name="lname"><br><br>
        <input type="submit" value="Gönder">
    </form>
</body>

</html>
```
Bu örnekte, `input:focus` seçici kullanılarak odaklandığında kenarlık rengi değiştirilmiş ve kutuya bir gölge eklenmiştir. `outline: none;` ifadesi, tarayıcının varsayılan odak çerçevesini kaldırır.

## 3. Placeholder Styling (Yer Tutucu Stil)

Yer tutucular (placeholders), kullanıcıya ne tür veri girmesi gerektiği hakkında ipucu verir. CSS ile yer tutucuların stilini değiştirmek mümkündür.

### Örnek 3:

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Placeholder Styling</title>
    <style>
        input::placeholder {
            color: #888;
            font-style: italic;
        }
    </style>
</head>

<body>
    <form>
        <label for="email">Email:</label><br><br>
        <input type="email" id="email" name="email" placeholder="example@example.com"><br><br>
        <input type="submit" value="Gönder">
    </form>
</body>

</html>
```

Bu örnekte, `input::placeholder` seçici kullanılarak yer tutucunun rengi ve yazı stili değiştirilmiştir.

## 4. Custom Checkboxes and Radio Buttons (Özel Onay Kutuları ve Radyo Düğmeleri)

CSS ile varsayılan onay kutuları ve radyo düğmelerinin yerine özel tasarımlar kullanılabilir.

### Örnek 4:

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Custom Checkboxes and Radio Buttons</title>
    <style>
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
    </style>
</head>

<body>
    <form>
        <input type="checkbox" id="chk1">
        <label for="chk1">Seçenek 1</label><br><br>
        <input type="radio" id="rad1" name="rad">
        <label for="rad1">Seçenek A</label><br><br>
        <input type="radio" id="rad2" name="rad">
        <label for="rad2">Seçenek B</label><br><br>
        <input type="submit" value="Gönder">
    </form>
</body>

</html>
```

Bu örnekte, `input[type="checkbox"]` ve `input[type="radio"]` elemanları gizlenmiş ve yerlerine stilize edilmiş `label` elemanları kullanılmıştır.

## 5. Styling Select Boxes (Seçim Kutularını Stilize Etme)

CSS ile seçim kutularının (select) stilini değiştirmek, formun genel estetiğini iyileştirebilir.

### Örnek 5:

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Styled Select Box</title>
    <style>
        select {
            width: 300px;
            padding: 10px;
            border: 2px solid #4CAF50;
            border-radius: 4px;
            background-color: #fff;
            appearance: none;
            -webkit-appearance: none;
            -moz-appearance: none;
            background-image: url('data:image/svg+xml;charset=US-ASCII,%3csvg xmlns%3d%22http%3a//www.w3.org/2000/svg%22 width%3d%2229%22 height%3d%2216%22 viewBox%3d%220 0 29 16%22%3e%3cpath fill%3d%22%234CAF50%22 d%3d%22M14.5 16L0 0h29z%22/%3e%3c/svg%3e');
            background-repeat: no-repeat;
            background-position: right 10px top 50%;
        }
    </style>
</head>

<body>
    <form>
        <label for="options">Seçenekler:</label><br><br>
        <select id="options" name="options">
            <option value="option1">Seçenek 1</option>
            <option value="option2">Seçenek 2</option>
            <option value="option3">Seçenek 3</option>
        </select><br><br>
        <input type="submit" value="Gönder">
    </form>
</body>

</html>
```

