# CSS Fonts

Web siteniz için doğru yazı tipini seçmek önemlidir. Yazı tipleri, bir web sitesinin genel estetiğini ve kullanılabilirliğini büyük ölçüde etkileyebilir. Bu nedenle, CSS ile yazı tiplerinin nasıl kullanılacağını ve özelleştirileceğini anlamak, profesyonel ve etkili bir web geliştirme süreci için kritiktir.

## CSS font-family Özelliği

`font-family` özelliği, bir öğe için yazı tipini belirtmek amacıyla kullanılır. Bu özellik, bir yazı tipi ailesi adı veya bir liste halinde alternatif yazı tipleri içerebilir. Alternatif yazı tipleri, belirli bir yazı tipi kullanılamadığında yedek olarak devreye girer. Bu özellik, yazı tipi ailesinin adlarını virgüllerle ayrılmış bir liste olarak alır.

Örnek:

```css
body {
    font-family: "Arial", "Helvetica", sans-serif;
}
```

Burada, tarayıcı "Arial" yazı tipini bulamazsa "Helvetica"yı dener ve son çare olarak genel `sans-serif` yazı tipini kullanır.

## CSS Web Güvenli Yazı Tipleri

Tamamen web güvenli yazı tipleri olmasa da, bazı yazı tipleri çoğu kullanıcı tarafından desteklenir. Ancak, her zaman yazı tipi bulunamadığında veya doğru yüklenemediğinde kullanılacak yedek yazı tiplerini eklemek önemlidir. Bu, `font-family` özelliğinde bir dizi benzer "yedek yazı tipi" ekleyerek yapılır. Bu yedekleme, listenin sonuna genel bir yazı tipi ailesi adı eklenerek tamamlanmalıdır.

Örnek:

```css
h1 {
    font-family: "Times New Roman", Times, serif;
}
```

## CSS font-style Özelliği

`font-style` özelliği, metnin italik olup olmayacağını belirtir. Bu özelliğin üç değeri vardır:

* `normal`: Metin normal gösterilir.
* `italic`: Metin italik olarak gösterilir.
* `oblique`: Metin eğik (italik benzeri) olarak gösterilir ancak daha az desteklenir.

Örnek:

```css
p {
    font-style: italic;
}
```

## Font Ağırlığı

`font-weight` özelliği, bir yazı tipinin kalınlığını belirtir. Yaygın olarak kullanılan değerler şunlardır:

* `normal` veya `400`: Normal yazı ağırlığı.
* `bold` veya `700`: Kalın yazı ağırlığı.

Örnek:

```css
h2 {
    font-weight: bold;
}
```

## Font Varyantı

`font-variant` özelliği, bir metnin küçük büyük harflerle mi gösterileceğini belirtir. Örneğin, `small-caps` değeri, tüm küçük harfleri büyük harf boyutunda, ama küçük harf biçiminde gösterir.

Örnek:

```css
h3 {
    font-variant: small-caps;
}
```

## Font Boyutu

`font-size` özelliği, metnin boyutunu ayarlamak için kullanılır. CSS'de yazı tipi boyutları mutlak (px, pt) veya göreli (% , em, rem) birimlerle belirtilebilir.

Örnek:

```css
p {
    font-size: 16px;
}
```

## CSS Google Fonts

Standart HTML yazı tiplerini kullanmak istemiyorsanız, Google Fonts'u kullanabilirsiniz. Google Fonts, geniş bir yazı tipi yelpazesi sunar ve kullanımı oldukça kolaydır. Google Fonts kullanmak için `<head>` bölümüne özel bir stil sayfası bağlantısı ekleyin ve ardından CSS'te yazı tipine referans verin.

Örnek:

```html
<head>
    <link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet">
</head>
<style>
    body {
        font-family: 'Roboto', sans-serif;
    }
</style>
```

Bu yöntemle, `Roboto` yazı tipini web sayfanızda kullanabilirsiniz.

Bu rehber, CSS ile yazı tiplerinin nasıl kullanıldığını ve özelleştirileceğini kapsamlı bir şekilde ele almıştır. Doğru yazı tipi seçimi ve kullanımı, web sitenizin profesyonel ve kullanıcı dostu görünmesini sağlayacaktır.
