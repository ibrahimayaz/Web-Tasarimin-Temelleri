# Hafta 13: JavaScript Form Validasyonu ve İleri Konular - Ders Notları

Bu doküman, Web Tasarım dersinin on üçüncü haftasında işlenen, kullanıcıdan alınan verilerin sunucuya gönderilmeden önce doğruluğunun kontrol edilmesi (Validasyon) ve bu süreçte gerekli olan JavaScript mantık yapılarını kapsamaktadır.

## 1. Form Validasyonu (Doğrulama) Nedir?
Kullanıcıların formlara girdiği verilerin, istenen formatta ve kurallara uygun olup olmadığını kontrol etme işlemidir.
*   **İstemci Taraflı (Client-side):** Tarayıcıda JavaScript ile yapılır. Hızlı geri bildirim sağlar. (Bu derste işlenen).
*   **Sunucu Taraflı (Server-side):** PHP, Node.js vb. ile sunucuda yapılır. Güvenlik için şarttır.

## 2. Temel Kontrol Yapıları

### a. `if - else` Koşulları
Bir şartın doğru (`true`) veya yanlış (`false`) olmasına göre farklı kod bloklarını çalıştırır.

```javascript
let yas = 15;
if (yas >= 18) {
    console.log("Ehliyet alabilirsiniz.");
} else {
    console.log("Yaşınız tutmuyor.");
}
```

### b. Karşılaştırma Operatörleri
*   `==` : Eşittir (Sadece değer kontrolü, `5 == "5"` True).
*   `===` : Tam Eşittir (Değer ve Tür kontrolü, `5 === "5"` False). **(Önerilen)**
*   `!=` : Eşit değildir.
*   `&&` : VE (İki şart da doğru olmalı).
*   `||` : VEYA (En az biri doğru olmalı).

## 3. String Metotları ve Sayı Kontrolü

Formdan gelen veri her zaman "Metin" (String) türündedir.

*   **`.length`**: Metnin karakter sayısını verir.
    ```javascript
    let sifre = "12345";
    if (sifre.length < 6) { alert("Şifre en az 6 karakter olmalı"); }
    ```
*   **`.trim()`**: Metnin başındaki ve sonundaki boşlukları temizler. Kullanıcı yanlışlıkla boşluk bırakmışsa temizlemek için kullanılır.
    ```javascript
    let ad = "  Ali  ";
    ad = ad.trim(); // "Ali" olur
    ```
*   **`isNaN()` (Is Not a Number)**: Değerin sayı olup olmadığını kontrol eder.
    *   Sayı DEĞİLSE `true` döner.
    *   Sayıysa `false` döner.
    ```javascript
    if (isNaN("abc")) { console.log("Lütfen sayı girin"); } // True döner
    ```

## 4. Form Gönderimini Durdurmak (`return false`)
Bir formdaki "Submit" butonuna basıldığında sayfa yenilenir ve veriler gider. Eğer hata varsa bunu engellememiz gerekir.

Bunun için form etiketine `onsubmit="return kontrolEt()"` eklenir. Fonksiyon `false` döndürürse form gönderilmez.

```html
<form onsubmit="return validateForm()"> ... </form>
```

## 5. Düzenli İfadeler (Regex) - Giriş
Metin içinde belirli desenleri (pattern) aramak için kullanılır.
*   E-posta formatı kontrolü (`@` var mı, `.` var mı?)
*   Sadece rakam veya sadece harf kontrolü.

```javascript
// Basit E-posta Regex Deseni
var emailPattern = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,6}$/;
if (emailPattern.test(girilenEmail)) {
    // Format doğru
}
```
