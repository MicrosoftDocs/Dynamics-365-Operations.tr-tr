---
title: "Finansal rapor tasarımcısında satır tanımları"
description: "Satır tanımını finansal rapordaki her satırın içeriğini belirten bir rapor bileşeni veya yapı taşıdır. Satır tanımı birden çok şirket tarafından kullanılabilen bir yapı taşı grubu oluşturmak için sütun tanımları, raporlama ağacı tanımları ve rapor tanımları ile birleştirilebilir."
author: aprilolson
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
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: c829af1da1b3109f4687c9a2536dd156339d5c76
ms.contentlocale: tr-tr
ms.lasthandoff: 08/13/2018

---

# <a name="row-definitions-in-financial-report-designer"></a><span data-ttu-id="47937-104">Finansal rapor tasarımcısında satır tanımları</span><span class="sxs-lookup"><span data-stu-id="47937-104">Row definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47937-105">Satır tanımını finansal rapordaki her satırın içeriğini belirten bir rapor bileşeni veya yapı taşıdır.</span><span class="sxs-lookup"><span data-stu-id="47937-105">A row definition is a report component, or building block, that specifies the contents of each row on a financial report.</span></span> <span data-ttu-id="47937-106">Satır tanımı birden çok şirket tarafından kullanılabilen bir yapı taşı grubu oluşturmak için sütun tanımları, raporlama ağacı tanımları ve rapor tanımları ile birleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="47937-106">A row definition can be combined with column definitions, reporting tree definitions, and report definitions to create a building block group that can be used by multiple companies.</span></span>

## <a name="create-a-row-definition"></a><span data-ttu-id="47937-107">Satır tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="47937-107">Create a row definition</span></span>

1. <span data-ttu-id="47937-108">Rapor Tasarımcısı'ndaki gezinti bölmesinde **Satır Tanımları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47937-108">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="47937-109">**Dosya** menüsünde, **Yeni**'ye ve ardından **Satır Tanımı**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47937-109">On the **File** menu, click **New**, and then click **Row Definition**.</span></span> <span data-ttu-id="47937-110">Her hücrenin içeriği hakkında daha fazla bilgi için, bkz. [Satır tanımı hücrelerini değiştirme](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="47937-110">For more information about the content of each cell, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="open-a-row-definition"></a><span data-ttu-id="47937-111">Bir satır tanımını açma</span><span class="sxs-lookup"><span data-stu-id="47937-111">Open a row definition</span></span>
1. <span data-ttu-id="47937-112">Rapor Tasarımcısı'ndaki gezinti bölmesinde **Satır Tanımları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47937-112">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="47937-113">Açmak için satır tanımının adına çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47937-113">Double-click the name of the row definition to open.</span></span>
3. <span data-ttu-id="47937-114">Satır tanımıyla ilişkili tüm yapı taşlarını görüntülemek için, satır tanımına sağ tıklayın ve ardından **İlişkiler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="47937-114">To view any building blocks that are associated with the row definition, right-click the row definition, and then select **Associations**.</span></span>

## <a name="contents-of-a-row-definition"></a><span data-ttu-id="47937-115">Bir satır tanımının içerikleri</span><span class="sxs-lookup"><span data-stu-id="47937-115">Contents of a row definition</span></span>
<span data-ttu-id="47937-116">Bir satır tanımı en fazla 20.000 mali boyut içerebilir ve içinde aşağıdaki bilgiler bulunabilir:</span><span class="sxs-lookup"><span data-stu-id="47937-116">A row definition can contain up to 20,000 financial dimension rows and can include the following information:</span></span>

- <span data-ttu-id="47937-117">**Nakit** veya **Toplam Gelir** gibi bölüm başlıkları, satırlar ve alanlar oluşturarak rapora anlam ekleyen açıklayıcı metin</span><span class="sxs-lookup"><span data-stu-id="47937-117">Descriptive text that adds meaning to the report by creating section headings, lines, and spaces, such as **Cash** or **Total Revenue**</span></span>
- <span data-ttu-id="47937-118">Microsoft Dynamics 365 for Finance and Operations içindeki boyut değerlerini içerebilen finansal veri bağlantıları</span><span class="sxs-lookup"><span data-stu-id="47937-118">Links to financial data, which can include dimension values in the Microsoft Dynamics 365 for Finance and Operations</span></span>

    > [!NOTE]
    > <span data-ttu-id="47937-119">Rapor her oluşturulduğunda mali boyutlar sisteminden verileri çekmek için bir satır tanımı ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47937-119">You can set up a row definition to pull data from the financial dimensions system every time that the report is generated.</span></span>

- <span data-ttu-id="47937-120">İlişkili mali verileri esas alan satır toplamları ve formüller</span><span class="sxs-lookup"><span data-stu-id="47937-120">Row totals and formulas that are based on the linked financial data</span></span>

<span data-ttu-id="47937-121">Genellikle, bir satır tanımındaki her satır aşağıdaki bilgi türlerinden birini içerir:</span><span class="sxs-lookup"><span data-stu-id="47937-121">Usually, each row in a row definition contains one of the following types of information:</span></span>

- <span data-ttu-id="47937-122">Mali boyutlar sisteminin referansları</span><span class="sxs-lookup"><span data-stu-id="47937-122">References to the financial dimensions system</span></span>
- <span data-ttu-id="47937-123">Verileri esas alan toplamlar veya hesaplamalar</span><span class="sxs-lookup"><span data-stu-id="47937-123">Totals or calculations that are based on the data</span></span>
- <span data-ttu-id="47937-124">Biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="47937-124">Formatting</span></span>

<span data-ttu-id="47937-125">Bir satır tanımına bilgi girmek için iki yöntem vardır:</span><span class="sxs-lookup"><span data-stu-id="47937-125">There are two methods for entering information in a row definition:</span></span>

- <span data-ttu-id="47937-126">Satır bilgilerini el ile yeni bir satır tanımına girin.</span><span class="sxs-lookup"><span data-stu-id="47937-126">Manually enter row information in a new row definition.</span></span> <span data-ttu-id="47937-127">Daha fazla bilgi için [Satır tanımı hücrelerini değiştirme](modify-row-definition-cells-financial-reporting.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="47937-127">For more information, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>
- <span data-ttu-id="47937-128">Satır bilgilerini doğrudan finansal boyutlardan çekmek için rapor tasarımcısını kullanın.</span><span class="sxs-lookup"><span data-stu-id="47937-128">Use report designer to pull row information directly from the financial dimensions.</span></span> <span data-ttu-id="47937-129">Daha fazla bilgi için, [Satır tanımı hücrelerini değiştirme](modify-row-definition-cells-financial-reporting.md) bölümündeki "İlgili formüller/satırlar/birimler" kısmına bakın.</span><span class="sxs-lookup"><span data-stu-id="47937-129">For more information, see the "Related formulas/rows/units" section in [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="add-dimensions-in-a-row-definition"></a><span data-ttu-id="47937-130">Bir satır tanımına boyut ekleme</span><span class="sxs-lookup"><span data-stu-id="47937-130">Add dimensions in a row definition</span></span>
<span data-ttu-id="47937-131">Bir boyut, veri ve değerlerin bir kesişimidir.</span><span class="sxs-lookup"><span data-stu-id="47937-131">A dimension is an intersection of data and values.</span></span> <span data-ttu-id="47937-132">Rapor tasarımcısında verileri ve değerleri gruplandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47937-132">You can group data and values in report designer.</span></span> <span data-ttu-id="47937-133">Ardından hareketleri sınıflandırabilir ve daha ayrıntılı şekilde çözümleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47937-133">You can then classify and analyze transactions in more detail.</span></span> <span data-ttu-id="47937-134">**Boyutlardan Satır Ekle** iletişim kutusunu kullanarak bir satır tanımına aynı anda birden fazla satır ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47937-134">You can use the **Insert Rows from Dimensions** dialog box to add multiple rows to a row definition at the same time.</span></span> <span data-ttu-id="47937-135">İletişim kutusu her boyut için bir sütun görüntüler.</span><span class="sxs-lookup"><span data-stu-id="47937-135">The dialog box displays one column for each dimension.</span></span> <span data-ttu-id="47937-136">Aşağıdaki tabloda her boyut için belirtebileceğiniz bilgiler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="47937-136">The following table describes the information that you can specify for each dimension.</span></span>

| <span data-ttu-id="47937-137">Seçenek</span><span class="sxs-lookup"><span data-stu-id="47937-137">Option</span></span>                | <span data-ttu-id="47937-138">Açıklama</span><span class="sxs-lookup"><span data-stu-id="47937-138">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="47937-139">Boyut</span><span class="sxs-lookup"><span data-stu-id="47937-139">Dimension</span></span>             | <span data-ttu-id="47937-140">Satır tanımına eklenecek boyutu tanımlayan model.</span><span class="sxs-lookup"><span data-stu-id="47937-140">The pattern that identifies the dimension to add to the row definition.</span></span> <span data-ttu-id="47937-141">Bu model, boyutlardaki her bir konum için bir ve işareti (&) veya rakam işareti (\#) içerir.</span><span class="sxs-lookup"><span data-stu-id="47937-141">This pattern contains one ampersand (&) or number sign (\#) for each position in the dimensions.</span></span> <span data-ttu-id="47937-142">Genellikle, Ana Hesap boyutu için tüm ve işaretlerini ve diğer boyutlar için tüm rakam işaretlerini kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="47937-142">Generally, use all ampersands for the Main Account dimension and all number signs for other dimensions.</span></span> |
| <span data-ttu-id="47937-143">Boyut Aralığı Başlangıcı</span><span class="sxs-lookup"><span data-stu-id="47937-143">Dimension Range Start</span></span> | <span data-ttu-id="47937-144">Bu boyutun satır tanımına eklenecek ilk değeri.</span><span class="sxs-lookup"><span data-stu-id="47937-144">The first value for this dimension to add to the row definition.</span></span> |
| <span data-ttu-id="47937-145">Boyut Aralığı Sonu</span><span class="sxs-lookup"><span data-stu-id="47937-145">Dimension Range End</span></span>   | <span data-ttu-id="47937-146">Bu boyutun satır tanımına eklenecek son değeri.</span><span class="sxs-lookup"><span data-stu-id="47937-146">The last value for this dimension to add to the row definition.</span></span> |

<span data-ttu-id="47937-147">Bir satır tanımına boyut eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="47937-147">To add dimensions to a row definition, follow these steps.</span></span>

1. <span data-ttu-id="47937-148">Rapor Tasarımcısı'nda, **Satır Tanımları**'na tıklayın ve ardından değiştirilecek satır tanımını açın.</span><span class="sxs-lookup"><span data-stu-id="47937-148">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="47937-149">**Düzenle** menüsünde, **Boyutlardan Satır Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47937-149">On the **Edit** menu, click **Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="47937-150">**Boyutlardan Satır Ekle** iletişim kutusundaki **Boyutlar** satırında, satır tanımına aktarılacak boyuta ait hücreyi seçin ve ardından **Tüm &&&** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47937-150">In the **Insert Rows from Dimensions** dialog box, in the **Dimensions** row, select the cell for the dimension to transfer to the row definition, and then click **All &&&**.</span></span>
4. <span data-ttu-id="47937-151">Satır tanımını belirli bir boyut değerleri aralığıyla sınırlandırmak için, **Boyut Aralığı Başlangıcı** hücresine başlangıç boyut değerini ve ardından **Boyut Aralığı Sonu** hücresindeki son boyut değerini girin.</span><span class="sxs-lookup"><span data-stu-id="47937-151">To limit the row definition to a specific range of dimension values, enter the starting dimension value in the **Dimension Range Start** cell, and then enter the ending dimension value in the **Dimension Range End** cell.</span></span> <span data-ttu-id="47937-152">Seçilen boyuta ait tüm değerleri eklemek için bu hücreleri boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="47937-152">To include all values for the selected dimension, leave these cells empty.</span></span>

    > [!NOTE]
    > <span data-ttu-id="47937-153">Boyut aralıklarındaki joker karakterler (\* veya ?) ERP veritabanının verileri nasıl harmanladığına bağlı olarak istediğiniz tüm sonuçları vermeyebilir.</span><span class="sxs-lookup"><span data-stu-id="47937-153">Wildcard characters (\* or ?) in dimension ranges might not return all the results that you want, depending on how the ERP database collates data.</span></span>

5. <span data-ttu-id="47937-154">**Başlangıç satır kodu** alanında, satır tanımına eklenecek ilk boyut değerine ait satır kodunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="47937-154">In the **Starting row code** field, specify the row code for the first dimension value to add to the row definition.</span></span>
6. <span data-ttu-id="47937-155">**Her satırı şu kadar artır:** alanında, art arda gelen satır kodları arasındaki boşluğu belirtin.</span><span class="sxs-lookup"><span data-stu-id="47937-155">In the **Increment each row by** field, specify the gap between consecutive row codes.</span></span> <span data-ttu-id="47937-156">Örneğin, ilk satır kodu 100 ve artış değeri 30 ise, ilk yeni satırların kodları 100, 130, 160, 190 ve 220 olur.</span><span class="sxs-lookup"><span data-stu-id="47937-156">For example, if the first row code is 100, and the increment value is 30, the first new rows have the codes 100, 130, 160, 190, and 220.</span></span> <span data-ttu-id="47937-157">Yeni biçim ve formül satırlarını eklemek için yeterli alan sağlayan bir artış değerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="47937-157">Use an increment value that provides enough space to insert new format and formula rows.</span></span>
7. <span data-ttu-id="47937-158">**Tamam** düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47937-158">Click **OK**.</span></span> <span data-ttu-id="47937-159">Seçilen boyut değerlerinin her biri için satır tanımına bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="47937-159">For each of the selected dimension values, one line is added to the row definition.</span></span>

## <a name="adjust-rounding-in-a-row-definition"></a><span data-ttu-id="47937-160">Bir satır tanımındaki yuvarlamayı ayarlama</span><span class="sxs-lookup"><span data-stu-id="47937-160">Adjust rounding in a row definition</span></span>
<span data-ttu-id="47937-161">Tutarların yuvarlandığı bir bilançonuz varsa toplamlar eşitlenmeyebilir.</span><span class="sxs-lookup"><span data-stu-id="47937-161">If you have a balance sheet where the amounts are rounded, the totals might not balance.</span></span> <span data-ttu-id="47937-162">Bu sorun, örneğin bir bilanço raporunda yuvarlama seçeneğini kullanıyorsanız ve aynı zamanda rapor tanımı da yuvarlamayı belirtiyorsa görülebilir.</span><span class="sxs-lookup"><span data-stu-id="47937-162">This issue can occur if, for example, you use the rounding option on a balance sheet report and the report definition also specifies rounding.</span></span> <span data-ttu-id="47937-163">Bilançolardaki tutarları eşitlemek için satır tanımındaki **Yuvarlama ayarlaması** seçeneğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47937-163">You can use the **Rounding adjustment** option in the row definition to balance the amounts in the balance sheets.</span></span> <span data-ttu-id="47937-164">Yuvarlamayı rapor tanımının **Ayarlar** sekmesinde kapatabilir veya değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47937-164">You can turn rounding off or modify it on the **Settings** tab of the report definition.</span></span> <span data-ttu-id="47937-165">Aşağıdaki tabloda tutarların nasıl yuvarlandığı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="47937-165">The following table shows how amounts are rounded.</span></span> <span data-ttu-id="47937-166">Bu tabloda, yuvarlama açıkken 100 ve 200. satırların toplamları farklı olur.</span><span class="sxs-lookup"><span data-stu-id="47937-166">In this table, the totals of rows 100 and 200 differ when rounding is turned on.</span></span>

| <span data-ttu-id="47937-167">Satır kodu</span><span class="sxs-lookup"><span data-stu-id="47937-167">Row code</span></span> | <span data-ttu-id="47937-168">Yuvarlamasız tutarlar</span><span class="sxs-lookup"><span data-stu-id="47937-168">Amounts without rounding</span></span> | <span data-ttu-id="47937-169">Tam binlere yuvarlamayla tutar</span><span class="sxs-lookup"><span data-stu-id="47937-169">Amount with rounding to whole thousands</span></span> |
|----------|--------------------------|-----------------------------------------|
| <span data-ttu-id="47937-170">100</span><span class="sxs-lookup"><span data-stu-id="47937-170">100</span></span>      | <span data-ttu-id="47937-171">3.600</span><span class="sxs-lookup"><span data-stu-id="47937-171">3,600</span></span>                    | <span data-ttu-id="47937-172">4</span><span class="sxs-lookup"><span data-stu-id="47937-172">4</span></span>                                       |
| <span data-ttu-id="47937-173">200</span><span class="sxs-lookup"><span data-stu-id="47937-173">200</span></span>      | <span data-ttu-id="47937-174">3.700</span><span class="sxs-lookup"><span data-stu-id="47937-174">3,700</span></span>                    | <span data-ttu-id="47937-175">4</span><span class="sxs-lookup"><span data-stu-id="47937-175">4</span></span>                                       |
| <span data-ttu-id="47937-176">Toplam</span><span class="sxs-lookup"><span data-stu-id="47937-176">Total</span></span>    | <span data-ttu-id="47937-177">7.300</span><span class="sxs-lookup"><span data-stu-id="47937-177">7,300</span></span>                    | <span data-ttu-id="47937-178">8</span><span class="sxs-lookup"><span data-stu-id="47937-178">8</span></span>                                       |

<span data-ttu-id="47937-179">Bir bilançodaki yuvarlamayı ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="47937-179">To adjust rounding in a balance sheet, follow these steps.</span></span>

1. <span data-ttu-id="47937-180">Rapor Tasarımcısı'nda, **Satır Tanımları**'na tıklayın ve ardından değiştirilecek satır tanımını açın.</span><span class="sxs-lookup"><span data-stu-id="47937-180">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="47937-181">**Düzenle** menüsünde, **Yuvarlama Ayarlaması**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47937-181">On the **Edit** menu, click **Rounding Adjustment**.</span></span>
3. <span data-ttu-id="47937-182">**Yuvarlama Ayarlamaları** iletişim kutusunda, şu değerleri girin:</span><span class="sxs-lookup"><span data-stu-id="47937-182">In the **Rounding Adjustments** dialog box, enter the following values:</span></span>

    - <span data-ttu-id="47937-183">**Yuvarlama ayarlaması satırı**: Bilançoyu eşitlemek için ayarlanması gereken satıra ait satır kodu.</span><span class="sxs-lookup"><span data-stu-id="47937-183">**Rounding adjustment row** – The row code for the row that should be adjusted to balance the balance sheet.</span></span>
    - <span data-ttu-id="47937-184">**Toplam kıymetler satırı**: Bilançoda toplam kıymetleri içeren satıra ait satır kodu.</span><span class="sxs-lookup"><span data-stu-id="47937-184">**Total assets row** – The row code for the row in the balance sheet that contains the total assets.</span></span>
    - <span data-ttu-id="47937-185">**Toplam borçlar ve öz sermaye satırı**: Bilançoda toplam borçları ve öz sermayeyi içeren satıra ait satır kodu.</span><span class="sxs-lookup"><span data-stu-id="47937-185">**Total liabilities and equity row** – The row code for the row in the balance sheet that contains the total liabilities and equity.</span></span>
    - <span data-ttu-id="47937-186">**Ayarlama tutarı sınırı**: Otomatik ayarlamalarda sınırı belirten pozitif bir tam sayı.</span><span class="sxs-lookup"><span data-stu-id="47937-186">**Adjustment amount limit** – A positive whole number that specifies the limit on automatic adjustments.</span></span> <span data-ttu-id="47937-187">Bu tutar gerçek yuvarlama farkının mutlak değeriyle kıyaslanır.</span><span class="sxs-lookup"><span data-stu-id="47937-187">This amount is compared with the absolute value of the actual rounding difference.</span></span>

    > [!NOTE]
    > <span data-ttu-id="47937-188">Bu satır kodları mali verilerinizle ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="47937-188">These row codes must be linked to your financial data.</span></span> <span data-ttu-id="47937-189">Başka bir deyişle, satırın **Mali Boyutlarla İlişkilendir** hücresinde bir boyut değeri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="47937-189">In other words, the row must have a dimension value in its **Link to Financial Dimensions** cell.</span></span> <span data-ttu-id="47937-190">Bir açıklamaya (**DESC**), hesaplanan (**CALC**) ya da toplamı alınan (**TOT**) satıra **başvurmayın**.</span><span class="sxs-lookup"><span data-stu-id="47937-190">Do **not** reference a description (**DESC**), calculated (**CALC**), or totaled (**TOT**) row.</span></span>

<span data-ttu-id="47937-191">Artık bilançonuzdaki tutarlar yuvarlama açıkken eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="47937-191">The amounts in your balance sheet will now balance evenly when rounding is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="47937-192">Ayarlama sınırı, rapor tanımı için belirtilen **Yuvarlama duyarlığı** seçeneğine göre uygulanır.</span><span class="sxs-lookup"><span data-stu-id="47937-192">The adjustment limit is applied based on the **Rounding precision** option that is specified for the report definition.</span></span> <span data-ttu-id="47937-193">Örneğin, raporunuzu binlere yuvarlayıp **Ayarlama tutarı sınırı** alanına **2** girerseniz **Yuvarlama ayarlaması satırı** alanındaki değer 2.000'den fazla artarsa veya azalırsa bir uyarı mesajı alırsınız.</span><span class="sxs-lookup"><span data-stu-id="47937-193">For example, if you round your report to thousands and enter **2** in the **Adjustment amount limit** field, you receive a warning message when the value in the **Rounding adjustment row** field increases or decreases by more than 2,000.</span></span>

## <a name="format-row-and-column-text"></a><span data-ttu-id="47937-194">Satır ve sütun metnini biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="47937-194">Format row and column text</span></span>
<span data-ttu-id="47937-195">Raporlarınızın görünümünü yazı tiplerini değiştirip metni biçimlendirerek özelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47937-195">You can customize the appearance of your reports by changing fonts and formatting text.</span></span> <span data-ttu-id="47937-196">Aşağıdaki bölümlerde raporlardaki satırların ve sütunların görünümünün nasıl değiştirileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="47937-196">The following sections explain how to format the appearance of rows and columns on reports.</span></span>

### <a name="manage-font-styles"></a><span data-ttu-id="47937-197">Yazı tipi stillerini yönetme</span><span class="sxs-lookup"><span data-stu-id="47937-197">Manage font styles</span></span>

<span data-ttu-id="47937-198">Raporunuz için yazı tipi stilleri oluşturup bunları değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47937-198">You can create and modify font styles for your report.</span></span> <span data-ttu-id="47937-199">Ardından bu stilleri belgeye ya da rapordaki belirli bir satıra veya sütuna uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47937-199">You can then apply those styles to the document, or to a specific row or column on a report.</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="47937-200"><strong>Yazı tipi stili oluşturma</strong></span><span class="sxs-lookup"><span data-stu-id="47937-200"><strong>Create a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="47937-201">Rapor Tasarımcısı'nda, <strong>Biçim</strong> menüsünde, <strong>Stiller ve Biçimlendirme</strong>'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47937-201">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="47937-202"><strong>Stiller ve Biçimlendirme</strong> iletişim kutusunda, <strong>Yeni</strong>'ye tıklayın ve ardından yeni stil için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="47937-202">In the <strong>Styles and Formatting</strong> dialog box, click <strong>New</strong>, and then enter a unique name for the new style.</span></span></li>
<li><span data-ttu-id="47937-203">Yazı tipi seçimlerinizi yapın ve <strong>Tamam</strong>'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47937-203">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="47937-204"><strong>Bir yazı tipi stilini değiştirme</strong></span><span class="sxs-lookup"><span data-stu-id="47937-204"><strong>Modify a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="47937-205">Rapor Tasarımcısı'nda, <strong>Biçim</strong> menüsünde, <strong>Stiller ve Biçimlendirme</strong>'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47937-205">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="47937-206"><strong>Stiller ve Biçimlendirme</strong> iletişim kutusunda, değiştirmek için bir stil seçin ve ardından <strong>Değiştir</strong>'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47937-206">In the <strong>Styles and Formatting</strong> dialog box, select a style to modify, and then click <strong>Modify</strong>.</span></span></li>
<li><span data-ttu-id="47937-207">Yazı tipi seçimlerinizi yapın ve <strong>Tamam</strong>'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47937-207">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="47937-208"><strong>Bir yazı tipi stilini uygulama</strong></span><span class="sxs-lookup"><span data-stu-id="47937-208"><strong>Apply a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="47937-209">Rapor Tasarımcısı'ndaki bir tanımda veya sütun tanımında ya da üst bilgilerde ve alt bilgilerde bir veya daha fazla hücreyi seçin.</span><span class="sxs-lookup"><span data-stu-id="47937-209">In Report Designer, in a definition or column definition, or in headers and footers, select one or more cells.</span></span></li>
<li><span data-ttu-id="47937-210">Araç çubuğundaki <strong>Stil</strong> listesinden bir yazı tipi stili seçin.</span><span class="sxs-lookup"><span data-stu-id="47937-210">In the <strong>Style</strong> list on the toolbar, select a font style.</span></span></li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a><span data-ttu-id="47937-211">Satır metnini biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="47937-211">Format row text</span></span>

<span data-ttu-id="47937-212">Satır tanımında belirtilen biçimlendirme sütun tanımında ve rapor tanımında belirtilen her türlü biçimlendirmeyi geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="47937-212">The formatting that is specified in the row definition overrides any formatting that is specified in the column definition and the report definition.</span></span> <span data-ttu-id="47937-213">Metin biçimini biçimlendirme araç çubuğundaki kontrolleri kullanarak değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47937-213">You can modify the text format by using the controls on the formatting toolbar.</span></span> <span data-ttu-id="47937-214">Bu kontroller standart Microsoft Windows kontrolleridir.</span><span class="sxs-lookup"><span data-stu-id="47937-214">These controls are standard Microsoft Windows controls.</span></span>

1. <span data-ttu-id="47937-215">Rapor Tasarımcısı'nda, değiştirilecek satır tanımını açın.</span><span class="sxs-lookup"><span data-stu-id="47937-215">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="47937-216">Biçimlendirilecek satırları seçin.</span><span class="sxs-lookup"><span data-stu-id="47937-216">Select the cells to format.</span></span> <span data-ttu-id="47937-217">Birden fazla hücre seçmek için, hücreyi seçerken Ctrl tuşunu basılı tutun.</span><span class="sxs-lookup"><span data-stu-id="47937-217">To select multiple cells, hold down the Ctrl key while you select the cell.</span></span>
3. <span data-ttu-id="47937-218">Uygulanacak biçimin araç çubuğu düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47937-218">Click the toolbar button of the format to apply.</span></span> <span data-ttu-id="47937-219">Örneğin, bir satıra girinti vermek için satırı seçin ve araç çubuğundaki **Girintiyi Artır** ![Girintiyi Artır](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Girintiyi Artır") düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47937-219">For example, to indent a row, select the row, and then click **Increase Indent** ![Increase Indent](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Increase Indent") on the toolbar.</span></span>

### <a name="adjust-columns-while-you-design-reports"></a><span data-ttu-id="47937-220">Rapor tasarlarken sütunları ayarlama</span><span class="sxs-lookup"><span data-stu-id="47937-220">Adjust columns while you design reports</span></span>

<span data-ttu-id="47937-221">Satır tanımında üzerinde çalıştığınız sütunları görüntülemeyi kolaylaştırmak için, bir sütunun genişliğini ayarlayabilir ve aynı zamanda görünüm bölmesinde sütunları gizleyebilir (küçültebilir) veya gösterebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47937-221">To make it easier to view the columns that you're working on in the row definition, you can adjust the width of a column, and can also hide (minimize) or show columns in the view pane.</span></span> <span data-ttu-id="47937-222">Yaptığınız değişiklikler yalnızca sütunların ekrandaki görünümlerini etkiler.</span><span class="sxs-lookup"><span data-stu-id="47937-222">The modifications that you make affect only the on-screen appearance of the columns.</span></span> <span data-ttu-id="47937-223">Raporlardaki sütun biçimlendirmesini etkilemez.</span><span class="sxs-lookup"><span data-stu-id="47937-223">They don't affect the column formatting on reports.</span></span>

### <a name="change-the-width-of-a-column-in-the-view-pane"></a><span data-ttu-id="47937-224">Görünüm bölmesinde bir sütunun genişliğini değiştirme</span><span class="sxs-lookup"><span data-stu-id="47937-224">Change the width of a column in the view pane</span></span>

1. <span data-ttu-id="47937-225">Rapor Tasarımcısı'nda, değiştirilecek satır tanımını açın.</span><span class="sxs-lookup"><span data-stu-id="47937-225">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="47937-226">**Biçim** menüsünde, **Sütun Genişliği**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="47937-226">On the **Format** menu, select **Column Width**.</span></span>
3. <span data-ttu-id="47937-227">**Sütun Genişliği** iletişim kutusunda, bir değer girin ve ardından **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47937-227">In the **Column Width** dialog box, enter a value, and then click **OK**.</span></span> <span data-ttu-id="47937-228">Alternatif olarak, sütunun genişliğini değiştirmek için bir sütun başlığı hücresinin sağ sınırını sürükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47937-228">Alternatively, you can drag the right boundary of a column heading cell to change the width of the column.</span></span>

### <a name="hide-columns-in-the-view-pane"></a><span data-ttu-id="47937-229">Görünüm bölmesindeki sütunları gizleme</span><span class="sxs-lookup"><span data-stu-id="47937-229">Hide columns in the view pane</span></span>

1. <span data-ttu-id="47937-230">Rapor Tasarımcısı'nda, değiştirilecek satır tanımını açın.</span><span class="sxs-lookup"><span data-stu-id="47937-230">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="47937-231">Küçültülecek sütunu veya sütunları seçin.</span><span class="sxs-lookup"><span data-stu-id="47937-231">Select the column or columns to minimize.</span></span>
3. <span data-ttu-id="47937-232">Sağ tıklayın ve ardından **Gizle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47937-232">Right-click, and then click **Hide**.</span></span>

### <a name="show-all-hidden-columns-in-the-view-pane"></a><span data-ttu-id="47937-233">Görünüm bölmesindeki tüm gizli sütunları gösterme</span><span class="sxs-lookup"><span data-stu-id="47937-233">Show all hidden columns in the view pane</span></span>

1. <span data-ttu-id="47937-234">Rapor Tasarımcısı'nda, değiştirilecek satır tanımını açın.</span><span class="sxs-lookup"><span data-stu-id="47937-234">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="47937-235">Görüntülemek için küçültülen sütuna sağ tıklayın ve ardından **Göster**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47937-235">Right-click the minimized column to display, and then click **Unhide**.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="47937-236">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="47937-236">Additional resources</span></span>

[<span data-ttu-id="47937-237">Mali raporlama</span><span class="sxs-lookup"><span data-stu-id="47937-237">Financial reporting</span></span>](financial-reporting-intro.md)

