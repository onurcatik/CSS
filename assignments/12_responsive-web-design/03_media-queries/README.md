## Media Queries

### Giriş

CSS3 ile tanıtılan medya sorguları, belirli bir koşul doğru olduğunda bir dizi CSS özelliğini içeren bir blok eklemek için kullanılan bir tekniktir. Bu teknik, modern web geliştirme ve özellikle duyarlı web tasarımı (responsive web design) için kritik öneme sahiptir.

Medya sorguları, ekran genişliği, çözünürlük, cihaz yönelimi gibi özelliklere göre farklı stiller uygulamaya olanak tanır. Bu doküman, medya sorgularının temel kavramlarını, kullanım alanlarını ve en iyi uygulama örneklerini detaylandırarak, konuyu bilimsel bir yaklaşımla ele alacaktır.

### Kavram ve Kullanım

Medya sorguları, `@media` kuralı ile kullanılır. Bu kural, belirli bir koşul sağlandığında uygulanacak CSS özelliklerini tanımlar. Aşağıda bir medya sorgusunun temel yapısı gösterilmektedir:

```css
@media only screen and (max-width: 600px) {
    body {
        background-color: lightblue;
    }
}
```

Yukarıdaki örnekte, ekran genişliği 600 pikselden küçük olduğunda `body` elementi için arka plan rengi `lightblue` olarak ayarlanacaktır.

### Kavram

Medya sorguları, CSS kodlarını belirli medya türlerine ve koşullarına göre uygulamayı sağlar. Örneğin, sadece ekranlar için geçerli olan stilleri tanımlayabilir veya belirli bir çözünürlüğün altındaki ekranlar için farklı düzenlemeler yapabilirsiniz.

#### Örnek:

```css
@media only screen and (min-width: 768px) {
    .container {
        width: 750px;
    }
}

@media only screen and (max-width: 767px) {
    .container {
        width: 100%;
    }
}
```

Bu örnekte, `.container` sınıfına sahip elemanların genişliği, ekran genişliğine bağlı olarak değişmektedir. Ekran genişliği 768 piksel veya daha büyükse, genişlik 750 piksel olarak ayarlanırken, daha küçük ekranlarda yüzde olarak ayarlanır.

### Duyarlı Web Tasarımı - Görseller ve Videolar

Görseller ve videoların duyarlı hale getirilmesi, medya sorgularının yaygın kullanım alanlarından biridir. Bu bölümde, görsel ve videoların genişlik ve yükseklik özelliklerini kullanarak nasıl duyarlı hale getirilebileceğini inceleyeceğiz.

#### Genişlik Özelliğini Kullanma

Eğer genişlik özelliği bir yüzde olarak ayarlanır ve yükseklik otomatik olarak ayarlanırsa, görsel duyarlı hale gelir ve ölçeklenir.

```css
img {
    width: 50%;
    height: auto;
}
```

#### Maksimum Genişlik Özelliğini Kullanma

Maksimum genişlik özelliği `%100` olarak ayarlandığında, görsel gerekli olduğunda küçülür ancak orijinal boyutundan daha büyük olmaz.

```css
img {
    max-width: 100%;
    height: auto;
}
```

### Medya Sorgularının Avantajları

Medya sorgularının kullanılması, kullanıcı deneyimini iyileştirir ve farklı cihazlar arasında tutarlılık sağlar. Duyarlı tasarım, kullanıcıların mobil cihazlar, tabletler ve masaüstü bilgisayarlar gibi farklı cihazlarda web sitelerini rahatça görüntülemelerini sağlar.

### Sonuç

Medya sorguları, modern web geliştirme için vazgeçilmez bir araçtır. Duyarlı web tasarımı oluşturmak, kullanıcı deneyimini iyileştirir ve web sitelerinin erişilebilirliğini artırır. Bu dokümanda, medya sorgularının temel kavramlarını ve uygulamalarını ele aldık. Doğru ve etkili kullanım, web projelerinizin başarısını artıracaktır.

Bu bilgiler, CSS medya sorguları konusunda kapsamlı bir anlayış sağlar ve bu alanda uzmanlaşmak isteyen geliştiricilere rehberlik eder.