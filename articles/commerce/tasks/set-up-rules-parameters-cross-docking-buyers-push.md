---
title: " Çapraz sevk ve merkezi alım için kurallar ve parametreler ayarlama"
description: Bu yordam, Stok yenileme kuralları oluşturmak için gereken adımları gösterir.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 776defca4a9d2a860901efe9e8890fd11ec8ce7302c53dc1507cc77ff501aded
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753064"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a> Çapraz sevk ve merkezi alım için kurallar ve parametreler ayarlama

[!include [banner](../includes/banner.md)]

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]