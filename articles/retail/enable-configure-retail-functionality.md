---
title: Yeni Retail ortamlarında çekirdek verileri başlatma
description: Bu konu, Dynamics 365 Retail için başlatma işleminin parçası olarak oluşturulan veriyi açıklar.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 49b21d81437ebd7cc55076444ee71ae1143bfac0
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025528"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a>Yeni Retail ortamlarında çekirdek verileri başlatma

[!include [banner](includes/banner.md)]

Bu konu, Dynamics 365 Retail için başlatma işleminin parçası olarak oluşturulan veriyi açıklar.

Perakende çözümü Microsoft Dynamics Lifecycle Services (LCS) aracılığıyla dağıtıldıktan sonra, temel yapılandırma verilerini oluşturmak için perakende yapılandırmasını başlatmanız gerekir.

> [!IMPORTANT]
> Perakende yapılandırmasını başlatmadan önce, perakende mağazaları ayarlayacağınız bir dil ve her bir tüzel kişilik için bir posta adresi belirtmiş olduğunuza emin olun. Bu adımın, perakende için kullandığınız her bir tüzel kişilik için tamamlanması gerekir.

Perakende yapılandırmasını başlatmak için aşağıdaki adımları izleyin.

1. Retail istemcisini başlatın.
2. **Perakende** &gt; **Genel merkez kurulumu** &gt; **Parametreler** &gt; **Perakende parametreleri** menüsüne tıklayın.
3. **Başlat** öğesine tıklayın.

Başlatma, aşağıdaki varsayılan yapılandırma verilerini oluşturur:

- Perakende planlayıcısı görevleri ve alt görevleri
- Perakende kanalı şeması
- Perakende dağıtım planlamaları
- Düğme grupları, görüntüler ve temaları içeren varsayılan ekran düzenleri
- Zaman dilimi bilgileri
- Satış noktası (POS) işlemleri
- POS izinleri
- Kanal raporları
- Öznitelik meta verileri
- Varlık doğrulama şablonları
- Commerce Data Exchange oturum geçmişini silmek için toplu iş

Ayrıca, Retail veritabanı için ödeme kartı sektörü ile ilgili günlük kaydı etkinleştirilmiştir.

> [!NOTE]
> Perakende planlayıcısını ayrıca yapılandırmak seçeneği vardır. Bu seçenek, Perakende planlayıcısı yapılandırmasını varsayılan ayarlarına sıfırlama olanağı sağlar.

Başlatma tamamlandıktan sonra ek perakende verilerini yapılandırmanız gerekir. Burada bazı örnekler verilmiştir:

- Perakende parametreleri
- Perakende Planlayıcısı parametreleri
- Perakende kanalları
- Kayıtlar ve cihazlar
- Sınıflamalar
