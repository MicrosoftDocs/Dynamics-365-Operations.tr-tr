---
title: Ürün girişleri ve faturalama ile ilgili sorunları giderme
description: Bu konu, ürün girişleri ve faturalama ile ilgili çalışırken karşılaşabileceğiniz sorunların nasıl düzeltilebileceğini açıklamaktadır.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 3522a024261ff6dfffb53f2101139460be7669e4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832022"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a>Ürün girişleri ve faturalama ile ilgili sorunları giderme

Bu konu, ürün girişleri ve faturalama ile ilgili çalışırken karşılaşabileceğiniz sorunların nasıl düzeltilebileceğini açıklamaktadır.

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Kategori tabanlı ögeler içeren bir satınalma siparişi satırı için birden fazla faturayı deftere nakledemiyorum.

Faturaları deftere nakletmek istiyorsanız miktar değeri zorunludur. Bu nedenle, bir satırın tam miktarı yalnızca kısmi bir tutar için faturalanmışsa, kalan tutarı başka bir faturada faturalayamazsınız.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Satınalma siparişi teyidi sırasında "Nesne başvurusu ayarlanmadı" hatasını alıyorum veya satıcı faturasının deftere nakli sırasında "Bir çağrı hedefi tarafından özel durum oluşturuldu" özel durumu oluştu.

Bu sorun, satınalma siparişi dağılımlarında tutarsızlık olması nedeniyle oluşabilir.

Bu sorunun engelini kaldırmak ve satınalma siparişini *Taslak* durumuna sıfırlamak için, **Satın alma ve kaynak hizmeti \> Dönemsel görevler \> Temizle \> Satınalma siparişi dağılımını sıfırlama** sayfasına gidin. Daha fazla bilgi için aşağıdaki blog postasına bakın: [SAS dağıtım hatalarını Dynamics 365 Supply Chain Management'da çözümle](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Çoklu ürün girişlerini tek bir satınalma siparişinde birleştiremiyorum.

Farklı ürün giriş satırları farklı muhasebe tarihlerine sahipse, çoklu ürün girişlerini tek bir satınalma siparişinde birleştiremezsiniz.

Microsoft Dynamics 365 Supply Chain Management uygulamasının önceki sürümlerinde, bu durumda birleştirmeye izin veriliyordu. Ancak, uygulama hataya açıktır. Oluşturulan satınalma siparişi satırlarındaki hesap tarihi, bu satınalma siparişi satırlarının oluşturulduğu ürün giriş satırlarındaki hesap tarihinden farklı olmamalıdır. (Satınalma siparişi satırlarındaki muhasebe tarihi, satınalma siparişi başlığındaki hesap tarihiyle eşleşir.) Bu nedenle, çoklu ürün girişinin tek bir satınalma siparişinde birleştirilmesine artık izin verilmez.

Muhasebe tarihi, örneğin bütçe rezervasyonları ve tutarlılık için kullanılır. Bu nedenle, ürün girişinden satınalma siparişine geçiş sırasında tutulmalıdır.

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a>Ürün girişleri iptal edildiğinde, hareketler askıya alınan genel muhasebe hesabına nakledilebilir.

### <a name="issue-description"></a>Sorun açıklaması

Bir ürün girişi iptal edilirse, ana hesaplar askıya alınmış olsa bile, sistem hareketlerin askıya alınan genel muhasebe hesaplarına nakledilmesini sağlar.

### <a name="reproduce-the-issue"></a>Sorunu yeniden oluşturma

Aşağıdaki yordamda, bu sorunu yeniden oluşturmanın bir yolu gösterilmektedir.

1. **Borç hesapları parametreleri** sayfasındaki **Genel** sekmesinde, **Ürün girişini deftere naklet** seçeneğinin *Evet* olarak ayarlandığından emin olun.
1. Satınalma siparişi oluşturun ve *bir ürün için 1.000'lik miktarı içeren bir sipariş satırı ekleyin*.
1. Satınalma siparişini doğrulayın.
1. Ürün girişini deftere nakledin ve fişleri denetleyin.
1. *200140* ve *140200* olan ilgili ana hesapları askıya alın.
1. Deftere nakledilen ürün girişini iptal edin.
1. Hareketlerin askıya alınan muhasebe hesaplara nakledilebileceğini unutmayın.

### <a name="issue-resolution"></a>Sorunun çözümü

Ürün girişleri iptal edildiğinde, hareketler, bu yaklaşım deftere doğru nakledilmeye olanak sağladığında, bekleyen genel muhasebe defterine nakledilebilir.

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a>Ürün girişi sırasında hiçbir mali fiş oluşturulmasa da, bir ürün girişi fiş numarası kullanılır.

Malzeme modeli grubu için **Ürün girişindeki tahakkuk borcu** seçeneği *Hayır* olarak ayarlanmışsa, genel muhasebeye nakil yapılmaz. Ancak, bir alt genel muhasebede muhasebe amacıyla fiziksel bir olay kaydedilir ve bu olay bir fiş numarası gerektirir. Bu fiş numarası stok hareketlerinde referans alınan fiş numarasıdır.

Aşağıdaki Web günlüğünde açıklandığı gibi, **Ürün girişindeki tahakkuk borcu** seçeneğini *Evet* olarak ayarlamanız önerilir: [Ürün makbuzu oluşturulurken sair giderleri deftere nakletme](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>Genel muhasebedeki gider hesabına naklet ayarı açık değil.

### <a name="issue-description"></a>Sorun açıklaması

Bu sorun bir satınalma siparişi faturalandığında, **Borç hesapları parametreleri** sayfasındaki **Fatura** sekmesinde **Genel muhasebedeki gider hesabına naklet** seçeneği *Evet* olarak ayarlandığında oluşur.

### <a name="reproduce-the-issue"></a>Sorunu yeniden oluşturma

Aşağıdaki yordamda, bu sorunu yeniden oluşturmanın bir yolu gösterilmektedir.

1. **Borç hesapları \> Kurulum \> Borç hesapları parametreleri**'ne gidin.
1. **Fatura** sekmesinde, **Genel muhasebedeki gider hesabına naklet** seçeneğini *Evet* olarak ayarlayın.
1. **Stok Yönetimi \> Kurulum \> Deftere nakil \> Deftere nakil** sayfasına gidin.
1. **Satınalma siparişi** sekmesinde, ürünle ilgili satın alma harcamaları içindeki tüm satırları sildiğinizden emin olun.
1. **Borç hesapları \> Satın alma siparişleri \> Tüm satınalma siparişleri**'ne gidin.
1. Bir satınalma siparişi oluşturmak. **Satıcı hesabı** alanında, *1001 Acme Office Supplies* ögesini seçin.
1. Aşağıdaki ayarlara sahip satınalma siparişi satırı oluşturun:

    - **Malzeme numarası:** *D0011 lazer projektör*
    - **Tesis:** *1*
    - **Ambar:** *11*
    - **Miktar:** *4*

1. Eylem Bölmesi'nde, **Satın al** sekmesindeki **Eylem** grubunda **Onayla**'yı seçin.
1. Eylem Bölmesi'nde, **Teslim al** sekmesindeki **Oluştur** grubunda **Ürün girişi**'ni seçin.
1. **Ürün girişi naklediliyor** iletişim kutusunda, **Ürün girişi** alanında rastgele bir numara girin ve **Tamam**'ı seçin.
1. Eylem Bölmesi'nde, **Fatura** sekmesindeki **Oluştur** grubunda **Fatura**'yı seçin.
1. **Numara** alanına, fatura numarası olarak rasgele bir numara girin.
1. Eşleştirme durumunu güncelleştirin ve deftere nakledin.
1. Bir satınalma siparişinden fatura oluştururken şimdi aşağıdaki hatayı alacağınızı unutmayın: "Ürün için satınalma harcamaları hareket türü için hesap numarası yok."

### <a name="issue-resolution"></a>Sorunun çözümü

Bu, fatura ve fatura gruplarının parametre ayarlarına bağlıdır. Daha fazla bilgi için, aşağıdaki Web günlüğü postasına bakın: [Satınalma ücreti ve stok farkı için hesap](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]