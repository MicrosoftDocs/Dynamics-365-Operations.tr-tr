---
title: İçeri aktarma işlerinde tarihi ve saati eşitleme
description: Saat dilimi dönüştürmelerinde sorunları önlemek için içeri aktarma işlerinde UTC saat dilimlerini kullanın.
author: peakerbl
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c76eadc5839785ba1624ee3894ef1d0872369aa9
ms.sourcegitcommit: 7aa7d756e1e98a53da62e03c608a9597ef9893ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2021
ms.locfileid: "7403853"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>İçeri aktarma işlerinde tarihi ve saati eşitleme

[!include [banner](../includes/banner.md)]

İçeri aktarma işinizin saat dilimini Eşgüdümlü Evrensel Saat'e (UTC) göre ayarlamanız önemlidir. Farklı bir ayar kullanırsanız içeri aktarılan verilerinizde beklenmeyen tarihler ve saatler görebilirsiniz. Doğru ayar olmazsa içeri aktarma işlemi UTC tarihini yerel biçime dönüştürür ve sonra sistem ayarları bunu yeniden dönüştürür.

Bu çift dönüştürme, uygulamalar arasında tarihlerin değişmesine neden olur. Örneğin, yerel saat dilimlerindeki farklar nedeniyle çift dönüştürme sorunu, bir çalışanın başlangıç tarihinin Dynamics 365 Human Resources ve Dynamics 365 Finance arasında farklı olmasına neden olabilir. İçeri aktar işini UTC'ye ayarlamak bu sorunu çözer.

1. Dynamics 365 Finance and Operations'da, **Veri yönetimi**'ni seçin.

2. **Projeleri içeri aktar**'ı ve ardından projeyi seçin.

3. **Kaynak tarih biçimi** bölümünde, **CSV-Unicode**'u seçin.

   [![Kaynak tarih biçimini UTC'ye dönüştürme.](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. **Saat dilimi**'ni **Eşgüdümlü Evrensel Saat** olarak değiştirin ve **Dil**'i **En-US** olarak değiştirin.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
