---
title: Resimleri karşıya yükleme
description: Bu konuda, Microsoft Dynamics 365 Commerce' site oluşturucuda görüntüleri karşıya yükleme yöntemi açıklanmaktadır.
author: psimolin
manager: annbe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 51571ce221714598b2e2d39c76cb69dcb57cc52b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213806"
---
# <a name="upload-images"></a>Resimleri karşıya yükleme

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce' site oluşturucuda görüntüleri karşıya yükleme yöntemi açıklanmaktadır.

## <a name="overview"></a>Özet

Commerce site oluşturucusu Ortam Kitaplığı, görüntüleri tek tek veya klasörler kullanarak toplu şekilde karşıya yüklemenize olanak tanır. Görüntü yeniden boyutlandırıcı bileşeni, görüntüyü farklı görünüm pencereleri ve kesme noktalarıyla en iyi duruma otomatik olarak getireceğinden her zaman en yüksek çözünürlük ve kaliteye sahip görüntü sürümünü yüklemeniz gerekir.

### <a name="image-information-specified-during-upload"></a>Karşıya yükleme sırasında belirtilen görüntü bilgileri

Görüntü karşıya yüklenirken, aşağıdaki bilgiler belirtilebilir.

- **Başlık, Alt Metin, Açıklama, Anahtar Sözcükler**: Görüntü veya görüntülerin meta verileri. Başlık ve alt metin gerekli değerlerdir.
- **Kategori seç**:
    - **Hiçbiri**: e-Ticaret öykülerinin görüntüsü veya görüntüleri için kullanılır.
    - **Ürün, Kategori, Müşteri, Personel, Katalog**: Dynamics 365 Commerce  çok yönlü kanal görüntüsü veya görüntüleri için kullanılır.
- **Karşıya yükleme sonrasında varlıkları yayımla**: Bu onay kutusu seçildiğinde, görüntü veya görüntüler karşıya yüklemeden hemen sonra yayımlanır.

> [!NOTE]
> Kategori atanan görüntü varlıkları da belirli bir kategorinin varlıklarını aramaya yardımcı olacak şekilde kategori ile otomatik olarak etiketlenir.

### <a name="naming-conventions-for-omni-channel-images"></a>Çok yönlü kanal görüntüleri için adlandırma kuralları 

Ortam Kitaplığını çok yönlü kanal görüntüsü arka ucu olarak yapılandırdıysanız, karşıya yüklenen görüntünün hangi kategoriye ait olduğunu göstermek için görüntü kategorilerini kullanabilirsiniz. Ayrıca, görüntülerin satış noktası (POS) gibi diğer kanallar tarafından doğru şekilde alınmasını sağlamak için izlenmesi gereken bir adlandırma kuralı da vardır.

Varsayılan adlandırma kuralı kategoriye göre değişir:
- Katalog görüntülerinin şu şekilde adlandırılması gerekir: "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"
- Kategori görüntülerinin şu şekilde adlandırılması gerekir: "**/Categories/\{CategoryName\}.png**"
- Müşteri görüntülerinin şu şekilde adlandırılması gerekir: "**/Customers/\{CustomerNumber\}.jpg**"
- Personel görüntülerinin şu şekilde adlandırılması gerekir: "**/Workers/\{WorkerNumber\}.jpg**"
- Ürün görüntülerinin şu şekilde adlandırılması gerekir: "**/Products/\{ProductNumber\}_000_001.png**"
    - 001 görüntünün sırasıdır ve 001, 002, 003, 004 veya 005 olabilir
- Ürün çeşidi görüntülerinin şu şekilde adlandırılması gerekir: "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"

## <a name="upload-an-image"></a>Görüntüyü karşıya yükleme

Site oluşturucuda bir görüntüyü karşıya yüklemek için aşağıdaki adımları izleyin.

1. Soldaki gezinti bölmesinde **Medya Kitaplığı**'nı seçin.
1. Komut çubuğunda, **Karşıya yükle \> Medya Öğelerini Karşıya Yükle**'yi seçin.
1. Dosya Gezgini penceresinde, karşıya yüklenecek bir veya daha fazla resim dosyasını bulun ve seçin ve ardından **Aç**'ı seçin.
1. **Medya Öğesini Karşıya Yükle** iletişim kutusunda gerekli başlığı ve alt metni girin.
1. İsteğe bağlı açıklama ve anahtar sözcükleri girin ve isterseniz kategoriyi seçin. 
1. Görüntüleri karşıya yükledikten hemen sonra yayımlamak isterseniz, **Karşıya yükleme sonrasında medyayı yayımla** onay kutusunu seçin.
1. **Tamam**'ı seçin.

## <a name="upload-a-folder-of-images"></a>Görüntü klasörünü karşıya yükleme

Site oluşturucuda bir görüntü klasörünü toplu olarak karşıya yüklemek için aşağıdaki adımları izleyin.

1. Soldaki gezinti bölmesinde **Medya Kitaplığı**'nı seçin.
1. Komut çubuğunda, **Karşıya yükle \> Klasörü Karşıya Yükle**'yi seçin.
1. Dosya Gezgini penceresinde, karşıya yüklenecek klasörü bulun ve seçin ve ardından **Aç**'ı seçin.
1. **Medya Öğelerini Karşıya Yükle** iletişim kutusunda isteğe bağlı anahtar sözcükleri girin ve isterseniz bir kategori seçin. 
1. Klasördeki görüntüleri karşıya yükledikten hemen sonra yayımlamak isterseniz, **Karşıya yükleme sonrasında medyayı yayımla** onay kutusunu seçin.
1. **Tamam**'ı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Dijital varlık yönetimine genel bakış](dam-overview.md)

[Videoyu karşıya yükleme](dam-upload-video.md)

[Dosyaları karşıya yükleme](dam-upload-files.md)

[Resimleri kırpma](dam-crop-images.md)

[Görüntü odak noktalarını özelleştirme](dam-custom-focal-point.md)

[Statik dosyaları karşıya yükleme ve sunma](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]