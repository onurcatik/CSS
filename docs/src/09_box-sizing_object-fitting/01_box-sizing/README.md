# CSS Box Sizing

CSS'de kutu boyutlandırma ( `box-sizing` ) özelliği, öğelerin genişlik ve yüksekliğini hesaplarken dolgu ( `padding` ) ve kenarlıkların ( `border` ) dahil edilip edilmediğini belirlememize olanak tanır. Bu özellik, tasarım sürecinde daha öngörülebilir ve tutarlı sonuçlar elde etmemize yardımcı olur.

## Temel Kullanım

`box-sizing` özelliğinin iki ana değeri vardır:

1. **content-box** : Bu varsayılan değerdir. Öğenin genişlik ve yüksekliği yalnızca içerik alanını kapsar. Dolgu ve kenarlıklar bu değerlere dahil edilmez.
2. **border-box** : Öğenin genişlik ve yüksekliği içerik, dolgu ve kenarlıkların tamamını kapsar.

### Örnekler

#### content-box (Varsayılan Değer)

```css
.element {
    width: 300px;
    height: 200px;
    padding: 20px;
    border: 10px solid black;
    box-sizing: content-box;
}
```

Yukarıdaki örnekte, `.element` sınıfına sahip öğenin toplam genişliği 300px (içerik) + 40px (dolgu) + 20px (kenarlık) = 360px, toplam yüksekliği ise 200px (içerik) + 40px (dolgu) + 20px (kenarlık) = 260px olacaktır.

#### border-box

```css
.element {
    width: 300px;
    height: 200px;
    padding: 20px;
    border: 10px solid black;
    box-sizing: border-box;
}
```

Bu örnekte, `.element` sınıfına sahip öğenin toplam genişliği ve yüksekliği 300px ve 200px olarak kalır çünkü dolgu ve kenarlık bu değerlere dahildir.

## Neden Kullanmalıyız?

`box-sizing: border-box;` kullanmanın ana avantajı, öğelerin toplam boyutlarını hesaplamayı ve kontrol etmeyi daha kolay hale getirmesidir. Bu, özellikle karmaşık düzenler oluştururken önemlidir. Modern tarayıcıların çoğu bu özelliği destekler ve CSS reset dosyalarında yaygın olarak kullanılır.

### CSS Reset Örneği

Birçok CSS reset dosyası, tüm öğelerde `box-sizing` özelliğini `border-box` olarak ayarlayarak başlar. Bu, tüm öğelerin aynı kutu boyutlandırma modelini kullanmasını sağlar ve tarayıcılar arası tutarlılığı artırır.

```css
/* CSS Reset */
*,
*::before,
*::after {
    box-sizing: border-box;
}
```

Bu kod, tüm öğeler ve onların `::before` ve `::after` pseudo-elementleri için `box-sizing` değerini `border-box` olarak ayarlar.

## Sonuç

CSS'de `box-sizing` özelliği, öğelerin toplam boyutlarını daha öngörülebilir ve yönetilebilir hale getirir. `border-box` değeri, özellikle karmaşık düzenler oluştururken ve farklı tarayıcılar arasında tutarlılığı sağlamak için çok yararlıdır. Bu özelliği doğru kullanarak, daha esnek ve bakım kolaylığı yüksek tasarımlar oluşturabilirsiniz.
