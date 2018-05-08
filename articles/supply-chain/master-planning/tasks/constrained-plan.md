--- 
title: "Kısıtlanmış plan oluşturma"
description: "Bu yordam, hem malzeme hem de kapasite kısıtlamalarını dikkate alan bir planın nasıl oluşturulacağını gösterir."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 59c6a4a2b239b3fd6b6ddc8f06bfd007f0191f0a
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="generate-a-constrained-plan"></a>Kısıtlanmış plan oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, hem malzeme hem de kapasite kısıtlamalarını dikkate alan bir planın nasıl oluşturulacağını gösterir. Plan, üretimin malzemeler hazır olmadan ve kaynaklar kapasite üzerinde rezerve edilmeden önce başlamamasını sağlar. 

Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu yordam için üretim planlayıcısına yöneliktir.


## <a name="set-up-a-constrained-plan"></a>Kısıtlı bir plan ayarlayın
1. Master planlama'ya tıklayın.
2. Master planlar'a tıklayın.
3. Listede, istenen kaydı bulun ve seçin.
    * Örnek: StaticPlan  
4. Sınırlı kapasite alanında Evet'i seçin.
5. Sınırlı kapasite zaman dilimi alanına '30' girin.
6. Gün cinsinden zaman dilimleri bölümünü genişletin.
7. Kapasite alanında Evet'i seçin.
8. Kapasite planlama zaman dilimi (gün) alanına bir sayı girin.
    * Örnek: 60  
9. Hesaplanan gecikmeler alanında Evet'i seçin.
10. Gecikme zaman dilimini (gün) hesapla alanına bir sayı girin.
    * Örnek: 60  
11. Hesaplanan gecikmeler bölümünü genişletin.
12. Hesaplanan gecikmeyi gereksinim tarihine ekle alanında Evet'i seçin.
13. Hesaplanan gecikmeyi gereksinim tarihine ekle alanında Evet'i seçin.
14. Hesaplanan gecikmeyi gereksinim tarihine ekle alanında Evet'i seçin.
15. Sayfayı kapatın.

## <a name="create-a-constrained-plan"></a>Sınırlandırılmış bir plan oluşturma
1. Çalıştır öğesine tıklayın.
2. Master plan alanında bir değer girin veya seçin.
    * Kısıtlamalar ayarladığınız planı seçin.  
3. Tamam'a tıklayın.
    * Bu işlem biraz zaman alabilir.  
4. Planlı siparişler'e tıklayın.


