---
title: Kazanca uygunluk ilkeleri
description: Bu makalede, kazanç uygunluk ilkeleri hakkında, belirli kazançlara uygun olan kişileri tanımlamanıza yardımcı olacak bilgiler verilmektedir.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 7b35d3f9a8afd3be44b648f6e138afd5f143ba55
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010937"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="84c91-103">Kazanca uygunluk ilkeleri</span><span class="sxs-lookup"><span data-stu-id="84c91-103">Benefit eligibility policies</span></span>

<span data-ttu-id="84c91-104">Bu makalede, kazanç uygunluk ilkeleri hakkında, belirli kazançlara uygun olan kişileri tanımlamanıza yardımcı olacak bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="84c91-104">This article provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="84c91-105">Kazançlar oluşturduğunuzda hangi kazançların hangi çalışanlar için geçerli olacağına karar verirsiniz.</span><span class="sxs-lookup"><span data-stu-id="84c91-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="84c91-106">Aşağıdaki tabloda belirli çalışanlar için geçerli hale getirilebilecek kazançlara örnekler verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="84c91-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="84c91-107">Kazanç</span><span class="sxs-lookup"><span data-stu-id="84c91-107">Benefit</span></span>          | <span data-ttu-id="84c91-108">Kazanç kimin için geçerli olur</span><span class="sxs-lookup"><span data-stu-id="84c91-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="84c91-109">Sağlık sigortası</span><span class="sxs-lookup"><span data-stu-id="84c91-109">Health insurance</span></span> | <span data-ttu-id="84c91-110">Tüm çalışanlar</span><span class="sxs-lookup"><span data-stu-id="84c91-110">All employees</span></span>                   |
| <span data-ttu-id="84c91-111">Cep telefonu</span><span class="sxs-lookup"><span data-stu-id="84c91-111">Mobile phone</span></span>     | <span data-ttu-id="84c91-112">Satış personeli, idareciler</span><span class="sxs-lookup"><span data-stu-id="84c91-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="84c91-113">Park geçişleri</span><span class="sxs-lookup"><span data-stu-id="84c91-113">Parking passes</span></span>   | <span data-ttu-id="84c91-114">İdareciler</span><span class="sxs-lookup"><span data-stu-id="84c91-114">Executives</span></span>                      |

<span data-ttu-id="84c91-115">Aşağıdaki bileşenler, uygunluk politikalarının oluşturulması için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="84c91-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="84c91-116">Politika kuralı türleri</span><span class="sxs-lookup"><span data-stu-id="84c91-116">Policy rule types</span></span>
-   <span data-ttu-id="84c91-117">Kazanca uygunluk ilkeleri</span><span class="sxs-lookup"><span data-stu-id="84c91-117">Benefit eligibility policies</span></span>

<span data-ttu-id="84c91-118">Politika kuralı türleri, belirli politika kuralları geliştirdiğinizde kullanılan sorgu parametrelerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="84c91-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="84c91-119">Politika kuralı türleri oluşturduktan sonra kazanç uygunluk politikaları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="84c91-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="84c91-120">Politikalar bir veya birden fazla tüzel kişilik için geçerli bir kurallar topluluğu oluşturmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="84c91-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="84c91-121">Her bir politika kapsamında, daha önceden oluşturduğunuz kazanç uygunluk politikası kural türlerinden herhangi birini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="84c91-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="84c91-122">Kuralın kapsamını politikada tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="84c91-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="84c91-123">Örneğin, **Yönetici** adında bir kazanç uygunluk politikası kural türü tanımlandığınızda hangi kuralın hangi politika kapsamında olduğunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="84c91-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="84c91-124">Bu örnekte, "yönetici" sözcüğü içeren tüm iş unvanlarının kurala dahil edilmesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="84c91-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="84c91-125">Politikaya dahil edilen kuralın veya kuralların parametrelerini tanımladıktan sonra kazanca belirli bir kural atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="84c91-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>




