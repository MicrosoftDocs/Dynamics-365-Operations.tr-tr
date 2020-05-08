---
title: Görüntünün odak noktalarını özelleştirme
description: Bu konuda, Microsoft Dynamics 365 Commerce site oluşturucuda görüntü odak noktalarının nasıl özelleştirileceği açıklanmaktadır.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: af922e857e6bd7a58c0b9891939c8265568b549b
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269533"
---
# <a name="customize-image-focal-points"></a>Görüntünün odak noktalarını özelleştirme

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce site oluşturucuda görüntü odak noktalarının nasıl özelleştirileceği açıklanmaktadır.

## <a name="overview"></a>Özet

Commerce site oluşturucu Ortam Kitaplığına bir görüntü yüklendiğinde, sistem görüntünün odak noktasını belirlemeye çalışır. Örneğin, görüntüde bir kişi varsa, sistem varsayılan olarak odak noktasını kişinin en yüzüne ayarlar. Çoğu durumda, odak noktasını otomatik olarak ayarlama tüm görünüm pencereleri için iyi çalışır, ancak bazen görüntünün belirli bir parçasının her zaman görünür olmasını sağlamak için odak noktasını ayarlamak isteyebilirsiniz.

### <a name="define-a-custom-focal-point-for-an-image"></a>Görüntü için özel bir odak noktası tanımlama

Bir görüntü için özel bir odak noktası tanımlamak üzere aşağıdaki adımları izleyin.

1. Commerce site oluşturucunun sol gezinti bölmesinde, **Ortam Kitaplığı**'nı seçin.
1. Ana pencerede, değiştirmek istediğiniz görüntüyü seçin.
1. Komut çubuğunda, **Düzenle** öğesini seçin.
1. **Düzenleme Modu**'na girmek için görüntüyü seçin.
1. **Düzenleme Modu** altında **Odak Noktasını Değiştir**'i seçin. Görüntünün üzerinde döngüsel bir odak noktası denetimi görünür.
1. İstediğiniz odak noktasının üzerine taşımak için odak noktası denetimini seçin.
1. Bitirdiğinizde, komut çubuğunda, **Kaydet**'i seçin ve sonra **Düzenlemeyi bitir**'i seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Dijital varlık yönetimine genel bakış](dam-overview.md)

[Resimleri karşıya yükleme](dam-upload-images.md)

[Videoyu karşıya yükleme](dam-upload-video.md)

[Dosyaları karşıya yükleme](dam-upload-files.md)

[Görüntüleri kırpma](dam-crop-images.md)
