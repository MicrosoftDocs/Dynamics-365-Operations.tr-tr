---
title: Çalışan kazanç planları oluşturma
description: Çalışanlar için kazanç planları seçmek ve kazanç planı seçimlerini onaylamak Için, Microsoft Dynamics 365 Human Resources'ta çalışan avantajı planları oluşturabilirsiniz.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitPlanEmployee
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 65b0ce2200a3c63a00ccd73fb26c79556aec55ad
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010876"
---
# <a name="create-worker-benefit-plans"></a><span data-ttu-id="e3abd-103">Çalışan kazanç planları oluşturma</span><span class="sxs-lookup"><span data-stu-id="e3abd-103">Create worker benefit plans</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="e3abd-104">Çalışanlar için kazanç planları seçmek ve kazanç planı seçimlerini onaylamak Için, Microsoft Dynamics 365 Human Resources'ta çalışan avantajı planları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e3abd-104">You can create worker benefit plans in Microsoft Dynamics 365 Human Resources to select benefit plans for employees and to confirm benefit plan selections.</span></span> <span data-ttu-id="e3abd-105">Normal olarak, Çalışanlar Çalışan Self Servis'i kullanarak tüm kazanç planlarını seçer ve daha sonra bir yarar Yöneticisi seçimleri onaylar.</span><span class="sxs-lookup"><span data-stu-id="e3abd-105">Typically, employees select benefit plans themselves by using Employee self service, and then a benefits administrator confirms the selections.</span></span> 

1. <span data-ttu-id="e3abd-106">**Sosyal haklar** yönetimi çalışma alanında, **Planlar** altında, **Çalışan kazanç planları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="e3abd-106">In the **Benefits management** workspace, under **Plans**, select **Worker benefit plans**.</span></span>

2. <span data-ttu-id="e3abd-107">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e3abd-107">Select **New**.</span></span>

3. <span data-ttu-id="e3abd-108">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="e3abd-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="e3abd-109">Alan</span><span class="sxs-lookup"><span data-stu-id="e3abd-109">Field</span></span> | <span data-ttu-id="e3abd-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3abd-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="e3abd-111">Dönem</span><span class="sxs-lookup"><span data-stu-id="e3abd-111">Period</span></span> | <span data-ttu-id="e3abd-112">Planlar hızlı sekmesindeki planları filtrelemek için kullanılacak bir yarar dönemi belirtir. Tüm plan kayıtlarının bir alt kümesini seçmenizi sağlamak için planları filtreleyin; böylece alt kümeyi onaylayabilmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e3abd-112">Specifies a benefits period to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> <span data-ttu-id="e3abd-113">Örneğin, 2015 ile ilgili tüm kazanç kayıt seçimlerini onaylamak için 2015 adlı oluşturduğunuz bir dönemi seçin.</span><span class="sxs-lookup"><span data-stu-id="e3abd-113">For example, select a period you created called 2015 to confirm all the benefit enrollment selections for 2015.</span></span> |
   | <span data-ttu-id="e3abd-114">Çalışan</span><span class="sxs-lookup"><span data-stu-id="e3abd-114">Worker</span></span> | <span data-ttu-id="e3abd-115">Planlar hızlı sekmesindeki planları filtrelemek için kullanılacak bir çalışan belirtir. Tüm plan kayıtlarının bir alt kümesini seçmenizi sağlamak için planları filtreleyin; böylece alt kümeyi onaylayabilmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e3abd-115">Specifies a worker to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="e3abd-116">Tüzel kişilik</span><span class="sxs-lookup"><span data-stu-id="e3abd-116">Legal entity</span></span> | <span data-ttu-id="e3abd-117">Planlar hızlı sekmesindeki planları filtrelemek için kullanılacak bir yasal varlık belirtir. Tüm plan kayıtlarının bir alt kümesini seçmenizi sağlamak için planları filtreleyin; böylece alt kümeyi onaylayabilmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e3abd-117">Specifies a legal entity to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="e3abd-118">Karşılama seçeneği</span><span class="sxs-lookup"><span data-stu-id="e3abd-118">Coverage option</span></span> | <span data-ttu-id="e3abd-119">Planlar hızlı sekmesindeki planları filtrelemek için kullanılacak bir kapsam seçeneği belirtir. Tüm plan kayıtlarının bir alt kümesini seçmenizi sağlamak için planları filtreleyin; böylece alt kümeyi onaylayabilmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e3abd-119">Specifies a coverage option to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="e3abd-120">Varsayılan</span><span class="sxs-lookup"><span data-stu-id="e3abd-120">Default</span></span> | <span data-ttu-id="e3abd-121">Varsayılan bir plan bulunup bulunmadığını temel alarak, kazanç planlarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="e3abd-121">Filters the benefit plans based on whether they are a default plan.</span></span> <span data-ttu-id="e3abd-122">Tüm plan kayıtlarının bir alt kümesini seçmenizi sağlamak için planları filtreleyin; böylece alt kümeyi onaylayabilmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e3abd-122">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="e3abd-123">Durum</span><span class="sxs-lookup"><span data-stu-id="e3abd-123">Status</span></span> | <span data-ttu-id="e3abd-124">Durumları temel alarak ayrıcalık planlarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="e3abd-124">Filters benefit plans based on their status.</span></span> <span data-ttu-id="e3abd-125">Tüm plan kayıtlarının bir alt kümesini seçmenizi sağlamak için planları filtreleyin; böylece alt kümeyi onaylayabilmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e3abd-125">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="e3abd-126">Onay</span><span class="sxs-lookup"><span data-stu-id="e3abd-126">Confirmation</span></span> | <span data-ttu-id="e3abd-127">Planlar hızlı sekmesindeki planları filtrelemek için kullanılacak bir onay durumu belirtir. Tüm plan kayıtlarının bir alt kümesini seçmenizi sağlamak için planları filtreleyin; böylece alt kümeyi onaylayabilmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e3abd-127">Specifies the confirmation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="e3abd-128">İptal</span><span class="sxs-lookup"><span data-stu-id="e3abd-128">Cancellation</span></span> | <span data-ttu-id="e3abd-129">Planlar hızlı sekmesindeki planları filtrelemek için kullanılacak bir iptal durumu belirtir. Tüm plan kayıtlarının bir alt kümesini seçmenizi sağlamak için planları filtreleyin; böylece alt kümeyi onaylayabilmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e3abd-129">Specifies the cancellation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="e3abd-130">Yürürlülük tarihi filtresi</span><span class="sxs-lookup"><span data-stu-id="e3abd-130">Effective date filter</span></span> | <span data-ttu-id="e3abd-131">Zaman aşımına uğramış, etkin veya gelecekte etkin olup olmadıklarını temel alarak planlara filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="e3abd-131">Filters the plans based on whether they’re expired, active, or will be active in the future.</span></span> <span data-ttu-id="e3abd-132">Planlar hızlı sekmesinde görmek istediğiniz planlara karşılık gelen onay kutularını seçin.</span><span class="sxs-lookup"><span data-stu-id="e3abd-132">Select the check boxes that correspond to the plans you want to see in the Plans fast tab.</span></span> |
   | <span data-ttu-id="e3abd-133">Planlar</span><span class="sxs-lookup"><span data-stu-id="e3abd-133">Plans</span></span> | <span data-ttu-id="e3abd-134">Planlar hızlı sekmesi, belirttiğiniz filtre ölçütüne uyan planları içerir.</span><span class="sxs-lookup"><span data-stu-id="e3abd-134">The Plans fast tab contains the plans that meet the filter criteria you specified.</span></span> <span data-ttu-id="e3abd-135">İK personeli tarafından ayarlanan ilgili konfigürasyon seçenekleri ve çalışanlar tarafından seçilen kayıt seçimleri her satıra dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="e3abd-135">The relevant configuration options that were set by HR staff and the enrollment selections that were chosen by employees are included on each line.</span></span> <span data-ttu-id="e3abd-136">Nitelenmiş alan, plan seçimiyle bir doğrulama çakışması olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3abd-136">The Qualified field specifies whether there is a validation conflict with the plan selection.</span></span> |

4. <span data-ttu-id="e3abd-137">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e3abd-137">Select **Save**.</span></span>
