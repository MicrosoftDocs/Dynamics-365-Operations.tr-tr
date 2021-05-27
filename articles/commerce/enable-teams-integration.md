---
title: Dynamics 365 Commerce ve Microsoft Teams tümleştirmesini etkinleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce ve Microsoft Teams tümleştirmesinin nasıl etkinleştirileceğini açıklamaktadır.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eb0b8b419b302fbd0bc107bca22f8b26774ba3c7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019847"
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
1. Kayıtlı uygulama için **genel bakış** sayfasından **uygulama (istemci) Kimliği** değerini kopyalayın. Bu değeri Commerce Headquarters'da Teams tümleştirmesini etkinleştirmek için kullanacaksınız.
1. Adım 1'de [bir sertifika eklediğinizde](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) girilen sertifika değerini kopyalayın. Sertifika, ortak anahtar veya uygulama anahtarı olarak da bilinir. Bu değeri Commerce Headquarters'da Teams tümleştirmesini etkinleştirmek için kullanacaksınız.

Commerce Headquarters'da Teams tümleştirmesini etkinleştirmek için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Kanal kurulumu \> Microsoft Teams tümleştirme yapılandırması** na gidin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Microsoft Teams tümleştirmesini etkinleştir** seçeneğini **Evet** olarak ayarlayın.
1. **Uygulama kodu** ve **uygulama anahtarı** alanlarına, Azure portalında Teams uygulamasını kaydettirdiğinizde elde ettiğiniz değerleri girin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

Aşağıdaki çizimde, Commerce Headquarters'da Teams tümleştirmesi yapılandırmasının bir örneği gösterilmektedir.

![Commerce Headquarters'da Teams tümleştirmesi yapılandırması](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

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