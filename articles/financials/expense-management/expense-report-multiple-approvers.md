---
title: Gider raporları ve birden çok onaylayan
description: Bu konu, birden fazla kişi tarafından onay gerektiren gider raporları hakkında bilgi sağlar.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1483de5405895d60f0cb302ab622758b2b05d2ca
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566996"
---
# <a name="expense-reports-and-multiple-approvers"></a>Gider raporları ve birden çok onaylayan

[!include [banner](../includes/banner.md)]

Kuruluşunuzun gider onay ilkelerine bağlı olarak, bir çalışan tarafından gönderilen bir gider raporunu birden fazla kişinin onaylaması gerekebilir. Gider raporu onayı için iş akışı işlemi ayarlarken, bir veya daha fazla gider raporu onaylayanı için görevleri veya adımları içeren iş akışı öğeleri ekleyebilirsiniz. Örneğin, tüm gider raporlarının öncelikle raporu gönderen kişinin yöneticisi ve ardından bir Borç hesapları koordinatörü tarafından onaylanması gerektiğini ayarlayabilirsiniz.

Birden fazla gider raporu onaylayanın gerekli olduğuna karar verirseniz, iş akışı öğelerini şu şekilde ekleyebilirsiniz:

- Bir adım içeren bir onay öğesi ekleyin. Örneğin, adım bir gider raporunun bir kullanıcı grubuna atanmasını ve bunun kullanıcı grubu üyelerinin yüzde 50'si tarafından onaylanmasını gerektirebilir.
- Birden fazla adım içeren bir onay öğesi ekleyin. Örneğin, onay öğesi aşağıdaki adımları içerebilir:

    1. Gider raporunu gönderen çalışanın yöneticisi raporu onaylar.
    2. Borç hesapları memuru girişleri ve gider raporu öğelerini doğrular.
    3. Bütçe sahibi gider raporunu onaylar.

- Her birinin tek bir adımı bulunan birden fazla onay öğesi ekleyin. Örneğin, aşağıdaki adımların her biri için ayrı onay bir öğesi ekleyebilirsiniz:

    1. Çalışanın yöneticisi gider raporunu onaylar.
    2. Bütçe sahibi gider raporunu onaylar.
