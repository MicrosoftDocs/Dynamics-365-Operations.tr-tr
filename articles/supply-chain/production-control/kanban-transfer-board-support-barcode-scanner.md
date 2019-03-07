---
title: Barkod tarayıcıları desteği için kanban transfer panosu
description: Kanban transfer panosunu, bir kanban işini Seçmek, Başlatmak, Tamamlamak ve Boşaltmak için bir pencere öğesi barkod tarayıcısından tarayıcı girişini destekler.
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e63a33af63144b78d0c375022b9802e11c255598
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "319466"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="34e7e-103">Barkod tarayıcıları desteği için kanban transfer panosu</span><span class="sxs-lookup"><span data-stu-id="34e7e-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34e7e-104">Kanban transfer panosunu, bir kanban işini Seçmek, Başlatmak, Tamamlamak ve Boşaltmak için bir pencere öğesi barkod tarayıcısından tarayıcı girişini destekler.</span><span class="sxs-lookup"><span data-stu-id="34e7e-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="34e7e-105">Kayıt modları</span><span class="sxs-lookup"><span data-stu-id="34e7e-105">Registration modes</span></span>
------------------

<span data-ttu-id="34e7e-106">**Tarayıcı kaydı** FastTab sekmesinde, bir kanban kart numarasını seçtiğinizde veya manuel olarak numarayı Kanban kart numarası alanına yazdığınızda eylemi kontrol eden kayıt modunu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34e7e-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="34e7e-107">Kayıt modu ayarla</span><span class="sxs-lookup"><span data-stu-id="34e7e-107">Set registration mode</span></span> | <span data-ttu-id="34e7e-108">Açıklama</span><span class="sxs-lookup"><span data-stu-id="34e7e-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e7e-109">Başlangıç</span><span class="sxs-lookup"><span data-stu-id="34e7e-109">Start</span></span>                 | <span data-ttu-id="34e7e-110">Bir Kanban transfer işini devam eden olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="34e7e-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="34e7e-111">Tam</span><span class="sxs-lookup"><span data-stu-id="34e7e-111">Complete</span></span>              | <span data-ttu-id="34e7e-112">Bir Kanban transfer işini tamamlandı olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="34e7e-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="34e7e-113">Boşalt</span><span class="sxs-lookup"><span data-stu-id="34e7e-113">Empty</span></span>                 | <span data-ttu-id="34e7e-114">Bir Kanban kartının referans verdiği malzeme işleme birimini boş olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="34e7e-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="34e7e-115">Seç</span><span class="sxs-lookup"><span data-stu-id="34e7e-115">Select</span></span>                | <span data-ttu-id="34e7e-116">Bir Kanban kart numarası kaydeder ve referans verilen işi Kanban listesinde otomatik olarak seçer.</span><span class="sxs-lookup"><span data-stu-id="34e7e-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<span data-ttu-id="34e7e-117">Kayıt modu Seç</span><span class="sxs-lookup"><span data-stu-id="34e7e-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="34e7e-118">İş seçmek için barkod okuyucuyu kullandığınızda, kanban panosunun görüntüleme modu değişir.</span><span class="sxs-lookup"><span data-stu-id="34e7e-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span><span data-ttu-id="34e7e-119"> Bu modda, aşağıdaki koşullar geçerlidir:</span><span class="sxs-lookup"><span data-stu-id="34e7e-119"> In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="34e7e-120">Yalnızca taranan kanban işi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="34e7e-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="34e7e-121">Seçilen işin ayrıntıları **Ayrıntılar** FastTab'inde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="34e7e-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="34e7e-122">**İletiler** FastTab'i, yalnızca seçilen işin iletilerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="34e7e-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="34e7e-123">İşin durumunu, Eylem Bölmesi'nde bulunan işlevleri kullanarak değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34e7e-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="34e7e-124">Kanban transfer panosu, bu süre boyunca yalnızca tek bir işi görüntülemeye devam eder.</span><span class="sxs-lookup"><span data-stu-id="34e7e-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="34e7e-125">İşler listesindeki bilgileri Eylem Bölmesi'ndeki **Yenile** (Shift+F5) seçeneğini tıklayarak el ile güncelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34e7e-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="34e7e-126">Bilgileri güncelledikten sonra, iş filtresi için tüm sonuçlar yeniden görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="34e7e-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="34e7e-127">İş durumu ve olası eylemler</span><span class="sxs-lookup"><span data-stu-id="34e7e-127">Job status and possible actions</span></span>
<span data-ttu-id="34e7e-128">İşi daha fazla işleyip işleyemeyeceğinizi, seçilen işin durumu ve etkinlik kanban'ları için ilişkilendirilmiş işlerin durumu belirler.</span><span class="sxs-lookup"><span data-stu-id="34e7e-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="34e7e-129">Aşağıdaki tabloda bu durum ve görevler hakkındaki bilgiler görüntülenmektedir:</span><span class="sxs-lookup"><span data-stu-id="34e7e-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="34e7e-130">İşler için kullanılabilir durumdaki veya işlerin referans verdiği işleme birimlerine yönelik durumlar.</span><span class="sxs-lookup"><span data-stu-id="34e7e-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="34e7e-131">İş için gerçekleştirebileceğiniz her bir görev.</span><span class="sxs-lookup"><span data-stu-id="34e7e-131">Each task that you can perform for the job.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34e7e-132">İş türü</span><span class="sxs-lookup"><span data-stu-id="34e7e-132">Job type</span></span></th>
<th><span data-ttu-id="34e7e-133">İş durumu veya işleme birimi durumu</span><span class="sxs-lookup"><span data-stu-id="34e7e-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="34e7e-134">Malzeme çekme listesini güncelleştir</span><span class="sxs-lookup"><span data-stu-id="34e7e-134">Update picking list</span></span></th>
<th><span data-ttu-id="34e7e-135">Başlangıç</span><span class="sxs-lookup"><span data-stu-id="34e7e-135">Start</span></span></th>
<th><span data-ttu-id="34e7e-136">Kaydı güncelleştir</span><span class="sxs-lookup"><span data-stu-id="34e7e-136">Update registration</span></span></th>
<th><span data-ttu-id="34e7e-137">Tam</span><span class="sxs-lookup"><span data-stu-id="34e7e-137">Complete</span></span></th>
<th><span data-ttu-id="34e7e-138">Boşalt</span><span class="sxs-lookup"><span data-stu-id="34e7e-138">Empty</span></span></th>
<th><span data-ttu-id="34e7e-139">Olay kanbanları oluştur</span><span class="sxs-lookup"><span data-stu-id="34e7e-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34e7e-140">Transfer et</span><span class="sxs-lookup"><span data-stu-id="34e7e-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="34e7e-141">Planlanmadı</span><span class="sxs-lookup"><span data-stu-id="34e7e-141">Not planned</span></span></li>
<li><span data-ttu-id="34e7e-142">İlişkilendirilmiş iş yok veya ilişkilendirilmiş işler Tamamlanmış</span><span class="sxs-lookup"><span data-stu-id="34e7e-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="34e7e-143">Evet</span><span class="sxs-lookup"><span data-stu-id="34e7e-143">Yes</span></span></td>
<td><span data-ttu-id="34e7e-144">Evet</span><span class="sxs-lookup"><span data-stu-id="34e7e-144">Yes</span></span></td>
<td><span data-ttu-id="34e7e-145">Evet</span><span class="sxs-lookup"><span data-stu-id="34e7e-145">Yes</span></span></td>
<td><span data-ttu-id="34e7e-146">Evet</span><span class="sxs-lookup"><span data-stu-id="34e7e-146">Yes</span></span></td>
<td><span data-ttu-id="34e7e-147">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-147">No</span></span></td>
<td><span data-ttu-id="34e7e-148">Evet</span><span class="sxs-lookup"><span data-stu-id="34e7e-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e7e-149">Transfer et</span><span class="sxs-lookup"><span data-stu-id="34e7e-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="34e7e-150">Planlanmadı</span><span class="sxs-lookup"><span data-stu-id="34e7e-150">Not planned</span></span></li>
<li><span data-ttu-id="34e7e-151">İlişkilendirilmiş iş Tamamlanmamış</span><span class="sxs-lookup"><span data-stu-id="34e7e-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="34e7e-152">Evet</span><span class="sxs-lookup"><span data-stu-id="34e7e-152">Yes</span></span></td>
<td><span data-ttu-id="34e7e-153">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-153">No</span></span></td>
<td><span data-ttu-id="34e7e-154">Evet</span><span class="sxs-lookup"><span data-stu-id="34e7e-154">Yes</span></span></td>
<td><span data-ttu-id="34e7e-155">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-155">No</span></span></td>
<td><span data-ttu-id="34e7e-156">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-156">No</span></span></td>
<td><span data-ttu-id="34e7e-157">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34e7e-158">Transfer et</span><span class="sxs-lookup"><span data-stu-id="34e7e-158">Transfer</span></span></td>
<td><span data-ttu-id="34e7e-159">Devam ediyor</span><span class="sxs-lookup"><span data-stu-id="34e7e-159">In progress</span></span></td>
<td><span data-ttu-id="34e7e-160">Evet</span><span class="sxs-lookup"><span data-stu-id="34e7e-160">Yes</span></span></td>
<td><span data-ttu-id="34e7e-161">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-161">No</span></span></td>
<td><span data-ttu-id="34e7e-162">Evet</span><span class="sxs-lookup"><span data-stu-id="34e7e-162">Yes</span></span></td>
<td><span data-ttu-id="34e7e-163">Evet</span><span class="sxs-lookup"><span data-stu-id="34e7e-163">Yes</span></span></td>
<td><span data-ttu-id="34e7e-164">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-164">No</span></span></td>
<td><span data-ttu-id="34e7e-165">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e7e-166">Transfer et</span><span class="sxs-lookup"><span data-stu-id="34e7e-166">Transfer</span></span></td>
<td><span data-ttu-id="34e7e-167">Tamamlandı</span><span class="sxs-lookup"><span data-stu-id="34e7e-167">Completed</span></span></td>
<td><span data-ttu-id="34e7e-168">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-168">No</span></span></td>
<td><span data-ttu-id="34e7e-169">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-169">No</span></span></td>
<td><span data-ttu-id="34e7e-170">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-170">No</span></span></td>
<td><span data-ttu-id="34e7e-171">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-171">No</span></span></td>
<td><span data-ttu-id="34e7e-172">Evet</span><span class="sxs-lookup"><span data-stu-id="34e7e-172">Yes</span></span></td>
<td><span data-ttu-id="34e7e-173">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34e7e-174">Transfer et veya işle</span><span class="sxs-lookup"><span data-stu-id="34e7e-174">Transfer or process</span></span></td>
<td><span data-ttu-id="34e7e-175">Boşalt</span><span class="sxs-lookup"><span data-stu-id="34e7e-175">Empty</span></span></td>
<td><span data-ttu-id="34e7e-176">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-176">No</span></span></td>
<td><span data-ttu-id="34e7e-177">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-177">No</span></span></td>
<td><span data-ttu-id="34e7e-178">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-178">No</span></span></td>
<td><span data-ttu-id="34e7e-179">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-179">No</span></span></td>
<td><span data-ttu-id="34e7e-180">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-180">No</span></span></td>
<td><span data-ttu-id="34e7e-181">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e7e-182">Transfer et veya işle</span><span class="sxs-lookup"><span data-stu-id="34e7e-182">Transfer or process</span></span></td>
<td><span data-ttu-id="34e7e-183">Kanban kartı bulunamadı</span><span class="sxs-lookup"><span data-stu-id="34e7e-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="34e7e-184">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-184">No</span></span></td>
<td><span data-ttu-id="34e7e-185">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-185">No</span></span></td>
<td><span data-ttu-id="34e7e-186">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-186">No</span></span></td>
<td><span data-ttu-id="34e7e-187">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-187">No</span></span></td>
<td><span data-ttu-id="34e7e-188">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-188">No</span></span></td>
<td><span data-ttu-id="34e7e-189">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34e7e-190">Transfer et veya işle</span><span class="sxs-lookup"><span data-stu-id="34e7e-190">Transfer or process</span></span></td>
<td><span data-ttu-id="34e7e-191">Kanban kartı bulundu, ancak bir kanbana atanmamış</span><span class="sxs-lookup"><span data-stu-id="34e7e-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="34e7e-192">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-192">No</span></span></td>
<td><span data-ttu-id="34e7e-193">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-193">No</span></span></td>
<td><span data-ttu-id="34e7e-194">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-194">No</span></span></td>
<td><span data-ttu-id="34e7e-195">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-195">No</span></span></td>
<td><span data-ttu-id="34e7e-196">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-196">No</span></span></td>
<td><span data-ttu-id="34e7e-197">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e7e-198">İşle</span><span class="sxs-lookup"><span data-stu-id="34e7e-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="34e7e-199">Planlanmadı</span><span class="sxs-lookup"><span data-stu-id="34e7e-199">Not planned</span></span></li>
<li><span data-ttu-id="34e7e-200">Hazırlandı</span><span class="sxs-lookup"><span data-stu-id="34e7e-200">Prepared</span></span></li>
<li><span data-ttu-id="34e7e-201">Devam ediyor</span><span class="sxs-lookup"><span data-stu-id="34e7e-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="34e7e-202">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-202">No</span></span></td>
<td><span data-ttu-id="34e7e-203">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-203">No</span></span></td>
<td><span data-ttu-id="34e7e-204">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-204">No</span></span></td>
<td><span data-ttu-id="34e7e-205">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-205">No</span></span></td>
<td><span data-ttu-id="34e7e-206">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-206">No</span></span></td>
<td><span data-ttu-id="34e7e-207">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34e7e-208">İşle</span><span class="sxs-lookup"><span data-stu-id="34e7e-208">Process</span></span></td>
<td><span data-ttu-id="34e7e-209">Tamamlandı</span><span class="sxs-lookup"><span data-stu-id="34e7e-209">Completed</span></span></td>
<td><span data-ttu-id="34e7e-210">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-210">No</span></span></td>
<td><span data-ttu-id="34e7e-211">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-211">No</span></span></td>
<td><span data-ttu-id="34e7e-212">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-212">No</span></span></td>
<td><span data-ttu-id="34e7e-213">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-213">No</span></span></td>
<td><span data-ttu-id="34e7e-214">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-214">No</span></span></td>
<td><span data-ttu-id="34e7e-215">Hayır</span><span class="sxs-lookup"><span data-stu-id="34e7e-215">No</span></span></td>
</tr>
</tbody>
</table>





