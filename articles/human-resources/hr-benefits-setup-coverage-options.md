---
title: Kapsam seçeneklerini oluşturma
description: Microsoft Dynamics 365 Human Resources içindeki kapsam seçenekleri, bir kişinin yalnızca tıbbi plan için çalışan veya bir ömür sigortası planı Için 2x maaş gibi bir kazanç planında veya programında yer alanın kapsam düzeyleridir.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0af2b6ae0853b4c7f64c4d4f04299c87089d622b
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092718"
---
# <a name="create-coverage-options"></a><span data-ttu-id="46e57-103">Kapsam seçeneklerini oluşturma</span><span class="sxs-lookup"><span data-stu-id="46e57-103">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="46e57-104">Microsoft Dynamics 365 Human Resources içindeki kapsam seçenekleri, bir kişinin yalnızca tıbbi plan için çalışan veya bir ömür sigortası planı Için 2x maaş gibi bir kazanç planında veya programında yer alanın kapsam düzeyleridir.</span><span class="sxs-lookup"><span data-stu-id="46e57-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="46e57-105">Tanımlandıktan sonra, kazanç karşılama seçenekleri yeniden kullanılabilir ve bir seçeneği bir veya daha fazla plan ile ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46e57-105">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="46e57-106">Kapsam seçenekleri tanımlandıktan sonra, karşılama seçeneklerini bir kazanç planı türüne iliştirin.</span><span class="sxs-lookup"><span data-stu-id="46e57-106">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="46e57-107">Plan türü daha sonra bir kazanç planıyla veya programla ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="46e57-107">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="46e57-108">Bir plan tipiyle ilişkilendirilmiş olan kapsam seçenekleri, bu plan türü ile oluşturulan tüm planlar tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="46e57-108">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="46e57-109">**Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Kapsam seçenekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="46e57-109">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="46e57-110">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="46e57-110">Select **New**.</span></span>

3. <span data-ttu-id="46e57-111">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="46e57-111">Specify values for the following fields:</span></span>

   | <span data-ttu-id="46e57-112">Alan</span><span class="sxs-lookup"><span data-stu-id="46e57-112">Field</span></span> | <span data-ttu-id="46e57-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="46e57-113">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="46e57-114">**Karşılama seçeneği**</span><span class="sxs-lookup"><span data-stu-id="46e57-114">**Coverage option**</span></span> | <span data-ttu-id="46e57-115">Benzersiz bir karşılama seçeneği adı.</span><span class="sxs-lookup"><span data-stu-id="46e57-115">A unique coverage option name.</span></span> |
   | <span data-ttu-id="46e57-116">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="46e57-116">**Description**</span></span> | <span data-ttu-id="46e57-117">Kapsam seçeneği için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="46e57-117">A description of the coverage option.</span></span> |
   | <span data-ttu-id="46e57-118">**Karşılama kodu**</span><span class="sxs-lookup"><span data-stu-id="46e57-118">**Coverage code**</span></span> | <span data-ttu-id="46e57-119">Karşılama kodları, uygun olan her kişi türü için minimum ve maksimum tutarları atar.</span><span class="sxs-lookup"><span data-stu-id="46e57-119">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="46e57-120">Bir karşılama kodu, bir plan türü için izin verilen kapsam miktarını veya kapsamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="46e57-120">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="46e57-121">Tedarik tutarını YTL tutarı veya yüzde olarak ifade edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46e57-121">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="46e57-122">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="46e57-122">For example:</span></span></br></br><span data-ttu-id="46e57-123">- **Çalışan+1** – nitelikli olması için çalışanın bir bağımlı seçili olması gerekir (birden fazla seçili ise, artık uygun olmayacaktır).</span><span class="sxs-lookup"><span data-stu-id="46e57-123">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="46e57-124">- **Çalışan + aile** – nitelikli olması için çalışanın en az iki yanındaki seçilmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="46e57-124">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="46e57-125">**Maksimum sayı**</span><span class="sxs-lookup"><span data-stu-id="46e57-125">**Maximum number**</span></span> | <span data-ttu-id="46e57-126">Maksimum bağımlı sayısı</span><span class="sxs-lookup"><span data-stu-id="46e57-126">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="46e57-127">**Durum**</span><span class="sxs-lookup"><span data-stu-id="46e57-127">**Status**</span></span> | <span data-ttu-id="46e57-128">Kapsam seçeneği durumu.</span><span class="sxs-lookup"><span data-stu-id="46e57-128">The status of the coverage option.</span></span> <span data-ttu-id="46e57-129">Kapsam seçeneğinin durumu etkin değil olarak ayarlandıysa, tedarik seçeneği plan türlerinde seçilemez.</span><span class="sxs-lookup"><span data-stu-id="46e57-129">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="46e57-130">**Yüzde**</span><span class="sxs-lookup"><span data-stu-id="46e57-130">**Percent**</span></span> | <span data-ttu-id="46e57-131">Yüzde tutarı.</span><span class="sxs-lookup"><span data-stu-id="46e57-131">The percent amount.</span></span> <span data-ttu-id="46e57-132">Bu alan yalnızca, Kapsam kodu alanında % x maaş seçilmişse etkindir.</span><span class="sxs-lookup"><span data-stu-id="46e57-132">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="46e57-133">**Bölen**</span><span class="sxs-lookup"><span data-stu-id="46e57-133">**Divisor**</span></span> | <span data-ttu-id="46e57-134">% X maaş kapsam kodunu seçtiğinizde hesaplamada kullanılacak bölen.</span><span class="sxs-lookup"><span data-stu-id="46e57-134">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="46e57-135">**Minimum yüzde**</span><span class="sxs-lookup"><span data-stu-id="46e57-135">**Percent minimum**</span></span> | <span data-ttu-id="46e57-136">Yüzde kapsam kodunu seçtiğinizde minimum yüzde.</span><span class="sxs-lookup"><span data-stu-id="46e57-136">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="46e57-137">**Maksimum yüzde**</span><span class="sxs-lookup"><span data-stu-id="46e57-137">**Percent maximum**</span></span> | <span data-ttu-id="46e57-138">Yüzde kapsam kodunu seçtiğinizde maksimum yüzde.</span><span class="sxs-lookup"><span data-stu-id="46e57-138">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="46e57-139">**Kişisel ilgili kişi uygunluğu seçenekleri** altında, her kapsam seçeneğine uygun özel ilgili kişiler uygunluk seçeneğini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="46e57-139">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="46e57-140">**Self servis** altında, aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="46e57-140">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="46e57-141">Alan</span><span class="sxs-lookup"><span data-stu-id="46e57-141">Field</span></span> | <span data-ttu-id="46e57-142">Tanım</span><span class="sxs-lookup"><span data-stu-id="46e57-142">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="46e57-143">**Personel katkı tutarına izin ver**</span><span class="sxs-lookup"><span data-stu-id="46e57-143">**Allow employee contribution amount**</span></span> | <span data-ttu-id="46e57-144">Sosyal haklar seçildiğinde, çalışanların, kazançlar self servis durumunda katkı tutarını değiştirmesine izin verip vermeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46e57-144">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="46e57-145">Bu onay kutusunu seçerseniz, sistem, sosyal haklar self servis üzerine girdiği katkı tutarını temel alarak, kazanç planı parametrelerini hesaplar.</span><span class="sxs-lookup"><span data-stu-id="46e57-145">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="46e57-146">**Personel karşılama tutarına izin ver**</span><span class="sxs-lookup"><span data-stu-id="46e57-146">**Allow employee coverage amount**</span></span> | <span data-ttu-id="46e57-147">Sosyal haklar seçildiğinde, çalışanların, kazançlar self servis durumunda kapsam tutarını değiştirmesine izin verip vermeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46e57-147">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="46e57-148">Bu onay kutusunu seçerseniz, sistem, personel self servis üzerine girdiği kapsam tutarını temel alarak, kazanç planı parametrelerini hesaplar.</span><span class="sxs-lookup"><span data-stu-id="46e57-148">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="46e57-149">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="46e57-149">Select **Save**.</span></span> 
