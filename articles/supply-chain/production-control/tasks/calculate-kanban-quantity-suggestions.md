---
title: Kanban miktarı önerilerini hesaplama
description: Bu yordam, kanban boyutunu ve miktarlarını belirli bir kanban kuralı için, kanban miktarı hesaplamayı kullanarak en iyi duruma getirme üzerinde odaklanır.
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6769eb1c971b4641aee7cae9dd710a856b3c8fb
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149378"
---
# <a name="calculate-kanban-quantity-suggestions"></a>Kanban miktarı önerilerini hesaplama

[!include [banner](../../includes/banner.md)]

Bu yordam, kanban boyutunu ve miktarlarını belirli bir kanban kuralı için, kanban miktarı hesaplamayı kullanarak en iyi duruma getirme üzerinde odaklanır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu yordam değer akışı yöneticisi için hazırlanmıştır. Yeni bir kanban miktar hesaplama ilkesini bir kanban kuralına ekle yordamını tamamlamış olmanız bir önkoşuldur.


## <a name="create-a-kanban-quantity-calculation"></a>Bir kanban miktar hesaplaması oluşturun
1. Üretim kontrol > Periyodik görevler > Kanban miktarı hesaplama > Kanban miktarı hesapla seçeneğine gidin.
2. Yeni'ye tıklayın.
3. İsim alanına 'Speaker2016' yazın.
4. Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.
    * Kanban kural için yeni bir kanban miktarı hesaplama İlkesi ekle yordamında oluşturduğunuz ilkeyi seçin. Örneğin Speaker2016.  
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Kuralın aktif olacağı tarih alanına tarih ve saati '2012-12-17T08:00:00' olarak yazın.
    * Bu tarih, Kanban miktarı hesaplamasına hangi sabit kanban kurallarının dahil edileceğinin belirlenmesi için temel olarak kullanılır.  
7. Kuralın aktif olacağı tarih alanına tarih ve saati '2012-11-17T09:00:00' yazın.
    * Kanban miktarını hesaplamak için geçmiş talep hareketlerinin dahil edilmeye başlayacağı tarih.  
8. Tamamlanan isteğin dönem bitiş tarihi alanına, tarihi ve saati '2012-12-17T07:59:59' olarak yazın.
    * Kanban miktarını hesaplamak için geçmiş talep hareketlerinin dahil edileceği son tarih.  
9. Talep tarihi başlangıç zamanı alanına, tarihi ve saati '2012-12-17T08:00:00' olarak yazın.
    * Kanban miktarını hesaplamak için geçerli talep hareketlerinin dahil edilmeye başlayacağı tarih.  
10. Talep dönem bitiş tarihi alanına, tarihi ve saati '2013-01-16T07:59:59' olarak yazın.
    * Kanban miktarını hesaplamak için geçerli talep hareketlerinin dahil edileceği son tarih.  

## <a name="generate-kanban-quantity-proposal"></a>Kanban miktarı teklifi oluşturun
1. Kaydet'e tıklayın.
2. Üret'i tıklatın.
    * Bu 000020 kanban kuralı için bir kanban miktar teklif satırı oluşturur.  

## <a name="run-kanban-quantity-calculation"></a>Kanban miktarı hesaplamasını çalıştırın
1. Hesapla'yı tıklatın.
    * Bu kanban miktarı teklifini hesaplar.  
2. Tamam'a tıklayın.
3. Listede, seçili satırı işaretleyin.
    * Önerilen kanban miktarının 2 olduğuna dikkat edin.  

## <a name="change-product-quantity-and-calculate-again"></a>Ürün miktarını değiştirin ve yeniden hesaplayın
1. Toplam ürün miktarını '5'e ayarlayın.
2. Hesapla'yı tıklatın.
3. Tamam'a tıklayın.
    * 5 kanban miktarı ile önerinin 4 kanban miktarına değiştirildiğine dikkat edin.  
    * Daha az ürün miktarıyla, talebini karşılamak için daha fazla kanbana gerek duyuyor olduğumuz gerçeğinden kaynaklanır.  

## <a name="update-kanban-rule"></a>Kanban kuralını güncelleştirin
1. Kural yürürlük tarihi alanına bir tarih ve saat girin.
    * 'Kural tarihi itibariyle etkin' gelecekte bir tarih olarak ayarlayın. Örneğin, bugün + bir yıl.  
2. Güncelleştir'i tıklatın.
3. Tamam'a tıklayın.
4. Sayfayı kapatın.

## <a name="validate-change-on-kanban-rule"></a>Kanban kural değişimini doğrulayın
1. Ürün bilgi yönetimi > Yalın imalat > Kanban kuralları'na gidin.
2. Listede, seçili satırdaki bağlantıya tıklayın.
    * Önceki alt görevinde oluşturulan kanban kuralını seçin. Bu listede, numarasına göre sıralanmış ilk kanban kuralı olmalıdır.  
3. Ayrıntılar bölümünün genişletilmiş görünümüne geçin.
    * Bu tarihe kadar kuralın etkin hale gelmeyeceği anlamına gelen etkin tarihe dikkat edin.  
4. Miktarlar bölümünün genişletilmiş görünümüne geçin.
    * Bunun kanban miktarı hesaplamak için girilen varsayılan miktar olduğuna dikkat edin.  
    * Bu kanban miktar hesaplamasından gelen sabit kanban miktarı olan 4'tür.  
5. ListPanel sekmesini tıklatın.

