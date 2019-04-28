---
title: Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (17 Eylül 2018)
description: Bu konuda, Microsoft Dynamics 365 for Talent Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
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
ms.openlocfilehash: 213324f9074f88d9fdc8efdfa46bc3ed7817d1e8
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "856819"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-17-2018"></a><span data-ttu-id="b0369-103">Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (17 Eylül 2018)</span><span class="sxs-lookup"><span data-stu-id="b0369-103">What's new or changed in Dynamics 365 for Talent Core HR (September 17, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b0369-104">**Derleme 8.1.154.0**</span><span class="sxs-lookup"><span data-stu-id="b0369-104">**Build 8.1.154.0**</span></span>

<span data-ttu-id="b0369-105">Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b0369-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="leave-and-absence--accrue-time-based-on-hours-worked"></a><span data-ttu-id="b0369-106">Bırakma ve devamsızlık – çalışma saatlerini temel alarak tahakkuk zamanı</span><span class="sxs-lookup"><span data-stu-id="b0369-106">Leave and Absence – Accrue time based on hours worked</span></span>

<span data-ttu-id="b0369-107">Bırakma planlarına yeni bir tahakkuk türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="b0369-107">A new accrual type has been added to Leave plans.</span></span> <span data-ttu-id="b0369-108">Tahakkuk planı şimdi hizmet verilen aylar veya çalışılan saatlere dayanabilir.</span><span class="sxs-lookup"><span data-stu-id="b0369-108">The accrual schedule can now be based on months of service or hours worked.</span></span> <span data-ttu-id="b0369-109">Daha fazla bilgi için bkz [Çalışılan saatlere dayanarak zaman tahakkuk](leave-accrue-hours-worked.md).</span><span class="sxs-lookup"><span data-stu-id="b0369-109">For more information, see [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

## <a name="platform-update-18"></a><span data-ttu-id="b0369-110">Platform güncelleştirmesi 18</span><span class="sxs-lookup"><span data-stu-id="b0369-110">Platform update 18</span></span>

<span data-ttu-id="b0369-111">Platform Güncelleştirmesi 18 şimdi Talent sürümünün parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="b0369-111">Platform update 18 is now part of the Talent release.</span></span> 

-   <span data-ttu-id="b0369-112">Zorunlu ve diğer alanlar kişiselleştirme ile gizlenebilir.</span><span class="sxs-lookup"><span data-stu-id="b0369-112">Mandatory and other fields can be hidden via personalization.</span></span> <span data-ttu-id="b0369-113">Bu basitleştirilmiş deneyimi oluşturmak bir kullanıcı burada iş mantığı tarafından varsayılan zorunlu alanların görüntülenmemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="b0369-113">This allows a user to create a simplified experience where mandatory fields that are defaulted by business logic are not shown.</span></span> <span data-ttu-id="b0369-114">Bir kaydetmeye teşebbüs edilirse, gizli zorunlu alanlar geçici olarak görünür hale gelir.</span><span class="sxs-lookup"><span data-stu-id="b0369-114">Hidden mandatory fields are also temporarily made visible if they are empty when a save is attempted.</span></span>

-   <span data-ttu-id="b0369-115">Platform Güncelleştirmesi 18'de, Talent web istemcisi şimdi Microsoft Fluent Design görselleri ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="b0369-115">In Platform update 18, the Talent web client now aligns its visuals with Microsoft Fluent Design.</span></span>

    -   <span data-ttu-id="b0369-116">Alanlar "okuma modunda" ise, formu düzenleye geçirmek için kolayca düzenleme seçeneğini işaretleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0369-116">When fields are in “read mode”, you can simply select the edit option in the fields to switch the form to edit.</span></span>

    -   <span data-ttu-id="b0369-117">Alanların okuma modunda görüntülenmesine dair değişiklikler.</span><span class="sxs-lookup"><span data-stu-id="b0369-117">Changes in how fields display when in read mode.</span></span>

    -   <span data-ttu-id="b0369-118">Çalışma alanlarındaki ve sayfalardaki başlıklar kalındır.</span><span class="sxs-lookup"><span data-stu-id="b0369-118">Headings in workspaces and pages are bold.</span></span>

-   <span data-ttu-id="b0369-119">Değişmeyen aramaların davranışı iyileştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="b0369-119">The behavior of non-replacing lookups has been improved.</span></span> <span data-ttu-id="b0369-120">Daha fazla bilgi için, bkz. [Değişmeyen aramalar için iyileştirilmiş davranışlar](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0).</span><span class="sxs-lookup"><span data-stu-id="b0369-120">For more information, see [Improved behavior for non-replacing lookups](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0).</span></span>

## <a name="bug-fixes"></a><span data-ttu-id="b0369-121">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="b0369-121">Bug fixes</span></span>

<span data-ttu-id="b0369-122">Bu sürüm çeşitli ek sorun giderme içermektedir, ACA, ADA ve I9'a referanslar şimdi yalnızca ABD şirketlerinde etkin olacaktır.</span><span class="sxs-lookup"><span data-stu-id="b0369-122">This release includes several additional bug fixes, including references to ACA, ADA, and I9 now will only be enabled in US companies.</span></span>
