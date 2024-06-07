## CSS Filter Property

### CSS Filter Özelliği

CSS `filter` özelliği, bir öğeye (genellikle `<img>` gibi) görsel efektler eklemek için kullanılır. Bu efektler arasında bulanıklık (blur) ve doygunluk (saturation) gibi işlemler yer alır.

#### Temel Kullanım

`filter` özelliği, bir HTML öğesinin görünümünü değiştiren çeşitli fonksiyonları içerir. Aşağıda bu fonksiyonlar ve kullanım örnekleri verilmiştir:

##### Bulanıklık (Blur)

Bulanıklık efekti, bir öğenin kenarlarını yumuşatmak için kullanılır. `blur()` fonksiyonu ile uygulanır ve piksel cinsinden bir yarıçap değeri alır. Örneğin:

```css
img {
  filter: blur(5px);
}
```

Bu kod, tüm `<img>` öğelerine 5 piksel yarıçapında bulanıklık efekti uygular.

##### Doygunluk (Saturation)

Doygunluk efekti, bir öğenin renk doygunluğunu ayarlamak için kullanılır. `saturate()` fonksiyonu ile uygulanır ve yüzde cinsinden bir değer alır. Örneğin:

```css
img {
  filter: saturate(150%);
}
```

Bu kod, tüm `<img>` öğelerinin renk doygunluğunu %150 yapar, yani renkleri daha canlı hale getirir.

#### Diğer Filter Fonksiyonları

`filter` özelliği, sadece blur ve saturate ile sınırlı değildir. Diğer önemli filter fonksiyonları şunlardır:

- **Grayscale**: Bir öğeyi siyah-beyaz yapmak için kullanılır.
  ```css
  img {
    filter: grayscale(100%);
  }
  ```

- **Sepia**: Bir öğeye sepya tonu ekler, yani kahverengi bir ton verir.
  ```css
  img {
    filter: sepia(100%);
  }
  ```

- **Brightness**: Bir öğenin parlaklığını ayarlamak için kullanılır.
  ```css
  img {
    filter: brightness(50%);
  }
  ```

- **Contrast**: Bir öğenin kontrastını ayarlamak için kullanılır.
  ```css
  img {
    filter: contrast(200%);
  }
  ```

- **Invert**: Bir öğenin renklerini tersine çevirir.
  ```css
  img {
    filter: invert(100%);
  }
  ```

#### Birden Fazla Filter Uygulamak

Bir öğeye birden fazla filter fonksiyonu uygulanabilir. Fonksiyonlar boşluk ile ayrılır. Örneğin:

```css
img {
  filter: blur(5px) saturate(150%);
}
```

Bu kod, tüm `<img>` öğelerine hem 5 piksel bulanıklık hem de %150 doygunluk uygular.

### Kritik Değerlendirme

PDF içeriğinde verilen bilgiler genel olarak doğru ve temel kullanımı kapsar. Ancak daha detaylı ve doğru bir bilgi sunumu için bazı eklemeler ve düzeltmeler gereklidir:

1. **Örnekteki Kod Blokları**: Kod örnekleri eksik veya hatalı olabilir. Her zaman çalışabilir kod örnekleri sağlamak önemlidir.
2. **Fonksiyonların Detayları**: Her fonksiyonun aldığı parametreler ve bu parametrelerin etkileri detaylı olarak açıklanmalıdır.
3. **Uyumluluk ve Performans**: Filter özelliklerinin tarayıcı uyumluluğu ve performans etkileri hakkında bilgi verilmelidir.

#### Özet

CSS `filter` özelliği, web geliştirme sürecinde görsel efektler eklemek için güçlü ve esnek bir araçtır. Doğru ve etkili kullanım, kullanıcı deneyimini artırabilir ve görsel olarak çekici web sayfaları oluşturulmasına yardımcı olabilir. Bu nedenle, her bir filter fonksiyonunun dikkatlice öğrenilmesi ve uygulanması önemlidir.

