---
title: Ürün önerilerini etkinleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce müşterileri için yapay bilgi destek sistemi öğrenme (AI-ML) tabanlı ürün önerilerinin nasıl yapılacağını açıklamaktadır.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
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
ms.openlocfilehash: d8a579be5df3c5e7718a6fb4720341f3bd01a64c
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154425"
---
# <a name="enable-product-recommendations"></a>Ürün önerilerini etkinleştirme

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce müşterileri için yapay bilgi destek sistemi öğrenme (AI-ML) tabanlı ürün önerilerinin nasıl yapılacağını açıklamaktadır. Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.

## <a name="recommendations-pre-check"></a>Öneriler ön kontrolü

Etkinleştirmeden önce, lütfen, ürün önerilerinin, depolama alanını Azure Data Lake Storage (ADLS) kullanarak geçirmiş olan Commerce müşterileri için desteklendiğini unutmayın. 

ADLS'yi etkinleştirme adımları için bkz. [Bir Dynamics 365 ortamında ADLS nasıl etkinleştirilir?](enable-ADLS-environment.md).

Ek olarak, RetailSale ölçümlerinin etkinleştirildiğinden emin olun. Bu ayarla ilgili işlemi hakkında daha fazla bilgi edinmek için [buraya](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures) gidin.


## <a name="turn-on-recommendations"></a>Önerileri açın

Ürün önerilerini açmak için aşağıdaki adımları izleyin.

1. **Retail and Commerce &gt; Ürün önerileri &gt; Öneri parametreleri**'ne gidin.
1. Paylaşılan parametreler listesinde, **Öneri Listeleri**'ni seçin.
1. **Önerileri etkinleştir** seçeneğini **Evet** olarak ayarlayın.

![Ürün önerilerini etkinleştirme](./media/enableproductrecommendations.png)

> [!NOTE]
> Bu yordam, ürün öneri listeleri oluşturma işlemini başlatır. Dynamics 365 Commerce'te listelerin kullanılabilmesi ve satış noktasında (POS) görülebilmesi için birkaç saate kadar gerekli olabilir.

## <a name="configure-recommendation-list-parameters"></a>Öneri listesi parametrelerini konfigüre et

Varsayılan olarak, AI-ML tabanlı ürün öneri listesi önerilen değerleri sağlar. Varsayılan önerilen değerleri işinizin akışına uyacak şekilde değiştirebilirsiniz. Varsayılan parametrelerin nasıl değiştirileceği hakkında daha fazla bilgi edinmek için [AI-ML tabanlı ürün öneri sonuçlarınıYönet](modify-product-recommendation-results.md) bölümüne gidin.

## <a name="show-recommendations-on-pos-devices"></a>POS cihazlarındaki önerileri göster

Commerce arka ofisinde önerileri etkinleştirdikten sonra, öneriler panelinin düzenleme aracını kullanarak kontrol POS ekranına eklenmesi gerekir. Bu işlem hakkında bilgi edinmek için bkz. [POS cihazlarında hareket ekranına öneriler denetimi ekleme](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Kişiselleştirilmiş önerileri etkinleştirme

Kişiselleştirilmiş ürün önerilerinin nasıl alınacağı hakkında daha fazla bilgi için bkz. [Kişiselleştirilmiş önerileri etkinleştirme](personalized-recommendations.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün önerilerine genel bakış](product-recommendations.md)

[Dynamics 365 Commerce ortamında ADLS'yi etkinleştirme](enable-adls-environment.md)

[Kişiselleştirilmiş önerileri etkinleştirme](personalized-recommendations.md)

[Kişiselleştirilmiş önerilerden vazgeçme](personalization-gdpr.md)

[POS'ta ürün önerileri ekleme](product.md)

[Hareket ekranına öneriler ekleme](add-recommendations-control-pos-screen.md)

[AI-ML öneri sonuçlarını ayarlama](modify-product-recommendation-results.md)

[Seçkin önerileri el ile oluşturma](create-editorial-recommendation-lists.md)

[Demo verileriyle öneriler oluşturma](product-recommendations-demo-data.md)

[Ürün önerileri SSS](faq-recommendations.md)

