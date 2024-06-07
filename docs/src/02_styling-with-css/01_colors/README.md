# CSS Color

CSS renkleri, web geliştirmede görsel tasarımın temel taşlarından biridir. Bu rehberde, CSS'de renklerin nasıl belirtileceği hakkında ayrıntılı bilgi sunulmaktadır.

## 1. Önceden Tanımlanmış Renk İsimleri

CSS'de bir renk, önceden tanımlanmış bir renk adı kullanılarak belirtilebilir. HTML/CSS'de 140 standart renk adı desteklenmektedir. Bu renk isimlerinden bazıları şunlardır:

* Red (Kırmızı)
* Blue (Mavi)
* Green (Yeşil)

Bu renk isimleri, tarayıcılar tarafından tanınır ve kolayca kullanılabilir.

## 2. CSS RGB Renkleri

RGB renk değeri, Kırmızı (Red), Yeşil (Green) ve Mavi (Blue) ışık kaynaklarını temsil eder. RGB renk modeli, ekranlarda renklerin nasıl görüntülendiğini açıklamak için kullanılır. RGB renk değeri şu formatta belirtilir:

```
rgb(red, green, blue)
```

Her bir bileşen 0 ile 255 arasında bir değere sahip olabilir. Örneğin:

```
rgb(255, 0, 0) // Kırmızı
rgb(0, 255, 0) // Yeşil
rgb(0, 0, 255) // Mavi
```

## 3. CSS HEX Renkleri

Hexadecimal (HEX) renkler, #RRGGBB formatında belirtilir. RR (kırmızı), GG (yeşil) ve BB (mavi) bileşenlerini temsil eden onaltılık (hexadecimal) sayılardır. HEX renkleri şu şekilde yazılır:

```
#FF0000 // Kırmızı
#00FF00 // Yeşil
#0000FF // Mavi
```

HEX renkleri, genellikle web tasarımında yaygın olarak kullanılır çünkü kısa ve özdür.

## 4. CSS HSL Renkleri

HSL, Ton (Hue), Doygunluk (Saturation) ve Açıklık (Lightness) anlamına gelir. HSL renk değeri şu formatta belirtilir:

```
hsl(ton, doygunluk, açıklık)
```

* **Ton (Hue):** 0 ile 360 derece arasında bir değerdir. 0 kırmızı, 120 yeşil ve 240 maviyi temsil eder.
* **Doygunluk (Saturation):** Yüzde değeri olarak belirtilir. %0 gri bir tonu, %100 ise tam rengi ifade eder.
* **Açıklık (Lightness):** Yine yüzde değeri olarak belirtilir. %0 siyah, %50 ne açık ne koyu, %100 beyaz anlamına gelir.

Örneğin:

```
hsl(0, 100%, 50%) // Kırmızı
hsl(120, 100%, 50%) // Yeşil
hsl(240, 100%, 50%) // Mavi
```

## 5. RGBA Renk Değeri

RGBA renk değerleri, RGB renk değerlerinin bir uzantısı olup alfa kanalını da içerir. Alfa kanalı, bir rengin opaklığını belirtir. RGBA renk değeri şu formatta belirtilir:

```
rgba(red, green, blue, alfa)
```

* **Alfa:** 0.0 ile 1.0 arasında bir değerdir. 0.0 tam şeffaflığı, 1.0 ise tam opaklığı ifade eder.

Örneğin:

```
rgba(255, 0, 0, 0.5) // %50 şeffaf kırmızı
rgba(0, 255, 0, 0.7) // %70 şeffaf yeşil
rgba(0, 0, 255, 1.0) // Tam opak mavi
```

Bu rehber, CSS renkleri hakkında temel bilgileri sağlamaktadır. Renklerin doğru kullanımı, web sitelerinin görsel çekiciliğini artırmanın yanı sıra kullanıcı deneyimini de iyileştirir. CSS renkleri hakkında daha fazla bilgi ve örnekler için CSS resmi dokümantasyonunu incelemeniz önerilir.
