## CSS Position Property

CSS (Cascading Style Sheets) konumlandırma özelliği, HTML belgelerinde elemanların konumlandırılma yöntemini belirler. Konumlandırma, bir web sayfasının düzenini ve kullanıcı etkileşimini önemli ölçüde etkiler. CSS, konumlandırma için beş farklı değer sunar: `static` , `relative` , `fixed` , `absolute` , ve `sticky` .

### 1. `position: static` 

`position: static;` değeri, bir elemanın özel bir şekilde konumlandırılmadığını belirtir. Bu eleman, sayfanın normal akışına göre yerleştirilir. `static` konumlandırma varsayılan değerdir ve elemanlar bu şekilde herhangi bir özel pozisyonlama olmaksızın sayfa akışında sıralanır.

```css
.element {
    position: static;
}
```
Bu durumda eleman, sayfadaki diğer içeriklerle birlikte doğal düzeninde yer alır ve üst, sağ, alt, sol gibi pozisyonlama özellikleri etkisizdir.
### 2. `position: relative` 

`position: relative;` değeri, bir elemanın normal pozisyonuna göre yerleştirildiğini belirtir. Eleman, doğal konumundan göreceli olarak yer değiştirebilir. Bu, pozisyon özelliklerinin (top, right, bottom, left) elemanın başlangıç pozisyonuna göre ayarlandığı anlamına gelir.

```css
.element {
    position: relative;
    top: 10px;
    left: 20px;
}
```
Bu örnekte eleman, normal konumundan 10 piksel aşağı ve 20 piksel sağa hareket ettirilir. Diğer elemanlar, elemanın orijinal yerleşimine göre yerleştirilir.
 #
 ### 3. `position: fixed` 

`position: fixed;` değeri, bir elemanın görünüm alanına (viewport) göre sabitlendiğini belirtir. Bu eleman, sayfa kaydırıldığında bile yerinde kalır. Sabit pozisyonlama, üst, sağ, alt ve sol özellikleri ile kontrol edilir.

```css
.element {
    position: fixed;
    top: 0;
    right: 0;
}
```
Bu örnekte eleman, görünüm alanının sağ üst köşesine sabitlenir. Sayfa kaydırıldığında bile eleman bu konumda kalır.

### 4. `position: absolute` 

`position: absolute;` değeri, bir elemanın en yakın konumlandırılmış ataya (ancestor) göre yerleştirildiğini belirtir. Bu, elemanın görünüm alanına göre değil, en yakın `relative` , `absolute` , `fixed` , veya `sticky` konumlandırılmış ataya göre pozisyonlandığı anlamına gelir.

```css
.container {
    position: relative;
}

.element {
    position: absolute;
    top: 50px;
    left: 100px;
}
```

Bu örnekte `.element` , `.container` elemanına göre 50 piksel aşağı ve 100 piksel sağa konumlandırılır. `.container` elemanı `relative` olarak konumlandırılmıştır, bu yüzden `.element` bu konteynere göre yerleştirilir.

### 5. `position: sticky` 

`position: sticky;` değeri, bir elemanın kullanıcı kaydırma pozisyonuna göre yerleştirildiğini belirtir. Bu eleman, belirli bir eşiğe ulaştığında `relative` ile `fixed` pozisyonlaması arasında geçiş yapar.

```css
.element {
    position: sticky;
    top: 0;
}
```
Bu örnekte eleman, kaydırma sırasında görünüm alanının üst kısmına yapışır. Eleman, belirlenen eşiğe (top: 0) ulaştığında sabitlenir ve sayfa kaydırıldıkça yerinde kalır.
### Sonuç
CSS konumlandırma özellikleri, web sayfalarının düzenini ve kullanıcı deneyimini şekillendirmek için güçlü araçlar sunar. Her pozisyonlama türünün kendine özgü kullanımları ve etkileri vardır. Doğru kullanıldığında, bu özellikler web sayfalarının daha dinamik ve kullanıcı dostu hale gelmesine yardımcı olabilir. Elemanların doğru bir şekilde konumlandırılması, web geliştirme sürecinde kritik bir adımdır ve her geliştiricinin bu konumlandırma türlerini ve nasıl çalıştıklarını derinlemesine anlaması gerekmektedir.
