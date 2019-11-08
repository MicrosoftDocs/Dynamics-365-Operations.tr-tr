---
title: Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (17 Eylül 2018)
description: Bu konuda, Microsoft Dynamics 365 Talent - Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 09/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 051be85a4424a273ae190a93ab11793d5b6e4326
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551369"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-17-2018"></a><span data-ttu-id="13c1d-103">Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (17 Eylül 2018)</span><span class="sxs-lookup"><span data-stu-id="13c1d-103">What's new or changed in Dynamics 365 Talent - Core HR (September 17, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="13c1d-104">**Derleme 8.1.154.0**</span><span class="sxs-lookup"><span data-stu-id="13c1d-104">**Build 8.1.154.0**</span></span>

<span data-ttu-id="13c1d-105">Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="13c1d-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="leave-and-absence--accrue-time-based-on-hours-worked"></a><span data-ttu-id="13c1d-106">Bırakma ve devamsızlık – çalışma saatlerini temel alarak tahakkuk zamanı</span><span class="sxs-lookup"><span data-stu-id="13c1d-106">Leave and Absence – Accrue time based on hours worked</span></span>

<span data-ttu-id="13c1d-107">Bırakma planlarına yeni bir tahakkuk türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="13c1d-107">A new accrual type has been added to Leave plans.</span></span> <span data-ttu-id="13c1d-108">Tahakkuk planı şimdi hizmet verilen aylar veya çalışılan saatlere dayanabilir.</span><span class="sxs-lookup"><span data-stu-id="13c1d-108">The accrual schedule can now be based on months of service or hours worked.</span></span> <span data-ttu-id="13c1d-109">Daha fazla bilgi için bkz [Çalışılan saatlere dayanarak zaman tahakkuk](leave-accrue-hours-worked.md).</span><span class="sxs-lookup"><span data-stu-id="13c1d-109">For more information, see [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

## <a name="platform-update-18-for-finance-and-operations"></a><span data-ttu-id="13c1d-110">Finance and Operations için Platform güncelleştirmesi 18</span><span class="sxs-lookup"><span data-stu-id="13c1d-110">Platform update 18 for Finance and Operations</span></span>

<span data-ttu-id="13c1d-111">Finance and Operations için Platform güncelleştirmesi 18 artık Talent sürümünün parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="13c1d-111">Platform update 18 for Finance and Operations is now part of the Talent release.</span></span> 

-   <span data-ttu-id="13c1d-112">Zorunlu ve diğer alanlar kişiselleştirme ile gizlenebilir.</span><span class="sxs-lookup"><span data-stu-id="13c1d-112">Mandatory and other fields can be hidden via personalization.</span></span> <span data-ttu-id="13c1d-113">Bu basitleştirilmiş deneyimi oluşturmak bir kullanıcı burada iş mantığı tarafından varsayılan zorunlu alanların görüntülenmemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="13c1d-113">This allows a user to create a simplified experience where mandatory fields that are defaulted by business logic are not shown.</span></span> <span data-ttu-id="13c1d-114">Bir kaydetmeye teşebbüs edilirse, gizli zorunlu alanlar geçici olarak görünür hale gelir.</span><span class="sxs-lookup"><span data-stu-id="13c1d-114">Hidden mandatory fields are also temporarily made visible if they are empty when a save is attempted.</span></span>

-   <span data-ttu-id="13c1d-115">Finance and Operations için Platform güncelleştirmesi 18'de, Talent web istemcisi, görsellerini artık Microsoft Fluent Design uyumlu hale getiriyor.</span><span class="sxs-lookup"><span data-stu-id="13c1d-115">In Platform update 18 for Finance and Operations, the Talent web client now aligns its visuals with Microsoft Fluent Design.</span></span>

    -   <span data-ttu-id="13c1d-116">Alanlar "okuma modunda" ise, formu düzenleye geçirmek için kolayca düzenleme seçeneğini işaretleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="13c1d-116">When fields are in “read mode”, you can simply select the edit option in the fields to switch the form to edit.</span></span>

    -   <span data-ttu-id="13c1d-117">Alanların okuma modunda görüntülenmesine dair değişiklikler.</span><span class="sxs-lookup"><span data-stu-id="13c1d-117">Changes in how fields display when in read mode.</span></span>

    -   <span data-ttu-id="13c1d-118">Çalışma alanlarındaki ve sayfalardaki başlıklar kalındır.</span><span class="sxs-lookup"><span data-stu-id="13c1d-118">Headings in workspaces and pages are bold.</span></span>

-   <span data-ttu-id="13c1d-119">Değişmeyen aramaların davranışı iyileştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="13c1d-119">The behavior of non-replacing lookups has been improved.</span></span> <span data-ttu-id="13c1d-120">Daha fazla bilgi için, bkz. [Değişmeyen aramalar için iyileştirilmiş davranışlar](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0).</span><span class="sxs-lookup"><span data-stu-id="13c1d-120">For more information, see [Improved behavior for non-replacing lookups](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0).</span></span>

## <a name="bug-fixes"></a><span data-ttu-id="13c1d-121">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="13c1d-121">Bug fixes</span></span>

<span data-ttu-id="13c1d-122">Bu sürüm çeşitli ek sorun giderme içermektedir, ACA, ADA ve I9'a referanslar şimdi yalnızca ABD şirketlerinde etkin olacaktır.</span><span class="sxs-lookup"><span data-stu-id="13c1d-122">This release includes several additional bug fixes, including references to ACA, ADA, and I9 now will only be enabled in US companies.</span></span>
