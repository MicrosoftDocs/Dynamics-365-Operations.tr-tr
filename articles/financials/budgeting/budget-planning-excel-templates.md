---
title: "Excel'de bütçe planlama şablonları"
description: "Bu konu bütçe planlamalarında kullanılabilecek Microsoft Excel şablonlarının nasıl oluşturulacağını açıklar."
author: ryansandness
manager: AnnBe
ms.date: 07/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 96df6bbfe5c9e158b616230c2b061762a5edda08
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="budget-planning-templates-for-excel"></a><span data-ttu-id="9bc55-103">Excel'de bütçe planlama şablonları</span><span class="sxs-lookup"><span data-stu-id="9bc55-103">Budget planning templates for Excel</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9bc55-104">Bu konu bütçe planlamalarında kullanılabilecek Microsoft Excel şablonlarının nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="9bc55-104">This topic describes how to create Microsoft Excel templates that can be used with budget plans.</span></span>

<span data-ttu-id="9bc55-105">Bu konu, standart demo veri kümesi ve Yönetici kullanıcı oturum açma kullanarak bütçe planlamalarında kullanılacak Excel şablonlarının nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9bc55-105">This topic shows how to create Excel templates that will be used with budget plans using the standard demo data set and the Admin user login.</span></span> <span data-ttu-id="9bc55-106">Bütçe planlama hakkında daha fazla bilgi için bkz: [Bütçe planlamaya genel bakış.](budget-planning-overview-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="9bc55-106">For more information about budget planning, see [Budget planning overview.](budget-planning-overview-configuration.md)</span></span> <span data-ttu-id="9bc55-107">Ayrıca [Bütçe planlama 101](budget-plan.md) eğitime de temel modül yapılandırması ve kullanım prensipleri için göz atabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9bc55-107">You can also follow the [Budget planning 101](budget-plan.md) tutorial to learn basic module configuration and usage principles.</span></span>

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a><span data-ttu-id="9bc55-108">Bütçe planlama belge şablonu kullanarak bir çalışma sayfası oluşturun</span><span class="sxs-lookup"><span data-stu-id="9bc55-108">Generate a worksheet using budget plan document layout</span></span>

<span data-ttu-id="9bc55-109">Bütçe planlama belgeleri bir veya daha fazla düzen kullanılarak görüntülenebilir ve düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="9bc55-109">Budget plan documents can be viewed and edited using one or more layouts.</span></span> <span data-ttu-id="9bc55-110">Her düzen, bir Excel çalışma sayfasında bütçe planını görüntülemek ve düzenlemek için ilişkili bir bütçe planlama belgesi şablonuna sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="9bc55-110">Each layout can have an associated budget plan document template to view and edit the budget plan data in an Excel worksheet.</span></span> <span data-ttu-id="9bc55-111">Bu konuda, bir bütçe plan belgesi şablonu, varsayılan düzen yapılandırması kullanılarak oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="9bc55-111">In this topic, a budget plan document template will be generated using an existing layout configuration.</span></span> 

1. <span data-ttu-id="9bc55-112">**Bütçe planları listesini** (**Bütçeleme** &gt; **Bütçe planları**) açın.</span><span class="sxs-lookup"><span data-stu-id="9bc55-112">Open the **Budget plans list** (**Budgeting** &gt; **Budget plans**).</span></span> 
2. <span data-ttu-id="9bc55-113">Yeni bir bütçe plan belgesi oluşturmak için **Yeni** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9bc55-113">Click **New** to create a new budget plan document.</span></span> 

  <span data-ttu-id="9bc55-114">[![Bütçe planları listesi](./media/bpt11-1024x552.png)](./media/bpt11.png)</span><span class="sxs-lookup"><span data-stu-id="9bc55-114">[![Budget plans list](./media/bpt11-1024x552.png)](./media/bpt11.png)</span></span> 

3. <span data-ttu-id="9bc55-115">Satır eklemek için **Ekle** seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9bc55-115">Use the **Add** line option to add lines.</span></span> <span data-ttu-id="9bc55-116">Bütçe planı belge düzeni yapılandırmasını görüntülemek için **Düzenler** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9bc55-116">Click **Layouts** to view the budget plan document layout configuration.</span></span> 

  <span data-ttu-id="9bc55-117">[![Bütçe planları ekle](./media/bpt2-1024x274.png)](./media/bpt2.png)</span><span class="sxs-lookup"><span data-stu-id="9bc55-117">[![Budget plans add](./media/bpt2-1024x274.png)](./media/bpt2.png)</span></span> 

<span data-ttu-id="9bc55-118">Düzen yapılandırmasını gözden geçirebilir ve gerektiği gibi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9bc55-118">You can review the layout configuration and adjust it as needed.</span></span> 
1. <span data-ttu-id="9bc55-119">**Şablon** &gt; **Oluştur** üzerine giderek bu düzen için bir Excel dosyası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9bc55-119">Go to **Template** &gt; **Generate** to create an Excel file for this layout.</span></span> 
2. <span data-ttu-id="9bc55-120">Şablon oluşturulduktan sonra, **Şablon** &gt; **Görüntüle** üzerine giderek açın ve bütçe planı belge şablonunu görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="9bc55-120">After the template is generated, go to **Template** &gt; **View** to open and review the budget plan document template.</span></span> <span data-ttu-id="9bc55-121">Excel dosyasını yerel sürücünüze kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9bc55-121">You can save the Excel file to your local drive.</span></span> 

<span data-ttu-id="9bc55-122">[![Farklı kaydet](./media/bpt3-1024x545.png)](./media/bpt3.png)</span><span class="sxs-lookup"><span data-stu-id="9bc55-122">[![Save as](./media/bpt3-1024x545.png)](./media/bpt3.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="9bc55-123">Bütçe planı belgesi düzeni, bir Excel şablonu onunla ilişkilendirilen sonra düzenlenemez.</span><span class="sxs-lookup"><span data-stu-id="9bc55-123">The Budget plan document layout cannot be edited after an Excel template is associated with it.</span></span> <span data-ttu-id="9bc55-124">Düzeni değiştirmek için ilişkili Excel şablon dosyasını silin ve onu yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9bc55-124">To modify the layout, delete the associated Excel template file and regenerate it.</span></span> <span data-ttu-id="9bc55-125">Bu, düzendeki ve çalışma sayfasındaki alanları eşit tutmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="9bc55-125">This is required to keep the fields in the layout and the worksheet synchronized.</span></span> 

<span data-ttu-id="9bc55-126">Excel şablonu bütçe planı belgesi düzenindeki **Çalışma Sayfasında kullanılabilir** sütunu Evet olarak ayarlanmış tüm öğeleri içerecektir.</span><span class="sxs-lookup"><span data-stu-id="9bc55-126">The Excel template will contain all of the elements from the budget plan document layout, where the **Available in Worksheet** column is set to True.</span></span> <span data-ttu-id="9bc55-127">Excel şablonunda çakışan öğelere izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="9bc55-127">Overlapping elements are not allowed in the Excel template.</span></span> <span data-ttu-id="9bc55-128">Örneğin, eğer düzen İstek Q1, İstek Q2, İstek Q3 ve İstek Q4 sütunlarını içeriyorsa ve toplam istek sütunu, tüm 4 çeyreklik sütunların toplamını temsil ediyorsa, yalnızca çeyrek sütunları veya toplam sütun Excel şablonunda kullanılmaya açıktır.</span><span class="sxs-lookup"><span data-stu-id="9bc55-128">For example, if the layout contains Request Q1, Request Q2, Request Q3, and Request Q4 columns, and a total request column that represents a sum of all 4 quarterly columns, only the quarterly columns or total column is available to be used in the Excel template.</span></span> <span data-ttu-id="9bc55-129">Excel şablonu çakışan sütunları güncelleştirme boyunca güncelleştiremez çünkü tablo içerisindeki verilerin tarihi geçebilir ve hatalı olabilirler.</span><span class="sxs-lookup"><span data-stu-id="9bc55-129">The Excel file cannot update overlapping columns during the update because data in the table could become out of date and inaccurate.</span></span>

<span data-ttu-id="9bc55-130">[![Örnek](./media/bpt4-1024x615.png)](./media/bpt4.png)</span><span class="sxs-lookup"><span data-stu-id="9bc55-130">[![Example](./media/bpt4-1024x615.png)](./media/bpt4.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="9bc55-131">Excel kullanarak bütçe planı verisini düzenleme ve görüntüleme ile ilgili potansiyel sorunları önlemek için, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ve Microsoft Dynamics Office Add-in Data Connector için aynı kullanıcı oturum açmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9bc55-131">To avoid potential issues with viewing and editing budget plan data using Excel, the same user should be logged into both Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and the Microsoft Dynamics Office Add-in Data Connector.</span></span>

## <a name="add-a-header-to-budget-plan-document-template"></a><span data-ttu-id="9bc55-132">Bütçe planı belge şablonuna bir başlık ekleyin</span><span class="sxs-lookup"><span data-stu-id="9bc55-132">Add a header to budget plan document template</span></span>
<span data-ttu-id="9bc55-133">Başlık bilgisi eklemek için, Excel dosyasındaki üst satırı seçin ve boş satırlar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9bc55-133">To add header information, select the top row in the Excel file and insert empty rows.</span></span> <span data-ttu-id="9bc55-134">**Veri Bağlayıcısı** içerisinde **Tasarım** üzerine tıklayarak Excel dosyasına başlıklar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9bc55-134">Click **Design** in the **Data Connector** to add header fields to the Excel file.</span></span>

<span data-ttu-id="9bc55-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span><span class="sxs-lookup"><span data-stu-id="9bc55-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span></span> 

<span data-ttu-id="9bc55-136">**Tasarım** sekmesinde, **Ekle** alanlar üzerine tıklayın ve sonra varlık veri kaynağı olarak **BudgetPlanHeader** seçin.</span><span class="sxs-lookup"><span data-stu-id="9bc55-136">In the **Design** tab, click **Add** fields, and then select **BudgetPlanHeader** as the entity data source.</span></span>

<span data-ttu-id="9bc55-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span><span class="sxs-lookup"><span data-stu-id="9bc55-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span></span>

<span data-ttu-id="9bc55-138">İmleci Excel dosyası üzerinde istenilen konuma getirin.</span><span class="sxs-lookup"><span data-stu-id="9bc55-138">Point the cursor to the desired location in the Excel file.</span></span> <span data-ttu-id="9bc55-139">Seçilen konuma alan etiketi eklemek için **Etiket ekle** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9bc55-139">Click **Add label** to add the field label to the selected location.</span></span> <span data-ttu-id="9bc55-140">Seçilen yere değer alanı eklemek için **Değer Ekle** seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="9bc55-140">Select **Add Value** to add the value field to the selected place.</span></span> <span data-ttu-id="9bc55-141">Tasarımcıyı kapatmak için **Kapat** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9bc55-141">Click **Done** to close the designer.</span></span>

## <a name="bpt7mediabpt7pngmediabpt7png"></a><span data-ttu-id="9bc55-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span><span class="sxs-lookup"><span data-stu-id="9bc55-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span></span>

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a><span data-ttu-id="9bc55-143">Bütçe planı belge şablonu tablosuna bir hesaplanmış sütun ekleyin</span><span class="sxs-lookup"><span data-stu-id="9bc55-143">Add a calculated column to budget plan document template table</span></span>
--------------------------------------------------------------

<span data-ttu-id="9bc55-144">Daha sonra, hesaplanmış sütunlar, oluşturulmuş bütçe planı belge şablonuna eklenir.</span><span class="sxs-lookup"><span data-stu-id="9bc55-144">Next, calculated columns will be added to generated budget plan document template.</span></span> <span data-ttu-id="9bc55-145">Bir **Toplam istek** sütunu, İstek Q1: İstek Q4 sütunlarını toplar ve bir **Ayarlama** sütunu, **Toplam İstek** sütununu önceden belirlenmiş bir faktör ile yeniden hesaplar.</span><span class="sxs-lookup"><span data-stu-id="9bc55-145">A **Total request** column, which summarizes Request Q1: Request Q4 columns, and an **Adjustment** column, which recalculates the **Total Request** column by a predefined factor.</span></span>

<span data-ttu-id="9bc55-146">**Veri Bağlayıcısı** içerisinde **Tasarım** üzerine tıklayarak tabloya sütunlar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9bc55-146">Click **Design** in the **Data connector** to add columns to the table.</span></span> <span data-ttu-id="9bc55-147">**BudgetPlanWorksheet** veri kaynağının yanındaki **Düzenle** üzerine tıklayarak sütunlar eklemeye başlayın.</span><span class="sxs-lookup"><span data-stu-id="9bc55-147">Click **Edit** next to **BudgetPlanWorksheet** data source to start adding columns.</span></span>

<span data-ttu-id="9bc55-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span><span class="sxs-lookup"><span data-stu-id="9bc55-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span></span> 

<span data-ttu-id="9bc55-149">Seçili alan grubu, şablonda kullanılan sütunları görüntüler.</span><span class="sxs-lookup"><span data-stu-id="9bc55-149">The selected field group displays the columns that are available in the template.</span></span> <span data-ttu-id="9bc55-150">Yeni bir sütun eklemek için **Formül** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9bc55-150">Click **Formula** to add a new column.</span></span> <span data-ttu-id="9bc55-151">Yeni sütuna bir ad verin ve formülü **Formül** alanına yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="9bc55-151">Name the new column and then paste the formula into the **Formula** field.</span></span> <span data-ttu-id="9bc55-152">Sütunu yerleştirmek için **Güncelleştir** düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9bc55-152">Click **Update** to insert the column.</span></span>

<span data-ttu-id="9bc55-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span><span class="sxs-lookup"><span data-stu-id="9bc55-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="9bc55-154">Formülü tanımlamak için, formülü elektronik tabloda oluşturun ve sonra **Tasarım** penceresine yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="9bc55-154">To define the formula, create the formula in the spreadsheet, and then copy it to the **Design** window.</span></span> <span data-ttu-id="9bc55-155">Finance and Operations'a bağlı bir tablo genellikle "AXTable1" olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="9bc55-155">A Finance and Operations bound table will typically be named "AXTable1".</span></span> <span data-ttu-id="9bc55-156">Örneğin, İstek Q1 : İstek Q4 sütunlarını elektronik sayfada özetlemk için, formül = AxTable1\[İstek Q1\]+AxTable1\[İstek Q2\]+AxTable1\[İstek Q3\]+AxTable1\[İstek Q4\].</span><span class="sxs-lookup"><span data-stu-id="9bc55-156">For example, to summarize Request Q1 : Request Q4 columns in the spreadsheet, the formula = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].</span></span>

<span data-ttu-id="9bc55-157">**Ayarlama** sütununu eklemek için bu adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="9bc55-157">Repeat these steps to insert the **Adjustment** column.</span></span> <span data-ttu-id="9bc55-158">Şu formülü kullanın = AxTable1\[Toplam istek\]\*$I$1 bu sütun için.</span><span class="sxs-lookup"><span data-stu-id="9bc55-158">Use formula = AxTable1\[Total request\]\*$I$1 for this column.</span></span> <span data-ttu-id="9bc55-159">Bu, hücre I1 içindeki değeri alır ve **Toplam istek** içindeki değerleri, ayarlama tutarlarını hesaplamak için çarpar.</span><span class="sxs-lookup"><span data-stu-id="9bc55-159">This will take the value in cell I1 and multiply the values in the **Total request** column to calculate adjustment amounts.</span></span>

<span data-ttu-id="9bc55-160">Kaydedin ve Excel dosyasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="9bc55-160">Save and close the Excel file.</span></span> <span data-ttu-id="9bc55-161">Finance and Operations'a geri dönün ve **Düzenler** içerisinde **Şablon &gt; Karşıya Yükleme** üzerine tıklayarak kaydedilmiş Excel şablonunu bütçe planında kullanılmak üzere karşıya yükleyin.</span><span class="sxs-lookup"><span data-stu-id="9bc55-161">Return to Finance and Operations, and in **Layouts**, click **Template &gt; Upload** to upload the saved Excel template to be used for the budget plan.</span></span> 

<span data-ttu-id="9bc55-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span><span class="sxs-lookup"><span data-stu-id="9bc55-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span></span> 

<span data-ttu-id="9bc55-163">**Düzenler** kaydırıcısını kapatın.</span><span class="sxs-lookup"><span data-stu-id="9bc55-163">Close the **Layouts** slider.</span></span> <span data-ttu-id="9bc55-164">**Bütçe planı** belgesi içinde **Çalışma sayfası** üzerine tıklayarak belgeyi Excel'de görüntüleyin ve düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="9bc55-164">In **Budget plan** document, click **Worksheet** to view and edit the document in Excel.</span></span> <span data-ttu-id="9bc55-165">Ayarlanabilir Excel şablonu, bu bütçe planı çalışma sayfasını oluşturmak için kullanıldı ve hesaplanmış sütunlar önceki adımlarda tanımlanan formüller kullanılarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="9bc55-165">Note that the adjusted Excel template was used to create this budget plan worksheet and calculated columns are updated using the formulas that were defined in the previous steps.</span></span> 

<span data-ttu-id="9bc55-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span><span class="sxs-lookup"><span data-stu-id="9bc55-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span></span>

## <a name="tips--tricks-for-creating-budget-plan-templates"></a><span data-ttu-id="9bc55-167">Bütçe planı şablonlarını oluşturmak için ipuçları ve püf noktalar</span><span class="sxs-lookup"><span data-stu-id="9bc55-167">Tips & tricks for creating budget plan templates</span></span>
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a><span data-ttu-id="9bc55-168">Bir bütçe planı şablonu için ek veri kaynakları ekleyebilir ve kullanabilir miyim?</span><span class="sxs-lookup"><span data-stu-id="9bc55-168">Can I add and use additional data sources to a budget plan template?</span></span>

<span data-ttu-id="9bc55-169">Evet, **Tasarım** menüsünü, Excel şablonundaki aynı ya da diğer sayfalara ek varlıklar eklemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9bc55-169">Yes, you can use the **Design** menu to add additional entities to the same or other sheets in the Excel template.</span></span> <span data-ttu-id="9bc55-170">Örneğin, **BudgetPlanProposedProject** veri kaynağını, Excel içindeki bir bütçe planı verisi üzerinde çalışırken aynı zamanda önerilen projelerin bir listesini oluşturmak ve tutmak için ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9bc55-170">For example, you can add the **BudgetPlanProposedProject** data source to create and maintain a list of proposed projects at the same time when working with budget plan data in Excel.</span></span> <span data-ttu-id="9bc55-171">Yüksek hacimli veri kaynakları dahil etmenin, Excel çalışma kitabının performansını etkileyebileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="9bc55-171">Note that including high-volume data sources might impact performance of the Excel workbook.</span></span> 

<span data-ttu-id="9bc55-172">**Veri Bağlayıcısı** içerisindeki **Filtre** seçeneğini, istediğiniz filtreleri ek veri kaynaklarına bağlamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9bc55-172">You can use the **Filter** option in the **Data Connector** to add desired filters to additional data sources.</span></span>

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a><span data-ttu-id="9bc55-173">Diğer kullanıcılar için Veri bağlayıcısı içindeki Tasarım seçeneğini gizleyebilir miyim?</span><span class="sxs-lookup"><span data-stu-id="9bc55-173">Can I hide the Design option in the Data connector for other users?</span></span>

<span data-ttu-id="9bc55-174">Evet **Veri Bağlayıcısı** seçeneğini açarak **Tasarım** seçeneğini diğer kullanıcılardan gizleyin.</span><span class="sxs-lookup"><span data-stu-id="9bc55-174">Yes, open the **Data Connector** options to hide the **Design** option from other users.</span></span>

<span data-ttu-id="9bc55-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span><span class="sxs-lookup"><span data-stu-id="9bc55-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span></span>

<span data-ttu-id="9bc55-176">**Veri bağlayıcısı seçeneklerini** genişletin ve **Tasarım etkinleştir** onay kutusunu temizleyin.</span><span class="sxs-lookup"><span data-stu-id="9bc55-176">Expand **Data connector options** and clear the **Enable design** check box.</span></span> <span data-ttu-id="9bc55-177">Bu, **Tasarım** seçeneğini **Veri bağlayıcısından** gizleyecektir.</span><span class="sxs-lookup"><span data-stu-id="9bc55-177">This will hide the **Design** option from the **Data connector**.</span></span>

<span data-ttu-id="9bc55-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span><span class="sxs-lookup"><span data-stu-id="9bc55-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span></span>

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a><span data-ttu-id="9bc55-179">Kullanıcıların verilerle çalışırken veri bağlayıcısını yanlışlıkla kapatmalarını engelleyebilir miyim?</span><span class="sxs-lookup"><span data-stu-id="9bc55-179">Can I prevent users from accidently closing the Data connector while working with data?</span></span>

<span data-ttu-id="9bc55-180">Kullanıcıların onu kapatmasını engellemek için şablonu kilitlemeyi öneririz.</span><span class="sxs-lookup"><span data-stu-id="9bc55-180">We recommend locking the template to prevent users from closing it.</span></span> <span data-ttu-id="9bc55-181">Kilidi açmak için **Veri bağlayıcısı** üzerine tıklayın, sağ üst köşede bir ok belirir.</span><span class="sxs-lookup"><span data-stu-id="9bc55-181">To turn on the lock, click the **Data connector**, in the top right corner an arrow appears.</span></span> 

<span data-ttu-id="9bc55-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span><span class="sxs-lookup"><span data-stu-id="9bc55-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span></span> 

<span data-ttu-id="9bc55-183">Ek bir menü için oku tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9bc55-183">Click the arrow for an additional menu.</span></span> <span data-ttu-id="9bc55-184">**Kilidi** seçin.</span><span class="sxs-lookup"><span data-stu-id="9bc55-184">Select **Lock**.</span></span>

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a><span data-ttu-id="9bc55-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span><span class="sxs-lookup"><span data-stu-id="9bc55-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span></span>

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a><span data-ttu-id="9bc55-186">Bütçe planı şablonlarımla hücre biçimlendirme, koşullu biçimlendirme ve grafikler gibi diğer Excel özelliklerini kullanabilir miyim?</span><span class="sxs-lookup"><span data-stu-id="9bc55-186">Can I use other Excel features, like cell formatting, colors, conditional formatting, and charts with my budget plan templates?</span></span>

<span data-ttu-id="9bc55-187">Evet, Excel yeteneklerinden çoğu bütçe planı şablonlarında çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="9bc55-187">Yes, most of the standard Excel capabilities will work in budget plan templates.</span></span> <span data-ttu-id="9bc55-188">Salt okunur ve düzenlenebilir sütunlar arasında ayrım yapmak için renk kodlaması kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="9bc55-188">We recommend using color-coding for users to distinguish between read-only and editable columns.</span></span> <span data-ttu-id="9bc55-189">Koşullu biçimlendirme, bütçenin sorunlu alanlarını vurgulamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9bc55-189">Conditional formatting can be used to highlight problematic areas of the budget.</span></span> <span data-ttu-id="9bc55-190">Standart Excel formüllerini tablo üzerinde kullanarak sütun toplamları kolaylıkla sunulabilir.</span><span class="sxs-lookup"><span data-stu-id="9bc55-190">Column totals can easily be presented by using standard Excel formulas above the table.</span></span>

<span data-ttu-id="9bc55-191">Bütçe verisinin ek gruplama ve görselleştirmeleri için özet tabloları ve grafikleri oluşturabilir ve kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9bc55-191">You can also create and use pivot tables and charts for additional groupings and visualizations of budget data.</span></span> <span data-ttu-id="9bc55-192">**Veri** sekmesinde, **Bağlantılar** grubunda, **Tümünü Yenile** üzerine tıklayın ve daha sonra **Bağlantı Özellikleri** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9bc55-192">On the **Data** tab, in the **Connections** group, click **Refresh All**, and then click **Connection Properties**.</span></span> <span data-ttu-id="9bc55-193">**Kullanım** sekmesini tıklatın. **Yenile** altında, **Dosya açarken veriyi yenile** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="9bc55-193">Click the **Usage** tab. Under **Refresh**, select the **Refresh data when opening the file** check box.</span></span> 

<span data-ttu-id="9bc55-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span><span class="sxs-lookup"><span data-stu-id="9bc55-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span></span>




