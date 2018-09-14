--- 
title: "Tesis için plan oluşturma"
description: "Üretim planlayıcısı, belirli bir maddenin üretim için malzeme ve kapasite gereksinimlerini hesaplar."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1452c5d6f5dd8d0dd4cb08eb5cc9a48fd8f875f9
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-plan-for-a-site"></a>Tesis için plan oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Üretim planlayıcısı, belirli bir maddenin üretim için malzeme ve kapasite gereksinimlerini hesaplar. Kaynak kullanımı önerileri oluşturduktan sonra, acil olanlardan başlanarak, planlama yapılan saha için siparişler ve sipariş tarihleri seçilir. En acil siparişler, güncel tarih olarak belirlenmesi gereken siparişlerdir. Bu görevleri gerçekleştirmek için USMF demo veri şirketini kullanın.


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a>Bir madde için bir malzeme ve kapasite planı oluşturma
1. Master planlama'ya tıklayın.
    * Varsayılan Panoya gitmeniz gerekir.  
2. Çalıştır öğesine tıklayın.
3. Eklenecek kayıtlar bölümünü genişletin.
4. Filtre'ye tıklayın.
5. Listede, seçili satırı işaretleyin.
6. Ölçütler alanına bir değer yazın.
    * Örnek: D0001  
7. Tamam'a tıklayın.
8. Tamam'a tıklayın.
    * Bu işlem birkaç dakika sürebilir.  
9. Sayfayı yenileyin.

## <a name="identify-the-urgent-planned-orders-for-the-item"></a>Madde için acil planlanan siparişleri tanımlama
1. Madde numarası sütunu filtresini açın.
2. "Madde numarası" alanında "ile başlar" filtre işlecini kullanan "D0001" değeriyle filtre uygulayın.
3. Sipariş tarihi sütun filtresini açın.
4. "tam olarak" filtresi işlecini kullanarak, "Sipariş tarihi" alanına bir güncel tarih değeriyle bir filtre uygulayın.

## <a name="firm-all-the-urgent-orders-for-the-item"></a>Madde için tüm acil siparişleri kesinleştirme
1. Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.
2. Kesinleştir öğesine tıklayın.
3. Tamam'a tıklayın.


