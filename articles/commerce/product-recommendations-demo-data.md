---
title: Demo verileriyle öneriler oluşturma
description: Bu konuda, önceden doldurulan ve özelleştirilebilir tanıtım verileri kullanılarak Katman 1 tek taraflı ortamlarda çoklu kanal ürün önerilerinin nasıl kullanılacağına ilişkin kılavuz sunmak amaçlanmıştır.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7ccb0b6c5aace0fc76c6886299fba7369abed860
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972390"
---
# <a name="create-recommendations-with-demo-data"></a>Demo verileriyle öneriler oluşturma

[!include [banner](includes/banner.md)]

Bu konuda, önceden doldurulan ve özelleştirilebilir tanıtım verileri kullanılarak Katman 1 tek taraflı ortamlarda çoklu kanal ürün önerilerinin nasıl kullanılacağına ilişkin kılavuz sunmak amaçlanmıştır.

Çoklu kanal ürün önerilerinde, editör tarafından düzenlenen veya program tarafından oluşturulan bir dizi sipariş edilmiş ürünlerin listesini sunulmaktadır. Bu listeler, iş ihtiyaçlarınıza bağlı olarak birçok senaryoda kullanılabilir. Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.

Katman 2 ve daha yüksek Dynamics 365 Ortamlarında ürün önerileri, müşteri verilerine göre otomatik olarak hesaplanır. Ürün önerileri tanıtım verilerini kullanmak, ortamda zaten sağlanmış olan herhangi bir ürün önerisi çözümünü ve bu çözümün kullanımıyla ilişkili hiçbir maliyeti devre dışı bırakmaz.

Katman 1 ortamlarında ürün önerilerinde yalnızca .csv dosyasında depolanan statik tanıtım verileri esas alınmaktadır.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Bir ortamdaki ürün önerileri tanıtım verilerini etkinleştirme
Ürün örnerileri demo tarhini etkinleştirmek için Müşterilerin Dynamics 365 Commerce Önizleme Tanıtım Uzantısı'nı ilgili ortama dağıtması gerekir. Böylece, ürün önerileri tanıtım verileri otomatik olarak etkinleştirilir.

## <a name="default-demo-data"></a>Varsayılan tanıtım verileri
Her OneBox türü ortamı, virgülle ayrılan Commerce Scale Unit'da bulunan ‘reco_demo_data.csv’ dosyasında depolanan bir dizi önceden yüklenmiş ürün önerileriyle birlikte gelir.

Bu veriler, aşağıdaki sütunlar boyunca yapılandırılmıştır.

| Sütun adı         | Zorunlu          | Tanım                                                                                                                                 | Olası değerler                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Tanıtım veri noktasının oluşturulması gereken özel ürün önerisi listesi türü.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Ürün önerilerinin kullanıma sunulmasının beklendiği özel işletme birimi numarası.                                        |                                                                              |
| Kategori            |                    |    Özel listenin geri döndürülmesi gerektiği kategori. Hiçbir kategori belirtilmezse liste, yalnızca gezinti hiyerarşisinin üst kısmı içindir.    |                                                                              |
| SeedItemId          |                    |    Çekirdek ürünün olması gerektiği listelerde (RecoPeopleAlsoBuy and RecoCart) ek ürünler gösterilmelidir.            |                                                                              |
| CustomerId          |                    |    Müşteri tanımlayıcısı gerektiren listeler için (RecoPicks).  Varsayılan '0' değeri tüm müşteriler için geçerlidir.          |                                                                              |
| ItemIds             | :heavy_check_mark: | Sonuç olarak döndürülmesi gereken ve ‘;’ ile ayrılan bir veya daha fazla ürün.                                                                  |                                                                              |

## <a name="customize-demo-data"></a>Tanıtım verilerini özelleştirme
HQ'da yapılandırılan tüm ürün ve kategori bilgileriyle varsayılan tanıtım verilerini düzenleyebilirsiniz. .CSV'yi güncelleştirdikten sonra değişiklikler müşterilere döndürülen ürün önerilerinde hemen yansıtılır.

Uzantı, sahte öneri sonuçlarını güçlendirmek için kullanılan veri kümesini denetlemenize olanak tanıyan, 'RecoMockDataset.csv' adlı veri dosyasını içerir. Dosya adı, **ext.Recommendations.DemoFilePath** ayarı kullanılarak uzantı yapılandırmasıyla denetlenebilir. Böylece, yapılandırma yoluyla değiştirilebilen mevcut birden fazla veri kümesine sahip olabilirsiniz.


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün önerilerine genel bakış](product-recommendations.md)

[Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme](enable-adls-environment.md)

[Ürün önerilerini etkinleştir](enable-product-recommendations.md)

[Kişiselleştirilmiş önerileri etkinleştirme](personalized-recommendations.md)

[Kişiselleştirilmiş önerilerden vazgeçme](personalization-gdpr.md)

["Benzer görünümleri araştır" önerilerini etkinleştirme](shop-similar-looks.md)

[POS'ta ürün önerileri ekleme](product.md)

[Hareket ekranına öneriler ekleme](add-recommendations-control-pos-screen.md)

[AI-ML öneri sonuçlarını ayarlama](modify-product-recommendation-results.md)

[Seçkin önerileri el ile oluşturma](create-editorial-recommendation-lists.md)

[Ürün önerileri SSS](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]