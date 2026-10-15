# Wytamin referans ürün sayfası

Gönderdiğiniz referansın yerleşimi Shopify Liquid ile hazırlandı: beyaz zemin, lacivert metin, mavi bilgi kutuları, kırmızı satın alma alanı, dikey küçük görseller, paket kartları ve yorumlar.

## Dosyalar

- `sections/wytamin-product.liquid`: ürün sayfası. Stil ve JavaScript aynı dosyada bulunur; harici paket gerekmez.
- `sections/wytamin-header.liquid`: marka, arama, kargo/ödeme/destek metinleri, hesap ve sepet bağlantıları.
- `templates/product.wytamin.json`: ürün bölümünü ve varsayılan fayda/içerik/paket bloklarını seçen ürün şablonu.
- `Wytamin-Referans-Kodlar.zip`: mevcut temanıza eklemek için yalnızca yukarıdaki kodlar ve bu belge. Tam tema ZIP'i olarak yüklemeyin.
- `Wytamin-Referans-Tema.zip`: önceki temanın bu başlık ve ürün sayfası etkinleştirilmiş tam sürümü; Shopify'a yeni tema olarak yüklenebilir.

Önceki Product Studio sürümü korunmuştur. Yeni dosyalar ayrı adlarla eklendi.

## Hazır temayı yükleme

1. Shopify → Online Mağaza → Temalar → Tema ekle → ZIP yükle adımından `Wytamin-Referans-Tema.zip` dosyasını yükleyin.
2. Yeni temayı özelleştirin, bir ürün sayfasını açın. Ürün adı, seçenekler, fotoğraflar, fiyat ve stok Shopify'daki üründen gelir.
3. `Wytamin Ürün Sayfası` bölümünde açıklama, içerik/fayda blokları ve paket kartlarını kendi ürününüzle eşleştirin.
4. Header'daki marka/logo ve kargo/destek metinlerini düzenleyin. Hazır tema başlığı mağazanın tüm sayfalarında kullanır.
5. Önizlemede ve Shopify test ödeme modunda kontrol ettikten sonra yayımlayın.

## Mevcut temaya yalnızca kodları ekleme

1. Mevcut temanızı çoğaltıp yedek alın.
2. Kodu düzenle bölümünden iki Liquid dosyasını `sections/` klasörüne ve ürün şablonunu `templates/` klasörüne ekleyin. Shopify kod editöründe `.liquid` dosyaları için uygun dosya adını kullanın.
3. Ürünün yönetim sayfasında Tema şablonu alanında `wytamin` şablonunu seçin. Yeni tema henüz yayımlı değilse önce tema düzenleyicisindeki ürün şablonu seçicisinde önizleyin; ürüne atama yayımlı temanın şablonlarına bağlıdır.
4. Üst başlık için tema düzenleyicisindeki Header/Üst bilgi grubuna `Wytamin Üst Başlık` bölümünü ekleyin. İki başlık görünmemesi için mevcut header bölümünü kaldırın veya gizleyin. Tema düzenleyicisi buna izin vermiyorsa kopya temanın `sections/header-group.json` dosyasında yeni başlığı seçin.
5. Yalnızca ürün bölümü isteniyorsa yeni header'ı eklemek zorunda değilsiniz; mevcut mağaza başlığıyla çalışır.

## Gerçek veri ve ayarlar

- Fiyatlar, karşılaştırma fiyatları ve stok ürünün seçili varyantından okunur. Sepet güncellemesinden sonra otomatik indirimler Shopify yanıtından gösterilir.
- 1/2/3 paket kartları aynı ürünün adetlerini seçer. Her paketin başlığı, açıklaması, adedi ve görseli düzenlenebilir. Kart için ayrı görsel seçerek referanstaki gibi arka plansız ürün fotoğrafı kullanabilirsiniz.
- Ekrandaki paket tutarı, gerçek Shopify fiyatıdır. Referanstaki 1.250/1.990/2.690 fiyatları koda sabit yazılmamıştır. Örneğin iki adet seçilince indirim oluşmasını istiyorsanız Shopify İndirimler alanında bu kuralı oluşturun. Seçilmemiş paketlerde henüz doğrulanmamış bir indirim gösterilmez.
- Üst görsel kampanya etiketi ve rozet görseli isteğe bağlıdır. Referanstaki yüzde veya satış liderliği iddiası otomatik eklenmez.
- Stok Shopify tarafından takip ediliyor ve stok aşımı kapalıysa gerçek kalan adet gösterilir. Aksi durumda yalnızca satın alınabilirlik gösterilir.
- Sayaç için saat dilimi içeren gerçek bitiş tarihi girin: `2026-12-31T23:59:59+03:00`. Boş/geçersiz tarihte gizlenir; bitince durur. Shopify indirim kuralını otomatik başlatmaz/durdurmaz.
- Değerlendirme puanı/sayısı önce ürünün `reviews.rating` / `reviews.rating_count` metafield verisinden, yoksa bölümde girilen gerçek değerlerden okunur. Yorum kartları yalnızca sizin eklediğiniz yorum bloklarıyla görünür.
- Doğrulanmış satıcı etiketi varsayılan olarak kapalıdır. Gerçek durumunuz uygunsa açın.
- Ücretsiz kargo, aynı gün kargo ve benzeri metinleri yalnızca mağazanızın koşullarıyla uyumluysa yazın. Varsayılanlar teslimat politikasına yönlendiren nötr metinlerdir.
- Ödeme ikonları `shop.enabled_payment_types` değerlerinden gelir; etkin olmayan ödeme yöntemleri varsayılmaz.

## Kontroller ve sınırlar

Yerel Chromium testleri galeriyi, varyantları, fiyatları, stok durumunu, miktar kurallarını, gerçek sepet yanıtlarından indirim gösterimini, diğer ürünleri korumayı, stok hatasını, doğrudan satın almayı, sayaç bitişini ve tema düzenleyicisinde yeniden yüklemeyi kapsar. Başlık ve bölüm için renk kontrastı dahil erişilebilirlik taraması yapılır. 320, 390, 768, 1024, 1440 ve 1680 piksel ekranlar kontrol edilir.

Önizlemeler çizim olarak üretilmiş örnek ürün görselleri ve test verileriyle oluşturulmuştur. Gerçek fotoğraflar, yorumlar ve ürün dosyaları tema ZIP'inde bulunmaz; mağazanızdan gelir. Eski temadan taşınan mağazaya özel `shopify://shop_images/...` bağlantıları başka mağazada yeniden seçilmelidir.

Gerçek Shopify ödeme, Markets, mağaza uygulamaları ve stok/indirim koşulları bağlı mağazada ayrıca doğrulanmalıdır. Bu işlem canlı Shopify temasını yayımlamaz.
