---
title: Kapsam seçeneklerini oluşturma
description: ''
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
ms.openlocfilehash: 27b43d858a92beac526ac0fc40b544649ef658b0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010808"
---
# <a name="create-coverage-options"></a><span data-ttu-id="1dd4b-102">Kapsam seçeneklerini oluşturma</span><span class="sxs-lookup"><span data-stu-id="1dd4b-102">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="1dd4b-103">Microsoft Dynamics 365 Human Resources içindeki kapsam seçenekleri, bir kişinin yalnızca tıbbi plan için çalışan veya bir ömür sigortası planı Için 2x maaş gibi bir kazanç planında veya programında yer alanın kapsam düzeyleridir.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-103">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="1dd4b-104">Tanımlandıktan sonra, kazanç karşılama seçenekleri yeniden kullanılabilir ve bir seçeneği bir veya daha fazla plan ile ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-104">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="1dd4b-105">Kapsam seçenekleri tanımlandıktan sonra, karşılama seçeneklerini bir kazanç planı türüne iliştirin.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-105">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="1dd4b-106">Plan türü daha sonra bir kazanç planıyla veya programla ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-106">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="1dd4b-107">Bir plan tipiyle ilişkilendirilmiş olan kapsam seçenekleri, bu plan türü ile oluşturulan tüm planlar tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-107">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="1dd4b-108">**Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Kapsam seçenekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-108">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="1dd4b-109">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-109">Select **New**.</span></span>

3. <span data-ttu-id="1dd4b-110">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="1dd4b-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="1dd4b-111">Alan</span><span class="sxs-lookup"><span data-stu-id="1dd4b-111">Field</span></span> | <span data-ttu-id="1dd4b-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="1dd4b-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1dd4b-113">**Karşılama seçeneği**</span><span class="sxs-lookup"><span data-stu-id="1dd4b-113">**Coverage option**</span></span> | <span data-ttu-id="1dd4b-114">Benzersiz bir karşılama seçeneği adı.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-114">A unique coverage option name.</span></span> |
   | <span data-ttu-id="1dd4b-115">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="1dd4b-115">**Description**</span></span> | <span data-ttu-id="1dd4b-116">Kapsam seçeneği için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-116">A description of the coverage option.</span></span> |
   | <span data-ttu-id="1dd4b-117">**Karşılama kodu**</span><span class="sxs-lookup"><span data-stu-id="1dd4b-117">**Coverage code**</span></span> | <span data-ttu-id="1dd4b-118">Karşılama kodları, uygun olan her kişi türü için minimum ve maksimum tutarları atar.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-118">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="1dd4b-119">Bir karşılama kodu, bir plan türü için izin verilen kapsam miktarını veya kapsamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-119">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="1dd4b-120">Tedarik tutarını YTL tutarı veya yüzde olarak ifade edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-120">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="1dd4b-121">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="1dd4b-121">For example:</span></span></br></br><span data-ttu-id="1dd4b-122">- **Çalışan+1** – nitelikli olması için çalışanın bir bağımlı seçili olması gerekir (birden fazla seçili ise, artık uygun olmayacaktır).</span><span class="sxs-lookup"><span data-stu-id="1dd4b-122">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="1dd4b-123">- **Çalışan + aile** – nitelikli olması için çalışanın en az iki yanındaki seçilmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-123">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="1dd4b-124">**Maksimum sayı**</span><span class="sxs-lookup"><span data-stu-id="1dd4b-124">**Maximum number**</span></span> | <span data-ttu-id="1dd4b-125">Maksimum bağımlı sayısı</span><span class="sxs-lookup"><span data-stu-id="1dd4b-125">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="1dd4b-126">**Durum**</span><span class="sxs-lookup"><span data-stu-id="1dd4b-126">**Status**</span></span> | <span data-ttu-id="1dd4b-127">Kapsam seçeneği durumu.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-127">The status of the coverage option.</span></span> <span data-ttu-id="1dd4b-128">Kapsam seçeneğinin durumu etkin değil olarak ayarlandıysa, tedarik seçeneği plan türlerinde seçilemez.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-128">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="1dd4b-129">**Yüzde**</span><span class="sxs-lookup"><span data-stu-id="1dd4b-129">**Percent**</span></span> | <span data-ttu-id="1dd4b-130">Yüzde tutarı.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-130">The percent amount.</span></span> <span data-ttu-id="1dd4b-131">Bu alan yalnızca, Kapsam kodu alanında % x maaş seçilmişse etkindir.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-131">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="1dd4b-132">**Bölen**</span><span class="sxs-lookup"><span data-stu-id="1dd4b-132">**Divisor**</span></span> | <span data-ttu-id="1dd4b-133">% X maaş kapsam kodunu seçtiğinizde hesaplamada kullanılacak bölen.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-133">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="1dd4b-134">**Minimum yüzde**</span><span class="sxs-lookup"><span data-stu-id="1dd4b-134">**Percent minimum**</span></span> | <span data-ttu-id="1dd4b-135">Yüzde kapsam kodunu seçtiğinizde minimum yüzde.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-135">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="1dd4b-136">**Maksimum yüzde**</span><span class="sxs-lookup"><span data-stu-id="1dd4b-136">**Percent maximum**</span></span> | <span data-ttu-id="1dd4b-137">Yüzde kapsam kodunu seçtiğinizde maksimum yüzde.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-137">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="1dd4b-138">**Kişisel ilgili kişi uygunluğu seçenekleri** altında, her kapsam seçeneğine uygun özel ilgili kişiler uygunluk seçeneğini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-138">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="1dd4b-139">**Self servis** altında, aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="1dd4b-139">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="1dd4b-140">Alan</span><span class="sxs-lookup"><span data-stu-id="1dd4b-140">Field</span></span> | <span data-ttu-id="1dd4b-141">Tanım</span><span class="sxs-lookup"><span data-stu-id="1dd4b-141">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1dd4b-142">**Personel katkı tutarına izin ver**</span><span class="sxs-lookup"><span data-stu-id="1dd4b-142">**Allow employee contribution amount**</span></span> | <span data-ttu-id="1dd4b-143">Sosyal haklar seçildiğinde, çalışanların, kazançlar self servis durumunda katkı tutarını değiştirmesine izin verip vermeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-143">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="1dd4b-144">Bu onay kutusunu seçerseniz, sistem, sosyal haklar self servis üzerine girdiği katkı tutarını temel alarak, kazanç planı parametrelerini hesaplar.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-144">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="1dd4b-145">**Personel karşılama tutarına izin ver**</span><span class="sxs-lookup"><span data-stu-id="1dd4b-145">**Allow employee coverage amount**</span></span> | <span data-ttu-id="1dd4b-146">Sosyal haklar seçildiğinde, çalışanların, kazançlar self servis durumunda kapsam tutarını değiştirmesine izin verip vermeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-146">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="1dd4b-147">Bu onay kutusunu seçerseniz, sistem, personel self servis üzerine girdiği kapsam tutarını temel alarak, kazanç planı parametrelerini hesaplar.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-147">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="1dd4b-148">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1dd4b-148">Select **Save**.</span></span> 
