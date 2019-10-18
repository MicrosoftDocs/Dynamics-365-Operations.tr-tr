---
title: POS'ta ürün önerileri
description: Bu konuda bir satış noktasında (POS) ürün önerilerinin nasıl kullanılacağı açıklanmaktadır.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c78fc1f2f1bb08d01828a8b71ad5d3c16ad31b86
ms.sourcegitcommit: 5b53bdafa5cb9a1279576bfece0452a50383b122
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2019
ms.locfileid: "2278404"
---
# <a name="product-recommendations-on-pos"></a>POS'ta ürün önerileri

[!include [banner](includes/banner.md)]

Temel olarak ürün önerileri; zengin, çekici ve özel ürün keşfi deneyimleri oluşturmak amacıyla tüm perakende alanlara yayılan, dönüştürülebilir iş uygulamasıdır. Bu özelliği POS'ta uygulamak için [POS cihazlarınıza öneri ekleme](add-recommendations-control-pos-screen.md) başlıklı makaledeki adımları izleyin. 

Ürün önerileri özelliği hakkında daha fazla bilgi edinmek için [ürün önerilerine genel bakış](../commerce/product-recommendations.md) başlıklı makaleyi okuyun. 

## <a name="scenarios"></a>Senaryolar

Ürün önerileri aşağıdaki POS senaryoları için etkinleştirilir. Bulut POS veya Modern POS'da (MPOS) kullanılabilir.

1. **Ürün ayrıntıları** sayfasında:

    - • Bir mağaza çalışanı farklı kanallardan gerçekleştirilen önceki hareketlere bakarken **Ürün ayrıntıları** sayfasını ziyaret ederse öneriler hizmeti, birlikte satın alınabilecek ek maddeleri önerir.

    [![Ürün ayrıntıları sayfasında öneriler](./media/proddetails.png)](./media/proddetails.png)

2. **Hareket** sayfasında:

    - • Öneri altyapısı, sepetteki sıklıkla birlikte satın alınan tüm maddeler listesine dayalı olarak madde önerir.

    > [!NOTE]
    > **Hareket** sayfasında önerileri görüntülemek için, perakendecinin Dynamics 365 for Retail'da ekran düzenini güncelleştirmesi gerekir. **Öneriler** denetimi, **Hareket** sayfasına geçirilmelidir.

    [![Hareketler sayfasında öneriler](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-dynamics-365-retail-to-enable-pos-recommendations"></a>POS önerilerini etkinleştirmek için Dynamics 365 Retail yapılandırma

Ürün önerilerini ayarlamak için aşağıdaki adımları izleyin:

1. Hizmetinizin **10.0.6 derlemesine** güncelleştirildiğinden emin olun.
2. İşletmeniz için [ürün önerilerini etkinleştirme](../commerce/enable-product-recommendations.md) yönergelerini izleyin.
3. İsteğe bağlı: Hareket ekranında önerileri görüntülemek için **Ekran düzeni**'ne gidin ekran düzeninizi seçin, **Ekran düzeni tasarımcısı**'nı başlatın ve sonra **öneriler** denetimini gereken yere bırakın.
4. **Perakende parametreleri**'ne gidin, **Makine öğrenimi**'ni seçin, **POS önerilerini etkinleştir** altından **Evet** seçeneğini seçin.
5. Önerileri POS'ta görmek için genel yapılandırma işini **1110** çalıştırın. Yapılan değişiklikleri POS ekran düzeni tasarımcısına yansıtmak için, kanal yapılandırma işini **1070** çalıştırın.



## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Zaten etkinleştirilmiş ürün önerileriyle ilgili sorunları giderme

- **Perakende Parametreleri** \> **Öneri listeleri** \> **Ürün önerilerini devre dışı bırak**'a gidip **Genel yapılandırma işi \[9999\]**'u çalıştırın. 
- **Öneriler denetimini** hareket ekranınıza **Ekran düzeni tasarımcısını** kullanarak eklediyseniz bunu da kaldırın.
- Ek sorularınız varsa daha fazla bilgi edinmek için [Önerilerle ilgili SSS](../commerce/faq-recommendations.md) başlıklı makaleye göz atın.

## <a name="additional-resources"></a>Ek kaynaklar

[Bir POS cihazındaki hareket sayfasına öneriler denetimini ekleme](add-recommendations-control-pos-screen.md)
[Ürün önerilerine genel bakış](../commerce/product-recommendations.md)
[Ürün önerilerini etkinleştirme](../commerce/enable-product-recommendations.md) 