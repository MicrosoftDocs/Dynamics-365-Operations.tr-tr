---
title: Çift yazılarda stok kullanılabilirliği
description: Bu makalede, çift yazmada envanter kullanılabilirliğini kontrol etme hakkında bilgi sağlanmaktadır.
author: RamaKrishnamoorthy
ms.date: 05/26/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 442486550d3a7c5132e26f663caaa7c2c02eeb6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289223"
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

Finance and Operations uygulamaları | Müşteri etkileşimi uygulamaları     | Tanım
---|---|---
[CDS eldeki stok girişleri](mapping-reference.md#145) | msdyn_inventoryonhandentries |
[CDS eldeki stok istekleri](mapping-reference.md#147) | msdyn_inventoryonhandrequests |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
