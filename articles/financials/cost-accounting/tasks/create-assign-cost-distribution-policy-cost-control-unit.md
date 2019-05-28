---
title: Maliyet dağıtım ilkesi oluşturma ve bir maliyet kontrol birimine atama
description: Maliyet dağıtım kuralları, bir maliyet merkezinde mali olarak sayılmış maliyetleri dağıtmak için kullanılır.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46ba6322f2cea7828033c214502accdf73f073be
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543876"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a>Maliyet dağıtım ilkesi oluşturma ve bir maliyet kontrol birimine atama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Maliyet dağıtım kuralları, bir maliyet merkezinde mali olarak sayılmış maliyetleri dağıtmak için kullanılır. Maliyet muhasebecisi, maliyetin seçilen tahsisat tabanına dayanarak maliyet merkezlerinde dağıtıldığından emin olur. Bir ilke ve karşılık gelen kurallar bir maliyet kontrol birimine atanır. Bu görev kılavuzu, bir maliyet dağıtım ilkesi ve karşılık gelen kuralları oluşturmayı göstermek için bir örnek kullanır.


## <a name="create-a-policy"></a>Bir ilke oluşturun
1. Maliyet muhasebesi > İlkeler > Maliyet dağıtım ilkeleri'ne gidin.
2. Yeni'ye tıklayın.
3. İlke adı alanına bir değer girin.
4. Açıklama alanına bir değer girin.
5. Maliyet nesnesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.
    * Kuruluşu seçin.  
6. Maliyet öğesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.
    * CDS P/L seçin.  
7. İstatistiksel boyutu alanına bir değer girin veya bir değer seçin.
    * İstatistiksel öğeler'i seçin.  
8. Kaydet'e tıklayın.

## <a name="create-rules-for-the-policy"></a>İlke için kurallar oluşturun
1. Yeni'ye tıklayın.
2. Listede, seçili satırı işaretleyin.
3. Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.
    * 094 seçmek için hiyerarşiyi genişletin.  
4. Maliyet öğesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.
    * Diğer işletme giderlerini seçin ve daha sonra 605110 Temizlik öğesini seçin.  
5. Maliyet davranışı alanında, bir seçenek seçin.
    * Sabit maliyet'i seçin  
6. Tahsisat tabanı alanına bir değer girin veya buradan bir değer seçin.
7. Yeni'ye tıklayın.
8. Listede, seçili satırı işaretleyin.
9. Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.
    * 094 seçmek için hiyerarşiyi genişletin.  
10. Maliyet öğesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.
    * Diğer işletme giderlerini seçin ve daha sonra 605150 Kira öğesini seçin.  
11. Maliyet davranışı alanında, bir seçenek seçin.
    * Sabit maliyet'i seçin  
12. Tahsisat tabanı alanına bir değer girin veya buradan bir değer seçin.
13. Kaydet'e tıklayın.

## <a name="assign-rules-to-a-cost-control-unit"></a>Bir maliyet kontrol birimine kurallar atayın
1. Maliyet kontrol birimi için ilke atamaları'na tıklayın.
2. Yeni'ye tıklayın.
3. Listede, seçili satırı işaretleyin.
4. Geçerlilik tarihi muhasebe veri alanına bir tarih girin.
    * Geçerli mali yılda Eylül 1'i seçin.  
5. Maliyet kontrol birimi alanına bir değer girin veya bir değer seçin.
6. Kaydet'e tıklayın.

