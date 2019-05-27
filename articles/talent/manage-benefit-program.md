---
title: Bir kazançlar programı tanımlama ve yönetme
description: İnsan kaynakları bir organizasyonun sunduğu veya çalışanları için yürürlüğe koyduğu kazançları, kesintileri ve çalışanların tazminat planlarını oluşturmak ve bunları yönetmek için kullanılabilecek bir takım araçlar sağlar. Bu makalede bir kazanç yönetiminin nasıl kurulacağı hakkında bilgiler verilmiştir.
author: andreabichsel
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 033377f7d45bfa2b798c098be2dde0c21739bb51
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519355"
---
# <a name="define-and-manage-a-benefits-program"></a><span data-ttu-id="243a0-104">Bir kazançlar programı tanımlama ve yönetme</span><span class="sxs-lookup"><span data-stu-id="243a0-104">Define and manage a benefits program</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="243a0-105">İnsan kaynakları bir organizasyonun sunduğu veya çalışanları için yürürlüğe koyduğu kazançları, kesintileri ve çalışanların tazminat planlarını oluşturmak ve bunları yönetmek için kullanılabilecek bir takım araçlar sağlar.</span><span class="sxs-lookup"><span data-stu-id="243a0-105">Human resources provides a set of tools that can be used to set up and maintain benefits, deductions, and workers' compensation plans that an organization offers or processes for its workers.</span></span> <span data-ttu-id="243a0-106">Bu konuda kazançların nasıl kurulacağı ve yönetileceği hakkında bilgiler verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="243a0-106">This topic provides information about how to set up and manage benefits.</span></span>

<a name="benefit-setup"></a><span data-ttu-id="243a0-107">Kazanç kurulumu</span><span class="sxs-lookup"><span data-stu-id="243a0-107">Benefit setup</span></span>
-------------

<span data-ttu-id="243a0-108">Çalışanları bir kazanca kaydetmeden önce her bir kazanç için öğeler oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="243a0-108">Before workers can be enrolled in benefits, you must create the elements of each benefit.</span></span> <span data-ttu-id="243a0-109">Bu öğeler benzer kazanç planlarını birleştirir ve indirim oranları ve muhasebe ayrıntıları vb. gibi varsayılan ayarları tanımlar.</span><span class="sxs-lookup"><span data-stu-id="243a0-109">These elements combine similar benefit plans and define default settings, such as deduction rates and accounting details.</span></span> <span data-ttu-id="243a0-110">Bu ayarların birçoğu, çalışanlar daha sonra kazanda kaydedildiklerinde ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="243a0-110">Many of these settings can be adjusted when workers are later enrolled in the benefit.</span></span> <span data-ttu-id="243a0-111">Bir organizasyon, her bir kazanç planı için birden fazla kayıt seçeneği sunabilir veya bir çalışan, plana kaydolmaktan feragat edebilir.</span><span class="sxs-lookup"><span data-stu-id="243a0-111">For each benefit plan, an organization can offer several enrollment options, or a worker can waive enrollment in the plan.</span></span> 

<span data-ttu-id="243a0-112">[![Kazanç süreç akışı](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span><span class="sxs-lookup"><span data-stu-id="243a0-112">[![Benefit process flow](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span></span>

## <a name="benefit-elements"></a><span data-ttu-id="243a0-113">Kazanç öğeleri</span><span class="sxs-lookup"><span data-stu-id="243a0-113">Benefit elements</span></span>
<span data-ttu-id="243a0-114">Kazançlar oluşturmadan ve çalışanları bu kazançlara kaydetmeden önce, kazancı meydana getirecek öğeleri tanımlamanız gerekir: tür, plan ve seçenekler.</span><span class="sxs-lookup"><span data-stu-id="243a0-114">Before you begin to create to create benefits and enroll workers in them, you must define the elements that make up a benefit: the type, plan, and options.</span></span>

-   <span data-ttu-id="243a0-115">**Tür** – Örneğin tıbbi veya otopark vb. gibi belirli bir kazanç için bir planlar topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="243a0-115">**Type** – A collection of plans for a specific benefit, such as medical or parking.</span></span>
-   <span data-ttu-id="243a0-116">**Plan** – Bir sağlayıcıdan sözleşme yapılarak alınan, özel bir kazançtır.</span><span class="sxs-lookup"><span data-stu-id="243a0-116">**Plan** – A specific benefit that is contracted from a provider.</span></span>
-   <span data-ttu-id="243a0-117">**Seçenek** – Sadece çalışanlar veya çalışanlar ve eşleri/partnerleri gibi kapsam düzeyi.</span><span class="sxs-lookup"><span data-stu-id="243a0-117">**Option** – The coverage level, such as employee only, or employee and spouse/partner.</span></span>

<span data-ttu-id="243a0-118">Bir organizasyon göz tedavileri veya diş tedavileri vb. gibi her bir kazanç türü için çalışanlarına bir veya birden fazla plan sunabilir.</span><span class="sxs-lookup"><span data-stu-id="243a0-118">For each type of benefit, such as vision or dental, an organization can offer one or more plans to its workers.</span></span> <span data-ttu-id="243a0-119">Her bir plan için organizasyon farklı seçenekler sunabilir.</span><span class="sxs-lookup"><span data-stu-id="243a0-119">For each plan, the organization can offer different options.</span></span> <span data-ttu-id="243a0-120">Örneğin, çalışanlar yıllık kazançlarının bir, iki veya üç katına kadar ilave hayat sigortası kapsamı satın alabilirler.</span><span class="sxs-lookup"><span data-stu-id="243a0-120">For example, workers can buy additional term life insurance coverage at one, two, or three times their yearly salary.</span></span> <span data-ttu-id="243a0-121">Her bir plan kombinasyonu ve seçenekler, çalışanların kaydolabileceği bir kazanç haline gelir.</span><span class="sxs-lookup"><span data-stu-id="243a0-121">Each combination of a plan and options becomes a benefit that workers can enroll in.</span></span> 

<span data-ttu-id="243a0-122">[![kazanç fotoğrafı](./media/benefit-pic.png)](./media/benefit-pic.png)</span><span class="sxs-lookup"><span data-stu-id="243a0-122">[![benefit pic](./media/benefit-pic.png)](./media/benefit-pic.png)</span></span>

## <a name="eligibility"></a><span data-ttu-id="243a0-123">Uygunluk</span><span class="sxs-lookup"><span data-stu-id="243a0-123">Eligibility</span></span>
<span data-ttu-id="243a0-124">Bir işverenin sunduğu çeşitli kazanç türleri için çalışanın uygunluğunu belirleyen çok sayıda faktör bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="243a0-124">Many factors determine worker eligibility for the various types of benefits that an employer offers.</span></span> <span data-ttu-id="243a0-125">Microsoft Talent'da bir kazanç oluşturduğunuzda, bu kazanç için geçerli uygunluk türünü ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="243a0-125">When you create a benefit in Microsoft Talent, you can set the type of eligibility that applies to that benefit.</span></span> 

<span data-ttu-id="243a0-126">Kazançları tüm çalışanlar için kullanılabilir kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="243a0-126">You can make a benefit available to all workers.</span></span> <span data-ttu-id="243a0-127">Örneğin, bazı şirketler park izinlerini tüm çalışanlara bir yan kazanç olarak sunar.</span><span class="sxs-lookup"><span data-stu-id="243a0-127">For example, some companies offer parking passes to all employees as a fringe benefit.</span></span> <span data-ttu-id="243a0-128">Bu kazancı oluşturduğunuzda uygunluğu **Tüm çalışanlar uygundur** olarak ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="243a0-128">When you create this benefit, you set the eligibility to **All workers are eligible**.</span></span> 

<span data-ttu-id="243a0-129">Maaş haczi ve vergi koyma gibi diğer kazançlar için, uygunluk uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="243a0-129">For other benefits, such as garnishments and tax levies, eligibility doesn't apply.</span></span> <span data-ttu-id="243a0-130">Bu tür kazançlar oluşturduğunuzda, uygunluğu **Uygunluk işlemini atla** olarak ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="243a0-130">Whey you create these types of benefits, you set the eligibility to **Bypass eligibility process**.</span></span> 

<span data-ttu-id="243a0-131">Son olarak, kazanç uygunluğu kural tabanlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="243a0-131">Finally, benefit eligibility can be rule-based.</span></span> <span data-ttu-id="243a0-132">Örneğin, şirket çalışanları için iki türde hayat sigortası kazancı sunar.</span><span class="sxs-lookup"><span data-stu-id="243a0-132">For example, a company offers two types of life insurance benefit to employees.</span></span> <span data-ttu-id="243a0-133">Yönetici personel bir hayat sigortası planında hak sahibiyken, diğer tüm tam zamanlı personel diğer hayat sigortası planına hak sahibidir.</span><span class="sxs-lookup"><span data-stu-id="243a0-133">Executive employees are eligible for one life insurance plan, whereas all other full-time employees are eligible for the other life insurance plan.</span></span> <span data-ttu-id="243a0-134">Talent içerisinde, tüm yönetici personeli bulmak için bir kural ve diğer tüm tam zamanlı personeli bulmak için başka bir kural oluşturabilirsiniz ve bunları daha sonra uygun kazanca uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="243a0-134">In Talent, you can create a benefit eligibility rule to find all executive employees and another rule to find all other full-time employees, and then apply those rules to the appropriate benefit.</span></span>

## <a name="enrollment"></a><span data-ttu-id="243a0-135">Kayıt</span><span class="sxs-lookup"><span data-stu-id="243a0-135">Enrollment</span></span>
<span data-ttu-id="243a0-136">Organizasyonunuzun sunduğu kazançları oluşturduktan ve uygunluğu belirledikten sonra çalışanları bu kazançlara kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="243a0-136">After you've created the benefits that your organization offers and determined eligibility, you can enroll your workers in benefits.</span></span> <span data-ttu-id="243a0-137">Kazançları tek bir çalışanı kaydedebileceğiniz gibi, tek bir süreçle çok sayıda çalışanı bir veya daha fazla sayıdaki kazanca da kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="243a0-137">You can enroll a single worker in benefits, or you can enroll many workers in one or more benefits during a single process.</span></span> 

<span data-ttu-id="243a0-138">Bazı durumlarda bir organizasyon belirli kazançları durdurur.</span><span class="sxs-lookup"><span data-stu-id="243a0-138">Sometimes, an organization stops offering certain benefits.</span></span> <span data-ttu-id="243a0-139">Bu durumda, kazancı ve katılım gösteren çalışanları güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="243a0-139">In this case, you must update the benefit and the workers who are enrolled in.</span></span> <span data-ttu-id="243a0-140">Toplu yarar sona erdirme, hem kazancın hem de bu kazanç için çalışan katılımlarının bitiş tarihini aynı zamanda değiştirmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="243a0-140">Mass benefit expiration lets you change the expiration date of both a benefit and the worker enrollments for that benefit at the same time.</span></span> <span data-ttu-id="243a0-141">Ayrıca, bir kazanca kayıtlı birden fazla çalışanı seçebilir ve kapsamlarının bitiş tarihini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="243a0-141">You can also select multiple workers who are enrolled in a benefit and change the ending date of their coverage.</span></span> 

<span data-ttu-id="243a0-142">Benzer şekilde, toplu kazanç uzatma özelliği, bir kazancı başlangıçta planladığınızdan daha uzun süre sunmaya karar verdiğinizde hem bu kazancın hem de bu kazanca kayıtlı çalışanların geçerlilik bitiş tarihini uzatmanıza izin verir.</span><span class="sxs-lookup"><span data-stu-id="243a0-142">Similarly, mass benefit extension lets you extend the expiration date of both a benefit and the worker enrollments for that benefit if you decide to offer a benefit longer than you originally planned.</span></span>

<a name="additional-resources"></a><span data-ttu-id="243a0-143">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="243a0-143">Additional resources</span></span>
--------

[<span data-ttu-id="243a0-144">Kazanca uygunluk ilkeleri</span><span class="sxs-lookup"><span data-stu-id="243a0-144">Benefit eligibility policies</span></span>](benefit-eligibility-policies.md)



