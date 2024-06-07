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

## Örnek Uygulama

Aşağıda basit bir duyarlı web sayfası örneği verilmiştir:

### HTML Kodu

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
      <aside>
        <h2>Kenar Çubuğu</h2>
        <p>Bu bir kenar çubuğu içeriğidir.</p>
      </aside>
    </main>
    <footer>
      <p>&copy; 2024 Duyarlı Web Tasarımı</p>
    </footer>
  </div>
</body>
</html>
```

### CSS Kodu

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

footer {
  background-color: #333;
  color: #fff;
  text-align: center;
  padding: 10px 0;
}

@media (max-width: 600px) {
  main {
    flex-direction: column;
  }
}
```

## Sonuç

Duyarlı web tasarımı, web sayfalarının farklı cihazlarda ve ekran boyutlarında iyi görünmesini ve işlevsel olmasını sağlayan önemli bir tekniktir. Esnek ızgaralar, esnek görseller ve medya sorguları gibi teknikler kullanılarak bu hedefe ulaşılabilir. Bu eğitimde, duyarlı web tasarımının temel kavramları ve uygulama yöntemleri ayrıntılı olarak ele alınmıştır.