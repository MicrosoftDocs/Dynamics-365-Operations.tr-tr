---
title: Planlı siparişleri koruma
description: Bu konuda planlı siparişleri yönetme yöntemleri hakkında bilgiler yer alır. Planlı siparişlerin durumunun nasıl güncelleştirileceğini, kesinleştirileceğini ve seçilen planlı sipariş ile aynı duruma sahip planlı siparişlerin nasıl filtreleneceğini açıklar.
author: roxanadiaconu
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ddf2c7b4c67bec6c29387c78d1fdb021d85d702
ms.sourcegitcommit: 620e15555d176eec3905b48d5001af1c50107ce6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/09/2019
ms.locfileid: "1993452"
---
# <a name="maintain-planned-orders"></a>Planlı siparişleri koruma

[!include [banner](../includes/banner.md)]

Bu konuda planlı siparişleri yönetme yöntemleri hakkında bilgiler yer alır. Planlı siparişlerin durumunun nasıl güncelleştirileceğini, kesinleştirileceğini ve seçilen planlı sipariş ile aynı duruma sahip planlı siparişlerin nasıl filtreleneceğini açıklar.

Planlı siparişleri **Master planlama** çalışma alanından, **Planlı sipariş** listesinden veya **Planlı üretim emirleri**, **Planlı satınalma emirleri** ve **Planlı transfer** listelerinden yönetebilirsiniz. 

## <a name="planned-order-status"></a>Planlı sipariş durumu
İlerlemenizi takip etmeye yardımcı olan **Durum** alanını kullanabilirsiniz. Aşağıdaki değerler kullanılır:

-   Master planlama planlı siparişler ürettiğinde, planlı siparişler **İşlem görmedi** durumunda olur.
-   Planlı bir siparişi kesinleştirmemeye karar vermeniz halinde, durumunu **Tamamlandı** olarak ayarlayabilirsiniz.
-   Planlı bir siparişi kesinleştirmek isterseniz sipariş durumunu **Onaylandı** olarak değiştirebilirsiniz. Değiştirilmemeleri veya silinmemeleri için **Onaylandı** durumundaki planlı siparişlere ana planlama tarafından riayet edilir. 

## <a name="firming-planned-orders"></a>Planlı siparişleri kesinleştirme 
Planlı siparişler kesinleştirilerek gerçek siparişler oluşturulur. Bunlar *serbest bırakılmış* veya *açık siparişler* olarak da bilinirler. Planlı bir sipariş kesinleştirildiğinde, ilgili modülün siparişler bölümüne taşınır.

**Planlı siparişler** sayfasındaki iki kesinleştirme seçeneğinden birini belirleyebilirsiniz:

-   **Kesinleştir** – Bu seçenek, bir veya birden fazla seçili planlı siparişi kesinleştirir.
-   **Tümünü kesinleştir** – Bu seçenek, filtredeki tüm planlı siparişleri kesinleştirir. **Tümünü kesinleştir** seçeneğini kullandığınızda planlı siparişi seçmeniz gerekmez; filtrdeki tüm planlı siparişler kesinleştirilir. Çok sayıda planlı siparişi kesinleştirmek istiyorsanız bu seçenek yararlı olabilir.

> [!NOTE]
> **Planlı siparişler formu > Görüntüle > Kesinleştirme geçmişi** altındaki **Kesinleştirme geçmişi**'nden kesinleştirilen planlı bir siparişi izleyebilirsiniz.

## <a name="parallelize-firming"></a>Kesinleştirmeyi paralel yap
Birçok siparişi aynı anda kesinleştirmek istiyorsanız çalışmayı koşut hale getirmek, çalışma süresini veya performansını iyileştirebilir. **Kesinleştir** veya **Tümünü kesinleştir** seçenekleriyle birden fazla planlı siparişi kesinleştirirken bu seçeneği kullanabilirsiniz. Aşağıdaki parametreler kullanılabilir:

-   **Kesinleştirmeyi koşut hale getir** – **Evet** seçilirse kesinleştirme işlemi, **Dizi sayısı**'nda tanımlanan dizilerin sayısıyla koşut hale getirilir.
-   **Dizi sayısı** – Kesinleştirme işlemini koşut hale getirmek için kullanılan dizi sayısını denetler. Parametre, yalnızca **Kesinleştirmeyi koşut hale getir** seçeneği **Evet** olarak ayarlandığında gösterilir.


<a name="additional-resources"></a>Ek kaynaklar
--------

[Master planlar](master-plans.md)



