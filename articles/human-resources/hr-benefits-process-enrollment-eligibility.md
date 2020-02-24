---
title: İşlem kayıt uygunluğu
description: Bu makalede, kayıt uygunluk işleminin nasıl çalıştırıldığı açıklanır.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 0344c48460a7d1540481e09ba106526e119de72b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010809"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="101fa-103">İşlem kayıt uygunluğu</span><span class="sxs-lookup"><span data-stu-id="101fa-103">Process enrollment eligibility</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="101fa-104">Bu makalede, kayıt uygunluk işleminin nasıl çalıştırıldığı açıklanır.</span><span class="sxs-lookup"><span data-stu-id="101fa-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="101fa-105">**Sosyal haklar** yönetimi çalışma alanında, **işlem** altında, kayıt **uygunluk işlemini** seçin.</span><span class="sxs-lookup"><span data-stu-id="101fa-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="101fa-106">**Kazanç kaydı uygunluk işlemini çalıştır** iletişim kutusunda, aşağıdaki alanlar için değer belirtin:</span><span class="sxs-lookup"><span data-stu-id="101fa-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="101fa-107">Alan</span><span class="sxs-lookup"><span data-stu-id="101fa-107">Field</span></span> | <span data-ttu-id="101fa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="101fa-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="101fa-109">Kayıt dönemi</span><span class="sxs-lookup"><span data-stu-id="101fa-109">Enrollment period</span></span> | <span data-ttu-id="101fa-110">Kayıt uygunluğunu işleyecek kayıt dönemi.</span><span class="sxs-lookup"><span data-stu-id="101fa-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="101fa-111">Tüzel kişilik</span><span class="sxs-lookup"><span data-stu-id="101fa-111">Legal entity</span></span> | <span data-ttu-id="101fa-112">Yasal varlık işleyecek kayıt dönemi.</span><span class="sxs-lookup"><span data-stu-id="101fa-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="101fa-113">Çalışan</span><span class="sxs-lookup"><span data-stu-id="101fa-113">Worker</span></span> | <span data-ttu-id="101fa-114">Çalışan işleyecek kayıt dönemi.</span><span class="sxs-lookup"><span data-stu-id="101fa-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="101fa-115">Bu alanı boş bırakırsanız, kayıt uygunluğu tüm çalışanlar için işlem görür.</span><span class="sxs-lookup"><span data-stu-id="101fa-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="101fa-116">Kazanç planı</span><span class="sxs-lookup"><span data-stu-id="101fa-116">Benefit plan</span></span> | <span data-ttu-id="101fa-117">Kazanç planı işleyecek kayıt dönemi.</span><span class="sxs-lookup"><span data-stu-id="101fa-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="101fa-118">İşlemi arka planda çalıştırmak istiyorsanız, **arka planda Çalıştır** 'ı seçin ve aşağıdaki görevleri gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="101fa-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="101fa-119">İşlem bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="101fa-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="101fa-120">Tekrarlayan iş ayarlamak için **tekrarlama**'yı seçin, yinelenme bilgilerini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="101fa-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="101fa-121">İş uyarısı ayarlamak için, **uyarılar**'ı seçin, alınacak uyarıları seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="101fa-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="101fa-122">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="101fa-122">Select **OK**.</span></span> <span data-ttu-id="101fa-123">İşlem, ayarladığınız parametrelerle çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="101fa-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="101fa-124">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="101fa-124">Select **OK**.</span></span>
