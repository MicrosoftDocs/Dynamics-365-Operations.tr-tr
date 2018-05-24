---
title: "Bir talep tahmin hesaplarken, geçmiş işlem verilerinden aykırı değerleri kaldırın."
description: "Bu makale bir talep tahmini hesaplamak için kullanılan geçmiş verilerden aykırı değerlerin nasıl dışarıda bırakılabileceğini açıklamaktadır. Aykırı değerleri dışarıda bırakarak tahmin doğruluğunu artırabilirsiniz."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b4805d343518a880ad0d6e6568c5493583a17783
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>Bir talep tahmin hesaplarken, geçmiş işlem verilerinden aykırı değerleri kaldırın.

[!include [banner](../includes/banner.md)]

Bu makale bir talep tahmini hesaplamak için kullanılan geçmiş verilerden aykırı değerlerin nasıl dışarıda bırakılabileceğini açıklamaktadır. Aykırı değerleri dışarıda bırakarak tahmin doğruluğunu artırabilirsiniz.

Tahmin doğruluğunu artırmak için aykırı değerleri dışarıda bırakabilirsiniz. Bu isteğe bağlı bir görevdir. İşleme genel bakış:

1.  Dışarıda bırakılacak hareketleri seçmek için bir sorgu kullanabileceğiniz **Aykırı değerleri temizleme** sayfasını açmak için **Master planlama** &gt; **Kurulum** &gt; **Talep tahmini** &gt; **Aykırı değerleri temizle** seçeneğine tıklayın.
2.  Sorgunun uygulandığı şirketi seçin ve sonra isim ve açıklama girin. **Sorgu tarihi** alanı otomatik olarak mevcut tarih olarak ayarlanır.
3.  Sorgunun bulacağı hareketlerden geçmişe dönük verileri çıkarmak için **Etkin** onay kutusunu seçin. Bu ayar, bir temel tahmin oluşturduğunuzda etkin olacaktır.
4.  **Aykırı değer temizleme sorgu** sayfası üzerinde ekleme, kaldırma ve temel tahmini hesaplanırken hangi hareketlerin hariç tutulacağını tanımlayan ölçütü seçin. Örneğin, dışlamak için belirli bir madde veya sipariş hareketini seçin.
5.  **Hareketleri görüntüle**'ye tıklayın. **Aykırı değer hareketleri** sayfası sorguda belirlediğiniz ve talep tahmini hesaplandığında geçmişe dönük verilerden hariç tutulacak kriterlere karşılık gelen hareketleri listeler.

**Not:** Ayrıca varolan bir sorguyu temel alan bir sorgu da oluşturabilirsiniz. Kopyalanacak sorguyu seçin ve sonra **Tekrarlama**'yı tıklatın. **Sorgu tarihi** alanı, sürümü tanımlar. Sorguyu olduğu gibi kullanabilir veya **Sorguyu düzenle**'yi tıklayıp ölçütü değiştirebilirsiniz. İsteğe bağlı olarak, yeni sorgunun adını ve açıklamasını değiştirebilirsiniz.

<a name="additional-resources"></a>Ek kaynaklar
--------

[Talep tahminine giriş](introduction-demand-forecasting.md)

[Tahmin doğruluğunu izleme](monitor-forecast-accuracy.md)




