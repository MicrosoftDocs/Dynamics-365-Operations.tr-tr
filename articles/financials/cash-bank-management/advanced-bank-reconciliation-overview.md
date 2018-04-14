---
title: "Gelişmiş banka mutabakatına genel bakış"
description: "Bu makale gelişmiş banka mutabakat işleminin akışını açıklar. Gelişmiş banka mutabakatı özelliği, banka hareketleri içinden otomatik olarak mutabakatı alınan banka ekstrelerini içe aktarmanıza izin verir."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ff59250b836a73986848109ce48f843fed1d71a9
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="advanced-bank-reconciliation-overview"></a>Gelişmiş banka mutabakatına genel bakış

[!INCLUDE [banner](../includes/banner.md)]

Bu makale gelişmiş banka mutabakat işleminin akışını açıklar. Gelişmiş banka mutabakatı özelliği, banka hareketleri içinden otomatik olarak mutabakatı alınan banka ekstrelerini içe aktarmanıza izin verir.

Gelişmiş banka mutabakatı özelliği banka ekstrelerini içe aktarmanıza izin verir. İçe aktarılan banka ekstresi için daha sonra banka hareketleri içinde otomatik olarak mutabakat sağlanabilir. Burada, gelişmiş banka mutabakatı akış içindeki adımlar açıklanmıştır.

1.  Bir banka ekstresini içe aktarın.
    -   Banka ekstrelerini veri varlığı çerçevesiyle içe aktarın.
    -   Üç tipik banka ekstresi formatı oluşturulur: ISO20022, BAI2 ve MT940.
    -   Bu işlev herhangi bir formata genişletilebilir.

2.  Gelişmiş banka mutabakatı için kullanılacak bir numara sırası oluşturun ve banka mutabakatı eşleştirme kurallarını tanımlayın.
    -   Mutabakat eşleştirme kuralı, mutabakat süreci sırasında banka ekstresi satırlarını ve Microsoft Dynamics 365 for Finance and Operations banka hareket satırlarını filtrelemek için kullanılan bir ölçüt kümesidir. İş yönteminize bağlı olarak, birden fazla eşleşme kuralını, mutabakat sürecinizi otomatikleştirme ve optimize etmek için ayarlayabilirsiniz.

3.  Banka ekstrelerinin Finance and Operations banka hareketleriyle mutabakatını sağlayın.
    -   Mutabakat günlükleri için otomatik eşleştirme ve oluşturma işlemleri yürütün.
    -   Banka ekstrelerini ve Finance and Operations banka hareketlerini yan yana görüntüleyin.
    -   Bir banka ekstresinde görüntülenmesine karşın Finance and Operations'ta görüntülenmiyorsa, Finance and Operations banka hareketlerini otomatik olarak nakledin.
    -   Bir mutabakat tablosu oluşturun.






