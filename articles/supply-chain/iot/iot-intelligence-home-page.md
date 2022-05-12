---
title: IoT Zekası giriş sayfası
description: Bu konu, IoT Zekası hakkındaki bilgilere bağlantılar sağlar.
author: tonyafehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: intro-internal
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c587f4e6a1dd58a7b8c238fc5afb16774828b2a
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644400"
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

- **Üretim gecikmeleri** – Bu senaryo gerçek döngü süresini planlanan döngü süresine karşılaştırır. Supply Chain Management üretimin zamanlamada ne zaman olmadığını size bildirir, böylece işletme verimliliğini en üst düzeye çıkarmak ve sipariş gecikmelerini önlemek için müdahale edebilirsiniz.
- **Donatım kapalı kalma süresi** – Bu senaryo ölçülen çalışma süresini kullanıcı tanımlı parametrelere karşılaştırır. Supply Chain Management, bir kesinti eşiği aşıldığında, üretim emri iş emrini yeniden çizelgeleme veya bakım iş emri oluşturma gibi eylemleri gerçekleştirebileceğiniz konusunda sizi bilgilendirir.
- **Ürün kalitesi** – Bu senaryo, nem ve sıcaklık gibi sensör okumalarını, kullanıcı tanımlı kalite ölçümleriyle karşılaştırır. Supply Chain Management, kalite standartlarını korumak ve atık durumuna küçültmek için müdahale edebilmeniz için bir sapma gerçekleştiğinde size bildirir.

Aşağıdaki şekil, Azure IoT Hub, IoT zekası ve Supply Chain Management'ın etkileşimini göstermektedir.

![IoT Hub, IoT zekası ve Supply Chain Management.](media/iot_intelligence.png)

<!-- KFM: hide setup info for now

## Setup

You can set up and configure IoT Intelligence without writing any code. Here are the basic steps.

1. [Set up Azure resources](iot-azure-setup.md) – Create an IoT hub, a Redis cache, and a key vault that can be accessed from Supply Chain Management.
2. [Message schema formats for IoT Hub](iot-schema-format.md) – Configure your devices to send messages to IoT Hub, and define the JavaScript Object Notation (JSON) message format.
3. In Feature Management, enable the IoT Intelligence feature flag. 
4. [Install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Install the add-in in LCS, and configure the Azure secrets.
5. [Set up metrics](iot-metrics-setup.md) – Set up metrics in Supply Chain Management.
6. [Scenario setup](iot-scenario-setup.md) – Set up the scenarios in Supply Chain Management.

-->

## <a name="tracking-and-maintenance"></a>İzleme ve bakım

- [Dynamics 365 Supply Chain Management'ta senaryoları izleme](iot-management.md#monitor-scenarios)
- [Senaryoyu devre dışı bırakma](iot-scenario-setup.md#disable-a-scenario)
- [Çalışan bir IoT Zekası senaryosunu değiştirme](iot-management.md#modify-a-running-iot-intelligence-scenario)
- [Benzetim seçenekleri](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]