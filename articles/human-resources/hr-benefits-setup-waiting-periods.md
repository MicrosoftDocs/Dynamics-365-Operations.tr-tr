---
title: Bekleme dönemlerini yapılandırma
description: Microsoft Dynamics 365 Human Resources'ta, bekleme günleri, kazanç planları için kullanılacak kilometre taşı oluşturur.
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
ms.openlocfilehash: 0e08c0c02393506e1e292676c954bdf3850029f7
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468311"
---
# <a name="configure-waiting-periods"></a><span data-ttu-id="a9631-103">Bekleme dönemlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a9631-103">Configure waiting periods</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a9631-104">Microsoft Dynamics 365 Human Resources'ta, bekleme günleri, kazanç planları için kullanılacak kilometre taşı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9631-104">In Microsoft Dynamics 365 Human Resources, waiting days establish a milestone to use for benefit plans.</span></span> <span data-ttu-id="a9631-105">Örneğin, işe alınma tarihinden itibaren üç ay, her ayın birincesinin veya altı ayın.</span><span class="sxs-lookup"><span data-stu-id="a9631-105">For example, three months from hire date, the first of each month, or six months.</span></span>   

1. <span data-ttu-id="a9631-106">**Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Bekleme dönemleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="a9631-106">In the **Benefits management** workspace, under **Setup**, select **Waiting periods**.</span></span>

2. <span data-ttu-id="a9631-107">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a9631-107">Select **New**.</span></span>

3. <span data-ttu-id="a9631-108">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="a9631-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="a9631-109">Alan</span><span class="sxs-lookup"><span data-stu-id="a9631-109">Field</span></span> | <span data-ttu-id="a9631-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9631-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a9631-111">**Bekleme kodu**</span><span class="sxs-lookup"><span data-stu-id="a9631-111">**Waiting code**</span></span> | <span data-ttu-id="a9631-112">Bekleme dönemi için benzersiz bir tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="a9631-112">A unique identifier for the waiting period.</span></span> |
   | <span data-ttu-id="a9631-113">**Tanım**</span><span class="sxs-lookup"><span data-stu-id="a9631-113">**Description**</span></span> | <span data-ttu-id="a9631-114">Bekleme dönemin bir açıklaması.</span><span class="sxs-lookup"><span data-stu-id="a9631-114">A description of the waiting period.</span></span> |
   | <span data-ttu-id="a9631-115">**Bekleme yöntemi**</span><span class="sxs-lookup"><span data-stu-id="a9631-115">**Waiting method**</span></span> | <span data-ttu-id="a9631-116">Aşağı açılan değerler listesinden uygun bekleme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="a9631-116">Select the appropriate waiting method from the drop-down list of values.</span></span> <span data-ttu-id="a9631-117">Seçenekler net, geçerli ay, geçerli üç aylık dönem, geçerli yıl ve geçerli haftadır.</span><span class="sxs-lookup"><span data-stu-id="a9631-117">Options are Net, Current month, Current quarter, Current year, and Current week.</span></span> |
   | <span data-ttu-id="a9631-118">**Aylar**</span><span class="sxs-lookup"><span data-stu-id="a9631-118">**Months**</span></span> | <span data-ttu-id="a9631-119">Bekleme tarihinin hesaplanması için bekleme yöntemine eklenecek ayların sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="a9631-119">Enter the number of months to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="a9631-120">**Vade erteleme gün sayısı**</span><span class="sxs-lookup"><span data-stu-id="a9631-120">**Days**</span></span> | <span data-ttu-id="a9631-121">Bekleme tarihinin hesaplanması için bekleme yöntemine eklenecek günlerin sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="a9631-121">Enter the number of days to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="a9631-122">**Bekleme günü**</span><span class="sxs-lookup"><span data-stu-id="a9631-122">**Waiting day**</span></span> | <span data-ttu-id="a9631-123">Bekleme tarihini hesaplamak için kullanılacak bir bekleme günü seçin.</span><span class="sxs-lookup"><span data-stu-id="a9631-123">Select the waiting day to use to calculate the waiting date.</span></span> |

4. <span data-ttu-id="a9631-124">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a9631-124">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]