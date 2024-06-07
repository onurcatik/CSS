# CSS Syntax

CSS (Cascading Style Sheets), web sayfalarının görünümünü ve düzenini tanımlamak için kullanılan stil dilidir. CSS kuralları, seçici ve bildirim bloğundan oluşur. Bu kılavuzda, CSS kurallarının temel yapı taşlarını, doğru ve detaylı bir şekilde ele alacağız. Belirli terimler ve yapıların nasıl kullanıldığını adım adım inceleyeceğiz.

## CSS Kuralı Nedir?

Bir CSS kuralı iki ana bileşenden oluşur:

1. **Seçici (Selector)** : Stil uygulamak istediğiniz HTML öğesini belirtir.
2. **Bildirim Bloğu (Declaration Block)** : Stilin nasıl uygulanacağını belirler.

Bildirim bloğu, küme parantezleri `{}` içine alınmış bir veya daha fazla stil özelliği ve değer çifti içerir. Her bildirim, noktalı virgülle `;` sonlandırılır.

Örnek bir CSS kuralı:

```css
h1 {
    color: blue;
    font-size: 12px;
}
```

Bu örnekte `h1` seçici, başlık 1 elemanını hedefler. Bildirim bloğu ise `color` ve `font-size` özelliklerini içerir.

## Tek Özellik Bildirimi

Tek bir özellik bildirimi, yalnızca bir stil özelliği ve değeri içerir. Örneğin:

```css
p {
    color: red;
}
```

Bu kural, tüm `<p>` (paragraf) elemanlarının metin rengini kırmızı yapar.

## Birden Fazla Özellik Bildirimi

Bir bildirim bloğu birden fazla özellik ve değer içerebilir. Örneğin:

```css
div {
    width: 100px;
    height: 100px;
    background-color: yellow;
}
```

Bu kural, tüm `<div>` elemanlarının genişliğini 100 piksel, yüksekliğini 100 piksel ve arka plan rengini sarı yapar.

## Seçiciler

CSS'de birkaç farklı seçici türü vardır:

1. **Evrensel Seçici** : Tüm öğeleri seçer.

```css
    * {
        margin: 0;
        padding: 0;
    }
```

2. **Tür Seçici** : Belirli bir HTML öğesi türünü seçer.

```css
    h1 {
        font-weight: bold;
    }
```

3. **Sınıf Seçici** : Belirli bir sınıfı olan öğeleri seçer. Nokta (`.`) ile başlar.

```css
    .highlight {
        background-color: yellow;
    }
```

4. **ID Seçici** : Belirli bir ID'ye sahip öğeleri seçer. Kare işareti (`#`) ile başlar.

```css
    #main {
        width: 80%;
    }
```

5. **Ayrılmış Seçiciler** : Seçicileri daha belirgin yapmak için birleştirilmiş türler.

```css
    p.intro {
        font-size: 14px;
    }
```

## Özellikler ve Değerler

CSS'de çok sayıda özellik vardır ve her özellik, belirli değer türlerini kabul eder. En yaygın özelliklerden bazıları:

* `color`: Metin rengini ayarlar. Renk ismi, hex değeri veya rgb değeri olabilir.

```css
    color: blue;
    color: #0000FF;
    color: rgb(0, 0, 255);
```

* `font-size`: Metin boyutunu ayarlar. Piksel, yüzde veya em cinsinden olabilir.

```css
    font-size: 16px;
    font-size: 1em;
```

* `margin`: Dış boşlukları ayarlar. Dört kenar için ayrı ayrı değerler verilebilir.

```css
    margin: 10px;
    margin-top: 10px;
    margin-right: 5px;
```

* `padding`: İç boşlukları ayarlar.

```css
    padding: 20px;
    padding-left: 15px;
```

## CSS Doğruluğu ve Yaygın Hatalar

CSS yazarken yaygın hatalardan kaçınmak önemlidir:

1. **Yanlış Sözdizimi** : CSS kuralları yanlış yazıldığında tarayıcı tarafından görmezden gelinebilir.

```css
    p {
        color blue
    }

    /* Yanlış: Eksik iki nokta üst üste */
```

2. **Çakışan Kurallar** : Aynı öğe için birden fazla kural tanımlandığında, en son tanımlanan kural geçerli olur.

```css
    p {
        color: red;
    }

    p {
        color: blue;
    }

    /* Bu kural geçerli olur */
```

3. **Öncelik Sorunları** : CSS'de öncelik sırasına dikkat edilmelidir. ID seçiciler sınıf seçicilerden daha yüksek önceliğe sahiptir.

```css
    .example {
        color: green;
    }

    #example {
        color: red;
    }

    /* ID seçici daha yüksek önceliğe sahiptir */
```

## Sonuç

* Bu kılavuz, CSS sözdiziminin temel yapı taşlarını ve yaygın hatalardan kaçınma yollarını ele almaktadır.
* CSS kurallarının doğru uygulanması, web sayfalarınızın profesyonel ve tutarlı görünmesini sağlar.
