---
title: 'Maliyet öğeleri oluşturma  '
description: Maliyet muhasebesinde maliyet öğeleri oluşturmanın birkaç yolu vardır.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c4c1e2aee7ba98c1cca378286afb643eaca1600
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810090"
---
# <a name="create-cost-elements"></a>Maliyet öğeleri oluşturma   

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]