---
title: İade edilen maddeleri incelemeye iletme
description: İade edilen bir maddeyi kaydederken, bir maddenin stoka iade edilmeden veya başka bir yöntemle elden çıkarılmadan önce denetlemeye gönderilmesini belirtebilirsiniz.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70aafb752b2c847d5d48236fd5d201a73e088c24
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556795"
---
# <a name="pass-returned-items-on-to-inspection"></a>İade edilen maddeleri incelemeye iletme 

[!include [banner](../includes/banner.md)]


İade edilen bir maddeyi kaydederken, bir maddenin stoka iade edilmeden veya başka bir yöntemle elden çıkarılmadan önce denetlemeye gönderilmesini belirtebilirsiniz.

1.  **Stok Yönetimi** \> **Günlükler** \> **Madde varışı** \> **Madde varışı**'na gidin.
    
    \-veya-
    
    **Stok Yönetimi** \> **Günlükler** \> **Madde varışı** \> **Üretim girişi**'ne tıklayın.

2.  **Konum günlüğü** formunda bir maddenin teslim alınmasını her zamanki gibi kaydedin.
    

    > [!NOTE]
    > <P>İade edilen maddelerin girişini kaydetme hakkında bilgi için bkz. <A href="register-the-receipt-of-returned-items.md">İade edilen maddelerin girişini kaydetme</A></P>



3.  **Varsayılan değerler** sekmesinde, **İşleme modu** alanında, **Karantina yönetimi** onay kutusunu seçin.

Bu seçimle sisteme bir karantina emri oluşturma isteği gönderilir ve denetimleri gerçekleştiren kişi veya departman **Karantina emri** formunu kullanarak bu emre yanıt verir.

## <a name="see-also"></a>Ayrıca bkz.

[İade edilen maddeleri inceleme yoluyla alma](take-returned-items-through-inspection.md)

[İade edilen maddelerin nasıl elden çıkarılacağını belirtme](specify-how-to-dispose-of-returned-items.md)

