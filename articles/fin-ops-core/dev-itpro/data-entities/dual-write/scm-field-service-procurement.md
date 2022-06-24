---
title: Supply Chain Management ve Field Service arasında tedariki tümleştirme
description: Bu makalede, çift yazma tümleştirmesinin satınalma siparişi oluşturmayı ve hem Supply Chain Management'tan hem de Field Service'tan güncelleştirmeleri desteklediği açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 11/11/2020
ms.topic: article
audience: Application User
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d5a59365b3a524b8a5ec9e1e829fe181aa3d3660
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897158"
---
# <a name="integrate-procurement-between-supply-chain-management-and-field-service"></a>Supply Chain Management ve Field Service arasında tedariki tümleştirme

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management, güçlü tedarik işlevleri sağlamaktadır. Dynamics 365 Field Service, servis işlemiyle ilişkili satınalma işlemlerini destekleyen benzer işlevler sunar. Bu iki uygulamadaki bu işlev, çift yazma aracılığıyla tümleştirilir ve sonuçta elde edilen işlevler arası kullanım alanları tablo eşlemeleri, çözüm mantığı, görünümler ve formlar aracılığıyla gerçekleştirilir.

Bu tümleştirme satınalma siparişinin oluşturulmasını ve çoğu durumda her iki uygulamadan da güncelleştirmeleri destekler. Ancak, Supply Chain Management fiyatlandırma, adresler ve ürün girişini denetler. Hem Field Service hem de Supply Chain Management kullanan kuruluşlar için birçok güçlü işlevler arası kullanım alanı sunulur. Bu kullanım alanları, tedariklerin her iki sistemde de başlatılmasını ve takip edilmesini sağlar.

Aşağıdaki çizimde, her iki sistemdeki tablolar ve birbirleriyle nasıl eşleştirildikleri gösterilmektedir. Field Service'taki satınalma siparişleri, *hesap* satırına başvururken Supply Chain Management'taki satınalma siparişleri *satıcı* satırına başvurur. Tümleştirmeyi sağlamak için çift yazma, *satıcı* satırlarını *hesap* satırlarına bağlamak için bir başvuru kullanır. Daha fazla bilgi için bkz. [Tümleşik satıcı aslı](vendor-mapping.md).

![Tedarik için eşlemeler.](media/scm-field-service-tables.png)

## <a name="prerequisites"></a>Önkoşullar

Supply Chain Management'ı Field Service ile tümleştirmek için aşağıdaki bileşenleri yüklemeniz gerekir:

- Kapsamlı satınalma siparişi tümleştirmesi için Field Service 8.8.31.60 sürümü veya sonraki sürümler
- Supply Chain Management 10.0.14 sürümü veya sonraki sürümler
- OneFSSCM çözümünü çalıştırmak için çift yazma

## <a name="installation-guidelines"></a>Yükleme yönergeleri

### <a name="prerequisites"></a>Önkoşullar

- **Çift yazma**: Daha fazla bilgi için bkz. [Çift yazma giriş sayfası](dual-write-home-page.md#dual-write-setup).
- **Dynamics 365 Field Service**: Daha fazla bilgi için bkz. [Dynamics 365 Field Service yükleme](/dynamics365/field-service/install-field-service#step-1-install-dynamics-365-field-service).

Microsoft Dataverse'te etkinleştirildiklerinde, çift yazma ve Field Service ortamı yeni meta veriler, formlar, görünümler ve mantık ile geliştiren birçok çözüm katmanı sunar. Bu çözümler genellikle burada verilen sırayla yüklense de herhangi bir sırada etkinleştirilebilir:

1. **Field Service Common**: Field Service ortama yüklendiğinde Field Service Common yüklenir.
2. **Field Service (Anchor)**: Field Service ortama yüklendiğinde Field Service (Anchor) yüklenir. 
3. **Supply Chain Management Extended**: Çift yazma ortamda etkinleştirildiğinde Supply Chain Management Extended otomatik olarak yüklenir. 
4. **OneFSSCM çözümü**: Field Service veya Supply Chain Management çözümlerinden biri yüklendiğinde OneFSSCM otomatik olarak yüklenir.

    - Field Service ortamda zaten yüklüyse ve Supply Chain Management Extended'ı yükleyen çift yazma işlevini etkinleştirdiyseniz OneFSSCM yüklüdür.
    - Supply Chain Management Extended ortamda zaten yüklüyse ve Field Service'ı yüklerseniz OneFSSCM yüklüdür.

## <a name="initial-synchronization"></a>Başlangıç eşitlemesi

Yeni satınalma siparişleri oluşturmak ve mevcut satınalma siparişleriyle çalışmak için Supply Chain Management ve Dataverse arasındaki başvuru verilerini eşleştirmeniz gerekir. Tablo ilişkilerini algılamak ve belirli bir eşlemede etkinleştirmeniz gereken tabloları bulmak için ilk yazma işlevini kullanırsınız.

Aşağıdaki tabloları eşitlemeniz gerekir:

- Ürün şablonları

    İlk yazmayı çalıştırdığınızda, gerekli tabloların tam listesini alırsınız. Aşağıda bu şablonların bazı örnekleri verilmiştir:

    - Tüm ürünler
    - Serbest bırakılan ürünler V2
    - Dataverse serbest bırakılan farklı ürünler

- Tesisler
- Ambarlar
- Tedarik kategorileri şablonları

    Aşağıda bu şablonların bazı örnekleri verilmiştir:

    - Tedarik kategorileri
    - Pro
    - Ürün kategori hiyerarşisi
    - Ürün kategorisi atamaları

- Satıcı V2 gibi satıcı şablonları
- Dataverse İlgili Kişiler V2 gibi ilgili kişi şablonları
- Çalışan gibi Çalışan şablonları

Tabloların eşitlenmesi, Supply Chain Management'ta bulunan tüm belgelerin (satınalma siparişleri ve ürün makbuzları) Dataverse'te kullanılabilir olmasını sağlar.

### <a name="account-and-vendor-tables"></a>Hesap ve Satıcı tabloları

Field Service'taki satınalma siparişleri satıcıları izlemek için Hesap tablosunu kullanır. Bu nedenle, satınalma siparişleri için Dataverse tabloları satıcıları takip etmek için hesapları kullanır. Bu önemli farkı dengelemek için hesapların ve satıcıların eşitlenmesini sağlayan şu dört iş akışının etkinleştirilmesi gerekir: 

- Hesaplar tablosunda Satıcılar oluşturma
- Satıcılar tablosunda Satıcılar oluşturma
- Hesaplar tablosunda Satıcıları Güncelleştirme
- Satıcılar tablosunda Satıcıları Güncelleştirme

Hem Field Service hem de Supply Chain Management Extended yüklendiği için OneFSSCM yüklenmişse bu iş akışları otomatik olarak etkinleştirilir. Field Service yüklü değilse, ancak satınalma siparişi tablolarını Dataverse ile tümleştirmek istiyorsanız bu iş akışlarını etkinleştirmelisiniz. Her iki durumda da sıfırdan başlamadığınız sürece, satınalma siparişleri oluşturmadan önce tüm satıcıların hesap olarak Dataverse'te oluşturulduğundan emin olmanız gerekebilir. Aksi takdirde, hatalar oluşabilir.

### <a name="initial-synchronization"></a>Başlangıç eşitlemesi

Tüm ön koşullar yerine getirildikten sonra, mevcut satınalma siparişlerinin ve ürün girişlerinin her iki sistemde de kullanılabilir olmasını istiyorsanız, aşağıdaki şablonlar için bir başlangıç eşitlemesi yapmanız gerekir:

- Satınalma Siparişi Başlığı V2
- CDS Satınalma Siparişi Satırı
- CD Satınalma Siparişi Satırı geçici silme
- Satınalma Siparişi Girişi
- Satın alm Siparişi Girişi Ürün

## <a name="mappings-with-logic"></a>Mantık ile eşleme

Tedarik tümleştirmesi, **Field Service Ürün Türü** sütununun Dataverse'teki ürünler tablosunda doğru şekilde ayarlandığından emin olmak için ürün eşleme aşağıdaki mantıkla genişletilir.

- **Ürün Türü** *Ürün* olarak ayarlanırsa ve **Madde modeli grubu, Stoğu tutulan ürün** *True* olarak ayarlanırsa **Field Service Ürün Türü** *Stok* olarak ayarlanır.
- **Ürün Türü** *Ürün* olarak ayarlanırsa ve **Madde modeli grubu, Stoğu tutulan ürün** *False* olarak ayarlanırsa **Field Service Ürün Türü** *Stok Dışı* olarak ayarlanır.
- **Ürün Türü** *Hizmet* olarak ayarlanmışsa **Field Service Ürün Türü** *Hizmet* olarak ayarlanır.

Ek olarak, Dataverse, satıcıları ilgili hesaplarıyla eşleyen bir mantık içerir. Bu mantık varsayılan fatura satıcı hesabını ayarlar. Oluşturma sırasında, sunucu tarafı eklenti mantığı, hesapla ilgili satıcıdan varsayılan fatura satıcı hesabını ayarlar. Satıcının, bu değeri ayarlamak için kullanılan fatura hesabına başvurusu vardır.

## <a name="supported-scenarios"></a>Desteklenen senaryolar

- Satınalma siparişleri Dataverse kullanıcıları tarafından oluşturulabilir ve güncelleştirilebilir. Ancak, işlem ve veriler Supply Chain Management tarafından kontrol edilir. Supply Chain Management'daki satınalma siparişi sütunlarına güncelleştirmelerle ilgili sınırlamalar, güncelleştirmeler Field Service'tan geldiğinde geçerlidir. Örneğin, sonlandırılmış bir satınalma siparişini güncelleştiremezsiniz. 
- Satınalma Supply Chain Management'taki değişiklik yönetimi tarafından denetleniyorsa, bir Field Service kullanıcısı satınalma siparişini yalnızca Supply Chain Management onay durumu *Taslak* olarak ayarlandığında güncelleştirebilir.
- Birçok sütun yalnızca Supply Chain Management tarafından yönetilir ve Field Service'ta güncelleştirilemez. Hangi sütunların güncelleştirilemeyeceğini öğrenmek için üründeki eşleme tablolarını inceleyin. Kolaylık olması için, bu sütunların çoğu Dataverse sayfalarında salt okunur olarak ayarlanmıştır. 

    Örneğin, fiyat bilgilerinin sütunları Supply Chain Management tarafından yönetilir. Supply Chain Management, Field Service'ın yararlanabileceği ticari anlaşmalara sahiptir. **Birim fiyat**, **İskonto** ve **Net tutar** gibi sütunlar yalnızca Supply Chain Management'tan gelir. Fiyatın Field Service ile eşitlendiğinden emin olmak için satınalma siparişi verileri girildiğinde Dataverse'te **Satınalma Siparişi** ve **Satınalma Siparişi Ürünü** sayfalarında **Eşitle** özelliğini kullanmanız gerekir. Daha fazla bilgi için bkz. [İstek üzerine Dynamics 365 Supply Chain Management tedarik verileriyle eşitleme](#sync-procurement).

- **Toplamlar** sütunu, yalnızca Field Service'ta kullanılabilir, çünkü Supply Chain Management'ta satınalma siparişinin güncel toplamı yoktur. Supply Chain Management'taki toplamlar, Field Service'ta kullanılamayan birden çok parametre temel alınarak hesaplanır.
- Yalnızca bir tedarik kategorisinin belirtildiği veya belirtilen ürünün *Hizmet* ürün türü veya Field Service ürün türünde bir madde olduğu satınalma siparişi satırları, yalnızca Supply Chain Management'ta başlatılabilir. Daha sonra satırlar Dataverse ile eşitlenir ve Field Service'ta görünür olur.
- Yalnızca Field Service yüklüyse ve Supply Chain Management yüklü değilse **Ambar** sütunu satınalma siparişinde zorunludur. Ancak, Supply Chain Management yüklüyse, bu gereklilik daha esnek olur. Bunun nedeni, Supply Chain Management'ın belirli durumlarda ambarın belirtilmediği satınalma siparişi satırlarına izin vermesidir.
- Ürün girişleri (Dataverse'te satınalma siparişi girişleri) Supply Chain Management tarafından yönetilir ve Supply Chain Management yüklüyse Dataverse'ten oluşturulamaz. Supply Chain Management'tan alınan ürün girişleri, Supply Chain Management'tan Dataverse'e eşitlenir.
- Supply Chain Management'ta eksik teslimata izin verilir. OneFSSCM çözümü mantık ekler. Böylece ürün girişi satırı (veya Dataverse'te satınalma siparişi girişi ürünü) oluşturulduğunda veya güncelleştirildiğinde, eksik teslimat senaryoları için siparişte kalan miktarı dengelemek üzere Dataverse'te stok günlüüğü satırı oluşturulur.

## <a name="unsupported-scenarios"></a>Desteklenmeyen senaryolar

- Field Service, Supply Chain Management'ta iptal edilen bir satınalma siparişine satır eklenmesini engeller. Geçici bir çözüm olarak, Field Service'ta satınalma siparişinin sistem durumunu değiştirebilir ve ardından yeni satırı Field Service'a veya Supply Chain Management'a ekleyebilirsiniz.
- Tedarik satırları stok düzeylerini her iki sistemde de stok düzeylerini etkilese de bu tümleştirme, Supply Chain Management ve Field Service arasında stok uyumlulaştırmasını sağlamaz. Hem Field Service hem de Supply Chain Management, stok düzeylerini güncelleştiren başka işlemlere sahiptir. Bu işlemler tedarik kapsamı dışındadır.

## <a name="status-management"></a>Durum yönetimi

Field Service'taki satınalma siparişlerinin durumları, Supply Chain Management'taki durumlardan farklıdır.

### <a name="field-service-purchase-order-and-purchase-order-product-statuses"></a>Field Service satınalma siparişi ve satınalma siparişi ürün durumları

| Başlık - Sistem durumu | Başlık - Onay durumu | Madde durumu |
|---|---|---|
| <ul><li>Taslak</li><li>Gönderildi</li><li>İptal edildi</li><li>Ürün alındı</li><li>Faturalanan</li></ul> | <ul><li>Null</li><li>Onaylı Tutar</li><li>Reddedildi</li></ul> | <ul><li>Bekliyor</li><li>Teslim alındı</li><li>İptal edildi</li></ul> |

### <a name="supply-chain-management-purchase-order-and-purchase-order-line-statuses"></a>Supply Chain Management satınalma siparişi ve satınalma siparişi satırı durumları

Satır onay durumları yalnızca bir satır iş akışı olduğunda etkindir.

| Başlık - Belge durumu | Başlık - Onay durumu | Satır durumu | Satır onayı durumu |
|---|---|---|---|
| <ul><li>Açık Sipariş (Karşılanamayan sipariş)</li><li>Teslim alındı</li><li>Faturalanan</li><li>İptal edildi</li></ul> | <ul><li>Taslak</li><li>İncelemede</li><li>Onaylı Tutar</li><li>Reddedildi</li><li>Harici İncelemede</li><li>Onaylı</li><li>Sonuçlandırılmış</li></ul> | <ul><li>Açık Sipariş (karşılanamayan sipariş)</li><li>Teslim alındı</li><li>Faturalanan</li><li>İptal edildi</li></ul> | <ul><li>Gönderilmedi</li><li>İncelemede</li><li>Onaylı Tutar</li><li>Reddedildi</li></ul> |

Durum sütunlarına aşağıdaki kurallar uygulanır:

- Supply Chain Management'taki durum, Field Service'tan güncelleştirilemez. Ancak, bazı durumlarda, satınalma siparişi durumu Supply Chain Management'ta değiştiğinde Field Service'taki durum güncelleştirilecektir.
- Supply Chain Management'taki bir satınalma siparişi değişiklik yönetimindeyse ve bir değişiklik işleniyorsa onay durumu *Taslak* veya *İncelemede* olur. Bu durumda, Field Service onay durumu *Null* olarak ayarlanır.
- Supply Chain Management'ta satınalma sipariş onay durumu *Onaylandı*, *Harici incelemede*, *Teyit edildi* veya *Sonlandırıldı* olarak ayarlandıysa Field Service satınalma siparişi onay durumu *Onaylandı* olarak ayarlanır.
- Supply Chain Management'ta satınalma sipariş onay durumu *Reddedildi* olarak ayarlandıysa, Field Service satınalma siparişi onay durumu *Reddedildi* olarak ayarlanır.
- Supply Chain Management'taki belge başlığı durumu *Açık sipariş (Karşılanamayan sipariş)* olarak değiştirilirse ve Field Service satınalma siparişi durumu *Taslak* veya *İptal Edildi* ise Field Service satınalma siparişi durumu *Gönderildi* olarak değişir.
- Supply Chain Management'ta belge başlığı durumu *İptal edildi* olarak değiştirilirse ve Field Service'ta hiçbir satınalma siparişi girişi ürünü satınalma siparişiyle (satınalma siparişi ürünleri yoluyla) ilişkilendirilmediyse, Field Service sistem durumu *İptal edildi* olarak ayarlanır.
- Supply Chain Management'ta satınalma siparişi satırı durumu *İptal edildi* olarak ayarlandıysa Field Service'taki satınalma siparişi ürünü durumu *İptal edildi* olarak ayarlanır. Ayrıca, Supply Chain Management'ta satınalma siparişi durumu *İptal Edildi* yerine *Karşılanamayan Sipariş* olarak değiştirilirse Field Service'taki satınalma siparişi madde durumu *Beklemede* olarak ayarlanır.

## <a name="sync-with-the-supply-chain-management-procurement-data-on-demand"></a><a id="sync-procurement"></a>Supply Chain Management tedarik verileriyle istek üzerine eşitleme

Supply Chain Management, ticari sözleşmeleri, iskontoları ve Supply Chain Management'taki ikincil süreçlere dayanan diğer senaryoları ele alan tedarik verilerini içerir. Tedarik altyapısı, belirli bir satınalma siparişi için en iyi fiyatı belirlemek amacıyla karmaşık kurallar kullanır. Çift yazmayı kullandığınızda veriler her zaman iki ortam arasında zaman uyumlu tutulmaz. Özellikle satırın Dataverse'te oluşturulduğu veya buradan güncelleştirildiği ve Supply Chain Management'ta takip eden işlemleri tetikleyebileceği senaryolarda bu durum geçerlidir.

## <a name="sync-the-procurement-data-from-supply-chain-management"></a>Supply Chain Management'tan tedarik verilerini eşitleme

1. Dataverse'te, **Stok \> Satınalma Siparişi**'ne gidin.
2. Yeni satınalma siparişi oluşturmak için **Yeni**'yi seçin veya mevcut bir satınalma siparişi için bir satır seçin.
3. Satınalma siparişi veya satınalma siparişi satırından.
4. Eylem Bölmesi'nde, **Eşitle**'yi seçin.

Dataverse'te ve Field Service'ta, Supply Chain Management tarafından paylaşılan tüm sütunlar eşitlenir.

**Eşitleme** işlevini kullanabileceğiniz durumlar şunlardır:

- Dataverse'ten aynı satırda art arda birden fazla değişiklik yaparsanız **Eşitle** işlevini çalıştırın.
- Bir değişikliğin Dataverse'ten ikinci ardışık değişiklik olup olmadığından emin değilseniz **Eşitle** işlevini çalıştırmak mantıklı olabilir.
- Supply Chain Management'tan bir değeri güncelleştirmeyle ilgili bir hata iletisi alırsanız **Eşitle** işlevini çalıştırın ve ardından Dataverse'te güncelleştirmeyi tekrar deneyin.

## <a name="cancelling-the-posting-process"></a>Deftere nakil işleminin iptali

Ürün girişini deftere nakletme işlemi, işleme sırasında iptal edildiyse çift yazma, Dataverse'te bir ürün girişi oluşturabilir ancak Supply Chain Management'ta bir ürün girişi satırı oluşturmayabilir. Bu durum, çift yazmanın dağıtılmış işlemleri desteklememesi nedeniyle oluşur.

## <a name="templates"></a>Şablonlar

Tedarikle ilgili belgelerin tümleştirilmesi için aşağıdaki belgeler kullanılabilir.

| Supply Chain Management | Field Service | Tanım |
|---|---|---|
| [Satınalma siparişi başlığı V2](mapping-reference.md#183) | msdyn\_Purchaseorders | Bu tablo, satınalma siparişi başlığını temsil eden sütunları içerir. |
| [Satınalma siparişi satırı varlığı](mapping-reference.md#181) | msdyn\_PurchaseOrderProducts | Bu tablo, satınalma siparişindeki satırları temsil eden satırları içerir. Ürün numarası eşitleme için kullanılır. Bu, ürün boyutları dahil olmak üzere ürünü stok tutma birimi (SKU) olarak tanımlar. Dataverse ile ürün tümleştirmesi hakkında daha fazla bilgi için bkz. [Tümleşik ürün deneyimi](product-mapping.md). |
| [Ürün girişi başlığı](mapping-reference.md#185) | msdyn\_purchaseorderreceipts | Bu tablo, ürün girişi Supply Chain Management'ta nakledildiğinde oluşturulan ürün girişi başlıklarını içerir. |
| [Ürün girişi satırı](mapping-reference.md#184) | msdyn\_purchaseorderreceiptproducts | Bu tablo, ürün girişi Supply Chain Management'ta nakledildiğinde oluşturulan ürün girişi satırlarını içerir. |
| [Satın alma sipariş satırı geçici silinen varlığı](mapping-reference.md#182) | msdyn\_purchaseorderproducts | Bu tablo, geçici olarak silinen satınalma siparişi satırları hakkında bilgi içerir. Supply Chain Management'taki bir satınalma siparişi satırı, yalnızca satınalma siparişinin teyit edildiği veya onaylandığı durumlarda değişiklik yönetimin açık olması koşuluyla geçici olarak silinebilir. Satır, Supply Chain Management veritabanında mevcuttur ve **IsDeleted** olarak işaretlidir. Dataverse'te geçici silme kavramı bulunmadığından bu bilgilerin Dataverse ile eşitlenmesi önemlidir. Bu şekilde, Supply Chain Management'ta geçici olarak silinen satırlar Dataverse'ten de otomatik olarak silinebilir. Bu durumda, Dataverse'de bir satırı silme mantığı Supply Chain Management Extended'da bulunur. |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
