---
title: Warehouse Management mobil uygulamasında kamera kullanarak barkodları tarama
description: Bu makalede, bir mobil cihazdaki kamerayı kullanarak barkodları taramak için Ambar Yönetimi mobil uygulamasının nasıl ayarlanacağı açıklanmaktadır.
author: Mirzaab
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8459ea6912328fa589b92f1731551f56df89c11b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862351"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a>Warehouse Management mobil uygulamasında kamera kullanarak barkodları tarama

[!include [banner](../includes/banner.md)]

Bu makalede, bir mobil cihazdaki kamerayı kullanarak barkodları taramak için Ambar Yönetimi mobil uygulamasının nasıl ayarlanacağı açıklanmaktadır.

## <a name="setup"></a>Ayar

Ambar Yönetimi mobil uygulamasının Görüntüleme ayarlarında kameranın barkod taraması için kullanılıp kullanılmayacağını seçebilirsiniz. **Kamerayı tarayıcı olarak kullan**'ı etkinleştirirseniz kamerayı, **Tarama**'ya ayarlanmış tercih edilen giriş moduna sahip her giriş alanında kullanabilirsiniz.

Giriş alanının taranabilir olup olmadığını denetlemek için **Ambar uygulaması alan adları** sayfasında **Tercih edilen giriş modu**'nu **Tarama** olarak ayarlayın. Bu seçenek belirlendiğinde, Ambar Yönetimi mobil uygulamasında tarama yapmak için kamera kullanılabilir. - Daha fazla bilgi için bkz. [Ambar Yönetimi mobil uygulaması için alanları yapılandırma](configure-app-field-names-priorities-warehouse.md).

## <a name="supported-bar-code-formats"></a>Desteklenen barkod biçimleri

Kod 128, Kod 39, Kod 93, EAN-8, EAN-13, UPC-E, UPC-A ve QR kodları da dahil olmak üzere en yaygın barkod biçimleri desteklenir.

## <a name="navigation"></a>Gezinme

Kamera sayfası, giriş alanının *Tarama*'ya ayarlanmış **tercih edilen giriş moduna** sahip olduğu her sayfada başlatılır. Kamera sayfasındayken, gezinmek için aşağıdaki seçenekleri kullanın:

- **Görev ve ayrıntılar** sayfasına dönmek için geri düğmesini seçin.
- Girişi el ile yazabileceğiniz sayfaya gitmek için **Görev ve ayrıntılar** sayfasındaki kurşun kalem simgesini seçin.
- Kamera sayfasına dönmek için **Görev ve ayrıntılar** sayfasındaki kamerayı seçin.

Kamera sayfasında, Kamera düğmesini seçtiğinizde, barkodu tanımlamaya çalışırken soluk görünür. Barkod 5 saniye içinde tanımlanmazsa işlem zaman aşımına uğrar ve Kamera düğmesi tekrar kullanılabilir olur. Ardından barkodu tekrar taramayı deneyebilirsiniz.

Kamerayı barkoda yönelttiğinizde en iyi sonuca ulaşmak için barkodu köşeli parantez içinde hizalayın. Barkod başarılı bir şekilde tarandığında sonuç işlenir ve bir sonraki adıma geçebilirsiniz. Sonraki adım, Tarama'ya ayarlanmış tercih edilen giriş moduna sahip başka bir giriş alanı içeriyorsa kamera yeniden başlatılır. Sonraki adım tarama alanı değilse kamera sayfası başlatılmaz.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]