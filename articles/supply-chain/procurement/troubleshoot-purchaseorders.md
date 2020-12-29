---
title: Satınalma siparişleri ile ilgili sorun giderme
description: Bu konu, satınalma siparişleri üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 234458f865e37a2d962aee8ab218b9521847081d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439721"
---
# <a name="troubleshoot-purchase-orders"></a>Satınalma siparişleri ile ilgili sorun giderme

Bu konu, satınalma siparişleri üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a>Eylem, yalnızca satır numarası tam olarak dağıtıldıktan sonra tamamlanabilir.

Bu sorun, satınalma siparişi dağılımlarında tutarsızlık olması nedeniyle oluşabilir.

Bu sorunun engelini kaldırmak ve satınalma siparişini *Taslak* durumuna sıfırlamak için, **Satın alma ve kaynak hizmeti \> Dönemsel görevler \> Temizle \> Satınalma siparişi dağılımını sıfırlama** sayfasına gidin. Daha fazla bilgi için aşağıdaki blog postasına bakın: [SAS dağıtım hatalarını Dynamics 365 Supply Chain Management'da çözümle](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a>Satınalma siparişleri veri yönetimi aracılığıyla içe aktarıldığında, satınalma siparişi satır numaraları sistem parametrelerinde tanımlanan artışı izlemez.

### <a name="issue-description"></a>Sorun açıklaması

Varsayılan olarak, *Satınalma siparişi satırları V2* veri varlığı aracılığıyla içe aktarılan satınalma siparişi satırları için otomatik olarak oluşturulan satır numaraları sistem parametrelerinde belirtilen sistem satır numarası artışını kullanmaz. El ile bir satınalma siparişi oluşturur ve kullanıcı arabirimiyle (UI) satır eklerseniz, satır numaraları doğru şekilde artırılır. Ancak, Veri yönetimi çerçevesi (DMF) kullanıyorsanız, doğru şekilde arttırılmazlar.

Bu sorun; satırları DMF ile içe aktardığınızda, içe aktarılan varlıkta satır numaraları atanmış değilse, sistem bu dosyaları atamak için DMF yöntemini kullandığı için oluşur. Bu yöntem satır numaralarını her zaman bir sayı kadar arttırır.

### <a name="issue-workaround"></a>Sorun geçici çözümü

Satınalma siparişi satırlarını içe aktardığınızda, gerekli satır numaralarının veri varlığı satır numarası alanlarında zaten verildiğinden emin olun. Bu durumda, DMF satır numaralarının üzerine yazmaz.

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a>Varsayılan bir vergi grubu ve varsayılan nakit iskontosu fatura hesabından doldurulmamış.

Müşteri hesabından farklı bir fatura hesabı kullanıyorsanız, bir satınalma siparişi oluşturulduğunda varsayılan vergi grubu ve varsayılan nakit iskontosu fatura hesabından doldurulmaz.

Bu davranış tasarımdan kaynaklanır. Vergi grubu, nakit iskontoları ve diğer fiyat bilgilerinin varsayılan değerleri fatura hesabına değil müşteri hesabına dayanır.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Satınalma siparişi teyidi sırasında "Nesne başvurusu ayarlanmadı" hatasını alıyorum veya satıcı faturasının deftere nakli sırasında "Bir çağrı hedefi tarafından özel durum oluşturuldu" özel durumu oluştu.

Bu sorun, satınalma siparişi dağılımlarında tutarsızlık olması nedeniyle oluşabilir.

Bu sorunun engelini kaldırmak ve satınalma siparişini *Taslak* durumuna sıfırlamak için, **Satın alma ve kaynak hizmeti \> Dönemsel görevler \> Temizle \> Satınalma siparişi dağılımını sıfırlama** sayfasına gidin. Daha fazla bilgi için aşağıdaki blog postasına bakın: [SAS dağıtım hatalarını Dynamics 365 Supply Chain Management'da çözümle](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Bir veya daha fazla muhasebe dağıtımı fazla dağıtılmış veya eksik dağıtılmış.

### <a name="issue-description"></a>Sorun açıklaması

Şu hatayı alırsınız: "Bir veya daha fazla muhasebe dağıtımı fazla dağıtılmış veya eksik dağıtılmış."

### <a name="issue-resolution"></a>Sorunun çözümü

Bu sorun, satınalma siparişi dağılımlarında tutarsızlık olması nedeniyle oluşabilir.

Bu sorunun engelini kaldırmak ve satınalma siparişini *Taslak* durumuna sıfırlamak için, **Satın alma ve kaynak hizmeti \> Dönemsel görevler \> Temizle \> Satınalma siparişi dağılımını sıfırlama** sayfasına gidin. Daha fazla bilgi için aşağıdaki blog postasına bakın: [SAS dağıtım hatalarını Dynamics 365 Supply Chain Management'da çözümle](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Yalnızca oluşturduğum satınalma siparişlerini görüntüleyebilir miyim?

Bu işlev şu anda kullanılamıyor.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Bir satınalma siparişindeki stok rezerve edebilir ve kayıtlı stokla hareket oluşturabilir miyim?

### <a name="issue-description"></a>Sorun açıklaması

Malzemeler bir satınalma siparişi üzerinde *Kayıtlı* durumda olsa bile, yine de stoku rezerve edebilirsiniz. Başka bir deyişle, kayıtlı stok için hareketler oluşturabilirsiniz.

### <a name="reproduce-the-issue"></a>Sorunu yeniden oluşturma

Aşağıdaki yordamda, bu sorunu yeniden oluşturmanın bir yolu gösterilmektedir.

1. Bir satınalma siparişi oluşturmak.
2. Satınalma siparişi satırını kaydedin.
3. Kayıtlı stok için rezervasyon veya hareket üretebildiğinize dikkat edin.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu davranış tasarımdan kaynaklanır. Bu, kayıtlı malzemelerin ambar veya stoka fiziksel olarak ulaşmış olması ve bu nedenle rezervasyon için kullanılabilir durumda olması beklenir.

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Satınalma siparişleri yasal varlığın dil ayarlarını yansıtmaz.

### <a name="issue-description"></a>Sorun açıklaması

Satın alma siparişindeki ürün adı, satınalma siparişinin oluşturulduğu yasal varlık için ayarlanmış dil yerine sistem dilinde gösterilir.

### <a name="reproduce-the-issue"></a>Sorunu yeniden oluşturma

Aşağıdaki yordamda, bu sorunu yeniden oluşturmanın bir yolu gösterilmektedir.

1. Sistem dilini *en-US* (ABD İngilizcesi) olarak ayarlayın.
1. Ürün adı çevirileri için *EN-US* ve *DE* (Almanca) dillerinin tutulduğu bir ürün bulunduğundan emin olun.
1. Geçerli bir varlığın dilini de *DE* olarak değiştirin.
1. *DE* dilinin ayarlandığı yasal varlıkta, ürünü içeren bir satınalma siparişi oluşturun.
1. Ürün adının ABD İngilizcesinde (sistem dili) gösterildiğine dikkat edin.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu davranış tasarımdan kaynaklanır. Satınalma siparişlerinde, ürün her zaman sistem dilinde gösterilir. Bir onay günlüğü oluşturulduğunda satınalma siparişi dili kullanılır.

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a>Ürün varlığına göre Onaylanan satıcı listesi geçerlilik tarihinin değiştirilmesine izin vermiyor.

### <a name="issue-description"></a>Sorun açıklaması

Bir üründe, örneğin, geçerlilik tarihi 11 Ocak 2018 (*11.01.2018*) ve sona erme tarihi *Hiçbir zaman* olan onaylanmış bir satıcı vardır. Geçerlilik tarihini 10 Ocak 2018 (*10.01.2018*) veya 12 Ocak 2018 (*12.01.2018*) olarak değiştirmeye çalışırsanız aşağıdaki hatayı alırsınız:

> Onaylanan tedarikçi listesinde (PdsApproveVendorList) bir kayıt oluşturulamıyor. "Geçerlilik süresi" değeri "Geçerli" değerinden büyük veya eşit olmalıdır.

### <a name="issue-resolution"></a>Sorunun çözümü

Yalnızca satıcı için onay verilen dönemi uzatabilirsiniz. Geçerli olan kurallar şunlardır:

- Geçerlilik tarihi, malzeme satıcısı için var olan kayıtlardan (dönemler) önce gelecek şekilde değiştirmek için, yeni dönemin sona erme tarihi var olan kayıtlardaki tüm sona erme tarihlerinden önce olmalıdır.
- Sona erme tarihini var olan herhangi bir dönemden daha geç olacak şekilde değiştirmek için, geçerli tarih var olan bir kayıttaki en son sona erme tarihinden sonra olmalıdır.
- Satıcının onaylandığı genel dönemi azaltmak için, var olan kayıtları silmeniz veya değiştirmeniz gerekir. Alternatif olarak, içe aktarma sırasında **kısaltma** anahtarını kullanabilirsiniz. Bu anahtar, tabloda onaylanan satıcılar için olan tüm kayıtları malzemeye göre siler.

Bir kaydın geçerlilik tarihi *11.01.2018* ve sona erme tarihi *Hiçbir zaman* olduğunda sorun açıklamasında açıklanan örnek senaryo için, geçerlilik tarihi *10.01.2018* ve sona erme tarihi *Hiçbir zaman* olan yeni bir kaydı içe aktarabilirsiniz. Ancak, geçerlilik tarihi veri yönetimi aracılığıyla *12.01.2018* olarak güncelleştirilecek şekilde dönemi azaltamazsınız. Bu değişikliği kullanıcı arayüzü aracılığıyla yapmalısınız.

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-nameisnt-synced"></a>Bir satınalma siparişi başlığındaki teslimat adresini değiştirdikten sonra, teslimat adı eşitlenmemiş.

### <a name="issue-description"></a>Sorun açıklaması

Bir satınalma siparişinin başlığındaki adres teslimat adresi olmayan bir adresle güncelleştirildi. Adres satınalma siparişinde güncelleştirilse de, teslimat adı güncelleştirilmiş adrese göre güncelleştirilmez.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu davranış tasarımdan kaynaklanır. Seçilen adresin teslimat adresi olarak sınıflandırılması gerekir. Aksi durumda, teslimat adı seçilen adrese göre güncelleştirilmez.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Bir satınalma siparişini iptal eden kullanıcıyı bulabilir miyim?

Bu bilgiler yalnızca satınalma siparişi değişiklik yönetimine tabi olduğunda izlenir. Değişiklik yönetimini kullanıyorsanız, değişikliği kimlerin göndermiş olduğunu (iptal) ve kimin onayladığını görebilirsiniz.
