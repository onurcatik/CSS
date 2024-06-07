### HTML ve CSS ile CSS Seçicilerin Uygulanması: Kapsamlı Bir Örnek

Aşağıda, HTML ve CSS dosyalarının nasıl ayrıldığını ve CSS seçicilerinin nasıl kullanıldığını gösteren kapsamlı bir örnek bulunmaktadır. Bu örnek, HTML yapısını ve CSS seçicilerini detaylı bir şekilde ele almaktadır.

#### HTML Dosyası ( `index.html` )

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Seçiciler Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header id="header">
        <h1 class="intro">Hoşgeldiniz</h1>
    </header>
    <section>
        <h2 class="intro">Giriş Bölümü</h2>
        <p>Bu, CSS seçicilerini açıklayan bir örnek dosyadır.</p>
        <p class="highlight">Bu paragraf özel olarak vurgulanmıştır.</p>
    </section>
    <footer>
        <p>&copy; 2024 CSS Seçiciler Örneği</p>
    </footer>
</body>

</html>
```

#### CSS Dosyası ( `styles.css` )

```css
/* Element Seçici */
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
}

/* ID Seçici */
#header {
    background-color: grey;
    color: white;
    padding: 20px 0;
    text-align: center;
}

/* Class Seçici */
.intro {
    font-size: 24px;
    font-weight: bold;
    color: navy;
}

/* Class Seçici */
.highlight {
    background-color: yellow;
    padding: 10px;
    border: 1px solid orange;
}

/* Grup Seçici */
h1,
h2,
p {
    margin-bottom: 20px;
}

/* Evrensel Seçici */
* {
    box-sizing: border-box;
}

/* Bağımlı Seçici */
section p {
    color: red;
}
```

### Açıklama

#### HTML Yapısı

HTML dosyası, `<!DOCTYPE html>` bildirimiyle başlar ve temel HTML yapısını içerir. `<head>` etiketinde, karakter seti, viewport ayarları ve CSS dosyasına link verilmiştir. `<body>` etiketinde, örnek içeriği barındıran `<header>` , `<section>` , ve `<footer>` etiketleri bulunmaktadır.

#### CSS Seçicileri

1. **Element Seçici:** `body` etiketi için genel stil ayarları yapılmıştır.
   

```css
   body {
       font-family: Arial, sans-serif;
       line-height: 1.6;
   }
```

2. **ID Seçici:** `#header` ID'sine sahip öğe için stil ayarları yapılmıştır.
   

```css
   #header {
       background-color: grey;
       color: white;
       padding: 20px 0;
       text-align: center;
   }
```

3. **Class Seçici:** `.intro` ve `.highlight` class'ına sahip öğeler için stil ayarları yapılmıştır.
   

```css
   .intro {
       font-size: 24px;
       font-weight: bold;
       color: navy;
   }

   .highlight {
       background-color: yellow;
       padding: 10px;
       border: 1px solid orange;
   }
```

4. **Grup Seçici:** `h1`, `h2`, ve `p` etiketleri için ortak stil ayarları yapılmıştır.
   

```css
   h1,
   h2,
   p {
       margin-bottom: 20px;
   }
```

5. **Evrensel Seçici:** Tüm öğeler için box model ayarı yapılmıştır.
   

```css
   * {
       box-sizing: border-box;
   }
```

6. **Bağımlı Seçici:** Sadece `<section>` içinde bulunan `<p>` etiketleri için stil ayarları yapılmıştır.
   

```css
   section p {
       color: red;
   }
```

Bu örnek, HTML ve CSS'in nasıl birlikte çalıştığını ve CSS seçicilerinin nasıl kullanıldığını kapsamlı bir şekilde göstermektedir. Her bir seçici türü, belirli bir amaca hizmet eder ve stil uygulamalarını daha etkili hale getirir. Bu tür bir yapı, web sayfalarının stilizasyonunda esneklik ve kontrol sağlar.
