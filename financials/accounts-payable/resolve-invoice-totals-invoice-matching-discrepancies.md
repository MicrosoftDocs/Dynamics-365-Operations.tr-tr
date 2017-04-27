---
title: "Fatura toplamları eşleştirme sırasındaki tutarsızlıkları çözümleme"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 1fd606817b06a05b9abaaedf20ea9872bd7edd5d
ms.openlocfilehash: a54b05bba2549a42f24b8425c9ee418c576d056a
ms.lasthandoff: 03/31/2017


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





