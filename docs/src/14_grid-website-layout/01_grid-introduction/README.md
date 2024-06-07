# CSS Grid Introduction

## Giriş

CSS Grid Layout Modülü, satır ve sütunlarla ızgara tabanlı bir düzen sistemi sunar. Bu sistem, web sayfalarını tasarlamayı, float ve konumlandırma kullanmadan daha kolay hale getirir. Bu modül, kullanıcıların daha esnek ve uyumlu düzenler oluşturmasına olanak tanır.

## Izgara Düzeni

Bir HTML elemanını ızgara konteyneri olarak tanımlamak için `display` özelliğini `grid` veya `inline-grid` olarak ayarlamanız gerekir.

### Izgara Elemanları

Izgara düzeni, bir ebeveyn eleman ve bir veya daha fazla çocuk elemandan oluşur.

### Izgara Sütunları

Izgara elemanlarının dikey çizgilerine sütun denir.

### Izgara Satırları

Izgara elemanlarının yatay çizgilerine satır denir.

### Izgara Boşlukları

Her sütun/satır arasındaki boşluklara boşluklar (gaps) denir.

### Izgara Çizgileri

Sütunlar arasındaki çizgilere sütun çizgileri denir.  
Satırlar arasındaki çizgilere satır çizgileri denir.

## Boşluk Özellikleri

Boşluk boyutunu ayarlamak için aşağıdaki özellikleri kullanabilirsiniz:

- `column-gap`
- `row-gap`
- `gap`

### `column-gap` Özelliği

Bu özellik, sütunlar arasındaki boşluğu belirler.

### `row-gap` Özelliği

Bu özellik, satırlar arasındaki boşluğu belirler.

### `gap` Özelliği

Bu özellik, hem sütunlar hem de satırlar arasındaki boşlukları belirler. Bu özellik, hem `column-gap` hem de `row-gap` özelliklerini tek bir özellikte birleştirir.

## Izgara Konteyneri

Izgara konteyneri, ızgara düzeninin ebeveyn elemanıdır. `display` özelliği `grid` veya `inline-grid` olarak ayarlandığında, bu eleman bir ızgara konteyneri haline gelir. Izgara konteyneri, içerdiği çocuk elemanları bir ızgara düzeninde düzenler.

### Temel Izgara Özellikleri

- `grid-template-columns`: Izgara konteynerinin sütunlarını tanımlar.
- `grid-template-rows`: Izgara konteynerinin satırlarını tanımlar.
- `grid-template-areas`: Izgara alanlarının isimlendirilmiş bölgelerini tanımlar.
- `grid-column-gap`: Sütunlar arasındaki boşluğu tanımlar.
- `grid-row-gap`: Satırlar arasındaki boşluğu tanımlar.
- `grid-gap`: Hem sütunlar hem de satırlar arasındaki boşlukları tanımlar.

### Izgara Öğeleri Konumlandırma

- `grid-column-start`: Izgara öğesinin başladığı sütun çizgisini tanımlar.
- `grid-column-end`: Izgara öğesinin bittiği sütun çizgisini tanımlar.
- `grid-row-start`: Izgara öğesinin başladığı satır çizgisini tanımlar.
- `grid-row-end`: Izgara öğesinin bittiği satır çizgisini tanımlar.

### Izgara Alanları

Izgara alanları, ızgara öğelerinin yerleştirildiği adlandırılmış alanlardır. `grid-template-areas` özelliği ile tanımlanırlar ve ızgara düzeninde belirli bölgeleri işaretler.

### Örnek Kullanım

```css
.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(2, 100px);
  gap: 10px;
}

.grid-item {
  background-color: lightblue;
  border: 1px solid #000;
}
```

Bu örnekte, `.grid-container` sınıfı bir ızgara konteyneri olarak tanımlanmış ve üç sütun ve iki satır içeren bir ızgara düzeni oluşturulmuştur. Izgara elemanları arasında 10 piksel boşluk bırakılmıştır.

## Sonuç

CSS Grid Layout Modülü, karmaşık web düzenlerini basit ve etkili bir şekilde oluşturmayı mümkün kılar. Satır ve sütunları kullanarak, ızgara elemanlarını kolayca yerleştirebilir ve boşlukları ayarlayabilirsiniz. Bu modül, modern web tasarımında esneklik ve düzen sağlamak için güçlü bir araçtır.