---
title: İade edilebilir masraflar, iade edilen miktara göre yanlış hesaplanmış
description: Bu konu satış noktasında (POS) iade edilen maddelerin miktarı için yanlış iade edilebilir masraflar gördüklerinde kasiyerlere yardımcı olabilecek sorun giderme kılavuzu sağlar.
author: gvrmohanreddy
ms.date: 03/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c8ecaa0cb73d06ac66b57cce815264e841a2259b
ms.sourcegitcommit: 94ebdaae6dc996b205ac78ed546e38f91f4f46ed
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/28/2022
ms.locfileid: "8490223"
---
# <a name="refundable-charges-are-miscalculated-based-on-the-quantity-returned"></a>İade edilebilir masraflar, iade edilen miktara göre yanlış hesaplanmış

[!include [banner](../../includes/banner.md)]

Bu konu satış noktasında (POS) iade edilen maddelerin miktarı için yanlış iade edilebilir masraflar gördüklerinde kasiyerlere yardımcı olabilecek sorun giderme kılavuzu sağlar.

## <a name="description"></a>Açıklama

Müşteri, satır düzeyinde iade edilebilir masrafların bulunduğu bir satış siparişinde satın alınan maddelerin kısmi miktarını iade eder. Ancak POS kısmi bir geri ödeme göstermek yerine tüm masrafları iade edilebilir olarak gösterir.

Örneğin, bir müşteri madde başına 5 $ olmak üzere toplam 25 $ ücret karşılığında beş madde satın alır. Ardından müşteri beş maddenin üçünü iade eder. Ancak, POS'ta kasiyere iade edilen üç ürün için iade edilebilir masraf beklenen 15 $ yerine 25 $ olarak gösterilir.

## <a name="resolution"></a>Çözüm

### <a name="turn-on-the-enable-refunding-charges-based-on-the-refunded-quantity-feature"></a>Geri ödenen miktara göre geri ödeme masraflarını etkinleştir özelliğini açma

Microsoft Dynamics 365 Commerce sürüm 10.0.26 itibariyle **Geri ödenen miktara göre geri ödeme masraflarını etkinleştir** özelliği, iade edilen maddelerin miktarına göre satır düzeyinde iade edilebilir masrafların hesaplanmasını sağlar.

Commerce Headquarters'da **Geri ödenen miktara göre geri ödeme masraflarını etkinleştir** özelliğini etkinleştirmek için bu adımları izleyin.

1. **Özellik yönetimi** çalışma alanını açın (**Sistem yöneticisi \> Çalışma alanları\> Özellik yönetimi**).
1. Kullanılabilir özellikler listesinde **Geri ödenen miktara göre geri ödeme masraflarını etkinleştir** özelliğini arayıp seçin.
1. Sağdaki bölmeden **Şimdi etkinleştir**'i seçin.
