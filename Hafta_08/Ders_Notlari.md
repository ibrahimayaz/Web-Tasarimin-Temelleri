# Hafta 8: CSS Metin, Font Özellikleri ve Ölçü Birimleri - Ders Notları

Bu doküman, Web Tasarım dersinin sekizinci haftasında işlenen yazı tipi (font/tipografi), metin düzenleme ve CSS ölçü birimleri konularını kapsamaktadır.

## 1. Yazı Tipi Özellikleri (Font Properties)

Yazının karakter yapısı, boyutu ve kalınlığı ile ilgili ayarlardır.

### a. Yazı Tipi Ailesi (`font-family`)
Kullanılacak yazı tipini belirler. Birden fazla değer verilmesi önerilir (Yedekli sistem).
```css
p {
    /* Önce Arial'e bakar, yoksa Helvetica, o da yoksa herhangi bir sans-serif font kullanır */
    font-family: "Arial", Helvetica, sans-serif;
}
```

### b. Yazı Boyutu (`font-size`)
Yazının büyüklüğünü belirler.
```css
h1 { font-size: 32px; }
p  { font-size: 16px; }
```

### c. Yazı Kalınlığı (`font-weight`)
Yazının ne kadar kalın olacağını belirler.
*   `normal` (400)
*   `bold` (700)
*   `100` - `900` arası sayısal değerler

### d. Yazı Stili (`font-style`)
Yazıyı sağa eğik (italik) yapmak için kullanılır.
*   `italic`
*   `normal`

## 2. Metin Düzenleme Özellikleri (Text Properties)

Metnin hizalanması, dekorasyonu ve harf aralıkları ile ilgilidir.

### a. Metin Rengi (`color`)
Yazının rengini belirler.
```css
p { color: #333333; }
```

### b. Metin Hizalama (`text-align`)
*   `left` (Sola yasla)
*   `right` (Sağa yasla)
*   `center` (Ortala)
*   `justify` (İki yana yasla - Blokla)

### c. Metin Dekorasyonu (`text-decoration`)
Altı çizili, üstü çizili vb. efektler. Linklerin altındaki çizgiyi kaldırmak için çok kullanılır.
```css
a { text-decoration: none; } /* Linkin alt çizgisini kaldırır */
h1 { text-decoration: underline; }
```

### d. Metin Dönüştürme (`text-transform`)
Yazıyı büyük/küçük harfe çevirir.
*   `uppercase` (TÜMÜ BÜYÜK)
*   `lowercase` (tümü küçük)
*   `capitalize` (Baş Harfleri Büyük)

### e. Satır ve Harf Aralığı
*   `line-height`: Satırlar arasındaki mesafe (Okunabilirlik için önemlidir. Örn: 1.5).
*   `letter-spacing`: Harfler arasındaki mesafe (örn: 2px).
*   `word-spacing`: Kelimeler arasındaki mesafe.

## 3. CSS Ölçü Birimleri

Web tasarımında boyutlandırma için kullanılan birimler ikiye ayrılır.

### a. Mutlak Birimler (Absolute Units) - `px`
*   **Piksel (px):** En yaygın birimdir. Ekran çözünürlüğüne bağlıdır. Sabit boyutludur, kullanıcının tarayıcı ayarlarından etkilenmez (Bazen dezavantajdır).

### b. Göreceli Birimler (Relative Units) - `em`, `rem`, `%`
Responsive (Duyarlı) tasarım için bu birimler tercih edilir.

*   **% (Yüzde):** Ebeveyn (üst) elementin boyutuna göre oranlanır.
*   **em:** Ebeveyn elementin yazı boyutunu baz alır. (Örn: Ebeveyn 16px ise, `2em` = 32px olur).
*   **rem (Root em):** Kök elementin (`<html>`) yazı boyutunu baz alır. En sağlıklı yöntemlerden biridir.
*   **vw (Viewport Width):** Ekran genişliğinin %1'i.
*   **vh (Viewport Height):** Ekran yüksekliğinin %1'i.
