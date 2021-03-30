---
title: Fatura toplamlarını eşleştirme sırasında uyuşmazlıkları gidermeye genel bakış
description: Fatura toplamları eşleştirmesini, toplam fatura tutarlarının beklenen tutarlar ile aralarındaki farkın kabul edilebilir bir düzeyden fazla olmadığını garanti etmek için kullanabilirsiniz.
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: roschlom
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0635f388dba16a1e4374f0915fbab5b88c3b76ab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227462"
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