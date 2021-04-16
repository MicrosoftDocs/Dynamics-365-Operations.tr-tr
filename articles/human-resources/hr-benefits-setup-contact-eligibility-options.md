---
title: Kişisel ilgili kişi uygunluk seçeneklerini yapılandır
description: Microsoft Dynamics 365 Human Resources'un kişisel kişileri için uygunluk seçeneklerini yapılandırın. Özel kişiler lehçileri veya bağımlı olabilir.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 49a519aafc56c303765619a66d815d79b668d0f9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790896"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="c3778-104">Kişisel ilgili kişi uygunluk seçeneklerini yapılandır</span><span class="sxs-lookup"><span data-stu-id="c3778-104">Configure personal contact eligibility options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c3778-105">Bu makalede, Microsoft Dynamics 365 Human Resources'un Yararlarında kullanılacak kişisel ilgili kişi türlerinin nasıl yapılandırılacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="c3778-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c3778-106">Özel kişiler lehçileri veya bağımlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="c3778-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="c3778-107">**Sosyal haklar** yönetimi çalışma alanında, **Kurulum** altında, **Kişisel iletişim kişisi uygunluk seçenekleri** seçin.</span><span class="sxs-lookup"><span data-stu-id="c3778-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="c3778-108">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3778-108">Select **New**.</span></span>

3. <span data-ttu-id="c3778-109">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="c3778-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="c3778-110">Alan</span><span class="sxs-lookup"><span data-stu-id="c3778-110">Field</span></span> | <span data-ttu-id="c3778-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3778-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c3778-112">**Uygunluk seçeneği**</span><span class="sxs-lookup"><span data-stu-id="c3778-112">**Eligibility option**</span></span> | <span data-ttu-id="c3778-113">Uygunluk seçeneğini tanımlamak için benzersiz uygunluk seçeneği adı veya kodu.</span><span class="sxs-lookup"><span data-stu-id="c3778-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="c3778-114">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="c3778-114">**Description**</span></span> | <span data-ttu-id="c3778-115">Uygunluk seçeneğinin kısa bir açıklaması</span><span class="sxs-lookup"><span data-stu-id="c3778-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="c3778-116">**İlgili kişi uygunluk kodu**</span><span class="sxs-lookup"><span data-stu-id="c3778-116">**Contact eligibility code**</span></span> | <span data-ttu-id="c3778-117">Kişisel uygunluk seçeneğini en iyi açıklayan sistem kodu.</span><span class="sxs-lookup"><span data-stu-id="c3778-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="c3778-118">Aşağıdaki seçeneklerden birini belirleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="c3778-118">You can choose from:</span></span> <ul><li><span data-ttu-id="c3778-119">İlişki</span><span class="sxs-lookup"><span data-stu-id="c3778-119">Relationship</span></span></li><li><span data-ttu-id="c3778-120">Öğrenci</span><span class="sxs-lookup"><span data-stu-id="c3778-120">Student</span></span></li><li><span data-ttu-id="c3778-121">Bakmakla yükümlü olunan kişinin yaşı çok büyük</span><span class="sxs-lookup"><span data-stu-id="c3778-121">Overage dependent</span></span></li><li><span data-ttu-id="c3778-122">Çok yaşlı engelli bakmakla yükümlü olunan kişi</span><span class="sxs-lookup"><span data-stu-id="c3778-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="c3778-123">**Durum**</span><span class="sxs-lookup"><span data-stu-id="c3778-123">**Status**</span></span> | <span data-ttu-id="c3778-124">Uygunluk seçeneği durumu.</span><span class="sxs-lookup"><span data-stu-id="c3778-124">The status of the eligibility option.</span></span> <span data-ttu-id="c3778-125">Uygunluk seçeneğinin durumu etkin değil olarak ayarlanmışsa, kişisel kişiler için o kişisel ilgili kişi uygunluk seçeneğini seçemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3778-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="c3778-126">**İlişki**</span><span class="sxs-lookup"><span data-stu-id="c3778-126">**Relationship**</span></span> | <span data-ttu-id="c3778-127">Kişisel ilgili kişi ve çalışan arasındaki ilişkiyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3778-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="c3778-128">Bu alan yalnızca, ilgili kişi uygunluğu kodu ilişki olarak ayarlandığında etkindir.</span><span class="sxs-lookup"><span data-stu-id="c3778-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="c3778-129">**Yaş**</span><span class="sxs-lookup"><span data-stu-id="c3778-129">**Age**</span></span> | <span data-ttu-id="c3778-130">Kazanç planı için uygun bir kişisel ilgili kişinin yaş üst sınırı.</span><span class="sxs-lookup"><span data-stu-id="c3778-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="c3778-131">Bu alan yalnızca bir ilişki seçerseniz etkindir.</span><span class="sxs-lookup"><span data-stu-id="c3778-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="c3778-132">Bu yaş, kişisel ilgili kişinin hesaplanan geçerlilik süresi ile karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="c3778-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="c3778-133">Hesaplanan Yaş: (tedarik tarihi – kişisel ilgili kişi Doğum tarihi/365).</span><span class="sxs-lookup"><span data-stu-id="c3778-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="c3778-134">Bu sayı her zaman bir tamsayıdır.</span><span class="sxs-lookup"><span data-stu-id="c3778-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="c3778-135">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c3778-135">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]