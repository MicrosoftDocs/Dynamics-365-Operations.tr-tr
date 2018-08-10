---
title: Dynamics 365 for Finance and Operations - Ambarlama'da kamera kullanarak barkod tarama
description: "Bu konuda, bir mobil cihazda kamera kullanarak barkodları taramak için Dynamics 365 for Finance and Operations – Ambarlama'nın nasıl kurulacağı açıklanmıştır."
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7be3e9970e2599c159e7c9d414b54876d0116350
ms.openlocfilehash: f7fe3ab07578b09822fbfeaa4b07331b79f13610
ms.contentlocale: tr-tr
ms.lasthandoff: 03/09/2018

---

# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a>Dynamics 365 for Finance and Operations - Ambarlama'da kamera kullanarak barkod tarama

[!include [banner](../includes/banner.md)]

Bu konuda, bir mobil cihazda kamera kullanarak barkodları taramak için Dynamics 365 for Finance and Operations – Ambarlama'nın nasıl kurulacağı açıklanmıştır. 

## <a name="prerequisites"></a>Ön koşullar
Bu özelliği kullanmak için Ambarlama 1.2.0.0 sürümünün yüklü olması ve cihazınızın bir kameraya sahip olması gerekir. Güncelleştirmeden sonra uygulamayı açtığınızda, Dynamics 365 for Finance and Operations – Ambarlama uygulamasına kamerayı kullanma izni vermeniz istenir. Cihazınızda kamera yoksa istem görüntülenmez ve kamerayı tarayıcı olarak kullanamazsınız. 

## <a name="setup"></a>Ayarlama
Ambarlama uygulamasının Görüntüleme ayarlarında kameranın barkod taraması için kullanılıp kullanılmayacağını seçebilirsiniz. **Kamerayı tarayıcı olarak kullan**'ı etkinleştirirseniz kamerayı, **Tarama**'ya ayarlanmış tercih edilen giriş moduna sahip her giriş alanında kullanabilirsiniz. 

Giriş alanının taranabilir olup olmadığını denetlemek için Dynamics 365 for Finance and Operations'taki **Ambar uygulaması alan adları** sayfasında **Tercih edilen giriş modu**'nu **Tarama** olarak ayarlayın. Bu seçenek belirlendiğinde, Ambarlama uygulamasında tarama yapmak için kamera kullanılabilir. Ambarlama uygulamasında uygulama alan adlarını yapılandırma hakkında bilgi için bkz. [Ambarlama uygulamasında uygulama alan adlarını yapılandırma](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

## <a name="supported-bar-code-formats"></a>Desteklenen barkod biçimleri
Kod 128, Kod 39, Kod 93, EAN-8, EAN-13, UPC-E, UPC-A ve QR kodları da dahil olmak üzere en yaygın barkod biçimleri desteklenir. 

## <a name="navigation"></a>Gezinme
Kamera sayfası, giriş alanının Tarama'ya ayarlanmış tercih edilen giriş moduna sahip olduğu her sayfada başlatılır. Kamera sayfasındayken, gezinmek için aşağıdaki seçenekleri kullanın:
- Görev ve ayrıntılar sayfasına dönmek için geri düğmesine tıklayın. 
- Girişi el ile yazabileceğiniz sayfaya gitmek için Görev ve ayrıntılar sayfasındaki kurşun kalem simgesine tıklayın.
- Kamera sayfasına dönmek için Görev ve ayrıntılar sayfasındaki kameraya tıklayın. 

| Görev ve ayrıntılar sayfası | Kamera sayfası | 
| :---------------------: | :--------------------: |
| ![kamera-tarama-örnek-görev-ayrıntı-sayfa](./media/camera-scanning-example-task-detail-page50.png)          | ![kamera-tarama-örnek-kamera-sayfa-küçük](./media/camera-scanning-example-camera-page50.png)          |

Kamera sayfasında, Kamera düğmesine tıkladığınızda, barkodu tanımlamaya çalışırken soluk görünür. Barkod 5 saniye içinde tanımlanmazsa işlem zaman aşımına uğrar ve Kamera düğmesi tekrar kullanılabilir olur. Ardından barkodu tekrar taramayı deneyebilirsiniz.

Kamerayı barkoda yönelttiğinizde en iyi sonuca ulaşmak için barkodu köşeli parantez içinde hizalayın. Barkod başarılı bir şekilde tarandığında sonuç işlenir ve bir sonraki adıma geçebilirsiniz. Sonraki adım, Tarama'ya ayarlanmış tercih edilen giriş moduna sahip başka bir giriş alanı içeriyorsa kamera yeniden başlatılır. Sonraki adım tarama alanı değilse kamera sayfası başlatılmaz.


