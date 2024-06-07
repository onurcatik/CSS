## CSS Selector

### İçerik

Bu bölümde, CSS Gelişmiş Seçiciler konusunu detaylı ve bilimsel bir yaklaşımla inceleyeceğiz. Ele alınacak konular şunlardır:

1. **Element Seçici**
2. **ID Seçici**
3. **Class Seçici**
4. **Pseudo Sınıf**
5. **Pseudo Element**
6. **Özellik (Attribute) Seçici**
7. **Evrensel Seçici**
8. **Birleştirici (Combinator) Seçici**

### Element Seçici

**Tanım:** Element seçici, HTML elemanlarını element isimlerine göre seçer. Örneğin, `<p>` elementi için `p` seçicisi kullanılır.

**Örnek Kullanım:**
```css
p {
    color: blue;
}
```
Bu örnekte, tüm `<p>` elementlerinin metin rengi mavi olarak ayarlanır.

### ID Seçici

**Tanım:** ID seçici, sayfa içinde benzersiz olan bir ID'ye sahip elementi seçmek için kullanılır. ID seçicisi bir `#` karakteri ile başlar ve ardından elementin ID'si gelir.

**Örnek Kullanım:**
```css
#uniqueElement {
    color: red;
}
```
Bu örnekte, ID'si `uniqueElement` olan elementin metin rengi kırmızı olarak ayarlanır.

### Class Seçici

**Tanım:** Class seçici, belirli bir sınıf (class) özniteliğine sahip HTML elemanlarını seçer. Class seçicisi bir `.` karakteri ile başlar ve ardından sınıf adı gelir.

**Örnek Kullanım:**
```css
.exampleClass {
    font-size: 20px;
}
```
Bu örnekte, `exampleClass` sınıfına sahip tüm elementlerin yazı boyutu 20 piksel olarak ayarlanır.

### Pseudo Sınıf

**Tanım:** Pseudo sınıf, bir elementin özel bir durumunu tanımlamak için kullanılır. Örneğin, bir kullanıcı fareyi elementin üzerine getirdiğinde veya bir link ziyaret edildiğinde stil uygulamak için kullanılır.

**Örnek Kullanım:**
```css
a:hover {
    color: green;
}
```
Bu örnekte, bir bağlantı üzerine fare getirildiğinde, metin rengi yeşil olur.

### Pseudo Element

**Tanım:** Pseudo element, bir elementin belirli bölümlerini stil vermek için kullanılır. Örneğin, bir elementin ilk harfini veya ilk satırını stil vermek için kullanılır.

**Örnek Kullanım:**
```css
p::first-line {
    font-weight: bold;
}
```
Bu örnekte, tüm `<p>` elementlerinin ilk satırı kalın yazı tipinde olur.

### Özellik (Attribute) Seçici

**Tanım:** Attribute seçici, belirli bir özniteliğe sahip elementleri seçmek için kullanılır.

**Örnek Kullanım:**
```css
input[type="text"] {
    background-color: yellow;
}
```
Bu örnekte, `type` özniteliği `text` olan tüm `<input>` elementlerinin arka plan rengi sarı olur.

### Evrensel Seçici

**Tanım:** Evrensel seçici, tüm elementleri seçer. Evrensel seçici `*` karakteri ile temsil edilir.

**Örnek Kullanım:**
```css
* {
    margin: 0;
    padding: 0;
}
```
Bu örnekte, tüm elementlerin margin ve padding değerleri sıfırlanır.

### Birleştirici (Combinator) Seçici

**Tanım:** Birleştirici seçici, seçiciler arasındaki ilişkiyi açıklar. CSS'de dört farklı birleştirici vardır:

1. **Descendant (Alt Eleman) Seçici (Boşluk)**
2. **Child (Çocuk) Seçici (>)**
3. **Adjacent Sibling (Bitişik Kardeş) Seçici (+)**
4. **General Sibling (Genel Kardeş) Seçici (~)**

#### Descendant (Alt Eleman) Seçici

**Tanım:** Belirtilen elementin alt elemanlarını seçer.

**Örnek Kullanım:**
```css
div p {
    color: blue;
}
```
Bu örnekte, `<div>` elementinin altındaki tüm `<p>` elementlerinin metin rengi mavi olur.

#### Child (Çocuk) Seçici (>)

**Tanım:** Belirtilen elementin doğrudan çocuklarını seçer.

**Örnek Kullanım:**
```css
div > p {
    color: blue;
}
```
Bu örnekte, `<div>` elementinin doğrudan çocukları olan `<p>` elementlerinin metin rengi mavi olur.

#### Adjacent Sibling (Bitişik Kardeş) Seçici (+)

**Tanım:** Belirli bir elementin hemen ardından gelen belirli bir elementi seçer.

**Örnek Kullanım:**
```css
h1 + p {
    margin-top: 0;
}
```
Bu örnekte, bir `<h1>` elementinden hemen sonra gelen `<p>` elementinin üst kenar boşluğu sıfırlanır.

#### General Sibling (Genel Kardeş) Seçici (~)

**Tanım:** Belirtilen elementin tüm kardeşlerini seçer.

**Örnek Kullanım:**
```css
h1 ~ p {
    color: red;
}
```
Bu örnekte, `<h1>` elementinin tüm kardeşleri olan `<p>` elementlerinin metin rengi kırmızı olur.

Bu derste, CSS'in gelişmiş seçicileri detaylı ve bilimsel bir yaklaşımla ele alınmıştır. Bu bilgilerin CSS'de daha karmaşık ve esnek stiller oluşturmanıza yardımcı olması umulmaktadır.