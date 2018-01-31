---
title: Kazanca uygunluk ilkeleri
description: "Bu makalede, kazanç uygunluk ilkeleri hakkında, belirli kazançlara uygun olan kişileri tanımlamanıza yardımcı olacak bilgiler verilmektedir."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 5c0af3d9446b4f8ae80eeb44494f1ef1e6667e55
ms.contentlocale: tr-tr
ms.lasthandoff: 01/31/2018

---

# <a name="benefit-eligibility-policies"></a><span data-ttu-id="38bd2-103">Kazanca uygunluk ilkeleri</span><span class="sxs-lookup"><span data-stu-id="38bd2-103">Benefit eligibility policies</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="38bd2-104">Bu konu, kazanç uygunluk ilkeleri hakkında, belirli kazançlara uygun olan kişileri tanımlamanıza yardımcı olacak bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="38bd2-104">This topic provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="38bd2-105">Kazançlar oluşturduğunuzda hangi kazançların hangi çalışanlar için geçerli olacağına karar verirsiniz.</span><span class="sxs-lookup"><span data-stu-id="38bd2-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="38bd2-106">Aşağıdaki tabloda belirli çalışanlar için geçerli hale getirilebilecek kazançlara örnekler verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="38bd2-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="38bd2-107">Kazanç</span><span class="sxs-lookup"><span data-stu-id="38bd2-107">Benefit</span></span>          | <span data-ttu-id="38bd2-108">Kazanç kimin için geçerli olur</span><span class="sxs-lookup"><span data-stu-id="38bd2-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="38bd2-109">Sağlık sigortası</span><span class="sxs-lookup"><span data-stu-id="38bd2-109">Health insurance</span></span> | <span data-ttu-id="38bd2-110">Tüm çalışanlar</span><span class="sxs-lookup"><span data-stu-id="38bd2-110">All employees</span></span>                   |
| <span data-ttu-id="38bd2-111">Cep telefonu</span><span class="sxs-lookup"><span data-stu-id="38bd2-111">Mobile phone</span></span>     | <span data-ttu-id="38bd2-112">Satış personeli, idareciler</span><span class="sxs-lookup"><span data-stu-id="38bd2-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="38bd2-113">Park geçişleri</span><span class="sxs-lookup"><span data-stu-id="38bd2-113">Parking passes</span></span>   | <span data-ttu-id="38bd2-114">İdareciler</span><span class="sxs-lookup"><span data-stu-id="38bd2-114">Executives</span></span>                      |

<span data-ttu-id="38bd2-115">Aşağıdaki bileşenler, uygunluk politikalarının oluşturulması için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="38bd2-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="38bd2-116">Politika kuralı türleri</span><span class="sxs-lookup"><span data-stu-id="38bd2-116">Policy rule types</span></span>
-   <span data-ttu-id="38bd2-117">Kazanca uygunluk ilkeleri</span><span class="sxs-lookup"><span data-stu-id="38bd2-117">Benefit eligibility policies</span></span>

<span data-ttu-id="38bd2-118">Politika kuralı türleri, belirli politika kuralları geliştirdiğinizde kullanılan sorgu parametrelerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="38bd2-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="38bd2-119">Politika kuralı türleri oluşturduktan sonra kazanç uygunluk politikaları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="38bd2-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="38bd2-120">Politikalar bir veya birden fazla tüzel kişilik için geçerli bir kurallar topluluğu oluşturmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="38bd2-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="38bd2-121">Her bir politika kapsamında, daha önceden oluşturduğunuz kazanç uygunluk politikası kural türlerinden herhangi birini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="38bd2-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="38bd2-122">Kuralın kapsamını politikada tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="38bd2-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="38bd2-123">Örneğin, **Yönetici** adında bir kazanç uygunluk politikası kural türü tanımlandığınızda hangi kuralın hangi politika kapsamında olduğunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="38bd2-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="38bd2-124">Bu örnekte, "yönetici" sözcüğü içeren tüm iş unvanlarının kurala dahil edilmesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="38bd2-124">In this example, the rule might state that any job title that contains the word “executive” should be included in the rule.</span></span> <span data-ttu-id="38bd2-125">Politikaya dahil edilen kuralın veya kuralların parametrelerini tanımladıktan sonra kazanca belirli bir kural atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="38bd2-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>

<a name="see-also"></a><span data-ttu-id="38bd2-126">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="38bd2-126">See also</span></span>
--------

[<span data-ttu-id="38bd2-127">Bir kazanç programı tanımlama ve yönetme</span><span class="sxs-lookup"><span data-stu-id="38bd2-127">Defining and managing a benefit program</span></span>](manage-benefit-program.md)




