---
title: Çalışma zamanı takvimi oluşturma
description: Dynamics 365 Human Resources'ta Çalışma zamanı takvimi, tatiller ve çalışma dışı zamanları tanımlayın .
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dc209b62836011b18362f78b63cdd3fcda884dc3
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198039"
---
# <a name="create-a-working-time-calendar"></a><span data-ttu-id="b7b14-103">Çalışma zamanı takvimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b7b14-103">Create a working time calendar</span></span>

<span data-ttu-id="b7b14-104">Dynamics 365 Human Resources'deki bir çalışma zamanı takvimi, çalışanların kuruluşunuzda çalıştığı günleri ve saatleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="b7b14-104">A working time calendar in Dynamics 365 Human Resources shows the days and hours that employees work in your organization.</span></span> <span data-ttu-id="b7b14-105">Bir çalışan zaman aşımı isteği gönderdiğinde, tatiller ve kapanışlar hakkında endişelenmenize gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="b7b14-105">When an employee submits a time-off request, they don't have to worry about holidays and closures.</span></span>

<span data-ttu-id="b7b14-106">Zaman aşımı isteklerini kolaylaştırmak için, bu öğeleri kuruluşunuz için konfigüre edin:</span><span class="sxs-lookup"><span data-stu-id="b7b14-106">To streamline time-off requests, configure these items for your organization:</span></span>

- <span data-ttu-id="b7b14-107">çalışma takvimi</span><span class="sxs-lookup"><span data-stu-id="b7b14-107">Working time calendar</span></span>
- <span data-ttu-id="b7b14-108">Tatiller ve kapanışlar</span><span class="sxs-lookup"><span data-stu-id="b7b14-108">Holidays and closures</span></span>
- <span data-ttu-id="b7b14-109">Çalışmama süresi</span><span class="sxs-lookup"><span data-stu-id="b7b14-109">Non-work time</span></span>

<span data-ttu-id="b7b14-110">Çalışma zamanı takvimi ayarlarken son iki öğeyi ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b7b14-110">You can add the last two items while you're setting up a working time calendar.</span></span> <span data-ttu-id="b7b14-111">Ayrıca, bunları ayrı olarak yapılandırabilir veya güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b7b14-111">You can also configure or update them separately.</span></span>

## <a name="set-up-a-working-time-calendar"></a><span data-ttu-id="b7b14-112">Bir çalışma zamanı takvimi ayarlama</span><span class="sxs-lookup"><span data-stu-id="b7b14-112">Set up a working time calendar</span></span>

<span data-ttu-id="b7b14-113">Günlerinizi ve operasyon saatlerinizi gösteren en az bir çalışma zamanı takvimi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b7b14-113">Set up at least one working time calendar that shows your days and hours of operation.</span></span> <span data-ttu-id="b7b14-114">Birden fazla ülkede ve bölgede konumlarınız varsa, her alan için bir çalışma zamanı takvimi ayarlamak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b7b14-114">If you have locations in multiple countries and regions, you might want to set up a working time calendar for each area.</span></span>

1. <span data-ttu-id="b7b14-115">**Kuruluş yönetimi** sayfasında **Takvimler** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b7b14-115">On the **Organization administration** page, select **Calendars**.</span></span>

2. <span data-ttu-id="b7b14-116">**Yeni**'yi seçin ve takviminiz için bir ad ve açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="b7b14-116">Select **New** and enter a name and description for your calendar.</span></span>

3. <span data-ttu-id="b7b14-117">**Oluşturma seçenekleri** altında, organizasyonunuzun iş günlerini seçin ve çalışma sürelerini girin.</span><span class="sxs-lookup"><span data-stu-id="b7b14-117">Under **Generation options**, select the work days for your organization and enter work times.</span></span> 
   - <span data-ttu-id="b7b14-118">Tatil veya kapanış eklemek için, **tatiller ve kapanışlar** yanında **Ekle** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b7b14-118">To add a holiday or closure, select the **Add** button next to **Holidays and closures**.</span></span>
   - <span data-ttu-id="b7b14-119">Yarım ve daha fazla mola gibi çalışma dışı zamanı eklemek için **çalışma dışı süresi** altında **Ekle**'yi seçin ve ad ve zaman aralığını girin.</span><span class="sxs-lookup"><span data-stu-id="b7b14-119">To add non-work time, like lunches or breaks, select **Add** under **NON-WORK TIME** and enter the name and time range.</span></span>

4. <span data-ttu-id="b7b14-120">**Günler** altında, takviminizde günleri oluşturmak için **Oluştur** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b7b14-120">Under **Days**, select **Generate** to generate the days in your calendar.</span></span> <span data-ttu-id="b7b14-121">Takviminizin tarih aralığını girin ve **gün oluştur** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="b7b14-121">Enter the date range for your calendar and then select **Generate days**.</span></span>

5. <span data-ttu-id="b7b14-122">Çalışma zamanlamaları eklemek için, **çalışma zamanlaması** altında, **Ekle**'yi seçin ve her iş çizelgesi için saatleri girin.</span><span class="sxs-lookup"><span data-stu-id="b7b14-122">To add work schedules, under **Work schedule**, select **Add** and then enter the times for each work schedule.</span></span>

## <a name="configure-holidays-and-closures"></a><span data-ttu-id="b7b14-123">Tatiller ve kapanışları yapılandırın</span><span class="sxs-lookup"><span data-stu-id="b7b14-123">Configure holidays and closures</span></span>

<span data-ttu-id="b7b14-124">Tatilleri ve kapanışları, çalışma zamanı takviminden ayrı olarak ekleyebilir veya değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b7b14-124">You can add or change holidays and closures separately from a working time calendar.</span></span>

1. <span data-ttu-id="b7b14-125">**Kuruluş yönetimi** sayfasında **Tatiller ve kapanışlar** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b7b14-125">On the **Organization administration** page, select **Holidays and closures**.</span></span>

2. <span data-ttu-id="b7b14-126">**Yeni**'yi seçin ve tatil veya kapanış için bir ad ve tarih girin.</span><span class="sxs-lookup"><span data-stu-id="b7b14-126">Select **New** and enter a name and date for the holiday or closure.</span></span>

## <a name="configure-non-work-time"></a><span data-ttu-id="b7b14-127">Çalışmama süresi yapılandırın</span><span class="sxs-lookup"><span data-stu-id="b7b14-127">Configure non-work time</span></span>

<span data-ttu-id="b7b14-128">Çalışmama süreleri çalışma zamanı takviminden ayrı olarak ekleyebilir veya değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b7b14-128">You can add or change non-work times separately from a working time calendar.</span></span>

1. <span data-ttu-id="b7b14-129">**Kuruluş yönetimi** sayfasında **Çalışmama süresi** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b7b14-129">On the **Organization administration** page, select **Non-work time**.</span></span>

2. <span data-ttu-id="b7b14-130">**Yeni**'yi seçin ve çalışmama süresi ad ve zaman aralığı girin.</span><span class="sxs-lookup"><span data-stu-id="b7b14-130">Select **New** and enter a name and time range for the non-work time.</span></span>

<span data-ttu-id="b7b14-131">İzin ve devamsızlığı Banka tatili düzeltmeleri önizlemesi özelliğini etkinleştirdiyseniz, İnsan Kaynakları takvimde kayıtlı olan çalışanlara göre ayarlanacak gün sayısını belirlemek için tatiller ve kapatma tarihleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="b7b14-131">If you've enabled the Leave and absence bank holiday corrections preview feature, Human Resources uses holidays and closure dates to determine the number of days to adjust for employees enrolled in the calendar.</span></span>

## <a name="see-also"></a><span data-ttu-id="b7b14-132">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="b7b14-132">See also</span></span>

- [<span data-ttu-id="b7b14-133">İzin ve devamsızlığa genel bakış</span><span class="sxs-lookup"><span data-stu-id="b7b14-133">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="b7b14-134">İzin ve devamsızlık türleri yapılandır</span><span class="sxs-lookup"><span data-stu-id="b7b14-134">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)
