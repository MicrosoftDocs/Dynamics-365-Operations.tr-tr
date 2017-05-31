---
title: "Gelişmiş banka mutabakatına genel bakış"
description: "Bu makale gelişmiş banka mutabakat işleminin akışını açıklar. Gelişmiş banka mutabakatı özelliği, banka hareketleri içinden otomatik olarak mutabakatı alınan banka ekstrelerini içe aktarmanıza izin verir."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: deba55d5e1e376f3f4063f372bfe853fcaf20498
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Gelişmiş banka mutabakatına genel bakış

[!include[banner](../includes/banner.md)]


Bu makale gelişmiş banka mutabakat işleminin akışını açıklar. Gelişmiş banka mutabakatı özelliği, banka hareketleri içinden otomatik olarak mutabakatı alınan banka ekstrelerini içe aktarmanıza izin verir.

Gelişmiş banka mutabakatı özelliği banka ekstrelerini içe aktarmanıza izin verir. İçe aktarılan banka ekstresi için daha sonra banka hareketleri içinde otomatik olarak mutabakat sağlanabilir. Burada, gelişmiş banka mutabakatı akış içindeki adımlar açıklanmıştır.

1.  Bir banka ekstresini içe aktarın.
    -   Banka ekstrelerini veri varlığı çerçevesiyle içe aktarın.
    -   Üç tipik banka ekstresi formatı oluşturulur: ISO20022, BAI2 ve MT940.
    -   Bu işlev herhangi bir formata genişletilebilir.

2.  Gelişmiş banka mutabakatı için kullanılacak bir numara sırası oluşturun ve banka mutabakatı eşleştirme kurallarını tanımlayın.
    -   Bir mutabakat eşleştirme kuralı, mutabakat süreci sırasında banka ekstresi satırlarını ve Microsoft Dynamics 365 for Operations banka hareket satırlarını filtrelemek için kullanılan bir ölçüt kümesidir. İş yönteminize bağlı olarak, birden fazla eşleşme kuralını, mutabakat sürecinizi otomatikleştirme ve optimize etmek için ayarlayabilirsiniz.

3.  Banka ekstrelerinin Dynamics 365 for Operations banka hareketleriyle mutabakatını sağlayın.
    -   Mutabakat günlükleri için otomatik eşleştirme ve oluşturma işlemleri yürütün.
    -   Banka ekstrelerini ve Dynamics 365 for Operations banka hareketlerini yan yana görüntüleyin.
    -   Bir banka ekstresinde görüntülenmesine karşın Dynamics 365 for Operations'ta görüntülenmiyorsa, Dynamics 365 for Operations banka hareketlerini otomatik olarak nakledin.
    -   Bir mutabakat tablosu oluşturun.






