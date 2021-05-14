---
title: Çalışma süresi şablonları oluşturma
description: Çalışma zamanı şablonları bir haftalık çalışma saatlerini tanımlar ve bir dönem için çalışma zamanları oluşturmak için kullanılır.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920941"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="1d488-103">Çalışma süresi şablonları oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d488-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1d488-104">Çalışma zamanı şablonları bir haftalık çalışma saatlerini tanımlar ve bir dönem için çalışma zamanları oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1d488-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="1d488-105">Bu yordam, çalışma zaman aralıklarını kategorilere ayırmak için çalışma zamanı planlama özelliklerini kullanarak bir çalışma zamanı şablonunun nasıl tanımlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d488-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="1d488-106">Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d488-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="1d488-107">**Çalışma alanları > Kaynak yaşam döngüsü yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="1d488-107">Go to **Workspaces > Resource lifecycle management**.</span></span>
1. <span data-ttu-id="1d488-108">**Çalışma zamanı şablonları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="1d488-108">Select **Working time templates**.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="1d488-109">Çalışma zamanı şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="1d488-109">Create working time template</span></span>

1. <span data-ttu-id="1d488-110">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1d488-110">Select **New**.</span></span>
1. <span data-ttu-id="1d488-111">**Çalışma zamanı şablonu** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1d488-111">In the **Working time template** field, type a value.</span></span>
1. <span data-ttu-id="1d488-112">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="1d488-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="1d488-113">**Pazartesi** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="1d488-113">Expand the **Monday** section.</span></span>
1. <span data-ttu-id="1d488-114">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1d488-114">Select **Add**.</span></span>
1. <span data-ttu-id="1d488-115">**Başlangıç** alanında bir saat girin.</span><span class="sxs-lookup"><span data-stu-id="1d488-115">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="1d488-116">İşin sabah başlayacağı saati belirtin.</span><span class="sxs-lookup"><span data-stu-id="1d488-116">Specify the time when work begins in the morning.</span></span>  
1. <span data-ttu-id="1d488-117">**Bitiş** alanında bir saat girin.</span><span class="sxs-lookup"><span data-stu-id="1d488-117">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="1d488-118">Çalışanların öğle yemeği saatini belirtin.</span><span class="sxs-lookup"><span data-stu-id="1d488-118">Specify the time when workers break for lunch.</span></span>  
1. <span data-ttu-id="1d488-119">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1d488-119">Select **Add**.</span></span>
1. <span data-ttu-id="1d488-120">**Başlangıç** alanında bir saat girin.</span><span class="sxs-lookup"><span data-stu-id="1d488-120">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="1d488-121">Öğle yemeğinin ardından işin başlayacağı saati belirtin.</span><span class="sxs-lookup"><span data-stu-id="1d488-121">Specify the time when work resumes after lunch.</span></span>  
1. <span data-ttu-id="1d488-122">**Bitiş** alanında bir saat girin.</span><span class="sxs-lookup"><span data-stu-id="1d488-122">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="1d488-123">İşin bitiş tarihini belirtin.</span><span class="sxs-lookup"><span data-stu-id="1d488-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="1d488-124">Çalışma saatlerini haftanın tüm günleri için çoğaltma</span><span class="sxs-lookup"><span data-stu-id="1d488-124">Replicate working times to all week days</span></span>

1. <span data-ttu-id="1d488-125">**Kopyalama günü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="1d488-125">Select **Copy day**.</span></span>
    * <span data-ttu-id="1d488-126">Çalışma saati tanımlarını Pazartesi gününden Salı gününe kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="1d488-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
1. <span data-ttu-id="1d488-127">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1d488-127">Select **OK**.</span></span>
1. <span data-ttu-id="1d488-128">**Kopyalama günü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="1d488-128">Select **Copy day**.</span></span>
    * <span data-ttu-id="1d488-129">Çalışma saati tanımlarını Pazartesi gününden Çarşamba gününe kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="1d488-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
1. <span data-ttu-id="1d488-130">**Hafta içi bitiş tarihi** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="1d488-130">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="1d488-131">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1d488-131">Select **OK**.</span></span>
1. <span data-ttu-id="1d488-132">**Kopyalama günü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="1d488-132">Select **Copy day**.</span></span>
    * <span data-ttu-id="1d488-133">Çalışma saati tanımlarını Pazartesi gününden Perşembe gününe kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="1d488-133">Copy the working times definitions from Monday to Thursday.</span></span>  
1. <span data-ttu-id="1d488-134">**Hafta içi bitiş tarihi** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="1d488-134">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="1d488-135">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1d488-135">Select **OK**.</span></span>
1. <span data-ttu-id="1d488-136">**Kopyalama günü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="1d488-136">Select **Copy day**.</span></span>
    * <span data-ttu-id="1d488-137">Çalışma saati tanımlarını Pazartesi gününden Cuma gününe kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="1d488-137">Copy the working times definitions from Monday to Friday.</span></span>  
1. <span data-ttu-id="1d488-138">**Hafta içi bitiş tarihi** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="1d488-138">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="1d488-139">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1d488-139">Select **OK**.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="1d488-140">Özel işlemler için zaman dilimi tanımlama</span><span class="sxs-lookup"><span data-stu-id="1d488-140">Define time slots for special operations</span></span>

1. <span data-ttu-id="1d488-141">**Cuma** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="1d488-141">Expand the **Friday** section.</span></span>
1. <span data-ttu-id="1d488-142">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="1d488-142">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="1d488-143">**Özellik** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="1d488-143">In the **Property** field, enter or select a value.</span></span>
1. <span data-ttu-id="1d488-144">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="1d488-144">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="1d488-145">**Özellik** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="1d488-145">In the **Property** field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="1d488-146">Haftasonlarını malzeme çekme için kapatıldı olarak işaretleme</span><span class="sxs-lookup"><span data-stu-id="1d488-146">Mark weekend days as closed for pickup</span></span>

1. <span data-ttu-id="1d488-147">**Cumartesi** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="1d488-147">Expand the **Saturday** section.</span></span>
1. <span data-ttu-id="1d488-148">**Malzeme çekme için kapatıldı** alanında *Evet* seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="1d488-148">Select *Yes* in the **Closed for pickup** field.</span></span>
1. <span data-ttu-id="1d488-149">**Pazar** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="1d488-149">Expand the **Sunday** section.</span></span>
1. <span data-ttu-id="1d488-150">**Malzeme çekme için kapatıldı** alanında *Evet* seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="1d488-150">Select *Yes* in the **Closed for pickup** field.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]