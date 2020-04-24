---
title: İşlem kayıt uygunluğu
description: Bu makalede, kayıt uygunluk işleminin nasıl çalıştırıldığı açıklanır.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1d978982213e713e362798c49aa57e6dc8b7a862
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230028"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="2e035-103">İşlem kayıt uygunluğu</span><span class="sxs-lookup"><span data-stu-id="2e035-103">Process enrollment eligibility</span></span>

<span data-ttu-id="2e035-104">Bu makalede, kayıt uygunluk işleminin nasıl çalıştırıldığı açıklanır.</span><span class="sxs-lookup"><span data-stu-id="2e035-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="2e035-105">**Sosyal haklar** yönetimi çalışma alanında, **işlem** altında, kayıt **uygunluk işlemini** seçin.</span><span class="sxs-lookup"><span data-stu-id="2e035-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="2e035-106">**Kazanç kaydı uygunluk işlemini çalıştır** iletişim kutusunda, aşağıdaki alanlar için değer belirtin:</span><span class="sxs-lookup"><span data-stu-id="2e035-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="2e035-107">Alan</span><span class="sxs-lookup"><span data-stu-id="2e035-107">Field</span></span> | <span data-ttu-id="2e035-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e035-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="2e035-109">**Kayıt dönemi**</span><span class="sxs-lookup"><span data-stu-id="2e035-109">**Enrollment period**</span></span> | <span data-ttu-id="2e035-110">Kayıt uygunluğunu işleyecek kayıt dönemi.</span><span class="sxs-lookup"><span data-stu-id="2e035-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="2e035-111">**Tüzel kişilik**</span><span class="sxs-lookup"><span data-stu-id="2e035-111">**Legal entity**</span></span> | <span data-ttu-id="2e035-112">Yasal varlık işleyecek kayıt dönemi.</span><span class="sxs-lookup"><span data-stu-id="2e035-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="2e035-113">**Çalışan**</span><span class="sxs-lookup"><span data-stu-id="2e035-113">**Worker**</span></span> | <span data-ttu-id="2e035-114">Çalışan işleyecek kayıt dönemi.</span><span class="sxs-lookup"><span data-stu-id="2e035-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="2e035-115">Bu alanı boş bırakırsanız, kayıt uygunluğu tüm çalışanlar için işlem görür.</span><span class="sxs-lookup"><span data-stu-id="2e035-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="2e035-116">**Kazanç planı**</span><span class="sxs-lookup"><span data-stu-id="2e035-116">**Benefit plan**</span></span> | <span data-ttu-id="2e035-117">Kazanç planı işleyecek kayıt dönemi.</span><span class="sxs-lookup"><span data-stu-id="2e035-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="2e035-118">İşlemi arka planda çalıştırmak istiyorsanız, **arka planda Çalıştır** 'ı seçin ve aşağıdaki görevleri gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="2e035-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="2e035-119">İşlem bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="2e035-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="2e035-120">Tekrarlayan iş ayarlamak için **tekrarlama**'yı seçin, yinelenme bilgilerini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2e035-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="2e035-121">İş uyarısı ayarlamak için, **uyarılar**'ı seçin, alınacak uyarıları seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2e035-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="2e035-122">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2e035-122">Select **OK**.</span></span> <span data-ttu-id="2e035-123">İşlem, ayarladığınız parametrelerle çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="2e035-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="2e035-124">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2e035-124">Select **OK**.</span></span>

## <a name="view-process-results"></a><span data-ttu-id="2e035-125">İşlem Sonuçlarını Görüntüleme</span><span class="sxs-lookup"><span data-stu-id="2e035-125">View Process Results</span></span>

<span data-ttu-id="2e035-126">Bu makalede, uygunluk işlemi sonuçlarının nasıl görüntüleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="2e035-126">This article explains how to view eligibility process results.</span></span>

1.  <span data-ttu-id="2e035-127">**Kazanç yönetimi** çalışma alanında, **İşleme** altında, **İşlem sonuçları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2e035-127">In the **Benefits management** workspace, under **Processing**, select **Process results**.</span></span>

2.  <span data-ttu-id="2e035-128">**İşlem sonuçları** formunda, aşağıdaki alanlar belirtilir:</span><span class="sxs-lookup"><span data-stu-id="2e035-128">In the **Process results** form, the following fields are specified:</span></span>

   | <span data-ttu-id="2e035-129">Alan</span><span class="sxs-lookup"><span data-stu-id="2e035-129">Field</span></span> | <span data-ttu-id="2e035-130">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e035-130">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="2e035-131">**İşlem Kodu**</span><span class="sxs-lookup"><span data-stu-id="2e035-131">**Process ID**</span></span> | <span data-ttu-id="2e035-132">Çalışan, Tüzel kişilik ve işlem çalıştırma birleşiminin benzersiz kodu.</span><span class="sxs-lookup"><span data-stu-id="2e035-132">The unique ID for the combination of Worker, Legal entity, and process run.</span></span> |
   | <span data-ttu-id="2e035-133">**İşlem türü**</span><span class="sxs-lookup"><span data-stu-id="2e035-133">**Process type**</span></span> | <span data-ttu-id="2e035-134">Çalıştırılmış olan işlemi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="2e035-134">This identifies the process that was run.</span></span> <span data-ttu-id="2e035-135">Örnek: Kayıt.</span><span class="sxs-lookup"><span data-stu-id="2e035-135">For example:  Enrollment.</span></span> |
   | <span data-ttu-id="2e035-136">**Zaman damgası**</span><span class="sxs-lookup"><span data-stu-id="2e035-136">**Time stamp**</span></span> | <span data-ttu-id="2e035-137">Uygunluk işleminin çalıştırıldığı zaman.</span><span class="sxs-lookup"><span data-stu-id="2e035-137">The time that the eligibility process was run.</span></span> |
   | <span data-ttu-id="2e035-138">**Tüzel kişilik**</span><span class="sxs-lookup"><span data-stu-id="2e035-138">**Legal entity**</span></span> | <span data-ttu-id="2e035-139">Kayıt işlemi sırasında belirtilen tüzel kişilik.</span><span class="sxs-lookup"><span data-stu-id="2e035-139">The legal entity specified during the enrollment process.</span></span> |
   | <span data-ttu-id="2e035-140">**Çalışan**</span><span class="sxs-lookup"><span data-stu-id="2e035-140">**Worker**</span></span> | <span data-ttu-id="2e035-141">İşlenmiş olan çalışan.</span><span class="sxs-lookup"><span data-stu-id="2e035-141">The worker who was processed.</span></span> |
   | <span data-ttu-id="2e035-142">\*\*Plan</span><span class="sxs-lookup"><span data-stu-id="2e035-142">\*\*Plan</span></span> | <span data-ttu-id="2e035-143">Kaydın denendiği Kazanç planı.</span><span class="sxs-lookup"><span data-stu-id="2e035-143">The Benefit plan that enrollment was attempted for.</span></span> |
   | <span data-ttu-id="2e035-144">**Uygunluk kuralı**</span><span class="sxs-lookup"><span data-stu-id="2e035-144">**Eligibility rule**</span></span> | <span data-ttu-id="2e035-145">İşlenmiş olan uygunluk kuralı.</span><span class="sxs-lookup"><span data-stu-id="2e035-145">The eligibility rule that was processed.</span></span> <span data-ttu-id="2e035-146">Uygunluk çalıştırılmadan önce hata oluştuysa, bu boş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="2e035-146">If an error was encountered before eligibility was run, this will be blank.</span></span> <span data-ttu-id="2e035-147">Örnek: Bir çalışan için ücret tanımlanmadıysa, uygunluk işlemi çalışmaz ve bu alan boş bırakılır.</span><span class="sxs-lookup"><span data-stu-id="2e035-147">For example: If compensation hasn't been defined for a worker, the eligibility process won't run, and this field will be left blank.</span></span> |
   | <span data-ttu-id="2e035-148">**Sonuç durumu**</span><span class="sxs-lookup"><span data-stu-id="2e035-148">**Result status**</span></span> | <span data-ttu-id="2e035-149">Bu, Uygun veya Uygun Değil olacaktır.</span><span class="sxs-lookup"><span data-stu-id="2e035-149">This will be Eligible or Ineligible.</span></span> <span data-ttu-id="2e035-150">Çalışan uygunluk kuralı kriterini karşılamıyorsa, çalışanın ödeme sıklığı veya sabit ücret gibi gerekli bilgileri eksikse veya kazanç planında çalışanın kaydedilmesini engelleyen eksik bilgi varsa sonuç durumu Uygun Değil olur.</span><span class="sxs-lookup"><span data-stu-id="2e035-150">The result status will be Ineligible if the worker didn’t meet the eligibility rule criteria, if the worker is missing required information such as a pay frequency or fixed compensation, or if there is information missing on the benefit plan that prevents workers from being enrolled.</span></span> |
   | <span data-ttu-id="2e035-151">**Sonuç iletisi**</span><span class="sxs-lookup"><span data-stu-id="2e035-151">**Result message**</span></span> | <span data-ttu-id="2e035-152">Bir çalışanın kazanç planı için neden uygun olmadığını veya uygunluk kuralının geçilip geçilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2e035-152">Indicates why a worker is ineligible for a benefit plan or if the eligibility rule passed.</span></span> |

