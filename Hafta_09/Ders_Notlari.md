# Hafta 9: CSS Arka Planlar (Backgrounds) ve Renkler - Ders Notları

Bu doküman, Web Tasarım dersinin dokuzuncu haftasında işlenen CSS arka plan özellikleri, renk sistemleri ve görsel efektleri kapsamaktadır.

## 1. Renk Sistemleri

CSS'de renkleri tanımlamanın birkaç yolu vardır.

*   **İsim ile:** `red`, `blue`, `green`
*   **HEX Kodu:** `#RRGGBB` formatında onaltılık kodlar. (Örn: `#FF0000` Kırmızı, `#000000` Siyah, `#FFFFFF` Beyaz).
*   **RGB:** `rgb(red, green, blue)` 0-255 arası değerler. (Örn: `rgb(255, 0, 0)`).
*   **RGBA:** RGB ile aynıdır, sondaki **A (Alpha)** şeffaflığı belirtir (0.0 ile 1.0 arası).
    *   `rgba(255, 0, 0, 0.5)` -> Yarı şeffaf kırmızı.

## 2. Arka Plan Özellikleri (Background Properties)

### a. Arka Plan Resmi (`background-image`)
Bir elementin arkasına resim koyar.
```css
body {
    background-image: url("bg.jpg");
}
```

### b. Arka Plan Tekrarı (`background-repeat`)
Resmin desen gibi döşenip döşenmeyeceğini belirler.
*   `repeat`: Yatay ve dikey tekrar eder (Varsayılan).
*   `no-repeat`: Tekrar etmez, sadece bir tane koyar.
*   `repeat-x`: Sadece yatayda tekrar eder.

### c. Arka Plan Konumu (`background-position`)
Resmin kutunun neresinde duracağını belirler.
*   `center`, `top`, `bottom`, `left`, `right` veya `x y` koordinatları (örn: `10px 20px`).

### d. Arka Plan Boyutu (`background-size`)
Resmin boyutunu ayarlar (En önemli özelliklerden biridir).
*   `auto`: Orijinal boyut.
*   `cover`: Kutuyu tamamen kaplayacak şekilde resmi büyütür/keser (En sık kullanılan).
*   `contain`: Resmin tamamı görünecek şekilde sığdırır (Boşluk kalabilir).

### e. Arka Plan Sabitleme (`background-attachment`)
Sayfa kaydırıldığında resmin hareket edip etmeyeceğini belirler.
*   `scroll`: Sayfayla beraber kayar (Varsayılan).
*   `fixed`: Sayfa kaysa bile resim arkada sabit kalır (**Parallax efekti** için kullanılır).

### f. Kısayol (Shorthand)
Tüm özellikleri tek satırda yazmak:
```css
/* background: color image repeat attachment position; */
background: #ffffff url("bg.jpg") no-repeat fixed center;
```

## 3. Gradyanlar (Gradients)

İki veya daha fazla renk arasında yumuşak geçiş sağlar. Resim kullanmadan görsel zenginlik katar.

### a. Doğrusal Gradyan (Linear Gradient)
Düz bir çizgi boyunca renk geçişi.
```css
background: linear-gradient(to right, red, yellow); /* Soldan sağa kırmızıdan sarıya */
```

### b. Radyal Gradyan (Radial Gradient)
Merkezden dışa doğru yayılan renk geçişi.
```css
background: radial-gradient(circle, red, yellow, green);
```
