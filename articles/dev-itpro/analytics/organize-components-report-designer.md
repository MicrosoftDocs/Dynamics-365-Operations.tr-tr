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
ms.search.scope: Core, Operations
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7207febc58dbab1df5551ae0f74ad74d9ced8e56
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---

# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="bcf6b-104">Rapor tasarımcısında rapor bileşenlerini düzenlemek</span><span class="sxs-lookup"><span data-stu-id="bcf6b-104">Organize report components in report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bcf6b-105">Yapı taşları tasarlayıp rapor oluşturduktan sonra bu nesneleri düzenlemeniz kullanıcıların bunları bulmasını kolaylaştırmaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-105">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="bcf6b-106">Bu makalede varolan raporların, yapı taşlarının ve nesnelerin rapor tasarımcısında nasıl düzenleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-106">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="bcf6b-107">Klasörleri, raporları, yapı taşlarını ve diğer nesneleri rapor tasarımcısında dosyalarınızı düzenlemenize yardımcı olması için yeniden adlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-107">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="bcf6b-108">Yeniden adlandırdığınız nesne türüne bağlı olarak, o nesneyle ilişkileri güncelleştirmek gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-108">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="bcf6b-109">Rapor Tasarımcısı'nda bir klasörü veya yapı taşını yeniden adlandırma</span><span class="sxs-lookup"><span data-stu-id="bcf6b-109">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="bcf6b-110">Rapor Tasarımcısı'nda, klasörler, rapor tanımları, satır tanımları, sütun tanımları ve raporlama ağacı tanımlarını yeniden adlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-110">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span> <span data-ttu-id="bcf6b-111">**Not:** Bir yapı taşını yeniden adlandırdığınızda, yapı taşını kullanan her türlü raporlama tanımını güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-111">**Note:** When you rename a building block, you must update any reporting definitions that use the building block.</span></span> <span data-ttu-id="bcf6b-112">Aksi takdirde, yeni bir rapor oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-112">Otherwise, a new report can't be generated.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="bcf6b-113">Rapor Tasarımcısı'nda bir klasörü veya yapı taşını yeniden adlandırma</span><span class="sxs-lookup"><span data-stu-id="bcf6b-113">Rename a folder or building block in Report Designer</span></span>

1.  <span data-ttu-id="bcf6b-114">Rapor Tasarımcısı'nda, yeniden adlandırılacak klasörü veya nesneyi bulmak için gezinti bölmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-114">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2.  <span data-ttu-id="bcf6b-115">Klasöre veya nesneye sağ tıklayın ve ardından **Yeniden Adlandır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-115">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="bcf6b-116">Gezinti bölmesindeki **Ad** alanı kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-116">The **Name** field in the navigation pane becomes available.</span></span>
3.  <span data-ttu-id="bcf6b-117">Yeni bir ad yazın ve ardından Enter'a basın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-117">Type a new name, and then press Enter.</span></span>
4.  <span data-ttu-id="bcf6b-118">Yapı taşı satır tanımı, sütun tanımı veya raporlama ağacı tanımıysa yapı taşıyla ilişkili diğer yapı taşlarını güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-118">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="bcf6b-119">3. adımda yeniden adlandırdığınız yapı taşına sağ tıklayın, **İlişkiler**'i seçin ve ardından güncelleştirmek için listeden bir madde seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-119">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5.  <span data-ttu-id="bcf6b-120">Tüm ilişkili maddeler güncelleştirilene kadar 4. adımı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-120">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="bcf6b-121">Rapor grupları oluşturma ve yönetme</span><span class="sxs-lookup"><span data-stu-id="bcf6b-121">Create and manage report groups</span></span>
<span data-ttu-id="bcf6b-122">Aynı anda birden fazla rapor oluşturmak için rapor tanımlarını gruplandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-122">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="bcf6b-123">Rapor gruplarını değiştirmek, silmek ve oluşturmak için, tasarımcı veya yönetici rolüne sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-123">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="bcf6b-124">Oluşturan rolüne sahip kullanıcılar rapor grupları oluşturabilir ve aynı zamanda rapor gruplarına ilişkin kullanıcı rapor tanımları ayarını değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-124">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="bcf6b-125">Rapor grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="bcf6b-125">Create a report group</span></span>

1.  <span data-ttu-id="bcf6b-126">Rapor Tasarımcısı'nda gezinme bölmesinde **Rapor Grupları** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-126">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="bcf6b-127">**Dosya** menüsünde, **Yeni** &gt; **Rapor Grubu Tanımı**'na tıklayarak görüntüleyici penceresinde yeni bir rapor grubu açın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-127">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="bcf6b-128">Alternatif olarak, araç çubuğundaki **Rapor Grubu** düğmesine ![Rapor Grubu](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Rapor Grubu") tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-128">Alternatively, click the **Report Group** button ![Report Group](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Report Group") on the toolbar.</span></span>
3.  <span data-ttu-id="bcf6b-129">**Rapor Grubu** sekmesine tıklayın. Bu raporun oluşturulması için tek rapor tanımlarındaki bilgileri geçersiz kılmak üzere, **Tek rapor tanımlarındaki şirket, ayrıntı ve tarih ayarlarını geçersiz kıl** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-129">Click the **Report Group** tab. To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="bcf6b-130">Şirket adı, ayrıntı düzeyi, geçici ayar ve tarih bilgileri otomatik olarak girilir, ancak güncelleştirmeler yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-130">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4.  <span data-ttu-id="bcf6b-131">Raporlama para birimlerini gösteren birden fazla rapor oluşturmak için **Tüm raporlama para birimlerini ekle** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-131">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="bcf6b-132">Böylece raporu görüntülediğinizde, Web Görüntüleyici'deki **Para Birimi** düğmesine tıklayarak birden fazla görünüme erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-132">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5.  <span data-ttu-id="bcf6b-133">Rapor grubuna eklemek üzere raporları seçmek için **Gruptaki raporlar** alanında **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-133">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="bcf6b-134">**Ekle** iletişim kutusunda birden fazla rapor seçmek için, raporları seçerken Ctrl tuşunu basılı tutun.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-134">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="bcf6b-135">Rapor seçme işlemini tamamladığınızda **Tamam** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-135">When you've finished selecting reports, click **OK**.</span></span>
6.  <span data-ttu-id="bcf6b-136">Yeni rapor grubu kaydetmek için **Dosya** &gt; **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-136">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="bcf6b-137">Bir rapor grubu değiştirin</span><span class="sxs-lookup"><span data-stu-id="bcf6b-137">Modify a report group</span></span>

1.  <span data-ttu-id="bcf6b-138">Rapor Tasarımcısı'nda gezinme bölmesinde **Rapor Grupları** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-138">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="bcf6b-139">Değiştirilecek rapor grubuna çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-139">Double-click the report group to modify.</span></span>
3.  <span data-ttu-id="bcf6b-140">**Rapor Grubu** sekmesinde, istediğiniz değişiklikleri yapın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-140">On the **Report Group** tab, make the changes that you want.</span></span>
4.  <span data-ttu-id="bcf6b-141">Değiştirilen rapor grubunu kaydetmek için **Dosya** menüsünde **Kaydet**'e tıklayın veya araç çubuğunda **Kaydet** düğmesine ![Kaydet](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Kaydet")  tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-141">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Save") on the toolbar.</span></span>

<span data-ttu-id="bcf6b-142">**Not:** Ayarlanan aralıklarda oluşturulmaları için planlı raporlarınız varsa bu ayarları geçersiz kılarak hemen bir rapor oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-142">**Note:** If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="bcf6b-143">Rapor grubu raporu oluşturma</span><span class="sxs-lookup"><span data-stu-id="bcf6b-143">Generate a report group report</span></span>

1.  <span data-ttu-id="bcf6b-144">Rapor Tasarımcısı'ndaki gezinti bölmesinde **Rapor Grupları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-144">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="bcf6b-145">Oluşturmak için rapor grubunu açın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-145">Open the report group to generate.</span></span>
3.  <span data-ttu-id="bcf6b-146">Rapor oluşturmak için **Rapor Oluştur** düğmesine ![Rapor Oluştur](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Rapor Oluştur") tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-146">Click the **Generate Report** button ![Generate Report](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="bcf6b-147">Bir rapor grubunu silme</span><span class="sxs-lookup"><span data-stu-id="bcf6b-147">Delete a report group</span></span>

1.  <span data-ttu-id="bcf6b-148">Rapor Tasarımcısı'ndaki gezinti bölmesinde **Rapor Grupları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-148">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="bcf6b-149">Silinecek rapor grubuna sağ tıklayın ve ardından **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-149">Right-click the report group to delete, and then select **Delete**.</span></span>
3.  <span data-ttu-id="bcf6b-150">Bir onay mesajı göründüğünde, **Evet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-150">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="bcf6b-151">Rapor Grubu sekmesi kontrolleri</span><span class="sxs-lookup"><span data-stu-id="bcf6b-151">Report Group tab controls</span></span>
<span data-ttu-id="bcf6b-152">Aşağıdaki tabloda **Rapor Grubu** sekmesindeki kontroller açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-152">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bcf6b-153">Kontrol</span><span class="sxs-lookup"><span data-stu-id="bcf6b-153">Control</span></span></th>
<th><span data-ttu-id="bcf6b-154">Açıklama</span><span class="sxs-lookup"><span data-stu-id="bcf6b-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bcf6b-155">Tek rapor tanımlarındaki şirket, ayrıntı ve tarih ayarlarını geçersiz kıl</span><span class="sxs-lookup"><span data-stu-id="bcf6b-155">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="bcf6b-156">Yalnızca bu raporların oluşturulması için bu rapor grubundaki raporların tek rapor tanımlarını geçersiz kılmak üzere bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-156">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bcf6b-157">Şirket adı</span><span class="sxs-lookup"><span data-stu-id="bcf6b-157">Company name</span></span></td>
<td><span data-ttu-id="bcf6b-158">Raporlar için kullanmak üzere şirketi seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-158">Select the company to use for the reports.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bcf6b-159">Ayrıntı düzeyi</span><span class="sxs-lookup"><span data-stu-id="bcf6b-159">Detail level</span></span></td>
<td><span data-ttu-id="bcf6b-160">Raporların içerdiği ayrıntı düzeyini belirtin.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-160">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="bcf6b-161"><strong>Mali</strong>: Üst düzey özet rapor.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-161"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="bcf6b-162">Raporlama ağacıyla eklenen hesaplar ve boyutlar dışında, hesaplarda ve boyutlarda ayrıntıya gidemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-162">You can&#39;t drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="bcf6b-163"><strong>Finans &amp; Hesap</strong> - Üst düzey bir özet ve hesap ayrıntıları içeren bir rapor.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-163"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="bcf6b-164"><strong>Finans, Hesap &amp; İşlem</strong> - Üst düzey bir özet ve işlem ayrıntıları içeren bir rapor.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-164"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bcf6b-165">Geçici</span><span class="sxs-lookup"><span data-stu-id="bcf6b-165">Provisional</span></span></td>
<td><span data-ttu-id="bcf6b-166">Raporların içerdiği faaliyet türlerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-166">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="bcf6b-167"><strong>Yalnızca deftere nakledilmiş faaliyet</strong>: Yalnızca mali verilerinize nakledilen hareketleri ve bakiyeleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-167"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="bcf6b-168"><strong>Deftere nakledilmiş ve nakledilmemiş faaliyet</strong>: Mali verilerinize girilip nakledilen tüm hareketleri ve bakiyeleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-168"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="bcf6b-169"><strong>Deftere nakledilmemiş faaliyet</strong>: Yalnızca mali verilerinize girilmiş ancak henüz nakledilmemiş hareketleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-169"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bcf6b-170">Tüm raporlama para birimlerini ekle</span><span class="sxs-lookup"><span data-stu-id="bcf6b-170">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="bcf6b-171">Microsoft Dynamics ERP sisteminizde yapılandırılan tüm ek raporlama para birimleri burada belirtilir.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-171">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="bcf6b-172">Belirtilen para birimlerinde ek raporlar oluşturmak için bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-172">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="bcf6b-173">Bu raporları Web Görüntüleyici'de görüntülemek için <strong>Para Birimi</strong> düğmesine tıklayın ve ardından bir para birimi seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-173">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bcf6b-174">Tarih bilgileri rapor tanımına kaydedilmedi</span><span class="sxs-lookup"><span data-stu-id="bcf6b-174">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="bcf6b-175">Esas dönem</span><span class="sxs-lookup"><span data-stu-id="bcf6b-175">Base period</span></span></li>
<li><span data-ttu-id="bcf6b-176">Esas yıl</span><span class="sxs-lookup"><span data-stu-id="bcf6b-176">Base year</span></span></li>
<li><span data-ttu-id="bcf6b-177">Kapsanan dönemler</span><span class="sxs-lookup"><span data-stu-id="bcf6b-177">Period covered</span></span></li>
</ul>
<span data-ttu-id="bcf6b-178">Rapor tanımıyla yalnızca varsayılan esas dönem ayarları kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-178">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bcf6b-179">Tarih bilgileri rapor tanımına kaydedildi</span><span class="sxs-lookup"><span data-stu-id="bcf6b-179">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="bcf6b-180">Rapor tarihi</span><span class="sxs-lookup"><span data-stu-id="bcf6b-180">Report date</span></span></li>
<li><span data-ttu-id="bcf6b-181">Varsayılan esas dönem</span><span class="sxs-lookup"><span data-stu-id="bcf6b-181">Default base period</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bcf6b-182">Gruptaki raporlar</span><span class="sxs-lookup"><span data-stu-id="bcf6b-182">Reports in group</span></span></td>
<td><span data-ttu-id="bcf6b-183">Rapor grubuna rapor ekleyin, bunları kaldırın ve yeniden sıralayın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-183">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="bcf6b-184">Rapor grubuna rapor tanımları eklemek için, açmak üzere rapor grubuna çift tıklayın ve ardından <strong>Ekle</strong>'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-184">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="bcf6b-185">Rapor grubuna eklenecek raporları seçin ve ardından <strong>Tamam</strong>'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-185">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="bcf6b-186">Bir raporu rapor grubundan kaldırmak için, raporu seçin ve ardından <strong>Kaldır</strong>'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-186">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="bcf6b-187">Raporların oluşturulduğu sırayı değiştirmek için, listeden bir rapor seçin ve ardından <strong>Yukarı taşı</strong>'ya veya <strong>Aşağı taşı</strong>'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcf6b-187">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="bcf6b-188">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="bcf6b-188">Additional resources</span></span>
--------

[<span data-ttu-id="bcf6b-189">Mali raporlama</span><span class="sxs-lookup"><span data-stu-id="bcf6b-189">Financial reporting</span></span>](financial-reporting-intro.md)




