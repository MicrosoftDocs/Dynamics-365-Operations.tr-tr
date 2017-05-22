---
title: "Sahtekarlık uyarıları ayarla"
description: "Bu konu, siparişler işlendiğinde, müşteri hizmetleri temsilcilerini sahte olması olası bilgilere karşı uyarmak için kuralların nasıl ayarlanacağını açıklar. Siparişleri otomatik olarak veya el ile beklemeye almak için kullanılacak belirli kodlar tanımlayabilirsiniz."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: ddcf68b9d9d35d63cb092225d468dd4a6a3d4446
ms.contentlocale: tr-tr
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-fraud-alerts"></a>Sahtekarlık uyarıları ayarla

[!include[banner](includes/banner.md)]


Bu konu, siparişler işlendiğinde, müşteri hizmetleri temsilcilerini sahte olması olası bilgilere karşı uyarmak için kuralların nasıl ayarlanacağını açıklar. Siparişleri otomatik olarak veya el ile beklemeye almak için kullanılacak belirli kodlar tanımlayabilirsiniz. 

Dolandırıcılık denetimi kurallarını ayarlamadan ve kullanmadan önce sahtekarlık denetimini etkinleştirmeniz ve çağrı merkezi parametrelerinde temel dolandırıcılık değerlerini tanımlamanız gerekir. İki tip sahtekarlık kuralı vardır:

-   **Statik kuralları** kara listede bir telefon numarası gibi belirli bir değer kullanır.
-   **Dinamik kuralları** değişkenler ve koşullardan oluşabilir.

Dinamik kuralı oluşturmadan önce kuralın kime uygulanacağını ve kuralın ne zaman uygulanacağını tanımlayan değişkenleri ve koşulları oluşturmanız gerekir. Örneğin, müşteri 1202'in 1.000,00 veya üzerinde değerinde koyduğu her satış siparişinin müşteri ödemesi doğrulanıncaya kadar beklemeye konmasını gerektiren bir kural oluşturmak istiyorsunuz. Bu durumda, müşteri 1202 ve sipariş toplamı 1.000,00 değişkenlerdir. Koşul, müşteri 1202 bir sipariş yaparsa ve toplam sipariş miktarı 1,000.00'e eşittir veya fazlaysa satış siparişi müşteri ödemesi doğrulanıncaya kadar beklemeye alınmalıdır.



