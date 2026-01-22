# Hafta 6: Modern Sayfa Yerleşimi (Layout), IFrame ve İlk Proje - Ders Notları

Bu doküman, Web Tasarım dersinin altıncı haftasında işlenen modern sayfa yerleşimi etiketleri, IFrame kullanımı ve proje yönetimi konularını kapsamaktadır.

> **Önemli Not:** Eski HTML sürümlerinde kullanılan `frameset` ve `frame` etiketleri **kullanımdan kaldırılmıştır (deprecated)**. Modern web tasarımında sayfa bölümlendirme işlemleri **Semantik Etiketler** ve **CSS** ile yapılır. İçerik gömmek için ise sadece `iframe` kullanılır. Bu ders notlarında güncel standartlar esas alınmıştır.

## 1. Semantik (Anlamsal) HTML5 Yapısı

Bir web sayfasını mantıksal bölümlere ayırmak için kullanılan etiketlerdir. Arama motorları (SEO) ve erişilebilirlik için kritiktir.

*   `<header>`: Sayfanın veya bir bölümün başlık kısmı (Logo, ana başlık).
*   `<nav>`: Navigasyon (Menü) linklerini kapsar.
*   `<main>`: Sayfanın ana, benzersiz içeriğinin bulunduğu kısımdır. Sayfada sadece bir tane olmalıdır.
*   `<section>`: Konu bütünlüğü olan bölümleri gruplar (örn: Haberler, Hizmetler).
*   `<article>`: Tek başına anlamlı olan bağımsız içerikler (örn: Blog yazısı, Haber detayı).
*   `<aside>`: Ana içerikle dolaylı ilişkili yan içerik (örn: Yan menü, reklamlar).
*   `<footer>`: Sayfanın alt bilgi kısmı (Telif hakkı, iletişim bilgileri).

Bu etiketler görsel olarak bir değişiklik yapmazlar (CSS olmadan), ancak kodun okunabilirliğini ve anlamını güçlendirirler.

## 2. IFrame (Inline Frame)

Bir HTML sayfasının içinde, başka bir HTML sayfasını, videoyu veya haritayı pencere gibi göstermek için kullanılır.

### Temel Kullanım
```html
<iframe src="https://www.google.com/maps/embed?..." width="600" height="450"></iframe>
```

### Özellikler (Attributes)
*   **src:** Gösterilecek kaynağın adresi.
*   **width / height:** Genişlik ve yükseklik.
*   **title:** Erişilebilirlik için pencerenin açıklaması.
*   **frameborder:** Kenarlık (0 yok, 1 var). *Not: Genelde CSS ile kontrol edilir.*
*   **allowfullscreen:** Videoların tam ekran yapılmasına izin verir.

## 3. Proje Planlama ve Dosya Organizasyonu

Büyük projelerde düzenli çalışmak hayat kurtarır.

### Klasör Yapısı Örneği
```text
Proje_Adi/
│
├── index.html        (Ana Sayfa - Tarayıcılar ilk bunu arar)
├── hakkimda.html     (Alt Sayfa)
├── iletisim.html     (Alt Sayfa)
│
├── images/           (Tüm resimler burada)
│   ├── logo.png
│   └── banner.jpg
│
└── css/              (Stil dosyaları - Gelecek hafta)
    └── style.css
```

### Dosya İsimlendirme Kuralları
1.  **Türkçe karakter kullanmayın:** `iletişim.html` ❌ -> `iletisim.html` ✅
2.  **Boşluk bırakmayın:** `son proje.html` ❌ -> `son-proje.html` veya `son_proje.html` ✅
3.  **Küçük harf kullanın:** `Resim.JPG` yerine `resim.jpg` tercih edin.
4.  **Ana sayfa her zaman** `index.html` olmalıdır.

## 4. Ara Proje Gereksinimleri (Kişisel Portföy)

Bu haftaya kadar öğrendiğiniz (HTML, Liste, Tablo, Form, Görsel) bilgileri kullanarak ilk web sitenizi oluşturacaksınız.

*   **Konu:** Kendinizi tanıtan kişisel web sitesi.
*   **Sayfa Sayısı:** En az 3-5 sayfa (Anasayfa, Özgeçmiş, Galerim, İletişim vb.).
*   **Menü:** Her sayfada diğer sayfalara giden bir menü olmalı.
*   **İçerik:**
    *   Resimler (`img`)
    *   Listeler (`ul`, `ol`)
    *   İletişim Formu (`form`)
    *   Anlamsal yapı (`header`, `footer` vb.) kullanımı.
