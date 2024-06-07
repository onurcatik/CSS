# CSS Text

CSS (Cascading Style Sheets), web sayfalarını biçimlendirmek için kullanılan güçlü bir araçtır. Bu kılavuzda, metin biçimlendirme ile ilgili CSS özelliklerini kapsamlı ve detaylı bir şekilde ele alacağız. 

## Metin Rengi ve Arka Plan Rengi

CSS, metin rengini ve arka plan rengini ayarlamak için çeşitli özellikler sunar. Metin rengini ayarlamak için `color` özelliği kullanılırken, arka plan rengini ayarlamak için `background-color` özelliği kullanılır. Bu özellikler, metnin ve arka planın görsel olarak öne çıkmasını sağlamak için kritik öneme sahiptir.

```css
p {
    color: blue;
    background-color: yellow;
}
```

Bu örnekte, `<p>` etiketindeki metin mavi renkte ve arka planı sarı renkte olacak şekilde ayarlanmıştır.

## Metin Hizalama

Metni yatay olarak hizalamak için `text-align` özelliği kullanılır. Bu özellik, metnin sol, sağ, merkez veya her iki yana yaslanmasını sağlar.

* **Sol Hizalama (Varsayılan)** : Metin sola yaslanır.
* **Sağ Hizalama** : Metin sağa yaslanır.
* **Merkez Hizalama** : Metin ortalanır.
* **İki Yana Yaslama (Justify)** : Metin, her iki kenara yaslanır ve satırlar arasındaki boşluklar eşitlenir.

```css
p.left {
    text-align: left;
}

p.right {
    text-align: right;
}

p.center {
    text-align: center;
}

p.justify {
    text-align: justify;
}
```

## Son Satırın Hizalanması

`text-align-last` özelliği, metnin son satırının hizalanma şeklini belirler. Bu özellik, özellikle iki yana yaslama uygulandığında son satırın hizalanmasını kontrol etmek için kullanılır.

```css
p {
    text-align: justify;
    text-align-last: right;
}
```

Bu örnekte, metin iki yana yaslanmış ancak son satır sağa hizalanmıştır.

## Dikey Hizalama

Dikey hizalama, `vertical-align` özelliği kullanılarak yapılır. Bu özellik, genellikle tablo hücrelerindeki içerikleri veya satır içi elemanları dikey olarak hizalamak için kullanılır.

```css
span {
    vertical-align: middle;
}
```

## Metin Dönüşümü ve Dekorasyonu

CSS, metin dönüşümü ( `text-transform` ) ve dekorasyonu ( `text-decoration` ) gibi metin üzerinde daha fazla kontrol sağlayan özellikler sunar.

* **Metin Dönüşümü** : `text-transform` özelliği, metni büyük harfe, küçük harfe veya her kelimenin ilk harfini büyük yapabilir.

```css
p.uppercase {
    text-transform: uppercase;
}

p.lowercase {
    text-transform: lowercase;
}

p.capitalize {
    text-transform: capitalize;
}
```

* **Metin Dekorasyonu** : `text-decoration` özelliği, metne altı çizgi, üstü çizgi veya üstü çarpı işareti gibi dekoratif çizgiler ekleyebilir.

```css
p.underline {
    text-decoration: underline;
}

p.overline {
    text-decoration: overline;
}

p.line-through {
    text-decoration: line-through;
}
```

## Harf ve Kelime Aralığı

Harf aralığı ( `letter-spacing` ) ve kelime aralığı ( `word-spacing` ) özellikleri, metin içindeki harfler ve kelimeler arasındaki boşluğu kontrol eder.

```css
p {
    letter-spacing: 2px;
    word-spacing: 4px;
}
```

Bu örnekte, harfler arasındaki boşluk 2 piksel, kelimeler arasındaki boşluk ise 4 piksel olarak ayarlanmıştır.

## Satır Yüksekliği

`line-height` özelliği, metin satırlarının yüksekliğini belirler ve metin bloklarının okunabilirliğini artırır.

```css
p {
    line-height: 1.5;
}
```

Bu ayar, metin satırlarının yüksekliğini metin boyutunun 1.5 katı yapar.

# Sonuç

CSS'in metin biçimlendirme özellikleri, web sayfalarının görsel estetiğini ve okunabilirliğini önemli ölçüde artırır. Bu kılavuzda ele alınan özellikler, metinlerinizi profesyonel ve etkileyici bir şekilde sunmanıza yardımcı olacaktır. 
