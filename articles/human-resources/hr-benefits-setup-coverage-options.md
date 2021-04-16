---
title: Kapsam seçeneklerini oluşturma
description: Microsoft Dynamics 365 Human Resources'taki karşılama seçenekleri, bir kazanç planında veya programında bir katılımcının seçimi için kapsam düzeyleridir.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d304b0cf65c7833ebc7f21323efc59540289de8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803693"
---
# <a name="create-coverage-options"></a><span data-ttu-id="5ee6d-103">Kapsam seçeneklerini oluşturma</span><span class="sxs-lookup"><span data-stu-id="5ee6d-103">Create coverage options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5ee6d-104">Microsoft Dynamics 365 Human Resources'taki karşılama seçenekleri, bir kazanç planında veya programında bir katılımcının seçimi için kapsam düzeyleridir.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program.</span></span> <span data-ttu-id="5ee6d-105">Örneğin, kapsam seçenekleri tıbbi bir plan için **Yalnızca Personel** veya bir hayat sigortası planı için **2x Maaş** içerebilir.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-105">For example, coverage options could include **Employee Only** for a medical plan, or **2x Salary** for a life insurance plan.</span></span> <span data-ttu-id="5ee6d-106">Tanımlandıktan sonra, kazanç kapsamı seçeneklerini yeniden kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-106">Once defined, you can reuse benefit coverage options.</span></span> <span data-ttu-id="5ee6d-107">Bir seçeneği bir veya daha fazla planla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-107">You can associate an option with one or more plans.</span></span>

<span data-ttu-id="5ee6d-108">Kapsam seçeneklerini tanımladıktan sonra, karşılama seçeneklerini bir kazanç planı türüne ekleyin.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-108">After you define coverage options, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="5ee6d-109">Plan türü daha sonra bir kazanç planıyla veya programla ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-109">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="5ee6d-110">Bir plan tipiyle ilişkilendirilmiş olan kapsam seçenekleri, bu plan türü ile oluşturulan tüm planlar tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-110">Coverage options that are associated with a plan type are available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="5ee6d-111">**Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Kapsam seçenekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-111">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="5ee6d-112">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-112">Select **New**.</span></span>

3. <span data-ttu-id="5ee6d-113">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="5ee6d-113">Specify values for the following fields:</span></span>

   | <span data-ttu-id="5ee6d-114">Alan</span><span class="sxs-lookup"><span data-stu-id="5ee6d-114">Field</span></span> | <span data-ttu-id="5ee6d-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ee6d-115">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5ee6d-116">**Karşılama seçeneği**</span><span class="sxs-lookup"><span data-stu-id="5ee6d-116">**Coverage option**</span></span> | <span data-ttu-id="5ee6d-117">Benzersiz bir karşılama seçeneği adı.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-117">A unique coverage option name.</span></span> |
   | <span data-ttu-id="5ee6d-118">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="5ee6d-118">**Description**</span></span> | <span data-ttu-id="5ee6d-119">Kapsam seçeneği için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-119">A description of the coverage option.</span></span> |
   | <span data-ttu-id="5ee6d-120">**Karşılama kodu**</span><span class="sxs-lookup"><span data-stu-id="5ee6d-120">**Coverage code**</span></span> | <span data-ttu-id="5ee6d-121">Karşılama kodları, uygun olan her kişi türü için minimum ve maksimum tutarları atar.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-121">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="5ee6d-122">Bir karşılama kodu, bir plan türü için izin verilen kapsam miktarını veya kapsamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-122">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="5ee6d-123">Tedarik tutarını YTL tutarı veya yüzde olarak ifade edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-123">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="5ee6d-124">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="5ee6d-124">For example:</span></span></br></br><span data-ttu-id="5ee6d-125">- **Çalışan+1** – nitelikli olması için çalışanın bir bağımlı seçili olması gerekir (birden fazla seçili ise, artık uygun olmayacaktır).</span><span class="sxs-lookup"><span data-stu-id="5ee6d-125">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="5ee6d-126">- **Çalışan + aile** – nitelikli olması için çalışanın en az iki yanındaki seçilmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-126">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="5ee6d-127">**Maksimum sayı**</span><span class="sxs-lookup"><span data-stu-id="5ee6d-127">**Maximum number**</span></span> | <span data-ttu-id="5ee6d-128">Maksimum bağımlı sayısı</span><span class="sxs-lookup"><span data-stu-id="5ee6d-128">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="5ee6d-129">**Durum**</span><span class="sxs-lookup"><span data-stu-id="5ee6d-129">**Status**</span></span> | <span data-ttu-id="5ee6d-130">Kapsam seçeneği durumu.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-130">The status of the coverage option.</span></span> <span data-ttu-id="5ee6d-131">Kapsam seçeneğinin durumu etkin değil olarak ayarlandıysa, tedarik seçeneği plan türlerinde seçilemez.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-131">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="5ee6d-132">**Yüzde**</span><span class="sxs-lookup"><span data-stu-id="5ee6d-132">**Percent**</span></span> | <span data-ttu-id="5ee6d-133">Yüzde tutarı.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-133">The percent amount.</span></span> <span data-ttu-id="5ee6d-134">Bu alan yalnızca, Kapsam kodu alanında % x maaş seçilmişse etkindir.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-134">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="5ee6d-135">**Bölen**</span><span class="sxs-lookup"><span data-stu-id="5ee6d-135">**Divisor**</span></span> | <span data-ttu-id="5ee6d-136">% X maaş kapsam kodunu seçtiğinizde hesaplamada kullanılacak bölen.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-136">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="5ee6d-137">**Minimum yüzde**</span><span class="sxs-lookup"><span data-stu-id="5ee6d-137">**Percent minimum**</span></span> | <span data-ttu-id="5ee6d-138">Yüzde kapsam kodunu seçtiğinizde minimum yüzde.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-138">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="5ee6d-139">**Maksimum yüzde**</span><span class="sxs-lookup"><span data-stu-id="5ee6d-139">**Percent maximum**</span></span> | <span data-ttu-id="5ee6d-140">Yüzde kapsam kodunu seçtiğinizde maksimum yüzde.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-140">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="5ee6d-141">**Kişisel ilgili kişi uygunluğu seçenekleri** altında, her kapsam seçeneğine uygun özel ilgili kişiler uygunluk seçeneğini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-141">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="5ee6d-142">**Self servis** altında, aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="5ee6d-142">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="5ee6d-143">Alan</span><span class="sxs-lookup"><span data-stu-id="5ee6d-143">Field</span></span> | <span data-ttu-id="5ee6d-144">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ee6d-144">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5ee6d-145">**Personel katkı tutarına izin ver**</span><span class="sxs-lookup"><span data-stu-id="5ee6d-145">**Allow employee contribution amount**</span></span> | <span data-ttu-id="5ee6d-146">Sosyal haklar seçildiğinde, çalışanların, kazançlar self servis durumunda katkı tutarını değiştirmesine izin verip vermeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-146">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="5ee6d-147">Bu onay kutusunu seçerseniz, sistem, sosyal haklar self servis üzerine girdiği katkı tutarını temel alarak, kazanç planı parametrelerini hesaplar.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-147">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="5ee6d-148">**Personel karşılama tutarına izin ver**</span><span class="sxs-lookup"><span data-stu-id="5ee6d-148">**Allow employee coverage amount**</span></span> | <span data-ttu-id="5ee6d-149">Sosyal haklar seçildiğinde, çalışanların, kazançlar self servis durumunda kapsam tutarını değiştirmesine izin verip vermeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-149">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="5ee6d-150">Bu onay kutusunu seçerseniz, sistem, personel self servis üzerine girdiği kapsam tutarını temel alarak, kazanç planı parametrelerini hesaplar.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-150">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="5ee6d-151">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5ee6d-151">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]