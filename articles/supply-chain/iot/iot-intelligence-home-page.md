---
title: IoT Zekası giriş sayfası
description: Bu konu, IoT Zekası hakkındaki bilgilere bağlantılar sağlar.
author: robinarh
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: intro-internal
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f32cb5578f3c15a10f863980491a687f64312cd
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/19/2021
ms.locfileid: "7652107"
---
# <a name="iot-intelligence-home-page"></a>IoT Zekası giriş sayfası

[!include [banner](../../includes/banner.md)]

> [!IMPORTANT]
> Bu özellik şu anda yalnızca aşağıdaki ülkelerde/bölgelerde kullanılabilir:
>
> - ABD (Amerika Birleşik Devletleri)
> - AB (Avrupa Birliği)
> - AU (Avustralya)
> - CA (Kanada)
> - BK (Birleşik Krallık)

IoT zekası, Microsoft Dynamics 365 Supply Chain Management için bir eklentidir. İlgili öngörüler oluşturmak için, Supply Chain Management'taki verilerle ilgili Nesnelerin İnterneti (IoT) sinyallerini tümleştirir.

IoT Zekası aşağıdaki senaryoları destekler:

+ **Üretim gecikmeleri** – Bu senaryo gerçek döngü süresini planlanan döngü süresine karşılaştırır. Supply Chain Management üretimin zamanlamada ne zaman olmadığını size bildirir, böylece işletme verimliliğini en üst düzeye çıkarmak ve sipariş gecikmelerini önlemek için müdahale edebilirsiniz.
+ **Donatım kapalı kalma süresi** – Bu senaryo ölçülen çalışma süresini kullanıcı tanımlı parametrelere karşılaştırır. Supply Chain Management, bir kesinti eşiği aşıldığında, üretim emri iş emrini yeniden çizelgeleme veya bakım iş emri oluşturma gibi eylemleri gerçekleştirebileceğiniz konusunda sizi bilgilendirir.
+ **Ürün kalitesi** – Bu senaryo, nem ve sıcaklık gibi sensör okumalarını, kullanıcı tanımlı kalite ölçümleriyle karşılaştırır. Supply Chain Management, kalite standartlarını korumak ve atık durumuna küçültmek için müdahale edebilmeniz için bir sapma gerçekleştiğinde size bildirir.

Aşağıdaki şekil, Azure IoT Hub, IoT zekası ve Supply Chain Management'ın etkileşimini göstermektedir.

![IoT Hub, IoT zekası ve Supply Chain Management.](media/iot_intelligence.png)

## <a name="setup"></a>Kurulum

IoT yönetim kodunu herhangi bir kod yazmadan ayarlayabilir ve konfigüre edebilirsiniz. Temel adımlar şunlardır.

1. [Azure kaynaklarını ayarla](iot-azure-setup.md) – bir IoT Merkezi, Redis Cache ve Supply Chain Management'tan erişilebilen bir Key Vault oluşturun.
2. [IoT Hub'ı için ileti şeması formatları](iot-schema-format.md) – Aygıtları IoT Hub'a göndermek üzere yapılandırın ve JavaScript Nesne Gösterimi (JSON) ileti biçimi tanımlayın.
3. Özellik Yönetiminde, IoT yönetim bilgileri özellik bayrağını etkinleştirin. 
4. [Microsoft Dynamics LifeCycle Services (LCS) içindeki IoT yönetim bilgileri eklentisini yükleyin](iot-lcs-setup.md) – Eklentiyi, LCS'ye yükleyin ve Azure gizli kod dizelerini yapılandırın.
5. [Ölçümleri ayarla](iot-metrics-setup.md) – Supply Chain Management'ta ölçümleri ayarlayın.
6. [Senaryo kurulumu](iot-scenario-setup.md) -Supply Chain Management'ta senaryolar ayarlayın.

## <a name="tracking-and-maintenance"></a>İzleme ve bakım

+ [Dynamics 365 Supply Chain Management'ta senaryoları izleme](iot-management.md#monitor-scenarios)
+ [Senaryoyu devre dışı bırakma](iot-scenario-setup.md#disable-a-scenario)
+ [Eklentiyi kaldırma](iot-lcs-setup.md#uninstall-addin)
+ [Çalışan bir IoT Zekası senaryosunu değiştirme](iot-management.md#modify-a-running-iot-intelligence-scenario)
+ [Benzetim seçenekleri](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]