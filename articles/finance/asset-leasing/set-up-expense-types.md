---
title: Gider türlerini ayarlama
description: Bu makalede, Varlık kiralamada giderleri ayarlama açıklanmaktadır.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseExpenseTypeTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9978041059437d5d3556236c7ac02c00db93f933
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908052"
---
# <a name="set-up-expense-types"></a>Gider türlerini ayarlama

[!include [banner](../includes/banner.md)]

Bu makalede, Varlık kiralamada giderleri ayarlama açıklanmaktadır. Ödeme planı ile temsil edilmeyen maliyetler *gider maliyetleri* olarak bilinir. Bu maliyetlere örnek olarak emlak vergileri, ortak alan bakım maliyetleri ve sigorta giderleri verilebilir.

## <a name="add-an-administrative-expense-type"></a>İdari gider türü ekleme

1. **Varlık kiralama \> Kurulum \> Gider türleri**'ne gidin.
2. **Yeni**'yi seçin.
3. Uygun alanlara yeni gider türünü ve açıklamasını girin.

## <a name="assign-accounts-to-administrative-costs"></a>İdari maliyetlere hesaplar atama

Daha sonra, hesapları gider türleriyle ilişkilendirmelisiniz. Gider planı girişleri deftere nakledildiğinde bu hesaplar borçlandırılır. Mahsup hesap, her bir kiralamadaki **İcra maliyeti ödeme planı** satırlarında belirtilir.

1. **Varlık kiralama \> Kurulum \> Varlık kiralama parametreleri**'ne gidin.
2. **Hesaplar** sekmesindeki **İcra maliyetleri** hızlı sekmesinin **Gider türü** alanında gider türünü seçin.
3. **Ekle**'yi seçin.
4. **Defter türü** alanında, idari maliyetlerle ilişkilendirilecek defter türünü seçin.

    > [!NOTE]
    > Aynı gider hesabına birden fazla defter türü bağlanabilir.

5. **Hesap kodu** alanında, defterin hangi kiralamalara uygulanacağını belirtin:

    - **Tümü**: Defteri tüm kiralamalara uygulayın.
    - **Grup**: Defteri belirli bir kiralama grubuna uygulayın.
    - **Tablo**: Defteri belirli kiralamalara uygulayın.

6. **Hesap kodu** alanında **Grup**'u veya **Tablo**'yu seçtiyseniz, **Hesap/Grup numarası** alanında bir hesap numarası veya grup numarası seçin.
7. Uygun alanlarda, finansal kiralama ana hesabını ve işletme kiralaması ana hesabını seçin.

Bu adımları tamamladığınızda, seçili bir kiralamanın **Kiralama ayrıntıları** sayfasınde **İcra maliyeti ödeme planı** satırları üzerinden giderleri ekleyebilirsiniz. Alternatif olarak, yeni bir kiralama oluştururken de giderleri ekleyebilirsiniz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
