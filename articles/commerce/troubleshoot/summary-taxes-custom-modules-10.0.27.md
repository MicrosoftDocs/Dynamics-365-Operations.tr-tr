---
title: Sipariş özeti alt toplamı, özelleştirilmiş sipariş özeti modüllerini kullanırken masraflarla ilgili vergileri içermiyor
description: Bu makalede, özelleştirilmiş sipariş özeti modülleri kullanırken sipariş özeti alt toplamının "fiyata satış vergisi dahildir" senaryosunda ücretlere vergi eklememesi durumunda yardımcı olabilecek sorun giderme yönergeleri sağlanır.
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-04-22
ms.openlocfilehash: 260dcb6bc1585615195e32adfcd1da6bfbca294e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848849"
---
# <a name="order-summary-subtotal-doesnt-include-taxes-on-charges-when-using-customized-order-summary-modules"></a>Sipariş özeti alt toplamı, özelleştirilmiş sipariş özeti modüllerini kullanırken masraflarla ilgili vergileri içermiyor

Bu makalede, özelleştirilmiş sipariş özeti modülleri kullanırken sipariş özeti alt toplamının "fiyata satış vergisi dahildir" senaryosunda ücretlere vergi eklememesi durumunda yardımcı olabilecek sorun giderme yönergeleri sağlanır.

## <a name="description"></a>Açıklama

Microsoft Dynamics 365 Commerce 10.0.27 sürümünün yayınlanmasından itibaren, e-ticaret sitesi sayfalarındaki sipariş özeti modüllerinde tutarlı bir deneyim sağlamak için "fiyata satış vergisi dahildir" senaryosunda aşağıdaki değişiklikler yapılmıştır.

- İki yeni alan eklendi: **TaxOnShippingCharge** ve **TaxOnNonShippingCharges**.
- **GetSalesOrderBySalesId** ve **GetSalesOrderByTransactionId** uygulama programı arabirimleri (API), "fiyata satış vergisi dahildir" senaryosunda aşağıdaki alanlar için doğru değerleri sağlar:

    - SubtotalSalesAmount
    - SubtotalAmountWithoutTax
    - SubtotalAmount
    - ShippingChargeAmount
    - OtherChargeAmount

Ancak, özelleştirilmiş sipariş özeti modülleri kullanıyorsanız bu değişiklikler, ücretlere vergileri dahil etmeyerek sipariş özeti alt toplam değerlerini etkileyebilir.

## <a name="resolution"></a>Çözüm

Özelleştirilmiş sipariş özeti modülleri kullanıyorsanız ve Commerce 10.0.27 sürümünde ve sonraki sürümlerinde "fiyata satış vergisi dahildir" senaryosuna yapılan değişiklikleri devralmak istemiyorsanız, bu bölümdeki yönergeleri izleyin.

**salesTransaction.SubtotalAmount** ve **salesTransaction.SubtotalAmountWithoutTax** alanlarının önceki (10.0.27 sürümünden eski) sipariş özeti davranışına dönüş yaparak, toplam ücret vergi miktarının (**TaxOnShippingCharge** ve **TaxOnNonShippingCharges**) alt toplam tutarlarına (**SubtotalAmount** ve **SubtotalAmountWithoutTax**) eklenmesi özelliğini geri yükleyebilirsiniz.

Önceki sipariş özeti davranışına dönmek için aşağıdaki adımları izleyin.

1. Commerce headquarters'da, Commerce parametreleri sayfasını açın (**Perakende ve Ticaret \> Headquarters kurulumu \> Parametreler \> Commerce parametreleri**).
1. Sol gezinti bölmesinde, **Yapılandırma parametreleri**'ni seçin.
1. Aşağıdaki yapılandırma parametrelerini ekleyin ve her birinin değerini **doğru** olarak ayarlayın:

    - IsLegacyTaxOnChargeInSubtotalAmountIncludedInTaxIncusiveEnabled
    - IsLegacyOrderSummaryHydrationEnabled

> [!NOTE]
> Daha önce **IsUpdatedPriceIncludesTaxSubtotalCalculationEnabled** yapılandırma parametresini kullandıysanız ve **order.NetAmountWithoutTax** özelliği için aynı davranışı korumak istiyorsanız **IsLegacyPriceIncludesTaxNetAmountWithoutTaxCalculationEnabled** yapılandırma parametresini de eklemeniz ve değerini **doğru** olarak ayarlamanız gerekir.

## <a name="additional-resources"></a>Ek kaynaklar

[Sipariş özetlerinde vergi döküm bilgilerini gizleme](../hide-taxes-breakup.md)
