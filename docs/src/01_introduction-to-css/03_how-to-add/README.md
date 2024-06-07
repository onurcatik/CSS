# CSS How to Add

Bu detaylı kılavuz, CSS'nin (Cascading Style Sheets) bir web sayfasına nasıl ekleneceğini kapsamlı ve titiz bir şekilde ele alacaktır. CSS eklemenin üç temel yolu vardır:

1. **Harici CSS (External CSS)** 
2. **Dahili CSS (Internal CSS)** 
3. **Satır İçi CSS (Inline CSS)** 

Bu yöntemlerin her biri, CSS'nin web sayfalarına eklenmesi ve yönetilmesi konusunda farklı avantajlar ve dezavantajlar sunar.

## Harici CSS (External CSS)

Harici stil sayfaları, birden fazla web sayfasının görünümünü tek bir dosyayı değiştirerek yönetmeyi mümkün kılar. Bu yöntem, büyük projelerde tutarlılığı sağlamak ve bakım sürecini kolaylaştırmak için idealdir. Harici CSS, `<link>` elementi kullanılarak tanımlanır ve genellikle `<head>` etiketi içerisinde bulunur.

**Örnek:** 

```html
<!DOCTYPE html>
<html>

<head>
    <link rel="stylesheet" type="text/css" href="styles.css">
</head>

<body>
    <h1>Harici CSS Örneği</h1>
</body>

</html>
```

Bu örnekte, `styles.css` dosyası tüm sayfanın stilini belirler.

## Dahili CSS (Internal CSS)

Dahili CSS, stil tanımlarının doğrudan HTML dosyasının `<head>` bölümünde bir `<style>` etiketi içerisinde tanımlanmasıyla oluşturulur. Bu yöntem, sadece tek bir sayfada stil uygulamak için kullanışlıdır.

**Örnek:** 

```html
<!DOCTYPE html>
<html>

<head>
    <style>
        body {
            background-color: lightblue;
        }

        h1 {
            color: navy;
        }
    </style>
</head>

<body>
    <h1>Dahili CSS Örneği</h1>
</body>

</html>
```

## Satır İçi CSS (Inline CSS)

Satır içi CSS, HTML elemanlarına doğrudan `style` özniteliği kullanılarak uygulanır. Bu yöntem, tek bir eleman için özel stil uygulamak gerektiğinde kullanılır. Ancak, kodun okunabilirliğini ve bakımını zorlaştırdığı için geniş çapta kullanımı önerilmez.

 **Örnek:** 

```html
<!DOCTYPE html>
<html>

<body>
    <h1 style="color:blue;text-align:center;">Satır İçi CSS Örneği</h1>
</body>

</html>
```

# CSS Öncelik Sırası (Priority of CSS)

CSS öncelik sırası, hangi stil tanımının uygulanacağını belirler. Genel kural, spesifik olan stilin daha az spesifik olana göre öncelikli olmasıdır:

1. **Satır İçi CSS (Inline CSS)** : En yüksek önceliğe sahiptir.
2. **Dahili CSS (Internal CSS)** : Orta düzey önceliğe sahiptir.
3. **Harici CSS (External CSS)** : En düşük önceliğe sahiptir.

Bir sayfada birden fazla stil sayfası tanımlanabilir. Bu durumda, spesifiklik ve kaynak düzeni dikkate alınarak stil kuralları uygulanır.

## Çakışan Kurallar

Bir stil kuralının birden fazla kaynaktan gelmesi durumunda, en yüksek önceliğe sahip olan kural uygulanır. Bu bağlamda, satır içi stil, dahili ve harici stillerden daha önce gelir. Örneğin, aynı eleman için hem dahili hem de harici stil tanımlandıysa, dahili stil geçerli olur.

 **Örnek:** 

```html
<!DOCTYPE html>
<html>

<head>
    <style>
        p {
            color: green;
        }
    </style>
    <link rel="stylesheet" type="text/css" href="styles.css">
</head>

<body>
    <p style="color: red;">Bu metin kırmızı renkte görünecektir.</p>
</body>

</html>
```

Bu örnekte, paragrafın rengi satır içi stil nedeniyle kırmızı olacaktır, dahili ve harici stil kurallarına rağmen.

# Sonuç

- Bu kılavuzda, CSS'nin bir web sayfasına eklenmesi için kullanılan üç temel yöntemi ve CSS öncelik sırasını inceledik. 
- CSS'nin doğru kullanımı, web sayfalarının stil yönetimini ve bakımını büyük ölçüde kolaylaştırır. 
- CSS kurallarının spesifiklik ve öncelik sırasını anlamak, karmaşık stil çatışmalarını önlemek ve tutarlı bir görünüm sağlamak için kritiktir.
