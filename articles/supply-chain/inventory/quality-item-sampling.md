---
title: Kalite yönetimi madde örnekleme
description: Bu konu, madde örneklemenin nasıl ayarlanacağını açıklar.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae8bfd329ca0d7c30adcd93a759ee6bea7b76278
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022240"
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
