---
title: IoT Zekası için ölçümler ayarlama
description: Bu makale, IoT Zekası için ölçümlerin nasıl ayarlanacağını açıklar.
author: johanhoffmann
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 147df50a9d0baf78f2efc3e57b2cda935e38cee3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882706"
---
# <a name="set-up-metrics-for-iot-intelligence"></a>IoT Zekası için ölçümler ayarlama

[!include [banner](../../includes/banner.md)]

## <a name="configure-metrics"></a>Ölçümleri yapılandırma

İletilerinizin zaman serisi grafiklerini Microsoft Dynamics 365 Supply Chain Management'ta görüntülemek istiyorsanız, bu adımları izleyerek ölçümleri ayarlamanız gerekir.

1. Redis Cache için bağlantı dizesini kopyalayın:

    1. Azure portalda, Redis Cache'ye gidin.
    2. **Ayarlar** \> **Erişim anahtarları**'na gidin.
    3. **Birincil bağlantı dizesi** alanındaki değeri kopyalayın.

2. Supply Chain Management'ta **Üretim denetimi \> Kurulum \> IoT Zekası \> Senaryo parametreleri**'ne gidin.
3. **Senaryo parametreleri** sayfasında, **Zaman serileri** sekmesinde, **Redis ölçüm mağazası bağlantı dizesi** alanına kopyaladığınız bağlantı dizesini yapıştırın. Bu adım, Azure IoT Hub'daki ölçümlerin Supply Chain Management içinde görselleştirmesine olanak tanır. Değeri alana yapıştırdığınızda, şöyle gösterilir: **\*\*\*\*\*\***.

    > [!NOTE]
    > Redis Cache bağlantı dizelerinden birini her güncelleştirdiğinizde bu alanı da güncelleştirmeniz gerekir.

4. **Üretim denetimi \> Sorgular ve raporlar \> IoT Zekası \> Ölçüm anahtarları**'na gidin.
5. **Metrik anahtarları** sayfasında, **Güncelleştir**'i seçin.
6. **Ölçüm anahtarlarının güncelleştir** iletişim kutusunda, alanda **Arka planda çalıştır** kutusunun işaretli olduğuna dikkat edin. **Tamam**'ı seçin.

Redis Cache içindeki tüm metrik anahtarlar alınır ve **Metrik anahtarlar** listesine eklenir. [Senaryolar etkinleştirilinceye](iot-scenario-setup.md) kadar ölçüm değerleri görünmeyecektir.

## <a name="configure-the-resource-status-time-series"></a>Kaynak Durumu zaman serisini konfigüre etme

**Kaynak Durumu** zaman serisini yapılandırmak için aşağıdaki adımları izleyin.

1. Supply Chain Management'ta, **Üretim denetimi \> Üretim yürütme \> Kaynak Durumu**'na gidin.
2. **Kaynak durumu** sayfasında **Yapılandır**'ı seçin.
2. **Yapılandır** iletişim kutusunda, **Kaynak** listesinde, izlenecek bir öğe seçin.
3. **Zaman serisi 1** için **Düzenle** düğmesini seçin.
4. **Zaman serilerini seç** iletişim kutusunda kılavuzda bir ölçü seçin. (Ayrıca **Ölçüm anahtarlarını güncelleştir** bağlantısı bu iletişim kutusundan ölçüm anahtarlarını güncelleştirmek için de kullanılabilir.)
5. **Yapılandır** iletişim kutusuna dönmek için **Tamam**'ı seçin.
6. Bir görünen ad girin.
7. **Veri görüntüleme kaynağı** alanında bir zaman dilimi seçin.
8. **Tamam**'ı seçin.

Grafik görüntülenir.

## <a name="delete-a-metric-key"></a>Ölçüm anahtarını silme

1. Supply Chain Management'ta **Üretim denetimi \> Sorgular ve raporlar \> IoT Zekası \> Ölçüm anahtarları**'na gidin.
2. **Ölçüm anahtarları** sayfasında, silinecek ölçüm anahtarını seçin.
3. **Sil**'i seçin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]