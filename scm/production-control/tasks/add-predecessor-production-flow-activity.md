--- 
title: "Üretim akışı faaliyetine bir öncel ekleme"
description: "Üretim akışı sürümünde, tüm faaliyetlerin sıralı olması gerekir."
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: c1afd6a5c2eb5235a42fc9aeea0c8aed6d33e0c9
ms.contentlocale: tr-tr
ms.lasthandoff: 07/28/2017

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>Üretim akışı faaliyetine bir öncel ekleme

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


