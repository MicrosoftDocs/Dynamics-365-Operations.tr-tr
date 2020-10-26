---
title: Master planlama çalışmasını izleme
description: Bu konu, üretim planlayıcısının bir master planlamanın devam edip etmediğini nasıl görebileceğini açıklar.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 045b82af6f65b22e1c683f8de47a6df282711e6a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978149"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="58d68-103">Master planlama çalışmasını izleme</span><span class="sxs-lookup"><span data-stu-id="58d68-103">Monitor a master planning run</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a><span data-ttu-id="58d68-104">Master planlama ilerlemesini görselleştirmek için Gantt şeması kullanma</span><span class="sxs-lookup"><span data-stu-id="58d68-104">Use a Gantt chart to visualize master planning progress</span></span>

<span data-ttu-id="58d68-105">**Master planlama ilerlemesini görüntüleme** sayfasından, geçmiş master planlama çalışmalarının ayrıntılarını Gantt şeması olarak görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58d68-105">From the **View master planning progress** page, you can view details of historical master planning runs as a Gantt chart.</span></span> <span data-ttu-id="58d68-106">Bu işlev, master planlamanın çeşitli aşamalarında harcanan zamanı anlamanıza yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="58d68-106">This functionality can help you understand the time that is spent on the various phases of master planning.</span></span> <span data-ttu-id="58d68-107">Var olan bir etkin planlama işi için ilerlemeyi izlemek ve tahmini kalan süreyi görüntülemek üzere **Master planlama ilerlemesini görüntüleme** sayfası kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="58d68-107">For a current active planning job, the **View master planning progress** page can be used to track progress and view the estimated remaining time.</span></span>

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a><span data-ttu-id="58d68-108">Master plan ilerlemesi görselleştirme özelliğini açma ve kullanma</span><span class="sxs-lookup"><span data-stu-id="58d68-108">Turn on and use the Master plan progress visualization feature</span></span>

<span data-ttu-id="58d68-109">Bu işlevi kullanmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="58d68-109">To use this functionality, follow these steps.</span></span>

1. <span data-ttu-id="58d68-110">**Özellik yönetimi** çalışma alanındaki **Yeni** sekmesinde, listeden **Master planlama ilerlemesi görselleştirmesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="58d68-110">In the **Feature management** workspace, on the **New** tab, select **Master planning progress visualization** in the list.</span></span> <span data-ttu-id="58d68-111">Özellik, **Yeni** sekmesinde görünmüyorsa **Etkileştirilmemiş** ve **Tümü** sekmelerine bakın.</span><span class="sxs-lookup"><span data-stu-id="58d68-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="58d68-112">**Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="58d68-112">Select **Enable now**.</span></span> <span data-ttu-id="58d68-113">Alternatif olarak, **Planla**'yı seçin ve ardından özelliğin açılmasını istediğiniz zamanı seçin.</span><span class="sxs-lookup"><span data-stu-id="58d68-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

<span data-ttu-id="58d68-114">**Master planlama ilerlemesini görüntüleme** sayfası hem geçmiş planlama işlerini hem de etkin planlama işlerini görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="58d68-114">The **View master planning progress** page can display both historical planning jobs and active planning jobs.</span></span> 

<span data-ttu-id="58d68-115">Geçmiş planlama işlerini görüntülemek için iki seçenek vardır.</span><span class="sxs-lookup"><span data-stu-id="58d68-115">To view historical planning jobs, there are two options.</span></span> 

1. <span data-ttu-id="58d68-116">**Master planlama \> Ayar \> Planlar \> Master planlar**'a gidin ve ardından Eylem Bölmesinde **Geçmiş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="58d68-116">Go to **Master planning \> Setup \> Plans \> Master plans**, and then, on the Action Pane, select **History**.</span></span> <span data-ttu-id="58d68-117">İstediğiniz iş seçiliyken **Sorgular**'ı seçin ve ardından **İlerlemeyi görüntüle** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="58d68-117">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>
1. <span data-ttu-id="58d68-118">**Master planlama \> Çalışma alanları \> Master planlama**'ya gidin, Master planlama kutucuğunda **Geçmiş**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58d68-118">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **History**.</span></span> <span data-ttu-id="58d68-119">İstediğiniz iş seçiliyken **Sorgular**'ı seçin ve ardından **İlerlemeyi görüntüle** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="58d68-119">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="58d68-120">Etkin planlama işlerini görüntülemek için iki seçenek vardır.</span><span class="sxs-lookup"><span data-stu-id="58d68-120">To view active planning jobs, there are two options.</span></span> 
1. <span data-ttu-id="58d68-121">**Master planlama \> Çalışma alanları \> Master planlama**'ya gidin, Eylem Bölmesinde **Bitirilmemiş planlama işlemi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="58d68-121">Go to **Master planning \> Workspaces \> Master planning**, on the Action Pane, select **Unfinished planning process**.</span></span> <span data-ttu-id="58d68-122">İstediğiniz iş seçiliyken **Sorgular**'ı seçin ve ardından **İlerlemeyi görüntüle** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="58d68-122">With the desired job selected, select **Inquiries**,  and then select **View progress**.</span></span>
1. <span data-ttu-id="58d68-123">**Master planlama \> Çalışma alanları \> Master planlama**'ya gidin, Master planlama kutucuğunda **İlerlemeyi görüntüle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58d68-123">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **View progress**.</span></span> <span data-ttu-id="58d68-124">İstediğiniz iş seçiliyken **Sorgular**'ı seçin ve ardından **İlerlemeyi görüntüle** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="58d68-124">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="58d68-125">Etkin işleri yalnızca bir planlama işi işlenirken görüntüleyebileceğinizi unutmayın.</span><span class="sxs-lookup"><span data-stu-id="58d68-125">Note you can view active jobs only when a planning job is processing.</span></span>

### <a name="analyze-a-master-planning-job"></a><span data-ttu-id="58d68-126">Master planlama işini analiz etme</span><span class="sxs-lookup"><span data-stu-id="58d68-126">Analyze a master planning job</span></span>

<span data-ttu-id="58d68-127">Gantt şemasında, harcanan zamanla ilgili ek ayrıntıları görüntülemek için aşağıdaki planlama süreçlerinin her birini genişletebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="58d68-127">In the Gantt chart, you can expand each of the following planning processes to view additional details about the time that is spent:</span></span>

- <span data-ttu-id="58d68-128">Başlatılıyor</span><span class="sxs-lookup"><span data-stu-id="58d68-128">Initializing</span></span>
- <span data-ttu-id="58d68-129">Veriler siliniyor ve ekleniyor</span><span class="sxs-lookup"><span data-stu-id="58d68-129">Deleting and inserting data</span></span>
- <span data-ttu-id="58d68-130">Tedarik planlama</span><span class="sxs-lookup"><span data-stu-id="58d68-130">Coverage planning</span></span>
- <span data-ttu-id="58d68-131">Gecikmeler</span><span class="sxs-lookup"><span data-stu-id="58d68-131">Delays</span></span>
- <span data-ttu-id="58d68-132">Eylem iletileri</span><span class="sxs-lookup"><span data-stu-id="58d68-132">Action messages</span></span>
- <span data-ttu-id="58d68-133">Sonlandırma</span><span class="sxs-lookup"><span data-stu-id="58d68-133">Finalization</span></span>
- <span data-ttu-id="58d68-134">Otomatik kesinleştirme</span><span class="sxs-lookup"><span data-stu-id="58d68-134">Auto-firming</span></span>

<span data-ttu-id="58d68-135">Eylem iletilerini kullanmanın etkisini görmek istiyorsanız Gantt şeması yararlı bir araçtır.</span><span class="sxs-lookup"><span data-stu-id="58d68-135">The Gantt chart is a useful tool if you want to view the impact of using action messages.</span></span>

#### <a name="navigation-in-the-gantt-chart"></a><span data-ttu-id="58d68-136">Gantt şemasında gezinme</span><span class="sxs-lookup"><span data-stu-id="58d68-136">Navigation in the Gantt chart</span></span>

- <span data-ttu-id="58d68-137">Seçilen grubu genişletmek ve ayrıntıları göstermek için ağaç görünümünde artı işaretini (**+**) seçin.</span><span class="sxs-lookup"><span data-stu-id="58d68-137">To expand the selected group and show the details, select the plus sign (**+**) in the tree view.</span></span>
- <span data-ttu-id="58d68-138">Seçilen grubu daraltmak için ağaç görünümünde eksi işaretini (**–**) seçin.</span><span class="sxs-lookup"><span data-stu-id="58d68-138">To collapse the selected group, select the minus sign (**–**) in the tree view.</span></span>
- <span data-ttu-id="58d68-139">Gezinmek için klavyenizi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58d68-139">You can use your keyboard for navigation.</span></span> <span data-ttu-id="58d68-140">Satırlar arasında gezinmek için **Yukarı ok** ve **Aşağı ok** tuşlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="58d68-140">Use the **Up arrow** and **Down arrow** keys to move between rows.</span></span> <span data-ttu-id="58d68-141">Grupları genişletmek ve daraltmak için **Sağ ok** ve **Sol ok** tuşlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="58d68-141">Use the **Right arrow** and **Left arrow** keys to expand and collapse groups.</span></span>
- <span data-ttu-id="58d68-142">Gantt şemasındaki tüm düzeyleri açmak veya kapatmak için **Tümünü genişlet** veya **Tümünü daralt**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="58d68-142">To open or close all levels in the Gantt chart, select **Expand all** or **Collapse all**.</span></span>
- <span data-ttu-id="58d68-143">İlgili işleme süresini görüntülemek için bir görevin üzerine gelin.</span><span class="sxs-lookup"><span data-stu-id="58d68-143">To view the related processing time, hover over a task.</span></span> <span data-ttu-id="58d68-144">(Görevler, Gantt şemasındaki en düşük düzeydir.)</span><span class="sxs-lookup"><span data-stu-id="58d68-144">(Tasks are the lowest level in the Gantt chart.)</span></span>

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a><span data-ttu-id="58d68-145">İşleri karşılaştırmak için ek bir master planlama çalışması görüntüleme</span><span class="sxs-lookup"><span data-stu-id="58d68-145">View an additional master planning run to compare jobs</span></span>

<span data-ttu-id="58d68-146">**Ek master planlama çalışması gösterme** alanında bir master planlama işi seçerek Gantt şemasında ek bir master planlama çalışmasını görüntüleyebilir ve iki işi karşılaştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58d68-146">By selecting a master planning job on field **Show additional master planning run**, you can view an additional master planning run in the Gantt chart and compare the two jobs.</span></span>

#### <a name="bom-level-display"></a><span data-ttu-id="58d68-147">Ürün reçetesi düzeyinde görüntüleme</span><span class="sxs-lookup"><span data-stu-id="58d68-147">BOM-level display</span></span>

<span data-ttu-id="58d68-148">Ürün reçetesi (BOM) düzeyleri tedarik planlama, gecikmeler, eylemler ve kesinleştirme için farklı gösterilir.</span><span class="sxs-lookup"><span data-stu-id="58d68-148">Bill of materials (BOM) levels are shown differently for coverage planning, delays, actions, and firming.</span></span>

- <span data-ttu-id="58d68-149">**Tedarik planlama**: Ürün reçetesi düzeyleri beklenen şekilde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="58d68-149">**Coverage planning** – BOM levels are shown as expected.</span></span> <span data-ttu-id="58d68-150">Yukarıdan aşağıya doğru hesaplanırlar.</span><span class="sxs-lookup"><span data-stu-id="58d68-150">They are calculated from the top down.</span></span>

    <span data-ttu-id="58d68-151">**Örnek:** Ürün reçetesi düzeyi 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="58d68-151">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="58d68-152">**Gecikmeler**: Ürün reçetesi düzeyleri, tedarik planlama ürün reçetesi seviyeleri -1 ile çarpılarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="58d68-152">**Delays** – BOM levels are shown as the coverage planning BOM levels multiplied by –1.</span></span> <span data-ttu-id="58d68-153">(Başka bir deyişle, bunların negatif işareti vardır.)</span><span class="sxs-lookup"><span data-stu-id="58d68-153">(In other words, they have a negative sign.)</span></span>

    <span data-ttu-id="58d68-154">**Örnek:** Ürün reçetesi düzeyi –2, –1, 0</span><span class="sxs-lookup"><span data-stu-id="58d68-154">**Example:** BOM level –2, –1, 0</span></span>

- <span data-ttu-id="58d68-155">**Eylem iletisi**: Ürün reçetesi düzeyleri beklenen şekilde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="58d68-155">**Action message** – BOM levels are shown as expected.</span></span> <span data-ttu-id="58d68-156">Yukarıdan aşağıya doğru hesaplanırlar.</span><span class="sxs-lookup"><span data-stu-id="58d68-156">They are calculated from the top down.</span></span>

    <span data-ttu-id="58d68-157">**Örnek:** Ürün reçetesi düzeyi 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="58d68-157">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="58d68-158">**Otomatik kesinleştirme**: Ürün reçetesi düzeyleri, 999 eksi tedarik planlama ürün reçetesi düzeyi olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="58d68-158">**Auto-firming** – BOM levels are shown as 999 minus the coverage planning BOM level.</span></span>

    <span data-ttu-id="58d68-159">**Örnek:** Ürün reçetesi düzeyi 999, 998, 997</span><span class="sxs-lookup"><span data-stu-id="58d68-159">**Example:** BOM level 999, 998, 997</span></span>

<span data-ttu-id="58d68-160">Aşağıdaki tablo, davranışı özetlemektedir.</span><span class="sxs-lookup"><span data-stu-id="58d68-160">The following table summarizes the behavior.</span></span>

| <span data-ttu-id="58d68-161">Gösterilen ürün reçetesi düzeyi</span><span class="sxs-lookup"><span data-stu-id="58d68-161">BOM level that is shown</span></span> | <span data-ttu-id="58d68-162">Son madde</span><span class="sxs-lookup"><span data-stu-id="58d68-162">End item</span></span> | <span data-ttu-id="58d68-163">Alt bileşen</span><span class="sxs-lookup"><span data-stu-id="58d68-163">Subcomponent</span></span> | <span data-ttu-id="58d68-164">Hammadde</span><span class="sxs-lookup"><span data-stu-id="58d68-164">Raw material</span></span> |
|---|---|---|---|
| <span data-ttu-id="58d68-165">Tedarik planlama</span><span class="sxs-lookup"><span data-stu-id="58d68-165">Coverage planning</span></span> | <span data-ttu-id="58d68-166">0</span><span class="sxs-lookup"><span data-stu-id="58d68-166">0</span></span> | <span data-ttu-id="58d68-167">1</span><span class="sxs-lookup"><span data-stu-id="58d68-167">1</span></span> | <span data-ttu-id="58d68-168">2</span><span class="sxs-lookup"><span data-stu-id="58d68-168">2</span></span> |
| <span data-ttu-id="58d68-169">Gecikmeler</span><span class="sxs-lookup"><span data-stu-id="58d68-169">Delays</span></span> | <span data-ttu-id="58d68-170">0</span><span class="sxs-lookup"><span data-stu-id="58d68-170">0</span></span> | <span data-ttu-id="58d68-171">–1</span><span class="sxs-lookup"><span data-stu-id="58d68-171">–1</span></span> | <span data-ttu-id="58d68-172">–2</span><span class="sxs-lookup"><span data-stu-id="58d68-172">–2</span></span> |
| <span data-ttu-id="58d68-173">Eylem iletisi</span><span class="sxs-lookup"><span data-stu-id="58d68-173">Action message</span></span> | <span data-ttu-id="58d68-174">0</span><span class="sxs-lookup"><span data-stu-id="58d68-174">0</span></span> | <span data-ttu-id="58d68-175">1</span><span class="sxs-lookup"><span data-stu-id="58d68-175">1</span></span> | <span data-ttu-id="58d68-176">2</span><span class="sxs-lookup"><span data-stu-id="58d68-176">2</span></span> |
| <span data-ttu-id="58d68-177">Otomatik kesinleştirme</span><span class="sxs-lookup"><span data-stu-id="58d68-177">Auto-firming</span></span> | <span data-ttu-id="58d68-178">999</span><span class="sxs-lookup"><span data-stu-id="58d68-178">999</span></span> | <span data-ttu-id="58d68-179">998</span><span class="sxs-lookup"><span data-stu-id="58d68-179">998</span></span> | <span data-ttu-id="58d68-180">997</span><span class="sxs-lookup"><span data-stu-id="58d68-180">997</span></span> |

#### <a name="visualize-progress"></a><span data-ttu-id="58d68-181">İlerlemeyi görselleştirme</span><span class="sxs-lookup"><span data-stu-id="58d68-181">Visualize progress</span></span>

<span data-ttu-id="58d68-182">Çalışmakta olan bir master planlama işini görüntülüyorsanız ilerleme, Gantt şemasında renklerle gösterilir.</span><span class="sxs-lookup"><span data-stu-id="58d68-182">If you view a master planning job that is currently running, progress is shown through colors in the Gantt chart.</span></span> <span data-ttu-id="58d68-183">Mavi tema için aşağıdaki renkler geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="58d68-183">The following colors apply to the blue theme.</span></span> <span data-ttu-id="58d68-184">Diğer renk temaları için renkler farklı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="58d68-184">For other color themes, the colors will differ.</span></span>

- <span data-ttu-id="58d68-185">**Lacivert**: Tamamlanmış planlama görevleri.</span><span class="sxs-lookup"><span data-stu-id="58d68-185">**Dark blue** – Completed planning tasks.</span></span>
- <span data-ttu-id="58d68-186">**Turuncu**: Şu anda devam eden görev.</span><span class="sxs-lookup"><span data-stu-id="58d68-186">**Orange** – The task that is currently in progress.</span></span>
- <span data-ttu-id="58d68-187">**Açık mavi**: Kalan görevler için tahmin.</span><span class="sxs-lookup"><span data-stu-id="58d68-187">**Light blue** – The estimate for remaining tasks.</span></span>

<span data-ttu-id="58d68-188">Renk, Gantt şemasında yalnızca en düşük düzeyde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="58d68-188">The color is shown only on the lowest level in the Gantt chart.</span></span> <span data-ttu-id="58d68-189">Master planlama işindeki tüm görevleri görüntülemek için **Tümünü genişlet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="58d68-189">Select **Expand all** to view all tasks in the master planning job.</span></span> <span data-ttu-id="58d68-190">Kalan görevlerin tahmini, geçmiş master planlama işlerini temel alır.</span><span class="sxs-lookup"><span data-stu-id="58d68-190">The estimate of remaining tasks is based on historical master planning jobs.</span></span>

## <a name="run-master-planning-and-track-processing-time"></a><span data-ttu-id="58d68-191">Master planlamayı çalıştırma ve işleme süresini izleme</span><span class="sxs-lookup"><span data-stu-id="58d68-191">Run master planning and track processing time</span></span>

1. <span data-ttu-id="58d68-192">Varsayılan panoda **Master planlama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="58d68-192">On the default dashboard, select **Master planning**.</span></span>
1. <span data-ttu-id="58d68-193">**Plan** alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="58d68-193">In the **Plan** field, enter or select a value.</span></span>
1. <span data-ttu-id="58d68-194">**Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="58d68-194">Select **Run**.</span></span>
1. <span data-ttu-id="58d68-195">**İşleme izleme saati** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="58d68-195">Set the **Track processing time** option to **Yes**.</span></span>
1. <span data-ttu-id="58d68-196">**İş parçacığı sayısı** alanına bir rakam girin.</span><span class="sxs-lookup"><span data-stu-id="58d68-196">In the **Number of threads** field, enter a number.</span></span>
1. <span data-ttu-id="58d68-197">**Eklenecek kayıtlar** hızlı sekmesinde **Filtrele**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="58d68-197">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="58d68-198">Kılavuzda, **Alan** alanının **Madde numarası** olarak ayarlandığı satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="58d68-198">In the grid, select the row where the **Field** field is set to **Item number**.</span></span>
1. <span data-ttu-id="58d68-199">**Ölçütler** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="58d68-199">In the **Criteria** field, enter a value.</span></span>
1. <span data-ttu-id="58d68-200">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="58d68-200">Select **OK**.</span></span>
