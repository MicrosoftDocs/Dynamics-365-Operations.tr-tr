---
title: Planlı siparişleri koru
description: Bu makalede planlı siparişleri yönetme yöntemleri hakkında bilgiler yer alır. Planlı siparişlerin durumunun nasıl güncelleştirileceğini, kesinleştirileceğini ve seçilen planlı sipariş ile aynı duruma sahip planlı siparişlerin nasıl filtreleneceğini açıklar.
author: t-benebo
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c127b25644e417983672c8111925ecd3a51d6ca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850713"
---
# <a name="maintain-planned-orders"></a>Planlı siparişleri koru

[!include [banner](../includes/banner.md)]

Bu makalede planlı siparişleri yönetme yöntemleri hakkında bilgiler yer alır. Planlı siparişlerin durumunun nasıl güncelleştirileceğini, kesinleştirileceğini ve seçilen planlı sipariş ile aynı duruma sahip planlı siparişlerin nasıl filtreleneceğini açıklar.

Planlı siparişleri **Master planlama** çalışma alanından, **Planlı sipariş** listesinden veya **Planlı üretim emirleri**, **Planlı satınalma emirleri** ve **Planlı transfer** listelerinden yönetebilirsiniz. 

## <a name="planned-order-status"></a>Planlı sipariş durumu
İlerlemenizi takip etmeye yardımcı olan **Durum** alanını kullanabilirsiniz. Aşağıdaki değerler kullanılır:

-   Master planlama planlı siparişler ürettiğinde, planlı siparişler **İşlem görmedi** durumunda olur.
-   Planlı bir siparişi kesinleştirmemeye karar vermeniz halinde, durumunu **Tamamlandı** olarak ayarlayabilirsiniz.
-   Planlı bir siparişi kesinleştirmek isterseniz sipariş durumunu **Onaylandı** olarak değiştirebilirsiniz. Sonraki bir master planlama çalışması sırasında değiştirilmemeleri veya silinmemeleri için **Onaylandı** durumundaki planlı siparişlere master planlama tarafından riayet edilir. Bunu başarmak için, planlama mantığı, Master planlama sırasında eski plan versiyonundaki **onaylanan** planlı siparişleri yeni plan sürümüne kopyalar.

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

> [!NOTE]
> **Parallelize Kesinleştirme** seçeneği yalnızca Kesinleştirmede birden fazla planlı sipariş seçildiğinde görüntülenir.

## <a name="additional-resources"></a>Ek kaynaklar

[Master planlara genel bakış](master-plans.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]