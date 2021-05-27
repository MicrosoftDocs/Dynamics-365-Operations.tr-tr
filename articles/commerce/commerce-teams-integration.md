---
title: Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bakış
description: Bu konu, Microsoft Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bir bakış sunar.
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
ms.openlocfilehash: c22af9bf76818dd682b4147c3677cd1715e4cbf8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022001"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a><span data-ttu-id="d5331-103">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bakış</span><span class="sxs-lookup"><span data-stu-id="d5331-103">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d5331-104">Bu konu, Microsoft Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bir bakış sunar.</span><span class="sxs-lookup"><span data-stu-id="d5331-104">This topic presents an overview of Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="d5331-105">Dynamics 365 Commerce, müşterilerin ve çalışanlarının iki uygulama arasında görev yönetimini eşitleyerek Üretkenliği artırmaya yardımcı olmak amacıyla Teams ile tümleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="d5331-105">Dynamics 365 Commerce is integrating with Teams to help customers and their employees improve productivity by synchronizing task management between the two applications.</span></span> <span data-ttu-id="d5331-106">Commerce ve Teams tümleştirmesinin sağladığı sorunsuz görev yönetimi, mağaza yöneticileri ve çalışanların bu iki uygulamanın herhangi birinden görev listeleri oluşturmalarına, birden fazla mağazaya görev atamalarına ve mağazalar arası görevlerin durumunu izlemelerine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="d5331-106">The seamless task management that Commerce and Teams integration provides lets store managers and employees create task lists, assign tasks to multiple stores, and track the status of tasks across stores, from either application.</span></span>

<span data-ttu-id="d5331-107">Commerce ve Teams tümleştirmesi Commerce sürüm 10.0.18 itibarıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d5331-107">Commerce and Teams integration is available as of the Commerce version 10.0.18 release.</span></span>

## <a name="key-features"></a><span data-ttu-id="d5331-108">Önemli özellikler</span><span class="sxs-lookup"><span data-stu-id="d5331-108">Key features</span></span>

<span data-ttu-id="d5331-109">Burada, Commerce ve Microsoft Teams tümleştirmesinin sağladığı önemli özelliklerden bazıları verilmektedir:</span><span class="sxs-lookup"><span data-stu-id="d5331-109">Here are some of the key features that the Commerce and Microsoft Teams integration provides:</span></span>

- <span data-ttu-id="d5331-110">Kurumsal yapı ve mağazalar, çalışanlar, izinler ve iş bağlamı ile ilgili bilgiler gibi Commerce'teki iyi tanımlanmış bilgilerden yararlanarak Teams'in sağlanması.</span><span class="sxs-lookup"><span data-stu-id="d5331-110">Provision Teams by taking advantage of well-defined information from Commerce, such as the organizational structure and information about stores, workers, permissions, and business context.</span></span>
- <span data-ttu-id="d5331-111">Devam eden değişiklikleri (örneğin yeni mağaza ve yeni çalışanların eklenmesi) Commerce ve Teams arasında kolaylıkla eşitleyebilirsiniz, ancak kuruluş yapısı verilerinin ana kaynağı olarak Commerce'i tutun.</span><span class="sxs-lookup"><span data-stu-id="d5331-111">Easily synchronize ongoing changes (for example, the addition of new stores or hiring of new employees) between Commerce and Teams, but keep Commerce as the master source of organizational structure data.</span></span>
- <span data-ttu-id="d5331-112">Çalışanların, Mağaza yöneticilerinin, bölge yöneticilerinin ve iletişim yöneticilerinin her iki uygulamadan da görev yönetimi işlemesini sağlamak için Commerce ve Teams arasında görev yönetimini tümleştirin.</span><span class="sxs-lookup"><span data-stu-id="d5331-112">Integrate task management between Commerce and Teams to help store workers, store managers, regional managers, and communications managers handle task management from either application.</span></span>

## <a name="prerequisites-for-using-integration-features"></a><span data-ttu-id="d5331-113">Tümleştirme özelliklerini kullanmak için Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="d5331-113">Prerequisites for using integration features</span></span>

<span data-ttu-id="d5331-114">Microsoft Teams Tümleştirme özellikleri kullanmaya başlamadan önce aşağıdaki önkoşulların sağlanması gerekir:</span><span class="sxs-lookup"><span data-stu-id="d5331-114">The following prerequisites must be in place before you can start to use Microsoft Teams integration features:</span></span>

- <span data-ttu-id="d5331-115">Microsoft 365 İş standart lisansı (Bu lisans Teams'i içerir.)</span><span class="sxs-lookup"><span data-stu-id="d5331-115">Microsoft 365 Business Standard License (This license includes Teams.)</span></span>
- <span data-ttu-id="d5331-116">Tüm mağaza yöneticileri ve çalışanları için Azure Active Directory (Azure AD) hesapları</span><span class="sxs-lookup"><span data-stu-id="d5331-116">Azure Active Directory (Azure AD) accounts for all store managers and workers</span></span>
- <span data-ttu-id="d5331-117">Azure AD Kimlik doğrulamasıyla yapılandırılan satış noktası (POS) sistemleri</span><span class="sxs-lookup"><span data-stu-id="d5331-117">Point of sale (POS) systems that are configured with Azure AD authentication</span></span>

## <a name="conceptual-architecture"></a><span data-ttu-id="d5331-118">Kavramsal mimari</span><span class="sxs-lookup"><span data-stu-id="d5331-118">Conceptual architecture</span></span>

<span data-ttu-id="d5331-119">Aşağıdaki resim örnek olarak bir San Francisco mağazasını kullanarak Dynamics 365 Commerce ve Microsoft Teams tümleştirmesinin kavramsal mimarisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="d5331-119">The following illustration shows the conceptual architecture of Dynamics 365 Commerce and Microsoft Teams integration, using a San Francisco store as an example.</span></span> <span data-ttu-id="d5331-120">Hem Teams hem de Commerce POS uygulaması Microsoft Planner'ı bir depo olarak kullanır, böylece Teams'den yayımlanan görevler POS uygulamasında görünür ve POS uygulamasında mağaza yöneticileri tarafından oluşturulan anlık görevler Teams'de de görünür, böylece uygulamalar arasında kesintisiz bir görev yönetimi deneyimi elde edilir.</span><span class="sxs-lookup"><span data-stu-id="d5331-120">Both Teams and the Commerce POS application use Microsoft Planner as a repository so that tasks published from Teams appear in the POS application and ad hoc tasks created by store managers in the POS application appear in Teams, resulting in a seamless task management experience between the applications.</span></span>    

![Commerce ve Teams tümleştirmesinin mimarisi](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a><span data-ttu-id="d5331-122">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d5331-122">Additional resources</span></span>

[<span data-ttu-id="d5331-123">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="d5331-123">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="d5331-124">Dynamics 365 Commerce'ten Microsoft Teams sağlama</span><span class="sxs-lookup"><span data-stu-id="d5331-124">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="d5331-125">Microsoft Teams ve Dynamics 365 Commerce POS arasında görev yönetimini eşitleme</span><span class="sxs-lookup"><span data-stu-id="d5331-125">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="d5331-126">Microsoft Teams'de kullanıcı rollerini yönetme</span><span class="sxs-lookup"><span data-stu-id="d5331-126">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="d5331-127">Microsoft Teams'de önceden var olan ekipler varsa mağazaları ve ekipleri eşleme</span><span class="sxs-lookup"><span data-stu-id="d5331-127">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="d5331-128">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi SSS</span><span class="sxs-lookup"><span data-stu-id="d5331-128">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
