---
title: " Çapraz sevk ve merkezi alım için kurallar ve parametreler ayarlama"
description: Bu yordam, Stok yenileme kuralları oluşturmak için gereken adımları gösterir.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a22756279ba316a7efd4d09c48c55e8cc98ba29d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "366340"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a> Çapraz sevk ve merkezi alım için kurallar ve parametreler ayarlama

[!include[task guide banner](../includes/task-guide-banner.md)]

Bu yordam, Stok yenileme kuralları oluşturmak için gereken adımları gösterir. Stok yenileme kuralları, Çapraz sevk ve Merkezi alım kullanırken ürünlerin mağazalara nasıl dağıtıldığını denetlemek için kullanılabilir. Stok yenileme kuralları, mağazalar veya mağaza grupları için ayarlanabilir. Kuraldaki her satır için tanımlanan ağırlık, Çapraz sevk veya Merkezi alımda dağıtım yöntemi olarak Stok yenilene kuralları kullanıldığında ürünlerin mağazalar arasında nasıl dağıtılacağını kontrol eder. Bu yordam, USRT demo şirketini kullanır.

1. Stok Yenileme kuralları'na gidin.
2. Yeni'ye tıklayın.
3. Stok yenilene kuralı alanına bir değer yazın.
4. Açıklama alanına bir değer girin.
5. Kaydet'e tıklayın.
6. Ekle öğesini tıklatın.
7. Listede, seçili satırı işaretleyin.
    * Tür için Stok yenileme hiyerarşisini veya Kanalı seçebilirsiniz. Değer, Ad bölümündeki seçimin kanallar hiyerarşisi mi yoksa belirli bir kanal mı olacağını denetler.  Bu örnekte, Stok yenileme hiyerarşisi ayarlanmış olarak bırakın.  
8. Ad alanından bir değer seçin.
    * Varsayılan ağırlık değeri ambar tanımlanan ağırlıkla doldurulur.  Bu ağırlık Stok yenileme kuralı için kullanılabilir veya Ağırlık alanına yeni bir ağırlık girebilirsiniz.  
9. Ağırlık alanına bir sayı girin.
10. Ekle öğesini tıklatın.
11. Listede, seçili satırı işaretleyin.
12. Tür alanında 'Kanal'ı seçin.
13. Ad alanına bir değer girin veya buradan bir değer seçin.
14. Ağırlık alanına bir sayı girin.
15. Kaydet'e tıklayın.

