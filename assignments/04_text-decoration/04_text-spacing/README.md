## CSS Text Spacing

Bu belgede, CSS kullanarak metin boşlukları ve dönüşümleri hakkında ayrıntılı ve kapsamlı bir rehber sunulmaktadır. Ele alınan konular arasında metin girintisi, harf aralığı, satır yüksekliği, kelime aralığı ve beyaz boşluk bulunmaktadır.

### Metin Girintisi (text-indent)

`text-indent` özelliği, bir paragrafın ilk satırının girintisini belirlemek için kullanılır. Bu özellik, metnin daha okunabilir ve estetik bir şekilde düzenlenmesine yardımcı olur. Negatif değerler, metnin ilk satırının sola doğru kaydırılmasını sağlar.
#### Kullanım Örneği:

```css
p {
    text-indent: 50px;
}
```

Bu örnekte, paragrafın ilk satırı 50 piksel içeriden başlar.

### Harf Aralığı (letter-spacing)

`letter-spacing` özelliği, metindeki karakterler arasındaki boşluğu belirlemek için kullanılır. Bu özellik, metnin daha geniş veya daha sıkı görünmesini sağlamak amacıyla kullanılabilir.

#### Kullanım Örneği:

```css
p {
    letter-spacing: 2px;
}
```

Bu örnekte, paragraf metnindeki her karakter arasında 2 piksel boşluk bırakılır.

### Satır Yüksekliği (line-height)

`line-height` özelliği, satırlar arasındaki boşluğu belirlemek için kullanılır. Bu özellik, metnin daha okunabilir olmasını sağlar ve farklı satırlar arasındaki boşluğu ayarlamak için kullanılır.

#### Kullanım Örneği:

```css
p {
    line-height: 1.5;
}
```

Bu örnekte, satır yüksekliği normal satır yüksekliğinin 1.5 katıdır.

### Kelime Aralığı (word-spacing)

`word-spacing` özelliği, metindeki kelimeler arasındaki boşluğu belirlemek için kullanılır. Bu özellik, metnin daha geniş veya daha sıkı görünmesini sağlamak amacıyla kullanılabilir.

#### Kullanım Örneği:

```css
p {
    word-spacing: 4px;
}
```

Bu örnekte, paragraf metnindeki her kelime arasında 4 piksel boşluk bırakılır.

### Beyaz Boşluk (white-space)

`white-space` özelliği, metindeki boşlukların nasıl ele alınacağını belirler. Bu özellik, metindeki boşluk karakterlerinin korunmasını veya göz ardı edilmesini sağlar ve metnin sarılma (wrap) davranışını kontrol eder.

#### Kullanım Örneği:

```css
p {
    white-space: nowrap;
}
```

Bu örnekte, metin satır sonunda sarılmaz ve tek bir satırda devam eder.

### Sonuç

Bu rehber, CSS kullanarak metin boşluklarını ve dönüşümlerini nasıl kontrol edebileceğinizi ayrıntılı bir şekilde ele almıştır. Her bir özellik, metnin görünümünü ve okunabilirliğini iyileştirmek için kullanılabilir. Metin girintisi, harf aralığı, satır yüksekliği, kelime aralığı ve beyaz boşluk özellikleri, web sayfalarınızda metin düzenlemelerini optimize etmenize yardımcı olacaktır.


