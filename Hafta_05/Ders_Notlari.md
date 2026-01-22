# Hafta 5: HTML Form Elemanları ve Validasyon - Ders Notları

Bu doküman, Web Tasarım dersinin beşinci haftasında işlenen gelişmiş form elemanları, HTML5 input tipleri ve veri doğrulama (validasyon) konularını kapsamaktadır.

## 1. Gelişmiş Input Tipleri (HTML5)

HTML5 ile gelen yeni input tipleri, veri girişini kolaylaştırır ve özellikle mobil cihazlarda uygun klavyenin açılmasını sağlar.

### a. Sayı Girişi (`number`)
Sadece sayı girilmesine izin verir. Min/Max değerler belirlenebilir.
```html
Yaşınız: <input type="number" name="yas" min="18" max="99">
```

### b. Tarih Seçici (`date`)
Tarayıcının takvim arayüzünü açar.
```html
Doğum Tarihi: <input type="date" name="dogum_tarihi">
```

### c. Renk Seçici (`color`)
Renk paletini açar ve seçilen rengin hex kodunu (örn: #ff0000) tutar.
```html
Favori Renk: <input type="color" name="renk">
```

### d. Dosya Yükleme (`file`)
Kullanıcının bilgisayarından dosya seçmesini sağlar.
```html
Profil Resmi: <input type="file" name="resim">
```

## 2. Seçim Elemanları

Kullanıcıya seçenekler sunmak için kullanılır.

### a. Radyo Butonları (`radio`)
Bir grup seçenekten **sadece birini** seçtirmek için kullanılır. Aynı gruptaki butonların `name` değeri **aynı olmalıdır**.
```html
Cinsiyet:
<input type="radio" name="cinsiyet" value="kadin"> Kadın
<input type="radio" name="cinsiyet" value="erkek"> Erkek
```

### b. Onay Kutuları (`checkbox`)
Birden fazla seçeneği işaretlemek için kullanılır.
```html
Hobileriniz:
<input type="checkbox" name="hobi" value="spor"> Spor
<input type="checkbox" name="hobi" value="müzik"> Müzik
```

### c. Açılır Liste (`select` & `option`)
Uzun listelerden seçim yapmak için kullanılır (örn: Şehir seçimi).
```html
Şehir:
<select name="sehir">
    <option value="06">Ankara</option>
    <option value="34">İstanbul</option>
    <option value="35">İzmir</option>
</select>
```

### d. Çok Satırlı Metin Alanı (`textarea`)
Uzun metinler (adres, mesaj vb.) için kullanılır.
```html
Adresiniz: <textarea name="adres" rows="4" cols="50"></textarea>
```

## 3. HTML5 Form Validasyonu (Doğrulama)

Veri sunucuya gönderilmeden önce tarayıcı tarafında kontrol edilmesini sağlar.

### Önemli Validasyon Nitelikleri
*   **required:** Alanın doldurulmasını zorunlu kılar.
*   **min / max:** Sayısal değerler için alt ve üst sınır.
*   **minlength / maxlength:** Metin karakter sayısı sınırı.
*   **pattern:** Düzenli ifadeler (Regex) ile özel format kontrolü (örn: sadece harf, belirli formatta telefon no).

```html
<!-- Zorunlu ve en az 3 karakterli kullanıcı adı -->
<input type="text" name="kadi" required minlength="3">
```

## 4. GET ve POST Metotları Farkı

Form verilerinin sunucuya nasıl gönderileceğini belirler.

### GET Metodu
*   Veriler URL adres çubuğunda görünür (`adres.com?ad=ali&yas=20`).
*   Güvenli **değildir** (Şifre gibi gizli veriler için kullanılmaz).
*   Daha hızlıdır, genellikle arama formlarında kullanılır.
*   Veri boyutu sınırlıdır.

### POST Metodu
*   Veriler URL'de görünmez, arka planda paketlenerek gider.
*   Daha **güvenlidir** (Kayıt, giriş işlemleri için uygundur).
*   Veri boyutu sınırı yoktur (Dosya yükleme vb. için zorunludur).

---

### Özet Tablosu

| Özellik | GET | POST |
| :--- | :--- | :--- |
| **Görünürlük** | URL'de görünür | Gizli |
| **Güvenlik** | Düşük | Yüksek |
| **Kullanım** | Arama, Filtreleme | Kayıt, Giriş, Dosya Yükleme |
