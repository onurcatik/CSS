# CSS Table

## Giriş

Bu eğitimde, CSS kullanarak tabloların nasıl stilize edileceğini ayrıntılı bir şekilde inceleyeceğiz. Bu eğitimde ele alınacak konular arasında tablo sınırları, tablo boyutu, yatay ve dikey hizalama, ve tablo stili bulunmaktadır. Tüm konular bilimsel ve profesyonel bir dil ile ele alınacak olup, herhangi bir hatalı bilgi kritik bir şekilde ele alınacaktır.

## Tablo Sınırları

Tablo sınırlarını belirlemek için CSS'te `border` özelliği kullanılır. Bu özellik, tabloların hücrelerinin çevresindeki çizgileri belirlemek için kullanılır. Örneğin:

```css
table, th, td {
  border: 1px solid black;
}
```

Bu kod, tüm tablo, başlık hücreleri (`<th>`) ve veri hücreleri (`<td>`) için siyah renkte 1 piksel genişliğinde katı çizgiler oluşturur.

## Tablo Boyutu

Tabloların genişliği ve yüksekliği `width` ve `height` özellikleri ile tanımlanır. Bu özellikler, tabloların boyutlarını belirlemek için kullanılır. Örneğin:

```css
table {
  width: 100%;
  height: 300px;
}
```

Bu kod, tablonun genişliğini konteynerinin tamamını kaplayacak şekilde (`%100`) ve yüksekliğini 300 piksel olarak ayarlar.

## Yatay Hizalama

Tablo içeriğinin yatay hizalaması `text-align` özelliği ile ayarlanır. Bu özellik, içeriklerin sol, sağ veya ortada hizalanmasını sağlar. Örneğin:

```css
th, td {
  text-align: center;
}
```

Bu kod, tablo başlık hücreleri (`<th>`) ve veri hücreleri (`<td>`) içindeki içeriğin ortalanmasını sağlar.

## Dikey Hizalama

Tablo içeriğinin dikey hizalaması `vertical-align` özelliği ile ayarlanır. Bu özellik, içeriklerin üst, alt veya ortada hizalanmasını sağlar. Örneğin:

```css
th, td {
  vertical-align: middle;
}
```

Bu kod, tablo başlık hücreleri (`<th>`) ve veri hücreleri (`<td>`) içindeki içeriğin dikey olarak ortalanmasını sağlar.

## Tablo Stili

Tablo içerisindeki hücrelerin sınırı ile içerik arasındaki boşluğu kontrol etmek için `padding` özelliği kullanılır. Bu özellik, hücrelerdeki içerik ile hücre sınırları arasındaki boşluğu ayarlamak için kullanılır. Örneğin:

```css
th, td {
  padding: 10px;
}
```

Bu kod, tablo başlık hücreleri (`<th>`) ve veri hücreleri (`<td>`) için 10 piksel dolgu uygular.

## CSS ile Tabloların Oluşturulması

Tablolar, web sayfalarında verileri düzenli ve anlaşılır bir şekilde sunmak için kullanılır. HTML ve CSS kullanarak tabloları oluşturmak ve stilize etmek mümkündür. Bu bölümde, adım adım bir tablo oluşturmayı ve CSS ile stil vermeyi öğreneceksiniz.

## 1. HTML ile Tablonun Yapılandırılması

İlk olarak, HTML kullanarak temel bir tablo oluşturacağız. İşte örnek bir tablo yapısı:

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
</body>
</html>
```

Bu HTML kodu, bir tablo (`<table>`) içerir ve başlık (`<thead>`) ve veri satırlarını (`<tbody>`) tanımlar. `<th>` elemanları tablo başlıklarını, `<td>` elemanları ise tablo verilerini temsil eder.

## 2. CSS ile Tabloya Stil Verme

Tablonun görünümünü güzelleştirmek ve daha kullanışlı hale getirmek için CSS kullanacağız. İşte tabloya uygulanacak bazı temel CSS stilleri:

```css
/* styles.css dosyasında yer alacak */
table {
    width: 100%;
    border-collapse: collapse;
}

th, td {
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
```

- `table` elementi için `width: 100%;` özelliği tabloyu konteynerinin tamamına yayar.
- `border-collapse: collapse;` özelliği, hücre sınırlarının birleşmesini sağlar ve daha kompakt bir görünüm oluşturur.
- `th, td` seçicileri ile tablo başlıkları ve veri hücreleri için sınır (`border`), dolgu (`padding`), ve hizalama (`text-align`) ayarlanır.
- `th` elementi için arka plan rengi (`background-color`) ayarlanarak başlık hücreleri vurgulanır.
- `tbody tr:nth-child(even)` seçici ile çift satırlara arka plan rengi verilerek satırların daha kolay ayırt edilmesi sağlanır.

## 3. Tamamlanmış Örnek

Aşağıda, HTML ve CSS bir arada kullanılarak oluşturulmuş tamamlanmış bir tablo örneği bulunmaktadır:

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tablo Örneği</title>
    <style>
        table {
            width: 100%;
            border-collapse: collapse;
        }

        th, td {
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
    </style>
</head>
<body>
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
</body>
</html>
```

Bu örnek, basit ve okunabilir bir tablo oluşturmak için gerekli adımları göstermektedir. Tabloyu ihtiyaçlarınıza göre daha fazla stil ve işlevsellik ekleyerek geliştirebilirsiniz.

## Özet

Bu eğitimde, CSS kullanarak tabloların nasıl stilize edileceğini öğrendik. Tablo sınırlarını belirlemek için `border` özelliğini, tablo boyutlarını ayarlamak için `width` ve `height` özelliklerini, içeriğin yatay hizalaması için `text-align` ve dikey hizalaması için `vertical-align` özelliklerini ve hücreler arası boşluğu kontrol etmek için `padding` özelliğini inceledik. Bu temel bilgiler, CSS ile tablolarınızı daha çekici ve işlevsel hale getirmenize yardımcı olacaktır.