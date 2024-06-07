# CSS Variables 

CSS değişkenleri, diğer adıyla CSS özel özellikleri, stil sayfalarınızı daha sürdürülebilir ve esnek hale getirmenin güçlü bir yoludur. Bu özellikler, CSS içinde değerleri saklamanızı ve bu değerleri yeniden kullanmanızı sağlar, böylece tek bir değeri değiştirerek tüm örnekleri güncellemek kolaylaşır. Bu eğitimde, CSS değişkenlerinin nasıl kullanılacağına dair kapsamlı bir inceleme yapılacak ve örnek kodlarla desteklenecektir.

## Adım 1: CSS Değişkeni Tanımlama

İlk olarak, özel özelliğinizi tanımlamanız gerekecektir. Bu genellikle belgenizin en üst seviyesini temsil eden `:root` seçicisi içinde yapılır. Bu, değişkeni küresel olarak kullanılabilir hale getirir.

Örneğin:

```css
:root {
    --primary-color: #3498db;
    --secondary-color: #2ecc71;
    --font-size: 16px;
}
```

Bu örnekte, `--primary-color` , `--secondary-color` ve `--font-size` adında üç değişken tanımlanmıştır. Bu değişkenler, tüm CSS dosyası boyunca kullanılabilir.

## Adım 2: CSS Değişkeni Kullanma

Bir CSS değişkenini kullanmak için `var()` fonksiyonunu kullanmanız gerekecektir. İşte tanımladığımız değişkenlerin nasıl kullanılacağına dair bir örnek:

```css
body {
    background-color: var(--primary-color);
    color: var(--secondary-color);
    font-size: var(--font-size);
}
```

Bu kodda, `body` elementinin arka plan rengi `--primary-color` değişkeninden, metin rengi `--secondary-color` değişkeninden ve yazı tipi boyutu `--font-size` değişkeninden alınmaktadır.

## Adım 3: Varsayılan Değerler

CSS değişkenleri için varsayılan değerler de tanımlanabilir. Bu, değişkenin tanımlanmadığı durumlarda bir yedek değerin kullanılmasını sağlar. Bu özellik, CSS'in daha esnek ve dayanıklı olmasını sağlar.

Örneğin:

```css
body {
    color: var(--main-color, black);
}
```

Bu kodda, `--main-color` değişkeni tanımlanmamışsa, metin rengi siyah ( `black` ) olacaktır.

## CSS Değişkenlerinin Avantajları

1. **Bakım Kolaylığı** : Tek bir merkezi konumdan değişiklik yaparak tüm stil sayfasını güncellemek kolaylaşır.
2. **Kod Tekrarının Azaltılması** : Değişkenler, aynı değeri birden çok yerde kullanmayı sağlar, bu da kod tekrarını azaltır.
3. **Temalar ve Özelleştirmeler** : CSS değişkenleri, temaların ve kullanıcı tercihlerine göre özelleştirmelerin kolayca uygulanmasını sağlar.

## Sonuç

CSS değişkenleri, stil sayfalarınızı daha sürdürülebilir, esnek ve yönetilebilir hale getirir. Bu eğitimde, CSS değişkenlerinin tanımlanması, kullanılması ve dinamik olarak güncellenmesi üzerinde durulmuştur. Bu özellikleri kullanarak, daha temiz ve verimli CSS kodları yazabilirsiniz.

---

Bu eğitim, CSS değişkenlerinin temel ve ileri düzey kullanımlarını kapsayan kapsamlı bir rehber sunmayı amaçlamaktadır. Sorularınız veya ek açıklamalarınız için lütfen iletişime geçin.
