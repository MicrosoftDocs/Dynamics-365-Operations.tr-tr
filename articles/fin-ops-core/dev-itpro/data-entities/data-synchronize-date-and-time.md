---
title: İçeri aktarma işlerinde tarihi ve saati eşitleme
description: Saat dilimi dönüştürmelerinde sorunları önlemek için içeri aktarma işlerinde UTC saat dilimlerini kullanın.
author: Sunil-Garg
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32090af050fdb97e7b581cefcfc9155357327441
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351003"
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