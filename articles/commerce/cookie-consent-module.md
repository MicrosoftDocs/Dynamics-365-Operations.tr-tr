---
title: Tanımlama bilgisi izin modülü
description: Bu konu tanımlama bilgisi izin modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 842096c6e3045e434aced9642c86690e2ff7483a
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761432"
---
# <a name="cookie-consent-module"></a>Tanımlama bilgisi izin modülü

[!include [banner](includes/banner.md)]

Bu konu tanımlama bilgisi izin modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel bakış

Tanımlama bilgisi izin modülü, site kullanıcılarının, tarayıcı tanımlama bilgilerini izleyen herhangi bir özellik veya modülle ilgili tanımlama bilgilerine izin vermek için açıkça onay sağlamasını ister. Bir site kullanıcısı yeni bir tarayıcı oturumunda siteye ilk kez göz attığında izin gereklidir. İzin alındığında, izlenir ve site kullanıcısına yeniden izin sorulmaz. Daha fazla bilgi için bkz. [Tanımlama bilgisi uyumluluğu](cookie-compliance.md).

Site kullanıcısından tanımlama bilgisi izni alınmazsa, tanımlama bilgisi izni gerektiren tüm özellikler veya modüller sayfada işlenmez. Örneğin, ödeme modülü, sosyal içerik paylaşım modülü ve tercih edilen mağaza özelliklerinin hepsi tanımlama bilgisi izni gerektirir ve site kullanıcısının izni alınmazsa işlenmez. 

Bir tanımlama bilgisi izin modülü, sayfa yüklenirken uygulanabilmesi için bir sayfanın başlık bölümünden yapılandırılabilir. Tanımlama bilgisi izin modülü, site kullanıcısına sitedeki tanımlama bilgisi kullanımına ilişkin bilgi veren açık bir iletiye sahip olmalıdır ve sitenin gizlilik sayfasına bir bağlantı sağlamalıdır.

Aşağıdaki resimde, site sayfası üstbilgisinde görüntülenen sitenin gizlilik ilkesi sayfasına verilen bir bağlantı bulunan tanımlama bilgisi izin iletisi örneği gösterilmiştir.
![Tanımlama bilgisi izin modülü örneği](./media/ecommerce-cookieconsent.png)

## <a name="cookie-consent-module-properties"></a>Tanımlama bilgisi izin modülünün özellikleri

| Özellik adı             | Değer                 | Tanım |
|---------------------------|-----------------------|-------------|
| Zengin Metin                  | Zengin Metin | Site kullanıcılarına sitenin tarayıcı tanımlama bilgileri kullandığı ve kullanıcıların tüm işlevlere erişmesi için tanımlama bilgisi kullanımını kabul etmelerini gerektiren zengin metin bildirimi gösterir. |
| Bağlantılar | URL | Sitenin gizlilik sayfasına, sitede izlenen tanımlama bilgilerinin türlerini açıklayan bir veya daha fazla bağlantı eklenebilir. |

## <a name="add-a-cookie-consent-module-to-site-pages"></a>Site sayfalarına tanımlama bilgisi izin modülü ekleme

Birden çok site sayfasına bir tanımlama bilgisi izin modülünü etkili şekilde eklemek için, paylaşılan sayfa üstbilgi parçasına eklenebilir. Üstbilgi parçası tüm site sayfalarına eklendikten sonra, bir site kullanıcısı herhangi bir site sayfasına ilk kez gittiğinde otomatik olarak bir tanımlama bilgisi izin bildirimi oluşturulur.

Üstbilgi parçaları ve modüller hakkında daha fazla bilgi için bkz. [Üstbilgi modülleri](author-header-module.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Üst bilgi modülü](author-header-module.md) 

[Tanımlama bilgisi uyumluluğu](cookie-compliance.md)
