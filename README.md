# web-projesi
# 🔍 Görsel Keşif Sistemi (Visual Search Engine)

Görsel Keşif Sistemi, kullanıcıların sürükle-bırak yöntemiyle yükledikleri görsellerdeki nesneleri yapay zeka (Computer Vision) ile tespit eden ve sistem kütüphanesindeki en iyi eşleşmeleri **Perceptual Hashing (pHash)** yöntemiyle saniyeler içinde bulan modern bir web uygulamasıdır.

## 🚀 Özellikler

- **Akıllı Nesne Tanıma:** Yüklenen görseller dış API'ler aracılığıyla analiz edilerek içindeki temel nesneler tespit edilir.
- **pHash ile Kusursuz Eşleşme:** Renk, boyut veya kırpma farklılıklarına rağmen görsellerin algısal hash'leri (pHash) karşılaştırılarak en doğru sonuçlar listelenir.
- **Sürükle ve Bırak (Drag & Drop):** Kullanıcı dostu, sezgisel dosya yükleme arayüzü.
- **Modern ve Hızlı UI:** Vanilla JavaScript, CSS3 Glassmorphism (Buzlu Cam) tasarımı ve Lottie animasyonları ile hafif ve akıcı bir deneyim.
- **Erişilebilirlik (a11y) & SEO:** Semantik HTML etiketleri, ekran okuyucu uyumluluğu ve `loading="lazy"` ile optimize edilmiş görsel yüklemeleri.
- **Güvenli Mimari:** İstemci (public) ve sunucu (src/api) dizinlerinin izole edildiği, çevre değişkenleri (`.env`) ile korunan backend yapısı.

## 🛠️ Teknoloji Yığını (Tech Stack)

**Frontend:**
- HTML5 (Semantik & a11y uyumlu)
- CSS3 (CSS Variables, Glassmorphism, CSS Grid)
- Vanilla JavaScript (ES6+, Fetch API)
- Lottie-Web (Tarama animasyonları için)

**Backend:**
- PHP 8.x
- Composer (Paket yönetimi)
- [Guzzle](https://github.com/guzzle/guzzle) (HTTP İstekleri)
- [vlucas/phpdotenv](https://github.com/vlucas/phpdotenv) (Çevre değişkenleri güvenliği)
- [jenssegers/imagehash](https://github.com/jenssegers/imagehash) (Perceptual Hash hesaplamaları)
- MySQL / PostgreSQL (PDO ile veritabanı bağlantısı)

## 📁 Proje Mimarisi

```text
visual-search-project/
├── public/                 # Document Root (Tarayıcıdan erişilebilen tek klasör)
│   ├── index.html          
│   ├── assets/             # CSS, JS ve sabit görseller
│   └── uploads/            # Geçici yüklemeler (Güvenlik önlemleri aktif)
├── api/                    # Frontend'in iletişim kurduğu PHP endpoint'leri
├── src/                    # Çekirdek PHP sınıfları (Erişime kapalı)
├── .env.example            # Örnek ortam değişkenleri şablonu
└── composer.json           # Bağımlılık listesi
