---
title: Üretim akışı faaliyetine bir öncel ekleme
description: Üretim akışı sürümünde, tüm faaliyetlerin sıralı olması gerekir.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc1aa742013faeeb545d746f9715c639a5b66b9b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575087"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>Üretim akışı faaliyetine bir öncel ekleme

[!include [banner](../../includes/banner.md)]

Üretim akışı sürümünde, tüm faaliyetlerin sıralı olması gerekir. Bir faaliyet bir veya daha fazla öncele ve ardıla sahip olabilir. 

Bu yordam bir önceli bir faaliyetle ilişkilendirmeyi gösterir. 

Bu görevi gerçekleştirmek için, birbirine bağlanabilen en az iki faaliyetin olduğu Taslak sürümüne sahip bir üretim akışına ihtiyacınız vardır. 

Daha fazla bilgi için, "Üretim akışları ve yalın imalat faaliyetleri" başlıklı teknik raporu okuyun.


## <a name="find-the-production-flow-and-version"></a>Üretim akışını ve sürümünü bulma
1. Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Listede, istenen kaydı bulun ve seçin.
5. Faaliyetler'i tıklatın.

## <a name="select-an-activity-and-add-a-predecessor"></a>Faaliyet seçme ve öncel ekleme
1. Listede, istenen kaydı bulun ve seçin.
2. Öncel ekle öğesine tıklayın.
3. Faaliyet alanına bir değer girin veya buradan bir değer seçin.
4. Döngü süresi oranı alanında bir sayı girin.
    * Bir faaliyet ilişkisinin varsayılan döngü süresi oranı 1'dir. Bu her iki faaliyetin de aynı takt zamanında çalıştığını varsayar. Öncel daha yüksek bir hızda çalışıyorsa (daha düşük takt süresi), bu oran 1'den düşük olmalıdır; öncel daha düşük bir hızda çalışıyorsa (daha yüksek takt süresi), döngü süresi oranı 1'den büyük olur.  
5. Tamam'a tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]