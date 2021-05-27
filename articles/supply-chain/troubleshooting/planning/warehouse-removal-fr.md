---
title: Tahmin satırlarından Ambar talebi tahmin boyutunu kaldıramazsınız
description: Tahmin satırlarından Ambar talebi tahmin boyutunu kaldıramazsınız.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026986"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a>Tahmin satırlarından Ambar talebi tahmin boyutunu kaldıramazsınız

KB numarası: 4614408

## <a name="symptoms"></a>Belirtiler

Bu sorun, **Talep tahmin parametresi** sayfasının **Tahmin boyutları** sekmesinde **Ambar** boyutu atanmamışsa oluşur. Bununla birlikte, **Ambar** sütunu **Talep tahmin** sayfasında gösterilir (**Master planlama \> Tahmin \>El ile tahmin varlığı \> Talep tahmin satırları**).

## <a name="resolution"></a>Çözünürlük

**Talep tahmin parametresi** sayfasının **Tahmin boyutları** sekmesindeki ayarlar, **Talep tahmin** sayfasını etkilemez. Oluşturulan ve düzeltilmiş talep tahmininde gösterilen temel tahmini denetler. Ancak, "gerçek" talep tahmini için gerekli olan boyutları denetmezler. **Düzeltilmiş talep tahmin** sayfasında gösterilen kayıtları yetkilendirerek, tahmin modeli için bunları "gerçek" tahmin girişlerine dönüştürebilirsiniz. Bu model, daha sonra master planlama için kullanılabilir.

**Talep tahmin** sayfasında, talep tahmin satırlarında gösterilen "gerçek" tahminin boyutları stok boyutlarının bir parçasıdır. (Bu davranış satış siparişi satırlarının davranışına benzer.) Sisteminiz zorunlu stok boyutunda **Ambar** seçeneğini zorunlu olarak kullanacak şekilde ayarlanmamışsa sütunu gizlemek için sayfayı özelleştirebilirsiniz.
