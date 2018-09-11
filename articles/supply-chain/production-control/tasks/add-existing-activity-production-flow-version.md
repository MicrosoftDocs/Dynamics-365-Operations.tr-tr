--- 
title: "Üretim akışı sürümüne mevcut bir faaliyeti ekleme"
description: "Üretim akışlarının yeni sürümlerini oluştururken, daha eski sürümler için oluşturulmuş faaliyetleri yeni sürüme eklemeyi seçebilirsiniz."
author: cvocph
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a74fb34db71ba4b539c1b6ede361329aaeb94920
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a>Üretim akışı sürümüne mevcut bir faaliyeti ekleme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Üretim akışlarının yeni sürümlerini oluştururken, daha eski sürümler için oluşturulmuş faaliyetleri yeni sürüme eklemeyi seçebilirsiniz. Bu yordam, faaliyetleri kopyalamadan mevcut bir üretim akışı için yeni bir sürüm oluşturmayı gösterir. Sonraki adımda, mevcut faaliyet yeni sürüme eklenir. 

Bu görev, önceden oluşturulmuş sürüme ve faaliyetlere sahip üretim akışı gerektirir.


## <a name="create-a-new-production-flow-version"></a>Yeni bir üretim akışı sürümü oluştur
1. Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Düzenle'yi tıklatın.
5. Listede, seçili satırı işaretleyin.
6. Bitiş tarihi alanına bir tarih ve saat girin.
    * Yeni bir üretim akışı sürümü oluşturmadan önce, etkin sürümün bitiş tarihini ve saatini denetlediğinizden emin olun. Yeni sürüm seçili sürümün bitiş tarihine bağlanan yürürlükteki başlangıç tarihi ile oluşturulur.  
7. Ekle öğesini tıklatın.
8. Sürümden kopyala alanında Hayır'ı seçin.
    * Kopyalanan sürüme ait faaliyetlerin çoğu yeni faaliyetlerle değiştirilecekse boş bir sürümle başlamak için Hayır'ı seçin. Değiştirilmeyen faaliyetleri faaliyet formundaki Mevcut işlev ekle seçeneğine el ile ekleyin.  
9. Kanban kurallarını çoğalt alanında Hayır'ı seçin.
    * Faaliyetler yeni sürüme kopyalanmadığında, yeni sürümü oluşturma sırasında kanban kurallarını kopyalamak mümkün değildir.   Bunun yerine, eski üretim akışı sürümünün kanban kurallarını yeni sürümün faaliyetlerini kullanan kanban kuralları ile değiştirmek için, daha sonra kanban kuralı formunda Yeni kanban oluşturma işlevini kullanacaksınız.  
10. Tamam'a tıklayın.
11. Listede, istenen kaydı bulun ve seçin.

## <a name="add-an-existing-activity"></a>Var olan faaliyeti ekleme
1. Faaliyetler'i tıklatın.
2. İletişim kutusunu açmak için Varolanı ekle'ye tıklayın.
    * Yeni üretim akışı sürümüne eklenecek mevcut faaliyeti bulun ve ekleyin.  Listede akışın önceki tüm sürümlerinde bu üretim akışı için oluşturulan tüm faaliyetlerin gösterildiğini unutmayın.  
3. Faaliyet alanına bir değer girin veya buradan bir değer seçin.
4. Tamam'a tıklayın.


