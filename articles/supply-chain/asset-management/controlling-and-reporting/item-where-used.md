---
title: Kullanıldığı madde
description: Bu konu, bir öğenin Varlık Yönetimi içinde nerede kullanıldığını açıklar.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 511108e689c10e27a42253d95b02e5394f9eb713
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652368"
---
# <a name="item-where-used"></a>Kullanıldığı madde

[!include [banner](../../includes/banner.md)]

 

Maddenin kıymet yönetiminde nereye kullanıldığını genel olarak almak için belirli bir madde için hesaplama yapabilirsiniz. Sonuçlar, ömrü boyunca öğenin kullanıldığı bağlamı gösterir. **Maddenin kullanımı** sayfası ana Varlık Yönetimi menüsünden açılabildiği gibi, ayrıca aşağıdaki sayfalardan da erişilebilir:

- [Varlık ürün reçetesi](../objects/object-BOM.md)

- [Varlık türü varsayılanları üzerinde yedek parçalar](../setup-for-objects/object-types.md)

- [Bakım iş türü varsayılan öngörüleri üzerinde madde öngörüsü](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [İş emri bakım tahmini](../work-orders/maintenance-forecasts.md)

- [İş emri satınalma talebi](../work-orders/procurement.md)

- [İş emri satınalma işlemi](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a>Madde oluşturma-kullanım yeri hesaplaması

1. **Varlık yönetimi** > **Sorgular** > **Maddenin kullanıldığı** veya **Kullanıldığı yerde madde** düğmesini yukarıda bahsi geçen sayfaların birinde seçebilirsiniz.

2. **Kullanılan madde** iletişim kutusunda, hesaplama yapmak istediğiniz maddeyi **Madde numarası** alanında seçin.

3. İşlem yapılacak yerleşimlerle ilgili olarak madde satırlarının ne kadar ayrıntılı olmasını istediğinizi belirtmek için **Düzey** alanını kullanabilirsiniz. 

    Örneğin, alana "1" numarasını girerseniz ve çok düzeyli işlem yapılacak yerleşim yapısına sahipseniz, işlem yapılacak yerleşim için tüm madde satırları üst düzeyde gösterilir. Bu nedenle, satırdaki ilişki/miktar, daha düşük bir düzeyde bulunan işlevsel konumlardan eklenebilir. 
    
    **Düzey** alanına "0" değerini girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeylerinde bulunan tüm madde satırlarını gösteren ayrıntılı bir sonuç görürsünüz.

4. **Dahil et** bölümünde, hesaplamayı dahil etmek istediğiniz düğmelerde "Evet"i seçin.

5. Hesaplamayı başlatmak için **Tamam**'a tıklayın.

6. **Madde kullanımı** sekmesinde gerekli hesaplama ayrıntı düzeyini göstermek için **Gruplama ölçütü** düğmelerini seçin. Seçilen **Gruplandırma ölçütü** düğmeleri vurgulanır. Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.

7. Maddeyle ilgili boyutları göstermek istiyorsanız, **boyutları görüntüle** üzerine tıklatın ve gösterilecek boyutları seçin.

## <a name="example"></a>Örnek

Aşağıdaki ekran görüntüsünde, "1000" numaralı madde için madde-kullanım yeri hesaplaması örneği görüntülenir.

![Madde kullanımı hesaplaması örneği](media/12-controlling-and-reporting.png)

