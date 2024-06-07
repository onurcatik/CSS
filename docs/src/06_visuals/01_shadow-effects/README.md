# CSS Shadow Effects

CSS ile metinlere ve öğelere gölge ekleyebilirsiniz. Bu rehberde, CSS'de gölge efektlerini uygulamak için kullanılan anahtar özellikleri ayrıntılı olarak inceleyeceğiz: `text-shadow` ve `box-shadow` . Her iki özellik de tasarımın görsel derinliğini artırmak ve öğeleri daha belirgin hale getirmek için kullanılır. Şimdi bu özellikleri detaylı bir şekilde ele alalım.

## CSS `text-shadow` Özelliği

`text-shadow` özelliği, metinlere gölge uygulamak için kullanılır. Bu özellik, dört parametre alır: yatay gölge mesafesi, dikey gölge mesafesi, bulanıklık yarıçapı ve gölge rengi. Aşağıdaki örnek, basit bir metin gölgesinin nasıl uygulanacağını göstermektedir:

```css
h1 {
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
}
```

Bu örnekte:
* `2px` yatay gölge mesafesini, 
* `2px` dikey gölge mesafesini, 
* `5px` bulanıklık yarıçapını, 
* `rgba(0, 0, 0, 0.5)` ise gölge rengini (yarı saydam siyah) belirtir.

## Çoklu Gölgeler

Bir metne birden fazla gölge eklemek için, gölgeleri virgülle ayırarak listeleyebilirsiniz. Bu, gölge efektlerini daha karmaşık ve ilgi çekici hale getirebilir. Örneğin:

```css
h1 {
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5), -2px -2px 5px rgba(255, 0, 0, 0.5);
}
```

Bu örnekte, metne hem siyah hem de kırmızı gölgeler eklenmiştir, bu da daha dramatik bir görünüm sağlar.

## CSS `box-shadow` Özelliği

```css
div {
    3px 3px 10px rgba(0, 0, 0, 0.5);
}
```

`box-shadow` özelliği, bir öğeye bir veya daha fazla gölge uygulamak için kullanılır. Bu özellik, `text-shadow` ile benzer parametrelere sahiptir ancak ek olarak iç gölge parametresi de bulunur. Aşağıdaki örnek, basit bir kutu gölgesinin nasıl uygulanacağını göstermektedir:

CSS Box Shadow özelliği, HTML elemanlarının çevresine gölge eklemenizi sağlar. `box-shadow` özelliği, gölgenin konumunu, rengini ve yayılma yarıçapını belirlemenize olanak tanır. `box-shadow` property'sinin kullanımı ve farklı değerlerle nasıl çalıştığına dair açıklamalar aşağıda verilmiştir:

1. **Temel Kullanım:** 

```css
div {
    box-shadow: 10px 10px;
}
```

Bu örnekte, `box-shadow` özelliği yalnızca iki değer alır: yatay ve dikey offset (10px 10px). Ancak, gölge bulanıklığı ve renk belirtilmediği için tarayıcı varsayılan değerleri kullanacaktır.

2. **Renk Belirtilmesi:** 

```css
div {
    box-shadow: 10px 10px aqua;
}
```

Bu örnekte, gölge için bir renk belirtilmiştir. Yatay ve dikey offset (10px 10px) ile birlikte gölgenin rengi "aqua" olarak ayarlanmıştır.

3. **Bulanıklık Yarıçapı Ekleme:** 

```css
div {
    box-shadow: 10px 10px 5px aqua;
}
```

Bu örnekte, üçüncü değer olan bulanıklık yarıçapı (5px) eklenmiştir. Bu, gölgenin ne kadar yayılacağını belirler. Renk yine "aqua" olarak belirtilmiştir.

4. **İç Gölge:** 

```css
div {
    box-shadow: 10px 10px 5px aqua inset;
}
```

Bu örnekte, `inset` anahtar kelimesi kullanılarak gölgenin içe doğru olacağı belirtilmiştir. Gölge, elemanın dışı yerine iç kısmına uygulanır.

5. **Çoklu Gölge Kullanımı:** 

```css
div {
    box-shadow: 5px 5px orange, 10px 10px green, 15px 15px aqua;
}
```

Bu örnekte, birden fazla gölge belirtilmiştir. Her bir gölge virgülle ayrılır ve farklı offset, bulanıklık yarıçapı ve renk değerleri kullanılarak tanımlanır. Bu örnekte:
* İlk gölge: 5px yatay, 5px dikey, renk "orange"
* İkinci gölge: 10px yatay, 10px dikey, renk "green"
* Üçüncü gölge: 15px yatay, 15px dikey, renk "aqua"

## Detaylı Açıklama

`box-shadow` özelliği genellikle şu formatta kullanılır:

```css
box-shadow: [h-offset] [v-offset] [blur-radius] [spread-radius] [color] [inset];
```

* **h-offset:** Gölgenin yatay konumunu belirler. Pozitif değerler sağa, negatif değerler sola taşır.
* **v-offset:** Gölgenin dikey konumunu belirler. Pozitif değerler aşağıya, negatif değerler yukarıya taşır.
* **blur-radius:** (Opsiyonel) Gölgenin bulanıklık derecesini belirler. Pozitif değerler daha bulanık gölgeler oluşturur. Varsayılan değer 0'dır.
* **spread-radius:** (Opsiyonel) Gölgenin yayılma derecesini belirler. Pozitif değerler gölgeyi büyütür, negatif değerler küçültür.
* **color:** (Opsiyonel) Gölgenin rengini belirler. Varsayılan değer mevcut metin rengidir.
* **inset:** (Opsiyonel) Gölgenin içe doğru uygulanmasını sağlar. Varsayılan olarak dışa doğru uygulanır.

Bu açıklamalarla birlikte `box-shadow` özelliğini CSS kodlarınızda nasıl kullanabileceğinizi detaylı bir şekilde öğrenmiş oldunuz.

Bu örnekte:
* `3px` yatay gölge mesafesini, 
* `3px` dikey gölge mesafesini, 
* `10px` bulanıklık yarıçapını, 
* `rgba(0, 0, 0, 0.5)` ise gölge rengini (yarı saydam siyah) belirtir.

## İç Gölgeler

`box-shadow` özelliği ile iç gölgeler de oluşturabilirsiniz. İç gölge, gölgenin öğenin iç kısmına uygulandığı anlamına gelir. Bunu yapmak için `inset` anahtar kelimesi kullanılır. Örneğin:

```css
div {
    box-shadow: inset 3px 3px 10px rgba(0, 0, 0, 0.5);
}
```

Bu örnekte, gölge öğenin içine uygulanmıştır ve bu da öğeye içsel bir derinlik kazandırır.

## Sonuç

CSS'deki `text-shadow` ve `box-shadow` özellikleri, metinler ve öğeler üzerinde etkileyici görsel efektler oluşturmak için güçlü araçlardır. Bu özellikler, tasarımlarınıza derinlik ve boyut kazandırmanıza yardımcı olur. Uygulamada, bu gölgeleri dikkatli ve estetik bir şekilde kullanmak, kullanıcı deneyimini zenginleştirebilir ve görsel hiyerarşiyi güçlendirebilir.
