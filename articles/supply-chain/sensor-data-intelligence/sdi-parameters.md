---
title: Sensor Data Intelligence parametreleri
description: Bu makalede, Sensör Veri Yönetim Bilgileri parametreleri sayfasında bulunan yapılandırma ayarları hakkında bilgi sağlanmaktadır.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreServiceParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 5240537e3a6526ceb35253b9e68f46b1753c6a37
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689386"
---
# <a name="sensor-data-intelligence-parameters"></a>Sensor Data Intelligence parametreleri

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

**Sensör Veri Yönetim Bilgileri parametreleri** sayfası, özelliği yapılandırmak için kullanabileceğiniz birkaç ayar sağlar. Bu ayarlar, Azure bağlantı parametrelerini ve algılayıcı ölçümlerine yanıt olarak kullanıcılara gönderilen uyarı iletilerinin ömrü için bir parametre içerir.

## <a name="read-and-change-connection-details-for-your-azure-iot-solution"></a>Azure IoT çözümünüz için bağlantı ayrıntılarını okuma ve değiştirme

Genellikle, Azure IoT çözümünüzü ayarlar ve bu çözümü her iki prosedürde de size yol gösterecek olan **Azure kaynaklarını dağıtma ve bağlama** sayfasından Microsoft Dynamics 365 Supply Chain Management'e bağlanırsınız. (Daha fazla bilgi için bkz. [Azure'da IoT çözümü dağıtma](sdi-deploy-iot-solution-on-azure.md).) Ayrıca, aşağıdaki adımları izleyerek bağlantı ayrıntılarını istediğiniz zaman Supply Chain Management'ta görüntüleyebilir ve düzenleyebilirsiniz.

1. **Sistem yönetimi \> Kurulum \> Sensör Veri Yönetim Bilgileri \> Sensör Veri Yönetim Bilgileri parametreleri**'ne gidin.
1. **Zaman serisi** sekmesindeki **Redis ölçüm deposu bağlantı dizesi** alanına, bağlanmak istediğiniz Azure IoT çözümü için **birincil bağlantı dizesi (StackExchange.Redis)** değerini girin. Bu değeri bulma hakkında daha fazla bilgi için bkz. [Azure'da IoT çözümü dağıtma](sdi-deploy-iot-solution-on-azure.md).
1. **Tümleştirmeler** sekmesindeki **Azure AD uygulama istemci kimliği** alanına, bağlanmak istediğiniz Azure IoT çözümü için **İstemci Kimliği** değerini girin. Bu değeri bulma hakkında daha fazla bilgi için bkz. [Azure'da IoT çözümü dağıtma](sdi-deploy-iot-solution-on-azure.md).

## <a name="set-the-lifetime-of-alert-messages"></a>Uyarı mesajlarının kullanım süresini ayarlama

Sensör Veri Yönetim Bilgileri, kullanıcının dikkatini gerektiren bir durumu her algıladığında, ilgili kullanıcıya bir bildirim gönderir. Bu bildirimlerin sistemde birikmesini önlemek için birkaç gün sonra süreleri dolacak şekilde ayarlamanız gerekir.

1. **Sistem yönetimi \> Kurulum \> Sensör Veri Yönetim Bilgileri \> Sensör Veri Yönetim Bilgileri parametreleri**'ne gidin.
1. **Bildirimler** sekmesindeki **Yayınlanmaya kalan bildirim gün sayısı** alanına bildirimin tutulacağı gün sayısını girin. Belirtilen süre geçtikten sonra bildirim silinir.
