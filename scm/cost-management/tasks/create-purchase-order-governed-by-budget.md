--- 
title: "Bütçeyle yönetilen bir satınalma siparişi oluşturma"
description: "Bu yordamı, kullanılabilir bütçeye karşı denetleyen bir satınalma siparişi oluşturmak için kullanın."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: f9b82db94d98fb19c67888a1f8a35b2fe62c98fe
ms.contentlocale: tr-tr
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-purchase-order-governed-by-budget"></a>Bütçeyle yönetilen bir satınalma siparişi oluşturma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordamı, kullanılabilir bütçeye karşı denetleyen bir satınalma siparişi oluşturmak için kullanın. Bu kayıt USMF demo veri şirketini kullanır.


## <a name="review-the-budget-control-configuration"></a>Bütçe kontrol konfigürasyonunu gözden geçirin
1. Bütçeleme > Kurulum > Bütçe kontrolü > Bütçe kontrol yapılandırması'na gidin.
2. Kullanılabilir bütçe fonları sekmesine tıklayın.
3. Belgeler ve günlükler sekmesine tıklayın.
4. Bütçe kontrol kuralları sekmesini tıklayın.
5. Bütçe grupları sekmesini tıklayın.
6. Sayfayı kapatın.

## <a name="create-the-purchase-order-header"></a>Satınalma siparişi başlığını oluşturun
1. Tedarik ve kaynak atama > Sipariş emirleri > Tüm sipariş emirleri öğesine gidin.
2. Yeni'ye tıklayın.
3. Satıcı hesabı alanında bir değer girin veya bir değer seçin.
4. Genel bölümünü genişletin.
5. Muhasebe tarih alanında, tarihi '2016-01-01' olarak ayarlayın.
6. Tamam'a tıklayın.

## <a name="add-a-purchase-order-line"></a>Bir satınalma siparişi satırı ekleyin
1. Satın alma kategorisi alanına bir değer girin veya buradan bir değer seçin.
2. Miktarı '2' olacak şekilde ayarlayın.
3. Birim alanına bir değer girin veya buradan bir değer seçin.
4. Birim fiyatını '10000' olarak ayarlayın.
5. Finansal öğeler'e tıklayın.
6. Dağıtım tutarlarını'nı tıklatın.
7. Genel muhasebe defteri hesabı alanında, '601300-001-023--' değerini belirtin.
8. Sayfayı kapatın.

## <a name="perform-budget-checking"></a>Bütçe kontrolü gerçekleştir
1. Finansal öğeler'e tıklayın.
2. Bütçe kontrolü gerçekleştir üzerine tıklayın.
3. Finansal öğeler'e tıklayın.
4. Bütçe denetim hataları veya uyarılarını görüntüleyin.
5. Kapat’a tıklayın.


