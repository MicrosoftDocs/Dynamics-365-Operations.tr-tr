---
title: Ana planlama işini iptal etme
description: Bu konuda, yerleşik planlama işlevini kullanan etkin bir planlama işinin nasıl iptal edileceği açıklanmaktadır.
author: ChristianRytt
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: c04e2b2c0e5d7f28ea688578b3e1d7a1e1d9f6d3
ms.sourcegitcommit: 66eae22cd99e53fe8e4c6c94945ad8061b69a442
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117460"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="b0b52-103">Ana planlama işini iptal etme</span><span class="sxs-lookup"><span data-stu-id="b0b52-103">Cancel a master planning job</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0b52-104">Microsoft Dynamics 365 Supply Chain Management'ta, Master planlama işini iptal etmek için çoklu seçenekler vardır.</span><span class="sxs-lookup"><span data-stu-id="b0b52-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="b0b52-105">Örneğin, bir ana planlama işini yanlışlıkla başlatılmış veya beklenenden uzun süre çalıştırılarak iptal etmek isteyebilirsiniz ve sonlandırmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0b52-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="b0b52-106">Bir planlama işini iptal etmenin en iyi yolu, **tamamlanmamış planlama işlemleri** sayfasından alınır.</span><span class="sxs-lookup"><span data-stu-id="b0b52-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="b0b52-107">**Toplu iş** ve **toplu iş gelişmiş** sayfalarından alternatif seçenekler yalnızca, **bitmemiş planlama işlemleri** sayfasından bir kaç dakika içinde ana planlama işi iptal edilirken kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b0b52-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="b0b52-108">Tercih edilen iptal seçeneği</span><span class="sxs-lookup"><span data-stu-id="b0b52-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="b0b52-109">**Bitmemiş planlama işlemleri** sayfasından Master planlama işini iptal et</span><span class="sxs-lookup"><span data-stu-id="b0b52-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="b0b52-110">**Master planlama > Sorgular ve raporlar > Master planlama > Bitmemiş planlama süreçleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b0b52-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="b0b52-111">İptal etmek istediğiniz planlama sürecini içeren satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="b0b52-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="b0b52-112">**İptal**'e tıklayın</span><span class="sxs-lookup"><span data-stu-id="b0b52-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="b0b52-113">Ek iptal seçenekleri</span><span class="sxs-lookup"><span data-stu-id="b0b52-113">Additional cancel options</span></span>
<span data-ttu-id="b0b52-114">Bunlar yalnızca, master planlama işi **Tamamlanmamış planlama işlemleri** sayfasından, birkaç dakika içinde tamamlanmamışsa kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b0b52-114">These should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="b0b52-115">Master planlama işini **toplu işler** sayfasından Sil</span><span class="sxs-lookup"><span data-stu-id="b0b52-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="b0b52-116">**Sistem yönetimi > Sorgular > Toplu işler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="b0b52-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="b0b52-117">Silmek istediğiniz planlama işini içeren satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="b0b52-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="b0b52-118">**Sil** öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b0b52-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="b0b52-119">Master planlama işi görevini **toplu işler gelişmiş** sayfasından iptal et</span><span class="sxs-lookup"><span data-stu-id="b0b52-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="b0b52-120">**Sistem yönetimi > Sorgular > Toplu işler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="b0b52-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="b0b52-121">İş kodu listede gösterilmezse, **Gelişmiş forma geç**'i tıklatın, aksi durumda bir sonraki adımla devam edin.</span><span class="sxs-lookup"><span data-stu-id="b0b52-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="b0b52-122">Toplu işi açın.</span><span class="sxs-lookup"><span data-stu-id="b0b52-122">Open the batch job.</span></span> <span data-ttu-id="b0b52-123">Sonlandırmak istediğiniz görevlerle ilgili toplu iş için **iş kodu** tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b0b52-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="b0b52-124">**Toplu iş görevlerinde** sona erdirmek istediğiniz görevleri seçin.</span><span class="sxs-lookup"><span data-stu-id="b0b52-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="b0b52-125">**Toplu işlem görevleri** hızlı sekmesinde, **Durdur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b0b52-125">On the **Batch tasks** FastTab, click **Abort**.</span></span>
