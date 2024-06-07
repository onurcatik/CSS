### CSS Object-Fit Property

#### Giriş

CSS `object-fit` özelliği, bir `<img>` veya `<video>` elemanının konteynerine nasıl sığdırılacağını belirlemek için kullanılır. Bu özellik, görsellerin ve videoların yeniden boyutlandırılması sırasında içeriğin nasıl kesileceği veya genişletileceği konusunda kontrol sağlar.

#### Temel Kullanım

`object-fit` özelliği, aşağıdaki değerleri alabilir:

- `fill`: Varsayılan değerdir. İçeriği konteynere sığdırır ve gerektiğinde bozulmasına izin verir.
- `contain`: İçeriği konteynere sığdırır, ancak içeriğin en boy oranını korur.
- `cover`: Konteyneri tamamen doldurur, ancak içeriğin en boy oranını korur.
- `none`: İçeriğin boyutunu korur, ancak konteynerin boyutuna uymaz.
- `scale-down`: İçeriği ya `none` ya da `contain` gibi ölçeklendirir, hangisi daha küçükse onu kullanır.

#### Örnekler

##### `fill` Değeri

Bu değer, içeriği konteynere sığdırır ve gerektiğinde içeriğin bozulmasına izin verir.

```html
<img src="example.jpg" style="object-fit: fill; width: 300px; height: 200px;">
```

##### `contain` Değeri

Bu değer, içeriğin en boy oranını koruyarak konteynere sığdırır.

```html
<img src="example.jpg" style="object-fit: contain; width: 300px; height: 200px;">
```

##### `cover` Değeri

Bu değer, içeriğin en boy oranını koruyarak konteyneri tamamen doldurur.

```html
<img src="example.jpg" style="object-fit: cover; width: 300px; height: 200px;">
```

##### `none` Değeri

Bu değer, içeriğin boyutunu korur ve konteynerin boyutuna uymaz.

```html
<img src="example.jpg" style="object-fit: none; width: 300px; height: 200px;">
```

##### `scale-down` Değeri

Bu değer, içeriği ya `none` ya da `contain` gibi ölçeklendirir, hangisi daha küçükse onu kullanır.

```html
<img src="example.jpg" style="object-fit: scale-down; width: 300px; height: 200px;">
```

#### `object-position` Özelliği

`object-position` özelliği, `object-fit` özelliği ile birlikte kullanılarak, bir `<img>` veya `<video>` elemanının kendi içeriği içinde x/y koordinatları ile nasıl konumlandırılacağını belirler.

##### Örnek Kullanım

```html
<img src="example.jpg" style="object-fit: cover; object-position: top right; width: 300px; height: 200px;">
```

Yukarıdaki örnekte, görsel `cover` değeri ile konteyneri tamamen dolduracak şekilde ölçeklendirilmiştir ve içeriğin sağ üst köşesinde konumlandırılmıştır.

### Sonuç

CSS `object-fit` ve `object-position` özellikleri, görsellerin ve videoların bir web sayfasında nasıl gösterileceğini kontrol etmek için güçlü araçlardır. Bu özellikler, içeriğin kullanıcı deneyimini iyileştirecek şekilde esnek ve duyarlı olmasını sağlar. Bu nedenle, modern web geliştirme süreçlerinde bu özelliklerin doğru ve etkin kullanımı büyük önem taşır.