---
title: Fatura toplamlarını eşleştirme sırasında uyuşmazlıkları gidermeye genel bakış
description: Fatura toplamları eşleştirmesini, toplam fatura tutarlarının beklenen tutarlar ile aralarındaki farkın kabul edilebilir bir düzeyden fazla olmadığını garanti etmek için kullanabilirsiniz.
author: abruer
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "63413"
- intro-internal
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 71e9b4940f910e0ecb7bff148b5cb7b77ab66ec9
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/03/2021
ms.locfileid: "6337339"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching-overview"></a>Fatura toplamlarını eşleştirme sırasında uyuşmazlıkları gidermeye genel bakış

[!include [banner](../includes/banner.md)]

Bir fatura eşleştirme doğrulaması türü eşleşen fatura toplamlarıdır. Sistemin eşleşen fatura toplamları gerçekleştirmesi gerektiğini belirtmek için **Borç hesapları parametreleri** sayfası **fatura doğrulama** sekmesinde, **fatura toplamları eşleştir** seçeneğini **Evet** olarak ayarlayın. 

Fatura toplamları eşleştirmesini, toplam fatura tutarlarının beklenen tutarlar ile aralarındaki farkın kabul edilebilir bir düzeyden fazla olmadığını garanti etmek için kullanabilirsiniz. Altı toplamları **fatura toplamları eşleşme ayrıntıları** sayfasında karşılaştırılır. Toplamlardan herhangi birini beklenen karşılık gelen satınalma siparişi toplamından saparsa, eşleşen bir tutarsızlık işaretlenir. 

Toplamlar eşleşme tutarsızlıkları içeren faturayı gözden geçirmek için **satıcı fatura girişi** çalışma alanında **bekleyen faturalar** döşemesini tıklatın. Daha sonra eylem bölmesinde, üzerinde **İnceleme** sekmesinde, **eşleştirme ayrıntıları**'nı tıklatın. Eşleşme tutarsızlığı algılanırsa, uyarı simgeleri fatura tutarı yanında görünür. Toplamları hakkında daha fazla ayrıntıyı fatura toplamları eşleşme ayrıntılarını görüntüleyerek görebilirsiniz. 

Farklılığı belirledikten sonra, faturadaki bilgilerin yanlış olduğunu düşünüyorsanız satıcınıza başvurmanız gerekebilir. Satıcıyla son anlaşmanıza bağlı olarak aşağıdaki eylemlerden birini gerçekleştirebilirsiniz:

-   Fiyat farkını kabul edin ve eşleşme tutarsızlıkları içeren faturayı nakledin. Eşleşen çelişki olursa deftere nakletmeden önce onay gerektirecek şekilde sisteminiz ayarlanmış olabilir. Bu durumda, eşleşen bir tutarsızlık onaylamanız gerekir ve isteğe bağlı olarak bir onay yorumu girebilirsiniz. Sonra faturayı nakletmeyi seçebilirsiniz.
-   Fatura tutarını beklenen tutarla değiştirin ve faturayı nakledin.
-   Satıcıdan tam kredi ve düzeltilmiş yeni bir fatura talep edin.

Daha fazla bilgi için bkz. [Özel durumları Araştırma/Çözme](tasks/research-resolve-exceptions.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]