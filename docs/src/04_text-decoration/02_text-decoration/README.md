# CSS Metin Süsleme (Text Decoration) Özellikleri

Bu kapsamlı ve detaylı rehberde, CSS metin süsleme (text decoration) özelliklerini ele alacağız. Bu rehberde yer alan konular şunlardır:

1. text-decoration-line
2. text-decoration-color
3. text-decoration-style
4. text-decoration-thickness
5. text-decoration

## 1. text-decoration-line

`text-decoration-line` özelliği, metne bir süsleme çizgisi eklemek için kullanılır. Bu özellik, metnin altını çizme, üstünü çizme veya üstünü kesme gibi dekoratif çizgiler eklemenizi sağlar. Aşağıdaki değerleri alabilir:

* `none`: Herhangi bir süsleme çizgisi eklenmez.
* `underline`: Metnin altına bir çizgi eklenir.
* `overline`: Metnin üstüne bir çizgi eklenir.
* `line-through`: Metnin ortasından bir çizgi geçer.

## Örnek Kullanım

```css
p {
    text-decoration-line: underline;
}
```

Yukarıdaki örnekte, `p` etiketine sahip metinlerin altı çizilecektir.

## 2. text-decoration-color

`text-decoration-color` özelliği, süsleme çizgisinin rengini belirlemek için kullanılır. Bu özellik, metin süslemesinin rengini ayarlamanızı sağlar.

## Örnek Kullanım

```css
p {
    text-decoration-line: underline;
    text-decoration-color: red;
}
```

Bu örnekte, `p` etiketine sahip metinlerin altı kırmızı bir çizgi ile çizilecektir.

## 3. text-decoration-style

`text-decoration-style` özelliği, süsleme çizgisinin stilini ayarlamak için kullanılır. Aşağıdaki değerleri alabilir:

* `solid`: Düz çizgi (varsayılan değer).
* `double`: Çift çizgi.
* `dotted`: Noktalı çizgi.
* `dashed`: Kesik çizgi.
* `wavy`: Dalgalı çizgi.

## Örnek Kullanım

```css
p {
    text-decoration-line: underline;
    text-decoration-style: wavy;
}
```

Bu örnekte, `p` etiketine sahip metinlerin altı dalgalı bir çizgi ile çizilecektir.

## 4. text-decoration-thickness

`text-decoration-thickness` özelliği, süsleme çizgisinin kalınlığını belirlemek için kullanılır. Kalınlık değeri uzunluk birimleri (px, em, rem, vb.) veya yüzde (%) cinsinden ifade edilebilir.

## Örnek Kullanım

```css
p {
    text-decoration-line: underline;
    text-decoration-thickness: 2px;
}
```

Bu örnekte, `p` etiketine sahip metinlerin altı 2 piksel kalınlığında bir çizgi ile çizilecektir.

## 5. text-decoration

`text-decoration` özelliği, yukarıda belirtilen tüm süsleme özelliklerini tek bir satırda tanımlamanıza olanak tanır. Bu özellik, süsleme çizgisinin türünü, rengini, stilini ve kalınlığını aynı anda belirlemenizi sağlar.

## Örnek Kullanım

```css
p {
    text-decoration: underline wavy red 2px;
}
```

Bu örnekte, `p` etiketine sahip metinlerin altı dalgalı, kırmızı ve 2 piksel kalınlığında bir çizgi ile çizilecektir.

## Sonuç

CSS metin süsleme özellikleri, metinlerinize görsel olarak çekici ve dikkat çekici dekoratif unsurlar eklemenizi sağlar. `text-decoration-line` , `text-decoration-color` , `text-decoration-style` , `text-decoration-thickness` ve `text-decoration` gibi özellikler, metin süslemesini ayrıntılı bir şekilde kontrol etmenize olanak tanır. Bu özellikleri kullanarak web sayfalarınızda estetik ve işlevsel metin süslemeleri oluşturabilirsiniz.
