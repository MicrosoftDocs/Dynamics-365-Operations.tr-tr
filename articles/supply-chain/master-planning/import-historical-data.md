---
title: Talep tahminleri için geçmiş verisini içe aktar
description: Doğru talep tahminleri elde etmek için madde veya madde tahsisat anahtarı başına tarihsel talep verisine ihtiyaç duyarsınız. Bu konu herhangi bir sistemden geçmiş verisini almak için veri varlıklarının nasıl kullanılacağını ve böylece daha uzun talep tahmin verisine nasıl sahip olacağınızı açıklar.
author: roxanadiaconu
manager: tfehr
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c66481b1dd8650960cad2947425c1e6c7450afcb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439539"
---
# <a name="import-historical-data-for-demand-forecasts"></a>Talep tahminleri için geçmiş verisini içe aktar

[!include [banner](../includes/banner.md)]

Talep tahminlerinin doğruluğunu garanti etmeye yardımcı olmak için, madde veya madde tahsisat anahtarı başına mümkün olduğunca fazla geçmiş talep verisine sahip olmalısınız. Geçmiş talep verisi halihazırda içe aktarılmamışsa, içe aktarmak için **Geçmiş harici talep** (ReqDemPlanHistoricalExternalDemandEntity) veri varlığını Dynamics 365 Supply Chain Management içinde kullanın.

**Veri yönetimi** çalışma alanı içerisinde, varlık içerisindeki tüm alanların bir genel görünümünü görürsünüz.

1. **Veri yönetimi** çalışma alanını açın.
2. **Veri varlıkları** kutucuğuna tıklayın.
3. Varlık listesinde **Geçmiş harici talep** arayın.
4. **Hedef alanları** üzerine tıklayın. Aşağıdaki varlık alanları zorunludur: site (**DeliveringSiteId**), tarih (**DemandDate**), miktar (**DemandQuantity**), ve madde numarası (**ItemNumber**) veya madde tahsisat anahtarı (**ProductAllocationKeyId**).

Varlık verisini kullanmak için geçmiş talep verisini içeren Microsoft Excel dosyası veya virgülle ayrılmış değerler (CSV) dosyasına sahip olmalısınız. Aşağıdaki örnek, verinin bir CSV dosyasından nasıl alınacağını gösterir.

## <a name="example"></a>Örnek

Aşağıdaki dosyayı bir örnek olarak kullanabilirsiniz. [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast) karşıdan yükleyin. Bu dosya, madde D0001 için geçmiş talep verisini içerir. Yalnızca aşağıdaki zorunlu alanları içerir: site, miktar ve talep tarihi.

1. Geçmiş talep verisinin aktarılacağı şirketi seçin.
2. **Veri yönetimi** çalışma alanını açın.
3. **İçe aktar** kutusunu tıklatın.
4. İçe aktarma projesi için bir ad seçin, örneğin **Madde D0001 için geçmiş talep verisi içe aktar**.
5. **Kaynak veri biçimi** alanında, içe aktardığınız dosyanın dosya formatını seçin. Bu örnek için HistoricalDemandData dosyasını içe aktarmak için, **CSV** seçeneğini işaretleyin.
6. **Varlık adı** alanında, **Geçmiş harici talep** seçeneğini işaretleyin.
7. Dosyayı bilgisayarınıza kaydedin ve sonra karşıya yükleyin.
8. **İçe aktar**'ı tıklatın.
9. **Yürütme özeti** sayfası otomatik olarak açılır. İçe aktarılan veriyi sayfada doğrulayın.

Geçmiş talep verisini içe aktardıktan sonra talep tahminleri oluşturabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

[İstatistiksel temel tahmin oluşturma](generate-statistical-baseline-forecast.md)
