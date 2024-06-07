# Responsive

## Giriş

Duyarlı web tasarımı (responsive web design), web sayfanızın tüm cihazlarda iyi görünmesini sağlayan bir tekniktir. Bu teknik, yalnızca HTML ve CSS kullanılarak uygulanır ve herhangi bir program veya JavaScript içermez. Duyarlı web tasarımı, masaüstü bilgisayarlar, tabletler ve telefonlar gibi çeşitli cihazlarda web sayfalarının görüntülenebilmesini sağlar. Web sayfanızın cihaz ne olursa olsun iyi görünmesi ve kolay kullanılabilir olması gereklidir.

## Temel Kavramlar ve İlkeler

### Duyarlı Web Tasarımının Tanımı

Duyarlı web tasarımı, web sayfalarının farklı ekran boyutlarına ve yönelimlerine uyum sağlamasını sağlayan bir yaklaşımdır. Bu yaklaşım, web sayfalarının kullanıcının cihazına ve tarayıcı penceresine dinamik olarak uyum sağlayarak optimal bir kullanıcı deneyimi sunmasını hedefler.

### HTML ve CSS Kullanımı

Duyarlı web tasarımı, yalnızca HTML ve CSS kullanılarak gerçekleştirilir. Bu, web sayfasının yapısal bileşenlerinin HTML ile tanımlanması ve stil özelliklerinin CSS ile uygulanması anlamına gelir. JavaScript gibi diğer teknolojiler bu süreçte kullanılmaz.

## Duyarlı Tasarım Teknikleri

### Esnek Izgaralar (Flexible Grids)

Esnek ızgaralar, duyarlı tasarımın temelini oluşturur. Bu ızgaralar, yüzde tabanlı genişlikler kullanarak farklı ekran boyutlarına uyum sağlar. Örneğin:

```css
.container {
  width: 100%;
}

.column {
  float: left;
  width: 50%;
}
```

Bu örnekte, `.container` sınıfı genişliğini %100 olarak ayarlar, böylece her ekran boyutuna uyum sağlar. `.column` sınıfı ise genişliğini %50 olarak ayarlayarak iki sütunun yan yana durmasını sağlar.

### Esnek Görseller (Flexible Images)

Esnek görseller, görüntülerin farklı ekran boyutlarına uyum sağlamasını sağlar. Bu, genellikle görsellerin maksimum genişliğinin %100 olarak ayarlanmasıyla gerçekleştirilir:

```css
img {
  max-width: 100%;
  height: auto;
}
```

Bu stil kuralı, görsellerin kapsayıcı öğelerinin genişliğini aşmamasını ve orantılı olarak yeniden boyutlandırılmasını sağlar.

### Medya Sorguları (Media Queries)

Medya sorguları, belirli koşullar altında farklı stil kuralları uygulamak için kullanılır. Bu koşullar, genellikle ekran boyutu, çözünürlük veya yönelimi içerir. Medya sorguları ile farklı cihazlarda farklı düzenler uygulanabilir:

```css
@media (max-width: 600px) {
  .column {
    width: 100%;
  }
}
```

Bu örnekte, ekran genişliği 600 pikselden az olduğunda `.column` sınıfının genişliği %100 olarak ayarlanır, böylece sütunlar dikey olarak yerleşir.

## Kapsamlı Örnek Uygulama

Aşağıda, duyarlı bir web sayfası için kapsamlı bir örnek verilmiştir. HTML ve CSS kodları ayrı ayrı verilmiş ve ek olarak yeni bölümler (section) ve altbilgi (footer) eklenmiştir.

### HTML Kodu (index.html)

```html
<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Duyarlı Web Tasarımı Örneği</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <header>
      <h1>Duyarlı Web Tasarımı</h1>
    </header>
    <nav>
      <ul>
        <li><a href="#">Ana Sayfa</a></li>
        <li><a href="#">Hakkında</a></li>
        <li><a href="#">İletişim</a></li>
      </ul>
    </nav>
    <main>
      <section>
        <h2>Başlık</h2>
        <p>Bu bir örnek paragraftır. Duyarlı web tasarımı ile ilgili içerik burada yer alacak.</p>
      </section>
      <section>
        <h2>Ek Başlık</h2>
        <p>Bu ikinci bölümün içeriğidir. Farklı cihazlarda nasıl görüneceği hakkında daha fazla bilgi burada verilecektir.</p>
      </section>
      <aside>
        <h2>Kenar Çubuğu</h2>
        <p>Bu bir kenar çubuğu içeriğidir. Burada ek bilgiler veya bağlantılar yer alabilir.</p>
      </aside>
    </main>
    
  </div>
</body>
</html>
```

### CSS Kodu (style.css)

```css
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, sans-serif;
}

.container {
  width: 100%;
  margin: 0 auto;
}

header, nav, main, footer {
  padding: 20px;
}

header {
  background-color: #333;
  color: #fff;
  text-align: center;
}

nav ul {
  list-style: none;
  text-align: center;
}

nav ul li {
  display: inline;
  margin: 0 10px;
}

nav ul li a {
  text-decoration: none;
  color: #333;
}

main {
  display: flex;
  flex-wrap: wrap;
}

section {
  flex: 1;
  padding: 20px;
}

aside {
  flex: 1;
  padding: 20px;
  background-color: #f4f4f4;
}



@media (max-width: 600px) {
  main {
    flex-direction: column;
  }
  nav ul li {
    display: block;
    margin: 5px 0;
  }
}
```

## Açıklamalar

### HTML Kodu

HTML kodu, duyarlı bir web sayfasının yapısal bileşenlerini tanımlar. `<!DOCTYPE html>` bildirimi, belgenin HTML5 standardında olduğunu belirtir. `<html>` etiketinde `lang="tr"` özelliği, sayfanın dilinin Türkçe olduğunu belirtir. `<head>` bölümünde, karakter seti, viewport ayarları ve stil dosyasının bağlantısı yer alır.

Ana yapı, `<div class="container">` öğesi ile kapsanmıştır. Başlık `<header>`, gezinme menüsü `<nav>`, ana içerik `<main>`, yan içerik `<aside>` öğeleri içinde tanımlanmıştır.

### CSS Kodu

CSS kodu, HTML öğelerinin stil özelliklerini tanımlar. Tüm öğeler için `box-sizing: border-box` kuralı uygulanarak, padding ve border değerlerinin toplam genişliği etkilememesi sağlanır. `body` için genel font ayarı yapılır. `.container` genişliği %100 olarak ayarlanır.

Başlık, gezinme menüsü, ana içerik ve altbilgi için padding değerleri ayarlanır. `header` ve `footer` için arka plan rengi ve metin rengi ayarlanır. `nav` içinde yer alan liste öğeleri, yatay olarak düzenlenir ve bağlantıların dekorasyonu kaldırılır.

`main` öğesi içinde `flex` düzeni kullanılarak, esnek bir düzen oluşturulur. `section` ve `aside` öğeleri için padding değerleri belirlenir. Küçük ekranlar için `@media` kuralı kullanılarak, `main` öğesinin yönü dikey olarak değiştirilir ve `nav` içindeki liste öğeleri blok halinde düzenlenir.

## Sonuç

Duyarlı web tasarımı, web sayfalarının farklı cihazlarda ve ekran boyutlarında iyi görünmesini ve işlevsel olmasını sağlayan önemli bir tekniktir. Esnek ızgaralar, esnek görseller ve medya sorguları gibi teknikler kullanılarak bu hedefe ulaşılabilir. Bu eğitimde, duyarlı web tasarımının temel kavramları ve uygulama yöntemleri ayrıntılı olarak ele alınmıştır. Kapsamlı örnek uygulama ile duyarlı web tasarımının nasıl gerçekleştirileceği detaylı bir şekilde gösterilmiştir.