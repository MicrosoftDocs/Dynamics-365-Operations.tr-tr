---
title: Yeni Commerce ortamlarında çekirdek verileri başlatma
description: Bu konu, Dynamics 365 Commerce için başlatma işleminin parçası olarak oluşturulan veriyi açıklar.
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
ms.openlocfilehash: 24d4d49c51738203bb89a9844d57f644b8afd4b7
ms.sourcegitcommit: 0d7b700950b1f95dc030ceab5bbdfd4fe1f79ace
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284391"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a>Yeni Commerce ortamlarında çekirdek verileri başlatma

[!include [banner](includes/banner.md)]

Bu konu, Dynamics 365 Commerce için başlatma işleminin parçası olarak oluşturulan veriyi açıklar.

Commerce çözümü Microsoft Dynamics Lifecycle Services (LCS) aracılığıyla dağıtıldıktan sonra, temel yapılandırma verilerini oluşturmak için Commerce yapılandırmasını başlatmanız gerekir.

> [!IMPORTANT]
> Commerce yapılandırmasını başlatmadan önce mağazaları ayarlayacağınız bir dil ve her bir tüzel kişilik için bir posta adresi belirtmiş olduğunuza emin olun. Bu adımın, Commerce için kullandığınız her bir tüzel kişilik için tamamlanması gerekir.

Yapılandırmayı başlatmak için bu adımları izleyin.

1. Commerce istemcisini başlatın.
2. **Retail ve Commerce** &gt; **Headquarters kurulumu** &gt; **Parametreler** &gt; **Commerce parametreleri**'ne tıklayın.
3. **Başlat** öğesine tıklayın.

Başlatma, aşağıdaki varsayılan yapılandırma verilerini oluşturur:

- Commerce planlayıcısı görevleri ve alt görevleri
- Ticaret kanalı şeması
- Commerce dağıtım planlamaları
- Düğme grupları, görüntüler ve temaları içeren varsayılan ekran düzenleri
- Zaman dilimi bilgileri
- Satış noktası (POS) işlemleri
- POS izinleri
- Kanal raporları
- Öznitelik meta verileri
- Varlık doğrulama şablonları
- Commerce Data Exchange oturum geçmişini silmek için toplu iş

Ayrıca, Commerce veritabanı için ödeme kartı sektörü ile ilgili günlük kaydı etkinleştirilmiştir.

> [!NOTE]
> Commerce planlayıcısını ayrıca yapılandırmak seçeneği vardır. Bu seçenek, Commerce planlayıcısı yapılandırmasını varsayılan ayarlarına sıfırlama olanağı sağlar.

Başlatma tamamlandıktan sonra ek Commerce verilerini yapılandırmanız gerekir. Burada bazı örnekler verilmiştir:

- Ticaret parametreleri
- Ticaret planlayıcı parametreleri
- Commerce kanalları
- Kayıtlar ve cihazlar
- Sınıflamalar
