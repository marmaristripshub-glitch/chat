# MarketVitrini — tek ürün mağazası

Bu paket, gönderdiğiniz MarketVitrini-Tema.zip temel alınarak düzenlenmiş tam Shopify temasıdır. Tema başka bir tabanla değiştirilmedi. Mevcut logo, görsel bağlantıları, iletişim bilgileri ve düzenleyici ayarları korunmuştur.

## Yükleme

1. Shopify → Online Mağaza → Temalar → Tema ekle → ZIP dosyası yükle.
2. `MarketVitrini-Tek-Urun-Profesyonel-Tema.zip` dosyasını seçin. ZIP'i açıp tekrar klasörleyerek yüklemeyin.
3. Temayı özelleştir → Tema ayarları → MarketVitrini PRO → Ana Satış Ürünü alanında kendi ürününüzü seçin. Pakette, gönderdiğiniz temadaki `collagen` ürünü seçili tutulmuştur.
4. Aynı yerden destek e-postasını ve blogunuzu seçin. Blog seçimi bütün yeni yazı listelerinde ortak kullanılır. Haberler blogunuz `news` veya `blog` adresindeyse otomatik bulunur.
5. Ana sayfa ve ürün sayfasındaki bölümler hazır sıralı gelir; tek tek bölüm eklemek gerekmez. Metin, renk, görsel ve SSS blokları tema düzenleyicisinden değiştirilebilir.
6. Kullanım rehberi ayarları ana ürün bölümündeki “Kullanım rehberi — düzenle” başlığı altındadır. Görsel kendi alanını tamamen doldurur. İç boşluk / yükseklik ayarı korunmuştur.

## Sayfalara otomatik eklenen alanlar

- Ana sayfa: mevcut görselli satış alanı, güven kartları, gerçek ürün açıklaması, üç adımlı kullanım, görselli hatırlatma, SSS, mevcut blog yazıları, son ürün çağrısı.
- Ürün: mobil galeri ve varyant seçimi, paket seçenekleri, stok ve fiyat bilgisi, kompakt kullanım rehberi, gerçek ürün açıklaması, bilgi kartları, kullanım görselleri, SSS, blog yazıları, son çağrı, sabit satın alma çubuğu.
- Blog listesi, yazı, sepet, arama, koleksiyon, genel sayfa ve 404: ilgili standart Shopify şablonu korunur; teslimat, iade ve destek bağlantıları eklenir. Yazı ve genel sayfalarda blog yönlendirmesi de bulunur.
- Blog yazısı: okunabilir metin genişliği, taşmayan görsel/tablo ve mevcut yazıyı tekrar önermeyen yazı kartları.
- İletişim: gerçek Shopify iletişim formu; etiketli alanlar, zorunlu e-posta/mesaj, hata ve başarı mesajları.
- Altbilgi: gerçek mağaza sayfaları ve yayınlanmış politikalar için bağlantılar. Mağazanın ödeme yöntemlerinden otomatik ödeme logoları.

### Mevcut sayfa adreslerini tanıma

Varsayılan sayfa şablonu şu adreslere göre ilgili bilgi veya form alanını otomatik gösterir:

| Sayfa | Tanınan adres sonları |
| --- | --- |
| Hakkımızda | hakkimizda, about, about-us |
| İletişim | iletisim, contact, contact-us |
| SSS | sss, sik-sorulan-sorular, faq, frequently-asked-questions |
| Teslimat | kargo, teslimat, kargo-ve-teslimat, shipping, shipping-policy |
| İade | iade, iade-ve-degisim, returns, refund-policy |
| Sipariş takibi | siparis-takibi, order-tracking, tracking |

Ayrı hazır şablonlar da eklendi: `page.about`, `page.contact`, `page.faq`, `page.shipping`, `page.returns`, `page.tracking`. Farklı adresli bir sayfanız varsa Shopify sayfa düzenleyicisinden uygun şablonu seçebilirsiniz. Bir sayfaya daha önce özel şablon atandıysa o atama korunur.

## Düzeltilen sorunlar

- Header-actions içindeki 15 Liquid/CSS hatası giderildi.
- Mobil galeri tam kullanılabilir genişliğe alındı; küçük görseller altta yatay dizildi. İlk ana görsel geciktirilmeden yüklenir.
- Mobil kartların hizaları, yorum yükseklikleri ve tablet taşmaları düzeltildi.
- Ürün seçeneklerini gizleyen eski form stilinden varyant seçicisi ayrıldı. JavaScript kapalıyken native ürün formu kullanılabilir.
- Varyanta ait minimum/maksimum/adet artış kuralları hem paketlerde hem sabit satın alma çubuğunda uygulanır. İşlem sürerken düğmeler ve varyant seçimi kilitlenir.
- İndirim kodu düğmesi çalışır hale getirildi. Kod gerçek Shopify indirim bağlantısı üzerinden sepet veya ödeme adımına taşınır; tema kodun geçerli olduğunu kendisi iddia etmez. Silinen kod artık uygulanmaz.
- Sabit stok sayıları yerine Shopify varyant stok bilgisi kullanılır. Kendini her oturumda yeniden başlatan kampanya sayacı kaldırıldı. Sayaç istenirse Tema ayarları → MarketVitrini PRO → Gerçek kampanya bitiş zamanı alanına saat dilimi içeren ISO tarih girilmelidir. Geçmiş veya boş tarihte sayaç gösterilmez.
- Sahte/örnek yorumlar, demo karşılaştırmalar, tekrarlanan satış alanları yayındaki akıştan çıkarıldı. Eski bölümler düzenleyicide kapalı halde korunur; örnek yorum metinleri temizlendi.
- Manuel puan/sayı gösterimi başlangıçta kapatıldı. Gerçek veriniz varsa düzenleyiciden açıp güncelleyebilirsiniz.
- Yapılandırması doğrulanamayan paket indirim önizlemeleri başlangıçta sıfırlandı. Gerçek Shopify indirimleri sepette hesaplanır. İndirim yüzdelerini yeniden açacaksanız Shopify yönetim panelindeki kampanyanızla eşleştirin.
- Koleksiyona yönlenen hatalı sosyal ağ bağlantıları kaldırıldı. Linki olmayan mobil uygulama indirme alanı kapatıldı.
- Ürün, giriş, soru ve iletişim alanlarında kontrast, klavye ile kullanım ve odak görünümü iyileştirildi.
- Ürün JSON-LD verisi Shopify'ın gerçek ürün verisiyle üretilecek şekilde eklendi.

## Doğrulama ve sınırlar

- 107 bölüm ve 17 JSON şablonu incelendi; Shopify Theme Check: 0 hata, 36 uyarı.
- Kalan uyarılar mevcut temanın büyük ayar grupları ve kod bakımına ilişkindir: 29 ExcessiveSettingsCount, 5 UnusedDocParam, 1 BlockIdUsage, 1 LiquidComplexity. Shopify'ın 250 ayarlık yükleme sınırını geçen bölüm yoktur. 40 ayar uyarısı, Theme Check'in daha düşük bakım önerisidir.
- 83 JavaScript varlığı sözdizimi kontrolünden geçti. Yeni bölümler ve 16 mağaza şablonunun özel bölümleri örnek verilerle render edildi; gömülü scriptler de ayrıştırıldı.
- Ana sayfa ve ürün özel bölümleri 320, 375, 390, 768, 1024 ve 1440 px genişliklerde; destek sayfaları mobil/masaüstünde tarayıcıyla kontrol edildi.
- Varyant, paket, stok kuralı, sepet ekleme, stok hatasından dönme, indirim yönlendirmesi, klavye ile SSS açma ve JavaScript kapalıyken native form dahil 43 tarayıcı kontrolü geçti. Örnek verili ana sayfa, ürün, iletişim ve SSS içeriklerinde ciddi/kritik erişilebilirlik ihlali bulunmadı.
- Otomatik sayfa seçimi, boş blogu gizleme, mevcut yazıyı hariç tutma ve JavaScript sözdizimi dahil 91 ek kontrol geçti.

Bu testler yerel tarayıcıda örnek ürünler ve taklit Shopify sepet uçlarıyla yapıldı. Canlı mağazada ödeme tahsilatı, kargo uygulamaları, captcha/e-posta teslimi ve harici uygulamalar için gerçek bir deneme siparişi henüz yapılmadı. Tema otomatik yayımlanmadı.

### ZIP'in kapsamı

Shopify ürün kayıtları, mevcut sayfa metinleri, blog yazılarının tam içerikleri, menü kayıtları ve politikalar tema ZIP'inde saklanmaz; mağazanın yönetim panelinde saklanır. Bu nedenle tema şablonları ve bölüm akışları incelendi; ZIP'te bulunmayan blog yazısı metinleri tek tek okunamadı. Tema güncellemesi mevcut kayıtları silmez veya yeni Shopify sayfa/blog kayıtları oluşturmaz.

Teslimat ve iade alanları, mağazada politika tanımlıysa doğrudan o içeriği gösterir. Politika yoksa yeni metin uydurmaz; süreç hakkında genel yönlendirme sunar. Mağazanızdaki gerçek koşulları Shopify → Ayarlar → Politikalar bölümüne girin.
