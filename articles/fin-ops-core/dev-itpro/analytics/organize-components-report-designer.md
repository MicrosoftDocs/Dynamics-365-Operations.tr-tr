---
title: Rapor tasarımcısında rapor bileşenlerini düzenlemek
description: Yapı taşları tasarlayıp rapor oluşturduktan sonra bu nesneleri düzenlemeniz kullanıcıların bunları bulmasını kolaylaştırmaya yardımcı olur. Bu makalede varolan raporların, yapı taşlarının ve nesnelerin rapor tasarımcısında nasıl düzenleneceği açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4a4733dc4da7a8713ac7ddec5c96ae18c91edc18
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185302"
---
# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="64d87-104">Rapor tasarımcısında rapor bileşenlerini düzenlemek</span><span class="sxs-lookup"><span data-stu-id="64d87-104">Organize report components in report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64d87-105">Yapı taşları tasarlayıp rapor oluşturduktan sonra bu nesneleri düzenlemeniz kullanıcıların bunları bulmasını kolaylaştırmaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="64d87-105">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="64d87-106">Bu makalede varolan raporların, yapı taşlarının ve nesnelerin rapor tasarımcısında nasıl düzenleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="64d87-106">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="64d87-107">Klasörleri, raporları, yapı taşlarını ve diğer nesneleri rapor tasarımcısında dosyalarınızı düzenlemenize yardımcı olması için yeniden adlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64d87-107">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="64d87-108">Yeniden adlandırdığınız nesne türüne bağlı olarak, o nesneyle ilişkileri güncelleştirmek gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="64d87-108">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="64d87-109">Rapor Tasarımcısı'nda bir klasörü veya yapı taşını yeniden adlandırma</span><span class="sxs-lookup"><span data-stu-id="64d87-109">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="64d87-110">Rapor Tasarımcısı'nda, klasörler, rapor tanımları, satır tanımları, sütun tanımları ve raporlama ağacı tanımlarını yeniden adlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64d87-110">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="64d87-111">Rapor Tasarımcısı'nda bir klasörü veya yapı taşını yeniden adlandırma</span><span class="sxs-lookup"><span data-stu-id="64d87-111">Rename a folder or building block in Report Designer</span></span>

1. <span data-ttu-id="64d87-112">Rapor Tasarımcısı'nda, yeniden adlandırılacak klasörü veya nesneyi bulmak için gezinti bölmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="64d87-112">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2. <span data-ttu-id="64d87-113">Klasöre veya nesneye sağ tıklayın ve ardından **Yeniden Adlandır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64d87-113">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="64d87-114">Gezinti bölmesindeki **Ad** alanı kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="64d87-114">The **Name** field in the navigation pane becomes available.</span></span>
3. <span data-ttu-id="64d87-115">Yeni bir ad yazın ve ardından Enter'a basın.</span><span class="sxs-lookup"><span data-stu-id="64d87-115">Type a new name, and then press Enter.</span></span>
4. <span data-ttu-id="64d87-116">Yapı taşı satır tanımı, sütun tanımı veya raporlama ağacı tanımıysa yapı taşıyla ilişkili diğer yapı taşlarını güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="64d87-116">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="64d87-117">3. adımda yeniden adlandırdığınız yapı taşına sağ tıklayın, **İlişkiler**'i seçin ve ardından güncelleştirmek için listeden bir madde seçin.</span><span class="sxs-lookup"><span data-stu-id="64d87-117">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5. <span data-ttu-id="64d87-118">Tüm ilişkili maddeler güncelleştirilene kadar 4. adımı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="64d87-118">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="64d87-119">Rapor grupları oluşturma ve yönetme</span><span class="sxs-lookup"><span data-stu-id="64d87-119">Create and manage report groups</span></span>
<span data-ttu-id="64d87-120">Aynı anda birden fazla rapor oluşturmak için rapor tanımlarını gruplandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64d87-120">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="64d87-121">Rapor gruplarını değiştirmek, silmek ve oluşturmak için, tasarımcı veya yönetici rolüne sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="64d87-121">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="64d87-122">Oluşturan rolüne sahip kullanıcılar rapor grupları oluşturabilir ve aynı zamanda rapor gruplarına ilişkin kullanıcı rapor tanımları ayarını değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="64d87-122">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="64d87-123">Rapor grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="64d87-123">Create a report group</span></span>

1. <span data-ttu-id="64d87-124">Rapor Tasarımcısı'nda gezinme bölmesinde **Rapor Grupları** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64d87-124">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="64d87-125">**Dosya** menüsünde, **Yeni** &gt; **Rapor Grubu Tanımı**'na tıklayarak görüntüleyici penceresinde yeni bir rapor grubu açın.</span><span class="sxs-lookup"><span data-stu-id="64d87-125">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="64d87-126">Alternatif olarak, araç çubuğundaki **Rapor Grubu** düğmesine ![Rapor Grubu](media/report-group.gif "Rapor Grubu") tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64d87-126">Alternatively, click the **Report Group** button ![Report Group](media/report-group.gif "Report Group") on the toolbar.</span></span>
3. <span data-ttu-id="64d87-127">**Rapor Grubu** sekmesine tıklayın. Bu raporun oluşturulması için tek rapor tanımlarındaki bilgileri geçersiz kılmak üzere, **Tek rapor tanımlarındaki şirket, ayrıntı ve tarih ayarlarını geçersiz kıl** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="64d87-127">Click the **Report Group** tab. To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="64d87-128">Şirket adı, ayrıntı düzeyi, geçici ayar ve tarih bilgileri otomatik olarak girilir, ancak güncelleştirmeler yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64d87-128">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4. <span data-ttu-id="64d87-129">Raporlama para birimlerini gösteren birden fazla rapor oluşturmak için **Tüm raporlama para birimlerini ekle** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="64d87-129">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="64d87-130">Böylece raporu görüntülediğinizde, Web Görüntüleyici'deki **Para Birimi** düğmesine tıklayarak birden fazla görünüme erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64d87-130">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5. <span data-ttu-id="64d87-131">Rapor grubuna eklemek üzere raporları seçmek için **Gruptaki raporlar** alanında **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64d87-131">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="64d87-132">**Ekle** iletişim kutusunda birden fazla rapor seçmek için, raporları seçerken Ctrl tuşunu basılı tutun.</span><span class="sxs-lookup"><span data-stu-id="64d87-132">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="64d87-133">Rapor seçme işlemini tamamladığınızda **Tamam** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64d87-133">When you've finished selecting reports, click **OK**.</span></span>
6. <span data-ttu-id="64d87-134">Yeni rapor grubu kaydetmek için **Dosya** &gt; **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64d87-134">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="64d87-135">Bir rapor grubu değiştirin</span><span class="sxs-lookup"><span data-stu-id="64d87-135">Modify a report group</span></span>

1. <span data-ttu-id="64d87-136">Rapor Tasarımcısı'nda gezinme bölmesinde **Rapor Grupları** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64d87-136">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="64d87-137">Değiştirilecek rapor grubuna çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64d87-137">Double-click the report group to modify.</span></span>
3. <span data-ttu-id="64d87-138">**Rapor Grubu** sekmesinde, istediğiniz değişiklikleri yapın.</span><span class="sxs-lookup"><span data-stu-id="64d87-138">On the **Report Group** tab, make the changes that you want.</span></span>
4. <span data-ttu-id="64d87-139">Değiştirilen rapor grubunu kaydetmek için **Dosya** menüsünde **Kaydet**'e tıklayın veya araç çubuğunda **Kaydet** düğmesine ![Kaydet](media/save.gif "Kaydet")  tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64d87-139">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](media/save.gif "Save") on the toolbar.</span></span>

> <span data-ttu-id="64d87-140">[NOT] Ayarlanan aralıklarda oluşturulmaları için planlanan raporlarınız varsa bu ayarları geçersiz kılarak hemen bir rapor oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64d87-140">[NOTE] If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="64d87-141">Rapor grubu raporu oluşturma</span><span class="sxs-lookup"><span data-stu-id="64d87-141">Generate a report group report</span></span>

1. <span data-ttu-id="64d87-142">Rapor Tasarımcısı'ndaki gezinti bölmesinde **Rapor Grupları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64d87-142">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="64d87-143">Oluşturmak için rapor grubunu açın.</span><span class="sxs-lookup"><span data-stu-id="64d87-143">Open the report group to generate.</span></span>
3. <span data-ttu-id="64d87-144">Rapor oluşturmak için **Rapor Oluştur** düğmesine ![Rapor Oluştur](media/generate-report.gif "Rapor Oluştur") tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64d87-144">Click the **Generate Report** button ![Generate Report](media/generate-report.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="64d87-145">Bir rapor grubunu silme</span><span class="sxs-lookup"><span data-stu-id="64d87-145">Delete a report group</span></span>

1. <span data-ttu-id="64d87-146">Rapor Tasarımcısı'ndaki gezinti bölmesinde **Rapor Grupları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64d87-146">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="64d87-147">Silinecek rapor grubuna sağ tıklayın ve ardından **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="64d87-147">Right-click the report group to delete, and then select **Delete**.</span></span>
3. <span data-ttu-id="64d87-148">Bir onay mesajı göründüğünde, **Evet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64d87-148">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="64d87-149">Rapor Grubu sekmesi kontrolleri</span><span class="sxs-lookup"><span data-stu-id="64d87-149">Report Group tab controls</span></span>
<span data-ttu-id="64d87-150">Aşağıdaki tabloda **Rapor Grubu** sekmesindeki kontroller açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="64d87-150">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="64d87-151">Kontrol</span><span class="sxs-lookup"><span data-stu-id="64d87-151">Control</span></span></th>
<th><span data-ttu-id="64d87-152">Açıklama</span><span class="sxs-lookup"><span data-stu-id="64d87-152">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64d87-153">Tek rapor tanımlarındaki şirket, ayrıntı ve tarih ayarlarını geçersiz kıl</span><span class="sxs-lookup"><span data-stu-id="64d87-153">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="64d87-154">Yalnızca bu raporların oluşturulması için bu rapor grubundaki raporların tek rapor tanımlarını geçersiz kılmak üzere bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="64d87-154">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64d87-155">Şirket adı</span><span class="sxs-lookup"><span data-stu-id="64d87-155">Company name</span></span></td>
<td><span data-ttu-id="64d87-156">Raporlar için kullanmak üzere şirketi seçin.</span><span class="sxs-lookup"><span data-stu-id="64d87-156">Select the company to use for the reports.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64d87-157">Ayrıntı düzeyi</span><span class="sxs-lookup"><span data-stu-id="64d87-157">Detail level</span></span></td>
<td><span data-ttu-id="64d87-158">Raporların içerdiği ayrıntı düzeyini belirtin.</span><span class="sxs-lookup"><span data-stu-id="64d87-158">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="64d87-159"><strong>Mali</strong>: Üst düzey özet rapor.</span><span class="sxs-lookup"><span data-stu-id="64d87-159"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="64d87-160">Bir raporlama ağacı aracılığıyla eklenen hesaplar ve boyutlar hariç, hesaplar ve boyutlarda ayrıntıya inemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="64d87-160">You can&#39;t drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="64d87-161"><strong>Finans &amp; Hesap</strong> - Üst düzey bir özet ve hesap ayrıntıları içeren bir rapor.</span><span class="sxs-lookup"><span data-stu-id="64d87-161"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="64d87-162"><strong>Finans, Hesap &amp; İşlem</strong> - Üst düzey bir özet ve işlem ayrıntıları içeren bir rapor.</span><span class="sxs-lookup"><span data-stu-id="64d87-162"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="64d87-163">Geçici</span><span class="sxs-lookup"><span data-stu-id="64d87-163">Provisional</span></span></td>
<td><span data-ttu-id="64d87-164">Raporların içerdiği faaliyet türlerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="64d87-164">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="64d87-165"><strong>Yalnızca deftere nakledilmiş faaliyet</strong>: Yalnızca mali verilerinize nakledilen hareketleri ve bakiyeleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="64d87-165"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="64d87-166"><strong>Deftere nakledilmiş ve nakledilmemiş faaliyet</strong>: Mali verilerinize girilip nakledilen tüm hareketleri ve bakiyeleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="64d87-166"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="64d87-167"><strong>Deftere nakledilmemiş faaliyet</strong>: Yalnızca mali verilerinize girilmiş ancak henüz nakledilmemiş hareketleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="64d87-167"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="64d87-168">Tüm raporlama para birimlerini ekle</span><span class="sxs-lookup"><span data-stu-id="64d87-168">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="64d87-169">Microsoft Dynamics ERP sisteminizde yapılandırılan tüm ek raporlama para birimleri burada belirtilir.</span><span class="sxs-lookup"><span data-stu-id="64d87-169">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="64d87-170">Belirtilen para birimlerinde ek raporlar oluşturmak için bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="64d87-170">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="64d87-171">Bu raporları Web Görüntüleyici'de görüntülemek için <strong>Para Birimi</strong> düğmesine tıklayın ve ardından bir para birimi seçin.</span><span class="sxs-lookup"><span data-stu-id="64d87-171">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64d87-172">Tarih bilgileri rapor tanımına kaydedilmedi</span><span class="sxs-lookup"><span data-stu-id="64d87-172">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="64d87-173">Esas dönem</span><span class="sxs-lookup"><span data-stu-id="64d87-173">Base period</span></span></li>
<li><span data-ttu-id="64d87-174">Esas yıl</span><span class="sxs-lookup"><span data-stu-id="64d87-174">Base year</span></span></li>
<li><span data-ttu-id="64d87-175">Kapsanan dönemler</span><span class="sxs-lookup"><span data-stu-id="64d87-175">Period covered</span></span></li>
</ul>
<span data-ttu-id="64d87-176">Rapor tanımıyla yalnızca varsayılan esas dönem ayarları kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="64d87-176">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64d87-177">Tarih bilgileri rapor tanımına kaydedildi</span><span class="sxs-lookup"><span data-stu-id="64d87-177">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="64d87-178">Rapor tarihi</span><span class="sxs-lookup"><span data-stu-id="64d87-178">Report date</span></span></li>
<li><span data-ttu-id="64d87-179">Varsayılan esas dönem</span><span class="sxs-lookup"><span data-stu-id="64d87-179">Default base period</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="64d87-180">Gruptaki raporlar</span><span class="sxs-lookup"><span data-stu-id="64d87-180">Reports in group</span></span></td>
<td><span data-ttu-id="64d87-181">Rapor grubuna rapor ekleyin, bunları kaldırın ve yeniden sıralayın.</span><span class="sxs-lookup"><span data-stu-id="64d87-181">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="64d87-182">Rapor grubuna rapor tanımları eklemek için, açmak üzere rapor grubuna çift tıklayın ve ardından <strong>Ekle</strong>'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64d87-182">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="64d87-183">Rapor grubuna eklenecek raporları seçin ve ardından <strong>Tamam</strong>'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64d87-183">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="64d87-184">Bir raporu rapor grubundan kaldırmak için, raporu seçin ve ardından <strong>Kaldır</strong>'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64d87-184">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="64d87-185">Raporların oluşturulduğu sırayı değiştirmek için, listeden bir rapor seçin ve ardından <strong>Yukarı taşı</strong>'ya veya <strong>Aşağı taşı</strong>'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64d87-185">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="64d87-186">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="64d87-186">Additional resources</span></span>

[<span data-ttu-id="64d87-187">Mali raporlama</span><span class="sxs-lookup"><span data-stu-id="64d87-187">Financial reporting</span></span>](financial-reporting-intro.md)
