---
title: Dynamics 365 Commerce ve Microsoft Teams tümleştirmesini etkinleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce ve Microsoft Teams tümleştirmesinin nasıl etkinleştirileceğini açıklamaktadır.
author: gvrmohanreddy
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dfada577ab97fdb9912c22d2399529f934b25d54
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695746"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Dynamics 365 Commerce ve Microsoft Teams tümleştirmesini etkinleştirme

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce ve Microsoft Teams tümleştirmesinin nasıl etkinleştirileceğini açıklamaktadır.

Dynamics 365 Commerce'den gelen bilgilerle Teams'i sağlamak ve Teams ile satış noktası (POS) uygulaması arasındaki görev yönetimi özelliklerini eşlemek için Commerce Headquarters'da tümleştirme özelliklerini etkinleştirmeniz gerekir.

> [!NOTE]
> Teams tümleştirmesini etkinleştirdiğinizde, verilerinizi Teams ile paylaşmayı kabul edersiniz. Teams paylaşılan veriler Commerce verilerinizden farklı bir ülkede yer alabilir ve farklı uyumluluk standartlarına tabi olabilir. Daha fazla bilgi için bkz. [Microsoft Güven Merkezi](https://www.microsoft.com/trust-center). Microsoft Gizlilik ilkeleri hakkında bilgi için, bkz. [Microsoft gizlilik bildirimi](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>Teams tümleştirmesini etkinleştirme

Microsoft Teams ve Commerce tümleştirmesini etkinleştirmeden önce, Teams uygulamasını Azure portalında kiracınızla kaydettirmeniz gerekir.

Teams uygulamasını kiracınızla Azure portalında kaydetmek için aşağıdaki adımları izleyin.

1. Azure portalında kiracınız ile Teams uygulamasını kaydettirmek için [Hızlı Başlangıç: Microsoft Kimlik Platformunda bir uygulamayı kaydetme](/azure/active-directory/develop/quickstart-register-app) konusundaki adımları izleyin.
1. **Uygulama Kaydı** sekmesinde, önceki adımda oluşturduğunuz uygulamayı seçin. Sonra, **Kimlik doğrulama** sekmesinde **Platform ekle**'yi seçin.
1. İletişim kutusunda **Web**'i seçin. Sonra, **Yeniden yönlendirme URL'leri** alanında, **\<HQUrl\>/oauth** biçiminde bir URL girin. **\<HQUrl\>** öğesini Commerce Headquarters URL'niz (örneğin, `https://hxennugbjtweufmdeo385f47fadb6aa9a0aos.cloudax.int.dynamics.com/oauth`) ile değiştirin.
1. Kayıtlı uygulama için **Genel bakış** sayfasında **Uygulama (istemci) Kimliği** değerini kopyalayın. Sonraki aşamada, bu değeri Commerce Headquarters'da Teams tümleştirmesini etkinleştirmek için sağlamanız gerekecek.
1. Bir istemci gizli anahtarı eklemek için [İstemci gizli anahtarı ekleme](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret) konusundaki yönergeleri izleyin. Sonra, istemci için **Gizli anahtar değeri** değerini kopyalayın. Sonraki aşamada, bu değeri Commerce Headquarters'da Teams tümleştirmesini etkinleştirmek için sağlamanız gerekecek.
1. **API izinleri**'ni ve ardından **İzin Ekle**'yi seçin.
1. **API izinleri iste** iletişim kutusunda **Microsoft Graph**'ı seçin, **Temsilci izinleri**'ni seçin , **Grup**'u genişletin **Group.ReadWrite.All** öğesini ve ardından **İzin ekle**'yi seçin . 
1. **API izinleri iste** iletişim kutusunda **Microsoft Graph**'ı seçmek için **İzin ekle**'yi, **Uygulama izinleri**'ni seçin, **Grup**'u genişletin, **Group.ReadWrite.All** öğesini ve **İzin ekle**'yi seçin.
1. **API izinleri iste** iletişim kutusunda **İzin ekle**'yi seçin. **Kuruluşumun kullandığı API'lar** sekmesinde  **Microsoft Teams Retail Service**'i bulun ve seçin.
1. **Temsilci izinleri**'ni seçin, **TaskPublishing** öğesini genişletin, **TaskPublising.ReadWrite.All** öğesini ve ardından **İzin ekle**'yi seçin, Daha fazla bilgi için bkz. [Web API'sına erişmek için istemci uygulaması yapılandırma](/azure/active-directory/develop/quickstart-configure-app-access-web-apis).

Commerce Headquarters'da Teams tümleştirmesini etkinleştirmek için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Kanal kurulumu \> Microsoft Teams tümleştirme yapılandırması** na gidin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Microsoft Teams tümleştirmesini etkinleştir** seçeneğini **Evet** olarak ayarlayın.
1. **Uygulama kodu** alanında, Azure portalında Teams uygulamasına kaydolurken aldığınız **Uygulama (istemci) kimliği** değerini girin.
1. **Uygulama anahtarı** alanında, Azure portalında istemci gizli anahtarı eklerken aldığınız **Gizli anahtar değeri** değerini girin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

Aşağıdaki çizimde, Commerce Headquarters'da Teams tümleştirmesi yapılandırmasının bir örneği gösterilmektedir.

![Commerce Headquarters'da Teams tümleştirmesi yapılandırması.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>Teams tümleştirmesini devre dışı bırakma

Commerce Headquarters'da Microsoft Teams tümleştirmesini devre dışı bırakmak için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Kanal kurulumu \> Microsoft Teams tümleştirme yapılandırması** na gidin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
3. **Microsoft Teams tümleştirmesini etkinleştir** seçeneğini **Hayır** olarak ayarlayın.
4. **Uygulama kodu** ve **uygulama anahtarı** alanlarındaki değerleri temizleyin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

> [!NOTE]
> Commerce ile Teams tümleşmesini devre dışı bıraktıktan sonra, POS terminalleri Teams uygulamasından yayımlanan görevleri artık göstermez.

## <a name="additional-resources"></a>Ek kaynaklar

[Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bakış](commerce-teams-integration.md)

[Dynamics 365 Commerce'ten Microsoft Teams sağlama](provision-teams-from-commerce.md)

[Microsoft Teams ve Dynamics 365 Commerce POS arasında görev yönetimini eşitleme](synchronize-tasks-teams-pos.md)

[Microsoft Teams'de kullanıcı rollerini yönetme](manage-user-roles-teams.md)

[Microsoft Teams'de önceden var olan ekipler varsa mağazaları ve ekipleri eşleme](map-stores-existing-teams.md)

[Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi SSS](teams-integration-faq.md)
