---
title: IoT Zekası için Azure kaynaklarını ayarlama
description: Bu konu, IoT Zekası için gerekli olan Microsoft Azure kaynaklarının nasıl oluşturulacağını ve yapılandırılacağını açıklamaktadır.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1277d2ab8bb1f2925874f7469250e164f6bde62d
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439612"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a>IoT Zekası için Azure kaynaklarını ayarlama

[!include [banner](../../includes/banner.md)]

Bu konu, IoT Zekası için gerekli olan Microsoft Azure kaynaklarının nasıl oluşturulacağını ve yapılandırılacağını açıklamaktadır.

## <a name="create-azure-resources"></a>Azure kaynakları oluşturma

Bir IoT hub'ı, Redis önbelleği ve Microsoft Dynamics 365 Supply Chain Management tarafından erişilebilen bir anahtar kasası oluşturmak için bu adımları izleyin.

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a>Microsoft Dynamics ERP Mikro Hizmetleri birinci taraf uygulama kimliğinin kiracınızda olduğunu doğrulama

Microsoft Dynamics ERP Mikro Hizmetleri birinci taraf uygulama kimliğinin kiracınızda olduğunu doğrulamak için aşağıdaki adımları izleyin.

1. Azure portalında <https://portal.azure.com> adresinden oturum açın.
2. **Azure Active Directory** gidin.
3. **Kurumsal uygulamalar**'a gidin.
4. **Uygulama türü** alanında, **Microsoft uygulamaları**'nı seçin.
5. Arama alanına, **Microsoft Dynamics ERP Mikro Hizmetleri**'ni girin.
6. **Microsoft Dynamics ERP Mikro Hizmetleri**'nin listede olduğunu doğrulayın. Diğer uygulamaların benzer adları vardır. Bu nedenle, doğru uygulamayı bulmaya özen gösterin. Uygulama kimliği şudur: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

    Uygulama listede değilse kiracınıza eklemeniz gerekir:

    1. Azure portalının araç çubuğunda, Azure Cloud Shell'i açmak için düğmeyi seçin.
    2. **Install-Module AzureAD** komutunu çalıştırın. Modülü yüklemek için **Y** değerini girin.
    3. Modülün yüklü olduğunu doğrulamak için **Get-InstalledModule -Name "AzureAD"** komutunu çalıştırın.
    4. Doğrulamayı çalıştırmak için **Connect-AzureAD -Confirm** komutunu çalıştırın.
    5. **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2** komutunu çalıştırın.

    Uygulama kimliğinin kiracınızda olduğunu doğrulamak için şimdi 1'den 6'ya kadar olan adımları tekrarlayabilirsiniz.

### <a name="create-a-key-vault-resource"></a>Anahtar kasası kaynağı oluşturma

Anahtar kasası kaynağı oluşturmak için aşağıdaki adımları izleyin.

1. Azure portalında, bir kaynak grubu oluşturun veya bir kaynak grubuna gidin.
2. **Ekle**'yi seçin.
3. **Yeni** sayfasındaki arama alanına **Anahtar kasası** yazın. Ardından **Oluştur**'u seçin.
4. **Anahtar kasası oluştur** sayfasında, **Anahtar kasası adı** alanına bir ad girin.
5. Varsayılan değerleri gözden geçirin ve sonra **Gözden geçir + oluştur**'u seçin.
6. **Oluştur**'u seçin.

Anahtar kasası arka planda oluşturulur.

### <a name="create-an-iot-hub-resource"></a>IoT hub kaynağı oluşturma

Bir IoT hub kaynağı oluşturmak için aşağıdaki adımları izleyin.

1. Kaynak grubu oluşturun veya bir kaynak grubuna gidin.
2. **Ekle**'yi seçin.
3. **Yeni** sayfasındaki arama alanına **IoT Hub** yazın. Ardından **Oluştur**'u seçin.
4. **IoT hub adı** alanında, bir ad girin.
5. Varsayılan değerleri gözden geçirin ve sonra **Gözden geçir + oluştur**'u seçin.
6. **Oluştur**'u seçin.

IoT hub arka planda oluşturulur.

> [!NOTE]
> Her ortam için yalnızca bir IoT hub kaynağı oluşturmanızı öneririz.

### <a name="create-a-redis-cache-resource"></a>Redis önbelleği kaynağı oluşturma

Bir Redis önbelleği kaynağı oluşturmak için aşağıdaki adımları izleyin.

1. Kaynak grubu oluşturun veya bir kaynak grubuna gidin.
2. **Ekle**'yi seçin.
3. **Yeni** sayfasındaki arama alanına **Redis için Azure Önbelleği** yazın. Ardından **Oluştur**'u seçin.
4. **DNS adı** alanına, bir ad girin.
5. Varsayılan değerleri gözden geçirin ve sonra **Oluştur**'u seçin.

Redis önbelleği arka planda oluşturulur.

> [!NOTE]
> Her ortam için yalnızca bir Redis önbelleği oluşturmanızı öneririz.

Tüm kaynaklar artık oluşturulmuştur.

## <a name="configure-the-azure-resources"></a>Azure kaynaklarını yapılandırma

### <a name="configure-the-iot-hub"></a>IoT hub'ı yapılandırma

IoT hub'ı yapılandırmak için şu adımları izleyin.

1. Kaynaklarınızda IoT hub kaynağını seçin.
2. Sol gezinti bölmesinde, **Yerleşik uç noktalar**'ı seçin.
3. **Tüketici grupları** altında, aşağıdaki tüketici gruplarını yapıştırın. Bu tüketici grupları, hazır senaryolara karşılık gelir.

    + microsoft.dynamics.iotintelligence-1
    + microsoft.dynamics.iotintelligence-2
    + microsoft.dynamics.iotintelligence-3

### <a name="configure-the-key-vault"></a>Anahtar kasasını yapılandırma

Anahtar kasasını yapılandırmak için şu adımları izleyin.

1. Kaynaklarınızda anahtar kasası kaynağını seçin.
2. Sol gezinti bölmesinde **Erişim ilkeleri**'ni seçin.
3. **Erişim ilkesi ekle**'yi seçin.
4. **Erişim ilkesi ekle** sayfasındaki **Gizli izinler** alanında, **Alma** ve **Liste**'yi seçin.
5. **Birincil olan seç**'i tıklayın.
6. **Birincil** iletişim kutusunda, **Microsoft Dynamics ERP Mikro Hizmetleri**'ni arayın ve seçin. Sonra, **Seç** öğesini seçin.
7. **Ekle**'yi seçin.
8. **Kaydet**'i seçin.

Uygulama şimdi anahtar kasasındaki gizli dizilere erişebilir.

### <a name="save-the-iot-hub-connection-string-secret"></a>IoT hub bağlantı dizesi gizli dizisini kaydetme

IoT hub bağlantı dizesinin gizli dizisini kaydetmek için aşağıdaki adımları izleyin.

1. Kaynaklarınızda IoT hub kaynağını seçin.
2. Sol gezinti bölmesinde, **Yerleşik uç noktalar**'ı seçin.
3. **Olay Hub'ı ile uyumlu uç nokta** alanındaki değeri kopyalayın.
4. Anahtar kasası kaynağına gidin.
5. Sol gezinti bölmesinde **Gizli diziler**'i seçin.
6. **Oluştur/İçe aktar** seçeneğini belirleyin.
7. **Ad** alanına, bir ad girin.
8. **Değer** alanında, önceden kopyaladığınız uç nokta değerini yapıştırın.
9. **Oluştur**'u seçin.

### <a name="save-the-redis-cache-connection-string-secret"></a>Redis önbelleği bağlantı dizesi gizli dizisini kaydetme

Redis önbelleği bağlantı dizesinin gizli dizisini kaydetmek için aşağıdaki adımları izleyin.

1. Kaynaklarınızda Redis önbelleği kaynağını seçin.
2. **Erişim anahtarları**'nı seçin.
3. **Birincil bağlantı dizesi** alanındaki değeri kopyalayın.
4. Anahtar kasası kaynağına gidin.
5. Sol gezinti bölmesinde **Gizli diziler**'i seçin.
6. **Oluştur/İçe aktar** seçeneğini belirleyin.
7. **Ad** alanına, bir ad girin.
8. **Değer** alanında, önceden kopyaladığınız bağlantı dizesini yapıştırın.
9. **Oluştur**'u seçin.

> [!NOTE]
> Bağlantı dizelerinden birini her güncelleştirdiğinizde gizli dizi değerlerini de güncelleştirmeniz gerekir.

Gerekli Azure kaynaklarını sağlamayı şimdi bitirdiniz. Sonraki adım, [Microsoft Dynamics LifeCycle Services'daki (LCS) IoT Zekası eklentisinin yüklenmesi](iot-lcs-setup.md) ile ilgilidir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]