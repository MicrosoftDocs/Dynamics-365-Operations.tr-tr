---
title: Dynamics 365 Commerce'ta kaldırılan veya artık kullanılmayan özellikler
description: Bu konu Dynamics 365 Commerce'dan kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: josaw
ms.date: 01/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: f80d1509c7c363e93b83cb47c1b93ab00bf67180
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193480"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Dynamics 365 Commerce'ta kaldırılan veya artık kullanılmayan özellikler

[!include [banner](../includes/banner.md)]

Bu konu Dynamics 365 Commerce'dan kaldırılmış veya kaldırılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır. 

> [!NOTE]
> Finance and Operations uygulamlarındai nesneler hakkında ayrıntılı bilgiye [Teknik referans](/dynamics/s-e/) raporları altından ulaşabilirsiniz. Finance and Operations uygulamalarının her sürümünde değiştirilen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Commerce 10.0.17 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="full-dataset-generation-interval-is-deprecated"></a>Tam veri kümesi oluşturma aralığı kullanım dışıdır

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu sürümden itibaren, Dynamics 365 Headquarters'daki **Commerce planlayıcı parametreleri** formunda, **Gün cinsinden tam veri kümesi oluşturma aralığı** alanı kullanım dışı olacaktır. Ayrıca, bu sürümden itibaren, değerin düzenlenememesi için alan görsel olarak kaldırılır. Bu, **0** değeri olarak kalır. |
| **Başka bir özellikle mi değiştirildi?**   | No |
| **Etkilenen ürün alanları**         | Dynamics 365 Commerce |
| **Dağıtım seçeneği**              | Tümü|
| **Durum**                         | Kaldırıldı. Bu alanı kullanmayın veya içindeki değeri değiştirmeyin.|

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Commerce 10.0.15 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 için Internet Explorer 11 desteği kullanım dışı bırakılmıştır

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Aralık 2020 itibarıyla geçerli olmak üzere, tüm Dynamics 365 ürünleri için Microsoft Internet Explorer 11 desteği kullanım dışı, bırakılacaktır ve Internet Explorer 11, Ağustos 2021'den sonra desteklenmeyecektir.<br><br>Bu, Internet Explorer 11 arabirimi aracılığıyla kullanılmak üzere tasarlanmış olan Dynamics 365 ürünlerini kullanan müşterileri etkileyecektir. Ağustos 2021'den sonra, Internet Explorer 11, bu tür Dynamics 365 ürünleri için desteklenmeyecektir. |
| **Başka bir özellikle mi değiştirildi?**   | Müşterilerin Microsoft Edge'e geçiş yapması önerilir.|
| **Etkilenen ürün alanları**         | Tüm Dynamics 365 ürünleri |
| **Dağıtım seçeneği**              | Tümü|
| **Durum**                         | Kaldırıldı. Internet Explorer 11 Ağustos 2021'den sonra desteklenmeyecektir.|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Commerce 10.0.11 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler
### <a name="data-action-hooks"></a>Veri eylemi kancaları
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Veri eylemi kancaları özelliği performans sorunları nedeniyle kullanımdan kaldırıldı. |
| **Başka bir özellikle mi değiştirildi?**   | Veri eylem katmanındaki iş mantığını değiştirmek için [veri eylemi geçersiz kılmaları](../e-commerce-extensibility/data-action-overrides.md) kullanmanızı öneririz.|
| **Etkilenen ürün alanları**         | e-Ticaret genişletilebilirliği veri eylemleri |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanımdan kaldırıldı: 10.0.11 sürümü itibarıyla |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Visual Studio 2015 için Retail SDK desteği, msbuild 14.0 ve Retail SDK\Referans kitaplıklar ve araçlar
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Visual Studio 2015 için Retail SDK desteği kullanım dışı bırakıldı ve VS 2017, msbuild 15.0 desteğine güncelleştirildi; RetailSDK\Referanslar klasöründeki tüm referans kitaplıkları ve ticaret ara sunucu oluşturucu araçları uzantı modeli ve SDK yükseltme işlemini kolaylaştırmak için NuGet paketlerine taşındı.|
| **Başka bir özellikle mi değiştirildi?**   | Sisteminizi güncelleştirmek için [Retail SDK'yı Visual Studio 2015'den Visual Studio 2017'ye taşıma](../dev-itpro/retail-sdk/migrate-sdk.md) bölümündeki bilgileri izlemenizi öneririz. |
| **Etkilenen ürün alanları**         | Retail SDK uzantıları |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanımdan kaldırıldı: 10.0.11 sürümü itibarıyla |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>IEdmModelExtender ve CommerceController kullanan Retail Server Uzantısı
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | IEdmModelExtender ve CommerceController kullanan Retail Server uzantısı, daha basşt uzantı modeli sağlamak amacıyla kullanım dışı bırakıldı. Yeni uygulamanın herhangi bir ek IEdmModelExtender sınıfı uygulaması olmadan yalnızca denetleyici sınıfı olacaktır. Bu, ayrıca belirli bir OData sürümüne bağımlılığı önler (OData sürümü güncelleştirilmişse uzantıları kesebilir.) |
| **Başka bir özellikle mi değiştirildi?**   |  NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) paketini içe aktararak IController sınıf uzantısı modelini kullanmanızı öneririz. |
| **Etkilenen ürün alanları**         | Retail server uzantıları |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanımdan kaldırıldı: 10.0.11 sürümü itibarıyla |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>IHardwareStationController kullanan Hardware Station Uzantısı
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | IHardwareStationController kullanan Hardware Station uzantısı daha basit uzantı modeli sağlamak amacıyla kullanım dışı bırakıldı. Yeni uygulamanın, ek sınıf uygulaması olmadan yalnızca IController sınıfı olacaktır ve temel donanım istasyonu kitaplıklarına bağımlılığın engellenmesi amaçlanmıştır; önceki uzantının birden fazla kitaplığa başvurması gerekir.) |
| **Başka bir özellikle mi değiştirildi?**   | NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) paketini içe aktararak IController sınıf uzantısı modelini kullanmanız önerilir. |
| **Etkilenen ürün alanları**         | Hardware Station uzantıları |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanımdan kaldırıldı: 10.0.11 sürümü itibarıyla |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Commerce 10.0.10 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler
### <a name="pos-operation-803---picking-and-receiving"></a>POS işlemi 803 - Malzeme çekme ve teslim alma
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeni işlem tasarımı nedeniyle, malzeme çekme ve teslim alma işlemleri kullanımdan kaldırıldı. |
| **Başka bir özellikle mi değiştirildi?**   | Evet. Bunun yerine iki yeni POS işlemi sunuldu: gelen işlem (804) ve giden işlem (805).|
| **Etkilenen ürün alanları**         | Satış noktası (POS) uygulaması |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 10.0.10 sürümü itibarıyla, malzeme çekme ve teslim alma işlemi artık yeni özellik güncelleştirmesi almayacak. Gelecekteki sürümlerde bu işlem için yalnızca kritik hata düzeltmeleri yapılacak. Tüm kullanıcıların, uzun dönemli ürün oyl haritasının bir parçası olmaya devam edecek yeni [Gelen işlemler](../pos-inbound-inventory-operation.md) ve [Giden işlemler](../pos-outbound-inventory-operation.md) özelliğine geçiş yapması önerilir. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Commerce 10.0.7 sürümünden kaldırılan veya kullanım dışı bırakılan özellikler
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce GetProductAvailabilities ve GetAvailableInventoryNearby API'ları
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | GetProductAvailabilities ve GetAvailableInventoryNearby API'larının yerini almak üzere yeni optimize edilmiş API'lar oluşturuldu. |
| **Başka bir özellikle mi değiştirildi?**   | Evet: GetEstimatedAvailabilty ve GetEstimatedProductWarehouseAvailability API'ları ile değiştirildi. |
| **Etkilenen ürün alanları**         | e-Ticaret uygulaması SDK |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 10.0.7 sürümü itibarıyla, GetProductAvailabilities ve GetAvailableInventoryNearby için mühendislik yatırımlar yapılmayacaktır. E-ticaret dağıtımlarında bu API'ları kullanan kuruluşların yeni GetProductAvailabilities ve GetAvailableInventoryNearby API'larına geçiş yapması ve [En iyi duruma getirilmiş ürün kullanılabilirliği hesaplama özelliğini](../calculated-inventory-retail-channels.md) etkinleştirmesi gerekir.  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Kaldırılmış veya kullanım dışı bırakılmış özellikler hakkındaki önceki duyurular
Önceki sürümlerde kaldırılmış veya kaldırılmış özellikler hakkında daha fazla bilgi edinmek için, [önceki sürümlerdeki kaldırılmış veya kaldırılmış özelliklere](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json) bakın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]