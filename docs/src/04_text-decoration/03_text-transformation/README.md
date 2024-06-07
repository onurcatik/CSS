# CSS Text Transformation

CSS (Cascading Style Sheets), web sayfalarının stil ve düzenini kontrol etmek için kullanılan bir stil dilidir. CSS, HTML ile birlikte kullanılarak web sayfalarının görünümünü ve özelleştirmek için güçlü bir araç sağlar. Bu kapsamlı ve detaylı öğretici, CSS'in metin dönüştürme (text transformation) özelliklerine odaklanacaktır.

## 1. Metin Dönüştürme Özellikleri (Text Transformation Properties)

CSS'in metin dönüştürme özellikleri, metnin büyük harf, küçük harf veya baş harflerin büyük harf olması gibi çeşitli şekillerde dönüştürülmesini sağlar. Bu özellikler, metnin görsel sunumunu değiştirmek için kullanılır, ancak metnin kendisini değiştirmez.

### a. text-transform Özelliği

`text-transform` özelliği, bir metnin büyük harf, küçük harf veya kelimelerin ilk harflerinin büyük harf yapılması gibi dönüştürmelerini belirtmek için kullanılır. Bu özellik aşağıdaki değerleri alabilir:

* **none** : Metin üzerinde herhangi bir dönüşüm uygulanmaz.
* **capitalize** : Her kelimenin ilk harfini büyük harf yapar.
* **uppercase** : Tüm harfleri büyük harf yapar.
* **lowercase** : Tüm harfleri küçük harf yapar.
* **initial** : Varsayılan değeri ayarlar.
* **inherit** : Üst öğenin text-transform değerini miras alır.

Örnek Kullanımlar:

```css
/* Tüm harfleri büyük harf yapar */
.uppercase {
    text-transform: uppercase;
}

/* Tüm harfleri küçük harf yapar */
.lowercase {
    text-transform: lowercase;
}

/* Her kelimenin ilk harfini büyük harf yapar */
.capitalize {
    text-transform: capitalize;
}
```

### Örnek Uygulamalar

1. **Uppercase Örneği:** 

HTML:

```html
<p class="uppercase">Bu bir örnek metindir.</p>
```

CSS:

```css
.uppercase {
    text-transform: uppercase;
}
```

Sonuç: "BU BİR ÖRNEK METİNDİR."

2. **Lowercase Örneği:** 

HTML:

```html
<p class="lowercase">Bu Bir Örnek Metindir.</p>
```

CSS:

```css
.lowercase {
    text-transform: lowercase;
}
```

Sonuç: "bu bir örnek metindir."

3. **Capitalize Örneği:** 

HTML:

```html
<p class="capitalize">bu bir örnek metindir.</p>
```

CSS:

```css
.capitalize {
    text-transform: capitalize;
}
```

Sonuç: "Bu Bir Örnek Metindir."

## 2. Bilimsel ve Teknik Değerlendirme

`text-transform` özelliği, web sayfalarının okunabilirliğini ve kullanıcı deneyimini artırmak için etkili bir araçtır. Ancak, bu özelliğin metin içeriğinin anlamını veya yapısını değiştirmediğini unutmamak önemlidir. Metin dönüştürme işlemleri, yalnızca metnin görsel sunumunu etkiler ve HTML veya veri katmanında herhangi bir değişiklik yapmaz.

## 3. Yanlış Anlaşılmalardan Kaçınma

Birçok geliştirici, `text-transform` özelliğini kullanırken, metinlerin veritabanlarında veya diğer veri depolarında nasıl saklandığını göz ardı edebilir. Bu nedenle, metin dönüştürme işlemlerinin yalnızca kullanıcı arayüzünde görsel bir değişiklik sağladığını ve arka planda metin verilerinin orijinal haliyle kaldığını vurgulamak önemlidir.

# 4. Sonuç

CSS `text-transform` özelliği, metinlerin büyük/küçük harf ve baş harflerin büyük harf yapılması gibi görsel dönüşümlerini kolaylaştırır. Bu öğreticide belirtilen kurallar ve örnekler, web geliştiricilerin metin dönüştürme işlemlerini doğru ve etkili bir şekilde uygulamalarına yardımcı olacaktır.
