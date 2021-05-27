---
title: Microsoft Teams'de kullanıcı rollerini yönetme
description: Bu konuda, Microsoft Teams'te Microsoft Dynamics 365 Commerce kullanıcı rollerinin nasıl yönetileceği açıklanmaktadır.
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
ms.openlocfilehash: 7b4734fd363cd5ee44f228e0c0f9ce73abad1aaa
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021864"
---
# <a name="manage-user-roles-in-microsoft-teams"></a><span data-ttu-id="ac2b0-103">Microsoft Teams'de kullanıcı rollerini yönetme</span><span class="sxs-lookup"><span data-stu-id="ac2b0-103">Manage user roles in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ac2b0-104">Bu konuda, Microsoft Teams'te Microsoft Dynamics 365 Commerce kullanıcı rollerinin nasıl yönetileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ac2b0-104">This topic describes how to manage Microsoft Dynamics 365 Commerce user roles in Microsoft Teams.</span></span>

<span data-ttu-id="ac2b0-105">Teams'de her mağaza veya kanal için bir ekip oluştururken, ekibe karşılık gelen bir grup üyeliği oluşturulur (örneğin, `HOUSTON_D365@<YourTenantAzureADDomain>.com`).</span><span class="sxs-lookup"><span data-stu-id="ac2b0-105">As you create a team for each store or channel in Teams, a group membership that corresponds to the team is created (for example, `HOUSTON_D365@<YourTenantAzureADDomain>.com`).</span></span> <span data-ttu-id="ac2b0-106">Bir ekip grubu üyeliğinin altındaki tüm depolama çalışanları şu iki Kullanıcı rolünden birine atanmıştır: **sahip** veya **üye**.</span><span class="sxs-lookup"><span data-stu-id="ac2b0-106">All the store workers under a team group membership are assigned one of two user roles: **Owner** or **Member**.</span></span> <span data-ttu-id="ac2b0-107">**Sahip** kullanıcı rolüne sahip mağaza çalışanları, özel kanal ekleme ve üye ekleme veya silme gibi işlemleri gerçekleştirebilirler.</span><span class="sxs-lookup"><span data-stu-id="ac2b0-107">Store employees who have the **Owner** user role can perform operations such as adding a private channel, and adding or deleting members.</span></span> <span data-ttu-id="ac2b0-108">Genellikle mağaza yöneticilerinin **sahip** Kullanıcı rolü vardır.</span><span class="sxs-lookup"><span data-stu-id="ac2b0-108">Typically, store managers have the **Owner** user role.</span></span>

<span data-ttu-id="ac2b0-109">Aşağıdaki çizimde, Microsoft Teams Yönetim Merkezi'ndeki ekip üyelerinin listesi ve bunların Kullanıcı rollerine ilişkin bir örnek gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ac2b0-109">The following illustration shows an example of a list of team members and their user roles in the Microsoft Teams admin center.</span></span>

![Microsoft Teams Yönetim merkezinde ekip üyeleri ve Kullanıcı rolleri](media/d365-commerce-teams-integration-user-roles.png)

<span data-ttu-id="ac2b0-111">Daha fazla bilgi için, bkz. [Microsoft Teams'de ekip sahipleri ve üyeleri atama](/microsoftteams/assign-roles-permissions).</span><span class="sxs-lookup"><span data-stu-id="ac2b0-111">For more information, see [Assign team owners and members in Microsoft Teams](/microsoftteams/assign-roles-permissions).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac2b0-112">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ac2b0-112">Additional resources</span></span>

[<span data-ttu-id="ac2b0-113">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bakış</span><span class="sxs-lookup"><span data-stu-id="ac2b0-113">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="ac2b0-114">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="ac2b0-114">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="ac2b0-115">Dynamics 365 Commerce'ten Microsoft Teams sağlama</span><span class="sxs-lookup"><span data-stu-id="ac2b0-115">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="ac2b0-116">Microsoft Teams ve Dynamics 365 Commerce POS arasında görev yönetimini eşitleme</span><span class="sxs-lookup"><span data-stu-id="ac2b0-116">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="ac2b0-117">Microsoft Teams'de önceden var olan ekipler varsa mağazaları ve ekipleri eşleme</span><span class="sxs-lookup"><span data-stu-id="ac2b0-117">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="ac2b0-118">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi SSS</span><span class="sxs-lookup"><span data-stu-id="ac2b0-118">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)