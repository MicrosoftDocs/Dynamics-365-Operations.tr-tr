---
title: POS'ta ürün önerileri ekleme
description: Bu makalede bir satış noktasında (POS) ürün önerilerinin nasıl kullanılacağı açıklanmaktadır.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 170e2bf18aefc79a796620818c7100ff8e6e689a
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460069"
---
# <a name="add-product-recommendations-on-pos"></a>POS'ta ürün önerileri ekleme

[!include [banner](includes/banner.md)]

Temel olarak ürün önerileri; zengin, çekici ve özel ürün keşfi deneyimleri oluşturmak amacıyla tüm ticari alanlara yayılan, dönüştürülebilir iş uygulamasıdır. Bu özelliği POS'ta uygulamak için [POS cihazlarınıza öneri ekleme](add-recommendations-control-pos-screen.md) başlıklı makaledeki adımları izleyin. 

Ürün önerileri özelliği hakkında daha fazla bilgi edinmek için [ürün önerilerine genel bakış](../commerce/product-recommendations.md) başlıklı makaleyi okuyun. 

## <a name="scenarios"></a>Senaryolar

Ürün önerileri aşağıdaki POS senaryoları için etkinleştirilir. Bulut POS veya Modern POS'da (MPOS) kullanılabilir.

1. **Ürün ayrıntıları** sayfasında:

    - Mağaza çalışanı farklı kanallardan gerçekleştirilen önceki hareketlere bakarken **Ürün ayrıntıları** sayfasını ziyaret ederse öneriler hizmeti, birlikte satın alınabilecek ek maddeleri önerir. Hizmetin eklentilerine bağlı olarak, perakendeciler daha önce satın alma geçmişi olan kullanıcılar için kişiselleştirilmiş önerilere ek olarak, ürünlere yönelik **Benzer görünümleri araştır** ve **Benzer açıklamaları araştır** önerileri gösterebilir.

    [![Ürün ayrıntıları sayfasında öneriler.](./media/proddetails.png)](./media/proddetails.png)

2. **Hareket** sayfasında:

    - Öneri altyapısı, sepetteki sıklıkla birlikte satın alınan tüm maddeler listesine göre madde önerir.

    > [!NOTE]
    > **Hareket** sayfasında önerileri görüntülemek için, perakendecinin Dynamics 365 Commerce'da ekran düzenini güncelleştirmesi gerekir. **Öneriler** denetimi, **Hareket** sayfasına geçirilmelidir.

    [![Hareketler sayfasında öneriler.](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>POS önerilerini etkinleştirmek için Commerce yapılandırma 

Ürün önerilerini ayarlamak için [Ürün önerilerini etkinleştirme](../commerce/enable-product-recommendations.md) bölümündeki adımları izleyerek Commerce ürün önerileri için sağlama işlemini tamamladığınızı onaylayın. Varsayılan olarak, öneriler, sağlama adımları tamamlandıktan ve veriler başarıyla işlendikten sonra hem **Ürün ayrıntıları** sayfasında hem de **Müşteri ayrıntıları** sayfasında görünür. 

## <a name="add-recommendations-to-the-transaction-screen"></a>Hareket ekranına öneriler ekleme

1. Hareket ekranına öneriler eklemek için [Hareket ekranına öneri ekleme](add-recommendations-control-pos-screen.md) bölümündeki adımları izleyin.
1. POS ekran düzeni tasarımcısında yapılan değişiklikleri yansıtmak için Commerce headquarters'da kanal yapılandırma işi **1070**'i çalıştırın.

> [!NOTE] 
> RecoMock virgülle ayrılmış değerler (CSV) dosyasını kullanarak POS önerilerini etkinleştirmek istiyorsanız düzen yöneticisini yapılandırmadan önce CSV dosyasını Microsoft Dynamics Lifecycle Services (LCS) varlık kitaplığına dağıtmanız gerekir. RecoMock CSV dosyasını kullanıyorsanız önerileri etkinleştirmeniz gerekmez. CSV dosyası yalnızca demo amacıyla kullanılabilir. Bir eklenti stok tutma birimi (SKU) satın almak zorunda kalmadan demo amacıyla öneri listelerinin görünümünü taklit etmek isteyen müşteriler veya çözüm mimarları için önerilir.

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün önerilerine genel bakış](product-recommendations.md)

[Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme](enable-adls-environment.md)

[Ürün önerilerini etkinleştir](enable-product-recommendations.md)

[Kişiselleştirilmiş önerileri etkinleştirme](personalized-recommendations.md)

[Kişiselleştirilmiş önerilerden vazgeçme](personalization-gdpr.md)

["Benzer görünümleri araştır" önerilerini etkinleştirme](shop-similar-looks.md)

[Hareket ekranına öneriler ekleme](add-recommendations-control-pos-screen.md)

[AI-ML öneri sonuçlarını ayarlama](modify-product-recommendation-results.md)

[Seçkin önerileri el ile oluşturma](create-editorial-recommendation-lists.md)

[Demo verileriyle öneriler oluşturma](product-recommendations-demo-data.md)

[Ürün önerileri SSS](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
