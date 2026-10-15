# Yüklenen Marketvitrini temasına Wytamin uyarlaması

Bu sürüm, son gönderdiğiniz `Marketvitrini-Gelistirilmis-Tema.zip` dosyası temel alınarak hazırlandı. Önceki genel tema paketinin yerine, yüklediğiniz temanın kendi içerik ve ayarlarına uyarlanmış sürümdür.

## Yükleme

1. `Marketvitrini-Wytamin-Uyarlanmis-Tema.zip` dosyasını indirin.
2. Shopify → Online Mağaza → Temalar → Tema ekle → ZIP dosyası yükle adımını kullanın.
3. Yeni temada bir ürün sayfasını önizleyin. Wytamin düzenindeki ürün bölümü varsayılan olarak seçilmiştir.
4. Logo, ürün görselleri, mevcut ürün metinleri, paketler ve sipariş işlemlerini kontrol edin. Hazır olduğunuzda yeni temayı yayımlayın.

Kodları tek tek eklemeniz gerekmez. Ana sayfanın orijinal başlığı korunmuştur; yeni başlık varsayılan olarak yalnızca ürün sayfalarında görünür. Eski başlık aynı sayfada gizlenir, böylece çift başlık oluşmaz. Mevcut duyuru çubuğu korunur.

## Korunanlar

- Yüklenen temadaki 549 dosyanın tamamı arşivde bulunur.
- Global tema ayarları, logo bağlantısı, ana sayfa, alt bilgi, sepet ve diğer sayfa dosyaları değiştirilmedi.
- Ürün sayfasındaki mevcut ek bölümler, yorum alanı ve sabit alışveriş çubuğu korundu.
- Önceki ana ürün bölümü tüm ayarlarıyla `mv_previous_product` adı altında kapalı olarak saklandı.
- Mevcut altı ürün özelliği yeni fayda kutusuna, 1/2/3 adet paketleri yeni paket kartlarına, kargo/destek/iade metinleri yeni güven alanlarına taşındı.
- Kayıtlı logo yeni ürün başlığında yeniden kullanılır. Varsayılan örnek marka adı yerine temada kayıtlı NeuroX adı kullanılır; logo yüklüyse görsel logo gösterilir.

## Değişenler

- `templates/product.json`: yeni ürün bölümü etkin; önceki ana bölüm kapalı; diğer bölümler korunmuş durumda.
- `sections/header-group.json`: mevcut başlık ve duyuru ayarları korunarak ürün sayfasına özel yeni başlık eklendi.
- Yeni dosyalar: `sections/wytamin-product.liquid`, `sections/wytamin-header.liquid`, `templates/product.wytamin.json`.

Bölüm açıklaması boş bırakıldığında Shopify ürün açıklaması kullanılır. Ürün adı, görseller, fiyat, stok ve seçenekler gerçek üründen gelir. Görseller mağazaya bağlıdır; farklı mağazaya yüklüyorsanız `shopify://shop_images/...` bağlantılarını yeniden seçin.

Yeni sayaç yalnızca gerçek bir bitiş tarihi girildiğinde görünür. Doğrulanmış satıcı veya örnek yorumlar otomatik eklenmez. Paket indirimleri Shopify'da ayrıca tanımlanmalı; gerçek sonuç sepette gösterilir.

## Geri dönüş

Kopya temanın ürün şablonunda yeni ana bölümü kapatıp `mv_previous_product` bölümünü açabilirsiniz. Header grubunda `wy_product_header` bölümünü kapattığınızda eski başlık tekrar görünür. Yükleme mevcut yayımlanmış temayı kendiliğinden değiştirmez.

## Doğrulama

- Uyarlamaya özel 7 test geçti: içerik/ayar koruması, logo, ürün/ana sayfa başlık ayrımı, çift başlık engeli, açıklama, paket-sepet-sayaç bağlantısı ve mobil/masaüstü taşma.
- Shopify Theme Check: 0 hata, 36 mevcut uyarı.
- Paket bütünlüğü ve tüm orijinal dosyaların korunması kontrol edildi. Mevcut dosyalardan yalnızca iki yapılandırma dosyası değişti.
- Canlı Shopify ödeme, Markets, uygulamalar ve gerçek stok/indirim koşulları yerel test ortamında çalıştırılmadı; mağaza önizlemesinde ayrıca kontrol edilmelidir.
