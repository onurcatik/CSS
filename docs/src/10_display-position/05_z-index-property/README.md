# CSS Z-index Property

CSS'nin z-index özelliği, bir HTML belgesindeki elemanların yığılma sırasını belirlemeye yarar. Bu özellik, özellikle üst üste binen elemanların görsel hiyerarşisini kontrol etmek için kullanılır. Bu rehberde, z-index özelliğinin detaylarını, kullanımını ve dikkat edilmesi gereken noktaları ele alacağız.

## Z-index Özelliğinin Tanımı

Z-index özelliği, bir elemanın diğer elemanlara göre hangi seviyede (üstte mi altta mı) görüneceğini belirler. Bu özellik, sadece pozisyonlanmış elemanlar için (position: relative, position: absolute, position: fixed veya position: sticky) geçerlidir. Varsayılan olarak, bir elemanın z-index değeri otomatik olarak "0"dır.

 **Örnek Kullanım:** 

```html
<div style="position: absolute; z-index: 1;">Birinci Eleman</div>
<div style="position: absolute; z-index: 2;">İkinci Eleman</div>
```

Yukarıdaki örnekte, "İkinci Eleman" birinci elemanın üstünde yer alacaktır çünkü z-index değeri daha yüksektir.

## Z-index Değerleri ve Anlamları

Z-index değeri, pozitif veya negatif bir tamsayı olabilir. Değer ne kadar yüksekse, eleman o kadar üstte yer alır. Negatif değerler ise elemanın daha alt seviyede görünmesini sağlar.

 **Örnek:** 

```html
<div style="position: absolute; z-index: -1;">Arka Plan Elemanı</div>
<div style="position: absolute; z-index: 1;">Ön Plan Elemanı</div>
```

Bu örnekte, "Arka Plan Elemanı" ön plan elemanının arkasında kalacaktır.

## Z-index ve Yığılma Bağlamı (Stacking Context)

Z-index özelliklerinin doğru anlaşılması için yığılma bağlamı kavramını bilmek önemlidir. Her HTML belgesi, kök yığılma bağlamı (root stacking context) adı verilen bir ana yığılma bağlamı ile başlar. Belirli CSS özelliklerinin kullanımı (örneğin, opacity, transform, filter) yeni yığılma bağlamları oluşturabilir. Bir yığılma bağlamı içinde, elemanlar z-index değerlerine göre sıralanır ve bu bağlamın dışındaki yığılma bağlamlarına etkileri olmaz.

 **Örnek:** 

```html
<div style="position: relative; z-index: 10;">
    <div style="position: absolute; z-index: 1;">Yığılma Bağlamı İçinde</div>
</div>
<div style="position: relative; z-index: 5;">Başka Bir Yığılma Bağlamı</div>
```

Bu örnekte, içteki "Yığılma Bağlamı İçinde" elemanı, dıştaki yığılma bağlamına göre sıralanmaz, sadece kendi bağlamında z-index 1 olarak değerlendirilir.

## Yanlış Anlaşılmalara Karşı Dikkat Edilmesi Gerekenler

1. **Pozisyonlanmış Elemanlar:** Z-index sadece `position` özelliği `relative`,  `absolute`,  `fixed` veya `sticky` olan elemanlar için geçerlidir. Diğer pozisyonlama değerlerine sahip elemanlarda z-index çalışmaz.
   
2. **Yığılma Bağlamlarının Önemi:** Yeni yığılma bağlamları oluşturmak, z-index sıralamasını etkileyebilir. Örneğin, bir eleman `transform` özelliği ile stilize edilirse, bu eleman yeni bir yığılma bağlamı oluşturur.

3. **Negatif Z-index Değerleri:** Negatif z-index değerleri, elemanın diğer elemanların arkasında yer almasını sağlar, ancak bu eleman yine de kök yığılma bağlamının üstünde kalır.

## Z-index Kullanımıyla İlgili Örnekler

 **Örnek 1: Basit Yığılma** 

```html
<style>
    .box1 {
        position: absolute;
        z-index: 2;
        width: 100px;
        height: 100px;
        background: red;
    }

    .box2 {
        position: absolute;
        z-index: 1;
        width: 100px;
        height: 100px;
        background: blue;
        top: 50px;
        left: 50px;
    }
</style>
<div class="box1"></div>
<div class="box2"></div>
```
Bu örnekte, kırmızı kutu mavi kutunun üstünde yer alır çünkü z-index değeri daha yüksektir.
**Örnek 2: Yığılma Bağlamı Oluşturma** 

```html
<style>
    .parent {
        position: relative;
        z-index: 1;
    }

    .child {
        position: absolute;
        z-index: 2;
        width: 100px;
        height: 100px;
        background: green;
    }

    .sibling {
        position: relative;
        z-index: 3;
        width: 100px;
        height: 100px;
        background: yellow;
    }
</style>
<div class="parent">
    <div class="child"></div>
</div>
<div class="sibling"></div>
```
Bu örnekte, sarı kutu (sibling) yeşil kutunun (child) üstünde yer alır çünkü sarı kutu farklı bir yığılma bağlamında daha yüksek bir z-index değerine sahiptir.
## Sonuç

Z-index özelliği, elemanların yığılma sırasını kontrol etmek için güçlü bir araçtır, ancak doğru kullanılmadığında karmaşık sorunlara yol açabilir. Z-index kullanırken pozisyonlama, yığılma bağlamları ve CSS özelliklerinin etkileşimlerini dikkate almak önemlidir. Bu rehberde, z-index özelliğinin temel kavramlarını ve pratik kullanım örneklerini ele aldık. Z-index özelliğinin gücünü tam anlamıyla kullanmak için bu prensipleri doğru anlamak ve uygulamak gereklidir.
