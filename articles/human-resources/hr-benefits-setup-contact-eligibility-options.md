---
title: Kişisel ilgili kişi uygunluk seçeneklerini yapılandır
description: Microsoft Dynamics 365 Human Resources'un kişisel kişileri için uygunluk seçeneklerini yapılandırın. Özel kişiler lehçileri veya bağımlı olabilir.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2f300ac917ac21db9fffbffcc6eb8589357c0a3e
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466218"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="d9ee8-104">Kişisel ilgili kişi uygunluk seçeneklerini yapılandır</span><span class="sxs-lookup"><span data-stu-id="d9ee8-104">Configure personal contact eligibility options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d9ee8-105">Bu makalede, Microsoft Dynamics 365 Human Resources'un Yararlarında kullanılacak kişisel ilgili kişi türlerinin nasıl yapılandırılacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="d9ee8-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d9ee8-106">Özel kişiler lehçileri veya bağımlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="d9ee8-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="d9ee8-107">**Sosyal haklar** yönetimi çalışma alanında, **Kurulum** altında, **Kişisel iletişim kişisi uygunluk seçenekleri** seçin.</span><span class="sxs-lookup"><span data-stu-id="d9ee8-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="d9ee8-108">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d9ee8-108">Select **New**.</span></span>

3. <span data-ttu-id="d9ee8-109">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="d9ee8-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="d9ee8-110">Alan</span><span class="sxs-lookup"><span data-stu-id="d9ee8-110">Field</span></span> | <span data-ttu-id="d9ee8-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9ee8-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d9ee8-112">**Uygunluk seçeneği**</span><span class="sxs-lookup"><span data-stu-id="d9ee8-112">**Eligibility option**</span></span> | <span data-ttu-id="d9ee8-113">Uygunluk seçeneğini tanımlamak için benzersiz uygunluk seçeneği adı veya kodu.</span><span class="sxs-lookup"><span data-stu-id="d9ee8-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="d9ee8-114">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="d9ee8-114">**Description**</span></span> | <span data-ttu-id="d9ee8-115">Uygunluk seçeneğinin kısa bir açıklaması</span><span class="sxs-lookup"><span data-stu-id="d9ee8-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="d9ee8-116">**İlgili kişi uygunluk kodu**</span><span class="sxs-lookup"><span data-stu-id="d9ee8-116">**Contact eligibility code**</span></span> | <span data-ttu-id="d9ee8-117">Kişisel uygunluk seçeneğini en iyi açıklayan sistem kodu.</span><span class="sxs-lookup"><span data-stu-id="d9ee8-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="d9ee8-118">Aşağıdaki seçeneklerden birini belirleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d9ee8-118">You can choose from:</span></span> <ul><li><span data-ttu-id="d9ee8-119">İlişki</span><span class="sxs-lookup"><span data-stu-id="d9ee8-119">Relationship</span></span></li><li><span data-ttu-id="d9ee8-120">Öğrenci</span><span class="sxs-lookup"><span data-stu-id="d9ee8-120">Student</span></span></li><li><span data-ttu-id="d9ee8-121">Bakmakla yükümlü olunan kişinin yaşı çok büyük</span><span class="sxs-lookup"><span data-stu-id="d9ee8-121">Overage dependent</span></span></li><li><span data-ttu-id="d9ee8-122">Çok yaşlı engelli bakmakla yükümlü olunan kişi</span><span class="sxs-lookup"><span data-stu-id="d9ee8-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="d9ee8-123">**Durum**</span><span class="sxs-lookup"><span data-stu-id="d9ee8-123">**Status**</span></span> | <span data-ttu-id="d9ee8-124">Uygunluk seçeneği durumu.</span><span class="sxs-lookup"><span data-stu-id="d9ee8-124">The status of the eligibility option.</span></span> <span data-ttu-id="d9ee8-125">Uygunluk seçeneğinin durumu etkin değil olarak ayarlanmışsa, kişisel kişiler için o kişisel ilgili kişi uygunluk seçeneğini seçemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="d9ee8-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="d9ee8-126">**İlişki**</span><span class="sxs-lookup"><span data-stu-id="d9ee8-126">**Relationship**</span></span> | <span data-ttu-id="d9ee8-127">Kişisel ilgili kişi ve çalışan arasındaki ilişkiyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9ee8-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="d9ee8-128">Bu alan yalnızca, ilgili kişi uygunluğu kodu ilişki olarak ayarlandığında etkindir.</span><span class="sxs-lookup"><span data-stu-id="d9ee8-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="d9ee8-129">**Yaş**</span><span class="sxs-lookup"><span data-stu-id="d9ee8-129">**Age**</span></span> | <span data-ttu-id="d9ee8-130">Kazanç planı için uygun bir kişisel ilgili kişinin yaş üst sınırı.</span><span class="sxs-lookup"><span data-stu-id="d9ee8-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="d9ee8-131">Bu alan yalnızca bir ilişki seçerseniz etkindir.</span><span class="sxs-lookup"><span data-stu-id="d9ee8-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="d9ee8-132">Bu yaş, kişisel ilgili kişinin hesaplanan geçerlilik süresi ile karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="d9ee8-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="d9ee8-133">Hesaplanan Yaş: (tedarik tarihi – kişisel ilgili kişi Doğum tarihi/365).</span><span class="sxs-lookup"><span data-stu-id="d9ee8-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="d9ee8-134">Bu sayı her zaman bir tamsayıdır.</span><span class="sxs-lookup"><span data-stu-id="d9ee8-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="d9ee8-135">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d9ee8-135">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]