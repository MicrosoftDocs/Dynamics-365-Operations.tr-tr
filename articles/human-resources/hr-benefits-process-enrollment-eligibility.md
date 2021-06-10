---
title: İşlem kayıt uygunluğu
description: Bu makalede, kayıt uygunluk işleminin nasıl çalıştırıldığı açıklanır.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4dd63e755f0afdbce411b3001410d2e56036e432
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054272"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="1cd0f-103">İşlem kayıt uygunluğu</span><span class="sxs-lookup"><span data-stu-id="1cd0f-103">Process enrollment eligibility</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1cd0f-104">Bu makalede, kayıt uygunluk işleminin nasıl çalıştırıldığı açıklanır.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="1cd0f-105">**Sosyal haklar** yönetimi çalışma alanında, **işlem** altında, kayıt **uygunluk işlemini** seçin.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="1cd0f-106">**Kazanç kaydı uygunluk işlemini çalıştır** iletişim kutusunda, aşağıdaki alanlar için değer belirtin:</span><span class="sxs-lookup"><span data-stu-id="1cd0f-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="1cd0f-107">Alan</span><span class="sxs-lookup"><span data-stu-id="1cd0f-107">Field</span></span> | <span data-ttu-id="1cd0f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1cd0f-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1cd0f-109">**Kayıt dönemi**</span><span class="sxs-lookup"><span data-stu-id="1cd0f-109">**Enrollment period**</span></span> | <span data-ttu-id="1cd0f-110">Kayıt uygunluğunu işleyecek kayıt dönemi.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="1cd0f-111">**Tüzel kişilik**</span><span class="sxs-lookup"><span data-stu-id="1cd0f-111">**Legal entity**</span></span> | <span data-ttu-id="1cd0f-112">Yasal varlık işleyecek kayıt dönemi.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="1cd0f-113">**Çalışan**</span><span class="sxs-lookup"><span data-stu-id="1cd0f-113">**Worker**</span></span> | <span data-ttu-id="1cd0f-114">Çalışan işleyecek kayıt dönemi.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="1cd0f-115">Bu alanı boş bırakırsanız, kayıt uygunluğu tüm çalışanlar için işlem görür.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="1cd0f-116">**Kazanç planı**</span><span class="sxs-lookup"><span data-stu-id="1cd0f-116">**Benefit plan**</span></span> | <span data-ttu-id="1cd0f-117">Kazanç planı işleyecek kayıt dönemi.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="1cd0f-118">İşlemi arka planda çalıştırmak istiyorsanız, **arka planda Çalıştır** 'ı seçin ve aşağıdaki görevleri gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="1cd0f-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="1cd0f-119">İşlem bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="1cd0f-120">Tekrarlayan iş ayarlamak için **tekrarlama**'yı seçin, yinelenme bilgilerini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="1cd0f-121">İş uyarısı ayarlamak için, **uyarılar**'ı seçin, alınacak uyarıları seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="1cd0f-122">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-122">Select **OK**.</span></span> <span data-ttu-id="1cd0f-123">İşlem, ayarladığınız parametrelerle çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="1cd0f-124">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-124">Select **OK**.</span></span>

## <a name="view-process-results"></a><span data-ttu-id="1cd0f-125">İşlem Sonuçlarını Görüntüleme</span><span class="sxs-lookup"><span data-stu-id="1cd0f-125">View Process Results</span></span>

<span data-ttu-id="1cd0f-126">Bu makalede, uygunluk işlemi sonuçlarının nasıl görüntüleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-126">This article explains how to view eligibility process results.</span></span>

1.  <span data-ttu-id="1cd0f-127">**Kazanç yönetimi** çalışma alanında, **İşleme** altında, **İşlem sonuçları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-127">In the **Benefits management** workspace, under **Processing**, select **Process results**.</span></span>

2.  <span data-ttu-id="1cd0f-128">**İşlem sonuçları** formunda, aşağıdaki alanlar belirtilir:</span><span class="sxs-lookup"><span data-stu-id="1cd0f-128">In the **Process results** form, the following fields are specified:</span></span>

   | <span data-ttu-id="1cd0f-129">Alan</span><span class="sxs-lookup"><span data-stu-id="1cd0f-129">Field</span></span> | <span data-ttu-id="1cd0f-130">Tanım</span><span class="sxs-lookup"><span data-stu-id="1cd0f-130">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1cd0f-131">**İşlem Kodu**</span><span class="sxs-lookup"><span data-stu-id="1cd0f-131">**Process ID**</span></span> | <span data-ttu-id="1cd0f-132">Çalışan, Tüzel kişilik ve işlem çalıştırma birleşiminin benzersiz kodu.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-132">The unique ID for the combination of Worker, Legal entity, and process run.</span></span> |
   | <span data-ttu-id="1cd0f-133">**İşlem türü**</span><span class="sxs-lookup"><span data-stu-id="1cd0f-133">**Process type**</span></span> | <span data-ttu-id="1cd0f-134">Çalıştırılmış olan işlemi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-134">This identifies the process that was run.</span></span> <span data-ttu-id="1cd0f-135">Örnek: Kayıt.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-135">For example:  Enrollment.</span></span> |
   | <span data-ttu-id="1cd0f-136">**Zaman damgası**</span><span class="sxs-lookup"><span data-stu-id="1cd0f-136">**Time stamp**</span></span> | <span data-ttu-id="1cd0f-137">Uygunluk işleminin çalıştırıldığı zaman.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-137">The time that the eligibility process was run.</span></span> |
   | <span data-ttu-id="1cd0f-138">**Tüzel kişilik**</span><span class="sxs-lookup"><span data-stu-id="1cd0f-138">**Legal entity**</span></span> | <span data-ttu-id="1cd0f-139">Kayıt işlemi sırasında belirtilen tüzel kişilik.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-139">The legal entity specified during the enrollment process.</span></span> |
   | <span data-ttu-id="1cd0f-140">**Çalışan**</span><span class="sxs-lookup"><span data-stu-id="1cd0f-140">**Worker**</span></span> | <span data-ttu-id="1cd0f-141">İşlenmiş olan çalışan.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-141">The worker who was processed.</span></span> |
   | <span data-ttu-id="1cd0f-142">\*\*Plan</span><span class="sxs-lookup"><span data-stu-id="1cd0f-142">\*\*Plan</span></span> | <span data-ttu-id="1cd0f-143">Kaydın denendiği Kazanç planı.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-143">The Benefit plan that enrollment was attempted for.</span></span> |
   | <span data-ttu-id="1cd0f-144">**Uygunluk kuralı**</span><span class="sxs-lookup"><span data-stu-id="1cd0f-144">**Eligibility rule**</span></span> | <span data-ttu-id="1cd0f-145">İşlenmiş olan uygunluk kuralı.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-145">The eligibility rule that was processed.</span></span> <span data-ttu-id="1cd0f-146">Uygunluk çalıştırılmadan önce hata oluştuysa, bu boş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-146">If an error was encountered before eligibility was run, this will be blank.</span></span> <span data-ttu-id="1cd0f-147">Örnek: Bir çalışan için ücret tanımlanmadıysa, uygunluk işlemi çalışmaz ve bu alan boş bırakılır.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-147">For example: If compensation hasn't been defined for a worker, the eligibility process won't run, and this field will be left blank.</span></span> |
   | <span data-ttu-id="1cd0f-148">**Sonuç durumu**</span><span class="sxs-lookup"><span data-stu-id="1cd0f-148">**Result status**</span></span> | <span data-ttu-id="1cd0f-149">Bu, Uygun veya Uygun Değil olacaktır.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-149">This will be Eligible or Ineligible.</span></span> <span data-ttu-id="1cd0f-150">Çalışan uygunluk kuralı kriterini karşılamıyorsa, çalışanın ödeme sıklığı veya sabit ücret gibi gerekli bilgileri eksikse veya kazanç planında çalışanın kaydedilmesini engelleyen eksik bilgi varsa sonuç durumu Uygun Değil olur.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-150">The result status will be Ineligible if the worker didn’t meet the eligibility rule criteria, if the worker is missing required information such as a pay frequency or fixed compensation, or if there is information missing on the benefit plan that prevents workers from being enrolled.</span></span> |
   | <span data-ttu-id="1cd0f-151">**Sonuç iletisi**</span><span class="sxs-lookup"><span data-stu-id="1cd0f-151">**Result message**</span></span> | <span data-ttu-id="1cd0f-152">Bir çalışanın kazanç planı için neden uygun olmadığını veya uygunluk kuralının geçilip geçilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1cd0f-152">Indicates why a worker is ineligible for a benefit plan or if the eligibility rule passed.</span></span> |



[!INCLUDE[footer-include](../includes/footer-banner.md)]