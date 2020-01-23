---
title: Çoklu kanal ürün önerileri tanıtım verileri
description: Bu belgeyle önceden doldurulan, ve özelleştirilebilir tanıtım verileri kullanılarak Katman 1 tek taraflı ortamlarda çoklu kanal ürün önerilerinin nasıl kullanılacağına ilişkin kılavuz sunmak amaçlanmıştır.
author: bebeale
manager: AnnBe
ms.date: 12/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 31aa5dbd2fa814fd572024a4ae36b9d9b46a2fb0
ms.sourcegitcommit: 398c0652acde12c953de007d06055456d6e0a516
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/02/2019
ms.locfileid: "2872338"
---
# <a name="omni-channel-product-recommendations-demo-data"></a>Çoklu kanal ürün önerileri tanıtım verileri

Bu belgeyle önceden doldurulan, ve özelleştirilebilir tanıtım verileri kullanılarak Katman 1 tek taraflı ortamlarda çoklu kanal ürün önerilerinin nasıl kullanılacağına ilişkin kılavuz sunmak amaçlanmıştır.

Çoklu kanal ürün önerilerinde, editör tarafından düzenlenen veya program tarafından oluşturulan bir dizi sipariş edilmiş ürünlerin listesini sunulmaktadır. Bu listeler, iş ihtiyaçlarınıza bağlı olarak birçok senaryoda kullanılabilir. Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](../commerce/product-recommendations.md) başlıklı makaleye bakın.

Katman 2 ve daha yüksek Dynamics Ortamlarında ürün önerileri, müşteri verilerine göre otomatik olarak hesaplanır.
Ürün önerileri tanıtım verilerini kullanmak, ortamda zaten sağlanmış olan herhangi bir ürün önerisi çözümünü ve bu çözümün kullanımıyla ilişkili hiçbir maliyeti devre dışı bırakmaz.

Katman 1 ortamlarında ürün önerilerinde yalnızca .csv dosyasında depolanan statik tanıtım verileri esas alınmaktadır.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Bir ortamdaki ürün önerileri tanıtım verilerini etkinleştirme

Müşterilerin **Dynamics 365 Commerce Önizleme Tanıtım Uzantısı**'nı ilgili ortama dağıtması gerekir. Böylece, ürün önerileri tanıtım verileri otomatik olarak etkinleştirilir.

## <a name="default-demo-data"></a>Varsayılan tanıtım verileri
Her bir Onebox türü ortamı, virgülle ayrılan **‘reco_demo_data.csv’** dosyasında depolanan bir dizi önceden yüklenmiş ürün önerileriyle birlikte gelir ve Retail Server'da bu belgeyle aynı klasörde bulunur.

Bu veriler, aşağıdaki sütunlar boyunca yapılandırılmıştır

| Sütun adı         | Zorunlu          | Tanım                                                                                                                                 | Olası Değerler                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Tanıtım veri noktasının oluşturulması gereken özel ürün önerisi listesi türü.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Ürün önerilerinin kullanıma sunulmasının beklendiği özel işletme birimi numarası.                                        |                                                                              |
| Kategori            |                    |    Özel listenin geri döndürülmesi gerektiği kategori. Hiçbir kategori belirtilmezse liste, yalnızca gezinti hiyerarşisinin üst kısmı içindir.    |                                                                              |
| SeedItemId          |                    |    Çekirdek ürünün olması gerektiği listelerde (RecoPeopleAlsoBuy and RecoCart) ek ürünler gösterilmelidir.            |                                                                              |
| ItemIds             | :heavy_check_mark: | Sonuç olarak döndürülmesi gereken ve **‘;’** ile ayrılan bir veya daha fazla ürün.                                                                  |                                                                              |


## <a name="customize-demo-data"></a>Tanıtım verilerini özelleştirme
Müşteriler, HQ'da yapılandırılan tüm ürün ve kategori bilgileriyle varsayılan tanıtım verilerini düzenleyebilirler. CSV güncelleştirildikten sonra müşterilere döndürülen Ürün Önerilerinde değişiklikler hemen yansıtılır.

Uzantı, müşterinin sahte öneri sonuçlarını güçlendirmek için kullanılan veri kümesini denetlemesine olanak tanıyan, "RecoMockDataset.csv" adlı veri dosyasını içerir. Dosya adı, **ext.Recommendations.DemoFilePath** ayarı kullanılarak uzantı yapılandırmasıyla denetlenebilir. Böylece müşteriler, yapılandırma yoluyla değiştirilebilen mevcut birden fazla veri kümesine sahip olabilirler.

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün önerilerine genel bakış](../commerce/product-recommendations.md)

[Ortam planlama](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
