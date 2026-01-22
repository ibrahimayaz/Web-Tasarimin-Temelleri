# HAFTA 14: Final Projesi ve Değerlendirme Esasları

Bu hafta, 13 hafta boyunca öğrenilen tüm bilgilerin (HTML, CSS, Bootstrap, JavaScript) harmanlanarak ortaya somut bir ürün çıkarılacağı final haftasıdır. Aşağıda final projesinin detayları, teknik gereksinimler ve puanlama kriterleri yer almaktadır.

## 1. Proje Konusu
Öğrenciler, tamamen kendi belirleyecekleri bir konuda (Kişisel Portfolio, E-Ticaret Ürün Tanıtımı, Kurumsal Firma Sitesi, Blog, Restoran Menüsü vb.) **çok sayfalı** ve **interaktif** bir web sitesi geliştireceklerdir.

## 2. Teknik Gereksinimler (İsterler)

Projenin geçerli sayılabilmesi için aşağıdaki teknik şartları sağlaması zorunludur:

### A. HTML Yapısı
*   `<!DOCTYPE html>` tanımı ve dil ayarları (`lang="tr"`) yapılmalıdır.
*   Semantic etiketler (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`, `<article>`) projede aktif olarak kullanılmalıdır.
*   SEO uyumlu `meta` etiketleri bulunmalıdır.

### B. CSS ve Tasarım (Responsive)
*   **Mobil Uyumluluk:** Site; telefon, tablet ve masaüstü ekranlarda bozulmadan görünmelidir (Responsive Design).
*   **Layout:** Sayfa düzeni için **Bootstrap Grid Sistemi** veya **CSS Flexbox/Grid** kullanılmalıdır.
*   Tasarım göze hoş gelmeli, renk uyumu ve okunabilir tipografi içermelidir.

### C. JavaScript (Etkileşim)
*   **Form Validasyonu:** İletişim sayfasındaki form, sunucuya gitmeden önce JavaScript ile kontrol edilmelidir (Boş alan kontrolü, Email formatı vb.).
*   **DOM Manipülasyonu:** Sayfada en az bir ekstra interaktif özellik olmalıdır. Örnekler:
    *   Resim galerisi (Lightbox).
    *   Basit bir hesaplama aracı.
    *   Yukarı çık butonu.

## 3. Sayfa İçeriği
Proje en az **4 farklı sayfadan** oluşmalıdır:

1.  **Anasayfa (`index.html`):** Hero (giriş) görseli, siteyi özetleyen bölümler.
2.  **Hakkımızda:** Kişi veya kurum hakkında bilgiler, misyon/vizyon.
3.  **Hizmetler / Galeri / Ürünler:** Grid yapısında sıralanmış görseller veya kartlar (`card`).
4.  **İletişim:** Google Maps (iframe) ve çalışan (validasyonlu) bir iletişim formu.

## 4. Dosya Düzeni ve Teslimat
Proje klasör yapısı aşağıdaki gibi düzenli olmalıdır:

```
OgrenciNo_AdSoyad_Final/
│
├── index.html
├── hakkimizda.html
├── iletisim.html
├── css/
│   └── style.css
├── js/
│   └── script.js
└── img/
    ├── logo.png
    └── banner.jpg
```

*   Proje `.zip` veya `.rar` formatında sıkıştırılarak teslim edilecektir.

## 5. Değerlendirme Kriterleri (Toplam 100 Puan)

Sınav notu aşağıdaki kriterlere göre verilecektir:

| Kriter | Açıklama | Puan |
| :--- | :--- | :--- |
| **Görsel Tasarım & UI** | Renkler, yazı tipleri, genel estetik ve düzen. | **20** |
| **Kod Kalitesi** | Temiz kod, girintiler, yorum satırları, semantic etiketler. | **15** |
| **Responsive Yapı** | Mobil cihazlarda sitenin düzgün çalışması. | **15** |
| **JavaScript İşlevleri** | Form kontrolü ve dinamik özelliklerin hatasız çalışması. | **25** |
| **Sunum & Soru-Cevap** | Kodların öğrenci tarafından yazıldığının teyidi için sorulacak sorulara verilen cevaplar. | **25** |

## 6. Sınav Günü Kuralları
1.  Öğrenciler projelerini sınav saatinde USB bellek ile getirecek veya öğrenme yönetim sistemine yüklemiş olacaktır.
2.  Her öğrenci projesini açıp kısaca tanıtacaktır.
3.  Öğretim görevlisi kod içerisinde rastgele bir yeri seçip "Bu kod ne işe yarıyor?", "Bu arka plan rengini nerede değiştirdin?" gibi sorular soracaktır.
4.  Kodu açıklayamayan öğrencinin projesi (kopya ve başkasına yaptırma şüphesiyle) geçersiz sayılabilir.


***Yapay zeka araçlarını kullanananların projeleri kopya olarak değerlendirilir.***
