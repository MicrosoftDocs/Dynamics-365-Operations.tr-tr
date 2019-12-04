---
title: Kazanca uygunluk ilkeleri
description: Bu makalede, kazanç uygunluk ilkeleri hakkında, belirli kazançlara uygun olan kişileri tanımlamanıza yardımcı olacak bilgiler verilmektedir.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: b44287bf22f0b6c4e33a29b4b86aaae934505a43
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814709"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="a4123-103">Kazanca uygunluk ilkeleri</span><span class="sxs-lookup"><span data-stu-id="a4123-103">Benefit eligibility policies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a4123-104">Bu konu, kazanç uygunluk ilkeleri hakkında, belirli kazançlara uygun olan kişileri tanımlamanıza yardımcı olacak bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a4123-104">This topic provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="a4123-105">Kazançlar oluşturduğunuzda hangi kazançların hangi çalışanlar için geçerli olacağına karar verirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4123-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="a4123-106">Aşağıdaki tabloda belirli çalışanlar için geçerli hale getirilebilecek kazançlara örnekler verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a4123-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="a4123-107">Kazanç</span><span class="sxs-lookup"><span data-stu-id="a4123-107">Benefit</span></span>          | <span data-ttu-id="a4123-108">Kazanç kimin için geçerli olur</span><span class="sxs-lookup"><span data-stu-id="a4123-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="a4123-109">Sağlık sigortası</span><span class="sxs-lookup"><span data-stu-id="a4123-109">Health insurance</span></span> | <span data-ttu-id="a4123-110">Tüm çalışanlar</span><span class="sxs-lookup"><span data-stu-id="a4123-110">All employees</span></span>                   |
| <span data-ttu-id="a4123-111">Cep telefonu</span><span class="sxs-lookup"><span data-stu-id="a4123-111">Mobile phone</span></span>     | <span data-ttu-id="a4123-112">Satış personeli, idareciler</span><span class="sxs-lookup"><span data-stu-id="a4123-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="a4123-113">Park geçişleri</span><span class="sxs-lookup"><span data-stu-id="a4123-113">Parking passes</span></span>   | <span data-ttu-id="a4123-114">İdareciler</span><span class="sxs-lookup"><span data-stu-id="a4123-114">Executives</span></span>                      |

<span data-ttu-id="a4123-115">Aşağıdaki bileşenler, uygunluk politikalarının oluşturulması için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="a4123-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="a4123-116">Politika kuralı türleri</span><span class="sxs-lookup"><span data-stu-id="a4123-116">Policy rule types</span></span>
-   <span data-ttu-id="a4123-117">Kazanca uygunluk ilkeleri</span><span class="sxs-lookup"><span data-stu-id="a4123-117">Benefit eligibility policies</span></span>

<span data-ttu-id="a4123-118">Politika kuralı türleri, belirli politika kuralları geliştirdiğinizde kullanılan sorgu parametrelerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a4123-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="a4123-119">Politika kuralı türleri oluşturduktan sonra kazanç uygunluk politikaları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4123-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="a4123-120">Politikalar bir veya birden fazla tüzel kişilik için geçerli bir kurallar topluluğu oluşturmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="a4123-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="a4123-121">Her bir politika kapsamında, daha önceden oluşturduğunuz kazanç uygunluk politikası kural türlerinden herhangi birini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4123-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="a4123-122">Kuralın kapsamını politikada tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="a4123-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="a4123-123">Örneğin, **Yönetici** adında bir kazanç uygunluk politikası kural türü tanımlandığınızda hangi kuralın hangi politika kapsamında olduğunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4123-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="a4123-124">Bu örnekte, "yönetici" sözcüğü içeren tüm iş unvanlarının kurala dahil edilmesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4123-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="a4123-125">Politikaya dahil edilen kuralın veya kuralların parametrelerini tanımladıktan sonra kazanca belirli bir kural atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4123-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>

<a name="additional-resources"></a><span data-ttu-id="a4123-126">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a4123-126">Additional resources</span></span>
--------

[<span data-ttu-id="a4123-127">Kazanç programı tanımlama ve yönetme</span><span class="sxs-lookup"><span data-stu-id="a4123-127">Define and manage a benefits program</span></span>](manage-benefit-program.md)



