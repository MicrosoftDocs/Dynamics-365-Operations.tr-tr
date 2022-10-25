---
title: Power Virtual Agents modülü ile Commerce Sohbeti
description: Bu makale, Dynamics 365 Commerce web siteleriyle Microsoft Power Virtual Agents'i entegre eden Power Virtual Agents modülüyle Commerce Sohbeti'ni açıklamaktadır.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-07
ms.openlocfilehash: 838990cb638479c9c90ba0e38794ecedd55e95b3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691106"
---
# <a name="commerce-chat-with-power-virtual-agents-module"></a>Power Virtual Agents modülü ile Commerce Sohbeti

[!include [banner](includes/banner.md)]

Bu makale, Dynamics 365 Commerce web siteleriyle Microsoft Power Virtual Agents'i entegre eden Power Virtual Agents modülüyle Commerce Sohbeti'ni açıklamaktadır.

Power Virtual Agents özellikli Commerce Sohbeti, Dynamics 365 e-ticaret müşterilerinin sorgularını işleyebilmeleri için Power Virtual Agents sohbet robotu yeteneklerini kullanmalarını sağlar. Dynamics 365 Commerce 10.0.30 sürümünde itibaren bu özellik, Commerce modül kütüphanesinin parçası olan Power Virtual Agents modüllü Commerce Sohbeti kullanılarak e-ticaret web sitelerine dahil edilebilir.

Power Virtual Agents özellikli Commerce Sohbeti, işletmelerin aşağıdaki hedeflere ulaşmasına yardımcı olur:

- Tutmayı iyileştirmek için tüketicilerle kişiselleştirilmiş etkileşimi artırın.
- Self servis sohbet botlarını tümleştirerek müşteri hizmetlerini artırın.
- Satışları artırmaya yardımcı olmak için müşteri memnuniyetini artırın.

> [!NOTE]
> Dynamics 365 Customer Service için Çok Yönlü Kanal ve Power Virtual Agents uygulamaları arasındaki farklılıklar hakkında bilgi edinmek için bkz. [Commerce sohbeti modüllerine genel bakış](/commerce-chat-modules-overview.md).

## <a name="prerequisites-for-using-power-virtual-agents"></a><a id="prereq"></a>Kullanım için önkoşullar Power Virtual Agents

Power Virtual Agents özellikli Commerce Sohbeti'ni kullanmak için öncelikle e-ticaret web siteniz için bir Power Virtual Agents sohbet robotu oluşturmanız gerekir. Talimatlar için bkz. [Güçlü bir sanal temsilci botu oluşturma](/power-virtual-agents/authoring-first-bot).

Sohbet robotunu yapılandırdıktan sonra, Commerce sohbeti deneyimini yapılandırmak için **Bot kimliği** ve **Kiracı kimliği** sohbet robotu parametrelerinin değerlerini kopyalamanız gerekir. Bu değerlerin nasıl kopyalanacağı hakkında bilgi edinmek için bkz. [Power Virtual Agents bot parametrelerinizi alma](/power-virtual-agents/publication-connect-bot-to-custom-application#retrieve-your-power-virtual-agents-bot-parameters).

## <a name="configure-your-e-commerce-site"></a>E-ticaret sitenizi yapılandırma 

E-ticaret siteniz için sohbet deneyimini uygulamanın önerilen yollarından biri Power Virtual Agents ile Commerce Sohbeti modülünü site sayfalarınızda kullanılan paylaşılan başlık parçasına eklemektir.

Sohbet modülünü Commerce site oluşturucuda sitenizin başlık parçasına eklemek için aşağıdaki adımları izleyin.

1. Siteniz için Commerce site oluşturucuda, **Parçalar**'a gidin.
1. **Yeni**'yi seçin.
1. **Parça seçin** iletişim kutusunda **Power Virtual Agents ile Commerce Sohbeti** modülünü seçin, parça için ad seçin ve **Tamam**'ı seçin.
1. Ana hat görünümünde **Msdyn365 pva sohbet bağlayıcısı** yuvasını seçin.
1. Sağdaki özellik bölmesinde şu adımları izleyin:

    1. **Bot Parametreleri** altında **Bot Framework Webchat Sohbeti CDN URL** alanında varsayılan değeri bırakın (örneğin `https://cdn.botframework.com/botframework-webchat/latest/webchat.js`).
    1. **Bot Framework Direct Line Kimlik Doğrulama URL**'si alanında, varsayılan değeri bırakın (örneğin `https://powerva.microsoft.com/api/botmanagement/v1/directline/directlinetoken`).
    1. **Bot kimliği** alanında [Power Virtual Agents kullanmak için ön koşullar](#prereq) bölümünde kopyaladığınız Power Virtual Agents **Bot kimliği** değerini girin.
    1. **Kiracı kimliği** alanında kopyaladığınız **Kiracı kimliği** değerini girin.

1. **Kaydet**'i seçin, parçayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **Parçalar**'a gidin ve siteniz için başlık parçasını açın.
1. **Varsayılan kapsayıcı** yuvasında, üç nokta (**...**) düğmesini seçin ve **Parça ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda daha önce oluşturduğunuz sohbet parçasını ve sonra **Tamam**'ı seçin.
1. **Kaydet**'i seçin, parçayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="proactive-chat-parameters"></a>Proaktif sohbet parametreleri

Proaktif sohbet yapılandırma parametrelerinin tam listesi için bkz. [Commerce sohbeti modülü proaktif sohbet parametreleri](chat-proactive-chat-parameters.md).

> [!NOTE]
> Şu anda Power Virtual Agents, Azure Active Directory B2C (Azure AD B2C) kimlik doğrulamasını desteklemiyor. Ürün kullanılabilirliğini almak veya diğer anonim API'lerle etkileşimde bulunmak için yalnızca anonim Retail Cloud Scale Unit (RCSU) çağrılarını destekler. Power Virtual Agents sohbet robotları yoluyla kimliği doğrulanmış API'lere yapılan çağrılar, açık müşteri oturum açma gerektirir.

## <a name="additional-resources"></a>Ek kaynaklar

[Commerce sohbeti özelliklerine genel bakış](commerce-chat-overview.md)

[Customer Service için Çok Yönlü Kanal modülüyle Commerce Sohbeti](commerce-chat-module.md)

[Commerce sohbet modülü proaktif sohbet parametreleri](chat-proactive-chat-parameters.md)
