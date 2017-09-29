---
title: "Rapor tasarımcısında rapor bileşenlerini düzenlemek"
description: "Yapı taşları tasarlayıp rapor oluşturduktan sonra bu nesneleri düzenlemeniz kullanıcıların bunları bulmasını kolaylaştırmaya yardımcı olur. Bu makalede varolan raporların, yapı taşlarının ve nesnelerin rapor tasarımcısında nasıl düzenleneceği açıklanmaktadır."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: fade9e2acdb94daa6a908d949c578fd7ed439882
ms.contentlocale: tr-tr
ms.lasthandoff: 07/18/2017

---

# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="aac97-104">Rapor tasarımcısında rapor bileşenlerini düzenlemek</span><span class="sxs-lookup"><span data-stu-id="aac97-104">Organize report components in report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="aac97-105">Yapı taşları tasarlayıp rapor oluşturduktan sonra bu nesneleri düzenlemeniz kullanıcıların bunları bulmasını kolaylaştırmaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="aac97-105">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="aac97-106">Bu makalede varolan raporların, yapı taşlarının ve nesnelerin rapor tasarımcısında nasıl düzenleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="aac97-106">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="aac97-107">Klasörleri, raporları, yapı taşlarını ve diğer nesneleri rapor tasarımcısında dosyalarınızı düzenlemenize yardımcı olması için yeniden adlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aac97-107">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="aac97-108">Yeniden adlandırdığınız nesne türüne bağlı olarak, o nesneyle ilişkileri güncelleştirmek gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="aac97-108">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="aac97-109">Rapor Tasarımcısı'nda bir klasörü veya yapı taşını yeniden adlandırma</span><span class="sxs-lookup"><span data-stu-id="aac97-109">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="aac97-110">Rapor Tasarımcısı'nda, klasörleri, rapor tanımlarını, satır tanımlarını, sütun tanımları ve raporlama ağaç tanımlarını yeniden adlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aac97-110">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span> <span data-ttu-id="aac97-111">**Not:** Bir yapı taşını yeniden adlandırdığınızda bu yapı taşını kullanan tüm raporlama tanımlarını güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="aac97-111">**Note:** When you rename a building block, you must update any reporting definitions that use the building block.</span></span> <span data-ttu-id="aac97-112">Aksi halde, yeni bir rapor oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="aac97-112">Otherwise, a new report can't be generated.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="aac97-113">Rapor Tasarımcısı'nda bir klasörü veya yapı taşını yeniden adlandırma</span><span class="sxs-lookup"><span data-stu-id="aac97-113">Rename a folder or building block in Report Designer</span></span>

1.  <span data-ttu-id="aac97-114">Rapor Tasarımcısı'nda, klasörü veya yeniden adlandırılacak nesneyi bulmak için gezinti bölmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="aac97-114">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2.  <span data-ttu-id="aac97-115">Klasör veya nesneyi sağ tıklatın ve ardından **Yeniden adlandır** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aac97-115">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="aac97-116">Gezinti bölmesinde **Ad** alanı kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="aac97-116">The **Name** field in the navigation pane becomes available.</span></span>
3.  <span data-ttu-id="aac97-117">Yeni bir ad yazın ve sonra Enter tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="aac97-117">Type a new name, and then press Enter.</span></span>
4.  <span data-ttu-id="aac97-118">Yapı taşı bir satır tanımı, sütun tanımı veya raporlama ağacı tanımı ise, bununla ilişkili diğer yapı taşlarını güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="aac97-118">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="aac97-119">3. adımda yeniden adlandırdığınız yapı taşına sağ tıklayın, **İlişkiler** seçeneğini seçin ve sonra güncelleştirmek için listeden bir öğe seçin.</span><span class="sxs-lookup"><span data-stu-id="aac97-119">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5.  <span data-ttu-id="aac97-120">Tüm ilişkili öğeleri güncelleştirilene kadar 4. adımı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="aac97-120">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="aac97-121">Rapor gruplarını oluşturmak ve yönetmek</span><span class="sxs-lookup"><span data-stu-id="aac97-121">Create and manage report groups</span></span>
<span data-ttu-id="aac97-122">Aynı anda birden çok rapor oluşturmak için rapor tanımlarını gruplandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aac97-122">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="aac97-123">Rapor gruplarını oluşturma, değiştirme, silme ve oluşturma için tasarımcı veya yönetici rolüne sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="aac97-123">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="aac97-124">Oluşturucu rolüne sahip kullanıcılar rapor grupları oluşturabilir ve ayrıca rapor grupları için kullanıcı rapor tanımlarını değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="aac97-124">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="aac97-125">Rapor grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="aac97-125">Create a report group</span></span>

1.  <span data-ttu-id="aac97-126">Rapor Tasarımcısı'nda gezinme bölmesinde **Rapor Grupları** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aac97-126">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="aac97-127">**Dosya** menüsünde, **Yeni** &gt; **Rapor Grubu Tanımı**'na tıklayarak görüntüleyici penceresinde yeni bir rapor grubu açın.</span><span class="sxs-lookup"><span data-stu-id="aac97-127">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="aac97-128">Alternatif olarak, araç çubuğundaki **Rapor Grubu** düğmesine ![Rapor Grubu](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Rapor Grubu") tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aac97-128">Alternatively, click the **Report Group** button ![Report Group](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Report Group") on the toolbar.</span></span>
3.  <span data-ttu-id="aac97-129">**Rapor Grubu** sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aac97-129">Click the **Report Group** tab.</span></span> <span data-ttu-id="aac97-130">Bu raporun oluşturulması için ayrı ayrı rapor tanımlarındaki bilgileri geçersiz kılmak için **Tek tek rapor tanımlarından şirket, ayrıntı ve tarih ayarlarını geçersiz kıl** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="aac97-130">To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="aac97-131">Şirket adı, ayrıntı düzeyi, geçici ayar ve tarih bilgileri otomatik olarak girilir ancak güncelleştirmeleri yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aac97-131">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4.  <span data-ttu-id="aac97-132">Raporlama para birimlerini gösteren birden çok rapor oluşturmak için **Tüm raporlama para birimlerini dahil et** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="aac97-132">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="aac97-133">Bundan sonra, raporu görüntülediğinizde Web Görüntüleyicisi üzerinde **Para** düğmesine tıklayarak birden çok görünüme erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aac97-133">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5.  <span data-ttu-id="aac97-134">**Grup içindeki raporlar** alanında, **Ekle** öğesine tıklayarak raporları rapor grubuna eklemek için seçin.</span><span class="sxs-lookup"><span data-stu-id="aac97-134">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="aac97-135">**Ekle** iletişim kutusunda birden fazla rapor seçmek için raporları seçerken Ctrl tuşunu basılı tutun.</span><span class="sxs-lookup"><span data-stu-id="aac97-135">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="aac97-136">Rapor seçme işlemini tamamladığınızda **Tamam** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aac97-136">When you've finished selecting reports, click **OK**.</span></span>
6.  <span data-ttu-id="aac97-137">Yeni rapor grubu kaydetmek için **Dosya** &gt; **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aac97-137">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="aac97-138">Bir rapor grubu değiştirin</span><span class="sxs-lookup"><span data-stu-id="aac97-138">Modify a report group</span></span>

1.  <span data-ttu-id="aac97-139">Rapor Tasarımcısı'nda gezinme bölmesinde **Rapor Grupları** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aac97-139">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="aac97-140">Rapor grubunu değiştirmek için çift tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aac97-140">Double-click the report group to modify.</span></span>
3.  <span data-ttu-id="aac97-141">**Rapor Grubu** sekmesinde istediğiniz değişiklikleri yapın.</span><span class="sxs-lookup"><span data-stu-id="aac97-141">On the **Report Group** tab, make the changes that you want.</span></span>
4.  <span data-ttu-id="aac97-142">Değiştirilen rapor grubunu kaydetmek için **Dosya** menüsünde **Kaydet**'e tıklayın veya araç çubuğunda **Kaydet** düğmesine ![Kaydet](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Kaydet")  tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aac97-142">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Save") on the toolbar.</span></span>

<span data-ttu-id="aac97-143">**Not:** Belirli aralıklarla oluşturulacak zamanlanmış raporlarınız varsa, bu ayarları geçersiz kılabilir ve hemen bir rapor üretebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aac97-143">**Note:** If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="aac97-144">Bir rapor grup raporu oluştur</span><span class="sxs-lookup"><span data-stu-id="aac97-144">Generate a report group report</span></span>

1.  <span data-ttu-id="aac97-145">Rapor Tasarımcısı'nda gezinme bölmesinde **Rapor Grupları** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aac97-145">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="aac97-146">Oluşturmak için rapor grubunu açın.</span><span class="sxs-lookup"><span data-stu-id="aac97-146">Open the report group to generate.</span></span>
3.  <span data-ttu-id="aac97-147">Rapor oluşturmak için **Rapor Oluştur** düğmesine ![Rapor Oluştur](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Rapor Oluştur") tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aac97-147">Click the **Generate Report** button ![Generate Report](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="aac97-148">Bir rapor grubu silme</span><span class="sxs-lookup"><span data-stu-id="aac97-148">Delete a report group</span></span>

1.  <span data-ttu-id="aac97-149">Rapor Tasarımcısı'nda gezinme bölmesinde **Rapor Grupları** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aac97-149">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="aac97-150">Silinecek rapor grubuna sağ tıklayın ve sonra **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="aac97-150">Right-click the report group to delete, and then select **Delete**.</span></span>
3.  <span data-ttu-id="aac97-151">Onay iletisi göründüğünde **Evet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aac97-151">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="aac97-152">Rapor Grubu sekmesi denetimleri</span><span class="sxs-lookup"><span data-stu-id="aac97-152">Report Group tab controls</span></span>
<span data-ttu-id="aac97-153">Aşağıdaki tablo **Rapor Grubu** sekmesindeki denetimlerle ilgili açıklamalar sağlar.</span><span class="sxs-lookup"><span data-stu-id="aac97-153">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aac97-154">Kontrol</span><span class="sxs-lookup"><span data-stu-id="aac97-154">Control</span></span></th>
<th><span data-ttu-id="aac97-155">Açıklama</span><span class="sxs-lookup"><span data-stu-id="aac97-155">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aac97-156">Şirket, ayrıntı ve tek tek rapor tanımları tarih ayarlarını geçersiz kıl</span><span class="sxs-lookup"><span data-stu-id="aac97-156">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="aac97-157">Yalnızca bu raporları oluşturmak için bu rapor grubu raporlarda tek tek rapor tanımları geçersiz kılmak için bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="aac97-157">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aac97-158">Şirket adı</span><span class="sxs-lookup"><span data-stu-id="aac97-158">Company name</span></span></td>
<td><span data-ttu-id="aac97-159">Raporlar için kullanılacak bir şirket seçin.</span><span class="sxs-lookup"><span data-stu-id="aac97-159">Select the company to use for the reports.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aac97-160">Ayrıntı düzeyi</span><span class="sxs-lookup"><span data-stu-id="aac97-160">Detail level</span></span></td>
<td><span data-ttu-id="aac97-161">Raporların içereceği ayrıntı düzeyini belirtin.</span><span class="sxs-lookup"><span data-stu-id="aac97-161">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="aac97-162"><strong>Finansal</strong>− Yüksek düzeyde özet raporu.</span><span class="sxs-lookup"><span data-stu-id="aac97-162"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="aac97-163">Raporlama ağacıyla eklenen hesaplar ve boyutlar dışında, hesaplarda ve boyutlarda ayrıntıya gidemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="aac97-163">You can't drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="aac97-164"><strong>Finans &amp; Hesap</strong> - Üst düzey bir özet ve hesap ayrıntıları içeren bir rapor.</span><span class="sxs-lookup"><span data-stu-id="aac97-164"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="aac97-165"><strong>Finans, Hesap &amp; İşlem</strong> - Üst düzey bir özet ve işlem ayrıntıları içeren bir rapor.</span><span class="sxs-lookup"><span data-stu-id="aac97-165"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aac97-166">Provizyon</span><span class="sxs-lookup"><span data-stu-id="aac97-166">Provisional</span></span></td>
<td><span data-ttu-id="aac97-167">Raporların içereceği etkinlik türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="aac97-167">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="aac97-168"><strong>Yalnızca nakledilen etkinlik</strong> − Yalnızca finansal verilere nakledilen hareketleri ve bakiyeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="aac97-168"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="aac97-169"><strong> Nakledilen ve nakledilmeyen etkinlik</strong> − Finansal verilere girilen ve nakledilen hareketlerin ve bakiyelerin tümünü içerir.</span><span class="sxs-lookup"><span data-stu-id="aac97-169"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="aac97-170"><strong>Yalnızca nakledilmeyen etkinlik</strong> − Yalnızca finansal verilere girilen ama henüz nakledilmeyen hareketleri içerir.</span><span class="sxs-lookup"><span data-stu-id="aac97-170"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aac97-171">Tüm raporlama para birimlerini dahil et</span><span class="sxs-lookup"><span data-stu-id="aac97-171">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="aac97-172">Microsoft Dynamics ERP sisteminizde yapılandırılan tüm ilave raporlama para birimleri burada listelenir.</span><span class="sxs-lookup"><span data-stu-id="aac97-172">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="aac97-173">Belirtilen para birimlerinde ek rapor oluşturmak için bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="aac97-173">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="aac97-174">Bu raporları Web Görüntüleyicisi'nde görüntülemek için <strong>Para Birimi</strong> düğmesine tıklayın ve bir para birimi seçin.</span><span class="sxs-lookup"><span data-stu-id="aac97-174">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aac97-175">Rapor tanımı ile kaydedilmemiş tarih bilgileri</span><span class="sxs-lookup"><span data-stu-id="aac97-175">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="aac97-176">Esas dönem</span><span class="sxs-lookup"><span data-stu-id="aac97-176">Base period</span></span></li>
<li><span data-ttu-id="aac97-177">Esas yıl</span><span class="sxs-lookup"><span data-stu-id="aac97-177">Base year</span></span></li>
<li><span data-ttu-id="aac97-178">Kapsanan dönem</span><span class="sxs-lookup"><span data-stu-id="aac97-178">Period covered</span></span></li>
</ul>
<span data-ttu-id="aac97-179">Yalnızca varsayılan esas dönem ayarları rapor tanımı ile kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="aac97-179">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aac97-180">Rapor tanımı ile kaydedilmiş tarih bilgileri</span><span class="sxs-lookup"><span data-stu-id="aac97-180">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="aac97-181">Rapor tarihi</span><span class="sxs-lookup"><span data-stu-id="aac97-181">Report date</span></span></li>
<li><span data-ttu-id="aac97-182">Varsayılan esas dönem</span><span class="sxs-lookup"><span data-stu-id="aac97-182">Default base period</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aac97-183">Grupta raporlar</span><span class="sxs-lookup"><span data-stu-id="aac97-183">Reports in group</span></span></td>
<td><span data-ttu-id="aac97-184">Rapor grubunda raporları ekleyin, kaldırın ve yeniden sıralayın.</span><span class="sxs-lookup"><span data-stu-id="aac97-184">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="aac97-185">Rapor tanımlarını rapor grubuna eklemek için rapor grubunu çift tıklatarak açın ve ardından <strong>Ekle</strong>'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aac97-185">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="aac97-186">Rapor grubuna eklenecek raporları seçin ve sonra <strong>Tamam</strong>'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="aac97-186">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="aac97-187">Bir raporu rapor grubundan kaldırmak için onu seçin ve sonra<strong>Kaldır</strong>'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aac97-187">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="aac97-188">Raporların üretilme sırasını değiştirmek için listeden bir rapor seçin ve sonra <strong>Yukarı taşı</strong> veya <strong>Aşağıya taşı</strong>'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aac97-188">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="aac97-189">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="aac97-189">See also</span></span>
--------

[<span data-ttu-id="aac97-190">Mali raporlama</span><span class="sxs-lookup"><span data-stu-id="aac97-190">Financial reporting</span></span>](financial-reporting-intro.md)




