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
ms.openlocfilehash: 20d3da65028b455ab1602e3a8b443ea7e585b1f0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462853"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-17-2018"></a><span data-ttu-id="41c2d-103">Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (17 Eylül 2018)</span><span class="sxs-lookup"><span data-stu-id="41c2d-103">What's new or changed in Dynamics 365 Talent - Core HR (September 17, 2018)</span></span>

<span data-ttu-id="41c2d-104">**Derleme 8.1.154.0**</span><span class="sxs-lookup"><span data-stu-id="41c2d-104">**Build 8.1.154.0**</span></span>

<span data-ttu-id="41c2d-105">Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="41c2d-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="leave-and-absence--accrue-time-based-on-hours-worked"></a><span data-ttu-id="41c2d-106">Bırakma ve devamsızlık – çalışma saatlerini temel alarak tahakkuk zamanı</span><span class="sxs-lookup"><span data-stu-id="41c2d-106">Leave and Absence – Accrue time based on hours worked</span></span>

<span data-ttu-id="41c2d-107">Bırakma planlarına yeni bir tahakkuk türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="41c2d-107">A new accrual type has been added to Leave plans.</span></span> <span data-ttu-id="41c2d-108">Tahakkuk planı şimdi hizmet verilen aylar veya çalışılan saatlere dayanabilir.</span><span class="sxs-lookup"><span data-stu-id="41c2d-108">The accrual schedule can now be based on months of service or hours worked.</span></span> <span data-ttu-id="41c2d-109">Daha fazla bilgi için bkz [Çalışılan saatlere dayanarak zaman tahakkuk](leave-accrue-hours-worked.md).</span><span class="sxs-lookup"><span data-stu-id="41c2d-109">For more information, see [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

## <a name="platform-update-18-for-finance-and-operations"></a><span data-ttu-id="41c2d-110">Finance and Operations için Platform güncelleştirmesi 18</span><span class="sxs-lookup"><span data-stu-id="41c2d-110">Platform update 18 for Finance and Operations</span></span>

<span data-ttu-id="41c2d-111">Finance and Operations için Platform Güncelleştirmesi 18 şimdi Talent sürümünün parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="41c2d-111">Platform update 18 for Finance and Operations is now part of the Talent release.</span></span> 

-   <span data-ttu-id="41c2d-112">Zorunlu ve diğer alanlar kişiselleştirme ile gizlenebilir.</span><span class="sxs-lookup"><span data-stu-id="41c2d-112">Mandatory and other fields can be hidden via personalization.</span></span> <span data-ttu-id="41c2d-113">Bu basitleştirilmiş deneyimi oluşturmak bir kullanıcı burada iş mantığı tarafından varsayılan zorunlu alanların görüntülenmemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="41c2d-113">This allows a user to create a simplified experience where mandatory fields that are defaulted by business logic are not shown.</span></span> <span data-ttu-id="41c2d-114">Bir kaydetmeye teşebbüs edilirse, gizli zorunlu alanlar geçici olarak görünür hale gelir.</span><span class="sxs-lookup"><span data-stu-id="41c2d-114">Hidden mandatory fields are also temporarily made visible if they are empty when a save is attempted.</span></span>

-   <span data-ttu-id="41c2d-115">Finance and Operations için Platform Güncelleştirmesi 18'de, Talent web istemcisi şimdi Microsoft Fluent Design görselleri ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="41c2d-115">In Platform update 18 for Finance and Operations, the Talent web client now aligns its visuals with Microsoft Fluent Design.</span></span>

    -   <span data-ttu-id="41c2d-116">Alanlar "okuma modunda" ise, formu düzenleye geçirmek için kolayca düzenleme seçeneğini işaretleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41c2d-116">When fields are in “read mode”, you can simply select the edit option in the fields to switch the form to edit.</span></span>

    -   <span data-ttu-id="41c2d-117">Alanların okuma modunda görüntülenmesine dair değişiklikler.</span><span class="sxs-lookup"><span data-stu-id="41c2d-117">Changes in how fields display when in read mode.</span></span>

    -   <span data-ttu-id="41c2d-118">Çalışma alanlarındaki ve sayfalardaki başlıklar kalındır.</span><span class="sxs-lookup"><span data-stu-id="41c2d-118">Headings in workspaces and pages are bold.</span></span>

-   <span data-ttu-id="41c2d-119">Değişmeyen aramaların davranışı iyileştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="41c2d-119">The behavior of non-replacing lookups has been improved.</span></span> <span data-ttu-id="41c2d-120">Daha fazla bilgi için, bkz. [Değişmeyen aramalar için iyileştirilmiş davranışlar](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/non-replacing-lookups).</span><span class="sxs-lookup"><span data-stu-id="41c2d-120">For more information, see [Improved behavior for non-replacing lookups](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/non-replacing-lookups).</span></span>

## <a name="bug-fixes"></a><span data-ttu-id="41c2d-121">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="41c2d-121">Bug fixes</span></span>

<span data-ttu-id="41c2d-122">Bu sürüm çeşitli ek sorun giderme içermektedir, ACA, ADA ve I9'a referanslar şimdi yalnızca ABD şirketlerinde etkin olacaktır.</span><span class="sxs-lookup"><span data-stu-id="41c2d-122">This release includes several additional bug fixes, including references to ACA, ADA, and I9 now will only be enabled in US companies.</span></span>
