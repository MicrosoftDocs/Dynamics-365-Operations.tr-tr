---
title: Kullanıcı, Attract veya Onboard'da Kişi Seçici içinde bulunamadı
description: Bu konuda şirket kiracısındaki kullanıcılar Dynamics 365 Talent - Attract veya Onboard'daki Kişi Seçici'de görüntülenmediğinde ne yapılacağı açıklanmaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d84dd9c22738a1b4fc5edb5331d4aa213b82facb
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551945"
---
# <a name="user-not-found-in-people-picker-in-attract-or-onboard"></a><span data-ttu-id="c0eba-103">Kullanıcı, Attract veya Onboard'da Kişi Seçici içinde bulunamadı</span><span class="sxs-lookup"><span data-stu-id="c0eba-103">User not found in People Picker in Attract or Onboard</span></span>
[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="c0eba-104">Çıkış</span><span class="sxs-lookup"><span data-stu-id="c0eba-104">Issue</span></span>

<span data-ttu-id="c0eba-105">Kiracı için Microsoft Microsoft Azure Active Directory (Azure AD) üzerindeki çeşitli geçerli kullanıcılar, Dynamics 365 Talent: Attract veya Dynamics 365 Talent: Onboard uygulamalarında Kişi Seçici'de adları aranırken görüntülenmiyor.</span><span class="sxs-lookup"><span data-stu-id="c0eba-105">Certain valid users in Microsoft Azure Active Directory (Azure AD) for the tenant do not appear when searching for the name in the People Picker in Dynamics 365 Talent: Attract or Dynamics 365 Talent: Onboard.</span></span>

## <a name="cause"></a><span data-ttu-id="c0eba-106">Nedeni</span><span class="sxs-lookup"><span data-stu-id="c0eba-106">Cause</span></span>

<span data-ttu-id="c0eba-107">Bazı kullanıcı türleri, Attract ve Onboard uygulamalarında şu anda desteklenmemektedir.</span><span class="sxs-lookup"><span data-stu-id="c0eba-107">Certain user types are not currently supported in Attract and Onboard.</span></span> <span data-ttu-id="c0eba-108">Kullanıcının bir Azure AD Business to Business (B2B) misafir kullanıcısı olmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="c0eba-108">Verify that the user is not an Azure AD Business to Business (B2B) guest user.</span></span> <span data-ttu-id="c0eba-109">"Kullanıcı Türü" bilgisi, Azure portalındaki Azure Active Directory dikey pencere taşında bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="c0eba-109">"User Type" information can be found in the Azure Active Directory blade on the Azure portal.</span></span>

<span data-ttu-id="c0eba-110">Azure B2B hakkında daha fazla bilgi için bkz. [Azure Active Directory B2B'de misafir kullanıcı erişimi nedir](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).</span><span class="sxs-lookup"><span data-stu-id="c0eba-110">For more information about Azure B2B, see [What is guest user access in Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).</span></span>

<span data-ttu-id="c0eba-111">B2B olmayan kullanıcılar için bazı kullanıcılar eksik "Kullanıcı Türü" özelliğine **Kullanıcı** nesnesi üzerinde sahip olabilirler.</span><span class="sxs-lookup"><span data-stu-id="c0eba-111">For non-B2B users, there are certain users who may have an incomplete "User Type" property on the **User** object.</span></span> <span data-ttu-id="c0eba-112">Bu, Azure AD PowerShell modülü kullanılarak düzeltilebilir.</span><span class="sxs-lookup"><span data-stu-id="c0eba-112">This can be verified and fixed using the Azure AD Powershell module.</span></span> <span data-ttu-id="c0eba-113">Daha fazla bilgi için [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="c0eba-113">For more information, see [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).</span></span>

## <a name="resolution"></a><span data-ttu-id="c0eba-114">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="c0eba-114">Resolution</span></span>

<span data-ttu-id="c0eba-115">Aşağıdaki adımları sorunu gidermek için tamamlamak için "Genel Yönetici" izinlerine Azure Active Directory kiracısı üzerinde sahip olmalısınız veya **User.ReadWrite.All** izinlerine sahip olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="c0eba-115">To complete the following steps to resolve the issue, you will need to have "Global Administrator" permissions on the Azure Active Directory tenant or permissions for **User.ReadWrite.All**.</span></span>

<span data-ttu-id="c0eba-116">Etkilenen kullanıcı için "Kullanıcı Türünü" doğrulamak için.</span><span class="sxs-lookup"><span data-stu-id="c0eba-116">To verify the "User Type" for the affected user.</span></span>

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
<span data-ttu-id="c0eba-117">Komut, aşağıdaki bilgiyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="c0eba-117">The command returns the following information.</span></span>
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
<span data-ttu-id="c0eba-118">Kullanıcı üzerindeki **UserType** özelliğini not edin.</span><span class="sxs-lookup"><span data-stu-id="c0eba-118">Note the **UserType** property on the user.</span></span> <span data-ttu-id="c0eba-119">**UserType** boş ise, örneğin "Üye" veya "Misafir" değilse, **UserType**'ı aşağıdaki komutu kullanarak güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="c0eba-119">If the **UserType** is blank, for example not "Member" or "Guest", update the **UserType** using the following command.</span></span>

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
