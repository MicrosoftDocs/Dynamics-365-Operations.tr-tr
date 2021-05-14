---
title: Kalite yönetimi madde örnekleme
description: Bu konu, madde örneklemenin nasıl ayarlanacağını açıklar.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 495bef32d63738e367167ee69f2028bc77945cc4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956857"
---
# <a name="quality-management-item-sampling"></a>Kalite yönetimi madde örnekleme

Madde örnekleme, kalite ilişkilendirmenin bir parçası olarak kullanılır. Denetlenecek geçerli fiziksel stok tutarını tanımlar. Örnekleme miktar, yüzde veya tam plaka tabanlı olabilir.

## <a name="set-up-item-sampling"></a>Madde örneklemesi ayarlayın

Madde örneklemeyi kurmak için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Kurulum \> Kalite kontrol \> Madde örnekleme**'ye gidin.
1. **Yeni**'yi seçin.
1. **Madde örnekleme** alanına bir değer girin.
1. **Açıklama** alanında bir değer girin.
1. **Değer** alanına bir sayı girin. Bu değer, bitişik alanda seçilen miktar belirtimi değeriyle ilgilidir.
1. Bir test başarısız olduğunda, tüm lot veya sipariş satırı miktarının engellenmesi için, **İşlem** bölümünde **Tam durdurma** onay kutusunu seçin. Bu onay kutusu temizlenirse, test başarısız olduğunda yalnızca kalite emrindeki maddeler engellenir.
1. **Kaydet**'i seçin.
1. Sayfayı kapatın.

> [!NOTE]
> *Ambar işlemleri için kalite yönetimi* özelliği bazı ek madde örnekleme yetenekleri sağlar. *Madde örnekleme kapsamı* kavramı ve miktar belirtimi olarak tam plaka tanımlamaya olanak tanır. Bu özelliği etkinleştirdiyseniz bkz. [Ambar işlemleri için kalite yönetimi](quality-management-for-warehouses-processes.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
