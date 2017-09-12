---
title: "Barkod tarayıcıları desteği için kanban transfer panosu"
description: "Kanban transfer panosunu, bir kanban işini Seçmek, Başlatmak, Tamamlamak ve Boşaltmak için bir pencere öğesi barkod tarayıcısından tarayıcı girişini destekler."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1dc40de2b77be5c5c2399fd55c3c3bd15a9f24ec
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---

# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="669be-103">Barkod tarayıcıları desteği için kanban transfer panosu</span><span class="sxs-lookup"><span data-stu-id="669be-103">Kanban transfer board support for barcode scanners</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="669be-104">Kanban transfer panosunu, bir kanban işini Seçmek, Başlatmak, Tamamlamak ve Boşaltmak için bir pencere öğesi barkod tarayıcısından tarayıcı girişini destekler.</span><span class="sxs-lookup"><span data-stu-id="669be-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="669be-105">Kayıt modları</span><span class="sxs-lookup"><span data-stu-id="669be-105">Registration modes</span></span>
------------------

<span data-ttu-id="669be-106">**Tarayıcı kaydı** FastTab sekmesinde, bir kanban kart numarasını seçtiğinizde veya manuel olarak numarayı Kanban kart numarası alanına yazdığınızda eylemi kontrol eden kayıt modunu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="669be-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>
| <span data-ttu-id="669be-107">Kayıt modu ayarla</span><span class="sxs-lookup"><span data-stu-id="669be-107">Set registration mode</span></span> | <span data-ttu-id="669be-108">Açıklama</span><span class="sxs-lookup"><span data-stu-id="669be-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="669be-109">Başlangıç</span><span class="sxs-lookup"><span data-stu-id="669be-109">Start</span></span>                 | <span data-ttu-id="669be-110">Bir Kanban transfer işini devam eden olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="669be-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="669be-111">Tam</span><span class="sxs-lookup"><span data-stu-id="669be-111">Complete</span></span>              | <span data-ttu-id="669be-112">Bir Kanban transfer işini tamamlandı olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="669be-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="669be-113">Boşalt</span><span class="sxs-lookup"><span data-stu-id="669be-113">Empty</span></span>                 | <span data-ttu-id="669be-114">Bir Kanban kartının referans verdiği malzeme işleme birimini boş olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="669be-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="669be-115">Seç</span><span class="sxs-lookup"><span data-stu-id="669be-115">Select</span></span>                | <span data-ttu-id="669be-116">Bir Kanban kart numarası kaydeder ve referans verilen işi Kanban listesinde otomatik olarak seçer.</span><span class="sxs-lookup"><span data-stu-id="669be-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="669be-117">Kayıt modu Seç</span><span class="sxs-lookup"><span data-stu-id="669be-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="669be-118">İş seçmek için barkod okuyucuyu kullandığınızda, kanban panosunun görüntüleme modu değişir.</span><span class="sxs-lookup"><span data-stu-id="669be-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="669be-119">Bu modda, aşağıdaki koşullar geçerlidir:</span><span class="sxs-lookup"><span data-stu-id="669be-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="669be-120">Yalnızca taranan kanban işi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="669be-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="669be-121">Seçilen işin ayrıntıları **Ayrıntılar** FastTab'inde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="669be-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="669be-122">**İletiler** FastTab'i, yalnızca seçilen işin iletilerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="669be-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="669be-123">İşin durumunu, Eylem Bölmesi'nde bulunan işlevleri kullanarak değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="669be-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="669be-124">Kanban transfer panosu, bu süre boyunca yalnızca tek bir işi görüntülemeye devam eder.</span><span class="sxs-lookup"><span data-stu-id="669be-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="669be-125">İşler listesindeki bilgileri Eylem Bölmesi'ndeki **Yenile** (Shift+F5) seçeneğini tıklayarak el ile güncelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="669be-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="669be-126">Bilgileri güncelledikten sonra, iş filtresi için tüm sonuçlar yeniden görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="669be-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="669be-127">İş durumu ve olası eylemler</span><span class="sxs-lookup"><span data-stu-id="669be-127">Job status and possible actions</span></span>
<span data-ttu-id="669be-128">İşi daha fazla işleyip işleyemeyeceğinizi, seçilen işin durumu ve etkinlik kanban'ları için ilişkilendirilmiş işlerin durumu belirler.</span><span class="sxs-lookup"><span data-stu-id="669be-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="669be-129">Aşağıdaki tabloda bu durum ve görevler hakkındaki bilgiler görüntülenmektedir:</span><span class="sxs-lookup"><span data-stu-id="669be-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="669be-130">İşler için kullanılabilir durumdaki veya işlerin referans verdiği işleme birimlerine yönelik durumlar.</span><span class="sxs-lookup"><span data-stu-id="669be-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="669be-131">İş için gerçekleştirebileceğiniz her bir görev.</span><span class="sxs-lookup"><span data-stu-id="669be-131">Each task that you can perform for the job.</span></span>

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
<th><span data-ttu-id="669be-132">İş türü</span><span class="sxs-lookup"><span data-stu-id="669be-132">Job type</span></span></th>
<th><span data-ttu-id="669be-133">İş durumu veya işleme birimi durumu</span><span class="sxs-lookup"><span data-stu-id="669be-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="669be-134">Malzeme çekme listesini güncelleştir</span><span class="sxs-lookup"><span data-stu-id="669be-134">Update picking list</span></span></th>
<th><span data-ttu-id="669be-135">Başlangıç</span><span class="sxs-lookup"><span data-stu-id="669be-135">Start</span></span></th>
<th><span data-ttu-id="669be-136">Kaydı güncelleştir</span><span class="sxs-lookup"><span data-stu-id="669be-136">Update registration</span></span></th>
<th><span data-ttu-id="669be-137">Tam</span><span class="sxs-lookup"><span data-stu-id="669be-137">Complete</span></span></th>
<th><span data-ttu-id="669be-138">Boşalt</span><span class="sxs-lookup"><span data-stu-id="669be-138">Empty</span></span></th>
<th><span data-ttu-id="669be-139">Olay kanbanları oluştur</span><span class="sxs-lookup"><span data-stu-id="669be-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="669be-140">Transfer et</span><span class="sxs-lookup"><span data-stu-id="669be-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="669be-141">Planlanmadı</span><span class="sxs-lookup"><span data-stu-id="669be-141">Not planned</span></span></li>
<li><span data-ttu-id="669be-142">İlişkilendirilmiş iş yok veya ilişkilendirilmiş işler Tamamlanmış</span><span class="sxs-lookup"><span data-stu-id="669be-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="669be-143">Evet</span><span class="sxs-lookup"><span data-stu-id="669be-143">Yes</span></span></td>
<td><span data-ttu-id="669be-144">Evet</span><span class="sxs-lookup"><span data-stu-id="669be-144">Yes</span></span></td>
<td><span data-ttu-id="669be-145">Evet</span><span class="sxs-lookup"><span data-stu-id="669be-145">Yes</span></span></td>
<td><span data-ttu-id="669be-146">Evet</span><span class="sxs-lookup"><span data-stu-id="669be-146">Yes</span></span></td>
<td><span data-ttu-id="669be-147">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-147">No</span></span></td>
<td><span data-ttu-id="669be-148">Evet</span><span class="sxs-lookup"><span data-stu-id="669be-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="669be-149">Transfer et</span><span class="sxs-lookup"><span data-stu-id="669be-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="669be-150">Planlanmadı</span><span class="sxs-lookup"><span data-stu-id="669be-150">Not planned</span></span></li>
<li><span data-ttu-id="669be-151">İlişkilendirilmiş iş Tamamlanmamış</span><span class="sxs-lookup"><span data-stu-id="669be-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="669be-152">Evet</span><span class="sxs-lookup"><span data-stu-id="669be-152">Yes</span></span></td>
<td><span data-ttu-id="669be-153">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-153">No</span></span></td>
<td><span data-ttu-id="669be-154">Evet</span><span class="sxs-lookup"><span data-stu-id="669be-154">Yes</span></span></td>
<td><span data-ttu-id="669be-155">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-155">No</span></span></td>
<td><span data-ttu-id="669be-156">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-156">No</span></span></td>
<td><span data-ttu-id="669be-157">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="669be-158">Transfer et</span><span class="sxs-lookup"><span data-stu-id="669be-158">Transfer</span></span></td>
<td><span data-ttu-id="669be-159">Devam ediyor</span><span class="sxs-lookup"><span data-stu-id="669be-159">In progress</span></span></td>
<td><span data-ttu-id="669be-160">Evet</span><span class="sxs-lookup"><span data-stu-id="669be-160">Yes</span></span></td>
<td><span data-ttu-id="669be-161">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-161">No</span></span></td>
<td><span data-ttu-id="669be-162">Evet</span><span class="sxs-lookup"><span data-stu-id="669be-162">Yes</span></span></td>
<td><span data-ttu-id="669be-163">Evet</span><span class="sxs-lookup"><span data-stu-id="669be-163">Yes</span></span></td>
<td><span data-ttu-id="669be-164">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-164">No</span></span></td>
<td><span data-ttu-id="669be-165">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="669be-166">Transfer et</span><span class="sxs-lookup"><span data-stu-id="669be-166">Transfer</span></span></td>
<td><span data-ttu-id="669be-167">Tamamlandı</span><span class="sxs-lookup"><span data-stu-id="669be-167">Completed</span></span></td>
<td><span data-ttu-id="669be-168">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-168">No</span></span></td>
<td><span data-ttu-id="669be-169">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-169">No</span></span></td>
<td><span data-ttu-id="669be-170">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-170">No</span></span></td>
<td><span data-ttu-id="669be-171">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-171">No</span></span></td>
<td><span data-ttu-id="669be-172">Evet</span><span class="sxs-lookup"><span data-stu-id="669be-172">Yes</span></span></td>
<td><span data-ttu-id="669be-173">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="669be-174">Transfer et veya işle</span><span class="sxs-lookup"><span data-stu-id="669be-174">Transfer or process</span></span></td>
<td><span data-ttu-id="669be-175">Boşalt</span><span class="sxs-lookup"><span data-stu-id="669be-175">Empty</span></span></td>
<td><span data-ttu-id="669be-176">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-176">No</span></span></td>
<td><span data-ttu-id="669be-177">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-177">No</span></span></td>
<td><span data-ttu-id="669be-178">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-178">No</span></span></td>
<td><span data-ttu-id="669be-179">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-179">No</span></span></td>
<td><span data-ttu-id="669be-180">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-180">No</span></span></td>
<td><span data-ttu-id="669be-181">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="669be-182">Transfer et veya işle</span><span class="sxs-lookup"><span data-stu-id="669be-182">Transfer or process</span></span></td>
<td><span data-ttu-id="669be-183">Kanban kartı bulunamadı</span><span class="sxs-lookup"><span data-stu-id="669be-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="669be-184">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-184">No</span></span></td>
<td><span data-ttu-id="669be-185">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-185">No</span></span></td>
<td><span data-ttu-id="669be-186">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-186">No</span></span></td>
<td><span data-ttu-id="669be-187">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-187">No</span></span></td>
<td><span data-ttu-id="669be-188">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-188">No</span></span></td>
<td><span data-ttu-id="669be-189">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="669be-190">Transfer et veya işle</span><span class="sxs-lookup"><span data-stu-id="669be-190">Transfer or process</span></span></td>
<td><span data-ttu-id="669be-191">Kanban kartı bulundu, ancak bir kanbana atanmamış</span><span class="sxs-lookup"><span data-stu-id="669be-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="669be-192">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-192">No</span></span></td>
<td><span data-ttu-id="669be-193">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-193">No</span></span></td>
<td><span data-ttu-id="669be-194">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-194">No</span></span></td>
<td><span data-ttu-id="669be-195">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-195">No</span></span></td>
<td><span data-ttu-id="669be-196">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-196">No</span></span></td>
<td><span data-ttu-id="669be-197">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="669be-198">İşle</span><span class="sxs-lookup"><span data-stu-id="669be-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="669be-199">Planlanmadı</span><span class="sxs-lookup"><span data-stu-id="669be-199">Not planned</span></span></li>
<li><span data-ttu-id="669be-200">Hazırlandı</span><span class="sxs-lookup"><span data-stu-id="669be-200">Prepared</span></span></li>
<li><span data-ttu-id="669be-201">Devam ediyor</span><span class="sxs-lookup"><span data-stu-id="669be-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="669be-202">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-202">No</span></span></td>
<td><span data-ttu-id="669be-203">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-203">No</span></span></td>
<td><span data-ttu-id="669be-204">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-204">No</span></span></td>
<td><span data-ttu-id="669be-205">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-205">No</span></span></td>
<td><span data-ttu-id="669be-206">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-206">No</span></span></td>
<td><span data-ttu-id="669be-207">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="669be-208">İşle</span><span class="sxs-lookup"><span data-stu-id="669be-208">Process</span></span></td>
<td><span data-ttu-id="669be-209">Tamamlandı</span><span class="sxs-lookup"><span data-stu-id="669be-209">Completed</span></span></td>
<td><span data-ttu-id="669be-210">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-210">No</span></span></td>
<td><span data-ttu-id="669be-211">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-211">No</span></span></td>
<td><span data-ttu-id="669be-212">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-212">No</span></span></td>
<td><span data-ttu-id="669be-213">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-213">No</span></span></td>
<td><span data-ttu-id="669be-214">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-214">No</span></span></td>
<td><span data-ttu-id="669be-215">Hayır</span><span class="sxs-lookup"><span data-stu-id="669be-215">No</span></span></td>
</tr>
</tbody>
</table>






