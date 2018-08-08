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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e63a33af63144b78d0c375022b9802e11c255598
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---

# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="35b7a-103">Barkod tarayıcıları desteği için kanban transfer panosu</span><span class="sxs-lookup"><span data-stu-id="35b7a-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35b7a-104">Kanban transfer panosunu, bir kanban işini Seçmek, Başlatmak, Tamamlamak ve Boşaltmak için bir pencere öğesi barkod tarayıcısından tarayıcı girişini destekler.</span><span class="sxs-lookup"><span data-stu-id="35b7a-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="35b7a-105">Kayıt modları</span><span class="sxs-lookup"><span data-stu-id="35b7a-105">Registration modes</span></span>
------------------

<span data-ttu-id="35b7a-106">**Tarayıcı kaydı** FastTab sekmesinde, bir kanban kart numarasını seçtiğinizde veya manuel olarak numarayı Kanban kart numarası alanına yazdığınızda eylemi kontrol eden kayıt modunu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="35b7a-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="35b7a-107">Kayıt modu ayarla</span><span class="sxs-lookup"><span data-stu-id="35b7a-107">Set registration mode</span></span> | <span data-ttu-id="35b7a-108">Açıklama</span><span class="sxs-lookup"><span data-stu-id="35b7a-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35b7a-109">Başlangıç</span><span class="sxs-lookup"><span data-stu-id="35b7a-109">Start</span></span>                 | <span data-ttu-id="35b7a-110">Bir Kanban transfer işini devam eden olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="35b7a-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="35b7a-111">Tam</span><span class="sxs-lookup"><span data-stu-id="35b7a-111">Complete</span></span>              | <span data-ttu-id="35b7a-112">Bir Kanban transfer işini tamamlandı olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="35b7a-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="35b7a-113">Boşalt</span><span class="sxs-lookup"><span data-stu-id="35b7a-113">Empty</span></span>                 | <span data-ttu-id="35b7a-114">Bir Kanban kartının referans verdiği malzeme işleme birimini boş olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="35b7a-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="35b7a-115">Seç</span><span class="sxs-lookup"><span data-stu-id="35b7a-115">Select</span></span>                | <span data-ttu-id="35b7a-116">Bir Kanban kart numarası kaydeder ve referans verilen işi Kanban listesinde otomatik olarak seçer.</span><span class="sxs-lookup"><span data-stu-id="35b7a-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="35b7a-117">Kayıt modu Seç</span><span class="sxs-lookup"><span data-stu-id="35b7a-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="35b7a-118">İş seçmek için barkod okuyucuyu kullandığınızda, kanban panosunun görüntüleme modu değişir.</span><span class="sxs-lookup"><span data-stu-id="35b7a-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="35b7a-119">Bu modda, aşağıdaki koşullar geçerlidir:</span><span class="sxs-lookup"><span data-stu-id="35b7a-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="35b7a-120">Yalnızca taranan kanban işi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="35b7a-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="35b7a-121">Seçilen işin ayrıntıları **Ayrıntılar** FastTab'inde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="35b7a-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="35b7a-122">**İletiler** FastTab'i, yalnızca seçilen işin iletilerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="35b7a-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="35b7a-123">İşin durumunu, Eylem Bölmesi'nde bulunan işlevleri kullanarak değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="35b7a-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="35b7a-124">Kanban transfer panosu, bu süre boyunca yalnızca tek bir işi görüntülemeye devam eder.</span><span class="sxs-lookup"><span data-stu-id="35b7a-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="35b7a-125">İşler listesindeki bilgileri Eylem Bölmesi'ndeki **Yenile** (Shift+F5) seçeneğini tıklayarak el ile güncelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="35b7a-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="35b7a-126">Bilgileri güncelledikten sonra, iş filtresi için tüm sonuçlar yeniden görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="35b7a-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="35b7a-127">İş durumu ve olası eylemler</span><span class="sxs-lookup"><span data-stu-id="35b7a-127">Job status and possible actions</span></span>
<span data-ttu-id="35b7a-128">İşi daha fazla işleyip işleyemeyeceğinizi, seçilen işin durumu ve etkinlik kanban'ları için ilişkilendirilmiş işlerin durumu belirler.</span><span class="sxs-lookup"><span data-stu-id="35b7a-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="35b7a-129">Aşağıdaki tabloda bu durum ve görevler hakkındaki bilgiler görüntülenmektedir:</span><span class="sxs-lookup"><span data-stu-id="35b7a-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="35b7a-130">İşler için kullanılabilir durumdaki veya işlerin referans verdiği işleme birimlerine yönelik durumlar.</span><span class="sxs-lookup"><span data-stu-id="35b7a-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="35b7a-131">İş için gerçekleştirebileceğiniz her bir görev.</span><span class="sxs-lookup"><span data-stu-id="35b7a-131">Each task that you can perform for the job.</span></span>

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
<th><span data-ttu-id="35b7a-132">İş türü</span><span class="sxs-lookup"><span data-stu-id="35b7a-132">Job type</span></span></th>
<th><span data-ttu-id="35b7a-133">İş durumu veya işleme birimi durumu</span><span class="sxs-lookup"><span data-stu-id="35b7a-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="35b7a-134">Malzeme çekme listesini güncelleştir</span><span class="sxs-lookup"><span data-stu-id="35b7a-134">Update picking list</span></span></th>
<th><span data-ttu-id="35b7a-135">Başlangıç</span><span class="sxs-lookup"><span data-stu-id="35b7a-135">Start</span></span></th>
<th><span data-ttu-id="35b7a-136">Kaydı güncelleştir</span><span class="sxs-lookup"><span data-stu-id="35b7a-136">Update registration</span></span></th>
<th><span data-ttu-id="35b7a-137">Tam</span><span class="sxs-lookup"><span data-stu-id="35b7a-137">Complete</span></span></th>
<th><span data-ttu-id="35b7a-138">Boşalt</span><span class="sxs-lookup"><span data-stu-id="35b7a-138">Empty</span></span></th>
<th><span data-ttu-id="35b7a-139">Olay kanbanları oluştur</span><span class="sxs-lookup"><span data-stu-id="35b7a-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35b7a-140">Transfer et</span><span class="sxs-lookup"><span data-stu-id="35b7a-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="35b7a-141">Planlanmadı</span><span class="sxs-lookup"><span data-stu-id="35b7a-141">Not planned</span></span></li>
<li><span data-ttu-id="35b7a-142">İlişkilendirilmiş iş yok veya ilişkilendirilmiş işler Tamamlanmış</span><span class="sxs-lookup"><span data-stu-id="35b7a-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="35b7a-143">Evet</span><span class="sxs-lookup"><span data-stu-id="35b7a-143">Yes</span></span></td>
<td><span data-ttu-id="35b7a-144">Evet</span><span class="sxs-lookup"><span data-stu-id="35b7a-144">Yes</span></span></td>
<td><span data-ttu-id="35b7a-145">Evet</span><span class="sxs-lookup"><span data-stu-id="35b7a-145">Yes</span></span></td>
<td><span data-ttu-id="35b7a-146">Evet</span><span class="sxs-lookup"><span data-stu-id="35b7a-146">Yes</span></span></td>
<td><span data-ttu-id="35b7a-147">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-147">No</span></span></td>
<td><span data-ttu-id="35b7a-148">Evet</span><span class="sxs-lookup"><span data-stu-id="35b7a-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35b7a-149">Transfer et</span><span class="sxs-lookup"><span data-stu-id="35b7a-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="35b7a-150">Planlanmadı</span><span class="sxs-lookup"><span data-stu-id="35b7a-150">Not planned</span></span></li>
<li><span data-ttu-id="35b7a-151">İlişkilendirilmiş iş Tamamlanmamış</span><span class="sxs-lookup"><span data-stu-id="35b7a-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="35b7a-152">Evet</span><span class="sxs-lookup"><span data-stu-id="35b7a-152">Yes</span></span></td>
<td><span data-ttu-id="35b7a-153">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-153">No</span></span></td>
<td><span data-ttu-id="35b7a-154">Evet</span><span class="sxs-lookup"><span data-stu-id="35b7a-154">Yes</span></span></td>
<td><span data-ttu-id="35b7a-155">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-155">No</span></span></td>
<td><span data-ttu-id="35b7a-156">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-156">No</span></span></td>
<td><span data-ttu-id="35b7a-157">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35b7a-158">Transfer et</span><span class="sxs-lookup"><span data-stu-id="35b7a-158">Transfer</span></span></td>
<td><span data-ttu-id="35b7a-159">Devam ediyor</span><span class="sxs-lookup"><span data-stu-id="35b7a-159">In progress</span></span></td>
<td><span data-ttu-id="35b7a-160">Evet</span><span class="sxs-lookup"><span data-stu-id="35b7a-160">Yes</span></span></td>
<td><span data-ttu-id="35b7a-161">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-161">No</span></span></td>
<td><span data-ttu-id="35b7a-162">Evet</span><span class="sxs-lookup"><span data-stu-id="35b7a-162">Yes</span></span></td>
<td><span data-ttu-id="35b7a-163">Evet</span><span class="sxs-lookup"><span data-stu-id="35b7a-163">Yes</span></span></td>
<td><span data-ttu-id="35b7a-164">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-164">No</span></span></td>
<td><span data-ttu-id="35b7a-165">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35b7a-166">Transfer et</span><span class="sxs-lookup"><span data-stu-id="35b7a-166">Transfer</span></span></td>
<td><span data-ttu-id="35b7a-167">Tamamlandı</span><span class="sxs-lookup"><span data-stu-id="35b7a-167">Completed</span></span></td>
<td><span data-ttu-id="35b7a-168">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-168">No</span></span></td>
<td><span data-ttu-id="35b7a-169">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-169">No</span></span></td>
<td><span data-ttu-id="35b7a-170">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-170">No</span></span></td>
<td><span data-ttu-id="35b7a-171">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-171">No</span></span></td>
<td><span data-ttu-id="35b7a-172">Evet</span><span class="sxs-lookup"><span data-stu-id="35b7a-172">Yes</span></span></td>
<td><span data-ttu-id="35b7a-173">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35b7a-174">Transfer et veya işle</span><span class="sxs-lookup"><span data-stu-id="35b7a-174">Transfer or process</span></span></td>
<td><span data-ttu-id="35b7a-175">Boşalt</span><span class="sxs-lookup"><span data-stu-id="35b7a-175">Empty</span></span></td>
<td><span data-ttu-id="35b7a-176">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-176">No</span></span></td>
<td><span data-ttu-id="35b7a-177">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-177">No</span></span></td>
<td><span data-ttu-id="35b7a-178">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-178">No</span></span></td>
<td><span data-ttu-id="35b7a-179">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-179">No</span></span></td>
<td><span data-ttu-id="35b7a-180">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-180">No</span></span></td>
<td><span data-ttu-id="35b7a-181">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35b7a-182">Transfer et veya işle</span><span class="sxs-lookup"><span data-stu-id="35b7a-182">Transfer or process</span></span></td>
<td><span data-ttu-id="35b7a-183">Kanban kartı bulunamadı</span><span class="sxs-lookup"><span data-stu-id="35b7a-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="35b7a-184">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-184">No</span></span></td>
<td><span data-ttu-id="35b7a-185">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-185">No</span></span></td>
<td><span data-ttu-id="35b7a-186">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-186">No</span></span></td>
<td><span data-ttu-id="35b7a-187">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-187">No</span></span></td>
<td><span data-ttu-id="35b7a-188">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-188">No</span></span></td>
<td><span data-ttu-id="35b7a-189">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35b7a-190">Transfer et veya işle</span><span class="sxs-lookup"><span data-stu-id="35b7a-190">Transfer or process</span></span></td>
<td><span data-ttu-id="35b7a-191">Kanban kartı bulundu, ancak bir kanbana atanmamış</span><span class="sxs-lookup"><span data-stu-id="35b7a-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="35b7a-192">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-192">No</span></span></td>
<td><span data-ttu-id="35b7a-193">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-193">No</span></span></td>
<td><span data-ttu-id="35b7a-194">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-194">No</span></span></td>
<td><span data-ttu-id="35b7a-195">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-195">No</span></span></td>
<td><span data-ttu-id="35b7a-196">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-196">No</span></span></td>
<td><span data-ttu-id="35b7a-197">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35b7a-198">İşle</span><span class="sxs-lookup"><span data-stu-id="35b7a-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="35b7a-199">Planlanmadı</span><span class="sxs-lookup"><span data-stu-id="35b7a-199">Not planned</span></span></li>
<li><span data-ttu-id="35b7a-200">Hazırlandı</span><span class="sxs-lookup"><span data-stu-id="35b7a-200">Prepared</span></span></li>
<li><span data-ttu-id="35b7a-201">Devam ediyor</span><span class="sxs-lookup"><span data-stu-id="35b7a-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="35b7a-202">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-202">No</span></span></td>
<td><span data-ttu-id="35b7a-203">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-203">No</span></span></td>
<td><span data-ttu-id="35b7a-204">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-204">No</span></span></td>
<td><span data-ttu-id="35b7a-205">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-205">No</span></span></td>
<td><span data-ttu-id="35b7a-206">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-206">No</span></span></td>
<td><span data-ttu-id="35b7a-207">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35b7a-208">İşle</span><span class="sxs-lookup"><span data-stu-id="35b7a-208">Process</span></span></td>
<td><span data-ttu-id="35b7a-209">Tamamlandı</span><span class="sxs-lookup"><span data-stu-id="35b7a-209">Completed</span></span></td>
<td><span data-ttu-id="35b7a-210">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-210">No</span></span></td>
<td><span data-ttu-id="35b7a-211">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-211">No</span></span></td>
<td><span data-ttu-id="35b7a-212">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-212">No</span></span></td>
<td><span data-ttu-id="35b7a-213">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-213">No</span></span></td>
<td><span data-ttu-id="35b7a-214">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-214">No</span></span></td>
<td><span data-ttu-id="35b7a-215">Hayır</span><span class="sxs-lookup"><span data-stu-id="35b7a-215">No</span></span></td>
</tr>
</tbody>
</table>






