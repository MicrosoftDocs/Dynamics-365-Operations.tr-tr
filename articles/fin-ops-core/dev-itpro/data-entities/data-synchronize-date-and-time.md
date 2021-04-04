---
title: İçeri aktarma işlerinde tarihi ve saati eşitleme
description: Saat dilimi dönüştürmelerinde sorunları önlemek için içeri aktarma işlerinde UTC saat dilimlerini kullanın.
author: Sunil-Garg
manager: tfehr
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
ms.openlocfilehash: 5ce3bf39e8342d3fe19a253f6d17684b2bd0aec0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570493"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>İçeri aktarma işlerinde tarihi ve saati eşitleme

[!include [banner](../includes/banner.md)]

İçeri aktarma işinizin saat dilimini Eşgüdümlü Evrensel Saat'e (UTC) göre ayarlamanız önemlidir. Farklı bir ayar kullanırsanız içeri aktarılan verilerinizde beklenmeyen tarihler ve saatler görebilirsiniz. Doğru ayar olmazsa içeri aktarma işlemi UTC tarihini yerel biçime dönüştürür ve sonra sistem ayarları bunu yeniden dönüştürür.

Bu çift dönüştürme, uygulamalar arasında tarihlerin değişmesine neden olur. Örneğin, yerel saat dilimlerindeki farklar nedeniyle çift dönüştürme sorunu, bir çalışanın başlangıç tarihinin Dynamics 365 Human Resources ve Dynamics 365 Finance arasında farklı olmasına neden olabilir. İçeri aktar işini UTC'ye ayarlamak bu sorunu çözer.

1. Dynamics 365 Finance and Operations'da, **Veri yönetimi**'ni seçin.

2. **Projeleri içeri aktar**'ı ve ardından projeyi seçin.

3. **Kaynak tarih biçimi** bölümünde, **CSV-Unicode**'u seçin.

   [![Kaynak tarih biçimini UTC'ye dönüştürme](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. **Saat dilimi**'ni **Eşgüdümlü Evrensel Saat** olarak değiştirin ve **Dil**'i **En-US** olarak değiştirin.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]