---
title: Microsoft Teams ve Dynamics 365 Commerce POS arasında görev yönetimini eşitleme
description: Bu makale görev yönetiminin Microsoft Teams ile Dynamics 365 Commerce Satış noktası (POS) arasında nasıl eşitleneceğini açıklar.
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f339ae031f11ad850dab47f84bc9823cf6776e74
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746110"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a>Microsoft Teams ve Dynamics 365 Commerce POS arasında görev yönetimini eşitleme

[!include [banner](includes/banner.md)]

Bu makale görev yönetiminin Microsoft Teams ile Dynamics 365 Commerce Satış noktası (POS) arasında nasıl eşitleneceğini açıklar.

Teams tümleştirmesinin başlıca amaçlarından biri, POS uygulaması ve Teams arasında görev yönetiminin eşitlenmesini etkinleştirmektir. Böylece, mağaza çalışanları, görevleri yönetmek için POS uygulamasını veya Teams'i kullanabilir ve uygulamalarda geçiş yapmak zorunda kalmaz.

Planner Teams'deki görevler için bir depo olarak kullanıldığı için, Teams ile Dynamics 365 Commerce arasında bir bağlantı olmalıdır. Bu bağlantı, belirli bir mağaza ekibi için özel bir plan kodu kullanılarak kurulur.

Aşağıdaki yordamlarda, POS ve Teams uygulamaları arasında görev yönetimi eşitlemesinin nasıl ayarlanacağı gösterilmektedir.

## <a name="link-pos-and-teams-for-task-management"></a>Görev yönetimi için POS ve Teams'i bağlama

POS ve Microsoft Teams uygulamalarını Commerce Headquarters'da görev yönetimi için bağlamak amacıyla aşağıdaki adımları izleyin.

> [!NOTE]
> Görev yönetimini Teams ile tümleştirmeyi denemeden önce, [Dynamics 365 Commerce ile Microsoft Teams tümleştirmesini](enable-teams-integration.md) etkinleştirdiğinizden emin olun. 

1. **Retail ve Commerce \> Veri yönetimi \> Microsoft Teams ile görev tümleştirme** bölümüne gidin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Görev Yönetimi tümleştirmesini etkinleştir** seçeneğini **Evet** olarak ayarlayın.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Eylem Panosundan **Görevi yönetimini ayarla**'yı seçin. **Teams sağlama** adlı bir toplu işin oluşturulmakta olduğunu gösteren bir bildirim almalısınız.
1. **Sistem Yönetimi \> sorgular \> toplu işler**'e gidin ve **Teams sağlama** açıklamasına sahip en son işi bulun. Bu işin çalışması bitene kadar bekleyin.
1. Plan kodunu ve mağaza referanslarını Retail Server'a yayımlamak için **CDX İş 1070**'i çalıştırın.

## <a name="publish-a-test-task-list-in-teams"></a>Teams'de bir test görev listesi yayımlama

Aşağıdaki prosedür, mağaza ekiplerinizin Commerce ile Microsoft Teams görev yönetimi tümleştirmesini ilk kez kullanmakta olduğunu varsayar.

Teams'de bir test görev listesi yayımlamak için, aşağıdaki adımları izleyin.

1. Teams'de iletişim yöneticisi olarak oturum açın. Genel olarak, iletişim yöneticileri Commerce'te **bölge yöneticisi** rolüne sahip kullanıcılardır.
1. Sol gezinti bölmesinde, **Planner'daki Görevler**'i seçin.
1. **Yayımlanan listeler** sekmesinde, sol alt tarafta **yeni liste**'yi seçin ve yeni listeyi **Test görev listesi** olarak adlandırın.
1. **Oluştur**'u seçin. Yeni liste **Taslaklar** altında görünür.
1. **Görev başlığı** altında, ilk göreve,**Teams tümleştirmesi testi** başlığını verin. **GİR**'ı seçin.
1. **Taslaklar** listesinde, görev listesini seçin. Ardından, sağ üst köşede  **yayımla** 'yı seçin.
1. **Kime yayımlanacağını seç** iletişim kutusunda, test görev listesini alması gereken ekipleri seçin.
1. Yayın planınızı gözden geçirmek için **ileri**'yi seçin. Değişiklik yapmanız gerekiyorsa,  **geri**'yi seçin. 
1. **Devam etmek için Onayla**'yı, ardından da **Yayınla**'yı seçin.
1. Yayımlama tamamlandıktan sonra, **yayımlanan listeler** sekmesinin başındaki bir ileti, Görev listenizin başarıyla teslim edilip edilmediğini belirtir.

Daha fazla bilgi için, bkz. [Kuruluşunuzda iş oluşturmak ve izlemek için görev listelerini yayımlama](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).

> [!NOTE]
> Görev listesi Teams'de başarıyla yayımlandıktan sonra, görevler POS'ta görüntülenir. Bundan sonra POS yöneticilerinin ve kasiyerlerin POS'ta Azure AD oturum açma özelliğini açması gerekir. Daha fazla bilgi için, [POS oturumu açmak için Azure Active Directory kimlik doğrulamasını etkinleştirme](aad-pos-logon.md) makalesine bakın. 

## <a name="additional-resources"></a>Ek kaynaklar

[Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bakış](commerce-teams-integration.md)

[Dynamics 365 Commerce ve Microsoft Teams tümleştirmesini etkinleştirme](enable-teams-integration.md)

[Dynamics 365 Commerce'ten Microsoft Teams sağlama](provision-teams-from-commerce.md)

[Microsoft Teams'de kullanıcı rollerini yönetme](manage-user-roles-teams.md)

[Microsoft Teams'de önceden var olan ekipler varsa mağazaları ve ekipleri eşleme](map-stores-existing-teams.md)

[Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi SSS](teams-integration-faq.md)
