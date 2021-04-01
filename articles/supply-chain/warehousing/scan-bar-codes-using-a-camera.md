---
title: Ambar uygulamasında kamera kullanarak barkod okutma
description: Bu konuda, bir mobil cihazdaki kamerayı kullanarak barkodları taramak için ambar uygulamasının nasıl ayarlanacağı açıklanmaktadır.
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 28a49736f43bd2d3bfd4c6856f2f87079a005ba2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239314"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-app"></a>Ambar uygulamasında kamera kullanarak barkod okutma

[!include [banner](../includes/banner.md)]

Bu konuda, bir mobil cihazdaki kamerayı kullanarak barkodları taramak için ambar uygulamasının nasıl ayarlanacağı açıklanmaktadır. 

## <a name="prerequisites"></a>Önkoşullar
Bu özelliği kullanmak için ambar uygulamasının 1.2.0.0 sürümünün yüklü olması ve cihazınızda bir kamera olması gerekir. Güncelleştirmeden sonra uygulamayı açtığınızda, uygulamaya kamerayı kullanma izni vermeniz istenir. Cihazınızda kamera yoksa istem görüntülenmez ve kamerayı tarayıcı olarak kullanamazsınız. 

## <a name="setup"></a>Ayar
Ambar uygulamasının Görüntüleme ayarlarında kameranın barkod taraması için kullanılıp kullanılmayacağını seçebilirsiniz. **Kamerayı tarayıcı olarak kullan**'ı etkinleştirirseniz kamerayı, **Tarama**'ya ayarlanmış tercih edilen giriş moduna sahip her giriş alanında kullanabilirsiniz. 

Giriş alanının taranabilir olup olmadığını denetlemek için **Ambar uygulaması alan adları** sayfasında **Tercih edilen giriş modu**'nu **Tarama** olarak ayarlayın. Bu seçenek belirlendiğinde, ambar uygulamasında tarama yapmak için kamera kullanılabilir. Ambar uygulamasında uygulama alan adlarını yapılandırma hakkında bilgi için bkz. [Ambar uygulamasında uygulama alan adlarını yapılandırma](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

## <a name="supported-bar-code-formats"></a>Desteklenen barkod biçimleri
Kod 128, Kod 39, Kod 93, EAN-8, EAN-13, UPC-E, UPC-A ve QR kodları da dahil olmak üzere en yaygın barkod biçimleri desteklenir. 

## <a name="navigation"></a>Gezinme
Kamera sayfası, giriş alanının Tarama'ya ayarlanmış tercih edilen giriş moduna sahip olduğu her sayfada başlatılır. Kamera sayfasındayken, gezinmek için aşağıdaki seçenekleri kullanın:
- Görev ve ayrıntılar sayfasına dönmek için geri düğmesine tıklayın. 
- Girişi el ile yazabileceğiniz sayfaya gitmek için Görev ve ayrıntılar sayfasındaki kurşun kalem simgesine tıklayın.
- Kamera sayfasına dönmek için Görev ve ayrıntılar sayfasındaki kameraya tıklayın. 

| Görev ve ayrıntılar sayfası | Kamera sayfası | 
| :---------------------: | :--------------------: |
| ![Kamera tarama örnek görevi ayrıntı sayfası](./media/camera-scanning-example-task-detail-page50.png)          | ![Kamera tarama örnek kamera sayfa küçük](./media/camera-scanning-example-camera-page50.png)          |

Kamera sayfasında, Kamera düğmesine tıkladığınızda, barkodu tanımlamaya çalışırken soluk görünür. Barkod 5 saniye içinde tanımlanmazsa işlem zaman aşımına uğrar ve Kamera düğmesi tekrar kullanılabilir olur. Ardından barkodu tekrar taramayı deneyebilirsiniz.

Kamerayı barkoda yönelttiğinizde en iyi sonuca ulaşmak için barkodu köşeli parantez içinde hizalayın. Barkod başarılı bir şekilde tarandığında sonuç işlenir ve bir sonraki adıma geçebilirsiniz. Sonraki adım, Tarama'ya ayarlanmış tercih edilen giriş moduna sahip başka bir giriş alanı içeriyorsa kamera yeniden başlatılır. Sonraki adım tarama alanı değilse kamera sayfası başlatılmaz.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]