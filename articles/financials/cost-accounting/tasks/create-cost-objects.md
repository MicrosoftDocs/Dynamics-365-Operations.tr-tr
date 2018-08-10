--- 
title: "Maliyet nesneleri oluşturma  "
description: "Bu yordam, Microsoft Dynamics 365 for Finance and Operations maliyet merkezi mali boyutunu bir veri bağlayıcı aracılığıyla Maliyet muhasebesine içe aktararak maliyet nesneleri oluşturmayı gösterir."
author: ShylaThompson
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 21fa90557b665e0777935cc6bae8cd9f1c29cb60
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---
# <a name="create-cost-objects"></a>Maliyet nesneleri oluşturma   

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, Microsoft Dynamics 365 for Finance and Operations maliyet merkezi mali boyutunu bir veri bağlayıcı aracılığıyla Maliyet muhasebesine içe aktararak maliyet nesneleri oluşturmayı gösterir. Bu yordamı oluşturmak için USMF demo şirketi kullanılmıştır. Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir Maliyet muhasebesi özelliği içindir.


## <a name="create-new-cost-objects"></a>Yeni maliyet nesneleri oluşturma
1. Maliyet muhasebesi > Boyutlar > Maliyet nesnesi boyutları öğesine gidin.
2. Yeni'ye tıklayın.
3. İsim alanına bir değer yazın.
4. Boyut üyeleri için veri bağlayıcı alanına bir değer girin veya bir değer seçin.
5. Açıklama alanına bir değer girin.
6. Kaydet'e tıklayın.

## <a name="configure-the-data-connector"></a>Veri bağlayıcıyı yapılandırma
1. Boyut üyesi sağlayıcısını yapılandır öğesine tıklayın.
    * CostCenter boyutunu Maliyet muhasebesine aktarmak için CostCenter öğesini seçin.  
2. Boyut adı alanında, Maliyet merkezi öğesini seçin.
3. Tamam'a tıklayın.

## <a name="import-cost-centers"></a>Maliyet merkezlerini içe aktarma
1. Boyut üyelerini içe aktar öğesine tıklayın.
2. Tamam'a tıklayın.

## <a name="view-the-imported-cost-centers"></a>İçe aktarılan maliyet merkezlerini görüntüleme
1. Boyut üyelerini görüntüle öğesine tıklayın.


