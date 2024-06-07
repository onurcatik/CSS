# CSS Introduction

- CSS (Cascading Style Sheets), HTML (HyperText Markup Language) ile birlikte kullanılan bir stil dilidir.
- Bu eğitim, CSS'nin temellerini, kullanım alanlarını ve doğru uygulamalarını kapsamaktadır.

## CSS Nedir?

- CSS, "Cascading Style Sheets" (Basamaklı Stil Şablonları) ifadesinin kısaltmasıdır.
- CSS, HTML öğelerinin ekran, kağıt veya diğer medya türlerinde nasıl görüntüleneceğini tanımlar.

## CSS'nin Temel Bileşenleri

CSS'nin temel bileşenleri şunlardır:

- **Seçiciler (Selectors)** : HTML öğelerini seçmek için kullanılır. Örneğin, bir elementin kimliğini, sınıfını veya türünü seçebilir.
- **Deklarasyon Blokları (Declaration Blocks)** : Seçilen elementin stil özelliklerini belirler. Her deklarasyon bir özellik ve bir değerden oluşur.
- **Özellikler (Properties)** ve **Değerler (Values)** : Özellikler, hangi CSS özelliğinin değiştirileceğini belirtir (örneğin, renk, yazı tipi boyutu). Değerler ise bu özelliklerin nasıl uygulanacağını belirtir.

## CSS'nin Uygulanma Yöntemleri

CSS, HTML belgelerine üç farklı şekilde uygulanabilir:

1. **Satır içi stiller (Inline Styles)** : HTML öğesinin `style` niteliği içinde tanımlanır. Örneğin:

```html
    <h1 style="color:blue;">Merhaba Dünya</h1>
```

2. **Dahili stiller (Internal Styles)** : HTML belgesinin `<head>` bölümünde bir `<style>` etiketi içinde tanımlanır. Örneğin:

```html
    <style>
        h1 {
            color: blue;
        }
    </style>
```

3. **Harici stiller (External Styles)** : Ayrı bir CSS dosyasında tanımlanır ve HTML belgesine `<link>` etiketi ile bağlanır. Örneğin:

```html
    <link rel="stylesheet" type="text/css" href="styles.css">
```

## CSS Seçicileri

CSS seçicileri, belirli HTML öğelerini hedeflemek için kullanılır. Bazı yaygın seçici türleri şunlardır:

- **Evrensel Seçici (`*`)** : Tüm öğeleri seçer.
- **Tür Seçici (`element`)** : Belirli bir türdeki öğeleri seçer.
- **Sınıf Seçici (`.class`)** : Belirli bir sınıfa sahip öğeleri seçer.
- **Kimlik Seçici (`#id`)** : Belirli bir kimliğe sahip öğeleri seçer.
- **Atribut Seçicileri** : Belirli bir atributa sahip öğeleri seçer.

## CSS'nin Doğru Kullanımı ve Kritik Değerlendirme

CSS'nin doğru kullanımı, temiz ve bakımı kolay kod yazmayı gerektirir. Bazı yaygın hatalar ve bunların nasıl önleneceği:

- **Özellikle `!important` kullanımı** : Bu özellik, stil kurallarını zorla uygular ancak gereksiz ve aşırı kullanımı kodun karmaşıklığını artırır.
- **Özelliklerin yinelenmesi** : Aynı stil özelliklerini tekrar tekrar tanımlamak yerine, stil kurallarını merkezi bir yerden yönetmek daha iyidir.
- **Kapsayıcı seçicilerle aşırı özelleştirme** : Fazla spesifik seçiciler kodun esnekliğini azaltır. Daha genel ve yeniden kullanılabilir seçiciler tercih edilmelidir.

## Sonuç

- CSS, web sayfalarının görsel sunumunu kontrol etmede önemli bir rol oynar.
- Doğru kullanımı, temiz ve etkili bir tasarım sağlar. Bu eğitimde, CSS'nin temellerini ve en iyi uygulamalarını inceledik.
- CSS'nin güçlü yönlerini anlamak ve doğru uygulamak, web geliştirme süreçlerinde büyük avantaj sağlar.
