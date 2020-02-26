---
title: Tanıtım verilerini kullanarak ürün önerileri edinme
description: Bu belgeyle önceden doldurulan, ve özelleştirilebilir tanıtım verileri kullanılarak Katman 1 tek taraflı ortamlarda çoklu kanal ürün önerilerinin nasıl kullanılacağına ilişkin kılavuz sunmak amaçlanmıştır.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6abac72b7530dc7b82c8e95faebdce791cf7dbd1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003246"
---
# <a name="get-product-recommendations-using-demo-data"></a>Tanıtım verilerini kullanarak ürün önerileri edinme
Bu belgeyle önceden doldurulan, ve özelleştirilebilir tanıtım verileri kullanılarak Katman 1 tek taraflı ortamlarda çoklu kanal ürün önerilerinin nasıl kullanılacağına ilişkin kılavuz sunmak amaçlanmıştır.

Çoklu kanal ürün önerilerinde, editör tarafından düzenlenen veya program tarafından oluşturulan bir dizi sipariş edilmiş ürünlerin listesini sunulmaktadır. Bu listeler, iş ihtiyaçlarınıza bağlı olarak birçok senaryoda kullanılabilir. Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.

Katman 2 ve daha yüksek Dynamics 365 Ortamlarında ürün önerileri, müşteri verilerine göre otomatik olarak hesaplanır. Ürün önerileri tanıtım verilerini kullanmak, ortamda zaten sağlanmış olan herhangi bir ürün önerisi çözümünü ve bu çözümün kullanımıyla ilişkili hiçbir maliyeti devre dışı bırakmaz.

Katman 1 ortamlarında ürün önerilerinde yalnızca .csv dosyasında depolanan statik tanıtım verileri esas alınmaktadır.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Bir ortamdaki ürün önerileri tanıtım verilerini etkinleştirme
Ürün örnerileri demo tarhini etkinleştirmek için Müşterilerin Dynamics 365 Commerce Önizleme Tanıtım Uzantısı'nı ilgili ortama dağıtması gerekir. Böylece, ürün önerileri tanıtım verileri otomatik olarak etkinleştirilir.

## <a name="default-demo-data"></a>Varsayılan tanıtım verileri
Her bir Onebox türü ortamı, virgülle ayrılan Commerce Scale Unit'da bulunan ‘reco_demo_data.csv’ dosyasında depolanan bir dizi önceden yüklenmiş ürün önerileriyle birlikte gelir.

Bu veriler, aşağıdaki sütunlar boyunca yapılandırılmıştır.

| Sütun adı         | Zorunlu          | Tanım                                                                                                                                 | Olası Değerler                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Tanıtım veri noktasının oluşturulması gereken özel ürün önerisi listesi türü.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Ürün önerilerinin kullanıma sunulmasının beklendiği özel işletme birimi numarası.                                        |                                                                              |
| Kategori            |                    |    Özel listenin geri döndürülmesi gerektiği kategori. Hiçbir kategori belirtilmezse liste, yalnızca gezinti hiyerarşisinin üst kısmı içindir.    |                                                                              |
| SeedItemId          |                    |    Çekirdek ürünün olması gerektiği listelerde (RecoPeopleAlsoBuy and RecoCart) ek ürünler gösterilmelidir.            |                                                                              |
| ItemIds             | :heavy_check_mark: | Sonuç olarak döndürülmesi gereken ve ‘;’ ile ayrılan bir veya daha fazla ürün.                                                                  |                                                                              |

## <a name="customize-demo-data"></a>Tanıtım verilerini özelleştirme
HQ'da yapılandırılan tüm ürün ve kategori bilgileriyle varsayılan tanıtım verilerini düzenleyebilirsiniz. .CSV'yi güncelleştirdiğinizde sonra müşterilere döndürülen Ürün Önerilerinde değişiklikler hemen yansıtılır.

Uzantı, sahte öneri sonuçlarını güçlendirmek için kullanılan veri kümesini denetlemenize olanak tanıyan, "RecoMockDataset.csv" adlı veri dosyasını içerir. Dosya adı, **ext.Recommendations.DemoFilePath** ayarı kullanılarak uzantı yapılandırmasıyla denetlenebilir. Böylece, yapılandırma yoluyla değiştirilebilen mevcut birden fazla veri kümesine sahip olabilirsiniz.


```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün önerilerine genel bakış](product-recommendations.md)

[Ortam planlama](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
