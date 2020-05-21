---
title: Dynamics 365 Commerce'ta kaldırılan veya artık kullanılmayan özellikler
description: Bu konu Dynamics 365 Commerce'dan kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: josaw
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: c47c5430a8f5d67e13c95db609a95d5ad66933ae
ms.sourcegitcommit: a8b6cd799eddaf5be9aec9ea3c2b55e2c3231652
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2020
ms.locfileid: "3335288"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Dynamics 365 Commerce'ta kaldırılan veya artık kullanılmayan özellikler

[!include [banner](../includes/banner.md)]

Bu konu Dynamics 365 Commerce'dan kaldırılmış veya kaldırılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır. 

> [!NOTE]
> Finance and Operations uygulamlarındai nesneler hakkında ayrıntılı bilgiye [Teknik referans](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep) raporları altından ulaşabilirsiniz. Finance and Operations uygulamalarının her sürümünde değiştirilen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Commerce 10.0.10 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler
### <a name="pos-operation-803---picking-and-receiving"></a>POS işlemi 803 - Malzeme çekme ve teslim alma
|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeni işlem tasarımı nedeniyle, malzeme çekme ve teslim alma işlemleri kullanımdan kaldırıldı. |
| **Başka bir özellikle mi değiştirildi?**   | Evet. Bunun yerine iki yeni POS işlemi sunuldu: gelen işlem (804) ve giden işlem (805).|
| **Etkilenen ürün alanları**         | Satış noktası (POS) uygulaması |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 10.0.10 sürümü itibarıyla, malzeme çekme ve teslim alma işlemi artık yeni özellik güncelleştirmesi almayacak. Gelecekteki sürümlerde bu işlem için yalnızca kritik hata düzeltmeleri yapılacak. Tüm kullanıcıların, uzun dönemli ürün oyl haritasının bir parçası olmaya devam edecek yeni [Gelen işlemler](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) ve [Giden işlemler](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) özelliğine geçiş yapması önerilir. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Commerce 10.0.7 sürümünden kaldırılan veya kullanım dışı bırakılan özellikler
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce GetProductAvailabilities ve GetAvailableInventoryNearby API'ları
|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | GetProductAvailabilities ve GetAvailableInventoryNearby API'larının yerini almak üzere yeni optimize edilmiş API'lar oluşturuldu. |
| **Başka bir özellikle mi değiştirildi?**   | Evet: GetEstimatedAvailabilty ve GetEstimatedProductWarehouseAvailability API'ları ile değiştirildi. |
| **Etkilenen ürün alanları**         | e-Ticaret uygulaması SDK |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 10.0.7 sürümü itibarıyla, GetProductAvailabilities ve GetAvailableInventoryNearby için mühendislik yatırımlar yapılmayacaktır. E-ticaret dağıtımlarında bu API'ları kullanan kuruluşların yeni GetProductAvailabilities ve GetAvailableInventoryNearby API'larına geçiş yapması ve [En iyi duruma getirilmiş ürün kullanılabilirliği hesaplama özelliğini](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels) etkinleştirmesi gerekir.  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Kaldırılmış veya kullanım dışı bırakılmış özellikler hakkındaki önceki duyurular
Önceki sürümlerde kaldırılmış veya kaldırılmış özellikler hakkında daha fazla bilgi edinmek için, [önceki sürümlerdeki kaldırılmış veya kaldırılmış özelliklere](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json) bakın.
