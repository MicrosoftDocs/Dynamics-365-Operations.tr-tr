---
title: Ürün önerilerini etkinleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce müşterileri için yapay bilgi destek sistemi öğrenme (AI-ML) tabanlı ürün önerilerinin nasıl yapılacağını açıklamaktadır.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770151"
---
# <a name="enable-product-recommendations"></a>Ürün önerilerini etkinleştirme

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce müşterileri için yapay bilgi destek sistemi öğrenme (AI-ML) tabanlı ürün önerilerinin nasıl yapılacağını açıklamaktadır. Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.

## <a name="recommendations-pre-check"></a>Öneriler ön kontrolü
Etkinleştirmeden önce, lütfen ürün önerilerinin yapı 10.0.6 destekleyen ve depolama alanını BDL'yi kullanarak geçirmiş olan F&O müşterileri için desteklendiğini unutmayın. 

Ek olarak, RetailSale ölçümlerinin etkinleştirildiğinden emin olun. Bu ayarla ilgili işlemi hakkında daha fazla bilgi edinmek için [buraya](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures) gidin.


## <a name="turn-on-recommendations"></a>Önerileri açın

Ürün önerilerini açmak için aşağıdaki adımları izleyin.

1. **Perakende** &gt; **ürün önerileri** &gt; **öneri parametrelerine** gidin.
1. Perakende paylaşılan parametreleri listesinde, **öneri listelerini** seçin.
1. **Önerileri etkinleştir** seçeneğini **Evet** olarak ayarlayın.

![Ürün önerilerini etkinleştirme](./media/enableproductrecommendations.png)

> [!NOTE]
> Bu yordam, ürün öneri listeleri oluşturma işlemini başlatır. Dynamics 365 for Commerce'te listelerin kullanılabilmesi ve satış noktasında (POS) görülebilmesi için birkaç saate kadar gerekli olabilir.

## <a name="configure-recommendation-list-parameters"></a>Öneri listesi parametrelerini konfigüre et
Varsayılan olarak, AI-ML tabanlı ürün öneri listesi önerilen değerleri sağlar. Varsayılan önerilen değerleri işinizin akışına uyacak şekilde değiştirebilirsiniz. Varsayılan parametrelerin nasıl değiştirileceği hakkında daha fazla bilgi edinmek için [AI-ML tabanlı ürün öneri sonuçlarınıYönet](modify-product-recommendation-results.md) bölümüne gidin.

## <a name="show-recommendations-on-pos-devices"></a>POS cihazlarındaki önerileri göster
Arka ofisin önerilerini etkinleştirdikten sonra, öneriler panelinin düzenleme aracı ile kontrol POS ekranına eklenmesi gerekir. Bu ayarla ilgili işlemi hakkında daha fazla bilgi edinmek için [buraya](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen) gidin.


## <a name="additional-resources"></a>Ek kaynaklar

[Ürün önerilerine genel bakış](product-recommendations.md)

[Sayfalarına ürün önerileri listesi ekleme](add-reco-list-to-page.md)

[POS cihazlarına öneriler paneli Ekle](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


