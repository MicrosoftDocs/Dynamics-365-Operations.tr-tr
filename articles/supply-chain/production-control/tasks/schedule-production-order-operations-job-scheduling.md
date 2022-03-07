---
title: İşlemler ve iş planlaması olan bir üretim emri planlama
description: Bu konu operasyon planlama ve iş planlama ile bir üretim emri planlamaya odaklanır.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc91fe5aa398cd94e38beea017d6d60ecb44f17e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574389"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>İşlemler ve iş planlaması olan bir üretim emri planlama

[!include [banner](../../includes/banner.md)]

Bu konu operasyon planlama ve iş planlama ile bir üretim emri planlamaya odaklanır. İşler iş planlama ile oluşturulurken, operasyon planlama ile iş oluşturulmaz. Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu yordam üretim müdürü, üretim planlayıcısı veya ayrı bir üretim ortamında çalışan atölye gözetmenine yöneliktir.


## <a name="create-a-production-order"></a>Üretim emri oluşturma
1. Gezinti bölmesinde **Modüller > Üretim denetimi > Üretim emirleri > Tüm üretim emirleri** öğesine gidin.
2. **Yeni üretim emri**'ni seçin.
3. **Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin. Madde numarası **D0001**'i seçin.  
4. **Oluştur**'u seçin.

## <a name="schedule-operations-for-the-production-order"></a>Üretim emri için işlemleri planlama
1. Yeni oluşturulan satırı işaretleyin.      
2. Eylem Bölmesinde, **Planlama** öğesine tıklayın.
3. **Operasyonları planla**'yı seçin.
4. **Planlama yönü** alanında **Planlama tarihinden ileriye doğru** öğesini seçin.
5. **Planlama tarihi** alanına bir tarih girin. Gelecekteki bir tarihi, örneğin bugünden itibaren bir hafta sonrasını seçin. Seçili Planlama yönü ile üretim emri bu tarihten ileriye doğru planlanır.  
6. **Tamam**'ı seçin.
7. Listede, seçili satırı işaretleyin. Durumun **Planlandı** olarak değiştiğine dikkat edin. 
8. **Tüm işler**'i seçin. Operasyon planlaması ile bir iş oluşturulmadığına dikkat edin.  
9. Sayfayı kapatın.

## <a name="schedule-jobs-for-the-production-order"></a>Üretim emri için işleri planlama
1. Eylem Bölmesinde, **Planlama** öğesine tıklayın.
2. **İşleri zamanla**'yı seçin.
3. **Planlama yönü** alanında **Planlama tarihinden ileriye doğru** öğesini seçin.
4. **Planlama tarihi** alanına bir tarih girin. Gelecekteki bir tarihi, örneğin bugünden itibaren bir hafta sonrasını seçin. Seçili Planlama yönü ile üretim emri bu tarihten ileriye doğru planlanır.  
5. **Tamam**'ı seçin.
6. Eylem Bölmesinde **Üretim emri**'ne tıklayın.
7. **Tüm işler**'i seçin. Etkin yola göre, iş planlamasında 5 işin oluşturulduğunda dikkat edin.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]