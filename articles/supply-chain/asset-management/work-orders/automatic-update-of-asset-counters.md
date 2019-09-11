---
title: Kıymet sayaçlarını otomatik olarak güncelleştirme
description: Bu konuda, Varlık Yönetiminde varlık sayaçlarının otomatik olarak güncelleştirilmesi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875952"
---
# <a name="automatic-update-of-asset-counters"></a>Kıymet sayaçlarını otomatik olarak güncelleştirme

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Önceki bölümde, varlık sayaçlarının el ile kaydı açıklanmıştır. Varlık sayaçları kurulumu [Sayaçlar](../setup-for-objects/counters.md) bölümünde açıklanmaktadır.

Sayaç değerleri, üretim saetleri veya üretim miktarına göre üretim kayıtlarından da otomatik olarak güncelleştirilebilir. Bu işlem, **Varlık sayaçlarını güncelleştir**'de gerçekleştirilir. Bir veya daha fazla varlığı **Başlangıç tarihi** parametresi ekleyerek güncelleştirebilirsiniz. Bu parametre, üretim kayıtları (saat veya üretilen miktar) için başlangıç tarihini belirtir; bu, sayaç değerlerinin güncelleştirilmesi gereken başlangıç tarihidir.

Bir kaynakla ilişkili olan *ve* üretilen miktara veya üretim saatlerine göre güncelleştirilmek üzere ayarlanan varlık sayaçları bulunan tüm varlıklar otomatik güncelleştirmeye dahil edilir ve yeni sayaç değerleri oluşturulur.

Üretim miktarına dayalı sayaçlarla ilgili olarak, ürün miktarının yanı sıra kaydedilen hata miktarı da sayımına dahil edilir. Üretilen miktar kaydı için kullanılan birim sayaçta kullanılan birimden farklıysa miktar, sayaç birimine karşılık gelecek şekilde dönüştürülür.

Yukarıda belirtildiği gibi, otomatik sayaçlar üretim kayıtlarından güncelleştirilebilir. Bu nedenle, sayaçlarını otomatik olarak güncelleştirmek istediğiniz varlık bir kaynakla (makine) ilişkili olmalıdır. Aşağıdaki açıklamalar, **Varlık yönetimi** modülündeki bir varlıkla ilgili sayaçların otomatik güncelleştirilmesi için temel olarak kullanılan üretim emirlerinin kurulumu ve işlenmesi (**Üretim denetimi** modülünde) ile ilgili genel bilgiler sağlar.

Üretilen miktarlar veya üretim saatleri kaynağa kaydedildiğinde, ilgili varlık sayaçlarını güncelleştirebilirsiniz.

1. **Varlık yönetimi** > **Periyodik** > **Varlıklar** > **Varlık sayaçlarını güncelleştir**'e tıklayın.

2. **Başlangıç tarihi** alanında otomatik güncelleştirmenin başlangıç tarihini seçin.

>[!NOTE]
>Bu alandaki tarih, **Rota hareketlerinden** gelen "süren iş" tarihidir (**Üretim denetimi** > **Sorgular ve raporlar** > **Üretim** > **Rota hareketleri** > **Fiziksel tarih** alanı).

3. Otomatik güncelleştirme için belirli varlıkları, varlık türlerini veya kaynakları seçmek isterseniz **Eklenecek kayıtlar** hızlı sekmesinde **Filtre**'ye tıklayın ve ilgili seçimleri yapın.

4. Gerekirse, **Arka planda çalıştır** hızlı sekmesinde otomatik güncelleştirmeyi toplu iş olarak ayarlayabilirsiniz.

![Şekil 1](media/12-work-orders.png)

5. **Tamam**'a tıklayın. Otomatik varlık sayacı tamamlandığında, varlıkla ilgili sayaç kayıtlarını **Varlık sayaçları**'nda görebilirsiniz (**Varlık yönetimi** > **Genel** > **Varlılklar** > **Tüm varlıklar** > varlık seçin > **Sayaçlar** düğmesi).

**Varlık sayacı toplamları**'nda tüm varlıklardaki tüm sayaç türlerinde yapılmış en son kaydın genel görünümünü alabilirsiniz. **Varlık Yönetimi** > **Sorgular** > **Varlıklar** > **Varlık toplam değeri**'ne tıklayın. Bu, **Varlık sayaçları**'na çok benzer ancak **Varlık toplam değeri**'nde kayıtları ekleyemez veya düzenleyemezsiniz. Yalnızca genel bakış içindir.

![Şekil 2](media/13-work-orders.png)


- Otomatik olarak güncelleştirilen sayaç türleri için el ile sayaç değeri kayıtları oluşturmak da mümkündür. Daha fazla bilgi için "Varlık sayaçlarını el ile güncelleştirme" bölümüne bakın.
- Başka bir sayaçla ilişkili sayaçlar ayarlayabilirsiniz. Bu, bir sayaç güncelleştirildiğinde ilgili sayaçların da aynı anda otomatik olarak güncelleştirileceği anlamına gelir. İlgili sayaçların kurulumuyla ilgili olarak [Sayaçlar](../setup-for-objects/counters.md) bölümüne bakın.
