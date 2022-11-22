---
title: 'Maliyet öğeleri oluşturma  '
description: Maliyet muhasebesinde maliyet öğeleri oluşturmanın birkaç yolu vardır.
author: kfend
ms.date: 08/29/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
ms.openlocfilehash: 0254f486816e852bcda52f90fe4da65c413c7032
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779702"
---
# <a name="create-cost-elements"></a>Maliyet öğeleri oluşturma   

[!include [banner](../../includes/banner.md)]

Maliyet muhasebesinde maliyet öğeleri oluşturmanın birkaç yolu vardır. Bu yordam ana hesapları bir veri bağlayıcı aracılığıyla içe aktararak maliyet öğeleri oluşturmayı gösterir. Bu yordamı oluşturmak için USMF demo şirketi kullanılmıştır. Bu yordam Dynamics 365 for Operations sürüm 1611 ile eklenen bir Maliyet muhasebesi özelliği içindir.


## <a name="create-new-cost-elements"></a>Yeni maliyet öğeleri oluşturma
1. **Maliyet muhasebesi > Boyutlar > Maliyet öğesi boyutları**'na gidin.
2. **Yeni**'yi tıklatın.
3. **Ad** alanına bir değer yazın.
4. **Boyut üyeleri için veri bağlayıcı** alanına bir değer girin veya bir değer seçin.
5. **Tanım** alanına bir değer girin.
6. **Kaydet**'e tıklayın.

## <a name="configure-the-data-connector"></a>Veri bağlayıcıyı yapılandırma
1. **Boyut üyesi sağlayıcısını yapılandır** öğesine tıklayın.
2. **Hesap planı** alanına bir değer girin veya bir değer seçin.
    * Paylaşılan hesap planını kullanmak için **Paylaşılan** öğesini seçin.  
3. **Yeni**'yi tıklatın.
4. Listede, seçili satırı işaretleyin.
    * Hesaplara ölçütlerinizi karşılayacak filtreler uygulayabilirsiniz.  
5. **Ana hesaptan** alanına bir değer girin veya bir değer seçin.
6. **Ana hesaba** alanına bir değer girin veya bir değer seçin.
7. **Tamam**'a tıklayın.

## <a name="import-main-accounts"></a>Ana hesapları içe aktar
1. **Boyut üyelerini içe aktar** öğesine tıklayın.
    * Ana hesapları Maliyet muhasebesine aktarılır ve maliyet öğesi olarak kullanılır.  
2. **Tamam**'a tıklayın.

## <a name="view-the-imported-accounts-as-cost-elements"></a>İçe aktarılan hesapları maliyet öğesi olarak görüntüleme
1. **Boyut üyelerini görüntüle** öğesine tıklayın.
    * Genel muhasebe hesaplarını işinizde maliyetlerin akış gerçekleştirebileceği maliyet öğeleri olarak görüntüleyin.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
