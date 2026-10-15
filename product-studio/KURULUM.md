# MarketVitrini Product Studio

Gönderilen tek ürün / 1–2–3 adet ürün bölümü; krem zemin, koyu yeşil aksanlar, büyük galeri, net ürün bilgileri ve düzenli bir sipariş özetiyle yeniden tasarlandı.

## Mevcut temada yalnızca bu bölümü değiştirme

1. Shopify → Online Mağaza → Temalar alanında mevcut temayı çoğaltın.
2. Kopya temada Kodu düzenle → `sections/product-information.liquid` dosyasını açın.
3. Önce mevcut dosyayı yedekleyin; ardından bu klasördeki `product-information.liquid` dosyasının tamamını yerine yapıştırıp kaydedin.
4. Ürün sayfasını tema düzenleyicisinde açıp ürün bölümünün renklerini ve yeni **Studio tasarım metinleri** ayarlarını düzenleyin.
5. Önizlemede seçenekleri, paketleri ve sepeti kontrol edin. Hazır olduğunda temayı yayımlayın.

Bu Liquid dosyası tek başına çalışacak biçimde hazırlanmıştır; ek CSS/JS dosyası yüklemek gerekmez. Mevcut 248 şema girdisi korunmuştur. Yeni tasarım için bir başlık grubu ve 9 metin ayarı eklenmiştir. Eski tasarımdaki artık kullanılmayan bazı ayarlar da mevcut mağaza yapılandırmalarının okunabilmesi için tutulur.

Mevcut bölümün kayıtlı renkleri yeni varsayılanları ezebilir. Önizlemedeki palet için:

- Bölüm zemini: `#F5F5F0`
- Buton başlangıcı: `#1D5146`
- Buton bitişi: `#153F36`
- Başlık ve fiyat: `#202C2A`
- Görsel zemini: `#ECEEE5`
- Çerçeve: `#DDE2DA`
- Görsel yerleşimi: Tamamını göster
- Kart köşesi: 22 px

## Hazır tema ZIP'i

Depo kökündeki `Marketvitrini-Product-Studio-Tema.zip`, önceki geliştirilmiş temanın bu bölüm eklenmiş tam sürümüdür. Shopify → Temalar → Tema ekle → ZIP yükle adımından yüklenebilir. Bu ZIP'te ürün şablonu zaten `product-information` bölümünü kullanır ve yeni renkler uygulanmıştır.

Tema, canlı mağazanın ürünlerini veya medya dosyalarını taşımaz. Ürün/görsel bağlantılarını kendi mağazanızda kontrol edin. Başka mağazadan gelen `shopify://shop_images/...` dosyaları yeniden seçilmelidir.

## Görünüm ve işlevler

- Masaüstünde büyük galeri, ürün bilgileri ve yapışkan sipariş özeti; mobilde galeri → bilgiler → paketler → özet sırası.
- Küçük görsel seçimi, önceki/sonraki kontrolleri ve klavye ile galeri kullanımı.
- Ürün özeti, fiyat, karşılaştırma fiyatı, adet ve varyant alanları için tek görsel sistem.
- 1/2/3 adet paket kartları, seçili paket işareti ve gerçek Shopify indirimlerinin gösterimi.
- Ana sepete ekle butonu. Sepet boşken adet değişimi yalnızca seçim yapar; butona basılmadan ürün eklemez.
- Diğer ürünleri, abonelik satırlarını ve özel özellikli satırları koruyan sepet güncellemesi.
- Yeni seçenek eklenemezse eski sepet satırı korunur; hata mesajı görünür kalır.
- Tema düzenleyicisindeki bölüm kaldırma/yenileme işlemlerinde olay dinleyicileri temizlenir.
- İlk ürün görseli öncelikli yüklenir, diğerleri ertelenir. Tekrarlı stil katmanları tek bir kapsamlı stil bloğuna indirildi.

Paket indirimi tema tarafından yaratılmaz. Shopify yönetiminde geçerli bir indirim tanımlandığında gerçek tutar sepette gösterilir. Kupon, ödeme ekranında Shopify tarafından doğrulanır. Stok/yorum/kampanya metinlerini kendi gerçek verilerinizle doldurun.

## Önizlemeler ve doğrulama

`onizleme-masaustu.png` ve `onizleme-mobil.png` örnek bir blender çizimi ve test ürün/sepet verileri kullanır. Ürün adı, görseller ve fiyatlar gerçek mağazada Shopify verilerinden gelir. Önizleme başlığındaki örnek mağaza menüsü bölüm dosyasının parçası değildir.

Yeni bölümün 10 Chromium testi geçti; mevcut 20 test de geçti. 320, 390, 768, 1024 ve 1440 piksel ekranlarda taşma kontrol edildi. Bölümün erişilebilirlik taramasında renk kontrastı dahil ciddi/kritik ihlal bulunmadı. Shopify Theme Check: 0 hata, 36 uyarı. Uyarılar geniş ayar listeleri ve mevcut tema analiz önerilerini içerir.

Testler yerel bileşen ortamında ve kontrollü Shopify sepet yanıtlarıyla çalışır. Canlı ödeme, mağaza uygulamaları, Markets dönüşümleri ve gerçek stok/indirim koşulları bağlı mağazada ayrıca doğrulanmalıdır. Bu çalışma canlı Shopify temasını yayımlamaz.
