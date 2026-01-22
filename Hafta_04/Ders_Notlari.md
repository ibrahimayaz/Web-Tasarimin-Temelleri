# Hafta 4: HTML Tablolar ve Form Temelleri - Ders Notları

Bu doküman, Web Tasarım dersinin dördüncü haftasında işlenen HTML Tabloları ve Form giriş konularını kapsamaktadır.

## 1. HTML Tablolar (Tables)

Verileri satır ve sütunlar halinde düzenli bir şekilde göstermek için kullanılır.

### Temel Tablo Etiketleri

*   `<table>`: Tabloyu başlatan ve bitiren kapsayıcı etiket.
*   `<caption>`: Tablonun başlığını belirtir (Tablonun hemen altında `<table>`'dan sonra yazılır).
*   `<tr>` (Table Row): Tablodaki her bir **satırı** oluşturur.
*   `<th>` (Table Header): Tablo **başlık hücresidir**. Varsayılan olarak metni **kalın** ve **ortalanmış** gösterir.
*   `<td>` (Table Data): Tablo **veri hücresidir**. Normal veriler buraya yazılır.

### Basit Tablo Yapısı
```html
<table border="1">
    <caption>Öğrenci Notları</caption>
    <tr>
        <th>Ad</th>
        <th>Soyad</th>
        <th>Not</th>
    </tr>
    <tr>
        <td>Ali</td>
        <td>Yılmaz</td>
        <td>85</td>
    </tr>
    <tr>
        <td>Ayşe</td>
        <td>Demir</td>
        <td>90</td>
    </tr>
</table>
```

### Önemli Tablo Nitelikleri (Attributes)
> **Not:** `border`, `cellpadding` ve `cellspacing` modern web tasarımında genellikle CSS ile yönetilir ancak HTML yapısını öğrenirken bilmek faydalıdır.

*   **border:** Tablo kenarlığının kalınlığını belirtir (örn: `border="1"`).
*   **width:** Tablonun genişliği (piksel veya % olarak).
*   **cellpadding:** Hücre içindeki veri ile kenarlık arasındaki boşluk.
*   **cellspacing:** Hücreler arasındaki boşluk.

## 2. Hücre Birleştirme (Merging Cells)

Excel'deki "Hücreleri Birleştir" özelliği gibidir.

### a. Sütun Birleştirme (`colspan`)
Yan yana olan hücreleri (sütunları) birleştirir.
```html
<!-- 2 sütunluk yer kaplayan hücre -->
<td colspan="2">Bu hücre 2 sütun genişliğindedir</td>
```

### b. Satır Birleştirme (`rowspan`)
Alt alta olan hücreleri (satırları) birleştirir.
```html
<!-- 2 satırlık yer kaplayan hücre -->
<td rowspan="2">Bu hücre 2 satır yüksekliğindedir</td>
```

## 3. HTML Formlarına Giriş

Kullanıcıdan bilgi almak (veri girişi) için formlar kullanılır.

### `<form>` Etiketi
Tüm form elemanlarını kapsayan etikettir.
*   **action:** Form verilerinin gönderileceği sunucu adresini (veya dosyasını) belirtir.
*   **method:** Verinin nasıl gönderileceğini belirtir (`GET` veya `POST`).

```html
<form action="kayit.php" method="POST">
    <!-- Form elemanları buraya -->
</form>
```

## 4. Temel Input (Girdi) Tipleri

Kullanıcıdan veri almak için `<input>` etiketi kullanılır. Kapanış etiketi yoktur. `type` niteliği ile görevi belirlenir.

### a. Metin Kutusu (`type="text"`)
Kısa metin girişleri için (Ad, Soyad vb.).
```html
Adınız: <input type="text" name="ad" placeholder="Adınızı yazın">
```
*   **placeholder:** Kullanıcıya kutunun içine ne yazacağını silik bir şekilde gösterir.
*   **name:** Verinin sunucuya hangi isimle gideceğini belirtir.

### b. Şifre Kutusu (`type="password"`)
Girilen karakterleri gizli (nokta veya yıldız) gösterir.
```html
Şifre: <input type="password" name="sifre">
```

### c. E-posta Kutusu (`type="email"`)
E-posta formatında veri girişi bekler. Mobilde klavyede @ işaretini getirir.
```html
E-posta: <input type="email" name="eposta">
```

### d. Gönder Butonu (`type="submit"`)
Formu `action` kısmında belirtilen adrese gönderir.
```html
<input type="submit" value="Kaydet">
```
