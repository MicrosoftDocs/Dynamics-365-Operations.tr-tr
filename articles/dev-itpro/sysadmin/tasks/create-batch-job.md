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
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d211dcd7cb47df135d395d2a993429746aa35a85
ms.sourcegitcommit: 6ba4006fb6a67ddd4b1e54e3d62b9d1239b5e5a3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/21/2019
ms.locfileid: "1700853"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="1abec-103">Toplu iş oluşturma</span><span class="sxs-lookup"><span data-stu-id="1abec-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1abec-104">Toplu iş, otomatik işlem için bir Uygulama Nesne Sunucusu (AOS) kurulumuna gönderilmiş görevlerin bir grubudur.</span><span class="sxs-lookup"><span data-stu-id="1abec-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="1abec-105">Toplu işler işi oluşturan kullanıcının güvenlik kimlik bilgilerini kullanarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="1abec-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="1abec-106">Toplu bir iş oluşturmak için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="1abec-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="1abec-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="1abec-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="1abec-108">Toplu işi oluşturun</span><span class="sxs-lookup"><span data-stu-id="1abec-108">Create the batch job</span></span>
1. <span data-ttu-id="1abec-109">**Gezinti bölmesi > Modüller > Sistem yönetimi > Sorgular > Toplu işler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="1abec-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="1abec-110">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1abec-110">Click **New**.</span></span>
3. <span data-ttu-id="1abec-111">**İş açıklaması** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="1abec-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="1abec-112">**Planlanan başlangıç tarihi/saati** alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="1abec-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="1abec-113">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1abec-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="1abec-114">Yineleme oluşturun</span><span class="sxs-lookup"><span data-stu-id="1abec-114">Create a recurrence</span></span>
1. <span data-ttu-id="1abec-115">Eylem Bölmesi'nde **Toplu iş**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1abec-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="1abec-116">**Yineleme**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1abec-116">Click **Recurrence**.</span></span> <span data-ttu-id="1abec-117">Bu seçenekleri bir aralık ve yineleme için model girmek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="1abec-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="1abec-118">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1abec-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="1abec-119">Uyarılar ekleyin</span><span class="sxs-lookup"><span data-stu-id="1abec-119">Add alerts</span></span>
1. <span data-ttu-id="1abec-120">Eylem Bölmesi'nde **Toplu iş**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1abec-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="1abec-121">**Uyarılar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1abec-121">Click **Alerts**.</span></span> <span data-ttu-id="1abec-122">Toplu işlem bittiğinde, bir hata olduğunda veya iptal edildiğinde uyarı iletileri istiyorsanız belirtin.</span><span class="sxs-lookup"><span data-stu-id="1abec-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="1abec-123">Ardından uyarıların açılır pencere iletileri olarak gösterilmesini istiyorsanız belirtin.</span><span class="sxs-lookup"><span data-stu-id="1abec-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="1abec-124">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1abec-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="1abec-125">Toplu iş durumunu düzelt</span><span class="sxs-lookup"><span data-stu-id="1abec-125">Adjust batch job status</span></span>
1. <span data-ttu-id="1abec-126">**Sistem yönetimi > Sorgular > Toplu işler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="1abec-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="1abec-127">Uygun olan toplu işi seçin.</span><span class="sxs-lookup"><span data-stu-id="1abec-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="1abec-128">Eylem Bölmesi'nde **Toplu iş > İşlevler > Durumu değiştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1abec-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="1abec-129">Uygun olan durumu seçin:</span><span class="sxs-lookup"><span data-stu-id="1abec-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="1abec-130">**Stopaj**: Toplu işi **stopaj** olarak ayarlayın, böylece toplu iş planlayıcısından kesilir.</span><span class="sxs-lookup"><span data-stu-id="1abec-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="1abec-131">*Durdur* ile eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="1abec-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="1abec-132">**Bekliyor**: Toplu işi **bekliyor** olarak ayarlayın, böylece toplu iş planlayıcısı tarafından alınmayı bekler.</span><span class="sxs-lookup"><span data-stu-id="1abec-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="1abec-133">*Git* ile eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="1abec-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="1abec-134">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1abec-134">Click **OK**.</span></span>
