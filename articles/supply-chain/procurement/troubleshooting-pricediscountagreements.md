---
title: Fiyatlar, indirimler, sözleşmeler ve para iadeleri ile ilgili sorunları giderme
description: Bu konu, fiyatlar, iskontolar, sözleşmeler ve iadeler ile ilgili çalışırken karşılaşabileceğiniz sorunların nasıl düzeltilebileceğini açıklamaktadır.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
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
ms.openlocfilehash: b4349eeba285492202b5df8481b277a06708a4c8
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439722"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a>Fiyatlar, indirimler, sözleşmeler ve para iadeleri ile ilgili sorunları giderme

Bu konu, fiyatlar, iskontolar, sözleşmeler ve iadeler ile ilgili çalışırken karşılaşabileceğiniz sorunların nasıl düzeltilebileceğini açıklamaktadır.

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a>Satınalma siparişi oluşturulduktan sonra bir satınalma siparişi satırına bir satınalma sözleşmesini bağlayamıyorum.

Satınalma siparişi oluşturulduğunda bir satınalma siparişinin bir satınalma sözleşmesi ile ilişkilendirilmesi gerekir. Aksi takdirde, satınalma siparişi satırları satınalma sözleşmesi satırlarıyla ilişkilendirilemez.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>"El ile veya harici belge ile girilen fiyatları ve indirimleri güncelleştir" iletisinin görünmesine neden olan denetimler nelerdir?

Sevkiyat tarihini değiştirdiğinizde, "El ile veya harici belge ile girilen fiyatları ve indirimleri güncelleştir" şeklinde bir ileti alabilirsiniz. Bu iletiyi alırsınız; çünkü sevkiyat tarihi değiştirilirse farklı bir ticaret veya satış sözleşmesi tetiklenebilir ve bir fiyat değişikliğine neden olabilir. Sevkiyat tarihinde yapılan bir değişiklik ambar zamanlamalarını ve diğer ilgili bilgileri de etkileyebilir.

İleti, herhangi bir tarih veya başka parametre değiştiğinde tetiklenir. İletinin amacı, bu değişikliklerden dolayı oluşabilecek fiyat değişikliklerinin farkında olduğunuzdan emin olmak içindir.

Bu ileti ticari sözleşme değerlendirme (TAE) istemidir. Tam açıklama için bkz. [Ticari sözleşme değerlendirme ilkeleri](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>Satınalma siparişi girişi tüm giderleri içermez.

### <a name="reproduce-the-issue"></a>Sorunu yeniden oluşturma

Aşağıdaki yordamda, bu sorunu yeniden oluşturmanın bir yolu gösterilmektedir.

1. **Satın alma ve kaynak hizmeti parametreleri** sayfasındaki **Teslimat** sekmesinde, **Ürün girişinde masraf oluştur** seçeneğinin *Evet* olarak ayarlandığından emin olun.
1. Masrafları içeren bir satınalma siparişi oluşturun.
1. Satınalma siparişini doğrulayın.
1. Satınalma siparişini teslim alın.
1. Makbuz toplamına bakın ve beklenen toplamla karşılaştırın.
1. Tüm giderlerin satınalma siparişi girişine dahil edilmediğinden emin olun.

### <a name="issue-resolution"></a>Sorunun çözümü

Çözüm, sair giderlerin ayarlandığı yönteme bağlıdır. Gereksinimlerinizi karşılamak amacıyla sair giderlerin nasıl ayarlanacağı hakkında bilgi için aşağıdaki blog yazısına bakın: [Ürün makbuzu oluşturulurken sair giderleri deftere nakletme](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a>Ticari sözleşme fiyatları ve iskontolar veri yönetimi aracılığıyla içe aktarılan satış veya satınalma siparişi satırlarına uygulanmaz.

### <a name="issue-description"></a>Sorun açıklaması

Satış veya satınalma siparişi için uygulanan ticari sözleşmeler veri yönetimi aracılığıyla içe aktarılan satırlara uygulanmaz. Ancak, aynı ticari sözleşmeler el ile oluşturulan satış veya satınalma siparişi satırlarına uygulanır.

### <a name="reason-for-the-issue"></a>Sorunun nedeni

Veri yönetimi aracılığıyla içe aktarılan satınalma siparişi satırları zaten fiyat bilgilerini içeriyorsa, ticaret sözleşmesi bu satırlar için yeniden değerlendirilmeyecektir. Örneğin **Satır iskontosu yüzdesi** veya fiyat ve iskonto değerlerinin herhangi biri bir satırla ilgili olarak ayarlanmışsa, ticari sözleşmeler bu satır için aranmayacaktır.

### <a name="issue-workaround"></a>Sorun geçici çözümü

Bu beklenen bir davranıştır ve hem satış siparişleri hem de satınalma siparişleri için benzerdir.

Geçici çözüm olarak, herhangi bir fiyat bilgisi ayarlamadan satınalma siparişi satırlarını içe aktarın. Ticari sözleşmeler daha sonra uygulanır ve satınalma siparişi satırları tanımlanan ticari sözleşmelere göre güncelleştirilir.

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>Satıcı indirimi, faturalara dayalı olarak kümülatif değildir.

### <a name="issue-description"></a>Sorun açıklaması

Deftere nakledilen faturaların farklı vade tarihleri varsa, bu faturalar bunlardan oluşturulan satıcı indirimlerine yansıtılmazlar.

### <a name="issue-resolution"></a>Sorunun çözümü

Tasarım sırasında, satıcı indirimi hesaplanırken vade tarihi dikkate alınmaz. Sistemi, gerçek satıcı indirimi açısından faturadaki vade sonu ve ilgili ilişki daha belirgin olacak şekilde özelleştirmeyi düşünebilirsiniz.

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Satınalma siparişlerindeki birim fiyatlar birim dönüştürmesi temel alınarak hesaplanmaz.

### <a name="issue-description"></a>Sorun açıklaması

Bir satınalma siparişinde bir birim değiştirildiğinde, ticari sözleşme fiyatları birim dönüştürme tanımlarına göre yeniden hesaplanmazlar.

### <a name="issue-resolution"></a>Sorunun çözümü

Fiyatlar her zaman ticari sözleşmelerden (veya satış sözleşmeleri veya malzeme fiyatları gibi sistemdeki diğer fiyat ayarlarından) elde edilir ve bunlar bir birim için ayarlanır.

Sipariş satırındaki birim değiştirilirse, sistem yeni birim için bir fiyat arar ve bu fiyatı uygular. Birim için bir fiyat bulunamazsa, sistem bir fiyat uygulamaz. Birim dönüştürme fiyatı başka bir birime yeniden hesaplamak için kullanılamaz. Teorik olarak, içerisinde on parça bulunan bir kutunun fiyatı bir tek kutunun fiyatının on katına eşit olmayabilir.

### <a name="issue-workaround"></a>Sorun geçici çözümü

Bu sorunu geçici olarak gidermek için kullanabileceğiniz bir yöntem de, malzemenin sipariş satırlarında kullanılmasını beklediğiniz birimler için ticari sözleşmeler olduğundan emin olmalıdır.

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a>Ticari sözleşmelerde para birimi dönüştürme sorunları oluşur.

Ticari sözleşme fiyatları, para birimi bir satınalma siparişinde farklılık gösterdiğinde para birimine göre yeniden hesaplanmazlar.

*Genel para birimi* özelliği, fiyatları ve iskontoları yalnızca bir para biriminde tanımlamanıza olanak sağlar. Daha sonra gerektiğinde diğer para birimlerine dönüştürebilirsiniz. Ayrıca, dönüştürme yapıldıktan sonra özellik otomatik olarak akıllı yuvarlama uygulayabilir.

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a>Bir satır görünümü modunda Satınalma sözleşmesi sayfasını açtığımda, satırın genel görünümüne Fiyat birimi alanı ekleyerek sayfayı kişiselleştiremiyorum.

Sözleşme çerçevesindeki bazı paylaşılan alanlar kişiselleştirmeler içine eklenemez. Bu sınırlama, uygulanan veri modeli nedeniyle oluşur. Bu nedenle, **Fiyat birimi** alanını kişiselleştiremezsiniz.

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a>Satınalma sözleşmesindeki maksimum sınır, satınalma talebinde etkili değildir.

### <a name="issue-description"></a>Sorun açıklaması

Bir satınalma talebi bir satınalma sözleşmesine bağlandığında, satınalma sözleşmesinden maksimum limit satınalma talebi üzerinde etkili olmaz. Varsayılan fiyat bilgileri doğru girilmiştir, ancak satınalma sözleşmesinden maksimum sınırdan fazlası satınalma talebinde sipariş edilebilir.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu davranış beklenmektedir. Talepler her zaman onaylanmadığından, satınalma sözleşmesinde bir miktar veya tutar rezerve edilmemelidir. Bu nedenle, satınalma sözleşmesinden maksimum sınırı karşılamazsınız.

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a>Ticari sözleşmeler, reddedilen RFQ'lardan oluşturulabilir. Bu nedenle, RFQ satırı kabul edilmediyse, sistem ticari sözleşme günlüklerinin oluşturulmasını engellemez.

Kabul edilip edilmediğine bakılmaksızın, bir teklif talebi (RFQ) için herhangi bir yanıt için ticari sözleşmeler oluşturabilirsiniz. Daha fazla bilgi için bkz. [Teklif talebine (RFQ) genel bakış](request-quotations.md).

