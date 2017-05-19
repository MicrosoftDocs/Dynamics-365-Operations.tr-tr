---
title: "Çekirdek verileri yeni bir perakende ortamında başlatılamıyor"
description: "Bu makale Microsoft Dynamics 365 for Operations - Perakende için başlatma işleminin bir parçasını oluşturulan veriyi açıklar."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: b5290bb62ab8ad71b06b0478ccaf6dbb61454170
ms.contentlocale: tr-tr
ms.lasthandoff: 04/26/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Çekirdek verileri yeni bir perakende ortamında başlatılamıyor

[!include[banner](includes/banner.md)]


Bu makale Microsoft Dynamics 365 for Operations - Perakende için başlatma işleminin bir parçasını oluşturulan veriyi açıklar.

Perakende çözümü Microsoft Dynamics Lifecycle Services (LCS) aracılığıyla dağıtıldıktan sonra, temel yapılandırma verilerini oluşturmak için perakende yapılandırmasını başlatmanız gerekir. **Önemli:** Perakende yapılandırmasını başlatmadan önce, perakende mağazaları ayarlayacağınız bir dil ve her bir tüzel kişilik için bir posta adresi belirtmiş olduğunuza emin olun. Bu adımın, perakende için kullandığınız her bir tüzel kişilik için tamamlanması gerekir. Perakende yapılandırmasını başlatmak için aşağıdaki adımları izleyin.

1.  Dynamics 365 for Operations istemcisini başlat.
2.  **Perakende ve ticaret** &gt; **Genel merkez kurulumu** &gt; **Parametreler** &gt; **Perakende parametreleri** menüsüne tıklayın.
3.  **Başlat** öğesine tıklayın.

Başlatma, aşağıdaki varsayılan yapılandırma verilerini oluşturur:

-   Perakende planlayıcısı görevleri ve alt görevleri
-   Perakende kanalı şeması
-   Perakende dağıtım planlamaları
-   Düğme grupları, görüntüler ve temaları içeren varsayılan ekran düzenleri
-   Zaman dilimi bilgileri
-   Satış noktası (POS) işlemleri
-   POS izinleri
-   Kanal raporları
-   Öznitelik meta verileri
-   Varlık doğrulama şablonları
-   Commerce Data Exchange oturum geçmişini temizlemeye yönelik toplu görev

Ayrıca, Dynamics 365 for Operations veritabanı için ödeme kartı sektörü ile ilgili günlük kaydı etkinleştirilmiştir. **Not:** Perakende planlayıcısını ayrıca yapılandırmak seçeneği vardır. Bu seçenek, Perakende planlayıcısı yapılandırmasını varsayılan ayarlarına sıfırlama olanağı sağlar. Başlatma tamamlandıktan sonra ek perakende verilerini yapılandırmanız gerekir. Burada bazı örnekler verilmiştir:

-   Perakende parametreleri
-   Perakende Planlayıcısı parametreleri
-   Perakende kanalları
-   Kayıtlar ve cihazlar
-   Sınıflamalar





