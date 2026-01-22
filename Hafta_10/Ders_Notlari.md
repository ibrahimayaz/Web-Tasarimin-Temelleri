# Hafta 10: CSS Kutu Modeli (Box Model) ve Pozisyonlama - Ders Notları

Bu doküman, Web Tasarım dersinin onuncu haftasında işlenen, CSS'in en temel yapı taşı olan Box Model ve elementleri sayfada konumlandırma tekniklerini kapsamaktadır.

## 1. CSS Kutu Modeli (Box Model)

Web sayfasındaki **her element** dikdörtgen bir kutu olarak kabul edilir. Bu kutu modelinin 4 ana katmanı vardır (İçten dışa doğru):

1.  **Content (İçerik):** Elementin kendisi (Metin, resim vb.). `width` ve `height` burayı etkiler.
2.  **Padding (İç Boşluk):** İçerik ile kenarlık arasındaki boşluktur. Arkaplan rengi burayı da kapsar.
3.  **Border (Kenarlık):** Padding ve Content'i çevreleyen çizgi.
4.  **Margin (Dış Boşluk):** Kutunun diğer elementlerle arasındaki boşluktur. Şeffaftır.

![Box Model](https://www.w3schools.com/css/box-model.png)

```css
.kutu {
    width: 300px;
    padding: 20px;
    border: 5px solid black;
    margin: 50px;
}
/* Toplam Genişlik = 300 + 20(sol pad) + 20(sağ pad) + 5(sol bor) + 5(sağ bor) = 350px */
```

### Box Sizing
Varsayılan olarak padding ve border, verdiğiniz `width` değerine **eklenir**. Bu da hesaplama yapmayı zorlaştırır.
*   `box-sizing: border-box;` : Bu özellik kullanıldığında padding ve border, genişliğe dahil edilir. Kutu tam olarak verdiğiniz genişlikte (örn: 300px) kalır. (Modern css resetlerinde mutlaka kullanılır).

## 2. Kenarlıklar (Borders)

*   `border-style`: solid (düz), dashed (kesik), dotted (noktalı) vb.
*   `border-width`: Kalınlık.
*   `border-color`: Renk.
*   **Kısayol:** `border: 1px solid red;`
*   **Border Radius:** Köşeleri yuvarlatmak için kullanılır. `border-radius: 10px;` veya `%50` (daire).

## 3. Görüntüleme (Display) Özelliği

Elementlerin yan yana mı yoksa alt alta mı geleceğini belirler.

*   `block`: Satırı tamamen kaplar (örn: `<div>`, `<p>`, `<h1>`). Alt alta dizilirler.
*   `inline`: Sadece içeriği kadar yer kaplar (örn: `<span>`, `<a>`). Yan yana dizilirler. Yükseklik/Genişlik verilemez.
*   `inline-block`: Hem yan yana dizilir hem de boyut verilebilir.
*   `flex`: Elementi esnek bir kapsayıcı yapar. İçindeki öğeleri kolayca yan yana dizer, ortalar veya sıralar. Modern tasarımların temelidir.
*   `none`: Elementi ve yerini tamamen yok eder (Gizler).

## 4. Pozisyonlama (Position)

Elementlerin normal akışın dışına çıkarılarak özel konumlara yerleştirilmesini sağlar.

*   `static`: Varsayılan durumdur. Normal akışa uyar.
*   `relative`: Normal konumuna **göre** hareket ettirilir. (Kendisi hareket etse de yeri ayrılmış (rezerve) kalır).
*   `absolute`: En yakın **pozisyonlanmış** (relative verilmiş) üst elemente göre konumlanır. Yoksa sayfaya göre konumlanır. Normal akıştan çıkar, yeri doldurulur.
*   `fixed`: Tarayıcı penceresine (ekrana) göre sabitlenir. Sayfa kaydırılsa da kıpırdamaz (Örn: "Yukarı Çık" butonu veya sabit menü).
*   `sticky`: Belli bir kaydırma noktasına kadar normal davranır, sonra `fixed` gibi yapışır.

## 5. Float (Kaydırma)
Elementleri sola veya sağa yaslamak için kullanılır. Metin resmin etrafını sarar.
*   `float: left;` / `float: right;`
*   **Clear:** Float kullanılan elementten sonra gelenlerin yanına girmesini engellemek için `clear: both;` kullanılır.
*   > Not: Modern tasarımlarda tüm sayfa iskeletini Float ile yapmak yerine Flexbox veya Grid tercih edilir, ancak Float hala resimler ve basit yan yana dizilimler için kullanılır.
