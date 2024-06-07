## CSS Tooltip

CSS Tooltip, web geliştirmede kullanıcı deneyimini artırmak için sıkça kullanılan bir tekniktir. Bu öğretici, CSS kullanarak ipuçları (tooltip) oluşturmanın temel ve ileri düzey yöntemlerini ele alacaktır. İçerik, ciddi ve bilimsel bir dille sunulacak ve herhangi bir yanlış veya eksik bilgi kritik bir şekilde ele alınacaktır.

### Tooltip Nedir?

Tooltip, kullanıcının fare imlecini bir öğenin üzerine getirdiğinde ek bilgi sağlamak için kullanılan küçük bir bilgi kutusudur. Bu bilgiler, kullanıcının daha iyi anlamasını ve etkileşimini sağlamak amacıyla kullanılır.

### Temel Tooltip Oluşturma

Tooltip oluşturmanın en basit yolu, HTML ve CSS kullanmaktır. Temel bir tooltip oluşturmak için aşağıdaki adımları izleyebilirsiniz:

#### HTML Yapısı

Öncelikle, HTML öğesi üzerinde bir tooltip oluşturmak için gerekli yapıyı kurmamız gerekir:

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Tooltip</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <div class="tooltip">Hover over me
        <span class="tooltiptext">Tooltip text</span>
    </div>
</body>

</html>
```

#### CSS Stilleri

Tooltip'in görünümünü ve konumunu ayarlamak için CSS kullanılır:

```css
.tooltip {
    position: relative;
    display: inline-block;
    cursor: pointer;
}

.tooltip .tooltiptext {
    visibility: hidden;
    width: 120px;
    background-color: black;
    color: #fff;
    text-align: center;
    border-radius: 6px;
    padding: 5px 0;
    position: absolute;
    z-index: 1;
    bottom: 125%;
    /* Tooltip'in yukarıda konumlanmasını sağlar */
    left: 50%;
    margin-left: -60px;
    opacity: 0;
    transition: opacity 0.3s;
}

.tooltip:hover .tooltiptext {
    visibility: visible;
    opacity: 1;
}
```

### İleri Seviye Tooltip Kullanımı

Tooltiplerin daha ileri seviye kullanımını ele alırken, daha fazla stil ve animasyon ekleyerek kullanıcı deneyimini artırabiliriz. Aşağıda, ileri düzey bir tooltip için bazı CSS teknikleri yer almaktadır.

#### CSS Animasyonları

Tooltip'in daha dikkat çekici olması için animasyon ekleyebiliriz:

```css
.tooltip .tooltiptext {
    visibility: hidden;
    width: 140px;
    background-color: black;
    color: #fff;
    text-align: center;
    border-radius: 6px;
    padding: 5px 0;
    position: absolute;
    z-index: 1;
    bottom: 125%;
    left: 50%;
    margin-left: -70px;
    opacity: 0;
    transition: opacity 0.6s, transform 0.6s;
    transform: translateY(-10px);
}

.tooltip:hover .tooltiptext {
    visibility: visible;
    opacity: 1;
    transform: translateY(0);
}
```

#### Farklı Konumlandırmalar

Tooltipleri farklı konumlarda göstermek için CSS'te position özelliklerini değiştirebiliriz:

```css
/* Sağda konumlanan tooltip */
.tooltip-right .tooltiptext {
    bottom: auto;
    top: 50%;
    left: 125%;
    margin-left: 0;
    margin-top: -30px;
}

/* Altta konumlanan tooltip */
.tooltip-bottom .tooltiptext {
    top: 125%;
    bottom: auto;
    left: 50%;
    margin-left: -60px;
}

/* Solda konumlanan tooltip */
.tooltip-left .tooltiptext {
    top: 50%;
    bottom: auto;
    right: 125%;
    left: auto;
    margin-top: -30px;
}
```

### Erişilebilirlik

Tooltiplerin erişilebilirlik açısından uygun olması önemlidir. Aşağıdaki yöntemlerle erişilebilirliği artırabilirsiniz:

* **Aria Etiketleri** : Tooltip öğelerine `aria-label` ve `aria-describedby` gibi etiketler ekleyerek ekran okuyucuların bu bilgileri doğru şekilde iletmesini sağlayabilirsiniz.
* **Odaklanabilirlik** : Tooltip içeriğinin sadece fare ile değil, klavye ile de erişilebilir olması için `tabindex` kullanabilirsiniz.

```html
<div class="tooltip" tabindex="0" aria-label="Tooltip text">Focus on me
    <span class="tooltiptext" id="tooltip1">Tooltip text</span>
</div>
```

### Sonuç

CSS kullanarak tooltip oluşturmak, web sayfalarında kullanıcı deneyimini önemli ölçüde artırabilir. Temel ve ileri düzey teknikler kullanarak çeşitli stillerde ve konumlarda tooltipler oluşturabilirsiniz. Ayrıca, erişilebilirlik standartlarına uygun tooltipler oluşturarak tüm kullanıcıların bu bilgilerden faydalanmasını sağlayabilirsiniz.
