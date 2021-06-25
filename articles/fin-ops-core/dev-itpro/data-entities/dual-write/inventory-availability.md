---
title: Çift yazılarda stok kullanılabilirliği
description: Bu konu, çift yazmada envanter kullanılabilirliğini kontrol etme hakkında bilgi sağlar.
author: RamaKrishnamoorthy
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 0fded78134b1427e6faea9656e1d3b02b467ae91
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193419"
---
# <a name="inventory-availability-in-dual-write"></a>Çift yazılarda stok kullanılabilirliği

[!include [banner](../../includes/banner.md)]

Stok kullanılabilirliğini kullanarak, bir ürünü Microsoft Dynamics 365 Sales'te model temelli uygulamalardaki **Teklifler**, **Siparişler** veya **Faturalar** sayfasına eklemeden önce Stoğunuzu kontrol edebilirsiniz. Örneğin, stok denetimi ve karşılama tarihi belirleme [aday müşteriden nakde](dual-write-prospect-to-cash.md) işlemindeki anahtar görevdir.

Yeterli stoğa sahip değilseniz, tahmini stok alış girişlerine ve çıkışlarına göre bir teslimat tarihi tahmin edebilirsiniz. Ayrıca, ATP miktarını önceden tanımlanmış zaman diliminden bulabileceğiniz, maddenin taahhüt edilebilir (ATP) bilgilerini de denetleyebilirsiniz.

## <a name="on-hand-inventory"></a>Eldeki stok

Dynamics 365 Sales'te **Teklifler**, **Siparişler** ve **Fatura** sayfalarının başlığına yen bir **Eldeki stok** düğmesi eklenmiştir. Bu düğmeyi seçtiğinizde, bir iletişim kutusu görüntülenir ve eldeki stoğu denetlemek istediğiniz şirketi ve ürünü burada belirtebilirsiniz. Bu iletişim kutusu [Eldeki stok](../../../../supply-chain/inventory/tasks/check-availability-stock.md) ile aynı bilgileri gösterir.

İletişim kutusu Dynamics 365 Supply Chain Management'tan stok bilgilerini getirir. Bilgiler aşağıdaki miktarları içerir:

- Eldeki miktar
- Tersine çevrilen eldeki miktar
- Kullanılabilir eldeki miktar
- Sipariş miktarı
- Siparişteki miktar
- Ayrılan sipariş edilen miktar
- Toplam kullanılabilir miktar

## <a name="atp-information"></a>KM bilgileri

Sales'te **Teklifler**, **Siparişler** ve **Faturalar** sayfalarındaki satır öğelerine yeni bir **ATP Bilgileri** düğmesi eklenmiştir. Bu düğmeyi seçtiğinizde, bir iletişim kutusu görüntülenir ve şirketi, stok tesisini, stok ambarını ve sipariş miktarını burada belirtebilirsiniz. Bu iletişim kutusu, [Sipariş taahhüdü](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) bölümünde açıklananlarla aynı ayarlara sahiptir.

İletişim kutusu, Supply Chain Management'taki ATP bilgilerini döndürür. Bilgiler aşağıdaki miktarları içerir:

- KM miktarı
- Giriş  miktarı
- Çıkış miktarı
- Eldeki miktar

## <a name="how-it-works"></a>Nasıl çalışır

**Teklifler**, **Siparişler** veya **Faturalar** sayfasında **Eldeki Stok** düğmesini seçtiğinizde, **Eldeki Stok API**'sine canlı bir çift yazma çağrısı yapılır. API, belirli ürün için eldeki stoku hesaplar. Sonuç, **InventCDSInventoryOnHandRequestEntity** ve **InventCDSInventoryOnHandEntryEntity** tablolarında saklanır ve daha sonra çift yazma tarafından Dataverse'e yazılır. Bu işlevi kullanmak için, aşağıdaki çift yazma eşlemelerini çalıştırmanız gerekir. Eşlemeleri çalıştırdığınızda ilk eşitlemeyi atlayın.

- CDS eldeki stok girişleri (msdyn_inventoryonhandentries)
- CDS eldeki stok istekleri (msdyn_inventoryonhandrequests)

## <a name="templates"></a>Şablonlar
Eldeki stok verilerini göstermek için aşağıdaki şablonlar kullanılabilir.

Finance and Operations uygulamaları | Müşteri etkileşimi uygulaması | Tanım 
---|---|---
[CDS eldeki stok girişleri](#145) | msdyn_inventoryonhandentries |
[CDS eldeki stok istekleri](#147) | msdyn_inventoryonhandrequests |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a>CDS eldeki stok girişleri (msdyn_inventoryonhandentries)

Bu şablon, Finance and Operations uygulamaları ve Dataverse arasında verileri eşitler.

Finance and Operations alanı | Eşleme türü | Müşteri etkileşimi alanı | Varsayılan değer
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a>CDS eldeki stok istekleri (msdyn_inventoryonhandrequests)

Bu şablon, Finance and Operations uygulamaları ve Dataverse arasında verileri eşitler.

Finance and Operations alanı | Eşleme türü | Müşteri etkileşimi alanı | Varsayılan değer
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]