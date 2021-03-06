---
title: Maliyet tahsisatı ilkesi oluşturma ve bir maliyet kontrol birimine atama
description: Bu yordamı bir maliyet tahsisat ilkesini ve karşılık gelen kuralları oluşturmak ve bir maliyet kontrol birimine atamak için kullanın.
author: ShylaThompson
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1cff10132e8007be885e9c69d97cf96c30d69f50
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822867"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a>Maliyet tahsisatı ilkesi oluşturma ve bir maliyet kontrol birimine atama

[!include [banner](../../includes/banner.md)]

Bu yordamı bir maliyet tahsisat ilkesini ve karşılık gelen kuralları oluşturmak ve bir maliyet kontrol birimine atamak için kullanın. Bu kayıt USP2 demo veri şirketini kullanır.


## <a name="create-a-policy"></a>Bir ilke oluşturun
1. Maliyet muhasebesi > İlkeler > Maliyet tahsisat ilkeleri'ne gidin.
2. Yeni'ye tıklayın.
3. İlke adı alanına bir değer girin.
4. Maliyet nesnesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.
    * Kuruluşu seçin.  
5. İstatistiksel boyutu alanına bir değer girin veya bir değer seçin.
6. Kaydet'e tıklayın.

## <a name="create-allocation-rules"></a>Tahsisat kuralları oluşturun
1. Yeni'ye tıklayın.
2. Listede, seçili satırı işaretleyin.
3. Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.
4. Maliyet davranışı alanında, 'Toplam'ı seçin.
5. Tahsisat tabanı alanına bir değer girin veya buradan bir değer seçin.
6. Yeni'ye tıklayın.
7. Listede, seçili satırı işaretleyin.
8. Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.
9. Maliyet davranışı alanında, 'Toplam'ı seçin.
10. Tahsisat tabanı alanına bir değer girin veya buradan bir değer seçin.
11. Yeni'ye tıklayın.
12. Listede, seçili satırı işaretleyin.
13. Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.
14. Maliyet davranışı alanında, 'Toplam'ı seçin.
15. Tahsisat tabanı alanına bir değer girin veya buradan bir değer seçin.
    * Tüm kuralları oluşturana kadar devam edin.  
16. Kaydet'e tıklayın.

## <a name="assign-the-policy-to-a-cost-control-unit"></a>İlkeyi bir maliyet kontrol birimine atayın
1. Maliyet kontrol birimi için ilke atamaları'na tıklayın.
2. Yeni'ye tıklayın.
3. Listede, seçili satırı işaretleyin.
4. Geçerlilik tarihi muhasebe veri alanına bir tarih girin.
    * Kuralların geçerlilik tarihi vardır. Sistemdeki bir kullanıcı, yeni bir sürüm oluşturulmuşsa kuralların vadesini doldurabilir.  
5. Maliyet kontrol birimi alanına bir değer girin veya bir değer seçin.
6. Kaydet'e tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]