---
title: Çevrimiçi ve çevrimdışı satış noktası (POS) işlemleri
description: Bu konu, Dynamics 365 Commerce içinde satış noktası (POS operasyonları hakkında bilgi verir). Uygulamada işlemlerin nereden çağrılabileceğini ve çevrimdışı modda kullanılabilir olup olmadığını belirtir.
author: jblucher
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-09-27
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 141b57586f5c4588b0b33bd85b584e570e39902f
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462509"
---
# <a name="online-and-offline-point-of-sale-pos-operations"></a>Çevrimiçi ve çevrimdışı satış noktası (POS) işlemleri

[!include [banner](includes/banner.md)]

Kullanıcıların satış noktasında (POS) gerçekleştirdiği çoğu eylem işlem olarak kabul edilir. Operasyonlar Dynamics 365 Commerce arka ofiste yapılandırılır ve yönetilir. Çoğu işlem POS düğme grubundaki düğmelere eklenebilir. Kullanıcılar daha sonra işlemleri başlatmak ve işlevlerini gerçekleştirmek için düğmeleri seçebilir. Diğer işlemler ana POS uygulamasının parçalarıdır ve ekran düğmeleri veya diğer iş akışları veya süreçleri tarafından başlatılır.

Aşağıdaki tablo, Modern POS ve Bulut POS için Bulut POS'ta bulunan operasyonlar hakkında ayrıntıları sağlar. Tablo uygulamada işlemlerin nereden çağrılabileceğini ve POS çevrimdışı moddayken kullanılabilir olup olmadığını da belirtir.

Bazı operasyonlar şu anda Modern POS veya Bulut POS içinde kullanılabilir değildir. Bu işlemlerin bazıları bölgeye özgü işlemlerdir ve ek uzantılar ve yapılandırma gerektirir. Bazıları ise Microsoft Dynamics AX 2012'den gelen ve şu an desteklenmeyen özelliklerdir.

Aşağıdaki sütunlar işlemlerin nereden çağrılabileceğini belirtir:

- **Düğme grubu**: İşlem POS ekran düzeninin bir parçası olan POS düğme grubundaki düğmelere atanabilir.
- **Hareket ekranı**: İşlem POS hareket ekranı üzerinde yapılandırılmış olan POS düğme gruplarından çağrılabilir.
- **Karşılama ekranı**: İşlem POS karşılama ekranı üzerinde yapılandırılmış olan POS düğme gruplarından çağrılabilir.

> [!NOTE]
> Aşağıda listelenen işlemler, Commerce'ın en son sürümü için geçerlidir. Bazı işlemler değişmiş veya önceki sürümlerde bulunmuyor olabilir.


| Kod | Operasyon | Tanım | Düğme grubu | Hareket ekranı | Hoş geldiniz ekranı | Çevrimdışı kullanılabilir | Konuma özgü |
|----|-----------|-------------|-------------|--------------------|----------------|-------------------|-----------------|
| 707 | Aygıtı etkinleştir | Kimliği doğrulanmış kullanıcının bağlantı bilgilerini sağlamasına izin vererek geçerli cihazı etkinleştirin, bir cihaz ve kayıt kimliği atayın. | Hayır | Hayır | Hayır | Hayır | Hayır |
| 134 | İlişki ekle | Bir harekete önceden seçilmiş bir ilişki ekleyin. İlişkiyi **Düğme özellikleri** sayfasından seçin. | Evet | Evet | Hayır | Evet | Hayır |
| 135 | Listeden ilişki ekle | Bir listeden seçerek bir harekete bir ilişki ekleyin. | Evet | Evet | Evet | Evet | Hayır |
| 137 | Müşteriye ilişki ekleme | Müşteriye bir ilişkiyi **Müşteri ayrıntıları** sayfasından ekleyin. | Hayır | Hayır | Hayır | Evet | Hayır |
| 138 | Müşteriden ilişkiyi kaldırma | İlişkiyi **Müşteri ayrıntıları** sayfasından kaldırın. | Hayır | Hayır | Hayır | Evet | Hayır |
| 643 | Kupon kodunu ekle | POS'ta kodunu girerek bir kupon ekleyin. | Evet | Evet | Hayır | Evet | Hayır |
| 141 | Başlık masrafları ekle | Sipariş başlığına sair gider ekleyin. | Evet | Evet | Hayır | Hayır| Hayır |
| 141 | Satır masrafları ekle | Seçili bir satış satırına sair gider ekleyin. | Evet | Evet | Hayır | Hayır| Hayır |
| 117 | Bağlılık programı kartı ekle | Kullanıcıdan geçerli harekete eklenecek olan bir bağlılık kartı numarası girmesini isteyin. | Evet | Evet | Hayır | Evet | Hayır |
| 136 | Seri numarası ekle | Bu işlem kullanıcının seçili ürün için bir seri numarası belirtmesine izin verir. | Evet | Evet | Hayır | Evet | Hayır |
| 1214 | Sevkiyat adresi ekle | Bu işlem desteklenmez. | Uygulanamaz | Uygulanamaz | Uygulanamaz | Uygulanamaz | Hayır |
| 519 | Hediye kartına ekle | Belirtilen hediye kartına para ekleyin. | Evet | Evet | Hayır | Hayır | Hayır |
| 6000 | Mali kaydı atlamaya izin ver | Bu işlem desteklenmez. | Uygulanamaz | Uygulanamaz | Uygulanamaz | Uygulanamaz | Evet |
| 1212 | Bankaya para nakli | Bankaya gönderilen para miktarını ve banka torba numarası gibi diğer bilgileri kaydedin. | Evet | Evet | Evet | Evet | Hayır |
| 923 | Banka toplamları doğrulaması | Bu işlem desteklenmez. | Uygulanamaz | Uygulanamaz | Uygulanamaz | Uygulanamaz | Evet |
| 915 | Boş işlem | Bu işlem işletmenin gereksinim duyduğu herhangi bir özel işlem için, bir yazılım geliştirici tarafından program vasıtasıyla değiştirilebilen, özelleştirilebilir bir düğmeyi gösterir. | Evet | Evet | Evet | Evet | Hayır |
| 1053 | Vardiyayı tamamen kapat | Geçerli vardiyayı tamamen kapalı olarak ayarlar ve kullanıcı oturumunu kapatır. Tamamen kapalı bir vardiya ek hareketlere kapalıdır ancak ödeme kaldırma veya ödeme beyanı gibi çekmece işlemleri için açık kalır. | Evet | Evet | Evet | Hayır | Hayır |
| 310 | Toplamı hesapla | İskonto hesaplaması ertelendiğinde, bu işlem geçerli hareket için hesaplamayı başlatır. | Evet | Evet | Hayır | Evet | Hayır |
| 642 | Tüm Ürünleri Gerçekleştir | Tüm satırlar için teslimat modunu **Teslim alınan** olarak ayarlayın. | Evet | Evet | Hayır | Evet\* | Hayır |
| 641 | Seçilen Ürünleri Gerçekleştir | Tüm seçili satırlar için teslimat modunu **Teslim alınan** olarak ayarlayın. | Evet | Evet | Hayır | Evet\* | Hayır |
| 647 | Teslimat şeklini değiştir | Önceden yapılandırılmış sevkiyat satış satırları için teslimat şeklini değiştirin. | Evet | Evet | Hayır | Hayır| Hayır |
| 1215 | Parolayı değiştir | Bu işlem, POS kullanıcısının parolasını değiştirmesini sağlar. | Evet | Evet | Evet | Hayır | Hayır |
| 123 | Ölçü birimini değiştir | Seçilen satır maddesi için ölçü birimi değiştirin. | Evet | Evet | Hayır | Evet | Hayır |
| 639 | Hareketteki varsayılan satış temsilcisini temizle | Komisyon satış grubunu (satış temsilcisi) hareketten kaldırın. | Evet | Evet | Hayır | Evet | Hayır |
| 106 | Miktarı temizle | Seçili satırdaki miktarı **1** olarak sıfırlayın. | Evet | Evet | Hayır | Evet | Hayır |
| 640 | Satırdaki satış temsilcisini temizle | Komisyon satış grubunu (satış temsilcisi) seçili satırdan kaldırın. | Evet | Evet | Hayır | Evet | Hayır |
| 121 | Satış temsilcisini sil | Bu işlem desteklenmez. | Uygulanamaz | Uygulanamaz | Uygulanamaz | Uygulanamaz | Hayır |
| 1055 | Vardiyayı kapat | Geçerli vardiyayı kapatın, Z raporu yazdırın ve kullanıcının sistemdeki oturumunu kapatın. | Evet | Evet | Evet | Hayır | Hayır |
| 139 | Hareketi sonlandır | Kullanıcıdan ödeme yöntemini seçmesini ister | Evet | Evet | Hayır | Evet | Hayır |
| 925 | Banka çekini kopyala | Bu işlem desteklenmez. | Uygulanamaz | Uygulanamaz | Uygulanamaz | Uygulanamaz | Evet |
| 620 | Müşteri siparişi oluştur | POS hareketini bir müşteri siparişine dönüştürün. | Evet | Evet | Hayır | Evet\* | Hayır |
| 621 | Teklif oluştur | POS hareketini bir satış teklifine dönüştürün. | Evet | Evet | Hayır | Evet\* | Hayır |
| 636 | Perakende hareketi oluşturma | Varsayılan POS davranışı müşteri siparişleri oluşturmak olduğunda, kullanıcının standart bir satış hareketi oluşturun. | Evet | Evet | Hayır | Evet | Hayır |
| 600 | Müşteri | Belirtilen müşteriyi harekete ekleyin. | Hayır | Hayır | Hayır | Evet | Hayır |
| 1100 | Müşteri hesabı havalesi | Bir müşterinin hesabına ödeme yapın. | Evet | Evet | Evet | Evet | Evet |
| 612 | Müşteri ekleme | Yeni bir müşteri kaydı oluşturun. | Evet | Evet | Evet | Evet† | Hayır |
| 603 | Müşteri silme | Müşteriyi geçerli hareketten kaldırın. | Evet | Evet | Hayır | Evet | Hayır |
| 602 | Müşteri araması | POS'taki müşteri arama sayfasına giderek bir müşteri kaydı arayın. | Evet | Evet | Evet | Evet | Hayır |
| 609 | Müşteri hareketleri | Bu işlem desteklenmez. | Uygulanamaz | Uygulanamaz | Geçerli değil | Geçerli değil | Hayır |
| 917 | Veritabanı bağlantı durumu | Geçerli bağlantı ayarlarını görüntüleyin ve çevrimdışı ve çevrimiçi modları arasında geçiş yapın. | Evet | Evet | Evet | Evet | Hayır |
| 1200 | Başlangıç tutarını beyan et | Gün veya vardiya başlangıcında kasa çekmecesindeki tutarı bildirir. | Evet | Evet | Evet | Evet | Hayır |
| 132 | Havale geçersiz kılma | Müşteri siparişleri için varsayılan havaleyi geçersiz kılın. | Evet | Evet | Hayır | Evet\* | Hayır |
| 913 | Tasarım modunu devre dışı bırakma | Bu işlem desteklenmez. | Uygulanamaz | Uygulanamaz | Uygulanamaz | Uygulanamaz | Hayır |
| 912 | Tasarım modunu etkinleştirme | Bu işlem desteklenmez. | Uygulanamaz | Uygulanamaz | Uygulanamaz | Uygulanamaz | Hayır |
| 1217 | Setleri ayrıştır | Bir seti bileşen ürünlerine ayrıştırın. | Evet | Evet | Evet | Evet | Hayır |
| 624 | İade tutarlarını görüntüle | Bu işlem desteklenmez. | Uygulanamaz | Uygulanamaz | Uygulanamaz | Uygulanamaz | Evet |
| 513 | Toplamı göster | Hareketin bakiyesini müşteri ekranında göster. | Evet | Evet | Evet | Evet | Hayır |
| 623 | Müşteri düzenle | Geçerli müşteri ayrıntılarını düzenleyin. | Evet | Evet | Hayır | Hayır | Hayır |
| 614 | Müşteri siparişini düzenle | POS'ta değiştirilebilmesi için seçili siparişi geri çağırın. | Hayır | Hayır | Hayır | Hayır | Hayır |
| 615 | Teklifi düzenle | POS'ta değiştirilebilmesi için seçili teklifi geri çağırın. | Hayır | Hayır | Hayır | Hayır | Hayır |
| 518 | Gider hesapları | Arada sırada oluşan giderler için para çekmecesinden çekilen parayı kaydedin. | Evet | Evet | Evet | Evet | Hayır |
| 919 | Genişletilmiş oturum açma | Bir barkod tarayarak veya kart geçirerek oturum açma izni atayın veya kaldırın. | Evet | Evet | Evet | Evet | Hayır |
| 1201 | Kasa devri girişi | Geçerli bölüm veya vardiyaya ek para ekleyin. | Evet | Evet | Evet | Evet | Hayır |
| 1218 | Çevre biriminin kilidini açmaya zorla | Sistem bu işlemi POS çevre birimlerinin kilidini açmak için dahili olarak kullanır. | Uygulanamaz | Uygulanamaz | Uygulanamaz | Uygulanamaz | Hayır |
| 520 | Hediye kartı bakiyesi | Hediye kartı bakiyesini görüntüleyin. | Evet | Evet | Hayır | Hayır | Hayır |
| 708 | Cihazı devre dışı bırak | POS kayı olarak kullanılabilmesi için geçerli cihazı devre dışı bırakın. | Hayır | Hayır | Hayır | Hayır | Hayır |
| 804 | Gelen işlem | Gelen mağaza stok yönetimi özelliklerine erişin. | Evet | Hayır | Evet | Hayır| Hayır |
| 517 | Gelir hesapları | Satış dışındaki bir nedenle kasa çekmecesine yerleştirilen parayı kaydedin. | Evet | Evet | Evet | Evet | Hayır |
| 801 | Stok arama | Geçerli mağaza ve diğer kullanılabilir konumlar için kullanılabilir, sipariş ve karşılanabilir miktar (KM) miktarlarını arayın. | Evet | Evet | Evet | No. | No. |
| 806 | Stok düzeltmesi | Ayarlama veya taşıma günlüğünü kullanarak mağaza deposunun stokta var ve stokta yok durumunu ayarlayın. | Evet | Evet | Evet | No. | No. |
| 807 | Stok hareketi | Mağaza deposunda maddeleri bir stok konumundan başka bir stok konumuna taşıyın. | Evet | Evet | Evet | No. | No. |
| 122 | Fatura açıklaması | Geçerli harekete yorum ekleyin. | Evet | Evet | Hayır | Evet | Hayır |
| 511 | Alacak faturası düzenle | İade yerine fiş vermek için bir alacak faturası düzenleyin. | Evet | Evet | Hayır | Hayır | Hayır |
| 512 | Hediye kartı ver | Belirtilen tutar için yeni bir hediye kartı düzenleyin. | Evet | Evet | Hayır | Hayır | Hayır |
| 625 | Bağlılık programı kartı ver | Müşterinin mağaza bağlılık programına katılabilmesi için müşteriye bir bağlılık kartı düzenleyin. | Evet | Evet | Evet | Hayır | Hayır |
| 300 | Satır indirim tutarı | Hareketteki satır maddesi için bir indirim tutarı girin. Bu işlem yalnızca indirim yapılabilir maddeler içindir ve belirtilen indirim sınırları dahilindedir. | Evet | Evet | Hayır | Evet | Hayır |
| 301 | Satır iskontosu yüzdesi | Hareketteki satır maddesi için bir indirim yüzdesi girin. Bu işlem yalnızca indirim yapılabilir maddeler içindir ve belirtilen indirim sınırları dahilindedir. | Evet | Evet | Hayır | Evet | Hayır |
| 703 | Kaydı kilitle | Kullanılamaması için geçerli kaydı kilitler ancak kullanıcı oturumunu kapatmaz. | Hayır | Hayır | Hayır | Evet | Hayır |
| 701 | Oturumu kapat | Geçerli kullanıcının kayıt oturumunu sonlandırır. | Evet | Evet | Evet | Evet | Hayır |
| 521 | Bağlılık programı kartı puanı bakiyesi | Belirtilen bağlılık programı kartının puan bakiyesi gösterin. | Evet | Evet | Hayır | Hayır | Hayır |
| 142 | Masrafları yönet | Harekete uygulanan sair giderleri görüntüleyin ve yönetin. | Evet | Evet | Hayır | Hayır| Hayır |
| 918 | Vardiyaları yönet | Etkin, beklemeye alınmış ve kapalı vardiyaların listesini görüntüleyin. | Evet | Evet | Evet | Hayır | Hayır |
| 914 | POS penceresini simge durumuna küçült | Bu işlem desteklenmez. | Uygulanamaz | Uygulanamaz | Uygulanamaz | Uygulanamaz | Hayır |
| 1000 | Çekmeceyi aç | "Satış yok" işlemi gerçekleştirin ve seçili olan kasa çekmecesini açın. | Evet | Evet | Evet | Evet | Hayır |
| 928 | Sipariş karşılama | Bu işlem kullanıcıların siparişleri mağazadan çekme işlemi için çekmesine, paketlemesine, sevk etmesine veya geri çağırmasına olanak tanır. | Evet | Evet | Evet | Hayır | Hayır |
| 805 | Giden işlem | Giden transfer emirlerinin sevkiyatları yönetimine ilişkin özelliklere erişin. | Evet | Hayır | Evet | Hayır| Hayır |
| 129 | Satır ürünü vergisini geçersiz kıl | Seçilen satır maddesindeki vergi geçersiz kılın ve farklı bir vergi kullanın. | Evet | Evet | Hayır | Evet | Hayır |
| 130 | Listedeki satır ürünü vergisini geçersiz kıl | Seçilen satır maddesindeki vergiyi geçersiz kılın ve kullanıcının listeden seçtiği bir vergiyi kullanın. | Evet | Evet | Hayır | Evet | Hayır |
| 127 | Hareket vergisini geçersiz kıl | Hareketteki vergiyi geçersiz kılın ve farklı bir vergi kullanın. | Evet | Evet | Hayır | Evet | Hayır |
| 128 | Listeden hareket vergisini geçersiz kıl | Hareketteki vergiyi geçersiz kılın ve kullanıcının listeden seçtiği bir vergiyi kullanın. | Evet | Evet | Hayır | Evet | Hayır |
| 131 | Sevk irsaliyesi | Seçili sipariş için bir sevk irsaliyesi oluşturun. | Hayır | Hayır | Hayır | Hayır | Hayır |
| 710 | Donanım istasyonunu eşleştir | Bu işlem desteklenmez. | Uygulanamaz | Uygulanamaz | Uygulanamaz | Uygulanamaz | Hayır |
| 201 | Kartla ödeme | Ödeme olarak kredi kartı veya ATM kartı gibi bir kart kabul edin. | Evet | Evet | Hayır | Evet | Hayır |
| 200 | Nakit ödeme | Ödeme olarak nakit kabul edin. | Evet | Evet | Hayır | Evet | Hayır |
| 206 | Hızlı nakit ödeme | Hareketi tek dokunuşla tamamlayın ve tutarı nakit olarak kabul edin (tam değiştirme). | Evet | Evet | Hayır | Evet | Hayır |
| 204 | Çekle ödeme | Ödeme olarak çek kabul edin. | Evet | Evet | Hayır | Evet | Hayır |
| 213 | Alacak Faturasıyla Ödeme | Mağaza tarafından verilen alacak faturasını (fiş) kabul edin. | Evet | Evet | Hayır | Hayır | Hayır |
| 203 | Ödeme para birimi | Çeşitli para birimlerinde ödeme kabul edin. | Evet | Evet | Hayır | Evet | Hayır |
| 202 | Müşteri hesabıyla ödeme | Hareketi müşterinin hesabına masraflandırın. Bu ödeme yöntemi müşteri siparişi havaleleri için geçerli değildir. | Evet | Evet | Hayır | Hayır | Hayır |
| 214 | Hediye kartıyla ödeme | Mağazanın verdiği hediye kartını kabul edin. | Evet | Evet | Hayır | Hayır | Hayır |
| 207 | Bağlılık programıyla ödeme | Ödeme için bağlılık programı kartı kabul edin ve uygun ürünler için puanları kullanın. | Evet | Evet | Hayır | Hayır | Hayır |
| 634 | Ödeme geçmişi | Geçerli müşteri siparişi için müşterinin ödeme geçmişini görüntüleyin. | Evet | Evet | Hayır | Hayır | Hayır |
| 803 | Malzeme çekme ve teslim alma | **Malzeme çekme ve teslim alma** sayfasını açın. Bu sayfadan mağazada çekilecek veya teslim alınacak siparişleri seçebilirsiniz. | Evet | Evet | Evet | Hayır | Hayır |
| 632 | Tüm ürünleri çek | Karşılama yöntemini tüm satırlar için **Mağazadan çekme** olarak ayarlayın. | Evet | Evet | Hayır | Evet\* | Hayır |
| 631 | Seçilen ürünleri çek | Karşılama yöntemini seçili satırlar için **Mağazadan çekme** olarak ayarlayın. | Evet | Evet | Hayır | Evet\* | Hayır |
| 400 | Açılır menü | Bu işlem desteklenmez. | Uygulanamaz | Uygulanamaz | Uygulanamaz | Uygulanamaz | Hayır |
| 101 | Fiyat denetimi | Bu işlem kullanıcının belirli bir ürünün fiyatını aramasına izin verir. | Evet | Evet | Evet | Evet | Hayır |
| 104 | Fiyat geçersiz kılma | Ürün fiyat geçersiz kılmaya izin verecek şekilde ayarlanmışsa, ürünün fiyatını geçersiz kılın. | Evet | Evet | Hayır | Evet | Hayır |
| 1058 | Mali X raporu yazdır | Bu işlem desteklenmez. | Uygulanamaz | Uygulanamaz | Uygulanamaz | Uygulanamaz | Evet |
| 1059 | Mali Z raporu yazdır | Bu işlem desteklenmez. | Uygulanamaz | Uygulanamaz | Uygulanamaz | Uygulanamaz | Evet |
| 927 | Madde etiketini yazdır | Bu işlem desteklenmez. | Uygulanamaz | Uygulanamaz | Uygulanamaz | Uygulanamaz | Hayır |
| 926 | Raf etiketini yazdır | Bu işlem desteklenmez. | Uygulanamaz | Uygulanamaz | Uygulanamaz | Uygulanamaz | Hayır |
| 1056 | X Yazdır | Geçerli vardiya için bir X raporu yazdırın. | Evet | Evet | Evet | Hayır | Hayır |
| 103 | Ürün açıklaması | Hareketteki seçili satır maddesine açıklama ekleyin. | Evet | Evet | Hayır | Evet | Hayır |
| 100 | Ürün satışı | Harekete belirli bir ürün ekleyin. | Evet | Evet | Evet | Evet | Hayır |
| 108 | Ürün arama | POS'taki ürün arama sayfasına giderek bir ürün arayın. | Evet | Evet | Evet | Evet | Hayır |
| 633 | Bitiş tarihi teklif et | Satış tekliflerindeki bitiş tarihini görün veya değiştirin. | Evet | Evet | Hayır | Evet\* | Hayır |
| 627 | Yeniden hesapla | Geçerli yapılandırmayı temel alarak tüm müşteri siparişi satırlarını ve vergilerini yeniden hesaplayın. | Evet | Evet | Hayır | Evet\* | Hayır |
| 143 | Masrafları yeniden hesapla | Siparişe uygulanan otomatik giderleri yeniden hesaplayın. | Evet | Evet | Hayır | Hayır| Hayır |
| 515 | Siparişi geri çağır | Müşteri siparişlerini ve satış tekliflerini arayın ve geri çağırın. | Evet | Evet | Evet | Hayır | Hayır |
| 504 | Hareketi geri çağır | Daha önce askıya alınmış bir hareketi geçerli depodan geri çağırın. | Evet | Evet | Hayır | Evet‡ | Hayır |
| 305 | Bağlılık programı puanlarını kullan | Bu işlem desteklenmez. | Uygulanamaz | Uygulanamaz | Geçerli değil | Geçerli değil | Evet |
| 635 | Sevkiyat masraflarını geri öde | İptal edilen bir siparişte kargo ücretlerini iade edin. | Hayır | Hayır | Hayır | Hayır | Hayır |
| 644 | Kupon kodunu kaldır | Kullanıcıdan hareketle ilişkilendirilen kupon listesinden seçim yaparak kuponları kaldırmasını isteyin. | Evet | Evet | Hayır | Evet | No. |
| 1057 | Z'yi yeniden yazdır | Önceki vardiyanın Z raporunu yeniden yazdırın. | Evet | Evet | Evet | No. | No. |
| 1216 | Parolayı sıfırla | Bu işlem parola sıfırlama izni olan bir kullanıcının başka bir personelin parolasını geçici bir parola kullanarak sıfırlamasına olanak tanır. | Evet | Evet | Evet | Hayır | Hayır |
| 1219 | POS'ta URL Aç | POS'ta yönetici tarafından yapılandırılmış bir URL'yi açın. | Evet | Evet | Evet | Evet | Hayır |
| 109 | Ürünü iade et | Tek tek ürünler için iade gerçekleştirin. Taranan sonraki ürün, negatif miktar ve fiyatı olan iade edilmiş bir ürün olarak gösterilir. | Evet | Evet | Hayır | Evet | Hayır |
| 114 | İade hareketi | Bazı ürünleri veya ürünlerin tümünü iade etmek için önceki hareketi makbuz numarasına göre geri çağırır. | Evet | Evet | Evet | Evet§ | Hayır |
| 1211 | Kasaya para nakli | Yazar kasadan kasaya para taşımak için kasaya para nakli işlemi yapın. | Evet | Evet | Evet | Evet | Hayır |
| 516 | Satış faturası | Bu işlem müşterinin seçili satış faturası için ödeme yapmasına izin verir. | Evet | Evet | Hayır | Hayır | Hayır |
| 502 | Satış temsilcisi | POS'taki müşteri siparişleri için satış siparişindeki **Satış alıcısı** değerini ayarlayın. | Evet | Evet | Hayır | Evet\* | Hayır |
| 2000 | Planlama yönetimi | Bu işlem henüz desteklenmiyor. | Evet | Evet | Evet | Hayır | Hayır |
| 2001 | Planlama talepleri | Bu işlem henüz desteklenmiyor. | Evet | Evet | Evet | Hayır | Hayır |
| 622 | Ara | Bu işlem kullanıcıların maddeye, müşteriye veya kategoriye göre arama yapmak üzere POS düğmelerini yeniden yapılandırmasına olanak tanır. | Evet | Evet | Evet | Evet | Hayır |
| 1213 | Sevkiyat adresi ara | Bu işlem desteklenmez. | Uygulanamaz | Uygulanamaz | Geçerli değil | Geçerli değil | Hayır |
| 709 | hardware station'ı seç | Kullanılabilir donanım istasyonları listesinden bir donanım istasyonu seçin. | Evet | Evet | Evet | Evet | Hayır |
| 637 | Hareketteki varsayılan satış temsilcisini ayarla | Daha sonra eklenen satırlar için varsayılan satış temsilcisi olarak uygun komisyon satış gruplarından birini (satış temsilcileri) seçin. | Evet | Evet | Hayır | Evet | Hayır |
| 105 | Miktarı ayarla | Hareketteki bir satır maddesinin miktarını değiştirin. | Evet | Evet | Hayır | Evet | Hayır |
| 638 | Satırdaki satış temsilcisini ayarla | Seçili durumdaki satır için uygun komisyon satış gruplarından birini (satış temsilcileri) seçin. | Evet | Evet | Hayır | Evet | Hayır |
| 630 | Tüm ürünleri sevk et | Karşılama modunu tüm satırlar için **Sevkiyat** olarak ayarlayın. | Evet | Evet | Hayır | Evet\* | Hayır |
| 629 | Seçilen ürünleri sevk et | Seçili satırlar için karşılama modunu **Sevkiyat** olarak ayarlayın. | Evet | Evet | Hayır | Evet\* | Hayır |
| 115 | Günlüğü göster | Mağazanın günlüğünü görüntüleyin. Hareketleri görüntüleyebilir, makbuzları ve hediye girişlerini yeniden yazdırabilir veya iade için geri çağırabilirsiniz. | Evet | Evet | Evet | Evet\*\* | Hayır |
| 802 | Stok sayımı | Fiziksel stok veya döngü sayısı için stok sayım günlüklerini oluşturun veya değiştirin. | Evet | Evet | Evet | Hayır | Hayır |
| 401 | Alt menü | Bu işlem kullanıcıyı başka bir bağlantılı düğme grubuna götürür. | Evet | Evet | Evet | Evet | Hayır |
| 1054 | Vardiyayı askıya al | Geçerli vardiyayı askıya alın; bu durumda geçerli kayıtta yeni veya farklı bir vardiya etkinleştirilebilir. | Evet | Evet | Evet | Hayır | Hayır |
| 503 | Hareketi askıya al | Geçerli satış hareketini askıya alın; böylece daha sonra mağazada geri çağrılabilir. | Evet | Evet | Hayır | Evet‡ | Hayır |
| 1004 | Görev kaydedici | POS'taki yordam adımlarını kaydetmek için Görev kaydediciyi açın. | Hayır | Hayır | Hayır | Evet | Hayır |
| 1052 | Kasa sayımı | Her sayılan ödeme yöntemi için çekmecedeki para tutarını belirtin. | Evet | Evet | Evet | Evet | Hayır |
| 1210 | Ödeme kaldırma | Geçerli çekmeceden veya vardiyadan para çıkarın. | Evet | Evet | Evet | Evet | Hayır |
| 920 | Saat | İş vardiyalarına ve molalara giriş ve çıkış yapın. | Evet | Evet | Evet | Hayır | Hayır |
| 302 | Toplam iskonto tutarı | Hareket için bir indirim tutarı girin. Bu işlem yalnızca indirim yapılabilir maddelere ve belirtilen indirim sınırları dahilinde uygulanır. | Evet | Evet | Hayır | Evet | Hayır |
| 303 | Toplam iskonto yüzdesi | Hareket için bir indirim yüzdesi girin. Bu işlem yalnızca indirim yapılabilir maddelere ve belirtilen indirim sınırları dahilinde uygulanır. | Evet | Evet | Hayır | Evet | Hayır |
| 501 | Hareket açıklaması | Geçerli harekete açıklama ekleyin. | Evet | Evet | Hayır | Evet | Hayır |
| 922 | Ürün ayrıntılarını görüntüle | Seçili satır maddesi için ürün ayrıntıları sayfasını açın. | Evet | Evet | Hayır | Evet | Hayır |
| 1003 | Raporları görüntüle | Geçerli kullanıcı için yapılandırılmış olan raporları görüntüleyin. | Evet | Evet | Evet | Hayır | Hayır |
| 921 | Saat girişlerini görüntüle | Mağazadaki tüm çalışanlar için saat girişlerini gösterin. | Evet | Evet | Evet | Hayır | Hayır |
| 211 | Ödemeyi hükümsüz kıl | Harekette seçili ödeme satırını geçersiz kılın. | Evet | Evet | Hayır | Evet | Hayır |
| 102 | Ürünü hükümsüz kıl | Harekette seçili satır maddesini geçersiz kılın. | Evet | Evet | Hayır | Evet | Hayır |
| 500 | Hareketi hükümsüz kıl | Geçerli hareketi geçersiz kılın. | Evet | Evet | Hayır | Evet | Hayır |
| 916 | Windows workflow foundation | Bu işlem desteklenmez. | Uygulanamaz | Uygulanamaz | Uygulanamaz | Uygulanamaz | Hayır |
| 924 | Banka kartları için X raporu | Bu işlem desteklenmez. | Geçerli değil | Geçerli değil | Geçerli değil | Geçerli değil | Evet |
| 311 | Sistem iskontolarını hareketlerin içinden kaldır | Hareketin, kupon tabanlı iskontolar dahil olmak üzere tüm sistem tarafından uygulanan iskontolarını hareketten kaldırın. Bu, el ile iskontoları kaldırmaz. | Evet | Evet | Evet | Evet | Hayır |
| 312 | Sistem iskontolarını yeniden uygula | **Hareket üzerindeki sistem iskontolarını kaldır** operasyonunu kullanarak kaldırıldıklarında, harekete sistem iskontolarını yeniden uygulayın . | Evet | Evet | Evet | Evet | Hayır |

\* İşlem yalnızca bir müşteri siparişi veya satış teklifi etkinleştirildiğinde çevrimdışı modda ve yalnızca POS işlevleri profilinde müşteri siparişleri ve satış teklifleri için çevrimdışı oluşturma yapılandırılmışsa kullanılabilir. İşlem, siparişler Gerçek Zamanlı Hizmet kullanılarak oluşturulduğunda veya siparişler geri çağrıldığında veya düzenlendiğinde gerçekleştirilemez.

† İşlem yalnızca POS'un POS işlevi profilinde çevrimdışı müşteri oluşturmaya izin verecek şekilde yapılandırılmış olması durumunda çevrimdışı modda kullanılabilir.

‡ POS çevrimdışı olduğunda, askıya alınan hareketler yalnızca geçerli kaydın çevrimdışı veritabanından geri çağrılabilir. Kullanıcılar kayıtlar arasında hareketleri askıya alamaz veya geri çağıramaz.

§ POS çevrimdışı olduğunda, yalnızca geçerli çevrimdışı veritabanındaki hareketler iade için geri çağrılabilir.

\*\* POS çevrimdışı olduğunda, yalnızca geçerli çevrimdışı kanal veritabanındaki hareketler günlükte gösterilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
