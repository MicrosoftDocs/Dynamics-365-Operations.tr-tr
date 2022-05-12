---
title: Abonelik faturalamasına genel bakış
description: Bu konuda Microsoft Dynamics 365 Finance'te abonelik faturalaması açıklanmaktadır.
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-02-09
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 9d46492cca3cc435048fa497f6b1f3a28b77140a
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644541"
---
# <a name="subscription-billing-overview"></a>Abonelik faturalamasına genel bakış

[!include [banner](../includes/banner.md)]

Abonelik faturalaması, kuruluşların abonelik geliri fırsatlarını ve fatura zamanlamaları aracılığıyla yinelenen faturalamayı yönetmesini sağlar. Karmaşık fiyatlama ve faturalama modelleri ve gelir tahsisatı kolayca yönetilebilir ve satır düzeyinde faturalanabilir ve kabul edilebilir. Çok öğeli gelir tahsisatı, gelirin tahsisinde Uluslararası Muhasebe Standartlarına (Uluslararası Finansal Raporlama Standardı 15 \[IFRS15 \]) ve Genel Olarak Kabul Edilmiş Muhasebe İlkeleri (ABD GAAP) standartlarına (Muhasebe Standartları Kodlama Konusu 606 \[ASC 606\]) ile uyumlu olacak şekilde tahsisat yapılmasını sağlar.

Çözüm için bağımsız olarak kullanılabilen üç modül vardır. Alternatif olarak, üç modülün tümü birlikte kullanılabilir.

- **Yinelenen sözleşme faturalaması** – Bu modül, fiyatlandırma ve faturalama parametreleri, sözleşme yenilemesi ve birleştirilmiş faturalama üzerinde kontrol sağlamak için tekrarlanan faturalama ve fiyat yönetiminin kullanılmasını sağlar.
- **Gelir ve gider ertelemeleri** – Bu modül, geliri yöneterek ve aylık yinelenen gelire gerçek zamanlı bilgiler sağlayarak, harici sistemlerdeki el ile yapılan işlemleri ve bağımlılığı ortadan kaldırır.
- **Çok öğeli gelir tahsisatı** – Bu modül, birden çok madde arasında fiyatlandırma ve gelir tahsisatı işlemlerini gerçekleştirerek gelir uyumluluğu sağlanmasına yardımcı olur.

Abonelik faturalaması hakkında daha fazla bilgi için bkz. [Abonelik faturalaması Power BI içeriği](sub-bill-power-bi.md).

Abonelik faturalaması **Özellik yönetimi** üzerinden etkinleştirilir. Ancak, **Gelir kabulü** özelliğiyle birlikte kullanılamaz. Bu nedenle, abonelik faturalaması özelliğini etkinleştirmeden önce bu özelliği devre dışı bırakmanız gerekir.

1. **Özellik Yönetimi** çalışma alanında, **Tümü** sekmesinde, filtreye **Gelir kabulü** girin ve ardından filtre olarak özellik adını seçin.
2. **Gelir kabulü** özelliğini ve ardından **Devre dışı bırak**'ı seçin.
3. **Özellik adı** filtresinde, **Abonelik faturalaması** girib ve modül filtresini seçin.
4. **Abonelik faturalaması** özelliğini ve ardından **Etkinleştir**'i seçin.
5. Önceki listeden üç modülden birini seçin ve sonra **Etkinleştir**'i seçin. Diğer iki modülün her biri için bu adımı tekrarlayın.

    > [!IMPORTANT]
    > Üç modülden herhangi birini etkinleştirebilmeniz için **Abonelik faturalaması** özelliğinin etkinleştirilmesi gerekir.
