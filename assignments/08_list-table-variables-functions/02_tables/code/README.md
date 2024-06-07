### CSS Table

Bu örnekte, HTML ve CSS kullanarak tablo oluşturmayı ve stil vermeyi, ayrıca sayfaya ek olarak bir başlık (header), ana içerik (main content) bölümü ve alt bilgi (footer) eklemeyi öğreneceksiniz. HTML ve CSS kodlarını ayrı dosyalarda tutarak temiz ve düzenli bir yapı oluşturacağız.

#### HTML Dosyası (index.html)

Aşağıda, tabloları ve diğer sayfa bölümlerini içeren HTML dosyasının örneği verilmiştir:

```html
<!DOCTYPE html>
<html lang="tr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tablo Örneği</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header>
        <h1>Tablo Örneği</h1>
    </header>
    <section>
        <h2>Veri Tablosu</h2>
        <table>
            <thead>
                <tr>
                    <th>Başlık 1</th>
                    <th>Başlık 2</th>
                    <th>Başlık 3</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Veri 1</td>
                    <td>Veri 2</td>
                    <td>Veri 3</td>
                </tr>
                <tr>
                    <td>Veri 4</td>
                    <td>Veri 5</td>
                    <td>Veri 6</td>
                </tr>
            </tbody>
        </table>
    </section>
    <footer>
        <p>&copy; 2024 Örnek Şirket</p>
    </footer>
</body>

</html>
```

#### CSS Dosyası (styles.css)

Aşağıda, tablonun ve diğer sayfa bölümlerinin stilini içeren CSS dosyasının örneği verilmiştir:

```css
/* Genel Stil */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Başlık (Header) */
header {
    background-color: #4CAF50;
    color: white;
    padding: 20px;
    text-align: center;
}

/* Ana İçerik Bölümü (Section) */
section {
    padding: 20px;
}

/* Tablo Stili */
table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 20px;
}

th,
td {
    border: 1px solid black;
    padding: 8px;
    text-align: left;
}

th {
    background-color: #f2f2f2;
}

tbody tr:nth-child(even) {
    background-color: #f9f9f9;
}

/* Alt Bilgi (Footer) */
footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px 0;
    position: fixed;
    width: 100%;
    bottom: 0;
}
```

### Açıklama

1. **HTML Yapısı:** 
   - `header` : Sayfanın üst kısmında yer alan başlık bölümüdür. Burada sayfanın başlığı bulunur.
   - `section` : Ana içerik bölümü olup, burada veri tablosu yer alır.
   - `footer` : Sayfanın alt kısmında yer alan alt bilgi bölümüdür. Genellikle telif hakkı bilgileri gibi ek bilgiler içerir.

2. **CSS Stil Dosyası:** 
   - **Genel Stil:** `body` için yazı tipi, margin, padding ve kutu modeli ayarları yapılır.
   - **Başlık (Header):** `header` için arka plan rengi, yazı rengi, padding ve metin hizalaması ayarlanır.
   - **Ana İçerik Bölümü (Section):** `section` için padding ayarlanarak içeriğin kenarlardan boşluk bırakması sağlanır.
   - **Tablo Stili:** 

     - `table` için genişlik, sınırların birleşmesi (border-collapse) ve üst marj ayarlanır.
     - `th, td` için sınır, padding ve metin hizalaması belirlenir.
     - `th` için arka plan rengi ayarlanarak başlık hücreleri vurgulanır.
     - `tbody tr:nth-child(even)` seçici ile çift satırlara arka plan rengi verilerek satırların daha kolay ayırt edilmesi sağlanır.

   - **Alt Bilgi (Footer):** `footer` için arka plan rengi, yazı rengi, metin hizalaması, padding ve sabit konumlandırma (position: fixed) ayarlanır.

Bu örnek, HTML ve CSS kullanarak bir tablo oluşturmayı ve stil vermeyi, ayrıca sayfaya başlık ve alt bilgi eklemeyi kapsamlı bir şekilde gösterir. Tabloları ve diğer sayfa bölümlerini ihtiyaçlarınıza göre daha fazla stil ve işlevsellik ekleyerek geliştirebilirsiniz.
