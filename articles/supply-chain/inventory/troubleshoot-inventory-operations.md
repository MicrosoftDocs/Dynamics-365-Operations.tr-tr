---
title: Stok işlemlerinde sorun giderme
description: Bu konuda, stok işlemleri ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceği açıklanmaktadır.
author: sherry-zheng
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 24e41e35b3e810c509a16b91fffd1e796ab9d134
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832070"
---
# <a name="troubleshoot-inventory-operations"></a><span data-ttu-id="aefbf-103">Stok işlemlerinde sorun giderme</span><span class="sxs-lookup"><span data-stu-id="aefbf-103">Troubleshoot inventory operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aefbf-104">Bu konuda, stok işlemleri ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="aefbf-104">This topic describes how to fix issues that you might encounter while you work with inventory operations.</span></span>

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a><span data-ttu-id="aefbf-105">Stok günlükleri için "İş akışı" açılan iletişim kutusunu bulamıyorum.</span><span class="sxs-lookup"><span data-stu-id="aefbf-105">I can't find the "Workflow" drop-down dialog box for inventory journals.</span></span>

### <a name="issue-description"></a><span data-ttu-id="aefbf-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="aefbf-106">Issue description</span></span>

<span data-ttu-id="aefbf-107">Günlük sayfasında **İş akışı** açılır iletişim kutusunu bulamazsınız veya ilgili iş akışı işlemleri kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="aefbf-107">You can't find the **Workflow** drop-down dialog box on the journal page, or related workflow operations aren't available.</span></span>

<span data-ttu-id="aefbf-108">Bu sorun, aşağıdaki alt bölümlerde açıklandığı gibi, üç nedenden dolayı oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-108">This issue can occur for three reasons, as described in the following subsections.</span></span>

### <a name="issue-resolution-1"></a><span data-ttu-id="aefbf-109">Sorunun çözümü 1</span><span class="sxs-lookup"><span data-stu-id="aefbf-109">Issue resolution 1</span></span>

<span data-ttu-id="aefbf-110">Sorun tüm kullanıcılar için geçerliyse sorunun nedeni onay iş akışının günlük adına atanmaması olabilir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-110">If the issue applies to all users, it might be occurring because the approval workflow hasn't been assigned to the journal name.</span></span> <span data-ttu-id="aefbf-111">Sorunu düzeltmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="aefbf-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="aefbf-112">**Stok Yönetimi &gt; Kurulum &gt;> Günlük adları &gt;> Stok** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="aefbf-112">Go to **Inventory Management &gt; Setup &gt; Journal names &gt; Inventory**.</span></span>
1. <span data-ttu-id="aefbf-113">Liste bölmesinde, ayarlarını açmak için bir günlük adı seçin.</span><span class="sxs-lookup"><span data-stu-id="aefbf-113">In the list pane, select a journal name to open its settings.</span></span>
1. <span data-ttu-id="aefbf-114">**Genel** hızlı sekmesinde, **Onay iş akışı** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="aefbf-114">On the **General** FastTab, set the **Approval workflow** option to *Yes*.</span></span> <span data-ttu-id="aefbf-115">Değişikliği onaylamanız istendiğinde, **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="aefbf-115">If you're prompted to confirm the change, select **Yes**.</span></span>
1. <span data-ttu-id="aefbf-116">**İş akışı** alanında, seçili günlük adı için kullanmak istediğiniz iş akışını seçin.</span><span class="sxs-lookup"><span data-stu-id="aefbf-116">In the **Workflow** field, select the workflow that you want to use for the selected journal name.</span></span>

### <a name="issue-resolution-2"></a><span data-ttu-id="aefbf-117">Sorunun çözümü 2</span><span class="sxs-lookup"><span data-stu-id="aefbf-117">Issue resolution 2</span></span>

<span data-ttu-id="aefbf-118">İş akışınızda özelleştirilmiş kod kullanılıyorsa sistemi yükselttikten sonra sorunlar oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-118">If your workflow uses customized code, issues might occur after you upgrade the system.</span></span> <span data-ttu-id="aefbf-119">Örneğin, günlük iş akışında **Gönder** düğmesi gri renkte olabilir. Bu nedenle, gönderimi onaylamak için düğmeyi seçemeyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aefbf-119">For example, in the journal workflow, the **Submit** button might be grayed out so you can't select it to approve a submission.</span></span>

<span data-ttu-id="aefbf-120">**Gönder** düğmesi gri renkteyse iş akışınız özelleştirilmiş olabilir. Bu, `FormDataUtil` öğesindeki `canSubmitToWorkflow()` iş akışı yönteminin genişletildiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-120">If the **Submit** button is grayed out, your workflow might have been customized, which means the method of the workflow, `canSubmitToWorkflow()` in `FormDataUtil`, has been extended.</span></span> <span data-ttu-id="aefbf-121">Bu sorunu gidermek için `canSubmitToWorkflow()` yöntemini genişletme şeklinizi aşağıdaki örnekte gösterilen yapıyı kullanarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="aefbf-121">To fix this issue, change the way that you extend the method of the `canSubmitToWorkflow()` to use the structure in the following example.</span></span>

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a><span data-ttu-id="aefbf-122">Sorunun çözümü 3</span><span class="sxs-lookup"><span data-stu-id="aefbf-122">Issue resolution 3</span></span>

<span data-ttu-id="aefbf-123">Sorun yalnızca belirli birkaç kullanıcı için geçerliyse bu kullanıcılar, stok günlüklerinde iş akışı işlemlerini çalıştırmak için gerekli güvenlik ayrıcalıklarına sahip olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-123">If the issue applies only to a few specific users, those users might not have the security privileges that are required to run workflow operations on inventory journals.</span></span> <span data-ttu-id="aefbf-124">Etkilenen her kullanıcının *Stok günlüğü iş akışının bakımını yapma* güvenlik ayrıcalığına sahip olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="aefbf-124">Verify that each affected user has the *Maintain inventory journal workflow* security privilege.</span></span> <span data-ttu-id="aefbf-125">Varsayılan olarak, bu ayrıcalık aynı adlı bir göreve atanır ve bu görev *Ambar çalışanı* ve *Ambar yöneticisi* rollerine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="aefbf-125">By default, this privilege is assigned to a duty that has same name, and that duty is applied to the *Warehouse worker* and *Warehouse manager* roles.</span></span>

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a><span data-ttu-id="aefbf-126">Stok günlüğüm sistem kilitli durumunda kalıyor ve iş akışı toplu işi çalışmıyor.</span><span class="sxs-lookup"><span data-stu-id="aefbf-126">My inventory journal remains in system-locked status, and the workflow batch job doesn't work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="aefbf-127">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="aefbf-127">Issue description</span></span>

<span data-ttu-id="aefbf-128">Stok günlükleriniz bir işlem tarafından kilitlenmiş ve yayınlanmıyor.</span><span class="sxs-lookup"><span data-stu-id="aefbf-128">One of your inventory journals is locked by some operation and isn't being released.</span></span> <span data-ttu-id="aefbf-129">Örneğin, deftere nakil sırasında (bir sistem kilitleme işlemidir) bilinmeyen bir hata oluşursa günlük, sistem kilitli durumunda kalabilir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-129">For example, if an unknown error occurs during posting (which is a system lock operation), the journal might remain in system-locked status.</span></span> <span data-ttu-id="aefbf-130">Bu durumda, iş akışı iş öğesi işleyicisi, kilit doğrulama işlemini gerçekleştirirken bir hata oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aefbf-130">In this case, the workflow work item handler will throw an error while it does lock validation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="aefbf-131">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="aefbf-131">Issue resolution</span></span>

<span data-ttu-id="aefbf-132">Supply Chain Management için SQL Server kurulumunda oturum açın ve **InventJournalTable.SystemBlocked** seçeneğinin *1* olarak ayarlanıp ayarlanmadığını kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="aefbf-132">Sign in to the SQL Server instance for Supply Chain Management, and check whether **InventJournalTable.SystemBlocked** is set to *1*.</span></span> <span data-ttu-id="aefbf-133">Bu şekilde ayarlanmışsa günlüğün kilitli durumda olmaması gerektiğinden emin olun ve ardından **InventJournalTable.SystemBlocked** seçeneğini *0* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="aefbf-133">If it is, make sure that the journal should not be in locked status, and then reset **InventJournalTable.SystemBlocked** to *0*.</span></span>

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a><span data-ttu-id="aefbf-134">Stok günlüğü iş akışım asla tamamlanmıyor ve günlük düzenlenemiyor ve nakledilemiyor.</span><span class="sxs-lookup"><span data-stu-id="aefbf-134">My inventory journal workflow is never completed, and the journal can't be edited or posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="aefbf-135">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="aefbf-135">Issue description</span></span>

<span data-ttu-id="aefbf-136">Bir günlük onay iş akışını gönderdikten sonra, iş akışı işlemesi yanıt vermemeye başlar ve günlüklerinizi düzenleyemez veya işleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="aefbf-136">After you submit a journal approval workflow, workflow processing stops responding, and you can't edit or process your journals.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="aefbf-137">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="aefbf-137">Issue resolution</span></span>

<span data-ttu-id="aefbf-138">İş akışı işlemenin tamamlanmamasının birden fazla nedeni olabilir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-138">There are several reasons why workflow processing might not be completed.</span></span> <span data-ttu-id="aefbf-139">Aşağıdaki sorunların olup olmadığını kontrol edin:</span><span class="sxs-lookup"><span data-stu-id="aefbf-139">Check for the following issues:</span></span>

- <span data-ttu-id="aefbf-140">**Stok yönetimi &gt; Kurulum &gt; Stok yönetimi iş akışları**'na gidin ve etkilenen iş akışının yapılandırmasını inceleyin.</span><span class="sxs-lookup"><span data-stu-id="aefbf-140">Go to **Inventory management &gt; Setup &gt; Inventory management workflows**, and review the configuration of the affected workflow.</span></span> <span data-ttu-id="aefbf-141">Daha fazla bilgi için bkz. [Stok günlüğü onay iş akışları](inventory-journal-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="aefbf-141">For more information, see [Inventory journal approval workflows](inventory-journal-workflow.md).</span></span>
- <span data-ttu-id="aefbf-142">İş akışı bir özel durum veya hata ile karşılaşıyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-142">The workflow might be encountering an exception or error.</span></span> <span data-ttu-id="aefbf-143">Etkilenen iş akışının iş öğesi geçmişini gözden geçirerek iş akışını sonlandıran bir uygulama hatası içerip içermediğini inceleyin.</span><span class="sxs-lookup"><span data-stu-id="aefbf-143">Review the work item history of the affected workflow to see whether it includes an application error that terminates the workflow.</span></span>
- <span data-ttu-id="aefbf-144">Stok günlüğü yalnızca onaylanırsa güncelleştirilebilir veya düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-144">The inventory journal can be updated or edited only if it's approved.</span></span> <span data-ttu-id="aefbf-145">Geri çağırma etkinse, günlüğü geri çağırmayı deneyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aefbf-145">If recall is active, you can try to recall the journal.</span></span> <span data-ttu-id="aefbf-146">İş akışı toplu işinin yürütülmesi birden çok nedenle askıya alınabilir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-146">Execution of the workflow batch job might be suspended for multiple reasons.</span></span> <span data-ttu-id="aefbf-147">Bu nedenlerden bazıları iş akışı çerçevesi sorunundan kaynaklanıyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-147">Some of these reasons might be caused by the workflow framework issue.</span></span>

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a><span data-ttu-id="aefbf-148">Stok günlüğü iş akışı koşulları, satır düzeyinde değil, yalnızca günlük düzeyinde uygulanıyor</span><span class="sxs-lookup"><span data-stu-id="aefbf-148">Inventory journal workflow conditions apply only at the journal level, not at the line level</span></span>

### <a name="issue-description"></a><span data-ttu-id="aefbf-149">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="aefbf-149">Issue description</span></span>

<span data-ttu-id="aefbf-150">Bu sorunla, maliyet tutarında stok günlüğü iş akışı koşulu ayarlamaya çalışmanız gibi durumlarda karşılaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aefbf-150">You might experience this issue if, for example, you try to set up an inventory journal workflow condition on the cost amount.</span></span> <span data-ttu-id="aefbf-151">1. adımın yalnızca maliyet tutarı 100'den az olduğunda çalışması için bir koşul ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="aefbf-151">You set up the condition so that step 1 is run only when the cost amount is less than 100.</span></span> <span data-ttu-id="aefbf-152">Ardından 2. adımın yalnızca maliyet tutarı 100'e eşit veya daha fazla olduğunda çalışması için başka bir koşul daha ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="aefbf-152">You then set up another condition so that step 2 is run only when the cost amount is more than or equal to 100.</span></span> <span data-ttu-id="aefbf-153">Ardından, iş akışı çalıştırıldığında iş akışı geçmişinde yalnızca tek satır gösterilir ve gönderilen değere bakılmaksızın, her zaman ilk koşul *true* olarak değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-153">Then, when the workflow is run, the workflow history shows only one line, and the first condition is always evaluated as *true*, regardless of the value that is submitted.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="aefbf-154">Sorun geçici çözümü</span><span class="sxs-lookup"><span data-stu-id="aefbf-154">Issue workaround</span></span>

<span data-ttu-id="aefbf-155">Geçerli sürümde, stok günlüğü iş akışı koşulları, satır düzeyinde değil, yalnızca günlük düzeyinde uyglanır.</span><span class="sxs-lookup"><span data-stu-id="aefbf-155">In the current release, inventory workflow conditions apply only at the journal level, not at the line level.</span></span> <span data-ttu-id="aefbf-156">Bu davranış tasarımdan kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="aefbf-156">This behavior is by design.</span></span> <span data-ttu-id="aefbf-157">Koşul ölçütlerinizi yalnızca günlük düzeyi özniteliklerinde ayarlamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="aefbf-157">We recommend that you set your condition criteria only on journal-level attributes.</span></span>

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a><span data-ttu-id="aefbf-158">Eldekilerin listesi sayfasındaki filtre bölmesi sonuçları beklediğim şekilde filtrelemiyor.</span><span class="sxs-lookup"><span data-stu-id="aefbf-158">The filter pane on the On-hand list page doesn't filter results as I expect.</span></span>

### <a name="issue-description"></a><span data-ttu-id="aefbf-159">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="aefbf-159">Issue description</span></span>

<span data-ttu-id="aefbf-160">**Eldekilerin listesi** sayfasındaki filtre bölmesinde yer alan filtreler, sonuçları beklediğiniz şekilde filtrelemiyor.</span><span class="sxs-lookup"><span data-stu-id="aefbf-160">The filters in the filter pane on the **On-hand list** page don't filter results as you expect.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="aefbf-161">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="aefbf-161">Issue resolution</span></span>

<span data-ttu-id="aefbf-162">Bu davranış tasarımdan kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="aefbf-162">This behavior is by design.</span></span>

<span data-ttu-id="aefbf-163"> *\*Eldekilerin listesi** sayfası, kullanılabilir tüm boyutları içeren ayrıntılı bir eldeki stok tablosundan toplanır.</span><span class="sxs-lookup"><span data-stu-id="aefbf-163">The **On-hand list** page is assembled from a detailed on-hand inventory table that includes all available dimensions.</span></span> <span data-ttu-id="aefbf-164">Ancak bu sayfadaki liste bir özettir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-164">However, the list on this page is a summary.</span></span> <span data-ttu-id="aefbf-165">Bu nedenle, gösterilen boyutlara göre değerleri toplayarak kaynak tablodaki satırları birleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-165">Therefore, it might combine rows from the source table by aggregating values according to the dimensions that are shown.</span></span>

<span data-ttu-id="aefbf-166">Filtre bölmesinde ayarlanan filtreler, toplanan listeye değil, kaynak tabloya uygulanır.</span><span class="sxs-lookup"><span data-stu-id="aefbf-166">Filters that are set up in the filter pane apply to the source table, not to the aggregated list.</span></span> <span data-ttu-id="aefbf-167">Bu davranış, [bu örneklerde](inventory-on-hand-list.md#examples) gösterildiği gibi bazen beklenmeyen sonuçlar doğurabilir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-167">This behavior can sometimes produce unexpected results, as shown in [these examples](inventory-on-hand-list.md#examples).</span></span>

<span data-ttu-id="aefbf-168">Ancak,  [ızgarada sağlanan filtreler](inventory-on-hand-list.md#grid-filters) toplanan liste için *geçerlidir* .</span><span class="sxs-lookup"><span data-stu-id="aefbf-168">However, the [filters that are provided in the grid](inventory-on-hand-list.md#grid-filters) *do* apply to the aggregated list.</span></span> <span data-ttu-id="aefbf-169">Bu filtreler kılavuzun üst kısmındaki hızlı filtreyi ve her sütun başlığının filtresini içerir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-169">These filters include both the QuickFilter at the top of the grid and the filter for each column heading.</span></span>

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a><span data-ttu-id="aefbf-170">Birim ve birim miktarı stok günlüğünde doğru çalışmıyor.</span><span class="sxs-lookup"><span data-stu-id="aefbf-170">The unit and unit quantity aren't working correctly in the inventory journal.</span></span>

### <a name="issue-description"></a><span data-ttu-id="aefbf-171">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="aefbf-171">Issue description</span></span>

<span data-ttu-id="aefbf-172">Stok günlüğünde birimlerle ve miktarlarla çalışırken aşağıdaki sorunlardan biriyle veya her ikisiyle birden karşılaşabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="aefbf-172">You might encounter one or both of the following issues when you work with units and quantities in an inventory journal:</span></span>

- <span data-ttu-id="aefbf-173">Serbest bırakılan ürün için bir dönüştürme birimi ayarlanırken stok günlüğünde birimleri veya birim miktarlarını görmezsiniz ve stok günlüğündeki birimi değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="aefbf-173">You don't see units or unit quantities in the inventory journal while a unit of conversion is set up for the released product, and you can't change the unit in the inventory journal.</span></span>
- <span data-ttu-id="aefbf-174">Stok günlüğünde **Miktar** ve **Birim** alanlarını görürsünüz ancak **Birim miktarı** alanını görmezsiniz.</span><span class="sxs-lookup"><span data-stu-id="aefbf-174">You see the **Quantity** and **Unit** fields in the inventory journal, but you don't see the **Unit quantity** field.</span></span> <span data-ttu-id="aefbf-175">Birimi değiştirir, bir miktar girer ve günlüğü deftere naklederseniz günlük, söz konusu miktar için özgün ölçü birimini göstermeye devam eder.</span><span class="sxs-lookup"><span data-stu-id="aefbf-175">If you change the unit, enter a quantity, and post the journal, the journal still shows the original unit of measurement for that quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="aefbf-176">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="aefbf-176">Issue resolution</span></span>

<span data-ttu-id="aefbf-177">Bu sorunu düzeltmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="aefbf-177">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="aefbf-178">**Özellik yönetimi** çalışma alanında, *Stok günlüklerinde ölçü birimi ve birim miktarı kullanımı* özelliğinin açık olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="aefbf-178">In the **Feature management** workspace, make sure that the *Using unit of measure and unit quantity in inventory journals* feature is turned on.</span></span> <span data-ttu-id="aefbf-179">Bu özellik, günlüğe **Birim** ve **Birim miktarı** alanlarını ekler.</span><span class="sxs-lookup"><span data-stu-id="aefbf-179">This feature adds the **Unit** and **Unit quantity** fields to the journal.</span></span>
1. <span data-ttu-id="aefbf-180">Özellik etkinleştirildikten sonra **Miktar**, **Birim miktarı** ve **Birim** alanlarını aşağıdaki şekilde kullanın.</span><span class="sxs-lookup"><span data-stu-id="aefbf-180">After the feature is turned on, use the **Quantity**, **Unit quantity**, and **Unit** fields in the following way:</span></span>

    - <span data-ttu-id="aefbf-181">**Miktar**: Serbest bırakılan ürün için tanımlanan varsayılan birimi kullanarak miktarı belirtin.</span><span class="sxs-lookup"><span data-stu-id="aefbf-181">**Quantity** – Specify the quantity by using the default unit that is defined for the released product.</span></span> <span data-ttu-id="aefbf-182">Ancak, varsayılan birimin kendisi burada gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="aefbf-182">However, the default unit itself isn't shown here.</span></span> <span data-ttu-id="aefbf-183">Varsayılan birim ile **Birim** alanında seçilen birim arasında dönüştürme işlemi ayarlandıysa, **Miktar** alanı **Birim miktarı** ve **Birim** alanlarındaki seçimlere göre otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-183">If a conversion is set up between the default unit and the unit that is selected in the **Unit** field, the **Quantity** field is automatically updated, based on the selections in the **Unit quantity** and **Unit** fields.</span></span>
    - <span data-ttu-id="aefbf-184">**Birim miktarı**: **Birim** alanında seçilen birimi kullanarak miktarı belirtin.</span><span class="sxs-lookup"><span data-stu-id="aefbf-184">**Unit quantity** – Specify the quantity by using the unit that is selected in the **Unit** field.</span></span>
    - <span data-ttu-id="aefbf-185">**Birim**: **Birim miktarı** alanındaki değere uygulanacak birimi seçin.</span><span class="sxs-lookup"><span data-stu-id="aefbf-185">**Unit** – Select the unit to apply to the value in the **Unit quantity** field.</span></span>

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a><span data-ttu-id="aefbf-186">Şu hata iletisini alıyorum: "Stok tutma birimi için maksimum ondalık birim sayısı 0'dır."</span><span class="sxs-lookup"><span data-stu-id="aefbf-186">I receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

### <a name="issue-description"></a><span data-ttu-id="aefbf-187">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="aefbf-187">Issue description</span></span>

<span data-ttu-id="aefbf-188">Bir stok hareketini veya stok rezervasyonunu deftere nakletmeye çalıştığınızda, şu hata iletisini alırsınız: "Stok tutma birimi için maksimum ondalık birim sayısı 0'dır."</span><span class="sxs-lookup"><span data-stu-id="aefbf-188">When you try to post an inventory transaction or an inventory reservation, you receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

<span data-ttu-id="aefbf-189">Bu sorun stok hareketi miktarı, alanın desteklediği duyarlık düzeyinin altında olan bir ondalık değer olarak belirtildiğinde oluşur.</span><span class="sxs-lookup"><span data-stu-id="aefbf-189">This issue occurs when the inventory transaction quantity is specified as a decimal value that is below the level of precision that the field supports.</span></span> <span data-ttu-id="aefbf-190">Örneğin, bir stok hareketi için *0,5* miktarı belirtilmiştir ancak yalnızca tamsayı olan miktarlar desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-190">For example, a quantity of *0.5* has been specified for an inventory transaction, but only integer quantities are supported.</span></span> <span data-ttu-id="aefbf-191">Bu nedenle, değer *0,5* yerine *1* olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="aefbf-191">Therefore, the value should be *1* instead of *0.5*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="aefbf-192">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="aefbf-192">Issue resolution</span></span>

1. <span data-ttu-id="aefbf-193">Stok hareketlerindeki miktarları yuvarlamak için SQL Server kurulumunuzda aşağıdaki kodu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="aefbf-193">Run the following script on your SQL Server instance to round quantities in the inventory transactions.</span></span> <span data-ttu-id="aefbf-194">Bu kod, **inventTrans** tablosundaki değerleri düzeltecektir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-194">This script will correct values in the **inventTrans** table.</span></span>

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. <span data-ttu-id="aefbf-195">**Sorunu düzelt** seçeneğinin açık olduğu bir eldekiler tutarlılık denetimi çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="aefbf-195">Run an on-hand consistency check where the **fix error** option is turned on.</span></span> <span data-ttu-id="aefbf-196">Bu denetim, **inventSum** tablosundaki değerleri düzeltecektir.</span><span class="sxs-lookup"><span data-stu-id="aefbf-196">This check will correct values in the **inventSum** table.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aefbf-197">Kodu ortam için gereken şekilde dikkatle düzenlemenizi, test ortamında test etmenizi ve kodu üretim ortamında çalıştırmadan önce sonuçta elde edilen verileri denetlemenizi önemle tavsiye ederiz.</span><span class="sxs-lookup"><span data-stu-id="aefbf-197">We strongly recommend that you carefully edit the script as required for your environment, test it in a test environment, and then check the resulting data before you run the script in a production environment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]