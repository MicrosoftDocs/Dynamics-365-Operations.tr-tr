---
title: Ödeme tutarı türleri ekle
description: Bu makalede, Varlık kiralamada ödeme tutarı türlerinin nasıl ayarlanacağı açıklanmaktadır.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 03fc903e6cfe78ef2fed7e3a0744a8f809f6892d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891623"
---
# <a name="add-payment-amount-types"></a>Ödeme tutarı türleri ekle

[!include [banner](../includes/banner.md)]

Bu makalede, Varlık kiralamada ödeme tutarı türlerinin nasıl ayarlanacağı açıklanmaktadır. Bu şekilde, ödeme planı satırlarına peşin ödeme tutarını eklemek yerine, kira ödemesi tutarını silebilirsiniz.

Ödeme tutarı türleri eklemek için bu adımları izleyin.

1. **Varlık kiralama \> Kurulum \> Ödeme tutarı**'na gidin.
2. **Yeni**'yi seçin.
3. Yeni ödeme tipini ve açıklamasını girin.

> [!NOTE]
> IFRS 16 dizin yeniden değerlendirmesi için, bir ödeme tutarı türü oluşturmanız ve bunu **IRFS 16 endeks yeniden değerlemesi için kullanıldı** olarak işaretlemeniz gerekir. Bu ödeme tutarı türü, IFRS 16 defteriyle ilgili olarak dizin yeniden değerleme işlemi çalıştırıldığında kullanılır ve dizin yeniden değerleme işlemi nedeniyle oluşan değişiklikleri dikkate alır.
>
> Kiradaki **Ödeme dökümü** seçeneği **Evet** olarak ayarlandığında, IFRS 16 için dizin yeniden değerlemesi çalışıyorsa ancak IFRS 16 için herhangi bir ödeme türü yoksa, işlem tamamlanmaz.

Yalnızca tek bir kayıt **IFRS 16 dizin yeniden değerlendirmesi için kullanıldı** olarak işaretlenebilir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
