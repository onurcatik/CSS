# CSS Grid Container

## Giriş

CSS Grid Layout, iki boyutlu bir düzen sistemi sağlayarak modern web tasarımına devrim niteliğinde bir katkı sağlamaktadır. Grid Layout, satır ve sütunlara dayalı karmaşık düzenlerin kolayca oluşturulmasına imkan verir. Bu rehberde, bir HTML öğesini grid konteyner olarak nasıl tanımlayacağımızı ve ilgili CSS özelliklerini detaylı bir şekilde ele alacağız.

## Grid Konteyner

Bir HTML öğesini grid konteyner olarak tanımlamak için `display` özelliğini `grid` veya `inline-grid` olarak ayarlamanız gerekmektedir. Bu ayar, öğenin çocuklarını grid ögeleri olarak tanımlar.

```css
.container {
    display: grid;
}
```

## Grid-Template-Columns Özelliği

`grid-template-columns` özelliği, grid düzeninizdeki sütunların sayısını ve her bir sütunun genişliğini tanımlar. Bu özellik, sütun genişliklerini piksel, yüzde veya fr (fractional) birimlerinde belirlemenize olanak tanır.

```css
.container {
    display: grid;
    grid-template-columns: 100px 200px 1fr;
}
```

Yukarıdaki örnekte, ilk sütun 100 piksel, ikinci sütun 200 piksel ve üçüncü sütun ise kalan alanın tamamını kaplar.

## Grid-Template-Rows Özelliği

`grid-template-rows` özelliği, grid düzeninizdeki satırların yüksekliğini tanımlar. Bu özellik de sütunlarda olduğu gibi, satır yüksekliklerini piksel, yüzde veya fr birimlerinde belirlemenize imkan tanır.

```css
.container {
    display: grid;
    grid-template-rows: 50px 1fr 2fr;
}
```

Bu örnekte, ilk satır 50 piksel yüksekliğinde, ikinci satır kalan alanın bir bölümünü ve üçüncü satır ise iki bölümünü kaplar.

## Justify-Content Özelliği

`justify-content` özelliği, tüm grid içeriğinin yatay eksende konteyner içinde nasıl hizalanacağını belirler. Olası değerler `start`, `end`, `center`, `space-between`, `space-around`, ve `space-evenly` şeklindedir.

```css
.container {
    display: grid;
    justify-content: center;
}
```

Bu örnek, tüm grid içeriğinin yatay olarak merkeze hizalanmasını sağlar.

## Align-Content Özelliği

`align-content` özelliği, tüm grid içeriğinin dikey eksende konteyner içinde nasıl hizalanacağını belirler. Olası değerler `start`, `end`, `center`, `space-between`, `space-around`, ve `space-evenly` şeklindedir.

```css
.container {
    display: grid;
    align-content: center;
}
```

Bu örnek, tüm grid içeriğinin dikey olarak merkeze hizalanmasını sağlar.

## Sonuç

CSS Grid Layout, karmaşık ve esnek web düzenleri oluşturmak için güçlü bir araçtır. Bu rehberde, bir HTML öğesini grid konteyner olarak tanımlamanın ve grid düzeninin temel özelliklerini ele aldık. Bu özellikler, modern ve kullanıcı dostu web siteleri tasarlamak için güçlü bir temel sağlar.

