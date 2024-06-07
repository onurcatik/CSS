# CSS El Kitabı

[CSS El Kitabı](https://onurcatik.github.io/CSS/)'na hoş geldiniz! Bu kılavuz, CSS'i temel bilgilerden daha ileri kavramlara kadar [görevlerle](assignments/README.md) birlikte kapsamlı bir şekilde anlamanızı sağlamak için tasarlanmıştır. İster başlamak isteyen bir acemi, ister bilgilerini derinleştirmeyi amaçlayan deneyimli bir geliştirici olun, bu el kitabında herkes için bir şeyler var.

## İçindekiler

1. [CSS ile Başlarken](./docs/src/01_Start/README.md)
   - CSS'e Giriş
   - Ortamınızı Ayarlama
   - İlk CSS Dosyanızı Oluşturma

2. [CSS Temelleri](./docs/src/02_Basics/README.md)
   - CSS'in Temelleri
   - Seçiciler ve Bildirimler
   - CSS Kurallarını Anlama

3. [Renk ve Arka Plan](./docs/src/03_Color-Background/README.md)
   - Renklerle Çalışma
   - Arka Planlar ve Desenler
   - Renk ve Arka Plan Uygulamaları

4. [Metin Stili ve Dekorasyon](./docs/src/04_Text-Styling/README.md)
   - Metin Stilleri
   - Metin Dekorasyonu
   - Yazı Tipleri ve Tipografi

5. [Kutu Modeli](./docs/src/05_Box-Model/README.md)
   - Kutu Modelini Anlamak
   - Dolgu ve Kenar Boşlukları
   - Sınırlar ve Boyutlandırma

6. [Yerleşim ve Düzen](./docs/src/06_Layout/README.md)
   - Kutu Yerleşimi
   - Flexbox ile Düzen
   - Grid Layout

7. [CSS'de Medya ve Görseller](./docs/src/07_Media-Images/README.md)
   - Görselleri ve Medyayı Yönetme
   - Görsel Boyutlandırma ve Konumlandırma
   - Arka Plan Görselleri

8. [CSS'de Animasyon ve Geçişler](./docs/src/08_Animation-Transitions/README.md)
   - CSS Geçişleri
   - Animasyonlar
   - İleri Animasyon Teknikleri

9. [Responsive Tasarım](./docs/src/09_Responsive-Design/README.md)
   - Responsive Tasarıma Giriş
   - Medya Sorguları
   - Mobil Dostu Tasarımlar

10. [Formlar ve Girdi Elemanları](./docs/src/10_Forms-Inputs/README.md)
    - Form Stilleri
    - Girdi Elemanları
    - Form Düzenleri ve Validasyon

11. [Gelişmiş Seçiciler ve Pseudo-sınıflar](./docs/src/11_Advanced-Selectors/README.md)
    - Gelişmiş Seçiciler
    - Pseudo-sınıflar ve Pseudo-elemanlar
    - CSS Seçici Stratejileri

12. [CSS'in Geleceği](./docs/src/12_Future-of-CSS/README.md)
    - CSS Özellikleri
    - Yeni ve Yaklaşan CSS Standartları
    - Modern CSS Araçları ve Teknikleri

---

## GitHub Deposu

Bu el kitabının kaynak kodu ve belgeleri GitHub'da barındırılmaktadır. Depoya aşağıdaki bağlantıyı kullanarak erişebilirsiniz:

[CSS El Kitabı GitHub Deposu](https://github.com/onurcatik/CSS)

Depoyu klonlayabilir, sorunlar açabilir veya pull request göndererek katkıda bulunabilirsiniz.

### Depoyu Klonlama

Depoyu klonlamak için aşağıdaki komutu kullanın:

```bash
git clone https://github.com/onurcatik/css.git
```

### Katkıda Bulunma

Topluluktan gelen katkılara açığız! Katkıda bulunmak isterseniz, lütfen şu adımları izleyin:

1. Depoyu fork edin
2. Yeni bir dal oluşturun (`git checkout -b feature-branch`)
3. Değişikliklerinizi yapın
4. Değişikliklerinizi commit edin (`git commit -m 'Add some feature'`)
5. Dalı push edin (`git push origin feature-branch`)
6. Bir pull request açın

---

## mdBook'u Oluşturma

Bu el kitabı, markdown dosyalarından modern çevrimiçi kitaplar oluşturmak için bir araç olan [mdBook](https://github.com/rust-lang/mdBook) kullanılarak oluşturulmuştur.

### Gereksinimler

Kitabı oluşturmak için `mdBook`un yüklü olması gerekir. Aşağıdaki komutu kullanarak yükleyebilirsiniz:

```bash
cargo install mdBook
```

### Kitabı Oluşturma

Kitabı oluşturmak için, depo kök dizinine gidin ve şu komutu çalıştırın:

```bash
mdbook build
```

Bu, kitabın statik dosyalarını `book` dizininde oluşturacaktır.

### Kitabı Yerel Olarak Servis Etme

Kitabı yerel olarak servis etmek ve tarayıcınızda görüntülemek için şu komutu çalıştırın:

```bash
mdbook serve
```

Bu, yerel bir sunucu başlatacak ve tarayıcınızda `http://localhost:3000` adresine giderek kitabı görüntüleyebilirsiniz.
