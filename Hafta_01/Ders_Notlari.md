# Hafta 1: Web Teknolojilerine Giriş ve HTML Temelleri - Ders Notları

Bu doküman, Web Tasarım ve Geliştirme dersinin ilk haftasında işlenen konuları detaylandırmaktadır.

## 1. Internet ve World Wide Web (WWW) Kavramları

### Internet Nedir?
İnternet, dünya genelindeki bilgisayar ağlarını birbirine bağlayan devasa bir "ağların ağı" sistemidir. 1960'larda askeri iletişim araştırmalarıyla başlamış, günümüzde hayatın her alanına girmiştir. TCP/IP protokolleri üzerinden çalışır.

### World Wide Web (WWW) Nedir?
WWW (Web), internet üzerinde çalışan bir bilgi paylaşım sistemidir. Web sayfalarını, metinleri, görselleri ve diğer multimedya içeriklerini birbirine bağlayan sistemdir. Tim Berners-Lee tarafından icat edilmiştir. 
* **Özetle:** İnternet altyapıdır, Web ise bu altyapı üzerinde çalışan bir hizmettir.

## 2. Web Sitesi ve Web Uygulaması Farkı

* **Web Sitesi (Web Site):** Genellikle bilgilendirme amaçlıdır. İçeriği daha çok okumak veya izlemek içindir. Etkileşim sınırlıdır (örn: haber siteleri, bloglar, kurumsal tanıtım siteleri).
* **Web Uygulaması (Web Application):** Kullanıcının veri girişi yaptığı, işlem gerçekleştirdiği yazılımlardır. Masaüstü programlar gibi çalışırlar (örn: Gmail, Facebook, İnternet Bankacılığı, Google Docs).

## 3. Front-End ve Back-End Kavramları

Bir web projesi genellikle iki ana bölümden oluşur:

### Front-End (Ön Yüz)
* Kullanıcının tarayıcıda gördüğü ve etkileşime girdiği kısımdır.
* **Kullanılan Teknolojiler:** HTML (İskelet), CSS (Görünüm/Stil), JavaScript (Hareket/Etkileşim).
* Tasarım, renkler, menüler ve sayfa düzeni burada yapılır.

### Back-End (Arka Yüz)
* Kullanıcının görmediği, sunucu tarafında çalışan kısımdır.
* Veritabanı işlemleri, kullanıcı doğrulama, sunucu ayarları burada yapılır.
* **Kullanılan Teknolojiler:** Python, PHP, Java, C#, Ruby, Node.js ve veritabanları (MySQL, MongoDB vb.).

## 4. Statik ve Dinamik İçerik

* **Statik Sayfalar:** Sunucuda oluşturulduğu gibi kalan dosyalardır. İçeriğini değiştirmek için kodun manuel olarak düzenlenmesi gerekir. Her kullanıcı aynı sayfayı görür. Uzantıları genelde `.html` veya `.htm`dir.
* **Dinamik Sayfalar:** İçeriği kullanıcıya, zamana veya veritabanından gelen bilgiye göre otomatik değişen sayfalardır. Örn: "Hoşgeldin Ahmet" yazısı veya güncel döviz kurları. Bir yönetici panelinden içerik güncellenebilir.

## 5. Responsive (Duyarlı) Web Tasarım Nedir?
Responsive tasarım, bir web sayfasının bilgisayar, tablet ve mobil cihazlar gibi farklı ekran boyutlarına otomatik olarak uyum sağlamasıdır. Amaç, her cihazda en iyi kullanıcı deneyimini sunmaktır.

## 6. Geliştirme Ortamları (Text Editors & IDEs)
HTML kodlarını yazmak için basit bir metin düzenleyici bile yeterlidir, ancak gelişmiş editörler işimizi kolaylaştırır.
* **Notepad:** Windows'un basit metin editörü. Öğrenme amaçlı ilk başta kullanılabilir ama yetersizdir.
* **Notepad++:** Kod renklendirme özelliği olan hafif bir editör.
* **Visual Studio Code (Önerilen):** Günümüzde en popüler editördür. Eklenti desteği, kod tamamlama ve hatayı gösterme gibi güçlü özellikleri vardır.

## 7. HTML'e Giriş ve Temel Yapısı

**HTML (HyperText Markup Language):** Hiper Metin İşaretleme Dili anlamına gelir. **Bir programlama dili değil, bir işaretleme dilidir**. Sayfanın iskeletini oluşturur.

![htmliskelet](https://d2dkqamqz2k831.cloudfront.net/posts/338-1733217432633.jpg)

### HTML Etiket (Tag) Mantığı
HTML etiketleri genellikle açılır ve kapanır:
`<etiket_ismi> İçerik </etiket_ismi>`

### Temel HTML Sayfa İskeleti
Her HTML5 dosyası şu standart yapıya sahiptir:

```html
<!DOCTYPE html> <!-- Tarayıcıya bunun bir HTML5 dosyası olduğunu söyler -->
<html>          <!-- Kök element, her şey bunun içindedir -->
    <head>
        <!-- Sayfa hakkında bilgiler buraya (meta data) -->
        <meta charset="UTF-8"> <!-- Türkçe karakter desteği için -->
        <title>Sayfa Başlığı</title> <!-- Tarayıcı sekmesinde görünen isim -->
    </head>
    <body>
        <!-- Sayfada görünecek her şey buraya yazılır -->
        <h1>Merhaba Dünya!</h1>
        <p>Bu benim ilk web sayfam.</p>
    </body>
</html>
```

### Başlık Etiketleri (Headings)
HTML'de 6 seviye başlık vardır. `h1` en önemli/büyük başlık, `h6` en önemsiz/küçük başlıktır.

```html
<h1>Ana Başlık (h1)</h1>
<h2>Alt Başlık (h2)</h2>
<h3>Daha Alt Başlık (h3)</h3>
...
<h6>En Küçük Başlık (h6)</h6>
```

> **Not:** Başlık etiketleri sadece metni büyütmek için değil, arama motorlarının (Google vb.) sayfa yapısını anlaması için hiyerarşik olarak kullanılmalıdır.
