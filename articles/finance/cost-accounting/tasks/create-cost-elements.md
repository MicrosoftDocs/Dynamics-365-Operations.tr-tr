---
title: 'Maliyet öğeleri oluşturma  '
description: Maliyet muhasebesinde maliyet öğeleri oluşturmanın birkaç yolu vardır.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cceec1d52e1b5b2a05525c8d96f46dece17363b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187809"
---
# <a name="create-cost-elements"></a>Maliyet öğeleri oluşturma   

[!include [task guide banner](../../includes/task-guide-banner.md)]

Maliyet muhasebesinde maliyet öğeleri oluşturmanın birkaç yolu vardır. Bu yordam ana hesapları bir veri bağlayıcı aracılığıyla içe aktararak maliyet öğeleri oluşturmayı gösterir. Bu yordamı oluşturmak için USMF demo şirketi kullanılmıştır. Bu yordam Dynamics 365 for Operations sürüm 1611 ile eklenen bir Maliyet muhasebesi özelliği içindir.


## <a name="create-new-cost-elements"></a>Yeni maliyet öğeleri oluşturma
1. Maliyet muhasebesi > Boyutlar > Maliyet öğesi boyutları öğesine gidin.
2. Yeni'ye tıklayın.
3. İsim alanına bir değer yazın.
4. Boyut üyeleri için veri bağlayıcı alanına bir değer girin veya bir değer seçin.
5. Açıklama alanına bir değer girin.
6. Kaydet'e tıklayın.

## <a name="configure-the-data-connector"></a>Veri bağlayıcıyı yapılandırma
1. Boyut üyesi sağlayıcısını yapılandır öğesine tıklayın.
2. Hesap planı alanına bir değer girin veya bir değer seçin.
    * Paylaşılan hesap planını kullanmak için Paylaştırılmış öğesini seçin.  
3. Yeni'ye tıklayın.
4. Listede, seçili satırı işaretleyin.
    * Hesaplara ölçütlerinizi karşılayacak filtreler uygulayabilirsiniz.  
5. Aba hesaptan alanına bir değer girin veya bir değer seçin.
6. Ana hesaba alanına bir değer girin veya bir değer seçin.
7. Tamam'a tıklayın.

## <a name="import-main-accounts"></a>Ana hesapları içe aktar
1. Boyut üyelerini içe aktar öğesine tıklayın.
    * Ana hesapları Maliyet muhasebesine aktarılır ve maliyet öğesi olarak kullanılır.  
2. Tamam'a tıklayın.

## <a name="view-the-imported-accounts-as-cost-elements"></a>İçe aktarılan hesapları maliyet öğesi olarak görüntüleme
1. Boyut üyelerini görüntüle öğesine tıklayın.
    * Genel muhasebe hesaplarını işinizde maliyetlerin akış gerçekleştirebileceği maliyet öğeleri olarak görüntüleyin.  

