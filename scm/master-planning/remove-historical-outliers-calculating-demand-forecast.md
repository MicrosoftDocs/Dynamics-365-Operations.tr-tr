---
title: "Bir talep tahmin hesaplarken, geçmiş işlem verilerinden aykırı değerleri kaldırın."
description: "Bu makale bir talep tahmini hesaplamak için kullanılan geçmiş verilerden aykırı değerlerin nasıl dışarıda bırakılabileceğini açıklamaktadır. Aykırı değerleri dışarıda bırakarak tahmin doğruluğunu artırabilirsiniz."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 6f44e1ce566781f1586203528d55b13b28001a2c
ms.lasthandoff: 03/31/2017


---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>Bir talep tahmin hesaplarken, geçmiş işlem verilerinden aykırı değerleri kaldırın.

Bu makale bir talep tahmini hesaplamak için kullanılan geçmiş verilerden aykırı değerlerin nasıl dışarıda bırakılabileceğini açıklamaktadır. Aykırı değerleri dışarıda bırakarak tahmin doğruluğunu artırabilirsiniz.

Tahmin doğruluğunu iyileştirmek için outliers dışlayabilirsiniz. Bu isteğe bağlı bir görevdir. İşleme genel bakış:

1.  ' I **Master planlama**&gt;**Kurulum**&gt;**talep tahmin**&gt;**Outlier Temizleme** açmak için **Outlier Temizleme** sayfası, burada bir sorgu dışlamak için hareketleri seçmek için kullanabilirsiniz.
2.  Sorgunun uygulandığı şirketi seçin ve sonra isim ve açıklama girin. **Sorgu tarihi** alanı otomatik olarak mevcut tarih olarak ayarlanır.
3.  Sorgunun bulacağı hareketlerden geçmişe dönük verileri çıkarmak için **Etkin** onay kutusunu seçin. Bu ayar, bir temel tahmin oluşturduğunuzda etkin olacaktır.
4.  **Aykırı değer temizleme sorgu** sayfası üzerinde ekleme, kaldırma ve temel tahmini hesaplanırken hangi hareketlerin hariç tutulacağını tanımlayan ölçütü seçin. Örneğin, dışlamak için belirli bir madde veya sipariş hareketini seçin.
5.  **Hareketleri görüntüle**'ye tıklayın. **Aykırı değer hareketleri** sayfası sorguda belirlediğiniz ve talep tahmini hesaplandığında geçmişe dönük verilerden hariç tutulacak kriterlere karşılık gelen hareketleri listeler.

**Not:** Ayrıca varolan bir sorguyu temel alan bir sorgu da oluşturabilirsiniz. Kopyalanacak sorguyu seçin ve sonra **Tekrarlama**'yı tıklatın. **Sorgu tarihi** alanı, sürümü tanımlar. Sorguyu olduğu gibi kullanabilir veya **Sorguyu düzenle**'yi tıklayıp ölçütü değiştirebilirsiniz. İsteğe bağlı olarak, yeni sorgunun adını ve açıklamasını değiştirebilirsiniz.

<a name="see-also"></a>Ayrıca bkz.
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)


