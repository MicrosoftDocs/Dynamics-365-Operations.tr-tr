---
title: Kazanca uygunluk kurallarını ve ilkelerini tanımlama
description: Bu makale, size yeni kazanç uygunluk kuralları ve ilkeleri oluşturmayı ve daha sonra kuralları kazançlara atamayı gösterir.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 39a9a1c96ae2a12a32b3c5fbc67571bcf983c898
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467999"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="c551f-103">Kazanca uygunluk kurallarını ve ilkelerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="c551f-103">Define benefit eligibility rules and policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c551f-104">Bu konu, size yeni kazanç uygunluk kuralları ve ilkeleri oluşturmayı ve daha sonra kuralları kazançlara atamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="c551f-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="c551f-105">Kazanç uygunluk ilkesi kural türü yaratın</span><span class="sxs-lookup"><span data-stu-id="c551f-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="c551f-106">**İnsan kaynakları > Kazançlar > Uygunluk > Kazanç uygunluğu ilkesi kural türleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c551f-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="c551f-107">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c551f-107">Select **New**.</span></span>
3. <span data-ttu-id="c551f-108">**Kural adı** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c551f-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="c551f-109">**Açıklama** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c551f-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="c551f-110">**Sorgu adı** alanında, açılır menü düğmesini seçerek aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="c551f-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c551f-111">Listeden, seçilen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="c551f-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="c551f-112">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c551f-112">Select **Save**.</span></span>
8. <span data-ttu-id="c551f-113">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c551f-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="c551f-114">Kazanç uygunluğu ilkesi</span><span class="sxs-lookup"><span data-stu-id="c551f-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="c551f-115">**İnsan kaynakları > Kazançlar > Uygunluk > Kazanç uygunluk ilkeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c551f-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="c551f-116">Varolan bir kazanç ilkesi seçin.</span><span class="sxs-lookup"><span data-stu-id="c551f-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="c551f-117">Listeden, seçilen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="c551f-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="c551f-118">**İlke kuruluşları** bölümlerinin genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="c551f-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="c551f-119">İlkeye dahil etmek istediğiniz kuruluşları ekleyebilir veya kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c551f-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="c551f-120">**İlke kuralları** bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="c551f-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="c551f-121">Listede, daha önce oluşturduğunuz ilke kuralını bulun.</span><span class="sxs-lookup"><span data-stu-id="c551f-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="c551f-122">**İlke kuralı oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="c551f-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="c551f-123">**Geçerlilik tarihi** alanına, ilkenin yürürlüğe girmesini istediğiniz tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="c551f-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="c551f-124">Geçerlilik bitiş tarihleri ayarlamak, ilke kurallarında gelecekte değişiklikler yapmanıza olanak tanır, böylece bu değişikliklerin etkili olmasını istediğinizde ilkeye geri dönmenize gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="c551f-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="c551f-125">Gerekirse, **Koşul ekle** alanına where yan tümcesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c551f-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="c551f-126">Örneğin, kuralın yalnızca Satış Yöneticileri için geçerli olmasını istiyorsanız where yan tümcesini oluşturabilirsiniz: Where konum açıklaması Satış Yöneticisi'ne eşittir.</span><span class="sxs-lookup"><span data-stu-id="c551f-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="c551f-127">Kuralda birden çok where deyimlerini birlikte ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c551f-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="c551f-128">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c551f-128">Select **OK**.</span></span>
11. <span data-ttu-id="c551f-129">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c551f-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="c551f-130">Kuralı, kazanca atayın</span><span class="sxs-lookup"><span data-stu-id="c551f-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="c551f-131">**İnsan kaynakları > Kazançlar > Kazançlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="c551f-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="c551f-132">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c551f-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c551f-133">Listeden, seçilen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="c551f-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="c551f-134">**Uygunluk kuralları** bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="c551f-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="c551f-135">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c551f-135">Select **Edit**.</span></span>
6. <span data-ttu-id="c551f-136">**Uygunluk** alanında, kuralı seçin.</span><span class="sxs-lookup"><span data-stu-id="c551f-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="c551f-137">**Kural türü** alanında, daha önce oluşturduğunuz kuralı seçin.</span><span class="sxs-lookup"><span data-stu-id="c551f-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="c551f-138">Listeden, seçilen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="c551f-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="c551f-139">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c551f-139">Select **Save**.</span></span>
11. <span data-ttu-id="c551f-140">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="c551f-140">Close the form.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]