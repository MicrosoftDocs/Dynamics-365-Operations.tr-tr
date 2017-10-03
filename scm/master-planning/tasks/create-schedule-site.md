--- 
title: "Tesis için zaman çizelgesi oluşturma"
description: "Bu prosedürde bir saha için henüz başlamamış üretim emirlerinin nasıl zamanlanacağı açıklanmıştır."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: a611cb773919284b2bbe55395a7ec2b947d5c0b4
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-schedule-for-a-site"></a>Tesis için zaman çizelgesi oluşturma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu prosedürde bir saha için henüz başlamamış üretim emirlerinin nasıl zamanlanacağı açıklanmıştır.  Bu prosedürün tamamlanması için USMF demo veri şirketi kullanılır.


## <a name="identify-production-orders-that-are-not-started"></a>Başlamamış üretim emirlerini tanımlama
1. Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.
2. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, Saha alanına '1' değeriyle filtre uygulayın.
    * 1, USMF'deki bir sahayı temsil eder. USMF'yi kullanmıyorsanız, kendi şirketinizden bir saha seçin.  
3. Durum sütunu filtresini açın.
4. "tam olarak" filtre işleci kullanılarak bir "Zamanlanmış" değeriyle "Durum" alanına bir filtre uygulayın.

## <a name="create-a-schedule"></a>Bir zamanlama oluşturma
1. Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.
2. Eylem Bölmesinde, Planla öğesini tıklatın.
3. İşleri planla'yı tıklatın.
4. İş planlama çizelgeleme yönü alanında 'Teslimat tarihinden geriye doğru' seçin.
5. Sınırlı kapasite alanında Hayır'ı seçin.
6. Sınırlı malzeme alanında Hayır'ı seçin.
7. Tamam'a tıklayın.
    * Bu işlem biraz zaman alabilir.  

## <a name="view-the-result-of-scheduled-production-orders"></a>Zamanlanmış üretim emirlerinin sonuçlarını görüntüleme
1. Listede, seçili satırı işaretleyin.
    * Herhangi bir sırayı işaretleyebilirsiniz.  
2. Eylem Bölmesinde, Üretim emri öğesine tıklayın.
3. Tüm işleri çalıştır'ı tıklatın.
    * Bu sayfada, işlerin listesini görebilirsiniz. Zamanlama sekmesinde, bir iş için Başlangıç tarihini ve Bitiş tarihini görüntülenebilirsiniz.  
4. Malzemeler öğesini tıklayın.
    * Bu sayfada, üretim emri ve güncel kullanılabilir stok üzerindeki işlemler için tahmini malzeme tüketimini görebilirsiniz.  


