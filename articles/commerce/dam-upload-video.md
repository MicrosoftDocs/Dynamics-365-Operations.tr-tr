---
title: Videoları karşıya yükleme
description: Bu konuda, Microsoft Dynamics 365 Commerce' site oluşturucuda videoları karşıya yükleme yöntemi açıklanmaktadır.
author: psimolin
ms.date: 06/09/2021
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
ms.openlocfilehash: e3579b54c58898b79c84406480a3b58f541c4621
ms.sourcegitcommit: 257437a57e146496a49782bc8aad179c92fbf6e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/11/2021
ms.locfileid: "6224550"
---
# <a name="upload-videos"></a>Videoları karşıya yükleme

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce' site oluşturucuda videoları karşıya yükleme yöntemi açıklanmaktadır.

Commerce site oluşturucu Ortam Kitaplığı videoları karşıya yüklemenize olanak tanır. Video farklı görünüm pencereleri ve kesme noktaları için otomatik olarak uygun duruma dönüştürüleceğinden her zaman en yüksek bit hızına ve çözünürlüğe sahip video sürümünü yüklemeniz gerekir.

### <a name="video-information-specified-during-upload"></a>Karşıya yükleme sırasında belirtilen video bilgileri

Video karşıya yüklenirken, aşağıdaki bilgiler belirtilebilir.

- **Başlık, Açıklama, Anahtar Sözcükler**: Videonun meta verileri.
- **Açıklamalı alt yazıları otomatik oluştur**: Video için açıklamalı alt yazıların otomatik olarak oluşturulup oluşturulmayacağını belirtir (yalnızca İngilizce dili desteklenir). 
- **Açıklamalı Altyazı**: Kullanılacak açıklamalı alt yazıları belirtir.
- **Normal Ses**: Kullanılacak normal ses parçasını belirtir.
- **Küçük resim**: Videonun küçük resmini belirtir. Belirtilmezse, otomatik olarak oluşturulacaktır.
- **Açıklayıcı Ses**: Kullanılacak açıklayıcı ses parçasını belirtir.

## <a name="upload-a-video"></a>Videoyu karşıya yükleme

Site oluşturucuda bir videoyu karşıya yüklemek için aşağıdaki adımları izleyin.

1. Soldaki gezinti bölmesinde **Medya Kitaplığı**'nı seçin.
1. Komut çubuğunda, **Karşıya yükle \> Medya Öğelerini Karşıya Yükle**'yi seçin.
1. Dosya Gezgini penceresinde, karşıya yüklenecek bir veya daha fazla video dosyasını bulun ve seçin ve ardından **Aç**'ı seçin.
1. **Medya Öğesini Karşıya Yükle** iletişim kutusunda gerekli başlığı ve alt metni girin.
1. İsteğe bağlı açıklama ve anahtar sözcükleri girin ve isterseniz kategoriyi seçin. 
1. Görüntüleri karşıya yükledikten hemen sonra yayımlamak isterseniz, **Karşıya yükleme sonrasında medyayı yayımla** onay kutusunu seçin
1. **Tamam**'ı seçin.

Birden çok varlık türünü aynı anda (örneğin, görüntüler ve videolar) karşıya yüklüyorsanız, **Ortam Öğesini Karşıya Yükle** iletişim kutusunda yalnızca anahtar sözcükler, dosyaların karşıya yüklendikten hemen sonra yayımlanıp yayımlanmayacağı ve video dosyaları için açıklamalı alt yazıların otomatik olarak oluşturulup oluşturulmayacağı belirtilebilir. Tüm varlıklar aynı anahtar sözcükleri paylaşacaktır.

## <a name="additional-resources"></a>Ek kaynaklar

[Dijital varlık yönetimine genel bakış](dam-overview.md)

[Resimleri karşıya yükleme](dam-upload-images.md)

[Dosyaları karşıya yükleme](dam-upload-files.md)

[Resimleri kırpma](dam-crop-images.md)

[Görüntü odak noktalarını özelleştirme](dam-custom-focal-point.md)

[Statik dosyaları karşıya yükleme ve sunma](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
