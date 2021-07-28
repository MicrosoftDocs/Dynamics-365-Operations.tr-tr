---
title: Dynamics 365 Commerce'ten Microsoft Teams sağlama
description: Bu konu, Dynamics 365 Commerce'deki organizasyon verilerini kullanarak nasıl Microsoft Teams sağlanacağını açıklar.
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
ms.openlocfilehash: 39dabeb8bacc4ebc3376f53f15c7fb292c8d301c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352120"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a>Dynamics 365 Commerce'ten Microsoft Teams sağlama

[!include [banner](includes/banner.md)]

Bu konu, Dynamics 365 Commerce'deki organizasyon verilerini kullanarak nasıl Microsoft Teams sağlanacağını açıklar.

Dynamics 365 Commerce henüz perakende mağazalarınız için Teams'i ayarlamadıysanız, Teams sağlamak için kolay bir yol sunar. Teams'de kullanmak istediğiniz Commerce'teki iyi tanımlanmış bilgilerden yararlanarak, mağaza çalışanlarınızın Teams'i kullanmaya başlaması konusunda yardımcı olabilirsiniz. Bu bilgiler, organizasyon hiyerarşisi, mağaza adları, çalışan bilgileri ve Azure Active Directory (Azure AD) hesaplarını içerir. 

Teams sağlama işleminin iki ana adımı vardır:

1. Teams'de her perakende mağazası için bir ekip oluşturun ve mağaza çalışanlarını uygun ekibin üyeleri olarak ekleyin. Bir çalışan birden fazla perakende mağazası ile ilişkilendirilmişse, ekip üyeliği bu olguyu yansıtır. Teams'den görev yayımlamaya yardımcı olmak üzere, bölgesel yöneticilerini üye olarak içeren bir iletişim ekibi oluşturulur.
1. Organizasyon hiyerarşinizi Commerce'ten Teams'e yükleyin.

## <a name="provision-teams-in-commerce-headquarters"></a>Commerce Headquarters'da Teams'i sağlama

Microsoft Teams'i sağlamadan önce, aşağıdaki görevleri tamamlayın:

- Tüm bölgesel yöneticilerin iletişim yöneticileri yapıldığını onaylayın.
- Her mağaza yöneticisinin ve çalışanın Azure hesabının Commerce Headquarters'da o yöneticinin veya çalışanın çalışan kaydıyla ilişkilendirildiğini onaylayın.

Commerce Headquarters'da Teams'i sağlamak için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Kanal kurulumu \> Microsoft Teams tümleştirme yapılandırması** na gidin.
1. Eylem bölmesinde, **Teams sağla**'yı seçin. **Teams sağlama** adlı bir toplu iş oluşturulur.
1. **Sistem Yönetimi \> sorgular \> toplu işler**'e gidin ve **Teams sağlama** açıklamasına sahip en son işi bulun. Bu işin çalışması bitene kadar bekleyin.

> [!TIP]
> Bölgesel yöneticileriniz, mağaza yöneticileri ve mağaza arkadaşlarınız bir Teams lisansıyla ilişkilendirilmediği takdirde, aşağıdaki hata iletisini alabilirsiniz: "Kullanıcı için appliable SKU kategorileri alınamadı." Sorunu düzeltmek için, Eylem bölmesinde, **Teams ve üyeleri Eşitle**'yi seçin.

<!-- ![Dynamics 365 Commerce - Teams integration configuration.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a>Teams Yönetim merkezinde Teams sağlamayı doğrulama

Microsoft Teams Yönetim Merkezi'nde Microsoft Teams sağlamayı doğrulamak için aşağıdaki adımları izleyin.
    
1. [Teams yönetim merkezine gidin](https://admin.teams.microsoft.com/) ve e-ticaret kiracınızın Yöneticisi olarak oturum açın.
1. Sol gezinti bölmesinde, genişletmek için **Teams**'i seçin ve sonra **Ekipleri yönet**'i seçin.
1. Her bir Commerce Retail Store için bir ekibin oluşturulmuş olduğunu doğrulayın.
1. Bir ekip seçin ve mağaza çalışanlarının üye olarak eklendiğini doğrulayın.
1. Sol gezinti bölmesinde, **kullanıcıları** seçin ve tüm mağazalardaki tüm mağaza çalışanlarının Kullanıcı olarak eklendiğini doğrulayın.

Aşağıdaki çizimde, Teams Yönetim merkezinde bulunan **Ekipleri Yönet** sayfasının bir örneği gösterilmektedir.

![Teams Yönetim Merkezi'ndeki ekipleri Yönet sayfası örneği.](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a>Commerce Organizasyon hiyerarşinizi Teams'e yükleme
    
Commerce organizasyon hiyerarşisi, aynı hiyerarşi yapısını kullanan tüm ya da seçilen mağazalara görev yayınlamak için Microsoft Teams'de kullanılabilir.

Commerce organizasyon hiyerarşisini Teams'e yüklemek için aşağıdaki adımları izleyin.
    
1. Commerce headquarters'da **Retail ve Commerce \> Kanal ayarı \> Microsoft Teams Tümleştirme Yapılandırması**'na gidin.
1. Organizasyon hiyerarşisinin bir virgülle ayrılmış değerler (CSV) dosyasını indirmek için, **hedef hiyerarşiyi yükle**'yi seçin ve **bölgeye göre perakende mağazalardan** birini seçin.
1. Microsoft Teams PowerShell modülünü [Microsoft Teams PowerShell modülünü yükleme](/microsoftteams/teams-powershell-install) bölümündeki adımları kullanarak yükleyin.
1. Teams PowerShell penceresinde sorulduğunda, Azure AD kiracınıza ait yönetici hesabını kullanarak oturum açın.
1. Hedefleme hiyerarşisinin CSV dosyasını yüklemek için [takım hedefleme hiyerarşinizi ayarlama](/microsoftteams/set-up-your-team-hierarchy) adımlarını izleyin.

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a>Kuruluş hiyerarşisinin Teams'e yüklenmiş olduğunu doğrulayın

Kuruluş hiyerarşisinin Microsoft Teams'e yüklenmiş olduğunu doğrulamak için şu adımları izleyin.

1. Teams'de iletişim yöneticisi olarak oturum açın.
1. Sol gezinti bölmesinde, **Planner'daki Görevler**'i seçin.
1. **Yayınlanan listeler** sekmesinde, sözde görevi olan yeni bir liste oluşturun.
1. **Yayımla**'yı seçin. Aşağıdaki çizimdeki örnekte gösterildiği gibi, kuruluş hiyerarşisi **Kime yayımlanacağını seç** iletişim kutusunda görünür.

![Kime yayımlanacağını seç iletişim kutusunda kuruluş hiyerarşisi örneği.](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bakış](commerce-teams-integration.md)

[Dynamics 365 Commerce ve Microsoft Teams tümleştirmesini etkinleştirme](enable-teams-integration.md)

[Microsoft Teams ve Dynamics 365 Commerce POS arasında görev yönetimini eşitleme](synchronize-tasks-teams-pos.md)

[Microsoft Teams'de kullanıcı rollerini yönetme](manage-user-roles-teams.md)

[Microsoft Teams'de önceden var olan ekipler varsa mağazaları ve ekipleri eşleme](map-stores-existing-teams.md)

[Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi SSS](teams-integration-faq.md)