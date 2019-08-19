---
title: Toplu iş oluşturma
description: Toplu iş, otomatik işlem için bir Uygulama Nesne Sunucusu (AOS) kurulumuna gönderilmiş görevlerin bir grubudur.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27541c84a40fe9b7e7705162e06167ad4f7e4ed9
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851299"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="9a406-103">Toplu iş oluşturma</span><span class="sxs-lookup"><span data-stu-id="9a406-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9a406-104">Toplu iş, otomatik işlem için bir Uygulama Nesne Sunucusu (AOS) kurulumuna gönderilmiş görevlerin bir grubudur.</span><span class="sxs-lookup"><span data-stu-id="9a406-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="9a406-105">Toplu işler işi oluşturan kullanıcının güvenlik kimlik bilgilerini kullanarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="9a406-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="9a406-106">Toplu bir iş oluşturmak için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="9a406-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="9a406-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="9a406-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="9a406-108">Toplu işi oluşturun</span><span class="sxs-lookup"><span data-stu-id="9a406-108">Create the batch job</span></span>
1. <span data-ttu-id="9a406-109">**Gezinti bölmesi > Modüller > Sistem yönetimi > Sorgular > Toplu işler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="9a406-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="9a406-110">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a406-110">Click **New**.</span></span>
3. <span data-ttu-id="9a406-111">**İş açıklaması** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9a406-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="9a406-112">**Planlanan başlangıç tarihi/saati** alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="9a406-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="9a406-113">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a406-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="9a406-114">Yineleme oluşturun</span><span class="sxs-lookup"><span data-stu-id="9a406-114">Create a recurrence</span></span>
1. <span data-ttu-id="9a406-115">Eylem Bölmesi'nde **Toplu iş**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a406-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="9a406-116">**Yineleme**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a406-116">Click **Recurrence**.</span></span> <span data-ttu-id="9a406-117">Bu seçenekleri bir aralık ve yineleme için model girmek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="9a406-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="9a406-118">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a406-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="9a406-119">Uyarılar ekleyin</span><span class="sxs-lookup"><span data-stu-id="9a406-119">Add alerts</span></span>
1. <span data-ttu-id="9a406-120">Eylem Bölmesi'nde **Toplu iş**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a406-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="9a406-121">**Uyarılar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a406-121">Click **Alerts**.</span></span> <span data-ttu-id="9a406-122">Toplu işlem bittiğinde, bir hata olduğunda veya iptal edildiğinde uyarı iletileri istiyorsanız belirtin.</span><span class="sxs-lookup"><span data-stu-id="9a406-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="9a406-123">Ardından uyarıların açılır pencere iletileri olarak gösterilmesini istiyorsanız belirtin.</span><span class="sxs-lookup"><span data-stu-id="9a406-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="9a406-124">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a406-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="9a406-125">Toplu iş durumunu düzelt</span><span class="sxs-lookup"><span data-stu-id="9a406-125">Adjust batch job status</span></span>
1. <span data-ttu-id="9a406-126">**Sistem yönetimi > Sorgular > Toplu işler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="9a406-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="9a406-127">Uygun olan toplu işi seçin.</span><span class="sxs-lookup"><span data-stu-id="9a406-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="9a406-128">Eylem Bölmesi'nde **Toplu iş > İşlevler > Durumu değiştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a406-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="9a406-129">Uygun olan durumu seçin:</span><span class="sxs-lookup"><span data-stu-id="9a406-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="9a406-130">**Stopaj**: Toplu işi **stopaj** olarak ayarlayın, böylece toplu iş planlayıcısından kesilir.</span><span class="sxs-lookup"><span data-stu-id="9a406-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="9a406-131">*Durdur* ile eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="9a406-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="9a406-132">**Bekliyor**: Toplu işi **bekliyor** olarak ayarlayın, böylece toplu iş planlayıcısı tarafından alınmayı bekler.</span><span class="sxs-lookup"><span data-stu-id="9a406-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="9a406-133">*Git* ile eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="9a406-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="9a406-134">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a406-134">Click **OK**.</span></span>
