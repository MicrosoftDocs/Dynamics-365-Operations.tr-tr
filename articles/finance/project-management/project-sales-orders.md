---
title: Proje satış siparişleri
description: Bu konu, projeye dayalı satış siparişlerinin zaman ve malzeme projeleri için nasıl oluşturulacağını açıklar.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 1d54c98a08dc7cccb5cafbbe401d0ce25a276c25
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185509"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Zaman ve malzeme projeleri için Proje satış siparişleri

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Bu konu, bir proje için satış siparişlerinin nasıl oluşturulacağını açıklar. Satış siparişleri yalnızca **zaman ve malzeme** türünde projeler için oluşturulabilir.

Proje sözleşmesinde birden fazla finansman kaynağı içeren bir satış ve zaman projesi varsa, **Birden fazla finansman kaynağına sahip projeler için satış siparişlerine izin ver** parametresini **Proje yönetimi ve muhasebe parametreleri** sayfasında etkinleştirmeniz gerekir. 

> [!NOTE]
> - Birden fazla finansman kaynağına sahip proje satış siparişleri desteği, uygulama sürümü 10.0.2 ve sonrası ile başlar.
> - Birden fazla finansman kaynağına sahip proje satış siparişleri için desteği etkinleştirme parametresi, Nisan 2020 sürüm dalgasında kaldırılacaktır, bundan sonra bu özellik her zaman etkin olacaktır.

Proje tabanlı satış siparişlerini iki şekilde oluşturabilirsiniz:

- Projenin kendisine gidin. Eylem Bölmesinde, **Yönet >Madde görevleri > Satış siparişleri**'ni seçin. Proje bilgisi, projedeki satış siparişine varsayılan olarak ayarlanır. Proje sözleşmesi, birden fazla finansman kaynağına sahipse, satış siparişi için fonlama kaynağını seçmeniz gerekecektir. Proje için yalnızca bir finansman kaynağı varsa, müşteri otomatik olarak ayarlanır.
- **Tüm satış siparişleri** liste sayfasına gidin ve yeni bir satış siparişi oluşturun. Satış siparişi için projeyi seçmeniz gerekecektir. Proje seçildikten sonra, müşteri finansman kaynağından ayarlanacaktır veya proje sözleşmesi birden fazla finansman kaynağına sahipse, finansman kaynağını seçmeniz gerekecektir.

