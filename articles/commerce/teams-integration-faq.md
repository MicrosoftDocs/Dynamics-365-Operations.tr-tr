---
title: Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi SSS
description: Bu makale, Microsoft Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi ile ilgili sık sorulan soruların yanıtlarını sağlar.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 02f10e446349803ce5629fed0be4176f2df2be0c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869139"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a>Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi SSS

[!include [banner](includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi ile ilgili sık sorulan soruların yanıtlarını sağlar.

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a>Commerce'ten Teams sağlanırken mağazada ekibin sahibi kim olur? 

Özel kanal ekleme ve üye ekleme veya silme gibi işlemleri gerçekleştirebilmeleri için, tüm mağaza yöneticileri ilgili ekip grubuna sahip olarak otomatik olarak eklenir. 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a>"İletişim Yöneticisi" rolünü Commerce Headquarters'da bir çalışana nasıl atayabilirim? 

Microsoft Teams'deki iletişim yöneticileri, görev listeleri oluşturma ve yayımlama yeteneğine sahiptir. İletişim yöneticileri olması gereken kuruluş çalışanlarının Commerce Headquarters'da kendilerine atanmış "perakende Görev Yöneticisi" rolü olmalıdır.

Commerce Headquarters'da bir çalışana perakende görev yöneticisi rolü atamak için aşağıdaki adımları izleyin.

1. **Perakende ve Ticaret \> Personel \> Kullanıcılar**'a gidin.
1. Bir çalışan seçin.
1. **Kullanıcının rolleri** hızlı sekmesinde, **Rol ata**'ya tıklayın.
1. **Kullanıcıya rol ata** iletişim kutusunda, **perakende görev Yöneticisi** rolünü seçin ve **Tamam**'ı seçin.

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a>Belirli bir kuruluş hiyerarşisini Microsoft Teams'e yüklenmek üzere nasıl kullanılabilir hale getirebilirim?

Commerce Headquarters'da, her kuruluşun hiyerarşisi bir veya daha çok amaçla ilişkilendirilir. Microsoft Teams'e sağlamak istediğiniz hiyerarşinin aşağıdaki örnek görüntüde gösterildiği gibi, kendisiyle ilişkilendirilmiş **perakende Raporlama** amacı olduğundan emin olun. 

![Commerce Headquarters'da kuruluş hiyerarşisi amacı örneği.](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a>Mağaza çalışanlarının Azure Active Directory (Azure AD) kullanarak Commerce satış noktasında (POS) oturum açmasını nasıl sağlarım?

Commerce POS oturum açma deneyimini Azure AD kimlik doğrulamayı kullanacak şekilde konfigüre etme hakkında bilgi için bkz. [POS oturum açma için Azure Active Directory kimlik doğrulamayı etkinleştirme](aad-pos-logon.md).

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a>Kuruluşumda zaten Microsoft Teams'de oluşturulmuş ekipler varsa Commerce Headquarters'da depoları ve ilgili ekipleri nasıl eşlerim?

Öncedenvar olan ekipler varsa mağaza ve ekiplerin nasıl eşleneceği hakkında daha fazla bilgi için, [kuruluşunuzda Microsoft Teams'de önceden varolan ekipler varsa, depoları ve ilgili ekipleri eşleme](map-stores-existing-teams.md) konusuna bakın.

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a>Oturum depolama alanında depolanan Microsoft Graph API belirtecini nasıl temizlerim?

Bir satış noktasında Azure Active Directory (Azure AD) hesabıyla oturum açan bir kullanıcının, oturum depolama alanını temizlemek için POS oturumunu kapatması veya uygulamayı kapatması gerekir. 

> [!TIP]
> Önerilen en iyi uygulama, Terminal kullanılmadığında mağaza çalışanlarının her zaman POS terminalini kilitlemesi veya oturumu kapatmasıdır. 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a>Bir mağazanın mağaza yöneticileri yoksa ne olur?

Bir mağazanın yöneticileri yoksa, mağaza için veya Teams'de bir ekip grubu oluşturulmaz. 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a>Mağaza yöneticisi şirketten ayrıldığında ne olur?

Sahip rolüne sahip herkes Commerce Headquarters'da yeni bir mağaza yöneticisi ekleyebilir ve yeni yöneticinin Teams'de gerekli ayrıcalıklara sahip olmasını sağlayacak şekilde Teams'i yeniden temin edebilir. 

## <a name="additional-resources"></a>Ek kaynaklar

[Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bakış](commerce-teams-integration.md)

[Dynamics 365 Commerce ve Microsoft Teams tümleştirmesini etkinleştirme](enable-teams-integration.md)

[Dynamics 365 Commerce'ten Microsoft Teams sağlama](provision-teams-from-commerce.md)

[Microsoft Teams ve Dynamics 365 Commerce POS arasında görev yönetimini eşitleme](synchronize-tasks-teams-pos.md)

[Microsoft Teams'de kullanıcı rollerini yönetme](manage-user-roles-teams.md)

[Microsoft Teams'de önceden var olan ekipler varsa mağazaları ve ekipleri eşleme](map-stores-existing-teams.md)
