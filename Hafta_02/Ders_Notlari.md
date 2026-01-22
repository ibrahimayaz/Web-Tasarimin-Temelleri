# Hafta 2: HTML Metin Biçimlendirme ve Bağlantılar - Ders Notları

Bu doküman, Web Tasarım dersinin ikinci haftasında işlenen metin biçimlendirme etiketleri, özel karakterler ve bağlantı (link) oluşturma konularını kapsamaktadır.

## 1. Paragraf ve Metin Düzeni Etiketleri

### Paragraf `<p>`
Metinleri paragraflara ayırmak için kullanılır. Tarayıcılar paragrafların altına ve üstüne otomatik olarak boşluk ekler.
```html
<p>Bu birinci paragraftır.</p>
<p>Bu ikinci paragraftır.</p>
```

### Satır Sonu `<br>`
Paragrafı bitirmeden alt satıra geçmek için kullanılır. Kapanış etiketi yoktur (Self-closing).
```html
<p>Bu satırın sonunda alt satıra geçilecek.<br>
Şimdi alt satıdayız.</p>
```

### Ön Tanımlı Metin `<pre>`
HTML normalde kod içindeki fazla boşlukları ve satır atlamalarını görmezden gelir. `<pre>` etiketi, metni editörde yazdığınız gibi (boşlukları ve girintileri koruyarak) gösterir. Şiirler veya kod blokları için idealdir.
```html
<pre>
   Bu metin      nasıl yazıldıysa
        öyle görünür.
</pre>
```

### Yatay Çizgi `<hr>`
Sayfada konu değişikliğini belirtmek veya bölümleri ayırmak için yatay bir çizgi çizer.
```html
<p>Birinci bölüm bitti.</p>
<hr>
<p>İkinci bölüm başladı.</p>
```

## 2. Metin Biçimlendirme Etiketleri

Metinleri kalın, italik veya altı çizili yapmak için kullanılır.

| Etiket | Açıklama |
| :--- | :--- |
| `<b>` | Metni **kalın** yapar (Sadece görsel). |
| `<strong>` | Metni **önemli/kalın** yapar (Semantik açıdan önemli, arama motorları önemser). |
| `<i>` | Metni *italik* yapar (Sadece görsel). |
| `<em>` | Metni *vurgulu/italik* yapar (Semantik vurgu). |
| `<u>` | Metnin <u>altını çizer</u>. (Linklerle karışmaması için dikkatli kullanılmalı). |
| `<del>` / `<s>` | Metnin ~~üzerini çizer~~. (Silinmiş veya geçersiz bilgi). |
| `<mark>` | Metni <mark>sarı fosforlu</mark> kalemle çizilmiş gibi vurgular. |

### Alt ve Üst Simge (`<sub>`, `<sup>`)
Matematiksel veya kimyasal formüller yazarken kullanılır.

```html
<p>H<sub>2</sub>O (Su Formülü)</p>
<p>x<sup>2</sup> + y<sup>2</sup> = z<sup>2</sup> (Matematik)</p>
```

## 3. Bağlantılar (Linkler) - `<a>` Etiketi

HTML'in en önemli özelliği olan "Hypertext" yapısını sağlayan etikettir. Başka sayfalara, dosyalara veya sayfa içi bölümlere gitmeyi sağlar.

### Temel Kullanım
`href` (Hypertext Reference) niteliği gidilecek adresi belirtir.
```html
<a href="https://www.google.com">Google'a Git</a>
```

### Target Attribute (Hedef)
Linkin nasıl açılacağını belirler.
* `_self`: Varsayılan değerdir. Link aynı sekmede açılır.
* `_blank`: Link **yeni bir sekmede** açılır.

```html
<a href="https://www.w3schools.com" target="_blank">W3Schools (Yeni Sekmede Aç)</a>
```

### Link Türleri
1.  **Dış Bağlantı (External):** Başka bir web sitesine giden link (örn: `https://...`).
2.  **İç Bağlantı (Internal):** Kendi sitenizdeki başka bir sayfaya giden link.
    ```html
    <a href="iletisim.html">İletişim Sayfasına Git</a>
    ```
3.  **E-posta Linki:** Tıklandığında mail programını açar.
    ```html
    <a href="mailto:info@ornek.com">Bize Mail Atın</a>
    ```

## 4. HTML Yorum Satırları
Kodu okuyan kişilere not bırakmak veya bazı kodları geçici olarak devre dışı bırakmak için kullanılır. Tarayıcıda **görünmezler**.

```html
<!-- Bu bir yorum satırıdır, ekranda görünmez -->
<p>Bu metin görünür.</p>
<!-- <p>Bu kod iptal edildi, çalışmaz.</p> -->
```

## 5. HTML Özel Karakterler (Entities)
Klavyede bulunmayan veya HTML için özel anlamı olan karakterleri (<, > gibi) yazmak için kullanılırlar.

| Karakter | Kod | Açıklama |
| :--- | :--- | :--- |
| (Boşluk) | `&nbsp;` | Non-breaking space (Fazladan boşluk bırakmak için). |
| < | `&lt;` | Küçüktür işareti (Tag açma ile karışmaması için). |
| > | `&gt;` | Büyüktür işareti. |
| © | `&copy;` | Telif hakkı sembolü. |
| ® | `&reg;` | Tescilli marka sembolü. |

```html
<p>Telif Hakkı &copy; 2024</p>
<p>5 &lt; 10</p>
```
