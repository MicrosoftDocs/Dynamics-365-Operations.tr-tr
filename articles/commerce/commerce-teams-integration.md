---
title: Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bakış
description: Bu konu, Microsoft Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bir bakış sunar.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3b7872757815d4eec0393e8b1c8c6ff5467e9473
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842758"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a>Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bakış

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bir bakış sunar.

Dynamics 365 Commerce, müşterilerin ve çalışanlarının iki uygulama arasında görev yönetimini eşitleyerek Üretkenliği artırmaya yardımcı olmak amacıyla Teams ile tümleştiriliyor. Commerce ve Teams tümleştirmesinin sağladığı sorunsuz görev yönetimi, mağaza yöneticileri ve çalışanların bu iki uygulamanın herhangi birinden görev listeleri oluşturmalarına, birden fazla mağazaya görev atamalarına ve mağazalar arası görevlerin durumunu izlemelerine olanak sağlar.

Commerce ve Teams tümleştirmesi Commerce sürüm 10.0.18 itibarıyla kullanılabilir.

## <a name="key-features"></a>Önemli özellikler

Burada, Commerce ve Microsoft Teams tümleştirmesinin sağladığı önemli özelliklerden bazıları verilmektedir:

- Kurumsal yapı ve mağazalar, çalışanlar, izinler ve iş bağlamı ile ilgili bilgiler gibi Commerce'teki iyi tanımlanmış bilgilerden yararlanarak Teams'in sağlanması.
- Devam eden değişiklikleri (örneğin yeni mağaza ve yeni çalışanların eklenmesi) Commerce ve Teams arasında kolaylıkla eşitleyebilirsiniz, ancak kuruluş yapısı verilerinin ana kaynağı olarak Commerce'i tutun.
- Çalışanların, Mağaza yöneticilerinin, bölge yöneticilerinin ve iletişim yöneticilerinin her iki uygulamadan da görev yönetimi işlemesini sağlamak için Commerce ve Teams arasında görev yönetimini tümleştirin.

## <a name="prerequisites-for-using-integration-features"></a>Tümleştirme özelliklerini kullanmak için Önkoşullar

Microsoft Teams Tümleştirme özellikleri kullanmaya başlamadan önce aşağıdaki önkoşulların sağlanması gerekir:

- Microsoft 365 İş standart lisansı (Bu lisans Teams'i içerir.)
- Tüm mağaza yöneticileri ve çalışanları için Azure Active Directory (Azure AD) hesapları
- Azure AD Kimlik doğrulamasıyla yapılandırılan satış noktası (POS) sistemleri

## <a name="conceptual-architecture"></a>Kavramsal mimari

Aşağıdaki resim örnek olarak bir San Francisco mağazasını kullanarak Dynamics 365 Commerce ve Microsoft Teams tümleştirmesinin kavramsal mimarisini gösterir. Hem Teams hem de Commerce POS uygulaması Microsoft Planner'ı bir depo olarak kullanır, böylece Teams'den yayımlanan görevler POS uygulamasında görünür ve POS uygulamasında mağaza yöneticileri tarafından oluşturulan anlık görevler Teams'de de görünür, böylece uygulamalar arasında kesintisiz bir görev yönetimi deneyimi elde edilir.    

![Commerce ve Teams tümleştirmesinin mimarisi](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Dynamics 365 Commerce ve Microsoft Teams tümleştirmesini etkinleştirme](enable-teams-integration.md)

[Dynamics 365 Commerce'ten Microsoft Teams sağlama](provision-teams-from-commerce.md)

[Microsoft Teams ve Dynamics 365 Commerce POS arasında görev yönetimini eşitleme](synchronize-tasks-teams-pos.md)

[Microsoft Teams'de kullanıcı rollerini yönetme](manage-user-roles-teams.md)

[Microsoft Teams'de önceden var olan ekipler varsa mağazaları ve ekipleri eşleme](map-stores-existing-teams.md)

[Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi SSS](teams-integration-faq.md)
