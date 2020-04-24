---
title: Ömür olaylarını işle
description: Microsoft Dynamics 365 Human Resources'un çalışan yaşam döngüsü sırasında, her çalışan çeşitli ömür etkinliği değişiklikleriyle karşılaşabilir.
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
ms.openlocfilehash: ba8d21482a18c6baa93437fc65c165907bdb515d
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229954"
---
# <a name="process-life-events"></a><span data-ttu-id="75b7a-103">Ömür olaylarını işle</span><span class="sxs-lookup"><span data-stu-id="75b7a-103">Process life events</span></span>

<span data-ttu-id="75b7a-104">Microsoft Dynamics 365 Human Resources'un çalışan yaşam döngüsü sırasında, her çalışan çeşitli ömür etkinliği değişiklikleriyle karşılaşabilir.</span><span class="sxs-lookup"><span data-stu-id="75b7a-104">During the employee lifecycle in Microsoft Dynamics 365 Human Resources, each employee may encounter various life event changes.</span></span> <span data-ttu-id="75b7a-105">Örneğin, evlilik, istihdam değişikliği veya bağımlı/lehdarlık değişikliği gibi.</span><span class="sxs-lookup"><span data-stu-id="75b7a-105">For example, marriage, change in employment, or dependent/beneficiary change.</span></span> <span data-ttu-id="75b7a-106">Ömür olaylarını kullanmak için, sosyal haklar parametreleri formunda ömür olaylarını etkinleştirmeniz, ömür olay tiplerini ayarlamanız ve plan tipleri için ömür olayı seçeneklerini ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="75b7a-106">To use life events, you must enable life events in the benefits parameters form, set up life event types, and set up life event options for plan types.</span></span>

<span data-ttu-id="75b7a-107">Ömür olaylarını işleyebilmeniz için, işe alma zaman dilimi sırasında açık kaydı en az bir kere çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="75b7a-107">Before you can process life events, you must have already run open enrollment at least once during a hiring time frame.</span></span> <span data-ttu-id="75b7a-108">Amerika Birleşik Devletleri, her yıl için kayıt açma işlemi genellikle bir kez yapılır.</span><span class="sxs-lookup"><span data-stu-id="75b7a-108">In the United States, open enrollment is typically once per year.</span></span> <span data-ttu-id="75b7a-109">Amerika Birleşik Devletleri dışında, açık kayıt işe alma sırasında çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="75b7a-109">Outside the United States, open enrollment may be run at the time of hire.</span></span> <span data-ttu-id="75b7a-110">Bir çalışanın ömür olaylarının işlenmesi için bir avantaj planı seçmesini, ancak açık kayıt işleme içinde yer almış olmaları gerekmez.</span><span class="sxs-lookup"><span data-stu-id="75b7a-110">A worker does not need to select a benefit plan in order for life events to be processed, but they need to have been included in open enrollment processing.</span></span> 

<span data-ttu-id="75b7a-111">Gelecekteki bir tarihte gerçekleşen ömür olayları olan çalışanlarınız varsa, ömür olayı işlemeyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="75b7a-111">Use life event processing when you have workers who have life events that take place on a future date.</span></span> <span data-ttu-id="75b7a-112">Bu olay, gelecekteki ömür olayları veya bir çalışana özgü olmayan, eklenen ömür olayları (yeni bir örnektir) gibi işlenmediği tüm ömür olaylarını işler.</span><span class="sxs-lookup"><span data-stu-id="75b7a-112">This event will process all life events that have not been processed (like future life events, or life events that have been added that are not specific to any one worker – one example is a new benefit).</span></span> <span data-ttu-id="75b7a-113">Gerçek zamanlı yaşam olayları gizlenir.</span><span class="sxs-lookup"><span data-stu-id="75b7a-113">Real-time life events are hidden.</span></span>

<span data-ttu-id="75b7a-114">Örneğin, bugün 1 Şubat ise ve 14 Şubat'ta Joe Smith'in bir yasal varlıkları değiştirmek için planlandıysa, 15 Şubat tarihinde ömür olayı işlemeyi çalıştırırsanız, sistem 15 Şubat tarihine kadar tüm olayları işler.</span><span class="sxs-lookup"><span data-stu-id="75b7a-114">For example, if today is February 1, and on February 14 worker Joe Smith is scheduled to change legal entities, if you run life event processing for February 15, the system processes all events up until February 15.</span></span> 

1. <span data-ttu-id="75b7a-115">**Sosyal haklar** yönetimi çalışma alanında, **işlem** altında, **Ömür olayı işlemini** seçin.</span><span class="sxs-lookup"><span data-stu-id="75b7a-115">In the **Benefits management** workspace, under **Processing**, select **Life event processing**.</span></span>

2. <span data-ttu-id="75b7a-116">**Ömür olayı işlemini çalıştır** iletişim kutusunda, aşağıdaki alanlar için değer belirtin:</span><span class="sxs-lookup"><span data-stu-id="75b7a-116">In the **Run life event process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="75b7a-117">Alan</span><span class="sxs-lookup"><span data-stu-id="75b7a-117">Field</span></span> | <span data-ttu-id="75b7a-118">Tanım</span><span class="sxs-lookup"><span data-stu-id="75b7a-118">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="75b7a-119">**Kayıt dönemi**</span><span class="sxs-lookup"><span data-stu-id="75b7a-119">**Enrollment period**</span></span> | <span data-ttu-id="75b7a-120">Ömür olayları işleyecek kayıt dönemi.</span><span class="sxs-lookup"><span data-stu-id="75b7a-120">The enrollment period to process life events for.</span></span> |
   | <span data-ttu-id="75b7a-121">**Tüzel kişilik**</span><span class="sxs-lookup"><span data-stu-id="75b7a-121">**Legal entity**</span></span> | <span data-ttu-id="75b7a-122">Ömür olayları işleyecek yasal varlık.</span><span class="sxs-lookup"><span data-stu-id="75b7a-122">The legal entity to process life events for.</span></span> |
   | <span data-ttu-id="75b7a-123">**Yaşam olayı tarihi**</span><span class="sxs-lookup"><span data-stu-id="75b7a-123">**Life event date**</span></span> | <span data-ttu-id="75b7a-124">Sistem, kayıt süresi boyunca bu tarihe kadar olan tüm olayları işler.</span><span class="sxs-lookup"><span data-stu-id="75b7a-124">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="75b7a-125">**Çalışan**</span><span class="sxs-lookup"><span data-stu-id="75b7a-125">**Worker**</span></span> | <span data-ttu-id="75b7a-126">Ömür olayları işleyecek çalışan.</span><span class="sxs-lookup"><span data-stu-id="75b7a-126">The worker to process life events for.</span></span> <span data-ttu-id="75b7a-127">Bu alanı boş bırakırsanız, ömür olayları tüm çalışanlar için işlem görür.</span><span class="sxs-lookup"><span data-stu-id="75b7a-127">If you leave this field blank, life events will be processed for all workers.</span></span> |

3. <span data-ttu-id="75b7a-128">İşlemi arka planda çalıştırmak istiyorsanız, **arka planda Çalıştır** 'ı seçin ve aşağıdaki görevleri gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="75b7a-128">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="75b7a-129">İşlem bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="75b7a-129">Enter information for the process.</span></span>

   2. <span data-ttu-id="75b7a-130">Tekrarlayan iş ayarlamak için **tekrarlama**'yı seçin, yinelenme bilgilerini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="75b7a-130">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="75b7a-131">İş uyarısı ayarlamak için, **uyarılar**'ı seçin, alınacak uyarıları seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="75b7a-131">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="75b7a-132">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="75b7a-132">Select **OK**.</span></span> <span data-ttu-id="75b7a-133">İşlem, ayarladığınız parametrelerle çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="75b7a-133">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="75b7a-134">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="75b7a-134">Select **OK**.</span></span>
