# CSS Gradyan

CSS gradyanları, iki veya daha fazla belirli renk arasında düzgün geçişler göstermenizi sağlar. CSS, üç tür gradyanı tanımlar:

1. Lineer Gradyanlar (aşağı/yukarı/sola/sağa/çapraz olarak gider)
2. Radyal Gradyanlar (merkezlerine göre tanımlanır)
3. Konik Gradyanlar (açısal olarak döner)

## CSS Lineer Gradyanlar

Lineer gradyan oluşturmak için en az iki renk duraklama noktası tanımlamalısınız. Renk duraklama noktaları, geçişin başladığı ve bittiği yerleri belirler. Lineer gradyanlar, başlangıç noktası ve bitiş noktası arasında doğrusal bir renk geçişi oluşturur.

### Temel Kullanım

Bir lineer gradyan oluşturmak için `linear-gradient()` fonksiyonunu kullanırız. Bu fonksiyon, iki ana parametre alır: yön (isteğe bağlı) ve renk duraklamaları.

```css
background: linear-gradient(direction, color-stop1, color-stop2, ...);
```

* `direction`: Gradyanın yönünü belirtir (varsayılan olarak aşağıya doğrudur). Yön, açı olarak (`deg` cinsinden) veya kelime olarak belirtilebilir (`to right`,    `to left`,    `to bottom`,    `to top`).
* `color-stop`: Gradyandaki belirli bir rengi ve bu rengin duraklama noktasını belirtir.

#### Örnekler

 **Yukarıdan Aşağıya Lineer Gradyan**

```css
background: linear-gradient(to bottom, red, yellow);
```

 **Sola Doğru Lineer Gradyan**

```css
background: linear-gradient(to left, blue, green);
```

 **45 Derecelik Açıyla Lineer Gradyan**

```css
background: linear-gradient(45deg, purple, orange);
```

### Çok Renkli Gradyanlar

Bir gradyan, ikiden fazla renk duraklaması içerebilir. Renklerin nerede duracağını belirlemek için yüzde (%) veya `px` cinsinden değerler kullanılabilir.

 **Çok Renkli Gradyan**

```css
background: linear-gradient(to right, red 0%, yellow 50%, green 100%);
```

## CSS Radyal Gradyanlar

Radyal gradyanlar, merkezden başlayarak dışa doğru yayılır. En az iki renk duraklama noktası tanımlamanız gerekmektedir. Radyal gradyanlar, dairesel veya eliptik olabilir.

### Temel Kullanım

Bir radyal gradyan oluşturmak için `radial-gradient()` fonksiyonunu kullanırız. Bu fonksiyon, merkez (isteğe bağlı), şekil (isteğe bağlı) ve renk duraklamaları gibi parametreler alır.

```css
background: radial-gradient(shape size at position, color-stop1, color-stop2, ...);
```

* `shape size at position`: Gradyanın şeklini, boyutunu ve pozisyonunu belirtir. Şekil `circle` (daire) veya `ellipse` (elips) olabilir. Pozisyon `at center`,  `at top left` vb. olarak belirtilir.
* `color-stop`: Gradyandaki belirli bir rengi ve bu rengin duraklama noktasını belirtir.

#### Örnekler

 **Dairesel Radyal Gradyan**

```css
background: radial-gradient(circle, red, yellow);
```

 **Eliptik Radyal Gradyan**

```css
background: radial-gradient(ellipse, blue, green);
```

 **Merkezde Konumlandırılmış Dairesel Radyal Gradyan**

```css
background: radial-gradient(circle at center, purple, orange);
```

### Çok Renkli Radyal Gradyanlar

Radyal gradyanlar da ikiden fazla renk duraklaması içerebilir.

**Çok Renkli Radyal Gradyan**

```css
background: radial-gradient(circle, red 0%, yellow 50%, green 100%);
```

## CSS Konik Gradyanlar

Konik gradyanlar, merkezi bir noktadan başlayarak saat yönünde döner. CSS'de konik gradyan oluşturmak için `conic-gradient()` fonksiyonu kullanılır.

### Temel Kullanım

```css
background: conic-gradient(from angle at position, color-stop1, color-stop2, ...);
```

* `from angle at position`: Gradyanın başlangıç açısını ve pozisyonunu belirtir.
* `color-stop`: Gradyandaki belirli bir rengi ve bu rengin duraklama noktasını belirtir.

#### Örnekler

 **Temel Konik Gradyan**

```css
background: conic-gradient(red, yellow, green);
```

**45 Derece Açıyla Başlayan Konik Gradyan**

```css
background: conic-gradient(from 45deg, blue, purple, orange);
```

## Gradyanlarda Opaklık ve Transparanlık

Gradyanlarda opaklık ve transparanlık ayarları da yapılabilir. Renk duraklamalarında RGBA veya HSLA renk değerleri kullanarak opaklık derecesi belirlenebilir.

**Transparanlık İçeren Gradyan**

```css
background: linear-gradient(to right, rgba(255, 0, 0, 0.5), rgba(0, 255, 0, 0.5));
```

Bu bilgiler doğrultusunda, CSS gradyanları kullanarak web sitelerinizde etkileyici ve modern arka planlar oluşturabilirsiniz. Gradyanlar, geçişlerin yumuşaklığı ve renklerin zenginliği ile dikkat çeker. Bu nedenle, doğru kullanımla estetik ve görsel açıdan etkileyici sonuçlar elde edebilirsiniz.a
