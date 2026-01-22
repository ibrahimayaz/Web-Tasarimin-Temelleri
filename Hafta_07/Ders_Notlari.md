# Hafta 7: CSS Temelleri ve Seçiciler (Selectors) - Ders Notları

Bu doküman, Web Tasarım dersinin yedinci haftasında (CSS'e Giriş) işlenen CSS'in temel yapısı, sayfaya eklenme yöntemleri ve elementleri seçme (selector) tekniklerini kapsamaktadır.

## 1. CSS (Cascading Style Sheets) Nedir?
CSS (Basamaklı Stil Sayfaları), HTML elementlerinin ekranda, kağıtta veya diğer medyalarda **nasıl görüneceğini** belirleyen dildir.
*   HTML iskeleti oluşturur, CSS ise onu giydirir.
*   Renkler, fontlar, yerleşim (layout) ve animasyonlar CSS ile yapılır.

## 2. CSS Söz Dizimi (Syntax)

Bir CSS kuralı **seçici (selector)** ve **bildirim bloğundan (declaration)** oluşur.

```css
/* Seçici { Özellik: Değer; } */
h1 {
  color: blue;
  font-size: 12px;
}
```

## 3. Web Sayfasına CSS Ekleme Yöntemleri

### a. Satır İçi (Inline) CSS
HTML etiketinin içine `style` niteliği (attribute) eklenerek yazılır. **Sadece o etiketi etkiler.** Tavsiye edilmez (kod tekrarına neden olur).
```html
<h1 style="color:red; text-align:center;">Başlık</h1>
```

### b. Dahili (Internal) CSS
HTML sayfasının `<head>` kısmında `<style>` etiketleri arasına yazılır. Sadece o sayfayı etkiler.
```html
<head>
    <style>
        body { background-color: linen; }
        h1 { color: maroon; }
    </style>
</head>
```

### c. Harici (External) CSS (En İyi Yöntem)
CSS kodları `.css` uzantılı ayrı bir dosyaya yazılır. HTML sayfasına `<link>` etiketi ile bağlanır. Böylece bir CSS dosyası ile binlerce sayfayı yönetebilirsiniz.

**index.html:**
```html
<head>
    <link rel="stylesheet" href="style.css">
</head>
```
**style.css:**
```css
body { background-color: lightblue; }
```

## 4. CSS Seçiciler (Selectors)

Hangi HTML elementine stil uygulanacağını belirlemek için kullanılır.

### a. Element Seçici (Element/Tag Selector)
Etiket ismiyle tüm elementleri seçer.
```css
p { color: red; } /* Sayfadaki TÜM p (paragraf) etiketlerini kırmızı yapar */
```

### b. ID Seçici (ID Selector) - `#`
Belirli bir **tek** elementi seçmek için kullanılır. ID ismi sayfada eşsiz olmalıdır. `#` işareti ile tanımlanır.
```css
#ozel-baslik { color: blue; }
```
```html
<h1 id="ozel-baslik">Bu mavidir</h1>
```

### c. Sınıf Seçici (Class Selector) - `.`
Aynı stili birden fazla elemente uygulamak için kullanılır. `.` (nokta) işareti ile tanımlanır.
```css
.kirmizi-yazi { color: red; }
```
```html
<p class="kirmizi-yazi">Bu kırmızıdır</p>
<h2 class="kirmizi-yazi">Bu da kırmızıdır</h2>
```

### d. Evrensel Seçici (Universal Selector) - `*`
Sayfadaki **tüm** elementleri seçer. Genellikle sıfırlama (reset) işlemleri için kullanılır.
```css
* { margin: 0; padding: 0; }
```

### e. Gruplama Seçicisi (Grouping Selector)
Aynı stili paylaşan elementleri virgül ile ayırarak yazarız.
```css
h1, h2, p { text-align: center; }
```

## 5. İlişkisel Seçiciler (Combinators)

Elementlerin birbirine göre konumuna bakarak seçim yapar.

*   **Torun Seçici (Descendant):** `div p` (div'in içindeki tüm p'ler)
*   **Çocuk Seçici (Child):** `div > p` (div'in sadece bir alt seviyesindeki -doğrudan çocuğu olan- p'ler)

## 6. CSS Yorum Satırları
```css
/* Bu bir CSS yorum satırıdır, tarayıcı tarafından okunmaz */
```
