---
title: Kazanca uygunluk ilkeleri
description: Bu makalede, kazanç uygunluk ilkeleri hakkında, belirli kazançlara uygun olan kişileri tanımlamanıza yardımcı olacak bilgiler verilmektedir.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 87a080c47e34a3265afea6494ff1733dac5bc384
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053117"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="b5092-103">Kazanca uygunluk ilkeleri</span><span class="sxs-lookup"><span data-stu-id="b5092-103">Benefit eligibility policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b5092-104">Bu makalede, kazanç uygunluk ilkeleri hakkında, belirli kazançlara uygun olan kişileri tanımlamanıza yardımcı olacak bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b5092-104">This article provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="b5092-105">Kazançlar oluşturduğunuzda hangi kazançların hangi çalışanlar için geçerli olacağına karar verirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5092-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="b5092-106">Aşağıdaki tabloda belirli çalışanlar için geçerli hale getirilebilecek kazançlara örnekler verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="b5092-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="b5092-107">Kazanç</span><span class="sxs-lookup"><span data-stu-id="b5092-107">Benefit</span></span>          | <span data-ttu-id="b5092-108">Kazanç kimin için geçerli olur</span><span class="sxs-lookup"><span data-stu-id="b5092-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="b5092-109">Sağlık sigortası</span><span class="sxs-lookup"><span data-stu-id="b5092-109">Health insurance</span></span> | <span data-ttu-id="b5092-110">Tüm çalışanlar</span><span class="sxs-lookup"><span data-stu-id="b5092-110">All employees</span></span>                   |
| <span data-ttu-id="b5092-111">Cep telefonu</span><span class="sxs-lookup"><span data-stu-id="b5092-111">Mobile phone</span></span>     | <span data-ttu-id="b5092-112">Satış personeli, idareciler</span><span class="sxs-lookup"><span data-stu-id="b5092-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="b5092-113">Park geçişleri</span><span class="sxs-lookup"><span data-stu-id="b5092-113">Parking passes</span></span>   | <span data-ttu-id="b5092-114">İdareciler</span><span class="sxs-lookup"><span data-stu-id="b5092-114">Executives</span></span>                      |

<span data-ttu-id="b5092-115">Aşağıdaki bileşenler, uygunluk politikalarının oluşturulması için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="b5092-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="b5092-116">Politika kuralı türleri</span><span class="sxs-lookup"><span data-stu-id="b5092-116">Policy rule types</span></span>
-   <span data-ttu-id="b5092-117">Kazanca uygunluk ilkeleri</span><span class="sxs-lookup"><span data-stu-id="b5092-117">Benefit eligibility policies</span></span>

<span data-ttu-id="b5092-118">Politika kuralı türleri, belirli politika kuralları geliştirdiğinizde kullanılan sorgu parametrelerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b5092-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="b5092-119">Politika kuralı türleri oluşturduktan sonra kazanç uygunluk politikaları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5092-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="b5092-120">Politikalar bir veya birden fazla tüzel kişilik için geçerli bir kurallar topluluğu oluşturmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="b5092-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="b5092-121">Her bir politika kapsamında, daha önceden oluşturduğunuz kazanç uygunluk politikası kural türlerinden herhangi birini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5092-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="b5092-122">Kuralın kapsamını politikada tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="b5092-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="b5092-123">Örneğin, **Yönetici** adında bir kazanç uygunluk politikası kural türü tanımlandığınızda hangi kuralın hangi politika kapsamında olduğunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5092-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="b5092-124">Bu örnekte, "yönetici" sözcüğü içeren tüm iş unvanlarının kurala dahil edilmesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5092-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="b5092-125">Politikaya dahil edilen kuralın veya kuralların parametrelerini tanımladıktan sonra kazanca belirli bir kural atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5092-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>






[!INCLUDE[footer-include](../includes/footer-banner.md)]