---
title: Tanımlama bilgisi izin modülü
description: Bu makale tanımlama bilgisi izin modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 514f54ea6ff05dc3e0885f21af176453dd604848
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878607"
---
# <a name="cookie-consent-module"></a>Tanımlama bilgisi izin modülü

[!include [banner](includes/banner.md)]

Bu makale tanımlama bilgisi izin modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

Tanımlama bilgisi izin modülü, site kullanıcılarının, tarayıcı tanımlama bilgilerini izleyen herhangi bir özellik veya modülle ilgili tanımlama bilgilerine izin vermek için açıkça onay sağlamasını ister. Bir site kullanıcısı yeni bir tarayıcı oturumunda siteye ilk kez göz attığında izin gereklidir. İzin alındığında, izlenir ve site kullanıcısına yeniden izin sorulmaz. Daha fazla bilgi için bkz. [Tanımlama bilgisi uyumluluğu](cookie-compliance.md).

Site kullanıcısından tanımlama bilgisi izni alınmazsa, tanımlama bilgisi izni gerektiren tüm özellikler veya modüller sayfada işlenmez. Örneğin, ödeme modülü, sosyal içerik paylaşım modülü ve tercih edilen mağaza özelliklerinin hepsi tanımlama bilgisi izni gerektirir ve site kullanıcısının izni alınmazsa işlenmez. 

Bir tanımlama bilgisi izin modülü, sayfa yüklenirken uygulanabilmesi için bir sayfanın başlık bölümünden yapılandırılabilir. Tanımlama bilgisi izin modülü, site kullanıcısına sitedeki tanımlama bilgisi kullanımına ilişkin bilgi veren açık bir iletiye sahip olmalıdır ve sitenin gizlilik sayfasına bir bağlantı sağlamalıdır.

Aşağıdaki resimde, site sayfası üstbilgisinde görüntülenen sitenin gizlilik ilkesi sayfasına verilen bir bağlantı bulunan tanımlama bilgisi izin iletisi örneği gösterilmiştir.
![Tanımlama bilgisi izin modülü örneği.](./media/ecommerce-cookieconsent.png)

## <a name="cookie-consent-module-properties"></a>Tanımlama bilgisi izin modülünün özellikleri

| Özellik adı             | Değer                 | Tanım |
|---------------------------|-----------------------|-------------|
| Zengin Metin                  | Zengin Metin | Site kullanıcılarına sitenin tarayıcı tanımlama bilgileri kullandığı ve kullanıcıların tüm işlevlere erişmesi için tanımlama bilgisi kullanımını kabul etmelerini gerektiren zengin metin bildirimi gösterir. |
| Bağlantılar | URL | Sitenin gizlilik sayfasına, sitede izlenen tanımlama bilgilerinin türlerini açıklayan bir veya daha fazla bağlantı eklenebilir. |

## <a name="add-a-cookie-consent-module-to-site-pages"></a>Site sayfalarına tanımlama bilgisi izin modülü ekleme

Birden çok site sayfasına bir tanımlama bilgisi izin modülünü etkili şekilde eklemek için, paylaşılan sayfa üstbilgi parçasına eklenebilir. Üstbilgi parçası tüm site sayfalarına eklendikten sonra, bir site kullanıcısı herhangi bir site sayfasına ilk kez gittiğinde otomatik olarak bir tanımlama bilgisi izin bildirimi oluşturulur.

Üstbilgi parçaları ve modüller hakkında daha fazla bilgi için bkz. [Üstbilgi modülleri](author-header-module.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Üst bilgi modülü](author-header-module.md) 

[Tanımlama bilgisi uyumluluğu](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]