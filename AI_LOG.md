Proje Başlangıcı: Gereksinim Analizi
Proje Amacı: Görseldeki nesneleri dış API ile tespit edip, pHash (Perceptual Hashing) yöntemiyle kütüphanedeki en iyi eşleşmeleri ekrana getiren görsel arama motoru.
Teknoloji Yığını: Frontend için Vanilla JavaScript ve HTML/CSS; Backend için PHP.
Tasarım ve UX Hedefi: Animasyonlu, sade, renkli, üyeliksiz, genel kitleye hitap eden ve yüksek performanslı yapı.

Aşama 1: Mimari ve Dizin Yapılandırması
Klasör Ağacı: Güvenlik ve modülerlik için istemci (public/) ve sunucu (src/, api/) katmanları izole edildi.
Backend Gereksinimleri: Çevresel değişkenler için phpdotenv, HTTP istekleri için Guzzle, görsel hash karşılaştırması için imagehash kütüphaneleri planlandı.
Frontend Gereksinimleri: Modern animasyonlar için LottieFiles seçildi. Ekstra framework yükünden kaçınılarak saf JavaScript kullanılmasına karar verildi.

Aşama 2: Semantik HTML ve İskelet Kurulumu
Çıktı: public/index.html dosyası kodlandı.
Erişilebilirlik ve SEO: Ekran okuyucular için aria-label, aria-live özellikleri ve anlamsal etiketler (<main>, <section>) sisteme entegre edildi.
Uygulama Akışı (DOM Yapısı): Kullanıcı deneyimi üç temel duruma (State) bölündü:
upload-section: Sürükle-bırak (Drag & Drop) ve dosya seçme giriş alanı.
processing-section: Analiz aşamasında gösterilecek, başlangıçta gizli tutulan yükleme/tarama ekranı.
results-section: Bulunan eşleşmelerin basılacağı, loading="lazy" destekli dinamik grid alanı.
