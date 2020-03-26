---
title: Çift yazmada aday müşteriden nakde
description: Bu konu, çift yazmadan aday müşteriden nakde hakkında bilgi sağlar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 249fde6f7bba5d6e0bc6cfde62fd792dee3f1301
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112534"
---
# <a name="prospect-to-cash-in-dual-write"></a>Çift yazmada aday müşteriden nakde

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Birçok işletmenin önemli bir hedefi, aday müşterileri müşterilere dönüştürmek ve bu müşterilerle devam eden bir iş ilişkisi sürdürmektir. Microsoft Dynamics 365 uygulamalarında, aday müşteriden nakde süreci teklifler veya sipariş işleme iş akışları aracılığıyla gerçekleştirilir ve mali değerler için mutabakat sağlanır ve kabul edilir. Çift yazma ile aday müşteriden nakde tümleştirmesi, Dynamics 365 Sales veya Dynamics 365 Supply Chain Management'ta oluşturulan bir teklif ve sipariş alır ve teklif ve siparişi her iki uygulamada da kullanılabilir duruma getirir.

Uygulama arabirimlerinde, işleme durumlarına ve fatura bilgilerine gerçek zamanlı olarak erişebilirsiniz. Bu nedenle, teklif ve siparişleri yeniden oluşturmak zorunda kalmadan ürün stoklama, stok işleme ve Supply Chain Management'ta karşılama gibi işlevleri daha kolay yönetebilirsiniz.

![Aday müşteriden nakde için çift yazma veri akışı](../dual-write/media/dual-write-prospect-to-cash[1].png)

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

Satış tekliflerini eşitleyebilmeniz için önce aşağıdaki ayarları güncelleştirmeniz gerekir.

### <a name="setup-in-sales"></a>Sales içinde kurulum

Sales'de **Ayarlar \> Yönetim \> Sistem ayarları \> Sales**'e gidin ve aşağıdaki ayarların kullanıldığından emin olun:

- **Sistem fiyatlama hesaplamasını kullan** sistem seçeneğini **Evet** olarak ayarlayın.
- **İndirim hesaplama yöntemi** alanı **Satır maddesi** olarak ayarlanmalıdır.

### <a name="sites-and-warehouses"></a>Tesisler ve ambarlar

Supply Chain Management'ta, **Tesis** ve **ambar** alanları teklif satırları ve sipariş satırları için gereklidir. Tesis ve ambarı varsayılan sipariş ayarlarında ayarlarsanız, teklif satırına veya sipariş satırına bir ürün eklediğinizde bu alanlar otomatik olarak ayarlanır. 

### <a name="number-sequences-for-quotations-and-orders"></a>Teklifler ve siparişler için numara serileri

Supply Chain Management ve Sales için numara serileri teklifler ve siparişler oluşturulduğunda ve Sales ile Supply Chain Management'ta eşitlendiğinde bağlı değildir. Sales'de oluşturulan bir satış siparişi Supply Chain Management ile eşitlenirse, Supply Chain Management'ta aynı satış siparişi numarasına sahip olur. Satış siparişi numarasının yinelenmemesini sağlamaya yardımcı olmak için iki uygulama içinde farklı numara serisi sistemleri kullanmanız gerekir.

Örneğin, Supply Chain Management'taki numara serisi **1, 2, 3, 4, 5 ,...** Sales'deki numaras serisi **100, 99, 98, ...** olur. Sales içinde 100 satış siparişi oluşturursanız, Supply Chain Management'ta zaten varolan bir sipariş numarası oluşturulur. Başka bir deyişle, Supply Chain Management ve Sales'de satış siparişleri oluşturulurken, iki numara serisi çakışacaktır. Bunun yerine, Supply Chain Management'ta **F1, F2, F3 ,...** ve Sales'de **C1, C2, C3, ...** gibi bir numara serisi kullanabilirsiniz. Bu numara serileri asla tekrarlanan satış siparişi numaraları oluşturmaz.

## <a name="sales-quotations"></a>Satış teklifleri

Satış teklifleri Sales veya Supply Chain Management'ta oluşturulabilir. Sales'de bir teklif oluşturursanız, bu gerçek zamanlı olarak Supply Chain Management ile eşitlenir. Aynı şekilde Supply Chain Management'ta bir teklif oluşturursanız, bu gerçek zamanlı olarak Sales ile eşitlenir. Aaşağıdaki noktaları unutmayın:

+ Teklifte ürüne iskonto ekleyebilirsiniz. Bu durumda, iskonto Supply Chain Management ile eşitlenecektir. Başlıktaki **İskonto**, **Masraflar** ve **Vergi** alanları Supply Chain Management'taki bir ayar tarafından denetlenir. Bu kurulum hiçbir tümleştirme eşlemesini desteklemez. Bunun yerine **Fiyat**, **İskonto**, **Masraf** ve **Vergi** alanları Supply Chain Management'ta korunur ve işlenir.
+ Satış teklifi başlığındaki **İskonto %**, **İskonto** ve **Navlun Tutarı** alanları salt okunur alanlardır.
+ **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerin parçası değildir. Bu alanları eşlemek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.

## <a name="sales-orders"></a>Satış siparişleri

Satış siparişleri Sales veya Supply Chain Management'ta oluşturulabilir. Sales'de bir satış siparişi oluşturursanız, bu gerçek zamanlı olarak Supply Chain Management ile eşitlenir. Aynı şekilde Supply Chain Management'ta bir satış siparişi oluşturursanız, bu gerçek zamanlı olarak Sales ile eşitlenir. Aaşağıdaki noktaları unutmayın:

+ Siparişteki tüm ürünler Finance and Operations uygulamalarından geliyorsa, siparişleri yalnızca Sales'den etkinleştirebilir ve eşitleyebilirsiniz. Bu nedenle, serbest olmayan ürünler olabilir.
+ İskonto hesaplama ve yuvarlama:

    - Sales'taki iskonto hesaplama modeli Supply Chain Management'taki iskonto hesaplama modelinden farklıdır. Supply Chain Management'ta, satış satırındaki nihai iskonto tutarı iskonto tutarları ile iskonto yüzdeleri kombinasyonun sonucu olabilir. Nihai iskonto tutarı satırdaki miktara bölünürse, yuvarlama oluşabilir. Bununla birlikte, bu yuvarlama yuvarlanan bir birim başına iskonto tutarı Sales'a eşitlenirse dikkate alınmaz. Supply Chain Management'taki bir satış satırından gelen tam iskonto tutarının Sales'e doğru şekilde eşitlenmesini sağlamak için, tam tutarın satır miktarına bölünmeden eşitlenmesi gerekir. Bu nedenle, Sales'ta iskonto hesaplama yöntemini **Satır maddesi** olarak tanımlamanız gerekir.
    - Bir satış siparişi satırı Sales'den Supply Chain Management'a eşitlendiğinde tam satır iskontosu tutarı kullanılır. Supply Chain Management'ta bir satır için tam iskonto tutarının saklanabileceği bir alan bulunmadığından tutar miktara bölünür ve **Satır iskontosu** alanında saklanır. Bu bölme işlemi sırasında gerçekleşen yuvarlamalar satış satırındaki **Satış masrafları** alanında saklanır.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Örnek: Sales'ten Supply Chain Management'a eşitleme

Aşağıdaki satış siparişine sahipsiniz:

+ **Sales:** Miktar = 3, satır başına iskonto = 10,00 TL
+ **Supply Chain Management:** Miktar = 3, satır iskonto tutarı = 3,33 TL, satış masrafı = -0,01 TL

Supply Chain Management'tan Sales'e eşitleme yaparsanız, aşağıdaki sonucu alırsınız:

+ **Supply Chain Management:** Miktar = 3, satır iskonto tutarı = 3,33 TL, satış masrafı = -0,01 TL
+ **Sales:** Miktar = 3, satır başına iskonto = (3 x 3,33 TL) + 0,01 TL = 10,00 TL

## <a name="dual-write-solution-for-sales"></a>Sales için çift yazma çözümü

**Sipariş** varlığına yeni alanlar eklenmiştir ve bunlar sayfada görüntülenir: Bu alanların çoğu Sales'deki **Tümleştirme** sekmesinde görünür. Birkaç özel alan vardır:

+ **İşleme durumu** alanı siparişin Supply Chain Management'taki işleme durumunu gösterir. Bu alan kilitlidir ve yalnızca Supply Chain Management'taki siparişin durumunu gösterir. Aşağıdaki değerler kullanılabilir:

    + **Etkin** – Sipariş Sales'taki **Etkinleştir** düğmesi kullanılarak etkinleştirildikten sonraki durum.
    + **Onaylandı**
    + **Teslim edildi**
    + **Faturalanan**
    + **Kısmen Teslim Edildi**
    + **Kısmen Faturalandı**
    + **Malzeme çekildi**
    + **İptal Edildi**

    Aşağıdaki tablo, işleme durumunun **CRM durum kodu** değeri ile nasıl eşlendiğini gösterir.

    | İşlem durumu           | CRM durum kodu    |
    |-----------------------------|--------------------|
    | Active                      | Yeni/Bekliyor/Beklemede |
    | Onaylandı/Çekildi            | Devam ediyor        |
    | Kısmen Teslim Edildi         | Kısmi            |
    | Teslim edildi                   | Tamamla           |
    | Faturalandı/Kısmen Faturalandı | Faturalanan           |
    | İptal Edildi                    | Para yok           |

+ Sales'de **Satış siparişi** sayfasındaki **Fatura Oluştur** ve **Siparişi İptal Et** düğmeleri gizlidir.
+ **Satış siparişi durumu** değeri, Supply Chain Management'tan gelen değişikliklerin Sales'de satış siparişine aktığından emin olunması için **Etkin** kalacaktır. Bu davranışı kontrol etmek için, varsayılan **Statecode\[Status\]** değerini **Etkin** olarak ayarlayın.

## <a name="invoices"></a>Faturalar

Satış faturaları Supply Chain Management'ta oluşturulur ve Sales'e eşitlenir. Aaşağıdaki noktaları unutmayın:

+ Bir **Fatura numarası** alanı **Fatura** varlığına eklenmiştir ve sayfada görüntülenir.
+ **Satış siparişi** sayfasındaki **Fatura oluştur** düğmesi gizlidir çünkü faturalar Supply Chain Management'ta oluşturulacak ve Sales'e eşitlenecektir. **Fatura** sayfası düzenlenemez çünkü faturalar Supply Chain Management'tan eşitlenecektir.
+ **Satış siparişi durumu** değeri ilgili fatura Supply Chain Management'tan Sales'e eşitlendiğinde otomatik olarak **Faturalandı** olarak değişir. Ayrıca, faturanın oluşturulduğu satış siparişinin sahibi, faturanın sahibi olarak atanır. Bu nedenle, satış siparişinin sahibi faturayı görebilir.
+ **Navlun koşulları**, **Teslimat koşulları** ve **Teslimat şekli** alanları varsayılan eşlemelere dahil değildir. Bu alanları eşlemek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.

## <a name="templates"></a>Şablonlar

Aday müşteriden nakde, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir temel varlık eşlemeleri topluluğudur.

| Finance and Operations uygulamaları | Dynamics 365'teki model yönetimli uygulamalar | Tanım |
|-----------------------------|-----------------------------------|-------------|
| Satış faturası başlıkları V2    | faturalar                          |             |
| Satış faturası satırları V2      | invoicedetails                    |             |
| CDS satış siparişi başlıkları     | salesorders                       |             |
| CDS satış siparişi satırları       | salesorderdetails                 |             |
| Satış siparişi kaynak kodları    | msdyn\_salesorderorigins          |             |
| CDS satış teklifi başlığı  | teklifler                            |             |
| CDS satış teklifi satırları   | quotedetails                      |             |

Aday müşteriden nakde için ilgili temel varlık eşlemeleri şunlardır:

+ [Müşteriler V3 ve hesaplar](customer-mapping.md#customers-v3-to-accounts)
+ [CDS İlgili Kişileri V2 ve contacts](customer-mapping.md#cds-contacts-v2-to-contacts)
+ [Müşteriler V3 ve ilgili kişiler](customer-mapping.md#customers-v3-to-contacts)
+ [Serbest bırakılan ürünler V2 ve msdyn_sharedproductdetails](product-mapping.md#released-products-v2-to-msdyn_sharedproductdetails)
+ [Tüm ürünler ve msdyn_globalproducts](product-mapping.md#all-products-to-msdyn_globalproducts)
+ [Fiyat listesi](product-mapping.md)

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [sales invoice](includes/SalesInvoiceHeaderV2Entity-invoice.md)]

[!include [sales invoice line](includes/SalesInvoiceLineV2Entity-invoicedetail.md)]

[!include [sales order header](includes/SalesOrderHeaderCDSEntity-salesorder.md)]

[!include [sales order line](includes/SalesOrderLineCDSEntity-salesorderdetails.md)]

[!include [sales order origin](includes/SalesOrderOriginEntity-msdyn-salesorderorigin.md)]

[!include [sales quotation header](includes/SalesQuotationHeaderCDSEntity-quote.md)]

[!include [sales quotation line](includes/SalesQuotationLineCDSEntity-QuoteDetails.md)]
