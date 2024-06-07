# CSS Selectors

CSS (Cascading Style Sheets) seçicileri, stil uygulamak istediğiniz HTML öğelerini bulmak veya seçmek için kullanılır. Bu dökümanda, CSS seçicilerini ele alarak, doğru ve bilimsel bir yaklaşımla inceleyeceğiz.

## Basit Seçiciler

Basit seçiciler, HTML öğelerini ad, id veya class'a göre seçer. Burada üç temel seçiciye odaklanacağız:

1. **Element Seçici** 
2. **ID Seçici** 
3. **Class Seçici** 

## 1. Element Seçici

Element seçici, HTML öğelerini element adına göre seçer. Örneğin, tüm `<p>` etiketlerini seçmek için `p` element seçicisini kullanabilirsiniz:

```css
p {
    color: blue;
}
```

Bu örnekte, tüm `<p>` öğeleri mavi renkte olacaktır.

## 2. ID Seçici

ID seçici, bir sayfa içerisindeki benzersiz bir öğeyi seçmek için kullanılır. ID seçiciyi kullanmak için, öğenin ID'sinden önce bir hash (#) karakteri yazılır. Örneğin, ID'si "header" olan bir öğeyi seçmek için şu şekilde kullanılır:

```css
#header {
    background-color: grey;
}
```

Bu örnekte, ID'si "header" olan öğenin arka plan rengi gri olacaktır. Unutulmamalıdır ki, her ID bir sayfa içerisinde benzersiz olmalıdır.

## 3. Class Seçici

Class seçici, belirli bir class attribute'üne sahip HTML öğelerini seçer. Class seçiciyi kullanmak için, class adından önce bir nokta (.) karakteri yazılır. Örneğin, class'ı "intro" olan tüm öğeleri seçmek için şu şekilde kullanılır:

```css
.intro {
    font-size: 16px;
}
```

Bu örnekte, class'ı "intro" olan tüm öğelerin yazı tipi boyutu 16 piksel olacaktır.

## ID ve Class Seçicilerinin Birlikte Kullanımı

ID ve class seçicileri aynı anda bir öğe üzerinde kullanılabilir. Örneğin:

```css
#header.intro {
    color: white;
}
```

Bu örnekte, ID'si "header" ve class'ı "intro" olan öğe beyaz renkte olacaktır.

## Ek CSS Seçicileri

Yukarıda ele alınan temel seçicilerin yanı sıra, CSS'de birçok başka seçici de bulunmaktadır. Bunlar şunlardır:

* **Grup Seçicileri:** Birden fazla öğeyi aynı anda seçmek için kullanılır.
  

```css
  h1,
  h2,
  p {
      margin-bottom: 10px;
  }
```

  Bu örnekte, `<h1>` , `<h2>` , ve `<p>` öğelerinin alt boşlukları 10 piksel olarak ayarlanmıştır.

* **Evrensel Seçici:** Tüm HTML öğelerini seçer.
  

```css
  * {
      box-sizing: border-box;
  }
```

  Bu örnekte, tüm öğelerin box model hesaplaması border-box olarak ayarlanmıştır.

* **Bağımlı Seçiciler:** Belirli bir yapıya sahip öğeleri seçer.
  

```css
  div p {
      color: red;
  }
```

  Bu örnekte, sadece `<div>` içindeki `<p>` öğeleri kırmızı renkte olacaktır.

## Sonuç

- CSS seçicileri, HTML öğelerini stilize etmek için güçlü araçlardır. 
- Element, ID ve class seçicileri, basit ve etkili seçici türleridir ve temel stil uygulamaları için yeterlidir. 
- Bununla birlikte, daha karmaşık stil gereksinimleri için diğer CSS seçicilerinin de bilinmesi önemlidir. 
- Bu dökümanda ele alınan bilgiler, CSS seçicilerinin temellerini anlamak ve doğru uygulamalar yapabilmek için sağlam bir temel oluşturacaktır.
