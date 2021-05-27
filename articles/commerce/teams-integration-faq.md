---
title: Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi SSS
description: Bu konu, Microsoft Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi ile ilgili sık sorulan soruların yanıtlarını sağlar.
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
ms.openlocfilehash: 3fc7cff0a3f8d0fbfb196ec5951b138088afece7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019482"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a><span data-ttu-id="70bf1-103">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi SSS</span><span class="sxs-lookup"><span data-stu-id="70bf1-103">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="70bf1-104">Bu konu, Microsoft Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi ile ilgili sık sorulan soruların yanıtlarını sağlar.</span><span class="sxs-lookup"><span data-stu-id="70bf1-104">This topic provides answers to frequently asked questions regarding Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a><span data-ttu-id="70bf1-105">Commerce'ten Teams sağlanırken mağazada ekibin sahibi kim olur?</span><span class="sxs-lookup"><span data-stu-id="70bf1-105">Who in the store becomes an owner of a team while provisioning Teams from Commerce?</span></span> 

<span data-ttu-id="70bf1-106">Özel kanal ekleme ve üye ekleme veya silme gibi işlemleri gerçekleştirebilmeleri için, tüm mağaza yöneticileri ilgili ekip grubuna sahip olarak otomatik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="70bf1-106">All store managers are automatically added as owners to the corresponding team group so that they can perform operations such as adding a private channel and adding or deleting members.</span></span> 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a><span data-ttu-id="70bf1-107">"İletişim Yöneticisi" rolünü Commerce Headquarters'da bir çalışana nasıl atayabilirim?</span><span class="sxs-lookup"><span data-stu-id="70bf1-107">How do I assign the "communications manager" role to an employee in Commerce headquarters?</span></span> 

<span data-ttu-id="70bf1-108">Microsoft Teams'deki iletişim yöneticileri, görev listeleri oluşturma ve yayımlama yeteneğine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="70bf1-108">Communication managers in Microsoft Teams have the ability to create and publish task lists.</span></span> <span data-ttu-id="70bf1-109">İletişim yöneticileri olması gereken kuruluş çalışanlarının Commerce Headquarters'da kendilerine atanmış "perakende Görev Yöneticisi" rolü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="70bf1-109">Organization employees who need to become communication managers must have the "retail task manager" role assigned to them in Commerce headquarters.</span></span>

<span data-ttu-id="70bf1-110">Commerce Headquarters'da bir çalışana perakende görev yöneticisi rolü atamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="70bf1-110">To assign the retail task manager role to an employee in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="70bf1-111">**Perakende ve Ticaret \> Personel \> Kullanıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="70bf1-111">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="70bf1-112">Bir çalışan seçin.</span><span class="sxs-lookup"><span data-stu-id="70bf1-112">Select an employee.</span></span>
1. <span data-ttu-id="70bf1-113">**Kullanıcının rolleri** hızlı sekmesinde, **Rol ata**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="70bf1-113">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="70bf1-114">**Kullanıcıya rol ata** iletişim kutusunda, **perakende görev Yöneticisi** rolünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="70bf1-114">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a><span data-ttu-id="70bf1-115">Belirli bir kuruluş hiyerarşisini Microsoft Teams'e yüklenmek üzere nasıl kullanılabilir hale getirebilirim?</span><span class="sxs-lookup"><span data-stu-id="70bf1-115">How do I make a specific organization hierarchy available to upload into Microsoft Teams?</span></span>

<span data-ttu-id="70bf1-116">Commerce Headquarters'da, her kuruluşun hiyerarşisi bir veya daha çok amaçla ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="70bf1-116">In Commerce headquarters, every organization's hierarchy is associated with one or more purposes.</span></span> <span data-ttu-id="70bf1-117">Microsoft Teams'e sağlamak istediğiniz hiyerarşinin aşağıdaki örnek görüntüde gösterildiği gibi, kendisiyle ilişkilendirilmiş **perakende Raporlama** amacı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="70bf1-117">Make sure the hierarchy that you want to provision into Microsoft Teams has the **Retail reporting** purpose associated with it, as shown in the following example image.</span></span> 

![Commerce Headquarters'da kuruluş hiyerarşisi amacı örneği](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a><span data-ttu-id="70bf1-119">Mağaza çalışanlarının Azure Active Directory (Azure AD) kullanarak Commerce satış noktasında (POS) oturum açmasını nasıl sağlarım?</span><span class="sxs-lookup"><span data-stu-id="70bf1-119">How do I enable retail store workers to sign in to Commerce point of sale (POS) using Azure Active Directory (Azure AD)?</span></span>

<span data-ttu-id="70bf1-120">Commerce POS oturum açma deneyimini Azure AD kimlik doğrulamayı kullanacak şekilde konfigüre etme hakkında bilgi için bkz. [POS oturum açma için Azure Active Directory kimlik doğrulamayı etkinleştirme](aad-pos-logon.md).</span><span class="sxs-lookup"><span data-stu-id="70bf1-120">For information about how to configure the Commerce POS sign-in experience to use Azure AD authentication, see [Enable Azure Active Directory authentication for POS sign-in](aad-pos-logon.md).</span></span>

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a><span data-ttu-id="70bf1-121">Kuruluşumda zaten Microsoft Teams'de oluşturulmuş ekipler varsa Commerce Headquarters'da depoları ve ilgili ekipleri nasıl eşlerim?</span><span class="sxs-lookup"><span data-stu-id="70bf1-121">How do I map stores and corresponding teams in Commerce headquarters if my organization has already created teams in Microsoft Teams?</span></span>

<span data-ttu-id="70bf1-122">Öncedenvar olan ekipler varsa mağaza ve ekiplerin nasıl eşleneceği hakkında daha fazla bilgi için, [kuruluşunuzda Microsoft Teams'de önceden varolan ekipler varsa, depoları ve ilgili ekipleri eşleme](map-stores-existing-teams.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="70bf1-122">For information on how to map stores and teams if there are pre-existing teams, see [Map stores and corresponding teams if your organization has pre-existing teams in Microsoft Teams](map-stores-existing-teams.md).</span></span>

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a><span data-ttu-id="70bf1-123">Oturum depolama alanında depolanan Microsoft Graph API belirtecini nasıl temizlerim?</span><span class="sxs-lookup"><span data-stu-id="70bf1-123">How do I clear the Microsoft Graph API token stored in the session storage?</span></span>

<span data-ttu-id="70bf1-124">Bir satış noktasında Azure Active Directory (Azure AD) hesabıyla oturum açan bir kullanıcının, oturum depolama alanını temizlemek için POS oturumunu kapatması veya uygulamayı kapatması gerekir.</span><span class="sxs-lookup"><span data-stu-id="70bf1-124">A user who has signed in to the point of sale (POS) with an Azure Active Directory (Azure AD) account should sign out from the POS or close the application to clear the session storage.</span></span> 

> [!TIP]
> <span data-ttu-id="70bf1-125">Önerilen en iyi uygulama, Terminal kullanılmadığında mağaza çalışanlarının her zaman POS terminalini kilitlemesi veya oturumu kapatmasıdır.</span><span class="sxs-lookup"><span data-stu-id="70bf1-125">A recommended best practice is to always have store workers lock the POS terminal or sign out from a session when not using the terminal.</span></span> 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a><span data-ttu-id="70bf1-126">Bir mağazanın mağaza yöneticileri yoksa ne olur?</span><span class="sxs-lookup"><span data-stu-id="70bf1-126">What happens if a store doesn't have store managers?</span></span>

<span data-ttu-id="70bf1-127">Bir mağazanın yöneticileri yoksa, mağaza için veya Teams'de bir ekip grubu oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="70bf1-127">If a store doesn't have managers, a team group will not be created for the store or in Teams.</span></span> 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a><span data-ttu-id="70bf1-128">Mağaza yöneticisi şirketten ayrıldığında ne olur?</span><span class="sxs-lookup"><span data-stu-id="70bf1-128">What happens if a store manager leaves the company?</span></span>

<span data-ttu-id="70bf1-129">Sahip rolüne sahip herkes Commerce Headquarters'da yeni bir mağaza yöneticisi ekleyebilir ve yeni yöneticinin Teams'de gerekli ayrıcalıklara sahip olmasını sağlayacak şekilde Teams'i yeniden temin edebilir.</span><span class="sxs-lookup"><span data-stu-id="70bf1-129">Anyone with the owner role can add a new store manager in Commerce headquarters and reprovision Teams so that the new manager will have the necessary privileges in Teams for the group.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="70bf1-130">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="70bf1-130">Additional resources</span></span>

[<span data-ttu-id="70bf1-131">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bakış</span><span class="sxs-lookup"><span data-stu-id="70bf1-131">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="70bf1-132">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="70bf1-132">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="70bf1-133">Dynamics 365 Commerce'ten Microsoft Teams sağlama</span><span class="sxs-lookup"><span data-stu-id="70bf1-133">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="70bf1-134">Microsoft Teams ve Dynamics 365 Commerce POS arasında görev yönetimini eşitleme</span><span class="sxs-lookup"><span data-stu-id="70bf1-134">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="70bf1-135">Microsoft Teams'de kullanıcı rollerini yönetme</span><span class="sxs-lookup"><span data-stu-id="70bf1-135">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="70bf1-136">Microsoft Teams'de önceden var olan ekipler varsa mağazaları ve ekipleri eşleme</span><span class="sxs-lookup"><span data-stu-id="70bf1-136">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)
