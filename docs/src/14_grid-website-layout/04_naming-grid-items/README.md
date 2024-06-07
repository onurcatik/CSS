# CSS Grid Items Naming

## Giriş

CSS Grid Layout, modern web tasarımında yerleşim oluşturmak için güçlü bir araçtır. Bu eğitimde, CSS Grid öğelerine isim verme konusunu ele alacağız. Bu işlem, karmaşık yerleşimleri daha okunabilir ve yönetilebilir hale getirir. CSS Grid ile ilgili detaylı bilgi sağlayarak, bu özelliğin nasıl etkili bir şekilde kullanılacağını göstereceğiz.

## Grid Alanına İsim Verme

CSS Grid Layout, `grid-area` özelliği ile grid öğelerine isim vermemizi sağlar. Bu özellik, karmaşık düzenlerin yönetimini kolaylaştırır ve kodun okunabilirliğini artırır. Aşağıda, bu özelliğin nasıl kullanılacağına dair örnekler ve açıklamalar bulunmaktadır.

## Grid-Area Özelliği

`grid-area` özelliği, bir grid öğesine isim atamak için kullanılır. Bu isim, grid şablonlarında ve grid yerleşimlerinde kullanılarak öğelerin konumunu belirler.

```css
.item1 { grid-area: header; }
.item2 { grid-area: main; }
.item3 { grid-area: sidebar; }
.item4 { grid-area: footer; }
```

Yukarıdaki kod parçasında, dört farklı grid öğesine isimler atanmıştır: `header`, `main`, `sidebar`, ve `footer`.

## Grid Template Areas

Grid şablonları, grid alanlarının düzenini tanımlamak için kullanılır. Aşağıdaki örnek, grid şablonlarının nasıl kullanılacağını göstermektedir.

```css
.container {
  display: grid;
  grid-template-areas:
    'header header header'
    'sidebar main main'
    'footer footer footer';
  grid-gap: 10px;
}

.header { grid-area: header; }
.main { grid-area: main; }
.sidebar { grid-area: sidebar; }
.footer { grid-area: footer; }
```

Bu örnekte, `grid-template-areas` özelliği kullanılarak bir grid şablonu tanımlanmıştır. Şablon, üç satırdan ve üç sütundan oluşmaktadır. Her alan, önceden belirlenmiş grid alan isimlerine göre yerleştirilmiştir.

## Grid Öğelerinin Sıralaması

Grid Layout, öğelerin sayfa üzerindeki sırasını ve konumunu esnek bir şekilde yönetmemizi sağlar. `grid-area` ve `grid-template-areas` özellikleri kullanılarak öğelerin sırası ve yerleşimi kolayca ayarlanabilir.

```html
<div class="container">
  <div class="header">Header</div>
  <div class="main">Main Content</div>
  <div class="sidebar">Sidebar</div>
  <div class="footer">Footer</div>
</div>
```

## Sonuç

CSS Grid Layout'un `grid-area` özelliği, karmaşık yerleşimlerin yönetimini basitleştirir ve kodun okunabilirliğini artırır. Bu eğitimde, grid öğelerine nasıl isim verileceğini ve bu isimlerin grid şablonlarında nasıl kullanılacağını inceledik. Bu teknikler, web sayfalarınızda daha esnek ve yönetilebilir düzenler oluşturmanıza yardımcı olacaktır.


