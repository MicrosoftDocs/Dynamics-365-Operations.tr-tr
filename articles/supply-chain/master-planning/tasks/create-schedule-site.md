---
title: Tesis için zaman çizelgesi oluşturma
description: Bu prosedürde bir saha için henüz başlamamış üretim emirlerinin nasıl zamanlanacağı açıklanmıştır.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0db5095020bc14d56ae3680e7d0caa68789180e
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469296"
---
# <a name="create-a-schedule-for-a-site"></a>Tesis için zaman çizelgesi oluşturma

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]