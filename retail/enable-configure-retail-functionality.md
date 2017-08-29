---
title: "Çekirdek verileri yeni bir perakende ortamında başlatılamıyor"
description: "Bu makale Microsoft Dynamics 365 for Retail için başlatma işleminin bir parçasını oluşturulan veriyi açıklar."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 0ee002d733882734c9f5a21e0467cacd1b3ff318
ms.contentlocale: tr-tr
ms.lasthandoff: 06/20/2017

---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Çekirdek verileri yeni bir perakende ortamında başlatılamıyor

[!include[banner](includes/banner.md)]


Bu makale Microsoft Dynamics 365 for Retail için başlatma işleminin bir parçasını oluşturulan veriyi açıklar.

Perakende çözümü Microsoft Dynamics Lifecycle Services (LCS) aracılığıyla dağıtıldıktan sonra, temel yapılandırma verilerini oluşturmak için perakende yapılandırmasını başlatmanız gerekir. **Önemli:** Perakende yapılandırmasını başlatmadan önce, perakende mağazaları ayarlayacağınız bir dil ve her bir tüzel kişilik için bir posta adresi belirtmiş olduğunuza emin olun. Bu adımın, perakende için kullandığınız her bir tüzel kişilik için tamamlanması gerekir. Perakende yapılandırmasını başlatmak için aşağıdaki adımları izleyin.

1.  Dynamics 365 for Retail istemcisini başlat.
2.  **Perakende** &gt; **Genel merkez kurulumu** &gt; **Parametreler** &gt; **Perakende parametreleri** menüsüne tıklayın.
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

Ayrıca, Dynamics 365 for Retail veritabanı için ödeme kartı sektörü ile ilgili günlük kaydı etkinleştirilmiştir. **Not:** Perakende planlayıcısını ayrıca yapılandırmak seçeneği vardır. Bu seçenek, Perakende planlayıcısı yapılandırmasını varsayılan ayarlarına sıfırlama olanağı sağlar. Başlatma tamamlandıktan sonra ek perakende verilerini yapılandırmanız gerekir. Burada bazı örnekler verilmiştir:

-   Perakende parametreleri
-   Perakende Planlayıcısı parametreleri
-   Perakende kanalları
-   Kayıtlar ve cihazlar
-   Sınıflamalar





