---
title: Resimleri karşıya yükleme
description: Bu konuda, Microsoft Dynamics 365 Commerce' site oluşturucuda görüntüleri karşıya yükleme yöntemi açıklanmaktadır.
author: psimolin
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a5607fa70f5d5d28d10bcbd50da11bb96cbf75de
ms.sourcegitcommit: 8592c661b41f9cef8b7ef2863a3b97bf49a4e6f9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/26/2021
ms.locfileid: "7423267"
---
# <a name="upload-images"></a>Resimleri karşıya yükleme

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce' site oluşturucuda görüntüleri karşıya yükleme yöntemi açıklanmaktadır.

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
- Ürün görüntülerinin şu şekilde adlandırılması gerekir: "**/Products/\{ProductNumber\}\_000_001.png**"
    - 001 görüntünün sırasıdır ve 001, 002, 003, 004 veya 005 olabilir
- Ürün çeşidi görüntülerinin şu şekilde adlandırılması gerekir: "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"
    - Örnek: 93039 \^ &nbsp;\^ 2 \^ Siyah \^\_000_001.png
- Yapılandırma boyutu bulunan ürün çeşidi görüntülerinin şu şekilde adlandırılması gerekir: "**/Products/\{ProductNumber\} \^ \{Configuration\}\_000_001.png**"
    - Örnek: 93039 \^ LB8017_000_001.png

> [!NOTE]
> Ürün çeşidi görüntüleri için boyut değeri boşsa dosya adındaki şapka işaretleri arasında iki boşluk olmalıdır.

Yukarıdaki örneklerde varsayılan yapılandırma kullanılır. Ayırıcı karakteri ve boyutlar yapılandırılabilir ve gerekli tam adlandırma, dağıtımlar arasında değişiklik gösterebilir. Gerekli tam adlandırma kuralını belirlemenin bir yöntemi, mağaza ürün ayrıntıları sayfasındaki (PDP) ürün boyutlarını değiştirirken ürün çeşidi görüntüsü isteklerini incelemek için tarayıcının geliştirici konsolunu kullanmaktır.

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
