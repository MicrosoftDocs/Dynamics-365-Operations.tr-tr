---
title: Kalite yönetimi madde örnekleme
description: Bu makale, madde örneklemenin nasıl ayarlanacağını açıklar.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 644eae4fbd9f82027c1cb69efba00dc893f8fc66
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865164"
---
# <a name="quality-management-item-sampling"></a>Kalite yönetimi madde örnekleme

[!include [banner](../includes/banner.md)]

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
