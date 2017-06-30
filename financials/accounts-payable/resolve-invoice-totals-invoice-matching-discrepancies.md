---
title: "Fatura toplamları eşleştirme sırasındaki tutarsızlıkları çözümleme"
description: 
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 8773773d9686bf5061958fbe414ed1fef7288f81
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a>Fatura toplamları eşleştirme sırasındaki tutarsızlıkları çözümleme

[!include[banner](../includes/banner.md)]




Bir fatura doğrulama karşılaştırma türü eşleşen fatura toplamlarıdır. Sistemin eşleşen fatura toplamları gerçekleştirmesi gerektiğini belirtmek için **Borç hesapları parametreleri** sayfası **fatura doğrulama** sekmesinde, **fatura toplamları eşleştir** seçeneğini **Evet** olarak ayarlayın. 

Fatura toplamları eşleştirmesini, toplam fatura tutarlarının beklenen tutarlar ile aralarındaki farkın kabul edilebilir bir düzeyden fazla olmadığını garanti etmek için kullanabilirsiniz. Altı toplamları **fatura toplamları eşleşme ayrıntıları** sayfasında karşılaştırılır. Toplamlardan herhangi birini beklenen karşılık gelen satınalma siparişi toplamından saparsa, eşleşen bir tutarsızlık işaretlenir. 

Toplamlar eşleşme tutarsızlıkları içeren faturayı gözden geçirmek için **satıcı fatura girişi** çalışma alanında **bekleyen faturalar** döşemesini tıklatın. Daha sonra eylem bölmesinde, üzerinde **İnceleme** sekmesinde, **eşleştirme ayrıntıları**'nı tıklatın. Eşleşme tutarsızlığı algılanırsa, uyarı simgeleri fatura tutarı yanında görünür. Toplamları hakkında daha fazla ayrıntıyı fatura toplamları eşleşme ayrıntılarını görüntüleyerek görebilirsiniz. 

Farklılığı belirledikten sonra, faturadaki bilgilerin yanlış olduğunu düşünüyorsanız satıcınıza başvurmanız gerekebilir. Satıcıyla son anlaşmanıza bağlı olarak aşağıdaki eylemlerden birini gerçekleştirebilirsiniz:

-   Fiyat farkını kabul edin ve eşleşme tutarsızlıkları içeren faturayı nakledin. Eşleşen çelişki olursa deftere nakletmeden önce onay gerektirecek şekilde sisteminiz ayarlanmış olabilir. Bu durumda, eşleşen bir tutarsızlık onaylamanız gerekir ve isteğe bağlı olarak bir onay yorumu girebilirsiniz. Sonra faturayı nakletmeyi seçebilirsiniz.
-   Fatura tutarını beklenen tutarla değiştirin ve faturayı nakledin.
-   Satıcıdan tam kredi ve düzeltilmiş yeni bir fatura talep edin.





