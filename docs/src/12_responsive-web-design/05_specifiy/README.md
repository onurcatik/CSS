# CSS Specifiy

CSS özgüllük, web sayfasındaki bir elemente uygulanacak stil kurallarının belirlenmesinde önemli bir rol oynar. Birden fazla CSS kuralının aynı elemente işaret ettiği durumlarda, en yüksek özgüllük değerine sahip olan seçici "kazanır" ve stil beyanı bu HTML elementine uygulanır. Bu yazıda, CSS özgüllük kavramını detaylı bir şekilde ele alacağız ve özgüllüğün nasıl hesaplandığını açıklayacağız.

## Özgüllük Seviyelerini Tanımlayan Kategoriler

CSS seçicilerinin özgüllük seviyelerini dört ana kategoriye ayırabiliriz:

1. **Satır İçi Stiller (Inline Styles)**: Örnek: `<h1 style="color: pink;">`
2. **ID Seçicileri**: Örnek: `#navbar`
3. **Sınıflar, Pseudo-sınıflar, Özellik Seçicileri**: Örnek: `.test`, `:hover`, `[href]`
4. **Elementler ve Pseudo-elementler**: Örnek: `h1`, `:before`

### Not:

Bu kurala bir istisna vardır: `!important` kuralı kullanıldığında, satır içi stilleri bile geçersiz kılacaktır.

## Özgüllük Nasıl Hesaplanır?

Özgüllüğü hesaplamak için belirli bir yöntem kullanılır. Bu yöntemi ezberlemek, CSS kodunuzun beklediğiniz gibi çalışmasını sağlamak için önemlidir. Özgüllük hesaplaması şu şekilde yapılır:

- Başlangıç değeri olarak 0 alınır.
- Her bir ID değeri için 100 eklenir.
- Her bir sınıf değeri (veya pseudo-sınıf veya özellik seçici) için 10 eklenir.
- Her bir element seçici veya pseudo-element için 1 eklenir.

### Örnek:

Aşağıda bir özgüllük hesaplama örneği verilmiştir:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Özgüllük Örneği</title>
    <style>
        .example-class {
            color: blue;
        }
        #example-id {
            color: red;
        }
        h1 {
            color: green;
        }
        h1#example-id.example-class {
            color: yellow;
        }
    </style>
</head>
<body>
    <h1 id="example-id" class="example-class">Merhaba Dünya</h1>
</body>
</html>
```

Bu örnekte, `h1` elementi üzerinde hangi stilin uygulanacağını belirlemek için her bir seçicinin özgüllüğünü hesaplamamız gerekir:

- `.example-class` için özgüllük: 0-0-1 (class)
- `#example-id` için özgüllük: 0-1-0 (ID)
- `h1` için özgüllük: 0-0-1 (element)
- `h1#example-id.example-class` için özgüllük: 0-1-1 (ID + class + element)

En yüksek özgüllüğe sahip olan seçici `h1#example-id.example-class` (0-1-1) olduğundan, `h1` elementine `color: yellow;` stili uygulanacaktır.

## Özgüllük Hesaplamasında Dikkat Edilmesi Gerekenler

- **Satır içi stiller**, diğer tüm CSS kurallarından daha yüksek bir özgüllüğe sahiptir.
- **ID seçicileri**, sınıf seçicilerinden ve element seçicilerinden daha yüksek bir özgüllüğe sahiptir.
- **!important** kuralı**, her zaman özgüllük hesaplamasından bağımsız olarak en yüksek önceliğe sahiptir.

Bu bilgiler, CSS kodlarınızın beklediğiniz gibi çalışmasını sağlamak ve stil çakışmalarını önlemek için önemlidir. Doğru bir özgüllük hesaplaması, web sayfalarınızın tutarlı ve istenen şekilde görünmesini sağlar.

