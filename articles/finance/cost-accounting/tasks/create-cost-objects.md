---
title: 'Maliyet nesneleri oluşturma  '
description: Bu yordam maliyet merkezi mali boyutunu bir veri bağlayıcı aracılığıyla Maliyet muhasebesine aktararak maliyet nesneleri oluşturmayı gösterir.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1219cb15ecec7c156579c5cf7c3a3511a141e00b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810066"
---
# <a name="create-cost-objects"></a>Maliyet nesneleri oluşturma   

[!include [banner](../../includes/banner.md)]

Bu yordam maliyet merkezi mali boyutunu bir veri bağlayıcı aracılığıyla Maliyet muhasebesine aktararak maliyet nesneleri oluşturmayı gösterir. Bu yordamı oluşturmak için USMF demo şirketi kullanılmıştır. 


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]