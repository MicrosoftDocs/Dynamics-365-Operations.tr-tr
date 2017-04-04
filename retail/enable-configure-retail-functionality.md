---
title: "Çekirdek verileri yeni bir perakende ortamında başlatılamıyor"
description: "Bu makale Microsoft Dynamics 365 işlemleri - perakende için başlatma işleminin bir parçası oluşturulan veri açıklar."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 137c675781cf75d9ce621a84c89224019c161362
ms.lasthandoff: 03/31/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Çekirdek verileri yeni bir perakende ortamında başlatılamıyor

Bu makale Microsoft Dynamics 365 işlemleri - perakende için başlatma işleminin bir parçası oluşturulan veri açıklar.

Perakende çözümü Microsoft Dynamics Lifecycle Services (LCS) aracılığıyla dağıtıldıktan sonra, temel yapılandırma verilerini oluşturmak için perakende yapılandırmasını başlatmanız gerekir. **Önemli:** Perakende yapılandırmasını başlatmadan önce, perakende mağazaları ayarlayacağınız bir dil ve her bir tüzel kişilik için bir posta adresi belirtmiş olduğunuza emin olun. Bu adımın, perakende için kullandığınız her bir tüzel kişilik için tamamlanması gerekir. Perakende yapılandırmasını başlatmak için aşağıdaki adımları izleyin.

1.  Dynamics 365 işlemleri istemci için başlatın.
2.  ' I **perakende ve ticaret**&gt;**Headquarters Kurulumu**&gt;**parametreleri**&gt;**perakende parametreleri**.
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

Ayrıca, diğer bir deyişle günlüğü ilgili ödeme kartı endüstri (PCI) veritabanı işlemleri için Dynamics 365 için etkinleştirilir. **Not:** Perakende planlayıcısını ayrıca yapılandırmak seçeneği vardır. Bu seçenek, Perakende planlayıcısı yapılandırmasını varsayılan ayarlarına sıfırlama olanağı sağlar. Başlatma tamamlandıktan sonra ek perakende verilerini yapılandırmanız gerekir. Burada bazı örnekler verilmiştir:

-   Perakende parametreleri
-   Perakende Planlayıcısı parametreleri
-   Perakende kanalları
-   Kayıtlar ve cihazlar
-   Sınıflamalar



