---
title: Stok değeri/yaşlandırma raporları ile bunların depolama sürümleri arasındaki işlevsel boşluklar
description: Stok değeri/yaşlandırma raporları ile bunların depolama sürümleri arasındaki işlevsel boşluklar
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f74389648034bf036ce48ac84b3421a8a340f105
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686667"
---
# <a name="functional-gaps-between-inventory-valueaging-reports-and-their-storage-versions"></a>Stok değeri/yaşlandırma raporları ile bunların depolama sürümleri arasındaki işlevsel boşluklar

[Stok yaşlandırma raporu depolama alanı](/dynamics365/supply-chain/cost-management/inventory-aging-report-storage)ve [Stok değeri depolama raporu özellikleri](/dynamics365/supply-chain/cost-management/inventory-value-report-storage), Supply Chain Management'ın büyük miktarda stok hareketi görüntülemesine olanak sağlar. Her durumda, rapor sonuçları, bu raporların depolama dışı sürümlerinden farklı olarak tarama ve dışarı aktarma için kaydedilir. Ancak, bu raporların depolama dışı sürümlerinde bulunan bazı işlevler depolama sürümlerinde yoktur. Aşağıdaki alt bölümler farklılıkları özetler ve geçici çözümler sağlar.

## <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Rapor düzeninde etkinleştirilmiş olsalar bile, depolama raporları alt toplamlar içermez

Sonuç dışarı aktarıldığında, özellikle de kullanıcılar kayıt sırasını değişiyorlarsa alt toplamlar sorunlara neden olabilir.

Alt toplamları denetlemek için sonucu Microsoft Excel'e dışarı aktarabilirsiniz. Alternatif olarak, Supply Chain Management içindeki alt toplamları denetlemek istiyorsanız tüm gruplar için alt toplamı sütuna göre görmek için daha esnek bir yol sağlayan *Yeni kılavuz denetimi* ve *Kılavuzlarda gruplama* özelliklerini etkinleştirmek için [Özellik yönetimi](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)'ni kullanın. Daha fazla bilgi için [Kılavuz özellikleri](/dynamics365/fin-ops-core/fin-ops/get-started/grid-capabilities) bölümüne bakın.

## <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Stok değeri depolama raporu, kayıt defteri hesap bilgilerini desteklemiyor

Stok hesapları bakiyesini almak ve bunu **Stok değeri depolama** raporuyla karşılaştırmak için mizanı çalıştırabilirsiniz.
