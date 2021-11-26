---
title: IoT Zekası'nı izleme ve yönetme
description: Bu konu, IoT Zekası'nın nasıl izleneceğini ve yönetileceğini açıklar.
author: tonyafehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8fbd750aa4a316f5e04f3c8622d0847ad9318360
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782669"
---
# <a name="monitor-and-manage-iot-intelligence"></a>IoT Zekası'nı izleme ve yönetme

[!include [banner](../../includes/banner.md)]

Bu konu, IoT Zekası'nın nasıl izleneceğini ve yönetileceğini açıklar.

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a>Microsoft Dynamics 365 Supply Chain Management'ta senaryoları izleme

IoT Zekası işlemesini çeşitli yerlerden izleyebilirsiniz:

+ **Modüller \> Üretim denetimi \> Sorgular ve raporlar \> IoT Zekası \> Bildirimler** - Çözüme ulaşmamış bildirimlerin listesini görüntüleyin.
+ **Modüller \> Üretim denetimi \> Sorgular ve raporlar \> IoT Zekası \> Kapanan bildirimler** - Çözüme ulaşmış veya kapatılmış bildirimlerin listesini görüntüleyin.
+ **Modüller \> Üretim denetimi \> Sorgular ve raporlar \> IoT Zekası \> Ölçüm anahtarları** - **Kaynak Durumu** zaman serisi grafiklerinin ölçüm anahtarlarını görüntüleyin.
+ **Modüller \> Üretim denetimi \> Üretim yürütme \> Kaynak durumu** – **Yapılandır** iletişim kutusunu kullanarak belirli ölçümleri izleyin. Senaryo bir özel durum algılarsa, özel durumun ayrıntılarını gösteren bir bildirim görüntülenir.
+ **Çalışma alanları \> Üretim katı yönetimi \> Bildirimleri** - Çözüme ulaşmamış bildirimlerin listesini görüntüleyin.

## <a name="modify-a-running-iot-intelligence-scenario"></a>Çalışan bir IoT Zekası senaryosunu değiştirme

Bir senaryo çalışırken şu değişiklikleri yapabilirsiniz:

+ Yeni sensör şeması tanımları ekleme.
+ Yeni sinyal verisi değerleri seçme.
+ Var olan sinyal verisi değerlerinin seçimini iptal etme.
+ Yeni sinyal verisi değerleri ekleme ve eşleme.
+ Eşik değerlerini güncelleştirme.

Bir senaryo çalışırken şu değişiklikler yapılamaz:

+ Etkin bir senaryo tarafından kullanılmakta olan tüm şema tanımlarını silme veya değiştirme.
+ Etkin senaryonun seçili şema yollarını değiştirme.

## <a name="simulation-options"></a>Benzetim seçenekleri

Fabrika makine sinyallerinin benzetimini yapabilirsiniz. Daha fazla bilgi edinmek için şu konulara bakın:

+ [IoT DevKit AZ3166'yı Azure IoT Hub'a bağlama](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Raspberry Pi online simulator'ı Azure IoT Hub'a (Node. js) bağlama](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [Aygıt Benzetimi çözüm hızlandırıcısına genel bakış](/azure/iot-accelerators/iot-accelerators-device-simulation-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]