---
title: Kullanıcı, Attract veya Onboard'da Kişi Seçici içinde bulunamadı
description: Bu konu, şirket kiracısı içindeki kullanıcılar Dynamics 365 for Talent Attract veya Onboard uygulamalarındaki Kişi Seçicide görüntülenmediğinde ne yapılacağını açıklar.
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
ms.openlocfilehash: d5a2c61fc21578d1db4c1bf0c3dfaf0c7a93298c
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "859517"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a><span data-ttu-id="937bd-103">Azure Active Directory kullanıcıları Kişi Seçici'de bulunamadı</span><span class="sxs-lookup"><span data-stu-id="937bd-103">Azure Active Directory users not found in People Picker</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="937bd-104">Çıkış</span><span class="sxs-lookup"><span data-stu-id="937bd-104">Issue</span></span>

<span data-ttu-id="937bd-105">Kiracı için Microsoft Azure Active Directory (Azure AD) içindeki çeşitli geçerli kullanıcılar, Dynamics 365 for Talent Attract veya Onboard uygulamalraında Kişi Seçicide adları aratılırken görüntülenmiyor.</span><span class="sxs-lookup"><span data-stu-id="937bd-105">Certain valid users in Microsoft Azure Active Directory (Azure AD) for the tenant do not appear when searching for the name in the People Picker in the Dynamics 365 for Talent Attract or Onboard applications.</span></span>

## <a name="cause"></a><span data-ttu-id="937bd-106">Nedeni</span><span class="sxs-lookup"><span data-stu-id="937bd-106">Cause</span></span>

<span data-ttu-id="937bd-107">Çeşitli kullanıcı türleri Attract ve Onboard uygulamalarında şu anda desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="937bd-107">Certain user types are not currently supported in the Attract and Onboard applications.</span></span> <span data-ttu-id="937bd-108">Kullanıcının bir Azure AD Business to Business (B2B) misafir kullanıcısı olmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="937bd-108">Verify that the user is not an Azure AD Business to Business (B2B) guest user.</span></span> <span data-ttu-id="937bd-109">"Kullanıcı Türü" bilgisi, Azure portalındaki Azure Active Directory dikey pencere taşında bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="937bd-109">"User Type" information can be found in the Azure Active Directory blade on the Azure portal.</span></span>

<span data-ttu-id="937bd-110">Azure B2B hakkında daha fazla bilgi için bkz. [Azure Active Directory B2B'de misafir kullanıcı erişimi nedir](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).</span><span class="sxs-lookup"><span data-stu-id="937bd-110">For more information about Azure B2B, see [What is guest user access in Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).</span></span>

<span data-ttu-id="937bd-111">B2B olmayan kullanıcılar için bazı kullanıcılar eksik "Kullanıcı Türü" özelliğine **Kullanıcı** nesnesi üzerinde sahip olabilirler.</span><span class="sxs-lookup"><span data-stu-id="937bd-111">For non-B2B users, there are certain users who may have an incomplete "User Type" property on the **User** object.</span></span> <span data-ttu-id="937bd-112">Bu, Azure AD PowerShell modülü kullanılarak düzeltilebilir.</span><span class="sxs-lookup"><span data-stu-id="937bd-112">This can be verified and fixed using the Azure AD Powershell module.</span></span> <span data-ttu-id="937bd-113">Daha fazla bilgi için [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="937bd-113">For more information, see [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).</span></span>

## <a name="resolution"></a><span data-ttu-id="937bd-114">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="937bd-114">Resolution</span></span>

<span data-ttu-id="937bd-115">Aşağıdaki adımları sorunu gidermek için tamamlamak için "Genel Yönetici" izinlerine Azure Active Directory kiracısı üzerinde sahip olmalısınız veya **User.ReadWrite.All** izinlerine sahip olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="937bd-115">To complete the following steps to resolve the issue, you will need to have "Global Administrator" permissions on the Azure Active Directory tenant or permissions for **User.ReadWrite.All**.</span></span>

<span data-ttu-id="937bd-116">Etkilenen kullanıcı için "Kullanıcı Türünü" doğrulamak için.</span><span class="sxs-lookup"><span data-stu-id="937bd-116">To verify the "User Type" for the affected user.</span></span>

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
<span data-ttu-id="937bd-117">Komut, aşağıdaki bilgiyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="937bd-117">The command returns the following information.</span></span>
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
<span data-ttu-id="937bd-118">Kullanıcı üzerindeki **UserType** özelliğini not edin.</span><span class="sxs-lookup"><span data-stu-id="937bd-118">Note the **UserType** property on the user.</span></span> <span data-ttu-id="937bd-119">**UserType** boş ise, örneğin "Üye" veya "Misafir" değilse, **UserType**'ı aşağıdaki komutu kullanarak güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="937bd-119">If the **UserType** is blank, for example not "Member" or "Guest", update the **UserType** using the following command.</span></span>

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
