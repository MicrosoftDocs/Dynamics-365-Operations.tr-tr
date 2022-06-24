---
title: LCS'de IoT Zekası eklentisini yükleme
description: Bu makale, Microsoft Dynamics LifeCycle Services (LCS) Içindeki IoT Zekası eklentisinin nasıl yükleneceğini açıklamaktadır.
author: johanhoffmann
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 52fe4c4a79378aca5f1e64c8b3f4fa85199c9911
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887500"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>LCS'de IoT Zekası eklentisini yükleme

[!include [banner](../../includes/banner.md)]

Bu makale, Microsoft Dynamics LifeCycle Services (LCS) Içindeki IoT Zekası eklentisinin nasıl yükleneceğini açıklamaktadır. Eklentilerin tanıtım/deneme ortamına yüklenemeyeceğini unutmayın. Eklentiyi yükleyebilmek için önce [Azure kaynaklarını oluşturmanız gerekir](iot-azure-setup.md).

IoT yönetim kodunu herhangi bir kod yazmadan ayarlayabilir ve konfigüre edebilirsiniz. Temel adımlar şunlardır.

1. [Azure kaynaklarını ayarla](iot-azure-setup.md) – bir IoT Merkezi, Redis Cache ve Supply Chain Management'tan erişilebilen bir Key Vault oluşturun.
2. [IoT Hub'ı için ileti şeması formatları](iot-schema-format.md) – Aygıtları IoT Hub'a göndermek üzere yapılandırın ve JavaScript Nesne Gösterimi (JSON) ileti biçimi tanımlayın.
3. Özellik Yönetiminde, IoT yönetim bilgileri özellik bayrağını etkinleştirin.
4. Microsoft Dynamics Lifecycle Services (LCS) içindeki IoT yönetim bilgileri eklentisini yükleyin – Eklentiyi, LCS'ye yükleyin ve Azure gizli kod dizelerini yapılandırın (bu makalede açıklandığı şekilde).
5. [Ölçümleri ayarla](iot-metrics-setup.md) – Supply Chain Management'ta ölçümleri ayarlayın.
6. [Senaryo kurulumu](iot-scenario-setup.md) -Supply Chain Management'ta senaryolar ayarlayın.

## <a name="set-up-the-lcs-environment"></a>LCS ortamını ayarlama

1. LCS'yi açın ve Microsoft Dynamics 365 Supply Chain Management ortamınıza gidin.
2. **Ortam eklentileri** bölümüne kaydırın.
3. Ortam için etkinleştirilmiş eklentilerin listesini göstermek için **Yeni eklenti yükle**'yi seçin.
4. **Yüklemek için bir eklenti seçin** iletişim kutusunda **IoT Zekası**'nı seçin.
5. **Eklenti ayarlama** iletişim kutusunda IoT Hub'ın ve Redis önbelleğinin ayrıntılarını belirtin. [Azure kaynakları oluştur](iot-azure-setup.md) altında oluşturduğunuz anahtar kasasında gerekli değerleri bulabilirsiniz.

    + **Kiracı kimliği:** Azure portalında, anahtar kasasına gidin ve sonra sol gezinti bölmesinde **Genel bakış**'ı seçip **Dizin kimliği** değerini kopyalayın. Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.
    + **IoT Olay Hub'ı ile uyumlu bitiş noktası Anahtar Kasası URI'si:** Anahtar kasasına gidin ve sol gezinti bölmesinde **Genel bakış**'ı seçip **DNS adı** değerini kopyalayın. Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.
    + **IoT Olayı Hub'ı ile uyumlu bitiş noktası gizli dizi adı:** Anahtar kasasına gidin ve sol gezinti bölmesinde, **Gizli diziler**'i seçip IoT Hub'ın olay hub'ı bağlantı dizesinin depolandığı gizli dizisinin adını kopyalayın. Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.
    + **Redis önbelleği anahtar kasası URI'si:** Anahtar kasasına gidin ve sol gezinti bölmesinde **Genel bakış**'ı seçip **DNS adı** değerini kopyalayın. Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.
    + **Redis önbelleği uç nokta gizli dizi adı:** Anahtar kasasına gidin ve sol gezinti bölmesinde, **Gizli diziler**'i seçip Redis önbelleği bağlantı dizesinin depolandığı gizli dizisinin adını kopyalayın. Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.

6. Hüküm ve koşulları kabul etmek için onay kutusunu seçin.
7. **Yükle**'yi seçin.
8. "Eklenti yükleme için başarıyla tetiklendi" yazılı bir ileti kutusu görüntülenir. **Tamam**'ı seçin.

LCS ayarlama artık tamamlanmıştır. Sonraki adım, [senaryoları ayarlamak içindir](iot-scenario-setup.md).

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a>Eklentiyi kaldırma

1. Supply Chain Management'ta [senaryoları devre dışı bırakın](iot-scenario-setup.md#disable-a-scenario).
2. LCS'de, Supply Chain Management ortamınızın ayrıntılarına gidin.
3. **Ortam eklentileri** bölümüne kaydırın.
4. IoT Zekası eklentisi için **Kaldır**'ı seçin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]