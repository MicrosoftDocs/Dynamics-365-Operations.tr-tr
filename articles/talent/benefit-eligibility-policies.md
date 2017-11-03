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
ms.search.scope: Core, Operations
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 682100881d6ea8c1e02db50629208c765600c49a
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="benefit-eligibility-policies"></a><span data-ttu-id="26b9c-103">Kazanca uygunluk ilkeleri</span><span class="sxs-lookup"><span data-stu-id="26b9c-103">Benefit eligibility policies</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="26b9c-104">Bu konu, kazanç uygunluk ilkeleri hakkında, belirli kazançlara uygun olan kişileri tanımlamanıza yardımcı olacak bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="26b9c-104">This topic provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="26b9c-105">Kazançlar oluşturduğunuzda hangi kazançların hangi çalışanlar için geçerli olacağına karar verirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26b9c-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="26b9c-106">Aşağıdaki tabloda belirli çalışanlar için geçerli hale getirilebilecek kazançlara örnekler verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="26b9c-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="26b9c-107">Kazanç</span><span class="sxs-lookup"><span data-stu-id="26b9c-107">Benefit</span></span>          | <span data-ttu-id="26b9c-108">Kazanç kimin için geçerli olur</span><span class="sxs-lookup"><span data-stu-id="26b9c-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="26b9c-109">Sağlık sigortası</span><span class="sxs-lookup"><span data-stu-id="26b9c-109">Health insurance</span></span> | <span data-ttu-id="26b9c-110">Tüm çalışanlar</span><span class="sxs-lookup"><span data-stu-id="26b9c-110">All employees</span></span>                   |
| <span data-ttu-id="26b9c-111">Cep telefonu</span><span class="sxs-lookup"><span data-stu-id="26b9c-111">Mobile phone</span></span>     | <span data-ttu-id="26b9c-112">Satış personeli, idareciler</span><span class="sxs-lookup"><span data-stu-id="26b9c-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="26b9c-113">Park geçişleri</span><span class="sxs-lookup"><span data-stu-id="26b9c-113">Parking passes</span></span>   | <span data-ttu-id="26b9c-114">İdareciler</span><span class="sxs-lookup"><span data-stu-id="26b9c-114">Executives</span></span>                      |

<span data-ttu-id="26b9c-115">Aşağıdaki bileşenler, uygunluk politikalarının oluşturulması için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="26b9c-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="26b9c-116">Politika kuralı türleri</span><span class="sxs-lookup"><span data-stu-id="26b9c-116">Policy rule types</span></span>
-   <span data-ttu-id="26b9c-117">Kazanca uygunluk ilkeleri</span><span class="sxs-lookup"><span data-stu-id="26b9c-117">Benefit eligibility policies</span></span>

<span data-ttu-id="26b9c-118">Politika kuralı türleri, belirli politika kuralları geliştirdiğinizde kullanılan sorgu parametrelerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="26b9c-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="26b9c-119">Politika kuralı türleri oluşturduktan sonra kazanç uygunluk politikaları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26b9c-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="26b9c-120">Politikalar bir veya birden fazla tüzel kişilik için geçerli bir kurallar topluluğu oluşturmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="26b9c-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="26b9c-121">Her bir politika kapsamında, daha önceden oluşturduğunuz kazanç uygunluk politikası kural türlerinden herhangi birini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26b9c-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="26b9c-122">Kuralın kapsamını politikada tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="26b9c-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="26b9c-123">Örneğin, **Yönetici** adında bir kazanç uygunluk politikası kural türü tanımlandığınızda hangi kuralın hangi politika kapsamında olduğunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26b9c-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="26b9c-124">Bu örnekte, "yönetici" sözcüğü içeren tüm iş unvanlarının kurala dahil edilmesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26b9c-124">In this example, the rule might state that any job title that contains the word “executive” should be included in the rule.</span></span> <span data-ttu-id="26b9c-125">Politikaya dahil edilen kuralın veya kuralların parametrelerini tanımladıktan sonra kazanca belirli bir kural atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26b9c-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>

<a name="see-also"></a><span data-ttu-id="26b9c-126">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="26b9c-126">See also</span></span>
--------

[<span data-ttu-id="26b9c-127">Bir kazanç programı tanımlama ve yönetme</span><span class="sxs-lookup"><span data-stu-id="26b9c-127">Defining and managing a benefit program</span></span>](manage-benefit-program.md)




