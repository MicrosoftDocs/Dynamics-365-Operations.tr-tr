---
title: Görüntünün odak noktalarını özelleştirme
description: Bu makalede, Microsoft Dynamics 365 Commerce site oluşturucuda görüntü odak noktalarının nasıl özelleştirileceği açıklanmaktadır.
author: josaw1
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 13238b7a6e06ea59287230222cda584c7781535e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278583"
---
# <a name="customize-image-focal-points"></a>Görüntünün odak noktalarını özelleştirme

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce site oluşturucuda görüntü odak noktalarının nasıl özelleştirileceği açıklanmaktadır.

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

[Resimleri kırpma](dam-crop-images.md)

[Statik dosyaları karşıya yükleme ve sunma](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
