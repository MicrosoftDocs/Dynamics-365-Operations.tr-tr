---
title: "Toplu işe alma projeleri"
description: "Toplu işe alma projeleri, insan kaynakları uzmanlarının çoklu pozisyonlar oluşturmasına ve çalışanları bu pozisyonlar için etkili biçimde işe almasına imkan verir."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HRMMassHireProject
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 7481
ms.assetid: 5f5eb271-76eb-4305-bd1c-5d171dafccc9
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e98e6b3baf57302804d9171833f2b48b60355b22
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="mass-hire-projects"></a><span data-ttu-id="585de-103">Toplu işe alma projeleri</span><span class="sxs-lookup"><span data-stu-id="585de-103">Mass hire projects</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="585de-104">Toplu işe alma projeleri, insan kaynakları uzmanlarının çoklu pozisyonlar oluşturmasına ve çalışanları bu pozisyonlar için etkili biçimde işe almasına imkan verir.</span><span class="sxs-lookup"><span data-stu-id="585de-104">Mass hire projects allow human resources specialists to create multiple positions and efficiently hire workers into those positions.</span></span>

<a name="overview"></a><span data-ttu-id="585de-105">Özet</span><span class="sxs-lookup"><span data-stu-id="585de-105">Overview</span></span>
--------

<span data-ttu-id="585de-106">Dönemsel bir talebin karşılanması gibi durumlarda, aynı anda birden fazla çalışanı işe aldığınızda toplu işe alma projeleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="585de-106">Use mass hire projects when you hire multiple workers at one time, such as when you hire to meet a seasonal demand.</span></span> <span data-ttu-id="585de-107">Pozisyon kayıtlarını, çalışan kayıtlarını ve pozisyonlar için çalışan atamalarını aynı anda oluşturabildiğinizden toplu işe alma projesi oluşturulması kullanışlı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="585de-107">Creating a mass hire project is useful because you can create position records, worker records, and worker assignments for positions at the same time.</span></span> <span data-ttu-id="585de-108">Bir toplu işe alma projesi için pozisyonlar oluştururken şu bilgileri belirtebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="585de-108">When you create positions for a mass hire project, you can specify the following information:</span></span>
-   <span data-ttu-id="585de-109">Oluşturulacak pozisyon sayısı</span><span class="sxs-lookup"><span data-stu-id="585de-109">The number of positions to create</span></span>
-   <span data-ttu-id="585de-110">Pozisyonlar için işe alacağınız insanların çalışan türü</span><span class="sxs-lookup"><span data-stu-id="585de-110">The worker type of the people that you will hire for the positions</span></span>
-   <span data-ttu-id="585de-111">Pozisyonlarla bağlantılı departman ve iş</span><span class="sxs-lookup"><span data-stu-id="585de-111">The department and the job that are associated with the positions</span></span>
-   <span data-ttu-id="585de-112">Pozisyonun tam zamanlı eşdeğeri</span><span class="sxs-lookup"><span data-stu-id="585de-112">The full-time equivalent value of the position</span></span>

## <a name="example"></a><span data-ttu-id="585de-113">Örnek</span><span class="sxs-lookup"><span data-stu-id="585de-113">Example</span></span>
<span data-ttu-id="585de-114">Yaz aylarında şirketinizdeki açık stajyer pozisyonlarını doldurmak için genellikle 15-20 üniversite öğrencisini yarı zamanlı çalıştırmak üzere işe alıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="585de-114">In the summer, you usually hire 15-20 part-time college students to fill available internships in your company.</span></span> <span data-ttu-id="585de-115">Bu yıl beş muhasebeci, beş sipariş işleme personeli ve beş kasiyerler işe almak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="585de-115">This year, you want to hire five accountants, five order processors, and five cashiers.</span></span> <span data-ttu-id="585de-116">Her bir pozisyon kaydını ve çalışan kaydını ayrı ayrı oluşturmak yerine "Yazstajyerleri" adlı bir toplu işe alma projesi oluşturuyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="585de-116">Instead of creating each position record and worker record separately, you create one mass hire project called “SummerInterns”.</span></span> <span data-ttu-id="585de-117">Proje başlangıç ve bitiş tarihleri, toplu işe alma projesi için oluşturduğunuz pozisyonlar için pozisyon sürelerinin başlangıç ve bitiş tarihleri ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="585de-117">The project start and end dates correlate with the start and end dates of the position durations for the positions you create for the mass hire project.</span></span> 

<span data-ttu-id="585de-118">**Toplu işe alma projeleri** sayfasında, "Yazstajyerleri" projesini seçin ve ardından **Projeyi aç** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="585de-118">In the **Mass hire projects** page, select the “SummerInterns” project and then click **Open project**.</span></span> <span data-ttu-id="585de-119">Açık toplu işe alma projesinde **Pozisyonlar oluştur** düğmesini tıklayın ve muhasebeci hakkındaki bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="585de-119">In the open mass hire project, click **Create positions** and enter information about the accountant position.</span></span> <span data-ttu-id="585de-120">Her biri için aynı bilgiler kullanılarak oluşturulmasını istediğiniz beş muhasebe pozisyonu olduğunu belirtebilir ve ardından Tamam düğmesini tıklayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="585de-120">You can indicate that five accountant positions should be created using the same information for each one, and then click OK.</span></span> <span data-ttu-id="585de-121">Bu işlemi sipariş alma yetkilisi ve kasiyer pozisyonları için de tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="585de-121">Repeat this process for the order processor and cashier positions.</span></span> 

<span data-ttu-id="585de-122">Stajyer pozisyonları için işe alacağınız öğrencileri seçtikten sonra, her bir öğrencinin bilgilerini o öğrenciyi işe aldığınız pozisyon için **Pozisyon bilgileri** altına gireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="585de-122">After selecting students to hire for the internship positions, you'll enter each student’s information in the **Position details** for the position that you're hiring them for.</span></span> <span data-ttu-id="585de-123">Tüm pozisyon bilgilerini girdikten sonra Toplu işe alma projesi sayfasından projeyi seçin ve **İşe alma** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="585de-123">When you have entered all of the position details, select the position in the Mass hire projects page, and then click **Hire**.</span></span> <span data-ttu-id="585de-124">Her bir pozisyon için bir pozisyon kaydı oluşturulacak ve bir çalışan kaydı oluşturulacak ve işe aldığınız her bir kişi için doğru pozisyona atanacaktır.</span><span class="sxs-lookup"><span data-stu-id="585de-124">A position record will be created for each position and a worker record will be created and assigned to the correct position for each person who you hire.</span></span>

## <a name="mass-hire-project-statuses"></a><span data-ttu-id="585de-125">Toplu işe alma projesinin durumları</span><span class="sxs-lookup"><span data-stu-id="585de-125">Mass hire project statuses</span></span>
<span data-ttu-id="585de-126">Bir toplu işe alma projesi aşağıdaki durumlara sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="585de-126">A mass hire project can have the following statuses.</span></span>
-   <span data-ttu-id="585de-127">Oluşturulma</span><span class="sxs-lookup"><span data-stu-id="585de-127">Created</span></span>
-   <span data-ttu-id="585de-128">Açık</span><span class="sxs-lookup"><span data-stu-id="585de-128">Open</span></span>
-   <span data-ttu-id="585de-129">Kapalı</span><span class="sxs-lookup"><span data-stu-id="585de-129">Closed</span></span>

<span data-ttu-id="585de-130">**Toplu işe alma projesi** sayfasında bir toplu işe alma projesinin durumunu değiştirmek için **Projeyi aç** veya **Projeyi kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="585de-130">On the **Mass hire project** page, click **Open project** or **Close project** to change the status of a mass hire project.</span></span> <span data-ttu-id="585de-131">Aşağıdaki tablo, durumuna bağlı olarak proje ile neler yapabileceğinizi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="585de-131">The following table describes what you can do with a project according to its status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="585de-132">Durum</span><span class="sxs-lookup"><span data-stu-id="585de-132">Status</span></span></th>
<th><span data-ttu-id="585de-133">Açıklama</span><span class="sxs-lookup"><span data-stu-id="585de-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="585de-134">Oluşturulma</span><span class="sxs-lookup"><span data-stu-id="585de-134">Created</span></span></td>
<td><span data-ttu-id="585de-135">Proje için bilgi oluşturabilir veya değiştirebilirsiniz, ama pozisyon oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="585de-135">You can create and modify information, but cannot create positions for the project.</span></span> <span data-ttu-id="585de-136">Bu yeni projeler için varsayılan durumdur.</span><span class="sxs-lookup"><span data-stu-id="585de-136">This is the default status for new projects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="585de-137">Açık</span><span class="sxs-lookup"><span data-stu-id="585de-137">Open</span></span></td>
<td><span data-ttu-id="585de-138">Proje bilgilerini değiştirebilir, toplu işe alma projesi için pozisyonlar oluşturabilir ve pozisyonlar için personel işe alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="585de-138">You can modify the project details, create positions for the mass hire project, and hire people for the positions.</span></span> <span data-ttu-id="585de-139">Aktif projelerin durumudur.</span><span class="sxs-lookup"><span data-stu-id="585de-139">This is the status for active projects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="585de-140">Kapalı</span><span class="sxs-lookup"><span data-stu-id="585de-140">Closed</span></span></td>
<td><span data-ttu-id="585de-141">Projeye pozisyonlar ekleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="585de-141">You cannot add positions to the project.</span></span> <span data-ttu-id="585de-142">Toplu işe alma projesine pozisyonlar eklemek için projeyi tekrar açın.</span><span class="sxs-lookup"><span data-stu-id="585de-142">To add positions to the mass hire project, open the project again.</span></span> <span data-ttu-id="585de-143">Tamamlanmış projelerin durumudur.</span><span class="sxs-lookup"><span data-stu-id="585de-143">This is the status for completed projects.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="585de-144"><strong>Not </strong></span><span class="sxs-lookup"><span data-stu-id="585de-144"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="585de-145">Bir toplu işe alma projesini kapatmadan önce projedeki tüm pozisyonları durumunun mutlaka Oluşturuldu veya Kapatıldı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="585de-145">Before you can close a mass hire project, all positions in the project must have a status of either Created or Closed.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
</tbody>
</table>

 





