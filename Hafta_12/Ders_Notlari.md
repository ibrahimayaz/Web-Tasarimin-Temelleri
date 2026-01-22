# Hafta 12: JavaScript Temelleri ve DOM Manipülasyonu - Ders Notları

Bu doküman, Web Tasarım dersinin on ikinci haftasında işlenen JavaScript programlama diline giriş ve web sayfalarını interaktif hale getirme (DOM) konularını kapsamaktadır.

## 1. JavaScript Nedir?
JavaScript (JS), web sayfalarına "davranış" ve "etkileşim" katan, tarayıcı tarafında çalışan bir programlama dilidir.
*   **HTML:** Sayfanın iskeletini oluşturur (İsim).
*   **CSS:** Sayfayı süsler (Sıfat).
*   **JS:** Sayfayı hareketlendirir (Fiil).

### JavaScript Ekleme Yöntemleri
1.  **Satır İçi (Inline):** Etiket içine yazılır (Örn: `onclick="alert('Merhaba')"`) - *Önerilmez*.
2.  **Dahili (Internal):** `<script>` etiketleri arasına yazılır.
3.  **Harici (External):** `.js` uzantılı ayrı bir dosya olarak yazılır ve `<script src="dosya.js"></script>` ile çağrılır.

## 2. Temel Kavramlar

### a. Değişkenler (Variables)
Veri saklamak için kullanılan kaplardır. Modern JS'de `let` ve `const` kullanılır.
```javascript
let isim = "Ahmet";      // Değiştirilebilir değer
const pi = 3.14;         // Sabit değer (Değiştirilemez)
var eski = "Eski stil";  // Eski kullanım (Pek önerilmez)
```

### b. Veri Tipleri
*   **String:** Metin ("Merhaba").
*   **Number:** Sayı (10, 5.5).
*   **Boolean:** Mantıksal (true, false).

### c. Çıktı Alma
*   `console.log("Mesaj");`: Tarayıcı konsoluna (F12) yazar. (Geliştirici için).
*   `alert("Mesaj");`: Ekrana uyarı kutusu çıkarır.
*   `document.write("Mesaj");`: Sayfaya direkt yazı basar.

## 3. Fonksiyonlar (Functions)
Belli bir işi yapan kod bloklarıdır. Kodun tekrar kullanılmasını sağlar.

```javascript
function selamla(ad) {
    alert("Merhaba " + ad);
}

// Kullanımı
selamla("Ali");
```

## 4. DOM (Document Object Model)
JavaScript'in HTML elementlerine erişip onları değiştirmesini sağlayan yapıdır. Tarayıcı HTML sayfasını bir "Nesne Ağacı" olarak görür.

### Element Seçimi
Bir elementi değiştirmeden önce onu JS ile seçmemiz gerekir.
1.  `document.getElementById("id_degeri")`: ID'ye göre seçer (En hızlısı).
2.  `document.querySelector(".class" veya "#id")`: CSS seçicileri ile seçer.

### İçeriği ve Stili Değiştirme
*   **innerHTML:** HTML içeriğini değiştirir.
    ```javascript
    document.getElementById("baslik").innerHTML = "Yeni Başlık";
    ```
*   **style:** CSS stilini değiştirir.
    ```javascript
    document.getElementById("kutu").style.backgroundColor = "red";
    document.getElementById("kutu").style.display = "none";
    ```
*   **value:** Input (giriş) alanındaki değeri okur veya değiştirir.
    ```javascript
    let deger = document.getElementById("ad").value;
    ```

## 5. Olaylar (Events)
Kullanıcının sayfada yaptığı eylemlerdir. JS bu eylemleri dinler ve tetiklenir.
*   `onclick`: Tıklandığında.
*   `onmouseover`: Fare üzerine geldiğinde.
*   `onmouseout`: Fare üzerinden gittiğinde.
*   `onchange`: Input değeri değiştiğinde.

```html
<button onclick="renkDegistir()">Tıkla</button>
```
