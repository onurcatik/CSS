# CSS Resize Property

## Giriş

Bu belge, CSS `resize` özelliği üzerine kapsamlı ve detaylı bir rehber sunmaktadır. `resize` özelliği, bir öğenin kullanıcı tarafından yeniden boyutlandırılıp boyutlandırılamayacağını ve nasıl boyutlandırılacağını tanımlar. Bu özellik, yalnızca belirli durumlarda geçerlidir ve doğru kullanımı, web uygulamalarında daha iyi kullanıcı deneyimi sağlamak için kritiktir.

## Genel Bakış

`resize` özelliği, CSS'de bir öğenin yeniden boyutlandırılabilirliğini kontrol etmek için kullanılır. Bu özellik, özellikle metin alanları gibi kullanıcı giriş alanlarında kullanışlıdır.

### Uygulama Koşulları

* `resize` özelliği, yalnızca `overflow` özelliği "scroll", "auto" veya "hidden" olarak ayarlandığında geçerlidir. `overflow` özelliği "visible" olarak ayarlandığında `resize` özelliği çalışmaz.
* `resize` özelliği, satır içi (inline) öğelerde uygulanamaz.

### Değerler

`resize` özelliği şu değerlere sahiptir:
* `none`: Öğenin yeniden boyutlandırılamayacağını belirtir.
* `both`: Öğenin hem yatay hem de dikey olarak yeniden boyutlandırılabileceğini belirtir.
* `horizontal`: Öğenin yalnızca yatay olarak yeniden boyutlandırılabileceğini belirtir.
* `vertical`: Öğenin yalnızca dikey olarak yeniden boyutlandırılabileceğini belirtir.

### Kullanım Örnekleri

Aşağıdaki örnekler, `resize` özelliğinin nasıl kullanılacağını göstermektedir.

#### Örnek 1: `none` Değeri

```css
div {
    resize: none;
    overflow: auto;
}
```

Bu örnekte, `div` öğesi yeniden boyutlandırılamaz.

#### Örnek 2: `both` Değeri

```css
textarea {
    resize: both;
    overflow: auto;
}
```

Bu örnekte, `textarea` öğesi hem yatay hem de dikey olarak yeniden boyutlandırılabilir.

#### Örnek 3: `horizontal` Değeri

```css
div {
    resize: horizontal;
    overflow: auto;
}
```

Bu örnekte, `div` öğesi yalnızca yatay olarak yeniden boyutlandırılabilir.

#### Örnek 4: `vertical` Değeri

```css
div {
    resize: vertical;
    overflow: auto;
}
```

Bu örnekte, `div` öğesi yalnızca dikey olarak yeniden boyutlandırılabilir.

## Uygulamada Dikkat Edilmesi Gerekenler

1. **`overflow` Özelliği:** `resize` özelliğinin çalışabilmesi için `overflow` özelliğinin "scroll", "auto" veya "hidden" olarak ayarlandığından emin olunmalıdır.
2. **Satır İçi Öğeler:** `resize` özelliği satır içi öğelerde (örneğin,  `<span>`,  `<a>`) çalışmaz. Bu özelliği yalnızca blok veya blok seviyesindeki öğelerde kullanın.
3. **Kullanıcı Deneyimi:** Yeniden boyutlandırma işlevi, kullanıcı deneyimini olumlu veya olumsuz etkileyebilir. Bu nedenle, hangi öğelerin yeniden boyutlandırılabilir olacağını dikkatlice seçin.

## Sonuç

CSS `resize` özelliği, kullanıcıların web sayfalarındaki belirli öğeleri yeniden boyutlandırmasına olanak tanır ve kullanıcı deneyimini özelleştirme imkanı sunar. Bu özellik, doğru kullanıldığında web uygulamalarının etkileşimli ve esnek olmasını sağlar. Ancak, bu özelliği kullanırken dikkat edilmesi gereken kurallar ve kısıtlamalar göz önünde bulundurulmalıdır.

Bu rehberde, `resize` özelliğinin tüm yönleri ele alınmış ve doğru kullanım için gerekli bilgiler sunulmuştur. Bu bilgileri kullanarak web projelerinizde daha iyi kullanıcı deneyimleri oluşturabilirsiniz.
