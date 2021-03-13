---
title: Barkod tarayıcıları desteği için kanban transfer panosu
description: Kanban transfer panosunu, bir kanban işini Seçmek, Başlatmak, Tamamlamak ve Boşaltmak için bir pencere öğesi barkod tarayıcısından tarayıcı girişini destekler.
author: ChristianRytt
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aedfe7ef96d62401b1d0de0f2cd035036c68e51a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007078"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="fdbda-103">Barkod tarayıcıları desteği için kanban transfer panosu</span><span class="sxs-lookup"><span data-stu-id="fdbda-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fdbda-104">Kanban transfer panosunu, bir kanban işini Seçmek, Başlatmak, Tamamlamak ve Boşaltmak için bir pencere öğesi barkod tarayıcısından tarayıcı girişini destekler.</span><span class="sxs-lookup"><span data-stu-id="fdbda-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="fdbda-105">Kayıt modları</span><span class="sxs-lookup"><span data-stu-id="fdbda-105">Registration modes</span></span>
------------------

<span data-ttu-id="fdbda-106">**Tarayıcı kaydı** FastTab sekmesinde, bir kanban kart numarasını seçtiğinizde veya manuel olarak numarayı Kanban kart numarası alanına yazdığınızda eylemi kontrol eden kayıt modunu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fdbda-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="fdbda-107">Kayıt modu ayarla</span><span class="sxs-lookup"><span data-stu-id="fdbda-107">Set registration mode</span></span> | <span data-ttu-id="fdbda-108">Açıklama</span><span class="sxs-lookup"><span data-stu-id="fdbda-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdbda-109">Başlangıç</span><span class="sxs-lookup"><span data-stu-id="fdbda-109">Start</span></span>                 | <span data-ttu-id="fdbda-110">Bir Kanban transfer işini devam eden olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fdbda-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="fdbda-111">Tam</span><span class="sxs-lookup"><span data-stu-id="fdbda-111">Complete</span></span>              | <span data-ttu-id="fdbda-112">Bir Kanban transfer işini tamamlandı olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fdbda-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="fdbda-113">Boşalt</span><span class="sxs-lookup"><span data-stu-id="fdbda-113">Empty</span></span>                 | <span data-ttu-id="fdbda-114">Bir Kanban kartının referans verdiği malzeme işleme birimini boş olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fdbda-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="fdbda-115">Seç</span><span class="sxs-lookup"><span data-stu-id="fdbda-115">Select</span></span>                | <span data-ttu-id="fdbda-116">Bir Kanban kart numarası kaydeder ve referans verilen işi Kanban listesinde otomatik olarak seçer.</span><span class="sxs-lookup"><span data-stu-id="fdbda-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="fdbda-117">Kayıt modu Seç</span><span class="sxs-lookup"><span data-stu-id="fdbda-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="fdbda-118">İş seçmek için barkod okuyucuyu kullandığınızda, kanban panosunun görüntüleme modu değişir.</span><span class="sxs-lookup"><span data-stu-id="fdbda-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="fdbda-119">Bu modda, aşağıdaki koşullar geçerlidir:</span><span class="sxs-lookup"><span data-stu-id="fdbda-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="fdbda-120">Yalnızca taranan kanban işi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="fdbda-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="fdbda-121">Seçilen işin ayrıntıları **Ayrıntılar** FastTab'inde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="fdbda-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="fdbda-122">**İletiler** FastTab'i, yalnızca seçilen işin iletilerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="fdbda-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="fdbda-123">İşin durumunu, Eylem Bölmesi'nde bulunan işlevleri kullanarak değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fdbda-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="fdbda-124">Kanban transfer panosu, bu süre boyunca yalnızca tek bir işi görüntülemeye devam eder.</span><span class="sxs-lookup"><span data-stu-id="fdbda-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="fdbda-125">İşler listesindeki bilgileri Eylem Bölmesi'ndeki **Yenile** (Shift+F5) seçeneğini tıklayarak el ile güncelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fdbda-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="fdbda-126">Bilgileri güncelledikten sonra, iş filtresi için tüm sonuçlar yeniden görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="fdbda-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="fdbda-127">İş durumu ve olası eylemler</span><span class="sxs-lookup"><span data-stu-id="fdbda-127">Job status and possible actions</span></span>
<span data-ttu-id="fdbda-128">İşi daha fazla işleyip işleyemeyeceğinizi, seçilen işin durumu ve etkinlik kanban'ları için ilişkilendirilmiş işlerin durumu belirler.</span><span class="sxs-lookup"><span data-stu-id="fdbda-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="fdbda-129">Aşağıdaki tabloda bu durum ve görevler hakkındaki bilgiler görüntülenmektedir:</span><span class="sxs-lookup"><span data-stu-id="fdbda-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="fdbda-130">İşler için kullanılabilir durumdaki veya işlerin referans verdiği işleme birimlerine yönelik durumlar.</span><span class="sxs-lookup"><span data-stu-id="fdbda-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="fdbda-131">İş için gerçekleştirebileceğiniz her bir görev.</span><span class="sxs-lookup"><span data-stu-id="fdbda-131">Each task that you can perform for the job.</span></span>

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
<th><span data-ttu-id="fdbda-132">İş türü</span><span class="sxs-lookup"><span data-stu-id="fdbda-132">Job type</span></span></th>
<th><span data-ttu-id="fdbda-133">İş durumu veya işleme birimi durumu</span><span class="sxs-lookup"><span data-stu-id="fdbda-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="fdbda-134">Malzeme çekme listesini güncelleştir</span><span class="sxs-lookup"><span data-stu-id="fdbda-134">Update picking list</span></span></th>
<th><span data-ttu-id="fdbda-135">Başlangıç</span><span class="sxs-lookup"><span data-stu-id="fdbda-135">Start</span></span></th>
<th><span data-ttu-id="fdbda-136">Kaydı güncelleştir</span><span class="sxs-lookup"><span data-stu-id="fdbda-136">Update registration</span></span></th>
<th><span data-ttu-id="fdbda-137">Tam</span><span class="sxs-lookup"><span data-stu-id="fdbda-137">Complete</span></span></th>
<th><span data-ttu-id="fdbda-138">Boşalt</span><span class="sxs-lookup"><span data-stu-id="fdbda-138">Empty</span></span></th>
<th><span data-ttu-id="fdbda-139">Olay kanbanları oluştur</span><span class="sxs-lookup"><span data-stu-id="fdbda-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fdbda-140">Transfer et</span><span class="sxs-lookup"><span data-stu-id="fdbda-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="fdbda-141">Planlanmadı</span><span class="sxs-lookup"><span data-stu-id="fdbda-141">Not planned</span></span></li>
<li><span data-ttu-id="fdbda-142">İlişkilendirilmiş iş yok veya ilişkilendirilmiş işler Tamamlanmış</span><span class="sxs-lookup"><span data-stu-id="fdbda-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="fdbda-143">Evet</span><span class="sxs-lookup"><span data-stu-id="fdbda-143">Yes</span></span></td>
<td><span data-ttu-id="fdbda-144">Evet</span><span class="sxs-lookup"><span data-stu-id="fdbda-144">Yes</span></span></td>
<td><span data-ttu-id="fdbda-145">Evet</span><span class="sxs-lookup"><span data-stu-id="fdbda-145">Yes</span></span></td>
<td><span data-ttu-id="fdbda-146">Evet</span><span class="sxs-lookup"><span data-stu-id="fdbda-146">Yes</span></span></td>
<td><span data-ttu-id="fdbda-147">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-147">No</span></span></td>
<td><span data-ttu-id="fdbda-148">Evet</span><span class="sxs-lookup"><span data-stu-id="fdbda-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdbda-149">Transfer et</span><span class="sxs-lookup"><span data-stu-id="fdbda-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="fdbda-150">Planlanmadı</span><span class="sxs-lookup"><span data-stu-id="fdbda-150">Not planned</span></span></li>
<li><span data-ttu-id="fdbda-151">İlişkilendirilmiş iş Tamamlanmamış</span><span class="sxs-lookup"><span data-stu-id="fdbda-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="fdbda-152">Evet</span><span class="sxs-lookup"><span data-stu-id="fdbda-152">Yes</span></span></td>
<td><span data-ttu-id="fdbda-153">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-153">No</span></span></td>
<td><span data-ttu-id="fdbda-154">Evet</span><span class="sxs-lookup"><span data-stu-id="fdbda-154">Yes</span></span></td>
<td><span data-ttu-id="fdbda-155">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-155">No</span></span></td>
<td><span data-ttu-id="fdbda-156">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-156">No</span></span></td>
<td><span data-ttu-id="fdbda-157">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdbda-158">Transfer et</span><span class="sxs-lookup"><span data-stu-id="fdbda-158">Transfer</span></span></td>
<td><span data-ttu-id="fdbda-159">Devam ediyor</span><span class="sxs-lookup"><span data-stu-id="fdbda-159">In progress</span></span></td>
<td><span data-ttu-id="fdbda-160">Evet</span><span class="sxs-lookup"><span data-stu-id="fdbda-160">Yes</span></span></td>
<td><span data-ttu-id="fdbda-161">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-161">No</span></span></td>
<td><span data-ttu-id="fdbda-162">Evet</span><span class="sxs-lookup"><span data-stu-id="fdbda-162">Yes</span></span></td>
<td><span data-ttu-id="fdbda-163">Evet</span><span class="sxs-lookup"><span data-stu-id="fdbda-163">Yes</span></span></td>
<td><span data-ttu-id="fdbda-164">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-164">No</span></span></td>
<td><span data-ttu-id="fdbda-165">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdbda-166">Transfer et</span><span class="sxs-lookup"><span data-stu-id="fdbda-166">Transfer</span></span></td>
<td><span data-ttu-id="fdbda-167">Tamamlandı</span><span class="sxs-lookup"><span data-stu-id="fdbda-167">Completed</span></span></td>
<td><span data-ttu-id="fdbda-168">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-168">No</span></span></td>
<td><span data-ttu-id="fdbda-169">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-169">No</span></span></td>
<td><span data-ttu-id="fdbda-170">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-170">No</span></span></td>
<td><span data-ttu-id="fdbda-171">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-171">No</span></span></td>
<td><span data-ttu-id="fdbda-172">Evet</span><span class="sxs-lookup"><span data-stu-id="fdbda-172">Yes</span></span></td>
<td><span data-ttu-id="fdbda-173">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdbda-174">Transfer et veya işle</span><span class="sxs-lookup"><span data-stu-id="fdbda-174">Transfer or process</span></span></td>
<td><span data-ttu-id="fdbda-175">Boşalt</span><span class="sxs-lookup"><span data-stu-id="fdbda-175">Empty</span></span></td>
<td><span data-ttu-id="fdbda-176">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-176">No</span></span></td>
<td><span data-ttu-id="fdbda-177">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-177">No</span></span></td>
<td><span data-ttu-id="fdbda-178">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-178">No</span></span></td>
<td><span data-ttu-id="fdbda-179">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-179">No</span></span></td>
<td><span data-ttu-id="fdbda-180">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-180">No</span></span></td>
<td><span data-ttu-id="fdbda-181">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdbda-182">Transfer et veya işle</span><span class="sxs-lookup"><span data-stu-id="fdbda-182">Transfer or process</span></span></td>
<td><span data-ttu-id="fdbda-183">Kanban kartı bulunamadı</span><span class="sxs-lookup"><span data-stu-id="fdbda-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="fdbda-184">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-184">No</span></span></td>
<td><span data-ttu-id="fdbda-185">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-185">No</span></span></td>
<td><span data-ttu-id="fdbda-186">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-186">No</span></span></td>
<td><span data-ttu-id="fdbda-187">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-187">No</span></span></td>
<td><span data-ttu-id="fdbda-188">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-188">No</span></span></td>
<td><span data-ttu-id="fdbda-189">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdbda-190">Transfer et veya işle</span><span class="sxs-lookup"><span data-stu-id="fdbda-190">Transfer or process</span></span></td>
<td><span data-ttu-id="fdbda-191">Kanban kartı bulundu, ancak bir kanbana atanmamış</span><span class="sxs-lookup"><span data-stu-id="fdbda-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="fdbda-192">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-192">No</span></span></td>
<td><span data-ttu-id="fdbda-193">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-193">No</span></span></td>
<td><span data-ttu-id="fdbda-194">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-194">No</span></span></td>
<td><span data-ttu-id="fdbda-195">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-195">No</span></span></td>
<td><span data-ttu-id="fdbda-196">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-196">No</span></span></td>
<td><span data-ttu-id="fdbda-197">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdbda-198">İşle</span><span class="sxs-lookup"><span data-stu-id="fdbda-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="fdbda-199">Planlanmadı</span><span class="sxs-lookup"><span data-stu-id="fdbda-199">Not planned</span></span></li>
<li><span data-ttu-id="fdbda-200">Hazırlandı</span><span class="sxs-lookup"><span data-stu-id="fdbda-200">Prepared</span></span></li>
<li><span data-ttu-id="fdbda-201">Devam ediyor</span><span class="sxs-lookup"><span data-stu-id="fdbda-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="fdbda-202">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-202">No</span></span></td>
<td><span data-ttu-id="fdbda-203">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-203">No</span></span></td>
<td><span data-ttu-id="fdbda-204">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-204">No</span></span></td>
<td><span data-ttu-id="fdbda-205">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-205">No</span></span></td>
<td><span data-ttu-id="fdbda-206">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-206">No</span></span></td>
<td><span data-ttu-id="fdbda-207">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdbda-208">İşle</span><span class="sxs-lookup"><span data-stu-id="fdbda-208">Process</span></span></td>
<td><span data-ttu-id="fdbda-209">Tamamlandı</span><span class="sxs-lookup"><span data-stu-id="fdbda-209">Completed</span></span></td>
<td><span data-ttu-id="fdbda-210">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-210">No</span></span></td>
<td><span data-ttu-id="fdbda-211">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-211">No</span></span></td>
<td><span data-ttu-id="fdbda-212">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-212">No</span></span></td>
<td><span data-ttu-id="fdbda-213">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-213">No</span></span></td>
<td><span data-ttu-id="fdbda-214">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-214">No</span></span></td>
<td><span data-ttu-id="fdbda-215">Hayır</span><span class="sxs-lookup"><span data-stu-id="fdbda-215">No</span></span></td>
</tr>
</tbody>
</table>





