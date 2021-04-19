---
title: Ambar Yönetimi mobil uygulamasında kamera kullanarak barkodları tarama
description: Bu konuda, bir mobil cihazdaki kamerayı kullanarak barkodları taramak için Ambar Yönetimi mobil uygulamasının nasıl ayarlanacağı açıklanmaktadır.
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f61f9c45b95b730a7f1743963658ec00abfbb56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831230"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a>Ambar Yönetimi mobil uygulamasında kamera kullanarak barkodları tarama

[!include [banner](../includes/banner.md)]

Bu konuda, bir mobil cihazdaki kamerayı kullanarak barkodları taramak için Ambar Yönetimi mobil uygulamasının nasıl ayarlanacağı açıklanmaktadır.

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