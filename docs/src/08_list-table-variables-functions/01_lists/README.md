# CSS Lists

CSS, web sayfalarının stilini ve düzenini belirlemek için kullanılan güçlü bir araçtır. Bu kılavuz, CSS listeleri ve ilgili özellikleri hakkında kapsamlı ve detaylı bilgi sağlamayı amaçlamaktadır. 

## Farklı Liste Elemanı İşaretleyicileri

 **list-style-type** özelliği, liste elemanları için kullanılacak işaretleyicinin türünü belirler. Bu özellik, numaralı listeler (ordered lists) ve numarasız listeler (unordered lists) için çeşitli işaretleyiciler sağlar. Örnek olarak:

* `list-style-type: disc;` -> Daire işaretleyici
* `list-style-type: circle;` -> Boş daire işaretleyici
* `list-style-type: square;` -> Kare işaretleyici
* `list-style-type: decimal;` -> Sayısal işaretleyici
* `list-style-type: lower-alpha;` -> Küçük harf alfabe işaretleyici
* `list-style-type: upper-alpha;` -> Büyük harf alfabe işaretleyici

## Liste Elemanı İşaretleyici Olarak Görüntü Kullanımı

 **list-style-image** özelliği, liste elemanı işaretleyicisi olarak bir görüntü belirlemenizi sağlar. Bu özellik, özellikle özelleştirilmiş liste işaretleyicileri oluşturmak için kullanışlıdır. Kullanımı:

```css
ul {
    list-style-image: url('path_to_image.png');
}
```

Bu örnekte, liste elemanı işaretleyicisi olarak belirtilen görüntü kullanılacaktır.

## Liste Elemanı İşaretleyicilerinin Konumu

 **list-style-position** özelliği, liste elemanı işaretleyicilerinin (madde işaretleri) konumunu belirler. Bu özellik, işaretleyicilerin liste elemanının içinde veya dışında yer almasını sağlar. İki olası değeri vardır:

* `list-style-position: outside;` -> İşaretleyici, liste elemanının dışında yer alır.
* `list-style-position: inside;` -> İşaretleyici, liste elemanının içinde yer alır.

## Örnekler

Aşağıda, farklı **list-style** özelliklerinin nasıl kullanılacağını gösteren bazı örnekler verilmiştir:

 **Numarasız Liste (Unordered List) Örneği:** 

```html
<!DOCTYPE html>
<html>

<head>
    <style>
        ul {
            list-style-type: square;
        }
    </style>
</head>

<body>

    <ul>
        <li>Elma</li>
        <li>Muz</li>
        <li>Çilek</li>
    </ul>

</body>

</html>
```

Bu örnekte, numarasız listenin elemanları kare işaretleyicilerle belirtilmiştir.

**Numaralı Liste (Ordered List) Örneği:** 

```html
<!DOCTYPE html>
<html>

<head>
    <style>
        ol {
            list-style-type: upper-roman;
        }
    </style>
</head>

<body>

    <ol>
        <li>Birinci</li>
        <li>İkinci</li>
        <li>Üçüncü</li>
    </ol>

</body>

</html>
```

Bu örnekte, numaralı listenin elemanları büyük Roma rakamları ile belirtilmiştir.

## Liste Stili Özelliklerinin Özeti

* **list-style-type** : Liste işaretleyicisinin türünü belirler.
* **list-style-image** : Liste işaretleyicisi olarak bir görüntü belirler.
* **list-style-position** : Liste işaretleyicisinin konumunu belirler.

Bu özelliklerin doğru kullanımı, web sayfalarınızın listesini daha okunabilir ve görsel olarak çekici hale getirebilir. CSS listeleri üzerinde çalışırken, bu özelliklerin tümünü dikkate alarak en uygun stili seçebilirsiniz. Bu kılavuz, CSS listeleri ve ilgili özellikler hakkında kapsamlı bilgi sağlamayı amaçlamaktadır. Her bir özelliğin doğru ve etkili bir şekilde kullanımı, web sayfalarınızın stilini ve düzenini optimize etmenize yardımcı olacaktır.
