--- 
title: "Toplu iş oluşturma"
description: "Toplu iş, otomatik işlem için bir Uygulama Nesne Sunucusu (AOS) kurulumuna gönderilmiş görevlerin bir grubudur."
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: fbb844ebcf8d4b47b127132a5bf0ea45fa40f747
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-batch-job"></a><span data-ttu-id="95b46-103">Toplu iş oluşturma</span><span class="sxs-lookup"><span data-stu-id="95b46-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="95b46-104">Toplu iş, otomatik işlem için bir Uygulama Nesne Sunucusu (AOS) kurulumuna gönderilmiş görevlerin bir grubudur.</span><span class="sxs-lookup"><span data-stu-id="95b46-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="95b46-105">Toplu işler işi oluşturan kullanıcının güvenlik kimlik bilgilerini kullanarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="95b46-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="95b46-106">Toplu bir iş oluşturmak için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="95b46-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="95b46-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="95b46-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="95b46-108">Toplu işi oluşturun</span><span class="sxs-lookup"><span data-stu-id="95b46-108">Create the batch job</span></span>
1. <span data-ttu-id="95b46-109">Sistem yönetimi > Sorgular > Toplu işler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="95b46-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="95b46-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="95b46-110">Click New.</span></span>
3. <span data-ttu-id="95b46-111">İş açıklaması alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="95b46-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="95b46-112">Planlanan başlangıç tarihi/saati alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="95b46-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="95b46-113">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="95b46-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="95b46-114">Yineleme oluşturun</span><span class="sxs-lookup"><span data-stu-id="95b46-114">Create a recurrence</span></span>
1. <span data-ttu-id="95b46-115">Eylem Bölmesi'nde Toplu iş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="95b46-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="95b46-116">Yineleme'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="95b46-116">Click Recurrence.</span></span>
    * <span data-ttu-id="95b46-117">Bu seçenekleri bir aralık ve yineleme için model girmek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="95b46-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="95b46-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="95b46-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="95b46-119">Uyarılar ekleyin</span><span class="sxs-lookup"><span data-stu-id="95b46-119">Add alerts</span></span>
1. <span data-ttu-id="95b46-120">Eylem Bölmesi'nde Toplu iş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="95b46-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="95b46-121">Uyarılar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="95b46-121">Click Alerts.</span></span>
    * <span data-ttu-id="95b46-122">Toplu işlem bittiğinde, bir hata olduğunda veya iptal edildiğinde uyarı iletileri istiyorsanız belirtin.</span><span class="sxs-lookup"><span data-stu-id="95b46-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="95b46-123">Ardından uyarıların açılır pencere iletileri olarak gösterilmesini istiyorsanız belirtin.</span><span class="sxs-lookup"><span data-stu-id="95b46-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="95b46-124">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="95b46-124">Click OK.</span></span>


