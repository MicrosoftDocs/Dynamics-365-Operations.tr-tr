---
title: Kazanca uygunluk kurallarını ve ilkelerini tanımlama
description: Bu makale, size yeni kazanç uygunluk kuralları ve ilkeleri oluşturmayı ve daha sonra kuralları kazançlara atamayı gösterir.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: fa507591fc89eaebf617deedb15b15a0f93f971d
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010931"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="5df23-103">Kazanca uygunluk kurallarını ve ilkelerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="5df23-103">Define benefit eligibility rules and policies</span></span>

<span data-ttu-id="5df23-104">Bu makale, size yeni kazanç uygunluk kuralları ve ilkeleri oluşturmayı ve daha sonra kuralları kazançlara atamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="5df23-104">This article shows you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="5df23-105">Bu kaydı oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="5df23-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="5df23-106">Kazanç uygunluk ilkesi kural türü yaratın</span><span class="sxs-lookup"><span data-stu-id="5df23-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="5df23-107">İnsan Kaynakları > Kazançlar > Uygunluk > Kazanç uygunluk ilkesi ve kural türleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5df23-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="5df23-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5df23-108">Click New.</span></span>
3. <span data-ttu-id="5df23-109">Kural adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="5df23-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="5df23-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="5df23-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5df23-111">Sorgu adı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="5df23-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5df23-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5df23-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="5df23-113">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5df23-113">Click Save.</span></span>
8. <span data-ttu-id="5df23-114">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5df23-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="5df23-115">Kazanç uygunluğu ilkesi</span><span class="sxs-lookup"><span data-stu-id="5df23-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="5df23-116">İnsan Kaynakları > Kazançlar > Uygunluk > Kazanç uygunluk ilkeleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5df23-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="5df23-117">Varolan bir kazanç ilkesi seçin.</span><span class="sxs-lookup"><span data-stu-id="5df23-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="5df23-118">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5df23-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="5df23-119">İlke kuruluşu bölümlerinin genişletimesini değiştirin.</span><span class="sxs-lookup"><span data-stu-id="5df23-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="5df23-120">Burada ilkesine dahil etmek istediğiniz kuruluşları ekleyebilir ve kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5df23-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="5df23-121">İlke kuralları bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="5df23-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="5df23-122">Daha önce oluşturduğunuz ilke kuralını listede bulun.</span><span class="sxs-lookup"><span data-stu-id="5df23-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="5df23-123">İlke kuralı oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5df23-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="5df23-124">Etkin tarih alanında, ilkenin etkin hale gelmesini istediğiniz tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="5df23-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="5df23-125">Etkili ve bitiş tarihlerini girmek, ilke kurallarında gelecekte değişiklik yapmanıza ve bu değişikliklerin etkin olmasını istediğiniz zamanda bu ilkeye geri dönmenize olan gereksinimi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5df23-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="5df23-126">Kuralın sadece Satış Yöneticilerine uygulanmasını istiyorsanız, Nerede yan tümcesini şunun olacağı şekilde oluşturursunuz: Pozisyon tanımının Satış Yöneticisine eşit olduğunda.</span><span class="sxs-lookup"><span data-stu-id="5df23-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="5df23-127">Birden çok Nerede ifadesini Ve/veya ifadeleri ile birlikte kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5df23-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="5df23-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5df23-128">Click OK.</span></span>
11. <span data-ttu-id="5df23-129">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5df23-129">Close the page.</span></span>
12. <span data-ttu-id="5df23-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5df23-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="5df23-131">Kuralı, kazanca atayın</span><span class="sxs-lookup"><span data-stu-id="5df23-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="5df23-132">İnsan kaynakları > Kazançlar > Kazançlar seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="5df23-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="5df23-133">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5df23-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="5df23-134">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5df23-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="5df23-135">Uygunluk kuralları bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="5df23-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="5df23-136">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5df23-136">Click Edit.</span></span>
6. <span data-ttu-id="5df23-137">Uygunluk alanında listeden Kurala göre'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5df23-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="5df23-138">Kural türü alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5df23-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="5df23-139">Listede, önceden oluşturduğunuz kuralı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5df23-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="5df23-140">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5df23-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="5df23-141">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5df23-141">Click Save.</span></span>
11. <span data-ttu-id="5df23-142">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="5df23-142">Close the form.</span></span>

