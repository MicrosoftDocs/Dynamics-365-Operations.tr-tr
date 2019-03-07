---
title: Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (10 Eylül 2018)
description: Bu konuda, Microsoft Dynamics 365 for Talent Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: b41ce93c8ae93054d2b0d71340b99e0910d4510f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "306632"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-10-2018"></a><span data-ttu-id="23aed-103">Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (10 Eylül 2018)</span><span class="sxs-lookup"><span data-stu-id="23aed-103">What's new or changed in Dynamics 365 for Talent Core HR (September 10, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="23aed-104">**Derleme 8.1.138.0**</span><span class="sxs-lookup"><span data-stu-id="23aed-104">**Build 8.1.138.0**</span></span>

<span data-ttu-id="23aed-105">Bu konuda, Microsoft Dynamics 365 for Talent Core HR'daki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="23aed-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 for Talent Core HR.</span></span>

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a><span data-ttu-id="23aed-106">İzin isteklerinde günün belirli zamanına izin verme (yarım günler)</span><span class="sxs-lookup"><span data-stu-id="23aed-106">Allow specific time of day on time-off requests (half days)</span></span>

<span data-ttu-id="23aed-107">İzin ve devamsızlık, bunların gün şeklinde gönderileceği gibi ayarlandıysa, yarım gün tanımı da etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23aed-107">If leave and absence is set up so that time off is submitted in days, you can now also enable a half-day definition.</span></span> <span data-ttu-id="23aed-108">Daha sonra, kullanıcılar izin talebi gönderdiklerinde, günün ilk yarısını mı yoksa ikinci yarısını mı izinli olmak istediklerini belirtebilirler.</span><span class="sxs-lookup"><span data-stu-id="23aed-108">Then, when users submit time-off requests, they can specify whether they are requesting the first half or the second half of the day off.</span></span>

<span data-ttu-id="23aed-109">Varsayılan olarak, bu seçenek kapalıdır.</span><span class="sxs-lookup"><span data-stu-id="23aed-109">By default, this option is turned off.</span></span> <span data-ttu-id="23aed-110">Çalışanların günün ilk veya ikinci yarısını izin isteyebilmeleri için bu özelliği İnsan kaynakları **İzin ve devamsızlık** parametrelerinde açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="23aed-110">For employees to request the first half or second half of the day off, you must turn on this option in the **Leave and absence** area of Human resources parameters.</span></span>

<span data-ttu-id="23aed-111">Bu özelliğin güvenlik ayrıcalığı İnsan Kaynakları Parametrelerini Koruma'dır.</span><span class="sxs-lookup"><span data-stu-id="23aed-111">The security privilege for this feature is Maintain Human Resources Parameters.</span></span>

## <a name="validation-of-leave-and-absence-entries"></a><span data-ttu-id="23aed-112">İzin ve devamsızlık girişlerinin doğrulaması</span><span class="sxs-lookup"><span data-stu-id="23aed-112">Validation of leave and absence entries</span></span>

<span data-ttu-id="23aed-113">İznin nasıl yapılandırıldığına bağlı olarak, çalışma günlerinden daha uzun izin isteyen çalışanlara bir uyarı mesajı gösterilebilir.</span><span class="sxs-lookup"><span data-stu-id="23aed-113">Depending on how leave is configured, employees who try to submit a time-off request that is longer than their work day receive a warning message.</span></span> <span data-ttu-id="23aed-114">Başka bir deyişle, bunlar üzerinde belirli bir tarihte tam bir günden daha fazla izin isterlerse, uyarı verilir.</span><span class="sxs-lookup"><span data-stu-id="23aed-114">In other words, they are warned if they try to take more than a full day off on any given date.</span></span>

<span data-ttu-id="23aed-115">Bu doğrulamayı her zaman açıktır.</span><span class="sxs-lookup"><span data-stu-id="23aed-115">This validation is always turned on.</span></span> <span data-ttu-id="23aed-116">Tanımlanan gün eşiğini aşan çalışanları, izin isteklerinde bir uyarı alırlar.</span><span class="sxs-lookup"><span data-stu-id="23aed-116">Any time that employees exceed the day threshold that is defined, they receive a warning in their time-off request.</span></span>

## <a name="additional-fields-for-conditional-statements-in-workflows"></a><span data-ttu-id="23aed-117">İş akışlarındaki koşul deyimleri için ek alanlar</span><span class="sxs-lookup"><span data-stu-id="23aed-117">Additional fields for conditional statements in workflows</span></span>

<span data-ttu-id="23aed-118">Ek alanla, koşul ifadelerine ve yer tutuculara Core HR içindeki çeşitli iş akışları için eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="23aed-118">Additional fields have been added to conditional statements and placeholders for several workflows in Core HR.</span></span>

<span data-ttu-id="23aed-119">Aşağıdaki alanlar ücret, işten çıkarma ve transfer iş akışları için eklenmiştir:</span><span class="sxs-lookup"><span data-stu-id="23aed-119">The following fields have been added to the compensation, termination, and transfer workflows:</span></span>

- <span data-ttu-id="23aed-120">EmploymentType</span><span class="sxs-lookup"><span data-stu-id="23aed-120">EmploymentType</span></span>
- <span data-ttu-id="23aed-121">LegalEntity</span><span class="sxs-lookup"><span data-stu-id="23aed-121">LegalEntity</span></span>
- <span data-ttu-id="23aed-122">AdjustedWorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="23aed-122">AdjustedWorkerStartDate</span></span>
- <span data-ttu-id="23aed-123">EmployerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="23aed-123">EmployerNoticeAmount</span></span>
- <span data-ttu-id="23aed-124">EmployerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="23aed-124">EmployerUnitOfNotice</span></span>
- <span data-ttu-id="23aed-125">TransitionDate</span><span class="sxs-lookup"><span data-stu-id="23aed-125">TransitionDate</span></span>
- <span data-ttu-id="23aed-126">WorkerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="23aed-126">WorkerNoticeAmount</span></span>
- <span data-ttu-id="23aed-127">WorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="23aed-127">WorkerStartDate</span></span>
- <span data-ttu-id="23aed-128">WorkerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="23aed-128">WorkerUnitOfNotice</span></span>
- <span data-ttu-id="23aed-129">ProbationEndDate</span><span class="sxs-lookup"><span data-stu-id="23aed-129">ProbationEndDate</span></span>
- <span data-ttu-id="23aed-130">Bölme</span><span class="sxs-lookup"><span data-stu-id="23aed-130">Position</span></span>
- <span data-ttu-id="23aed-131">Birlik</span><span class="sxs-lookup"><span data-stu-id="23aed-131">Union</span></span>
- <span data-ttu-id="23aed-132">Departman</span><span class="sxs-lookup"><span data-stu-id="23aed-132">Department</span></span>
- <span data-ttu-id="23aed-133">PositionType</span><span class="sxs-lookup"><span data-stu-id="23aed-133">PositionType</span></span>
- <span data-ttu-id="23aed-134">CompLocation</span><span class="sxs-lookup"><span data-stu-id="23aed-134">CompLocation</span></span>
- <span data-ttu-id="23aed-135">Ünvan</span><span class="sxs-lookup"><span data-stu-id="23aed-135">Title</span></span>
- <span data-ttu-id="23aed-136">İş</span><span class="sxs-lookup"><span data-stu-id="23aed-136">Job</span></span>
- <span data-ttu-id="23aed-137">JobType</span><span class="sxs-lookup"><span data-stu-id="23aed-137">JobType</span></span>
- <span data-ttu-id="23aed-138">JobFamily</span><span class="sxs-lookup"><span data-stu-id="23aed-138">JobFamily</span></span>
- <span data-ttu-id="23aed-139">JobFunction</span><span class="sxs-lookup"><span data-stu-id="23aed-139">JobFunction</span></span>

<span data-ttu-id="23aed-140">Aşağıdaki alanlar konum iş akışına eklendi:</span><span class="sxs-lookup"><span data-stu-id="23aed-140">The following fields have been added to the position workflow:</span></span>

- <span data-ttu-id="23aed-141">Bölme</span><span class="sxs-lookup"><span data-stu-id="23aed-141">Position</span></span>
- <span data-ttu-id="23aed-142">Birlik</span><span class="sxs-lookup"><span data-stu-id="23aed-142">Union</span></span>
- <span data-ttu-id="23aed-143">Departman</span><span class="sxs-lookup"><span data-stu-id="23aed-143">Department</span></span>
- <span data-ttu-id="23aed-144">PositionType</span><span class="sxs-lookup"><span data-stu-id="23aed-144">PositionType</span></span>
- <span data-ttu-id="23aed-145">CompLocation</span><span class="sxs-lookup"><span data-stu-id="23aed-145">CompLocation</span></span>
- <span data-ttu-id="23aed-146">Ünvan</span><span class="sxs-lookup"><span data-stu-id="23aed-146">Title</span></span>
- <span data-ttu-id="23aed-147">İş</span><span class="sxs-lookup"><span data-stu-id="23aed-147">Job</span></span>
- <span data-ttu-id="23aed-148">JobType</span><span class="sxs-lookup"><span data-stu-id="23aed-148">JobType</span></span>
- <span data-ttu-id="23aed-149">JobFamily</span><span class="sxs-lookup"><span data-stu-id="23aed-149">JobFamily</span></span>
- <span data-ttu-id="23aed-150">JobFunction</span><span class="sxs-lookup"><span data-stu-id="23aed-150">JobFunction</span></span>

<span data-ttu-id="23aed-151">Koşul ifadelerindeki alanlar ve yer tutucular, önceden belirtilen iş akışlarını düzenlemeye erişime sahip tüm kullanıcılara açıktır.</span><span class="sxs-lookup"><span data-stu-id="23aed-151">Fields in conditional statements and placeholders are available to all users who have access to configure the previously mentioned workflows.</span></span>

## <a name="navigation-to-attract-from-personnel-management"></a><span data-ttu-id="23aed-152">Kişisel yönetimden Attract'e gezinti</span><span class="sxs-lookup"><span data-stu-id="23aed-152">Navigation to Attract from personnel management</span></span>

<span data-ttu-id="23aed-153">Personel yönetiminde, Attract kurulmamışsa, **İşe alım adayları** bölümü, kullanıcıları "Burada gösterecek bir şey bulamadık" mesajı yerine Attract kullanmaya başlamaya yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="23aed-153">In personnel management, if Attract hasn't been set up, the **Candidates to hire** section directs users to get started with Attract instead of showing the message, "We didn't find anything to show here."</span></span>

## <a name="other-changes"></a><span data-ttu-id="23aed-154">Diğer değişimler</span><span class="sxs-lookup"><span data-stu-id="23aed-154">Other changes</span></span>

<span data-ttu-id="23aed-155">Bu sürüm çeşitli hatalara yönelik düzeltmeler içerir:</span><span class="sxs-lookup"><span data-stu-id="23aed-155">This release includes several additional bug fixes:</span></span>

- <span data-ttu-id="23aed-156">Bir alt yüklenici işe alındığında **Ücret** sekmesi, istek/eylem sayfasında kullanılabilir olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="23aed-156">When a contractor is hired, the **Compensation** tab should not be available on the request/action page.</span></span>
- <span data-ttu-id="23aed-157">İstek sonlandırma işleminde, tüm alanlar veri içerene kadar devam edemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="23aed-157">During the request termination process, you can't continue until all required fields contain data.</span></span>
- <span data-ttu-id="23aed-158">Personel yönetimi analizlerindeki sıralama düzeni ve tarih göstergesi sorunları giderilmiştir.</span><span class="sxs-lookup"><span data-stu-id="23aed-158">Sort order and date display issues on the Personnel management analytics have been addressed.</span></span>
