# Hafta 3: HTML Görseller ve Listeler - Ders Notları

Bu doküman, Web Tasarım dersinin üçüncü haftasında işlenen görsel ekleme, dosya yolları ve liste türleri konularını kapsamaktadır.

## 1. Web Sayfalarına Resim Ekleme (`<img>`)

Web sayfalarını görsel açıdan zenginleştirmek için `<img>` etiketi kullanılır. Bu etiket **kapanış etiketi olmayan** (self-closing) bir etikettir.

### Temel Kullanım
```html
<img src="resim.jpg" alt="Resim Açıklaması">
```

### Önemli Nitelikler (Attributes)
*   **src (Source):** Resmin dosya yolunu belirtir. Zorunludur.
*   **alt (Alternative Text):** Resim yüklenemezse veya görme engelli kullanıcılar için ekran okuyucular tarafından okunan metindir. SEO (Arama Motoru Optimizasyonu) için çok önemlidir.
*   **width:** Resmin genişliği (piksel veya % olarak).
*   **height:** Resmin yüksekliği.

**Not:** Genellikle sadece `width` veya sadece `height` verilir, diğeri otomatik orantılanır. İkisi birden verilirse resim büzülebilir veya uzayabilir.

```html
<!-- Genişliği 300px olan, yüklenemezse 'Manzara' yazan resim -->
<img src="manzara.jpg" alt="Dağ Manzarası" width="300">
```

## 2. Resim Yolları (File Paths)

Resmin nerede olduğu tarayıcıya doğru tarif edilmelidir.

### a. Mutlak Yol (Absolute Path)
Resmin tam internet adresidir. Başka bir web sitesindeki resmi kullanırken gereklidir.
```html
<img src="https://www.google.com/images/logo.png" alt="Google Logo">
```

### b. Göreceli Yol (Relative Path)
Kendi proje klasörümüzdeki resimler için kullanılır. Tavsiye edilen yöntemdir.

*   **Aynı klasörde:** `src="resim.jpg"`
*   **Alt klasörde:** `src="images/resim.jpg"` (images klasörünün içindeyse)
*   **Üst klasörde:** `src="../resim.jpg"` (Bir üst dizine çıkmak için `../` kullanılır)

## 3. Listeler

HTML'de bilgileri maddeler halinde göstermek için üç temel liste türü vardır.

### a. Sırasız Listeler (Unordered Lists) - `<ul>`
Maddelerin sırasının önemsiz olduğu, genellikle madde imi (bullet point) ile gösterilen listelerdir. Her madde `<li>` (List Item) etiketi ile başlar.

```html
<ul>
    <li>Elma</li>
    <li>Armut</li>
    <li>Kiraz</li>
</ul>
```
*   `type` niteliği ile şekil değiştirilebilir: `disc` (daire), `circle` (içi boş daire), `square` (kare).

### b. Sıralı Listeler (Ordered Lists) - `<ol>`
Maddelerin numaralandırıldığı listelerdir (1, 2, 3...).

```html
<ol>
    <li>HTML Öğren</li>
    <li>CSS Öğren</li>
    <li>JavaScript Öğren</li>
</ol>
```
*   `type` niteliği ile sıralama şekli değiştirilebilir:
    *   `type="1"` (1, 2, 3 - Varsayılan)
    *   `type="A"` (A, B, C)
    *   `type="a"` (a, b, c)
    *   `type="I"` (I, II, III - Romen Rakamı)
    *   `type="i"` (i, ii, iii)

### c. Tanım Listeleri (Description Lists) - `<dl>`
Terimler ve açıklamaları için kullanılır. Sözlük yapısı gibidir.
*   `<dl>`: Listenin tamamı
*   `<dt>`: Tanımlanan terim (Term)
*   `<dd>`: Tanım açıklaması (Description)

```html
<dl>
    <dt>HTML</dt>
    <dd>Web sayfaları oluşturmak için kullanılan işaretleme dilidir.</dd>
    
    <dt>CSS</dt>
    <dd>Web sayfalarını biçimlendirmek için kullanılan dildir.</dd>
</dl>
```

### d. İç İçe Listeler
Bir listenin maddesi, kendi içinde başka bir liste barındırabilir.

```html
<ul>
    <li>Meyveler
        <ul>
            <li>Elma</li>
            <li>Muz</li>
        </ul>
    </li>
    <li>Sebzeler
        <ul>
            <li>Domates</li>
            <li>Biber</li>
        </ul>
    </li>
</ul>
```

## 4. Modern Görsel ve Medya Kapayıcıları - `<figure>` ve `<figcaption>`

HTML5 ile birlikte gelen bu etiketler, görselleri ve onlara ait açıklamaları (altyazıları) semantik olarak gruplamak için kullanılır. Arama motorları ve tarayıcılar için görselle metnin ilişkisini netleştirir.

*   `<figure>`: Görsel, diyagram veya kod bloğu gibi bağımsız içeriği kapsar.
*   `<figcaption>`: `<figure>` elemanının başlığını veya açıklamasını belirtir.

### Kullanım Örneği
Eskiden görsellerin altına açıklama yazmak için sadece `<p>` etiketi kullanılırdı ve görsel ile metin arasında anlamsal bir bağ kurulamazdı.

```html
<figure>
    <img src="istanbul.jpg" alt="İstanbul Boğazı" width="100%">
    <figcaption>Şekil 1: İstanbul Boğazı'ndan bir görünüm.</figcaption>
</figure>
```

Bu yapı kullanıldığında, görsel ve açıklama bir bütün olarak taşınır ve anlamlandırılır.
