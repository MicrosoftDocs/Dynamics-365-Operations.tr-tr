---
title: Parça çekme onayı
description: Bu konu bir mobil cihazdan parça çekme onayının nasıl ayarlanacağını ve uygulanacağını açıklamaktadır.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b85414dd1385dc3d8c97632eaaeb252759590ff
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562916"
---
# <a name="piece-picking-confirmation"></a>Parça çekme onayı

[!include [banner](../includes/banner.md)]

Parça çekme, bir mobil cihazda çekme veya sayım işi aracılığıyla stoktaki her parçayı onaylamanıza olanak tanır. Çekme işleri için, işte çekim için belirtilen miktara kadar olan miktarda işi onaylayabilirsiniz. Sayım işi için, saydığınız stoğu tarayabilir ve toplam tutarı izleyebilirsiniz.

Parça çekmeyi etkinleştirdiğinizde, ürün onayı otomatik olarak seçilir. İş türü çekmeler için, maksimum parça sayısı etkinleştirilir. Bu, parça sayısı için iş işlenirken onaylanması gereken maksimum değeri ayarlamanıza olanak sağlar. Maksimum miktar işlenmekte olan geçerli iş birimini temel alır. Sayım iş türü maksimum ayarlanmasına izin vermez.

Taranan bir barkodla ilişkili olan miktarı ve ölçü birimini de kullanabilirsiniz. Karma plaka alma, satınalma siparişi maddesi, transfer emri maddesi ve yük maddesi de dahil olmak üzere gelen akışlar üzerinde alma için işe yarar. Ayrıca, barkod tarama işleminin miktarı onaylanan toplam parça sayısına barkod ile iş birimi üzerindeki ölçü birimine göre dönüştürme yaparak eklediği parça çekme işleminde de kullanılabilir. Barkod üzerindeki ölçü birimi sayımı yapılırken, miktarın sıra grubunda sayımına izin verildiği onaylanırsa, miktar toplam sayıma eklenir.

## <a name="where-it-applies"></a>Uygulandığı yerler

Parça çekme tüm sayım işlemleri ve herhangi bir iş türü için ilk çekme işleminde kullanılır. Parça çekme, madde seri numaraları tarafından denetleniyorsa veya bir plaka konumundan yapılan bir kanban veya üretim çekme işlemiyse ve madde aşamalandırma için ayarlandıysa kullanılamaz.

## <a name="set-up-piece-picking"></a>Parça çekme işlemini ayarlama

1.  Mobil cihaz menü öğesinden iş onayı için kurulum formunu açın: Ambar yönetimi > **Ambar yönetimi** > **Kurulum** > **Mobil cihaz** > **Mobil cihaz menü öğeleri**. 
2. Mobil cihaz menü öğesinden İş onayı ayarını açın.

İş türü çekme veya sayım olduğunda aşağıdaki seçenekler seçim için kullanılabilir hale gelir.


|           Seçenek           |                                                                            Açıklama                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Parça çekme onayı | Çekme ve sayım iş türleri için kullanılabilir. Ürün onayı otomatik olarak seçilir. Her stok parçasını mobil cihazınızdan onaylamanıza olanak tanır. |
|  Maksimum parça sayısı  |                   Parça çekme onayı etkinleştirilmişse, çekme işi için kullanılabilir. Onaylamak zorunda olduğunuz parça sayısı için bir sınır ayarlar.                   |

