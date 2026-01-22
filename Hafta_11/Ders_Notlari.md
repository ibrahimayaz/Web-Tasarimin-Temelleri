# Hafta 11: CSS Listeler, Tablolar ve Bootstrap Framework - Ders Notları

Bu doküman, Web Tasarım dersinin on birinci haftasında işlenen CSS liste/tablo stillendirme ve dünyanın en popüler CSS kütüphanesi olan Bootstrap giriş konularını kapsamaktadır.

## 1. CSS ile Liste ve Tablo Stillendirme

### a. Liste Stilleri (`list-style`)
`ul` ve `ol` listelerinin madde işaretlerini değiştirmek için kullanılır.
*   `list-style-type`: `none` (yok), `circle`, `square`, `upper-roman` vb.
*   `list-style-image`: Madde imi olarak resim kullanma (`url('ikon.png')`).
*   `list-style-position`: `inside` (içeride), `outside` (dışarıda).

```css
ul {
    list-style: none; /* Noktaları kaldırır (Genelde menüler için yapılır) */
    padding: 0;
    margin: 0;
}
```

### b. Tablo Stilleri
Tabloları daha şık hale getirmek için CSS kullanılır.
*   `border-collapse: collapse;`: Hücre kenarlarını birleştirir (Çift çizgi görünümünü engeller).
*   `nth-child(even)`: Satırları zebra desenli (bir dolu bir boş) boyamak için kullanılır.

## 2. Bootstrap Framework Nedir?
Bootstrap, Twitter tarafından geliştirilen, açık kaynaklı ve dünyanın en popüler **HTML, CSS ve JS kütüphanesidir**.
*   **Amaç:** Sıfırdan CSS yazmakla uğraşmadan, hazır sınıfları (class) kullanarak hızlıca modern ve responsive (mobil uyumlu) siteler yapmaktır.
*   **Kurulum:** CDN linkini `<head>` kısmına eklemek yeterlidir.

### Temel Kurulum (CDN)
```html
<!-- CSS Linki -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
<!-- JS Linki (Body sonuna) -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
```

## 3. Bootstrap Grid Sistemi
Sayfayı 12 eşit parçaya bölen sanal bir ızgara sistemidir.
*   `.container`: İçeriği ortalar ve kenarlardan boşluk bırakır.
*   `.container-fluid`: İçeriği %100 genişliğe yayar.
*   `.row`: Satır oluşturur.
*   `.col-*`: Sütun oluşturur (Toplamları 12 olmalıdır).

### Örnek (3 Eşit Kolon)
```html
<div class="container">
  <div class="row">
    <div class="col-4">Sol</div>   <!-- 12 parçanın 4'ü -->
    <div class="col-4">Orta</div>  <!-- 12 parçanın 4'ü -->
    <div class="col-4">Sağ</div>   <!-- 12 parçanın 4'ü -->
  </div>
</div>
```

## 4. Temel Bootstrap Bileşenleri

Sadece `class` isimlerini yazarak hazır stilleri kullanabiliriz.

### a. Renkler (Contextual Colors)
Bootstrap renkleri belli anlamlara gelir:
*   `primary` (Mavi - Ana işlem)
*   `success` (Yeşil - Başarılı)
*   `danger` (Kırmızı - Hata/Sil)
*   `warning` (Sarı - Uyarı)
*   `info` (Turkuaz - Bilgi)
*   `dark` / `light`

### b. Butonlar (`btn`)
```html
<button class="btn btn-primary">Giriş Yap</button>
<button class="btn btn-danger">Sil</button>
```

### c. Tablolar (`table`)
```html
<table class="table table-striped table-hover">...</table>
```
*   `table-striped`: Zebra deseni ekler.
*   `table-hover`: Üzerine gelince satırı koyulaştırır.

### d. Uyarı Kutuları (`alert`)
```html
<div class="alert alert-success">
    İşlem başarıyla tamamlandı!
</div>
```

### e. Kartlar (`card`)
Resim, başlık ve metin içeren kutular oluşturur (Ürün kartı, profil kartı vb.).
```html
<div class="card" style="width: 18rem;">
  <img src="..." class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">Kart Başlığı</h5>
    <p class="card-text">İçerik...</p>
  </div>
</div>
```
