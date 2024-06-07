## CSS Transitions

CSS geçişleri, belirli bir süre boyunca CSS özellik değerlerini yumuşak bir şekilde değiştirmeyi sağlar. Bu eğitimde aşağıdaki konuları öğreneceğiz:

- transition-property
- transition-duration
- transition-delay
- transition-timing-function
- transition

### transition-property

`transition-property` özelliği, geçiş efektinin hangi CSS özelliği için geçerli olduğunu belirtir. Belirtilen CSS özelliği değiştiğinde geçiş efekti başlar.

```css
.example {
  transition-property: background-color;
}
```

Bu örnekte, `background-color` özelliği değiştiğinde geçiş efekti uygulanacaktır.

### transition-duration

`transition-duration` özelliği, bir geçiş efektinin tamamlanmasının ne kadar süreceğini belirtir. Süre saniye (s) veya milisaniye (ms) cinsinden tanımlanır.

```css
.example {
  transition-duration: 2s;
}
```

Bu örnekte, geçiş efekti 2 saniye sürecektir.

### transition-delay

`transition-delay` özelliği, geçiş efektinin ne zaman başlayacağını belirtir. Değer saniye (s) veya milisaniye (ms) cinsinden tanımlanır.

```css
.example {
  transition-delay: 1s;
}
```

Bu örnekte, geçiş efekti 1 saniye gecikmeyle başlayacaktır.

### transition-timing-function

`transition-timing-function` özelliği, geçiş efektinin hız eğrisini belirtir. Bu, geçiş efektinin nasıl bir hızla ilerleyeceğini tanımlar.

```css
.example {
  transition-timing-function: ease-in-out;
}
```

Bu örnekte, geçiş efekti yavaş başlayacak, hızlanacak ve sonra tekrar yavaşlayacaktır.

### transition

`transition` özelliği, aşağıdaki dört özelliğin kısayoludur:

- transition-property
- transition-duration
- transition-timing-function
- transition-delay

```css
.example {
  transition: background-color 2s ease-in-out 1s;
}
```

Bu örnekte, `background-color` özelliği 1 saniye gecikme ile başlayacak, 2 saniye sürecek ve `ease-in-out` hız eğrisi ile geçiş yapacaktır.

### Sonuç

CSS geçişleri, web sayfalarındaki animasyonları ve etkileşimleri daha pürüzsüz ve kullanıcı dostu hale getirmek için güçlü araçlardır. Geçiş özelliklerini dikkatlice kullanarak, kullanıcı deneyimini artırabilir ve web sayfanıza dinamik bir görünüm kazandırabilirsiniz.

Bu eğitimin sonunda, CSS geçişlerinin temel özelliklerini ve nasıl kullanılacaklarını öğrendiniz. Daha ayrıntılı bilgi ve örnekler için ilgili kaynaklara başvurabilirsiniz.