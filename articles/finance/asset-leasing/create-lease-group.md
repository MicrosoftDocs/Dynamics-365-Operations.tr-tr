---
title: Kiralama grubu oluşturma
description: Bu makalede, kiralama gruplarının nasıl ayarlanacağı açıklanmaktadır. Yeni kiralamalar oluşturmak için kiralama grupları gereklidir.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseGroupTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: cd1a6f61346233bf205657917c65fccd82167f7f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895036"
---
# <a name="create-a-lease-group"></a>Kiralama grubu oluşturma

[!include [banner](../includes/banner.md)]

Bu makalede, kiralama gruplarının nasıl ayarlanacağı açıklanmaktadır. Yeni kiralamalar oluşturmak için kiralama grupları gereklidir. Kiralama defterleri her bir kiralama grubuyla ilişkilidir. Kiralama defterleri, her kiralama için oluşturulması gereken varsayılan defterleri belirler. **Kiralamayı deftere nakletme parametreleri** sayfasında bir kiralama grubuna belirli hesaplar atayabilirsiniz.

## <a name="create-a-lease-book-and-add-a-lease-group"></a>Kiralama defteri oluşturma ve kiralama grubu ekleme

1. **Varlık kiralama \> Kurulum \> Kiralama grupları**'na gidin.
2. Eylem Bölmesinde, kiralama grubu eklemek için **Yeni**'yi seçin. Izgaraya yeni bir satır eklenir.
3. Yeni satırdaki **Kiralama grubu** alanına bir değer girin.
4. **Açıklama** alanında bir değer girin.

Yeni girdiğiniz bilgiler, **Kiralama ekle** sayfasındaki **Kiralama grubu**'na eklenir.

## <a name="associate-a-book-with-a-lease-group"></a>Defteri bir kiralama grubuyla ilişkilendirme

Kiralama grupları oluşturduktan sonra her gruba defter atayabilirsiniz. Kiralama oluşturup bunu bir kiralama grubuna atadıktan sonra sistem, söz konusu kiralama grubuyla ilişkili her defter için bir dizi plan oluşturur.

> [!NOTE]
> Defterler kiralama grubuna atanmadan önce ayarlanmalıdır.

1. **Varlık kiralama \> Kurulum \> Kiralama grubu**'na gidin.
2. Bir kiralama grubunu seçin ve ardından **Defter**'i seçin.
3. **Yeni**'yi seçin ve ardından **Defter türü** alanında kiralama grubuna atanacak defteri seçin. Bir kiralamanın farklı yöntemlerle hesaplanması gerekiyorsa bir kiralama grubuna birden fazla defter atayabilirsiniz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
