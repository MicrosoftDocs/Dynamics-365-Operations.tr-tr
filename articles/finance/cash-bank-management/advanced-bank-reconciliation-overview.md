---
title: Gelişmiş banka mutabakatına genel bakış
description: Bu makale gelişmiş banka mutabakat işleminin akışını açıklar. Gelişmiş banka mutabakatı özelliği, banka hareketleri içinden otomatik olarak mutabakatı alınan banka ekstrelerini içe aktarmanıza izin verir.
author: angelad116
ms.date: 10/24/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: kfend
ms.custom:
- "22104"
- intro-internal
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 677a032ce77fbe57393c85235a1c64dba3958f2d
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715163"
---
# <a name="advanced-bank-reconciliation-overview"></a>Gelişmiş banka mutabakatına genel bakış

[!include [banner](../includes/banner.md)]

Bu makale gelişmiş banka mutabakat işleminin akışını açıklar. Gelişmiş banka mutabakatı özelliği, banka hareketleri içinden otomatik olarak mutabakatı alınan banka ekstrelerini içe aktarmanıza izin verir.

Gelişmiş banka mutabakatı özelliği banka ekstrelerini içe aktarmanıza izin verir. İçe aktarılan banka ekstresi için daha sonra banka hareketleri içinde otomatik olarak mutabakat sağlanabilir. Burada, gelişmiş banka mutabakatı akış içindeki adımlar açıklanmıştır.

1.  Bir banka ekstresini içe aktarın.
    -   Banka ekstrelerini veri varlığı çerçevesiyle içe aktarın.
    -   Üç tipik banka ekstresi formatı oluşturulur: ISO20022, BAI2 ve MT940.
    -   Bu işlev herhangi bir formata genişletilebilir.

2.  Gelişmiş banka mutabakatı için kullanılacak bir numara sırası oluşturun ve banka mutabakatı eşleştirme kurallarını tanımlayın.
    -   Bir mutabakat eşleştirme kuralı, mutabakat süreci sırasında banka ekstresi satırlarını ve Microsoft Dynamics 365 Finance banka hareketi satırlarını filtrelemek için kullanılan bir ölçüt kümesidir. İş yönteminize bağlı olarak, birden fazla eşleşme kuralını, mutabakat sürecinizi otomatikleştirme ve optimize etmek için ayarlayabilirsiniz.

3.  Banka ekstrelerinin Finance banka hareketleriyle mutabakatını sağlayın.
    -   Mutabakat günlükleri için otomatik eşleştirme ve oluşturma işlemleri yürütün.
    -   Banka ekstrelerini ve Finance banka hareketlerini yan yana görüntüleyin.
    -   Bir banka ekstresinde görüntülenmesine karşın Finance uygulamasında görüntülenmiyorsa, Finance banka hareketlerini otomatik olarak nakledin.
    -   Bir mutabakat tablosu oluşturun.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
