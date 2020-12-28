---
title: Her tüzel kişilik için belirtilen parametreleri kullanmak için ER biçimlerini yapılandırma
description: Bu konu, Elektronik raporlama (ER) biçimlerini her tüzel kişilik için belirtilen parametreleri kullanacak şekilde nasıl yapılandıracağınızı açıklar.
author: NickSelin
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 0ed1442403ae82dfc820212e3e235737f37f21a4
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679738"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a><span data-ttu-id="5623e-103">Her tüzel kişilik için belirtilen parametreleri kullanmak için ER biçimlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5623e-103">Configure ER formats to use parameters that are specified per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="5623e-104">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="5623e-104">Overview</span></span>

<span data-ttu-id="5623e-105">Tasarlayacağınız Elektronik raporlama (ER) biçimlerinin çoğunda, kurulumunuzun her bir tüzel kişiliğine özgü bir değer kümesi kullanarak verileri filtrelemelisiniz (örneğin, vergi hareketlerini filtrelemek için bir vergi kodu kümesi).</span><span class="sxs-lookup"><span data-stu-id="5623e-105">In many of the Electronic reporting (ER) formats that you will design, you must filter data by using a set of values that are specific to each legal entity of your instance (for example, a set of tax codes to filter tax transactions).</span></span> <span data-ttu-id="5623e-106">Şu anda, bu tür filtreleme bir ER biçiminde yapılandırıldığında tüzel kişiliğe bağlı değerler (örneğin vergi kodları) ER biçiminin ifadelerinde veri filtreleme kurallarını belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5623e-106">Currently, when filtering of this type is configured in an ER format, values that are dependent on the legal entity (for example, tax codes) are used in expressions of the ER format to specify data filtering rules.</span></span> <span data-ttu-id="5623e-107">Bu nedenle, ER biçimi tüzel kişiliğe özgü yapılır ve gerekli raporları oluşturmak için ER biçimini çalıştırmanız gereken her tüzel kişilik için orijinal ER biçiminin türetilmiş kopyalarını oluşturmalısınız.</span><span class="sxs-lookup"><span data-stu-id="5623e-107">Therefore, the ER format is made legal entity–specific, and to generate the required reports, you must create derived copies of the original ER format for each legal entity where you have to run the ER format.</span></span> <span data-ttu-id="5623e-108">Her türetilmiş ER biçimi; tüzel kişiliğe özgü değerleri içine alacak şekilde düzenlenmeli, orijinal (temel) sürüm güncellendiğinde yeniden yayınlanmalı, bir test ortamından dışa aktarılmalı ve üretim kullanımı için dağıtılması gerektiğinde bir üretim ortamına içe aktarılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5623e-108">Each derived ER format must be edited to bring legal entity–specific values into it, rebased whenever the original (base) version has been updated, exported from a test environment and imported into a production environment when it must be deployed for production use, and so on.</span></span> <span data-ttu-id="5623e-109">Bu nedenle, bu tür yapılandırılmış ER çözümünün bakımı çeşitli nedenlerden dolayı oldukça karmaşık ve zaman alıcıdır:</span><span class="sxs-lookup"><span data-stu-id="5623e-109">Therefore, maintenance of this type of configured ER solution is quite complex and time-consuming for several reasons:</span></span>

-   <span data-ttu-id="5623e-110">Ne kadar çok tüzel kişilik varsa o kadar çok ER biçim yapılandırması korunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5623e-110">The more legal entities there are, the more ER format configurations must be maintained.</span></span>
-   <span data-ttu-id="5623e-111">ER yapılandırmalarının bakımı, iş kullanıcılarının ER bilgisine sahip olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="5623e-111">Maintenance of ER configurations requires that business users have ER knowledge.</span></span>

<span data-ttu-id="5623e-112">ER uygulamasına özgü parametreler özelliği, yetkili kullanıcıların veri filtrelemelerini bir dizi soyut kurala göre ER biçiminde yapılandırmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="5623e-112">The ER application-specific parameters feature lets power users configure data filtering in an ER format so that it's based on a set of abstract rules.</span></span> <span data-ttu-id="5623e-113">Bu kurallar kümesi, bir ER biçiminde mevcut olan veri kaynaklarını kullanmak için yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="5623e-113">This set of rules can be configured to use the data sources that are available in an ER format.</span></span> <span data-ttu-id="5623e-114">İş kullanıcıları daha sonra, karşılık gelen ER biçimi ayarlarına ve ER biçiminin veri kaynakları tarafından erişilecek olan mevcut tüzel kişilik verilerine dayanarak otomatik olarak oluşturulan kullanıcı arabirimini (UI) kullanarak ER çerçevesinin ötesinde gerçek kurallar belirleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="5623e-114">Business users can then specify real rules beyond the ER framework by using the user interface (UI) that is automatically generated based on the settings of the corresponding ER format and the current legal entity data that will be accessed by the ER format's data sources.</span></span> <span data-ttu-id="5623e-115">ER biçimi için belirtilen kurallar kümesi Dynamics 365 Finance (Finance) kurulumunun geçerli tüzel kişiliğinden dışa aktarılabilir.</span><span class="sxs-lookup"><span data-stu-id="5623e-115">The set of rules that is specified for an ER format can be exported from the current legal entity of the Dynamics 365 Finance (Finance) instance.</span></span> <span data-ttu-id="5623e-116">Bu daha sonra, aynı Finance kurulumunun ya da aynı ER biçiminin bir kurallar kümesi olarak farklı bir kurulumun başka bir tüzel kişiliğine içe aktarılabilir.</span><span class="sxs-lookup"><span data-stu-id="5623e-116">It can then be imported into another legal entity of either the same Finance instance or a different instance as a set of rules for the same ER format.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5623e-117">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="5623e-117">Prerequisites</span></span>

<span data-ttu-id="5623e-118">Bu konudaki örnekleri tamamlamak üzere aşağıdaki rollerden biri için Finance ile aynı kiracıya sağlanan Regulatory Configuration Services (RCS) kurulumuna erişiminiz olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="5623e-118">To complete the examples in this topic, you must have access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>

- <span data-ttu-id="5623e-119">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="5623e-119">Electronic reporting developer</span></span>
- <span data-ttu-id="5623e-120">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="5623e-120">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="5623e-121">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="5623e-121">System administrator</span></span>

<span data-ttu-id="5623e-122">[HESAPLANAN ALAN türüne göre ER veri kaynaklarının parametreli çağrılarını destekleme](er-calculated-field-type.md) konusundaki adımları tamamlamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="5623e-122">We recommend that you complete the steps in the [Support parameterized calls of ER data sources of CALCULATED FIELD type](er-calculated-field-type.md) topic.</span></span> <span data-ttu-id="5623e-123">Bu adımları zaten tamamladıysanız takip eden **ER yapılandırmalarını RCS'ye içe aktarma** bölümündeki adımları atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5623e-123">If you've already completed those steps, you can skip the steps in the **Import ER configurations into RCS** section that follows.</span></span>

## <a name="import-er-configurations-into-rcs"></a><span data-ttu-id="5623e-124">ER yapılandırmalarını RCS'ye içe aktarma</span><span class="sxs-lookup"><span data-stu-id="5623e-124">Import ER configurations into RCS</span></span>

<span data-ttu-id="5623e-125">[Microsoft İndirme Merkezi](https://go.microsoft.com/fwlink/?linkid=851448)'nden **HESAPLANAN ALAN türüne göre ER veri kaynaklarının parametreli çağrılarını destekleme** zip dosyasını indirin.</span><span class="sxs-lookup"><span data-stu-id="5623e-125">From [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=851448), download the **Support parameterized calls of ER data sources of CALCULATED FIELD type** zip file.</span></span> <span data-ttu-id="5623e-126">Bu zip dosyası, ayıklanması ve yerel olarak depolanması gereken aşağıdaki ER yapılandırmalarını içerir.</span><span class="sxs-lookup"><span data-stu-id="5623e-126">This zip file contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="5623e-127">**İçerik açıklaması**</span><span class="sxs-lookup"><span data-stu-id="5623e-127">**Content description**</span></span>                        | <span data-ttu-id="5623e-128">**Dosya adı**</span><span class="sxs-lookup"><span data-stu-id="5623e-128">**File name**</span></span>                                        |
|------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5623e-129">Örnek **ER veri modeli** yapılandırma dosyası</span><span class="sxs-lookup"><span data-stu-id="5623e-129">Sample **ER data model** configuration file</span></span>    | <span data-ttu-id="5623e-130">Parametreleştirilmiş calls.version.1.xml öğrenme modeli</span><span class="sxs-lookup"><span data-stu-id="5623e-130">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="5623e-131">Örnek **ER meta verisi** yapılandırma dosyası</span><span class="sxs-lookup"><span data-stu-id="5623e-131">Sample **ER metadata** configuration file</span></span>      | <span data-ttu-id="5623e-132">Parametreleştirilmiş calls.version.1.xml öğrenmek için meta veri</span><span class="sxs-lookup"><span data-stu-id="5623e-132">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="5623e-133">Örnek **ER model eşlemesi** yapılandırma dosyası</span><span class="sxs-lookup"><span data-stu-id="5623e-133">Sample **ER model mapping** configuration file</span></span> | <span data-ttu-id="5623e-134">Parametreleştirilmiş calls.version.1.xml öğrenmek için eşleme</span><span class="sxs-lookup"><span data-stu-id="5623e-134">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="5623e-135">Örnek **ER biçimi** yapılandırması</span><span class="sxs-lookup"><span data-stu-id="5623e-135">Sample **ER format** configuration</span></span>             | <span data-ttu-id="5623e-136">Parametreleştirilmiş calls.version.1.xml öğrenmek için biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="5623e-136">Format to learn parameterized calls.version.1.1.xml</span></span>  |

<span data-ttu-id="5623e-137">Ardından, RCS kurulumunuzda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="5623e-137">Next, sign in to your RCS instance.</span></span>

<span data-ttu-id="5623e-138">Bu örnekte, Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="5623e-138">In this example, you will create a configuration for the Litware, Inc sample company.</span></span> <span data-ttu-id="5623e-139">Bu prosedürü tamamlamadan önce RCS'deki [Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) konusundaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5623e-139">Before you can complete this procedure, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic in RCS.</span></span>

1.  <span data-ttu-id="5623e-140">Varsayılan panoda **Elektronik raporlama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-140">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="5623e-141">**Raporlama yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-141">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="5623e-142">Daha önce indirdiğiniz ER yapılandırmalarını aşağıdaki sırayla RCS'ye içe aktarın: veri modeli, meta veriler, model eşleme ve biçim.</span><span class="sxs-lookup"><span data-stu-id="5623e-142">Import the ER configurations that you downloaded earlier into RCS, in the following order: data model, metadata, model mapping, and format.</span></span> <span data-ttu-id="5623e-143">Her bir ER yapılandırması için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="5623e-143">For each ER configuration, follow these steps:</span></span>

    1.  <span data-ttu-id="5623e-144">**Döviz**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-144">Select **Exchange**.</span></span>
    2.  <span data-ttu-id="5623e-145">**XML dosyasından yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-145">Select **Load from XML file**.</span></span>
    3.  <span data-ttu-id="5623e-146">Gerekli ER yapılandırması için XML biçimindeki dosyayı seçmek üzere **Gözat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-146">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    4.  <span data-ttu-id="5623e-147">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-147">Select **OK**.</span></span>

## <a name="review-the-er-solution-that-is-provided"></a><span data-ttu-id="5623e-148">Sağlanan ER çözümünü gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="5623e-148">Review the ER solution that is provided</span></span>

1.  <span data-ttu-id="5623e-149">Yapılandırma ağacında, **Parametreli çağrıları öğrenme modeli** öğesinin içeriğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="5623e-149">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="5623e-150">**Parametreli çağrıları öğrenmek için biçimlendirme** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-150">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="5623e-151">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-151">Select **Designer**.</span></span>
4.  <span data-ttu-id="5623e-152">**Genişlet/Daralt**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-152">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="5623e-153">**Parametreli çağrıları öğrenmek için biçimlendirme** ER biçimi, çeşitli vergilendirme düzeylerini (normal, azaltılmış ve yok) sunan XML biçiminde bir vergi beyannamesi oluşturmak için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="5623e-153">The **Format to learn parameterized calls** ER format is designed to generate a tax statement in XML format that presents several levels of taxation (regular, reduced, and none).</span></span> <span data-ttu-id="5623e-154">Her düzey farklı ayrıntılara sahiptir.</span><span class="sxs-lookup"><span data-stu-id="5623e-154">Each level has a different number of details.</span></span>

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  <span data-ttu-id="5623e-156">**Eşleme** sekmesinde **Model**, **Veri** ve **Özet** öğelerini genişletin.</span><span class="sxs-lookup"><span data-stu-id="5623e-156">On the **Mapping** tab, expand the **Model**, **Data**, and **Summary** items.</span></span>

    <span data-ttu-id="5623e-157">**Model. Data. Summary** veri kaynağı, vergi hareketleri listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5623e-157">The **Model.Data.Summary** data source returns the list of tax transactions.</span></span> <span data-ttu-id="5623e-158">Bu hareketler vergi koduna göre özetlenir.</span><span class="sxs-lookup"><span data-stu-id="5623e-158">These transactions are summarized by tax code.</span></span> <span data-ttu-id="5623e-159">Bu veri kaynağı için **Model.Data.Summary.Level** hesaplanan alanı, her özetlenen kaydın vergilendirme düzeyine ilişkin kodu döndürecek şekilde yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="5623e-159">For this data source, the **Model.Data.Summary.Level** calculated field has been configured to return the code for the taxation level of each summarized record.</span></span> <span data-ttu-id="5623e-160">Çalışma zamanında **Model.Data.Summary** veri kaynağından alınabilecek herhangi bir vergi kodu için hesaplanan alan vergilendirme düzeyi kodunu (**Normal**, **Azaltılmış**, **Yok** veya **Diğer**) metin değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="5623e-160">For any tax code that can be retrieved from the **Model.Data.Summary** data source at runtime, the calculated field returns the taxation level code (**Regular**, **Reduced**, **None**, or **Other**) as a text value.</span></span> <span data-ttu-id="5623e-161">**Model.Data.Summary.Level** hesaplanan alanı, **Model.Data.Summary** veri kaynağının kayıtlarını filtrelemek ve **Model.Data2.Level1**, **Model.Data2.Level2** ve **Model.Data2.Level3** alanlarını kullanarak vergilendirme düzeyini temsil eden her XML öğesinde filtrelenmiş verileri girmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5623e-161">The **Model.Data.Summary.Level** calculated field is used to filter records of the **Model.Data.Summary** data source and enter the filtered data in each XML element that represents a taxation level by using the **Model.Data2.Level1**, **Model.Data2.Level2**, and **Model.Data2.Level3** fields.</span></span>

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    <span data-ttu-id="5623e-163">**Model.Data.Summary.Level** hesaplanan alanı bir ER ifadesi içerecek şekilde yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="5623e-163">The **Model.Data.Summary.Level** calculated field has been configured so that it contains an ER expression.</span></span> <span data-ttu-id="5623e-164">Vergi kodlarının (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD** ve **InVAT0**) bu yapılandırmaya sabit kodlandığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="5623e-164">Note that tax codes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD**, and **InVAT0**) are hardcoded into this configuration.</span></span> <span data-ttu-id="5623e-165">Bu nedenle, bu ER biçimi belirtilen vergi kodlarının yapılandırıldığı tüzel kişiliğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="5623e-165">Therefore, this ER format is dependent on the legal entity where these tax codes were configured.</span></span>

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    <span data-ttu-id="5623e-167">Her tüzel kişiliğe ait farklı vergi kodları kümesini desteklemek için aşağıdaki adımları izlemelisiniz:</span><span class="sxs-lookup"><span data-stu-id="5623e-167">To support a different set of tax codes for each legal entity, you must follow these steps:</span></span>

    - <span data-ttu-id="5623e-168">Her tüzel kişilik için ER biçiminin türetilmiş bir sürümünü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5623e-168">Create a derived version of the ER format for each legal entity.</span></span>
    - <span data-ttu-id="5623e-169">Tüzel kişilik ayarını temel alarak **Model.Data.Summary.Level** hesaplanan alanındaki vergi kodlarını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="5623e-169">Update the tax codes in the **Model.Data.Summary.Level** calculated field, based on the legal entity setting.</span></span>

6.  <span data-ttu-id="5623e-170">**Biçim tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="5623e-170">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="5623e-171">Türetilmiş biçim oluşturma</span><span class="sxs-lookup"><span data-stu-id="5623e-171">Create a derived format</span></span>

<span data-ttu-id="5623e-172">Ardından, her tüzel kişilik için farklı bir vergi kodu setini tek bir ER biçiminde desteklemek için ER uygulamasına özgü parametreler özelliğini kullanacaksınız.</span><span class="sxs-lookup"><span data-stu-id="5623e-172">Next, you will use the ER application-specific parameters feature to support a different set of tax codes for each legal entity in a single ER format.</span></span>

1.  <span data-ttu-id="5623e-173">Yapılandırma ağacında, **Parametreli çağrıları öğrenme modeli** öğesinin içeriğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="5623e-173">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="5623e-174">**Parametreli çağrıları öğrenmek için biçimlendirme** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-174">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="5623e-175">**Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-175">Select **Create configuration**.</span></span>
4.  <span data-ttu-id="5623e-176">**Ad'dan Türet: Parametreli çağrıları öğrenme biçimi, Microsoft** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="5623e-176">Select the **Derive from Name: Format to learn parameterized calls, Microsoft** option.</span></span>
5.  <span data-ttu-id="5623e-177">**Ad** alanına **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** yazın.</span><span class="sxs-lookup"><span data-stu-id="5623e-177">In the **Name** field, enter **Format to learn how to lookup LE data**.</span></span>
6.  <span data-ttu-id="5623e-178">**Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-178">Select **Create configuration**.</span></span>

## <a name="configure-a-derived-format"></a><span data-ttu-id="5623e-179">Türetilmiş biçim yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5623e-179">Configure a derived format</span></span>

### <a name="add-a-format-enumeration"></a><span data-ttu-id="5623e-180">Biçim numaralandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="5623e-180">Add a format enumeration</span></span>

<span data-ttu-id="5623e-181">Ardından, yeni bir ER biçim numaralandırması ekleyeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="5623e-181">Next, you will add a new ER format enumeration.</span></span> <span data-ttu-id="5623e-182">Bu biçim numaralandırma değerleri, ER biçiminde kullanılan çeşitli vergilendirme düzeyleri için tüzel kişiliğe bağlı vergi kodu setlerini belirten iş kullanıcılarına sunulur.</span><span class="sxs-lookup"><span data-stu-id="5623e-182">The values of this format enumeration will be presented to business users, who will specify legal entity–dependent sets of tax codes for the various taxation levels that are used in the ER format.</span></span>

1.  <span data-ttu-id="5623e-183">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-183">Select **Designer**.</span></span>
2.  <span data-ttu-id="5623e-184">**Biçim numaralandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-184">Select **Format enumerations**.</span></span>
3.  <span data-ttu-id="5623e-185">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-185">Select **Add**.</span></span>
4.  <span data-ttu-id="5623e-186">**Ad** alanına **Vergilendirme düzeyleri listesi** yazın.</span><span class="sxs-lookup"><span data-stu-id="5623e-186">In the **Name** field, enter **List of taxation levels**.</span></span>
5.  <span data-ttu-id="5623e-187">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-187">Select **Save**.</span></span>
6.  <span data-ttu-id="5623e-188">**Biçim numaralandırması değerleri** sekmesinde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-188">On the **Format enumeration values** tab, select **Add**.</span></span>
7.  <span data-ttu-id="5623e-189">**Ad** alanına **Normal vergilendirme** yazın.</span><span class="sxs-lookup"><span data-stu-id="5623e-189">In the **Name** field, enter **Regular taxation**.</span></span>
8.  <span data-ttu-id="5623e-190">Yeniden **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-190">Select **Add** again.</span></span>
9.  <span data-ttu-id="5623e-191">**Ad** alanına **Azaltılmış vergilendirme** yazın.</span><span class="sxs-lookup"><span data-stu-id="5623e-191">In the **Name** field, enter **Reduced taxation**.</span></span>
10. <span data-ttu-id="5623e-192">Yeniden **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-192">Select **Add** again.</span></span>
11. <span data-ttu-id="5623e-193">**Ad** alanına **Vergilendirme yok** yazın.</span><span class="sxs-lookup"><span data-stu-id="5623e-193">In the **Name** field, enter **No taxation**.</span></span>
12. <span data-ttu-id="5623e-194">Yeniden **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-194">Select **Add** again.</span></span>
13. <span data-ttu-id="5623e-195">**Ad** alanına, **Diğer** yazın.</span><span class="sxs-lookup"><span data-stu-id="5623e-195">In the **Name** field, enter **Other**.</span></span>

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    <span data-ttu-id="5623e-197">İş kullanıcıları, tüzel kişiliğe bağlı vergi kodu kümelerini belirlemek için farklı dilleri kullanabileceğinden, bu numaralandırma değerlerini Finance'taki kullanıcılar için tercih edilen dil olarak yapılandırılmış dillere çevirmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="5623e-197">Because the business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the values of this enumeration into the languages that are configured as the preferred languages for those users in Finance.</span></span>

14. <span data-ttu-id="5623e-198">**Vergilendirme yok** kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-198">Select the **No taxation** record.</span></span>
15. <span data-ttu-id="5623e-199">**Etiket** alanına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5623e-199">Click in the **Label** field.</span></span>
16. <span data-ttu-id="5623e-200">**Çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-200">Select **Translate**.</span></span>
17. <span data-ttu-id="5623e-201">**Metin çevirisi** bölmesinde, **Etiket Kodu** alanına **LBL_LEVELENUM_NO** yazın.</span><span class="sxs-lookup"><span data-stu-id="5623e-201">In the **Text translation** pane, in the **Label Id** field, enter **LBL_LEVELENUM_NO**.</span></span>
18. <span data-ttu-id="5623e-202">**Varsayılan dilde metin** alanına **Vergilendirme yok** yazın.</span><span class="sxs-lookup"><span data-stu-id="5623e-202">In the **Text in default language** field, enter **No taxation**.</span></span>
19. <span data-ttu-id="5623e-203">**Dil** alanında, **DE**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-203">In the **Language** field, select **DE**.</span></span>
20. <span data-ttu-id="5623e-204">**Çevrilen metin** alanına, **keine Besteuerung** yazın.</span><span class="sxs-lookup"><span data-stu-id="5623e-204">In the **Translated text** field, enter **keine Besteuerung**.</span></span>
21. <span data-ttu-id="5623e-205">**Çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-205">Select **Translate**.</span></span>

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. <span data-ttu-id="5623e-207">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-207">Select **Save**.</span></span>
23. <span data-ttu-id="5623e-208">**Biçim numaralandırmaları** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="5623e-208">Close the **Format enumerations** page.</span></span>

### <a name="add-a-new-lookup-data-source"></a><span data-ttu-id="5623e-209">Yeni bir veri kaynağı araması ekleme</span><span class="sxs-lookup"><span data-stu-id="5623e-209">Add a new lookup data source</span></span>

<span data-ttu-id="5623e-210">Ardından, iş kullanıcılarının özetlenen her hareket kaydı için doğru vergilendirme düzeyini tanıyacak şekilde tüzel kişiliğe bağlı kuralları nasıl belirteceğini belirlemek için yeni bir veri kaynağı ekleyeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="5623e-210">Next, you will add a new data source to specify how business users will specify legal entity–dependent rules to recognize the correct taxation level for each summarized transaction record.</span></span>

1.  <span data-ttu-id="5623e-211">**Eşleme** sekmesinde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-211">On the **Mapping** tab, select **Add**.</span></span>
2.  <span data-ttu-id="5623e-212">**Biçim numaralandırması\Arama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-212">Select **Format enumeration\Lookup**.</span></span>

    <span data-ttu-id="5623e-213">Az önce, iş kullanıcılarının vergilendirme düzeyi kabulü için belirlediği her kuralın bir ER biçim numaralandırması değeri döndüreceğini tanımladınız.</span><span class="sxs-lookup"><span data-stu-id="5623e-213">You just identified that each rule that business users specify for taxation level recognition will return a value of an ER format enumeration.</span></span> <span data-ttu-id="5623e-214">**Biçim numaralandırma** bloğuna ek olarak, **Arama** veri kaynağı türüne **Veri modeli** ve **Dynamics 365 for Operations** blokları altından erişilebildiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="5623e-214">Notice that the **Lookup** data source type can be accessed under the **Data model** and **Dynamics 365 for Operations** blocks in addition to the **Format enumeration** block.</span></span> <span data-ttu-id="5623e-215">Bu nedenle, ER veri modeli numaralandırmaları ve uygulama numaralandırmaları, bu tür veri kaynakları için döndürülen değer türlerini belirtmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5623e-215">Therefore, ER data model enumerations and application enumerations can be used to specify the type of values that is are returned for data sources of that type.</span></span>
    
3.  <span data-ttu-id="5623e-216">**Ad** alanına, **Seçici** yazın.</span><span class="sxs-lookup"><span data-stu-id="5623e-216">In the **Name** field, enter **Selector**.</span></span>
4.  <span data-ttu-id="5623e-217">**Biçim numaralandırma** alanında, **Vergilendirme düzeyleri listesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-217">In the **Format enumeration** field, select **List of taxation levels**.</span></span>

    <span data-ttu-id="5623e-218">Az önce, bu veri kaynağında belirtilen her kural için bir iş kullanıcısının, **Vergilendirme düzeyleri listesi** biçim numaralandırma değerlerinden birini, döndürülen değer olarak seçmesi gerektiğini belirlediniz.</span><span class="sxs-lookup"><span data-stu-id="5623e-218">You just specified that, for each rule that is specified in this data source, a business user must select one of the values of the **List of taxation levels** format enumeration as a returned value.</span></span>
    
5.  <span data-ttu-id="5623e-219">**Aramayı düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-219">Select **Edit lookup**.</span></span>
6.  <span data-ttu-id="5623e-220">**Sütunlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-220">Select **Columns**.</span></span>
7.  <span data-ttu-id="5623e-221">**Model** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="5623e-221">Expand the **Model** item.</span></span>
8.  <span data-ttu-id="5623e-222">**Veri** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="5623e-222">Expand the **Data** item.</span></span>
9.  <span data-ttu-id="5623e-223">**Vergi** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="5623e-223">Expand the **Tax** item.</span></span>
10. <span data-ttu-id="5623e-224">**Model.Data.Tax.Code** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-224">Select the **Model.Data.Tax.Code** item.</span></span>
11. <span data-ttu-id="5623e-225">**Ekle** düğmesini (sağ ok) seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-225">Select the **Add** button (the right arrow).</span></span>

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    <span data-ttu-id="5623e-227">Az önce, vergilendirme düzeyinin kabulünde bu veri kaynağında belirtilen her kural için iş kullanıcısının bir koşul olarak vergi kodlarından birini seçmesi gerektiğini belirttiniz.</span><span class="sxs-lookup"><span data-stu-id="5623e-227">You just specified that, for each rule that is specified in this data source for taxation level recognition, a business user must select one of the tax codes as a condition.</span></span> <span data-ttu-id="5623e-228">İş kullanıcısının seçebileceği vergi kodlarının listesi **Model.Data.Tax** veri kaynağı tarafından döndürülür.</span><span class="sxs-lookup"><span data-stu-id="5623e-228">The list of tax codes that the business user can select will be returned by the **Model.Data.Tax** data source.</span></span> <span data-ttu-id="5623e-229">Bu veri kaynağı **Ad** alanını içerdiğinden iş kullanıcılarına sunulan aramadaki her vergi kodu değeri için vergi kodunun adı gösterilir.</span><span class="sxs-lookup"><span data-stu-id="5623e-229">Because this data source contains the **Name** field, the name of the tax code will be shown for each tax code value in the lookup that is presented to the business user.</span></span>
    
12. <span data-ttu-id="5623e-230">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-230">Select **OK**.</span></span>

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    <span data-ttu-id="5623e-232">İş kullanıcıları, bu veri kaynağının kayıtları olarak birden fazla kural ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="5623e-232">Business users can add multiple rules as records of this data source.</span></span> <span data-ttu-id="5623e-233">Her kayıt bir satır koduyla numaralandırılır.</span><span class="sxs-lookup"><span data-stu-id="5623e-233">Each record will be numbered by a line code.</span></span> <span data-ttu-id="5623e-234">Kurallar artan satır numarasına göre değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="5623e-234">Rules will be evaluated in order of increasing line number.</span></span>

    <span data-ttu-id="5623e-235">**Vergi kodu** alanını bu arama veri kaynağındaki kurallar için bir koşul olarak seçtiğiniz ve **Vergi kodu**, **Dize** veri türünün bir alanı olarak ayarlandığı için her kural, veri kaynağına iletilen vergi kodu ile veri kaynağının bu kaydında tanımlanan vergi kodu karşılaştırılarak çalışma zamanında değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="5623e-235">Because you selected the **Tax code** field as a condition for rules in this lookup data source, and because **Tax code** is set up as a field of the **String** data type, each rule will be evaluated at runtime by comparing the tax code that is passed to the data source with the tax code that is defined in this record of the data source.</span></span>

    <span data-ttu-id="5623e-236">Yapılandırılmış koşulu sağlayan bir kural bulunduğunda bu veri kaynağı **Arama sonucu** alanında tanımlanan kuralın arama değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5623e-236">When a rule that satisfies the configured condition is found, this data source returns the lookup value of the rule that is defined in the **Lookup result** field.</span></span> <span data-ttu-id="5623e-237">Herhangi bir kural bulunmazsa kullanıcıya mevcut veri kaynağının doğru bir değer veremediğini bildirmek için bir özel durum oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5623e-237">If no rule is found, an exception is thrown to notify the user that the current data source can't return a correct value.</span></span>

13. <span data-ttu-id="5623e-238">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-238">Select **Save**.</span></span>
14. <span data-ttu-id="5623e-239">**Arama tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="5623e-239">Close the **Lookup designer** page.</span></span>
15. <span data-ttu-id="5623e-240">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-240">Select **OK**.</span></span>

    <span data-ttu-id="5623e-241">Veri kaynağına **Dize** veri türünün **Kod** parametresinin bağımsız değişkeni olarak iletilen herhangi bir vergi kodu için vergilendirme düzeyini **Vergilendirme düzeyleri listesi** biçimindeki numaralandırma değeri olarak döndürecek yeni bir veri kaynağı eklediğinizi unutmayın.</span><span class="sxs-lookup"><span data-stu-id="5623e-241">Notice that you added a new data source that will return the taxation level as the value of the **List of taxation levels** format enumeration for any tax code that is passed to the data source as the argument of the **Code** parameter of the **String** data type.</span></span>
    
    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    <span data-ttu-id="5623e-243">Yapılandırılmış kuralların değerlendirilmesinin, bu kuralların koşullarını tanımlamak için seçilen alanların veri türüne bağlı olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="5623e-243">Note that the evaluation of configured rules depends on the data type of the fields that have been selected to define conditions of those rules.</span></span> <span data-ttu-id="5623e-244">**Sayısal** veya **Tarih** veri türünün bir alanı olarak yapılandırılmış bir alan seçtiğinizde ölçütler daha önce **Dize** veri türü için açıklanan ölçütlerden farklı olur.</span><span class="sxs-lookup"><span data-stu-id="5623e-244">When you select a field that is configured as a field of either the **Numeric** or **Date** data type, the criteria will differ from the criteria that were described earlier for the **String** data type.</span></span> <span data-ttu-id="5623e-245">**Sayısal** ve **Tarih** alanları için kuralın bir değer aralığı olarak belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="5623e-245">For **Numeric** and **Date** fields, the rule must be specified as a range of values.</span></span> <span data-ttu-id="5623e-246">Veri kaynağına iletilen bir değer yapılandırılmış aralıkta olduğunda kuralın koşulu yerine getirilmiş sayılır.</span><span class="sxs-lookup"><span data-stu-id="5623e-246">The condition of the rule will then be considered satisfied when a value that is passed to the data source is in the configured range.</span></span>
    
    <span data-ttu-id="5623e-247">Aşağıdaki çizim, bu tür bir ayarın örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5623e-247">The following illustration shows an example of this type of setup.</span></span> <span data-ttu-id="5623e-248">**String** veri türünün **Model.Data.Tax.Code** alanına ek olarak **Gerçek** veri türünün **Model.Tax.Summary.Base** alanı, bir arama veri kaynağının koşullarını belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5623e-248">In addition to the **Model.Data.Tax.Code** field of the **String** data type, the **Model.Tax.Summary.Base** field of the **Real** data type is used to specify conditions for a lookup data source.</span></span>
    
    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    <span data-ttu-id="5623e-250">Bu arama veri kaynağı için **Model.Data.Tax.Code** ve **Model.Tax.Summary.Base** alanları seçildiğinden, bu veri kaynağının her kuralı aşağıdaki şekilde yapılandırılır:</span><span class="sxs-lookup"><span data-stu-id="5623e-250">Because the **Model.Data.Tax.Code** and **Model.Tax.Summary.Base** fields are selected for this lookup data source, each rule of this data source will be configured in the following way:</span></span>
    
    -   <span data-ttu-id="5623e-251">Sunulan listede **Vergilendirme düzeyleri listesi** biçim numaralandırma değeri, döndürülen bir değer olarak seçilmelidir.</span><span class="sxs-lookup"><span data-stu-id="5623e-251">In the list that is presented, the value of the **List of taxation levels** format enumeration must be selected as a returned value.</span></span>
    -   <span data-ttu-id="5623e-252">Vergi kodu, bu kuralın bir koşulu olarak girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="5623e-252">The tax code must be entered as a condition of this rule.</span></span> <span data-ttu-id="5623e-253">Yalnızca **Model.Data.Tax** veri kaynağı tarafından sağlanan vergi kodları geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="5623e-253">Only tax codes that are provided by the **Model.Data.Tax** data source are applicable.</span></span>
    -   <span data-ttu-id="5623e-254">Vergi matrahının minimum ve maksimum değerleri bu kuralın şartları olarak girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="5623e-254">Minimum and maximum values of the tax base amount must be entered as conditions of this rule.</span></span>

    <span data-ttu-id="5623e-255">Aşağıda bu veri kaynağının her kuralının çalışma zamanında nasıl değerlendirileceği verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="5623e-255">Here is how each rule of this data source will be evaluated at runtime:</span></span>
    -   <span data-ttu-id="5623e-256">Bu veri kaynağına iletilen **Dize** veri türünün kodu, bir kuralın vergi koduna eşit mi?</span><span class="sxs-lookup"><span data-stu-id="5623e-256">Does the code of the **String** data type that was passed to this data source equal the tax code of a rule?</span></span>
    -   <span data-ttu-id="5623e-257">Bu veri kaynağına iletilen **Gerçek** veri türünün değeri, belirli minimum ve maksimum değerler arasında mı?</span><span class="sxs-lookup"><span data-stu-id="5623e-257">Does the value of the **Real** data type that was passed to this data source fall between specific minimum and maximum values?</span></span>

    <span data-ttu-id="5623e-258">Bir kural, her iki koşul da sağlandığında geçerli sayılır.</span><span class="sxs-lookup"><span data-stu-id="5623e-258">A rule will be considered applicable when both conditions are satisfied.</span></span>

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a><span data-ttu-id="5623e-259">Eklenen arama veri kaynağının etiketini çevirme</span><span class="sxs-lookup"><span data-stu-id="5623e-259">Translate the label of the lookup data source that was added</span></span>

<span data-ttu-id="5623e-260">İş kullanıcıları, tüzel kişiliğe bağlı vergi kodu kümelerini belirlemek için farklı diller kullanabileceğinden eklediğiniz arama veri kaynağının etiketini çevirmenizi öneririz; böylece etiket, ilgili sayfada her kullanıcının tercih ettiği dilde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="5623e-260">Because business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the label of any lookup data source that you add, so that it's presented in each user's preferred language on the corresponding page.</span></span>

1.  <span data-ttu-id="5623e-261">**Model.Data.Selector** veri kaynağını seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-261">Select the **Model.Data.Selector** data source.</span></span>
2.  <span data-ttu-id="5623e-262">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-262">Select **Edit**.</span></span>
3.  <span data-ttu-id="5623e-263">**Etiket** alanına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5623e-263">Click in the **Label** field.</span></span>
4.  <span data-ttu-id="5623e-264">**Çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-264">Select **Translate**.</span></span>
5.  <span data-ttu-id="5623e-265">**Metin çevirisi** bölmesinde, **Etiket Kodu** alanına **LBL_SELECTOR_DS** yazın.</span><span class="sxs-lookup"><span data-stu-id="5623e-265">In the **Text translation** pane, in the **Label Id** field, enter **LBL_SELECTOR_DS**.</span></span>
6.  <span data-ttu-id="5623e-266">**Varsayılan dilde metin** alanına **Vergi koduyla vergi düzeyini seçme** yazın.</span><span class="sxs-lookup"><span data-stu-id="5623e-266">In the **Text in default language** field, enter **Select tax level by tax code**.</span></span>
7.  <span data-ttu-id="5623e-267">**Dil** alanında, **DE**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-267">In the **Language** field, select **DE**.</span></span>
8.  <span data-ttu-id="5623e-268">**Çevrilmiş metin** alanına **Steuerebene für Steuerkennzeichen auswählen** yazın.</span><span class="sxs-lookup"><span data-stu-id="5623e-268">In the **Translated text** field, enter **Steuerebene für Steuerkennzeichen auswählen**.</span></span>
9.  <span data-ttu-id="5623e-269">**Çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-269">Select **Translate**.</span></span>
10. <span data-ttu-id="5623e-270">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-270">Select **OK**.</span></span>

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a><span data-ttu-id="5623e-272">Yapılandırılmış aramayı kullanmak için yeni bir alan ekleme</span><span class="sxs-lookup"><span data-stu-id="5623e-272">Add a new field to consume the configured lookup</span></span>

1.  <span data-ttu-id="5623e-273">**Model.Data** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="5623e-273">Expand the **Model.Data** item.</span></span>
2.  <span data-ttu-id="5623e-274">**Model.Data.Summary** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-274">Select the **Model.Data.Summary** item.</span></span>
3.  <span data-ttu-id="5623e-275">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-275">Select **Add**.</span></span>
4.  <span data-ttu-id="5623e-276">**İşlevler/Hesaplanan alan** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-276">Select **Functions/Calculated field**.</span></span>
5.  <span data-ttu-id="5623e-277">**Ad** alanına **LevelByLookup** yazın.</span><span class="sxs-lookup"><span data-stu-id="5623e-277">In the **Name** field, enter **LevelByLookup**.</span></span>
6.  <span data-ttu-id="5623e-278">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-278">Select **Edit formula**.</span></span>
7.  <span data-ttu-id="5623e-279">**Formül alanı**'na **Model.Selector(Model.Data.Summary.Code)** yazın.</span><span class="sxs-lookup"><span data-stu-id="5623e-279">In the **Formula field**, enter **Model.Selector(Model.Data.Summary.Code)**.</span></span>
8.  <span data-ttu-id="5623e-280">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-280">Select **Save**.</span></span>

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  <span data-ttu-id="5623e-282">**Formül düzenleyici** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="5623e-282">Close the **Formula editor** page.</span></span>
10. <span data-ttu-id="5623e-283">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-283">Select **OK**.</span></span>

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    <span data-ttu-id="5623e-285">Eklediğiniz **LevelByLookup** hesaplanan alanın vergilendirme düzeyini, özetlenen her vergi hareketi kaydı için **Vergilendirme düzeyleri listesi** biçimi numaralandırmasının değeri olarak döndüreceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="5623e-285">Notice that the **LevelByLookup** calculated field that you added will return the taxation level as the value of the **List of taxation levels** format enumeration for each summarized tax transactions record.</span></span> <span data-ttu-id="5623e-286">Kaydın vergi kodu **Model.Selector** arama veri kaynağına geçirilir ve bu veri kaynağı için kurallar, doğru vergilendirme düzeyini seçmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5623e-286">The tax code of the record will be passed to the **Model.Selector** lookup data source, and the set of rules for this data source will be used to select the correct taxation level.</span></span>

### <a name="add-a-new-format-enumeration-based-data-source"></a><span data-ttu-id="5623e-287">Yeni bir biçim numaralandırması tabanlı veri kaynağı ekleme</span><span class="sxs-lookup"><span data-stu-id="5623e-287">Add a new format enumeration-based data source</span></span>

<span data-ttu-id="5623e-288">Ardından, daha önce eklediğiniz biçim numaralandırmasını ifade eden yeni bir veri kaynağı ekleyeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="5623e-288">Next, you will add a new data source that refers to the format enumeration that you added earlier.</span></span> <span data-ttu-id="5623e-289">Bu veri kaynağının değerleri daha sonra bir ER biçimi ifadesinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5623e-289">Values of this data source will be used in an ER format expression later.</span></span>

1.  <span data-ttu-id="5623e-290">**Kök ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-290">Select **Add root**.</span></span>
2.  <span data-ttu-id="5623e-291">**Biçim numaralandırması\Numaralandırma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-291">Select **Format enumerations\Enumeration**.</span></span>
3.  <span data-ttu-id="5623e-292">**Ad** alanına **TaxationLevel** yazın.</span><span class="sxs-lookup"><span data-stu-id="5623e-292">In the **Name** field, enter **TaxationLevel**.</span></span>
4.  <span data-ttu-id="5623e-293">**Biçim numaralandırma** alanında, **Vergilendirme düzeyleri listesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-293">In the **Format enumeration** field, select **List of taxation levels**.</span></span>
5.  <span data-ttu-id="5623e-294">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-294">Select **Save**.</span></span>

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a><span data-ttu-id="5623e-295">Aramayı kullanmaya başlamak için var olan bir alanı değiştirme</span><span class="sxs-lookup"><span data-stu-id="5623e-295">Modify an existing field to start to use the lookup</span></span>

<span data-ttu-id="5623e-296">Ardından var olan hesaplanan alanı, vergi koduna bağlı olarak doğru vergilendirme düzeyi değerini döndürmek için yapılandırılmış arama veri kaynağını kullanacak şekilde değiştireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="5623e-296">Next, you will modify the existing calculated field so that it uses the configured lookup data source to return the correct taxation level value, depending on the tax code.</span></span>

1.  <span data-ttu-id="5623e-297">**Model.Data.Summary.Level** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-297">Select the **Model.Data.Summary.Level** item.</span></span>
2.  <span data-ttu-id="5623e-298">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-298">Select **Edit**.</span></span>
3.  <span data-ttu-id="5623e-299">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-299">Select **Edit formula**.</span></span>

    <span data-ttu-id="5623e-300">**Model.Data.Summary.Level** alanının geçerli ifadesinin aşağıdaki sabit kodlanmış vergi kodlarını içerdiğini unutmayın:</span><span class="sxs-lookup"><span data-stu-id="5623e-300">Notice that the current expression of the **Model.Data.Summary.Level** field includes the following hard-coded tax codes:</span></span>
    
    <span data-ttu-id="5623e-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span><span class="sxs-lookup"><span data-stu-id="5623e-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span></span>

4.  <span data-ttu-id="5623e-302">**Formül** alanına **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")** yazın.</span><span class="sxs-lookup"><span data-stu-id="5623e-302">In the **Formula** field, enter **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.</span></span>

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    <span data-ttu-id="5623e-304">**Model.Data.Summary.Level** alanına ait ifadenin artık geçerli kaydın vergi koduna göre vergilendirme düzeyini ve bir iş kullanıcısının **Model.Data.Selector** arama veri kaynağında yapılandırdığı kurallar kümesini döndüreceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="5623e-304">Notice that the expression of the **Model.Data.Summary.Level** field will now return the taxation level, based on the tax code of the current record and the set of rules that that a business user configures in the **Model.Data.Selector** lookup data source.</span></span>
    
5.  <span data-ttu-id="5623e-305">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-305">Select **Save**.</span></span>
6.  <span data-ttu-id="5623e-306">**Formül tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="5623e-306">Close **Formula designer** page.</span></span>
7.  <span data-ttu-id="5623e-307">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-307">Select **OK**.</span></span>
8.  <span data-ttu-id="5623e-308">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-308">Select **Save**.</span></span>
9.  <span data-ttu-id="5623e-309">**Biçim tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="5623e-309">Close **Format designer** page.</span></span>

## <a name="complete-the-draft-version-of-a-derived-format"></a><span data-ttu-id="5623e-310">Türetilmiş biçimin taslak sürümünü tamamlama</span><span class="sxs-lookup"><span data-stu-id="5623e-310">Complete the draft version of a derived format</span></span>

1.  <span data-ttu-id="5623e-311">**Sürümler** hızlı sekmesinde **Durumu değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-311">On the **Versions** fast tab, select **Change status**.</span></span>
2.  <span data-ttu-id="5623e-312">**Tamamlandı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-312">Select **Complete**.</span></span>
3.  <span data-ttu-id="5623e-313">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-313">Select **OK**.</span></span>

## <a name="export-completed-version-of-modified-format"></a><span data-ttu-id="5623e-314">Değiştirilmiş biçimin tamamlanmış sürümünü dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="5623e-314">Export completed version of modified format</span></span>

1.  <span data-ttu-id="5623e-315">Yapılandırma ağacında **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-315">In the configuration tree, select the **Format to learn how to lookup LE data** item.</span></span>
2.  <span data-ttu-id="5623e-316">**Sürümler** hızlı sekmesinde durumu **Tamamlandı** olan kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-316">On the **Versions** fast tab, select the record that has a status of **Completed**.</span></span>
3.  <span data-ttu-id="5623e-317">**Döviz**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-317">Select **Exchange**.</span></span>
4.  <span data-ttu-id="5623e-318">**XML dosyası olarak dışa aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-318">Select **Export as XML file**.</span></span>
5.  <span data-ttu-id="5623e-319">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5623e-319">Select **OK**.</span></span>
6.  <span data-ttu-id="5623e-320">Web tarayıcısı bir **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme.xml** dosyası indirir.</span><span class="sxs-lookup"><span data-stu-id="5623e-320">The web browser downloads a **Format to learn how to lookup LE data.xml** file.</span></span> <span data-ttu-id="5623e-321">Bu dosyayı yerel olarak depolayın.</span><span class="sxs-lookup"><span data-stu-id="5623e-321">Store this file locally.</span></span>

<span data-ttu-id="5623e-322">**LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** öğesinin üst öğeleri için bu bölümdeki adımları tekrarlayın ve aşağıdaki dosyaları yerel olarak depolayın:</span><span class="sxs-lookup"><span data-stu-id="5623e-322">Repeat steps in this section for parent items of the **Format to learn how to lookup LE data** format, and store the following files locally:</span></span>

-   <span data-ttu-id="5623e-323">Parametreli çağrıları öğrenmek için biçimlendirme.xml</span><span class="sxs-lookup"><span data-stu-id="5623e-323">Format to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="5623e-324">Parametreli çağrıları öğrenmek için eşleme.xml</span><span class="sxs-lookup"><span data-stu-id="5623e-324">Mapping to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="5623e-325">Parametreli çağrıları öğrenme modeli.xml</span><span class="sxs-lookup"><span data-stu-id="5623e-325">Model to learn parameterized calls.xml</span></span>

<span data-ttu-id="5623e-326">Vergi hareketlerini farklı vergilendirme düzeylerine göre filtrelemek üzere tüzel kişiliğe bağlı vergi kodları kümeleri oluşturmak üzere yapılandırılmış **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** ER biçimini nasıl kullanacağınızı öğrenmek için [Her tüzel kişilik için ER biçiminin parametrelerini ayarlama](er-app-specific-parameters-set-up.md) konusundaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="5623e-326">To learn how to use the configured **Format to learn how to lookup LE data** ER format to set up legal entity–dependent sets of tax codes to filter tax transactions by different taxation levels, complete the steps in the [Set up the parameters of an ER format per legal entity](er-app-specific-parameters-set-up.md) topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5623e-327">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="5623e-327">Additional resources</span></span>

[<span data-ttu-id="5623e-328">Elektronik raporlamada formül tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="5623e-328">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="5623e-329">Her tüzel kişilik için ER biçiminin parametrelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="5623e-329">Set up the parameters of an ER format per legal entity</span></span>](er-app-specific-parameters-set-up.md)
