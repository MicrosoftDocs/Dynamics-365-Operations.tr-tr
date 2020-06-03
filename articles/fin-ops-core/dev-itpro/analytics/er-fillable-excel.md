---
title: Excel biçiminde belgeler oluşturmak için bir yapılandırma tasarlama
description: Bu konuda, bir Excel şablonunu doldurmak ve ardından giden Excel biçimi belgeleri oluşturmak için Elektronik raporlama (ER) biçiminin nasıl tasarlanacağı hakkında bilgi verilmektedir.
author: NickSelin
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e889b08f10c5d0c95fed7c9e422340706bdd154a
ms.sourcegitcommit: 67ce81c57194afb26a04ae4c0b7509e0efa32afc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2020
ms.locfileid: "3375825"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a><span data-ttu-id="c8e1d-103">Excel biçiminde belgeler oluşturmak için bir yapılandırma tasarlama</span><span class="sxs-lookup"><span data-stu-id="c8e1d-103">Design a configuration for generating documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c8e1d-104">Microsoft Excel çalışma kitabı biçiminde giden bir belge oluşturmak için yapılandırabileceğiniz bir ER [biçim bileşeni](general-electronic-reporting.md#FormatComponentOutbound) olan bir [Elektronik raporlama (ER)](general-electronic-reporting.md) biçimi yapılandırması tasarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) format configuration that has an ER [format component](general-electronic-reporting.md#FormatComponentOutbound) that you can configure to generate an outbound document in a Microsoft Excel workbook format.</span></span> <span data-ttu-id="c8e1d-105">Bu amaçla belirli ER biçimli bileşenler kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-105">Specific ER format components must be used for this purpose.</span></span>

<span data-ttu-id="c8e1d-106">Bu özellik hakkında daha fazla bilgi edinmek için [OPENXML biçiminde raporlar oluşturmak için yapılandırma tasarlama](tasks/er-design-reports-openxml-2016-11.md) konusundaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-106">To learn more about this feature, follow the steps in the topic, [Design a configuration for generating reports in OPENXML format](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="add-a-new-er-format"></a><span data-ttu-id="c8e1d-107">Yeni bir ER biçimi ekleme</span><span class="sxs-lookup"><span data-stu-id="c8e1d-107">Add a new ER format</span></span>

<span data-ttu-id="c8e1d-108">Excel çalışma kitabı biçiminde giden bir belge oluşturmak için yeni bir ER biçimi yapılandırması eklediğinizde biçimin **Biçim türü** özniteliği için **Excel** değerini seçmeniz veya **Biçim türü** özniteliğini boş bırakmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-108">When you add a new ER format configuration to generate an outbound document in an Excel workbook format, you must either select the **Excel** value for the **Format type** attribute of the format or leave the **Format type** attribute blank.</span></span>

- <span data-ttu-id="c8e1d-109">**Excel**'i seçerseniz giden belgeyi yalnızca Excel biçiminde oluşturacak şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-109">If you select **Excel**, you can configure the format to generate an outbound document only in Excel format.</span></span>
- <span data-ttu-id="c8e1d-110">Özniteliği boş bırakırsanız biçimi ER çerçevesi tarafından desteklenen herhangi bir biçimde, giden bir belge oluşturacak şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-110">If you leave the attribute blank, you can configure the format to generate an outbound document in any format that is supported by the ER framework.</span></span>

<span data-ttu-id="c8e1d-111">Yapılandırmanın ER biçimi bileşenini yapılandırmak için Eylem Bölmesi'nde **Tasarımcı**'yı seçin ve ER İşlem tasarımcısında düzenleme için ER biçimi bileşenini açın.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-111">To configure the ER format component of the configuration, select **Designer** on the Action Pane, and open the ER format component for editing in the ER Operation designer.</span></span>

![Yapılandırma sayfası](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a><span data-ttu-id="c8e1d-113">Excel dosya bileşeni</span><span class="sxs-lookup"><span data-stu-id="c8e1d-113">Excel file component</span></span>

### <a name="manual-entry"></a><span data-ttu-id="c8e1d-114">El ile yapılan giriş</span><span class="sxs-lookup"><span data-stu-id="c8e1d-114">Manual entry</span></span>

<span data-ttu-id="c8e1d-115">Excel biçiminde giden bir belge oluşturmak için yapılandırılmış ER biçimine bir **Excel\\File** bileşeni eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-115">You must add an **Excel\\File** component to the configured ER format to generate an outbound document in Excel format.</span></span>

![Excel\File bileşeni](./media/er-excel-format-add-file-component.png)

<span data-ttu-id="c8e1d-117">Giden belgenin düzenini belirtmek için giden belgelerin şablonu olarak **Excel\\File** bileşenine .xlsx uzantısına sahip bir Excel çalışma kitabı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-117">To specify the layout of the outbound document, attach an Excel workbook that has the .xlsx extension to the **Excel\\File** component as the template for outbound documents.</span></span>

> [!NOTE]
> <span data-ttu-id="c8e1d-118">Şablonu el ile eklediğinizde [ER parametreleri](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)'nde bu amaçla yapılandırılmış bir [belge türü](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-118">When you manually attach a template, you must use a [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) that has been configured for that purpose in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span></span>

![Excel\File bileşenine bir ek ekleme](./media/er-excel-format-add-file-component2.png)

<span data-ttu-id="c8e1d-120">Yapılandırılmış ER biçimini çalıştırdığınızda ekteki şablonun nasıl doldurulacağını belirtmek için **Excel\\File** bileşenine iç içe geçirilmiş **Sayfa**, **Aralık** ve **Hücre** bileşenleri eklemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-120">To specify how the attached template will be filled in when you run the configured ER format, you must add nested **Sheet**, **Range**, and **Cell** components to the **Excel\\File** component.</span></span> <span data-ttu-id="c8e1d-121">Her iç içe geçirilmiş bileşen, adlandırılmış bir Excel öğesi ile ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-121">Each nested component must be associated with an Excel named item.</span></span>

### <a name="template-import"></a><span data-ttu-id="c8e1d-122">Şablon içe aktarma</span><span class="sxs-lookup"><span data-stu-id="c8e1d-122">Template import</span></span>

<span data-ttu-id="c8e1d-123">Yeni bir şablonu boş bir ER biçimine aktarmak için Eylem Panosu'nun **İçe Aktar** sekmesinde **Excel'den İçe Aktar**'ı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-123">You can select **Import from Excel** on the **Import** tab of the Action Pane to import a new template into a blank ER format.</span></span> <span data-ttu-id="c8e1d-124">Bu örnekte, otomatik olarak bir **Excel\\File** bileşeni oluşturulacak ve içe aktarılan şablon buna eklenecektir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-124">In this example, an **Excel\\File** component will be created automatically, and the imported template will be attached to it.</span></span> <span data-ttu-id="c8e1d-125">Gereken tüm ER bileşenleri, keşfedilen adlandırılmış Excel öğelerinin listesine göre otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-125">All required ER components will also be created automatically, based on the list of Excel named items that are discovered.</span></span>

![Excel'den İçe Aktar'ı seçme](./media/er-excel-format-import-template.png)

> [!NOTE]
> <span data-ttu-id="c8e1d-127">İsteğe bağlı **Sayfa** öğesini, düzenlenebilir ER biçiminde oluşturmak istiyorsanız **Excel Sayfası biçim öğesi oluşturma** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-127">If you want to create the optional **Sheet** element in the editable ER format, set the **Create Excel Sheet format element** option to **Yes**.</span></span>

## <a name="sheet-component"></a><span data-ttu-id="c8e1d-128">Sayfa bileşeni</span><span class="sxs-lookup"><span data-stu-id="c8e1d-128">Sheet component</span></span>

<span data-ttu-id="c8e1d-129">**Sayfa** bileşeni, ekli Excel çalışma kitabının doldurulması gereken bir çalışma sayfasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-129">The **Sheet** component indicates a worksheet of the attached Excel workbook that must be filled in.</span></span> <span data-ttu-id="c8e1d-130">Excel şablonundaki çalışma sayfasının adı, bu bileşenin **Sayfa** özelliğinde tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-130">The name of the worksheet in an Excel template is defined in the **Sheet** property of this component.</span></span>

> [!NOTE]
> <span data-ttu-id="c8e1d-131">Bu bileşen, tek bir çalışma sayfası içeren Excel çalışma kitapları için isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-131">This component is optional for Excel workbooks that contain a single worksheet.</span></span>

<span data-ttu-id="c8e1d-132">ER İşlem tasarımcısının **Eşleme** sekmesinde, bileşenin oluşturulan bir belgeye konulması gerekip gerekmediğini belirtmek için bir **Sayfa** bileşeni için **Etkin** özelliğini yapılandırabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="c8e1d-132">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Sheet** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="c8e1d-133">**Etkin** özelliğinin bir ifadesi, çalışma zamanında **Doğru** değerini döndürecek şekilde yapılandırılmışsa veya hiçbir ifade yapılandırılmamışsa uygun çalışma sayfası, oluşturulan belgeye yerleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-133">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate worksheet will be put in the generated document.</span></span>
- <span data-ttu-id="c8e1d-134">**Etkin** özelliğinin bir ifadesi, çalışma zamanında **Yanlış** döndürecek şekilde yapılandırılırsa oluşturulan belge bir çalışma sayfası içermez.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-134">If an expression of the **Enabled** property is configured to return **False** at runtime, the generated document won't contain a worksheet.</span></span>

![Sayfa bileşeni örneği](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a><span data-ttu-id="c8e1d-136">Aralık bileşeni</span><span class="sxs-lookup"><span data-stu-id="c8e1d-136">Range component</span></span>

<span data-ttu-id="c8e1d-137">**Aralık** bileşeni, ER bileşeni tarafından kontrol edilmesi gereken bir Excel aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-137">The **Range** component indicates an Excel range that must be controlled by this ER component.</span></span> <span data-ttu-id="c8e1d-138">Aralığın adı, bu bileşenin **Excel aralığı** özelliğinde tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-138">The name of the range is defined in the **Excel range** property of this component.</span></span>

<span data-ttu-id="c8e1d-139">**Yineleme yönü** özelliği, aralığın oluşturulan bir belgede tekrarlanıp tekrarlanmayacağını ve nasıl tekrarlanacağını belirtir:</span><span class="sxs-lookup"><span data-stu-id="c8e1d-139">The **Replication direction** property specifies whether and how the range will be repeated in a generated document:</span></span>

- <span data-ttu-id="c8e1d-140">**Yineleme yönü** özelliği **Yineleme yok** olarak ayarlanırsa oluşturulan Excel'de uygun Excel aralığı yinelenmez.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-140">If the **Replication direction** property is set to **No replication**, the appropriate Excel range won't be repeated in the generated document.</span></span>
- <span data-ttu-id="c8e1d-141">**Yineleme yönü** özelliği **Dikey** olarak ayarlanırsa oluşturulan Excel'de uygun Excel aralığı yinelenir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-141">If the **Replication direction** property is set to **Vertical**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="c8e1d-142">Yinelenen her aralık, bir Excel şablonundaki orijinal aralığın altına yerleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-142">Every replicated range is put below the original range in an Excel template.</span></span> <span data-ttu-id="c8e1d-143">Yineleme sayısı, ER bileşenine bağlı **Kayıt listesi** türünün bir veri kaynağındaki kayıt sayısı ile tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-143">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>
- <span data-ttu-id="c8e1d-144">**Yineleme yönü** özelliği **Yatay** olarak ayarlanırsa oluşturulan Excel'de uygun Excel aralığı yinelenir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-144">If the **Replication direction** property is set to **Horizontal**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="c8e1d-145">Yinelenen her aralık, bir Excel şablonundaki orijinal aralığın sağına yerleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-145">Every replicated range is put to the right of the original range in an Excel template.</span></span> <span data-ttu-id="c8e1d-146">Yineleme sayısı, ER bileşenine bağlı **Kayıt listesi** türünün bir veri kaynağındaki kayıt sayısı ile tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-146">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>

<span data-ttu-id="c8e1d-147">Yatay yineleme hakkında daha fazla bilgi edinmek için [Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanma](tasks/er-horizontal-1.md) bölümündeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-147">To learn more about horizontal replication, follow the steps in [Use horizontally expandable ranges to dynamically add columns in Excel reports](tasks/er-horizontal-1.md).</span></span>

<span data-ttu-id="c8e1d-148">**Aralık** bileşeni, adlandırılmış uygun Excel aralıklarındaki değerleri girmek için kullanılan diğer iç içe geçirilmiş ER bileşenlerine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-148">The **Range** component can have other nested ER components that are used to enter values in the appropriate Excel named ranges.</span></span>

- <span data-ttu-id="c8e1d-149">Değerleri girmek için **Metin** grubunun herhangi bir bileşeni kullanılırsa değer, bir Excel aralığına metin değeri olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-149">If any component of the **Text** group is used to enter values, the value is entered in an Excel range as a text value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c8e1d-150">Girilen değerleri, uygulamada tanımlanan yerel ayara göre biçimlendirmek için bu deseni kullanın.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-150">Use this pattern to format entered values based on the locale that is defined in the application.</span></span>

- <span data-ttu-id="c8e1d-151">Değerleri girmek için **Excel** grubunun **Hücre** bileşeni kullanılıyorsa değer, bir Excel aralığına **Hücre** bileşeninin bağlanmasıyla tanımlanan veri türünün değeri olarak girilir (örneğin, **Dize**, **Gerçek** veya **Tamsayı**).</span><span class="sxs-lookup"><span data-stu-id="c8e1d-151">If the **Cell** component of the **Excel** group is used to enter values, the value is entered in an Excel range as a value of the data type that is defined by the binding of that **Cell** component (for example, **String**, **Real**, or **Integer**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="c8e1d-152">Excel uygulamasının, girilen değerleri giden belgeyi açan yerel bilgisayarın yerel ayarına göre biçimlendirmesini sağlamak için bu deseni kullanın.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-152">Use this pattern to enable the Excel application to format entered values based on the locale of the local computer that opens the outbound document.</span></span>

<span data-ttu-id="c8e1d-153">ER İşlem tasarımcısının **Eşleme** sekmesinde, bileşenin oluşturulan bir belgeye konulması gerekip gerekmediğini belirtmek için bir **Aralık** bileşeni için **Etkin** özelliğini yapılandırabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="c8e1d-153">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Range** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="c8e1d-154">**Etkin** özelliğinin bir ifadesi, çalışma zamanında **Doğru** değerini döndürecek şekilde yapılandırılmışsa veya hiçbir ifade yapılandırılmamışsa uygun aralık, oluşturulan belgeye doldurulur.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-154">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate range will be filled in in the generated document.</span></span>
- <span data-ttu-id="c8e1d-155">**Etkin** özelliğinin bir ifadesi, çalışma zamanında **Yanlış** değerini döndürecek şekilde yapılandırılmışsa ve bu aralık tüm satırları veya sütunları temsil etmiyorsa oluşturulan belge içinde uygun aralık doldurulmaz.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-155">If an expression of the **Enabled** property is configured to return **False** at runtime, and if this range doesn't represent the entire rows or columns, the appropriate range won't be filled in in the generated document.</span></span>
- <span data-ttu-id="c8e1d-156">**Etkin** özelliğinin bir ifadesi, çalışma zamanında **Yanlış** değerini döndürmek üzere yapılandırılmışsa ve bu aralık, tüm satırları veya sütunları temsil ediyorsa oluşturulan belge, bu satırları ve sütunları gizli satırlar ve sütunlar olarak içerir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-156">If an expression of the **Enabled** property is configured to return **False** at runtime, and this range represents the entire rows or columns, the generated document will contain those rows and columns as hidden rows and columns.</span></span>

## <a name="cell-component"></a><span data-ttu-id="c8e1d-157">Hücre bileşeni</span><span class="sxs-lookup"><span data-stu-id="c8e1d-157">Cell component</span></span>

<span data-ttu-id="c8e1d-158">**Hücre** bileşeni; adlandırılmış Excel hücrelerini, şekillerini ve resimlerini doldurmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-158">The **Cell** component is used to fill in Excel named cells, shapes, and pictures.</span></span> <span data-ttu-id="c8e1d-159">**Hücre** ER bileşeni tarafından doldurulması gereken bir adlandırılmış Excel nesnesini belirtmek için **Hücre** bileşeninin **Excel aralığı** özelliğinde bu nesnenin adını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-159">To indicate an Excel named object that must be filled in by a **Cell** ER component, you must specify the name of that object in the **Excel range** property of the **Cell** component.</span></span>

<span data-ttu-id="c8e1d-160">ER İşlem tasarımcısının **Eşleme** sekmesinde, nesnenin oluşturulan bir belge içine doldurulmasının gerekip gerekmediğini belirtmek üzere bir **Hücre** bileşeni için **Etkin** özelliğini yapılandırabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="c8e1d-160">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Cell** component to specify whether the object must be filled in in a generated document:</span></span>

- <span data-ttu-id="c8e1d-161">**Etkin** özelliğinin bir ifadesi, çalışma zamanında **Doğru** değerini döndürecek şekilde yapılandırılmışsa veya hiçbir ifade yapılandırılmamışsa uygun nesne, oluşturulan belgeye doldurulur.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-161">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate object will be filled in in the generated document.</span></span> <span data-ttu-id="c8e1d-162">Bu **Hücre** bileşeninin bağlanması, uygun nesneye koyulan bir değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-162">The binding of this **Cell** component specifies a value that is put in the appropriate object.</span></span>
- <span data-ttu-id="c8e1d-163">**Etkin** özelliğinin bir ifadesi, çalışma zamanında **Yanlış** döndürecek şekilde yapılandırılırsa uygun nesne oluşturulan belgeye doldurulmaz.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-163">If an expression of the **Enabled** property is configured to return **False** at runtime, the appropriate object won't be filled in in the generated document.</span></span>

<span data-ttu-id="c8e1d-164">**Hücre** bileşeni, hücreye bir değer girilecek şekilde yapılandırıldığında ilkel veri türünün değerini döndüren bir veri kaynağına bağlanabilir (örneğin, **Dize**, **Gerçek** veya **Tamsayı**).</span><span class="sxs-lookup"><span data-stu-id="c8e1d-164">When a **Cell** component is configured to enter a value in a cell, it can be bound with a data source that returns the value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="c8e1d-165">Bu durumda değer, hücreye aynı veri türünün değeri olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-165">In this case, the value is entered in the cell as a value of the same data type.</span></span>

<span data-ttu-id="c8e1d-166">**Hücre** bileşeni, bir Excel şekline bir değer girilecek şekilde yapılandırıldığında ilkel veri türünün değerini döndüren bir veri kaynağına bağlanabilir (örneğin, **Dize**, **Gerçek** veya **Tamsayı**).</span><span class="sxs-lookup"><span data-stu-id="c8e1d-166">When a **Cell** component is configured to enter a value in an Excel shape, it can be bound with a data source that returns a value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="c8e1d-167">Bu durumda değer, Excel şekline o şeklin metni olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-167">In this case, the value is entered in the Excel shape as the text of that shape.</span></span> <span data-ttu-id="c8e1d-168">**Dize** olmayan veri türlerinin değerleri için metne dönüştürme otomatik olarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-168">For values of data types that aren't **String**, the conversion to text is done automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="c8e1d-169">**Hücre** bileşenini, yalnızca şekil metni özelliğinin desteklendiği durumlarda bir şekli dolduracak şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-169">You can configure a **Cell** component to fill in a shape only in cases where a shape text property is supported.</span></span>

<span data-ttu-id="c8e1d-170">**Hücre** bileşeni, bir Excel resminde bir değer girilecek şekilde yapılandırıldığında ikili biçimdeki görüntüyü temsil eden **Kapsayıcı** veri türünün değerini döndüren bir veri kaynağına bağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-170">When a **Cell** component is configured to enter a value in an Excel picture, it can be bound with a data source that returns a value of the **Container** data type that represents an image in binary format.</span></span> <span data-ttu-id="c8e1d-171">Bu durumda değer, Excel resmine görüntü olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-171">In this case, the value is entered in the Excel picture as an image.</span></span>

> [!NOTE]
> <span data-ttu-id="c8e1d-172">Her Excel resmi ve şekli, sol üst köşesi tarafından belirli bir Excel hücresine veya aralığına tutturulmuş olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-172">Every Excel picture and shape is considered to be anchored by its upper-left corner to a specific Excel cell or range.</span></span> <span data-ttu-id="c8e1d-173">Excel resmini veya şeklini yinelemek istiyorsanız tutturulduğu hücreyi veya aralığı yinelenmiş hücre veya aralık olarak yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-173">If you want to replicate an Excel picture or shape, you must configure the cell or range that it's anchored to as a replicated cell or range.</span></span>

<span data-ttu-id="c8e1d-174">Görüntüleri ve şekilleri gömme hakkında daha fazla bilgi için, bkz. [ER kullanarak oluşturduğunuz belgelere resimler ve şekiller katıştırma](electronic-reporting-embed-images-shapes.md)</span><span class="sxs-lookup"><span data-stu-id="c8e1d-174">To learn more about how to embed images and shapes, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="page-break-component"></a><span data-ttu-id="c8e1d-175">Sayfa sonu bileşeni</span><span class="sxs-lookup"><span data-stu-id="c8e1d-175">Page break component</span></span>

<span data-ttu-id="c8e1d-176">**PageBreak** bileşeni, Excel'i yeni bir sayfa başlatmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-176">The **PageBreak** component forces Excel to start a new page.</span></span> <span data-ttu-id="c8e1d-177">Excel'in varsayılan sayfalandırmasını kullanmak istediğinizde bu bileşen gerekli değildir ancak Excel'in, ER biçiminizle sayfalandırmayı yapılandırmasını istediğinizde bunu kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-177">This component isn't required when you want to use Excel's default paging, but you should use it when you want Excel to follow your ER format to structure paging.</span></span>

## <a name="edit-an-added-er-format"></a><span data-ttu-id="c8e1d-178">Eklenen bir ER biçimini düzenleme</span><span class="sxs-lookup"><span data-stu-id="c8e1d-178">Edit an added ER format</span></span>

### <a name="update-a-template"></a><span data-ttu-id="c8e1d-179">Şablon güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c8e1d-179">Update a template</span></span>

<span data-ttu-id="c8e1d-180">Güncelleştirilmiş bir şablonu düzenlenebilir bir ER biçimine aktarmak için Eylem Panosu'nun **İçe Aktar** sekmesinde **Excel'den Güncelleştir**'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-180">You can select **Update from Excel** on the **Import** tab of the Action Pane to import an updated template into an editable ER format.</span></span> <span data-ttu-id="c8e1d-181">Bu işlem sırasında, seçili **Excel\\Dosya** bileşeninin bir şablonu yeni bir şablonla değiştirilecektir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-181">During this process, a template of the selected **Excel\\File** component will be replaced by a new template.</span></span> <span data-ttu-id="c8e1d-182">Düzenlenebilir ER biçiminin içeriği, güncelleştirilmiş ER şablonunun içeriği ile senkronize edilecektir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-182">The content of the editable ER format will be synced with the content of the updated ER template.</span></span>

- <span data-ttu-id="c8e1d-183">ER biçimi bileşeni, düzenlenebilir biçimde bulunmazsa her Excel adı için otomatik olarak yeni bir ER biçimi bileşeni oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-183">A new ER format component will automatically be created for every Excel name if the ER format component isn't found in the editable format.</span></span>
- <span data-ttu-id="c8e1d-184">Her ER biçimi bileşeni, uygun Excel adı bulunamazsa düzenlenebilir ER biçiminden silinir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-184">Every ER format component will be deleted from the editable ER format if the appropriate Excel name isn't found for it.</span></span>

> [!NOTE]
> <span data-ttu-id="c8e1d-185">Düzenlenebilir ER biçiminde isteğe bağlı **Sayfa** öğesi oluşturmak istiyorsanız **Excel Sayfası biçim öğesi oluşturma** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-185">Set the **Create Excel Sheet format element** option to **Yes** if you want to create the optional **Sheet** element in the editable ER format.</span></span>
>
> <span data-ttu-id="c8e1d-186">Düzenlenebilir ER biçimi, başlangıçta **Sayfa** öğeleri içeriyorsa güncelleştirilmiş bir şablonu içe aktardığınızda **Excel Sayfası biçim öğesi oluşturma** seçeneğini **Evet** olarak ayarlamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-186">If the editable ER format originally contained **Sheet** elements, we recommend that you set the **Create Excel Sheet format element** option to **Yes** when you import an updated template.</span></span> <span data-ttu-id="c8e1d-187">Aksi takdirde, özgün **Sayfa** öğesinin tüm iç içe geçirilmiş öğeleri sıfırdan oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-187">Otherwise, all nested elements of the original **Sheet** element will be created from scratch.</span></span> <span data-ttu-id="c8e1d-188">Bu nedenle, yeniden oluşturulan biçim öğelerinin tüm bağları güncelleştirilmiş ER biçiminde kaybolacaktır.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-188">Therefore, all bindings of the re-created format elements will be lost in the updated ER format.</span></span>

![Excel iletişim kutusundan Güncelleştir'de Excel Çalışma Sayfası biçim öğesi oluşturma seçeneği](./media/er-excel-format-update-template.png)

<span data-ttu-id="c8e1d-190">Bu özellik hakkında daha fazla bilgi edinmek için [Excel şablonlarını yeniden uygulayarak Elektronik raporlama biçimlerini değiştirme](modify-electronic-reporting-format-reapply-excel-template.md) bölümündeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-190">To learn more about this feature, follow the steps in [Modify Electronic reporting formats by reapplying Excel templates](modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

## <a name="validate-an-er-format"></a><span data-ttu-id="c8e1d-191">ER biçimini doğrulama</span><span class="sxs-lookup"><span data-stu-id="c8e1d-191">Validate an ER format</span></span>

<span data-ttu-id="c8e1d-192">Düzenlenebilir bir ER biçimini doğruladığınızda Excel adının şu anda kullanılan Excel şablonunda bulunduğundan emin olmak için bir tutarlılık denetimi yapılır.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-192">When you validate an ER format that can be edited, a consistency check is done to make sure that the Excel name is present in the Excel template that is currently used.</span></span> <span data-ttu-id="c8e1d-193">Herhangi bir tutarsızlık size bildirilecektir.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-193">You will be notified about any inconsistencies.</span></span> <span data-ttu-id="c8e1d-194">Bazı tutarsızlıklar için sorunları otomatik olarak düzeltme seçeneği sunulur.</span><span class="sxs-lookup"><span data-stu-id="c8e1d-194">For some inconsistencies, the option to automatically fix issues will be offered.</span></span>

![Doğrulama hatası iletisi](./media/er-excel-format-validate.png)


## <a name="additional-resources"></a><span data-ttu-id="c8e1d-196">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c8e1d-196">Additional resources</span></span>

[<span data-ttu-id="c8e1d-197">Elektronik Raporlamaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="c8e1d-197">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="c8e1d-198">OPENXML formatında raporların oluşturulması için bir yapılandırma tasarlama</span><span class="sxs-lookup"><span data-stu-id="c8e1d-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks\er-design-reports-openxml-2016-11.md)

[<span data-ttu-id="c8e1d-199">Excel şablonlarını yeniden uygulayarak Elektronik raporlama biçimlerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="c8e1d-199">Modify Electronic reporting formats by reapplying Excel templates</span></span>](modify-electronic-reporting-format-reapply-excel-template.md)

[<span data-ttu-id="c8e1d-200">Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanma</span><span class="sxs-lookup"><span data-stu-id="c8e1d-200">Use horizontally expandable ranges to dynamically add columns in Excel reports</span></span>](tasks/er-horizontal-1.md)

[<span data-ttu-id="c8e1d-201">Er kullanarak oluşturduğunuz belgelere resimler ve şekiller katıştırma</span><span class="sxs-lookup"><span data-stu-id="c8e1d-201">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md)

[<span data-ttu-id="c8e1d-202">Power BI'a veri çekmek için Elektronik raporlamayı (ER) yapılandırma</span><span class="sxs-lookup"><span data-stu-id="c8e1d-202">Configure Electronic reporting (ER) to pull data into Power BI</span></span>](general-electronic-reporting-report-configuration-get-data-powerbi.md)
