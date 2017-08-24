--- 
title: "Maliyet nesneleri oluşturma  "
description: "Bu yordam , Microsoft Dynamics 365 for Finance and Operations, Enterprise edition maliyet merkezi mali boyutunu bir veri bağlayıcı aracılığıyla Maliyet muhasebesine içe aktararak maliyet nesneleri oluşturmayı gösterir."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 79cb18717c6b42ef0307f304d28902dd66f0f932
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="create-cost-objects"></a>Maliyet nesneleri oluşturma   

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordam , Microsoft Dynamics 365 for Finance and Operations, Enterprise edition maliyet merkezi mali boyutunu bir veri bağlayıcı aracılığıyla Maliyet muhasebesine içe aktararak maliyet nesneleri oluşturmayı gösterir. Bu yordamı oluşturmak için USMF demo şirketi kullanılmıştır. Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir Maliyet muhasebesi özelliği içindir.


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


