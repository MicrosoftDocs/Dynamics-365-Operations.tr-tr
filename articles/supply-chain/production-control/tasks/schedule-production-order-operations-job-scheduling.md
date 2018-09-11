--- 
title: "İşlemler ve iş planlaması olan bir üretim emri planlama"
description: "Bu yordam operasyon planlama ve iş planlama ile bir üretim emri planlamaya odaklanır."
author: ChristianRytt
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d4aac437876862e9f776264fc81f246c820bdf45
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>İşlemler ve iş planlaması olan bir üretim emri planlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam operasyon planlama ve iş planlama ile bir üretim emri planlamaya odaklanır. İşler iş planlama ile oluşturulurken, operasyon planlama ile iş oluşturulmaz. Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu yordam üretim müdürü, üretim planlayıcısı veya ayrı bir üretim ortamında çalışan atölye gözetmenine yöneliktir.


## <a name="create-a-production-order"></a>Üretim emri oluşturma
1. Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.
2. Yeni üretim emri'ne tıklayın.
3. Madde numarası alanında bir değer girin veya seçin.
    * Madde numarası D0001'i seçin.  
4. Oluştur'a tıklayın.

## <a name="schedule-operations-for-the-production-order"></a>Üretim emri için işlemleri planlama
1. Listede, seçili satırı işaretleyin.
    * Yeni oluşturduğunuz üretim emrini seçin. Bu emir listenin en üstünde olmalıdır.      
2. Eylem Bölmesinde, Planla öğesini tıklatın.
3. Operasyonları planla seçeneğine tıklayın.
4. İş planlama çizelgeleme yönü alanında 'Planlama tarihinden ileriye doğru' öğesini seçin.
5. Planlama tarihi alanına bir tarih girin.
    * Gelecekteki bir tarihi, örneğin bugünden itibaren bir hafta sonrasını seçin. Seçili Planlama yönü ile üretim emri bu tarihten ileriye doğru planlanır.  
6. Tamam'a tıklayın.
7. Listede, seçili satırı işaretleyin.
    * Durumun Planlandı olarak değiştiğine dikkat edin.  
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. Tüm işleri çalıştır'ı tıklatın.
    * Operasyon planlaması ile bir iş oluşturulmadığına dikkat edin.  
10. Sayfayı kapatın.

## <a name="schedule-jobs-for-the-production-order"></a>Üretim emri için işleri planlama
1. Eylem Bölmesinde, Planla öğesini tıklatın.
2. İşleri planla'ya tıklayın.
3. İş planlama çizelgeleme yönü alanında 'Planlama tarihinden ileriye doğru' öğesini seçin.
4. Planlama tarihi alanına bir tarih girin.
    * Gelecekteki bir tarihi, örneğin bugünden itibaren bir hafta sonrasını seçin. Seçili Planlama yönü ile üretim emri bu tarihten ileriye doğru planlanır.  
5. Tamam'a tıklayın.
6. Eylem Bölmesinde, Üretim emri öğesine tıklayın.
7. Tüm işleri çalıştır'ı tıklatın.
    * Etkin yola göre, iş planlamasında 5 işin oluşturulduğunda dikkat edin.  


