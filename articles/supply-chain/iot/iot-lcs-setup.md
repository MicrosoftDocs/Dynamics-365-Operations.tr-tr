---
title: LCS'de IoT Zekası eklentisini yükleme
description: Bu konu, Microsoft Dynamics LifeCycle Services (LCS) Içindeki IoT Zekası eklentisinin nasıl yükleneceğini açıklamaktadır.
author: robinarh
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ad8b33633646f27bc368dc4bbedc1eb64c150a9f
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4014947"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>LCS'de IoT Zekası eklentisini yükleme

[!include [banner](../../includes/banner.md)]

Bu konu, Microsoft Dynamics LifeCycle Services (LCS) Içindeki IoT Zekası eklentisinin nasıl yükleneceğini açıklamaktadır. Eklentilerin tanıtım/deneme ortamına yüklenemeyeceğini unutmayın. Eklentiyi yükleyebilmek için önce [Azure kaynaklarını oluşturmanız gerekir](iot-azure-setup.md).

## <a name="set-up-the-lcs-environment"></a>LCS ortamını ayarlama

1. LCS'yi açın ve Microsoft Dynamics 365 Supply Chain Management ortamınıza gidin.
2. **Ortam eklentileri** bölümüne kaydırın.
3. Ortam için etkinleştirilmiş eklentilerin listesini göstermek için **Yeni eklenti yükle** 'yi seçin.
4. **Yüklemek için bir eklenti seçin** iletişim kutusunda **IoT Zekası** 'nı seçin.
5. **Eklenti ayarlama** iletişim kutusunda IoT Hub'ın ve Redis önbelleğinin ayrıntılarını belirtin. [Azure kaynakları oluştur](iot-azure-setup.md) altında oluşturduğunuz anahtar kasasında gerekli değerleri bulabilirsiniz.

    + **Kiracı kimliği:** Azure portalında, anahtar kasasına gidin ve sonra sol gezinti bölmesinde **Genel bakış** 'ı seçip **Dizin kimliği** değerini kopyalayın. Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.
    + **IoT Olay Hub'ı ile uyumlu bitiş noktası Anahtar Kasası URI'si:** Anahtar kasasına gidin ve sol gezinti bölmesinde **Genel bakış** 'ı seçip **DNS adı** değerini kopyalayın. Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.
    + **IoT Olayı Hub'ı ile uyumlu bitiş noktası gizli dizi adı:** Anahtar kasasına gidin ve sol gezinti bölmesinde, **Gizli diziler** 'i seçip IoT Hub'ın olay hub'ı bağlantı dizesinin depolandığı gizli dizisinin adını kopyalayın. Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.
    + **Redis önbelleği anahtar kasası URI'si:** Anahtar kasasına gidin ve sol gezinti bölmesinde **Genel bakış** 'ı seçip **DNS adı** değerini kopyalayın. Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.
    + **Redis önbelleği uç nokta gizli dizi adı:** Anahtar kasasına gidin ve sol gezinti bölmesinde, **Gizli diziler** 'i seçip Redis önbelleği bağlantı dizesinin depolandığı gizli dizisinin adını kopyalayın. Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.

6. Hüküm ve koşulları kabul etmek için onay kutusunu seçin.
7. **Yükle** 'yi seçin.
8. "Eklenti yükleme için başarıyla tetiklendi" yazılı bir ileti kutusu görüntülenir. **Tamam** 'ı seçin.

LCS ayarlama artık tamamlanmıştır. Sonraki adım, [senaryoları ayarlamak içindir](iot-scenario-setup.md).

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a>Eklentiyi kaldırma

1. Supply Chain Management'ta [senaryoları devre dışı bırakın](iot-scenario-setup.md#disable-a-scenario).
2. LCS'de, Supply Chain Management ortamınızın ayrıntılarına gidin.
3. **Ortam eklentileri** bölümüne kaydırın.
4. IoT Zekası eklentisi için **Kaldır** 'ı seçin.
