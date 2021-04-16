---
title: Hesaplanan alan türünün ER veri kaynaklarının parametreleştirilmiş çağrılarını destekleme
description: Bu konu, ER veri kaynakları için Hesaplanan alan türünün nasıl kullanılacağı hakkında bilgi sağlar.
author: NickSelin
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 897133a27f9d3da2f576ce675c0949f824cde881
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749501"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="c3628-103">Hesaplanan alan türünün ER veri kaynaklarının parametreleştirilmiş çağrılarını destekleme</span><span class="sxs-lookup"><span data-stu-id="c3628-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3628-104">Bu konu **Hesaplanan alan** türünü kullanarak Elektronik raporlama (ER) veri kaynağını nasıl tasarlayabileceğinizi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="c3628-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="c3628-105">Bu veri kaynağı, yürütüldüğünde bu veri kaynağını çağıran bir bağlamada yapılandırılmış olan parametre bağımsız değişkenlerinin değerleriyle denetlenebilecek bir ER ifadesi içerebilir.</span><span class="sxs-lookup"><span data-stu-id="c3628-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="c3628-106">Bu tür bir veri kaynağının parametreleştirilmiş çağrılarını yapılandırarak, birçok bağlamada tek bir veri kaynağını yeniden kullanabilirsiniz ve böylece, ER model eşlemeleri veya ER biçimlerinde yapılandırılması gereken veri kaynaklarının toplam sayısı azalır.</span><span class="sxs-lookup"><span data-stu-id="c3628-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="c3628-107">Ayrıca, bakım maliyetlerini ve diğer tüketicilerin kullanım maliyetini azaltan yapılandırılmış ER bileşenini de basitleştirir.</span><span class="sxs-lookup"><span data-stu-id="c3628-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c3628-108">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="c3628-108">Prerequisites</span></span>
<span data-ttu-id="c3628-109">Bu konudaki örnekleri tamamlamak için şu erişimlere sahip olmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="c3628-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="c3628-110">Aşağıdaki rollerden birine erişim:</span><span class="sxs-lookup"><span data-stu-id="c3628-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="c3628-111">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="c3628-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="c3628-112">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="c3628-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="c3628-113">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="c3628-113">System administrator</span></span>

- <span data-ttu-id="c3628-114">Aşağıdaki rollerden biri için, Finance and Operations ile aynı kiracı için sağlanan Regulatory Configuration Services'a (RCS) erişim:</span><span class="sxs-lookup"><span data-stu-id="c3628-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="c3628-115">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="c3628-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="c3628-116">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="c3628-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="c3628-117">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="c3628-117">System administrator</span></span>

<span data-ttu-id="c3628-118">Ayrıca, aşağıdaki dosyaları da indirip yerel olarak depolamalısınız.</span><span class="sxs-lookup"><span data-stu-id="c3628-118">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="c3628-119">**İçerik**</span><span class="sxs-lookup"><span data-stu-id="c3628-119">**Content**</span></span>                           | <span data-ttu-id="c3628-120">**Dosya adı**</span><span class="sxs-lookup"><span data-stu-id="c3628-120">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c3628-121">Örnek ER verisi modeli yapılandırması</span><span class="sxs-lookup"><span data-stu-id="c3628-121">Sample ER data model configuration</span></span>    | [<span data-ttu-id="c3628-122">Parametreleştirilmiş calls.version.1.xml öğrenme modeli</span><span class="sxs-lookup"><span data-stu-id="c3628-122">Model to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| <span data-ttu-id="c3628-123">Örnek ER meta verisi yapılandırması</span><span class="sxs-lookup"><span data-stu-id="c3628-123">Sample ER metadata configuration</span></span>      | [<span data-ttu-id="c3628-124">Parametreleştirilmiş calls.version.1.xml öğrenmek için meta veri</span><span class="sxs-lookup"><span data-stu-id="c3628-124">Metadata to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| <span data-ttu-id="c3628-125">Örnek ER model eşleme yapılandırması</span><span class="sxs-lookup"><span data-stu-id="c3628-125">Sample ER model mapping configuration</span></span> | [<span data-ttu-id="c3628-126">Parametreleştirilmiş calls.version.1.xml öğrenmek için eşleme</span><span class="sxs-lookup"><span data-stu-id="c3628-126">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="c3628-127">Örnek ER biçimi yapılandırması</span><span class="sxs-lookup"><span data-stu-id="c3628-127">Sample ER format configuration</span></span>        | [<span data-ttu-id="c3628-128">Parametreleştirilmiş calls.version.1.xml öğrenmek için biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="c3628-128">Format to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="c3628-129">RCS kurulumunuzda oturum açın</span><span class="sxs-lookup"><span data-stu-id="c3628-129">Sign in to your RCS instance</span></span>
<span data-ttu-id="c3628-130">Bu örnekte, Litware, Inc. adlı örnek şirket için bir yapılandırma oluşturacaksınız. Öncelikle, RCS'de [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) prosedüründeki adımları tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="c3628-130">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="c3628-131">Varsayılan panoda **Elektronik raporlama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-131">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="c3628-132">**Raporlama yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-132">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="c3628-133">İndirilen yapılandırmaları RCS'de şu sırada içe aktarın: veri modeli, meta veriler, model eşleme, biçim.</span><span class="sxs-lookup"><span data-stu-id="c3628-133">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="c3628-134">Her bir ER yapılandırması için aşağıdaki adımları tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="c3628-134">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="c3628-135">**Exchange**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-135">Select **Exchange.**</span></span>
    2. <span data-ttu-id="c3628-136">**XML dosyasından yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-136">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="c3628-137">Gerekli ER yapılandırması için XML biçimini seçmek için **Gözat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-137">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="c3628-138">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-138">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="c3628-139">Sağlanan ER çözümünü gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="c3628-139">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="c3628-140">Model eşlemeyi gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="c3628-140">Review model mapping</span></span>

1. <span data-ttu-id="c3628-141">Yapıalndırma ağacında, **Parametreli çağrıları öğrenme modeli** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c3628-141">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="c3628-142">**Parametreli çağrıları öğrenmek için eşleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-142">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="c3628-143">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-143">Select **Designer**.</span></span>
4. <span data-ttu-id="c3628-144">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-144">Select **Designer**.</span></span>  
   
    <span data-ttu-id="c3628-145">Bu ER model eşlemesi aşağıdakileri yapacak şekilde tasarlanmıştır:</span><span class="sxs-lookup"><span data-stu-id="c3628-145">This ER model mapping is designed to do the following:</span></span>

    - <span data-ttu-id="c3628-146">**TaxTable** tablosunda bulunan vergi kodlarının lisesini (**Vergi** veri kaynağı) getirmek.</span><span class="sxs-lookup"><span data-stu-id="c3628-146">Fetch the list of tax codes (**Tax** data source) residing in the **TaxTable** table.</span></span>
    - <span data-ttu-id="c3628-147">**TaxTrans** tablosunda bulunan vergi hareketlerinin listesini (**Hareket** veri kaynağı) getirmek:</span><span class="sxs-lookup"><span data-stu-id="c3628-147">Fetch the list of tax transactions (**Trans** data source) residing in the **TaxTrans** table:</span></span>
    
        - <span data-ttu-id="c3628-148">Getirilen hareketlerin (**GR** veri kaynağı) listesini vergi koduna göre gruplandırmak.</span><span class="sxs-lookup"><span data-stu-id="c3628-148">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
        - <span data-ttu-id="c3628-149">Her vergi kodu için toplu değerleri izleyen gruplanan hareketler için hesaplama yapmak:</span><span class="sxs-lookup"><span data-stu-id="c3628-149">Calculate for grouped transactions following aggregated values per tax code:</span></span>

            - <span data-ttu-id="c3628-150">Vergi matrahı değerlerinin toplamı.</span><span class="sxs-lookup"><span data-stu-id="c3628-150">Sum of tax base values.</span></span>
            - <span data-ttu-id="c3628-151">Vergi değerlerinin toplamı.</span><span class="sxs-lookup"><span data-stu-id="c3628-151">Sum of tax values.</span></span>
            - <span data-ttu-id="c3628-152">Uygulanan vergi oranının minimum değeri.</span><span class="sxs-lookup"><span data-stu-id="c3628-152">Minimum value of applied tax rate.</span></span>

    <span data-ttu-id="c3628-153">Bu yapılandırmadaki model eşlemesi, bu model için oluşturulan ve Finance and Operations'da yürütülen ER biçimleri için temel veri modelini uygular.</span><span class="sxs-lookup"><span data-stu-id="c3628-153">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="c3628-154">Sonuç olarak **Vergi** ve **Gr** veri kaynaklarının içeriği soyut veri kaynakları gibi ER biçimleri için sunulur.</span><span class="sxs-lookup"><span data-stu-id="c3628-154">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

    ![Vergi ve Gr veri kaynaklarını gösteren model eşleme tasarımcısı sayfası](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="c3628-156">**Model eşleme tasarımcısı** sayfasını kapatın</span><span class="sxs-lookup"><span data-stu-id="c3628-156">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="c3628-157">**Model eşleme** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="c3628-157">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="c3628-158">Biçimi gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="c3628-158">Review format</span></span>

1. <span data-ttu-id="c3628-159">Yapıalndırma ağacında, **Parametreli çağrıları öğrenme modeli** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c3628-159">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="c3628-160">**Parametreli çağrıları öğrenmek için biçimlendirme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-160">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="c3628-161">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-161">Select **Designer**.</span></span> <span data-ttu-id="c3628-162">Bu ER biçimi aşağıdakileri yapacak şekilde tasarlanmıştır:</span><span class="sxs-lookup"><span data-stu-id="c3628-162">This ER format is designed to do the following:</span></span>

    - <span data-ttu-id="c3628-163">XML biçiminde bir vergi beyanı oluşturmak.</span><span class="sxs-lookup"><span data-stu-id="c3628-163">Generate a tax statement in XML format.</span></span>
    - <span data-ttu-id="c3628-164">Vergi beyanında aşağıdaki vergilendirme düzeylerini sunmak: normal, azaltılmış ve yok.</span><span class="sxs-lookup"><span data-stu-id="c3628-164">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
    - <span data-ttu-id="c3628-165">Her bir vergilendirme düzeyinde birden çok ayrıntı sunmak ve her düzeyde farklı ayrıntılara sahip olmak.</span><span class="sxs-lookup"><span data-stu-id="c3628-165">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

    ![Biçim tasarımcısı sayfası](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="c3628-167">**Eşleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-167">Select **Mapping**.</span></span>
5. <span data-ttu-id="c3628-168">**Model**, **Veri** ve **Özet** öğelerini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c3628-168">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

    <span data-ttu-id="c3628-169">Hesaplanan **Model.Data.Summary.Level** alanı, vergilendirme düzeyi kodunu döndüren ifadeyi içerir (**Normal**, **Azaltılmış**, **Yok** veya **Diğer)**; bu ifade çalışma zamanında **Model.Data.Summary** veri kaynağından elde edilebilecek vergi kodu için metin değeridir.</span><span class="sxs-lookup"><span data-stu-id="c3628-169">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

    ![Parametreli çağrıları öğrenmek için veri modeli modelinin ayrıntılarını gösteren biçim tasarımcısı sayfası](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="c3628-171">**Model**.**Data2** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c3628-171">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="c3628-172">**Model**.**Data2.Summary2** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c3628-172">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
    <span data-ttu-id="c3628-173">**Model**.**Data2.Summary2**, **Model.Data.Summary** veri kaynağı hareketi ayrıntılarını vergilendirme düzeyine göre (**Model.Data.Summary.Level** hesaplanan alanı tarafından döndürülen) gruplandırmak ve toplamları hesaplamak üzere yapılandıırlır.</span><span class="sxs-lookup"><span data-stu-id="c3628-173">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

    ![Model.Data2.Summary2 veri kaynağının ayrıntılarını gösteren biçim tasarımcısı sayfası](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="c3628-175">**Model**.**Data2.Level1**, **Model**.**Data2.Level2** ve **Model**.**Data2.Level3.** hesaplanan alanlarını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="c3628-175">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="c3628-176">Bu hesaplanan alanlar **Model**.**Data2.Summary2** kayıtları listesini filtremek için kullanılır ve yalnızca belirli bir vergilendirme düzeyini temsil eden kayıtları döndürür.</span><span class="sxs-lookup"><span data-stu-id="c3628-176">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="c3628-177">**Biçim tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="c3628-177">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="c3628-178">Türetilmiş biçim oluşturma</span><span class="sxs-lookup"><span data-stu-id="c3628-178">Create a derived format</span></span>
<span data-ttu-id="c3628-179">Var olan üç alanı kullanmak yerine, gerekli vergilendirme düzeyini filtrelemek için bir hesaplanmış alan ekleyerek sağlanan biçimi geliştirebilirsiniz: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** ve **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="c3628-179">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="c3628-180">Gerekli vergilendirme düzeyi, bu yeni hesaplanan alanın çağrıldığı yerde belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="c3628-180">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="c3628-181">Yapıalndırma ağacında, **Parametreli çağrıları öğrenme modeli** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c3628-181">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="c3628-182">**Parametreli çağrıları öğrenmek için biçimlendirme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-182">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="c3628-183">**Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-183">Select **Create configuration**.</span></span>
4. <span data-ttu-id="c3628-184">**Ad'dan Türet: Parametreli çağrıları öğrenme biçimi, Microsoft** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-184">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="c3628-185">**Ad** alanına **Parametreleri çağrıları öğrenme biçimi (özel)** girin.</span><span class="sxs-lookup"><span data-stu-id="c3628-185">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="c3628-186">**Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-186">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="c3628-187">Kayıt listesi döndüren parametreli bir hesaplanan alan yapılandırma</span><span class="sxs-lookup"><span data-stu-id="c3628-187">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="c3628-188">Yeni hesaplanan alan eklemeye başlama</span><span class="sxs-lookup"><span data-stu-id="c3628-188">Start adding a new calculated field</span></span>

1. <span data-ttu-id="c3628-189">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-189">Select **Designer**.</span></span>
2. <span data-ttu-id="c3628-190">Tüm biçim öğelerini genişletmek için **Genişlet/Daralt**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-190">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="c3628-191">**Eşleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-191">Select **Mapping**.</span></span>
4. <span data-ttu-id="c3628-192">**Model** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c3628-192">Expand the **Model** item.</span></span>
5. <span data-ttu-id="c3628-193">**Model.Data2** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-193">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="c3628-194">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-194">Select **Add**.</span></span>
7. <span data-ttu-id="c3628-195">**İşlevler\\Hesaplanan alan** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-195">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="c3628-196">**Ad** alanına, **Düzeyler** yazın.</span><span class="sxs-lookup"><span data-stu-id="c3628-196">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="c3628-197">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-197">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="c3628-198">Hesaplanan alan eklemek için parametre tanımlama</span><span class="sxs-lookup"><span data-stu-id="c3628-198">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="c3628-199">**Parametreler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-199">Select **Parameters**.</span></span>
2. <span data-ttu-id="c3628-200">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-200">Select **New**.</span></span>
3. <span data-ttu-id="c3628-201">**Ad** alanına **Vergilendirme Düzeyi** girin.</span><span class="sxs-lookup"><span data-stu-id="c3628-201">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="c3628-202">**Tür** alanında **Dize**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-202">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="c3628-203">Parametrenin bağımsız değişkeninin türünü belirtmek için yalnızca temel veri türleri kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c3628-203">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="c3628-204">Bu nedenle **Kayıt listesi**, **Kayıt** ve **Numaralandırma** türleri bu amaçla kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="c3628-204">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="c3628-205">Tek bir hesaplanan alan için belirtilebilecek maksimum parametre sayısı 8'dir.</span><span class="sxs-lookup"><span data-stu-id="c3628-205">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Parametre veri kaynağı listesi](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="c3628-207">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-207">Select **OK**.</span></span>

<span data-ttu-id="c3628-208">Bu parametreyi ekleyerek, bu hesaplanan alanı çağırmak için yerinde olması gereken koşulu belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3628-208">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="c3628-209">Bu hesaplanan alanı çağırdığınızda, **Vergilendirme Düzeyi** parametresinin bağımsız değişkenini **Dize** biçimiyle bir değer olarak belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c3628-209">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="c3628-210">Yalnızca bir kapsayıcıda bulunan hesaplanan alanlar için parametreler (**Kayıt listesi**, **Kayıt** veya **Kapsayıcı**) tanımladığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="c3628-210">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="c3628-211">Yapılandırılan parametre, bu hesaplanan alan için veri kaynakları listesinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="c3628-211">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="c3628-212">**Veri kaynağı ekle**'yi seçerek parametreyi yapılandırılan ifadeye ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3628-212">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Veri kaynağı alanları](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="c3628-214">Hesaplanan alan eklemek için ifade tanımlama</span><span class="sxs-lookup"><span data-stu-id="c3628-214">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="c3628-215">**Formül** alanına şunu girin:</span><span class="sxs-lookup"><span data-stu-id="c3628-215">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="c3628-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="c3628-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="c3628-217">Veri kaynakları listesinde **Vergilendirme Düzeyi** parametresini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-217">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="c3628-218">**Veri kaynağını ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-218">Select **Add data source**.</span></span>
4. <span data-ttu-id="c3628-219">**Formül** alanında, ifadeyi şu şekilde tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="c3628-219">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="c3628-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span><span class="sxs-lookup"><span data-stu-id="c3628-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="c3628-221">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-221">Select **Save**.</span></span>

    ![Veri kaynağı alanı bilgileri](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="c3628-223">**Formül tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="c3628-223">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="c3628-224">Yeni hesaplanan alan eklemeyi bitirme</span><span class="sxs-lookup"><span data-stu-id="c3628-224">Finish adding a new calculated field</span></span>

- <span data-ttu-id="c3628-225">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-225">Select **OK**.</span></span>

<span data-ttu-id="c3628-226">**Biçim Tasarımcısı** sayfasında, yapılandırılmış **Düzeyler** parametreli hesaplanan alanı bir **Dize** bağımsız değişkeni gerektirir.</span><span class="sxs-lookup"><span data-stu-id="c3628-226">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Hesaplanan alan düzeylerinin genişletilmiş listesi](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements&quot;></a><span data-ttu-id=&quot;c3628-228&quot;>Biçim öğelerini bağlamak için yapılandırılmış hesaplanan alanı kullanma</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c3628-228&quot;>Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id=&quot;c3628-229&quot;>Yapılandırılmış hesaplanan alanı seçmek için **Model.Data2.Levels** öğesini seçin.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c3628-229&quot;>Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id=&quot;c3628-230&quot;>**Statement.Taxation.Regular** biçim öğesini seçin.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c3628-230&quot;>Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id=&quot;c3628-231&quot;>**Bağla**'yı seçin.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c3628-231&quot;>Select **Bind**.</span></span>
4. <span data-ttu-id=&quot;c3628-232&quot;>Seçili biçim öğesinin tüm iç içe geçmiş biçim öğelerinde kullanılmakta olan **Level1** veri kaynağının yeni **Levels** veri kaynağıyla değiştirilmesini onaylamak için **Evet**'i seçin.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c3628-232&quot;>Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id=&quot;c3628-233&quot;>Uygulanan bağlama parametreli hesaplanan alan çağrısı olarak oluşturuldu.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c3628-233&quot;>Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id=&quot;c3628-234&quot;>Varsayılan olarak, bağlı biçim öğesinin adı aşağıdaki koşullarda parametreli hesaplanan alan için bağımsız değişken olarak kullanılır:</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c3628-234&quot;>By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id=&quot;c3628-235&quot;>Hesaplanan alan tek bir parametre kullanacak şekilde yapılandırılır.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c3628-235&quot;>The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id=&quot;c3628-236&quot;>Bu parametrenin veri türü **Dize** olarak tanımlanır.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c3628-236&quot;>The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id=&quot;c3628-237&quot;>Bağlı biçim öğesinin adı boş olduğunda, bu öğenin veri kaynağı adı uygulanan bağlamada kullanılır.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c3628-237&quot;>When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id=&quot;c3628-238&quot;>**Statement.Taxation.Reduced** biçim öğesini seçin.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c3628-238&quot;>Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id=&quot;c3628-239&quot;>**Bağla**'yı seçin.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c3628-239&quot;>Select **Bind**.</span></span>
7. <span data-ttu-id=&quot;c3628-240&quot;>Seçili biçim öğesinin altında tüm iç içe geçmiş biçim öğelerinde kullanılmakta olan **Level2** veri kaynağının yeni **Levels** veri kaynağıyla değiştirilmesini onaylamak için **Evet**'i seçin.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c3628-240&quot;>Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id=&quot;c3628-241&quot;>**Statement.Taxation.None** biçim öğesini seçin.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c3628-241&quot;>Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id=&quot;c3628-242&quot;>**Bağla**'yı seçin.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c3628-242&quot;>Select **Bind**.</span></span>
10. <span data-ttu-id=&quot;c3628-243&quot;>Seçili biçim öğesinin altında tüm iç içe geçmiş biçim öğelerinde kullanılmakta olan **Level3** veri kaynağının yeni **Levels** veri kaynağıyla değiştirilmesini onaylamak için **Evet**'i seçin.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;c3628-243&quot;>Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id=&quot;c3628-244&quot;>Vergilendirme düzeyini temsil eden XML öğesi için parametreli hesaplanan alanın bağımsız değişkenini belirttiğinizde (örneğin, metin değeri olarak **Model.Data2.Levels(&quot;Reduced")**), iç içe geçmiş XML öznitelikleri için aynı işlemi yapmanız gerekmez — bunların bağlamaları, üst düzeyde tanımlanan bağımsız değişken değerini devralır(**Model.Data2.Levels("Reduced").aggregated.Base** değil **Model.Data2.Levels.aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="c3628-244">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="c3628-245">Parametreli hesaplanan alanın yinelenen çağrıları desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="c3628-245">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="c3628-246">**Formülü düzenle**'yi seçebilir ve seçili bağlamada parametreli hesaplanan alanın varsayılan olarak uygulanan bağımsız değişkenini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3628-246">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="c3628-247">Bu bağımsız değişken eksikse, çalışma zamanında hatalara neden olabilir — kullanıcılara, geçerli biçim doğrulandığında böyle bir durumla ilgili bilgi verilir.</span><span class="sxs-lookup"><span data-stu-id="c3628-247">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Doğrulama uyarı bildirimi](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="c3628-249">Bir kayıt döndüren parametreli bir hesaplanan alan yapılandırma</span><span class="sxs-lookup"><span data-stu-id="c3628-249">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="c3628-250">Parametreli hesaplanan alan bir kayıt döndürdüğünde, öğeleri biçimlendirmek için bu kaydın ayrı alanların bağlamasını desteklemesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="c3628-250">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="c3628-251">Bu gibi durumlarda parametreli hesaplanan alanı çağırmak için bir bağımsız değişkenin değerini içeren üst bir bağlama olmaz — bu değerin tek bir kayıt alanı bağlamasında tanımlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="c3628-251">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="c3628-252">Yeni hesaplanan alan eklemeye başlama</span><span class="sxs-lookup"><span data-stu-id="c3628-252">Start adding a new calculated field</span></span>

1. <span data-ttu-id="c3628-253">**Model.Data2** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-253">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="c3628-254">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-254">Select **Add**.</span></span>
3. <span data-ttu-id="c3628-255">**İşlevler\\Hesaplanan alan** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-255">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="c3628-256">**Ad** alanına, **LevelRecord** girin.</span><span class="sxs-lookup"><span data-stu-id="c3628-256">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="c3628-257">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-257">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="c3628-258">Hesaplanan alan eklemek için parametre tanımlama</span><span class="sxs-lookup"><span data-stu-id="c3628-258">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="c3628-259">**Parametreler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-259">Select **Parameters**.</span></span>
2. <span data-ttu-id="c3628-260">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-260">Select **New**.</span></span>
3. <span data-ttu-id="c3628-261">**Ad** alanına **Vergilendirme Düzeyi** girin.</span><span class="sxs-lookup"><span data-stu-id="c3628-261">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="c3628-262">**Tür** alanında **Dize**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-262">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="c3628-263">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-263">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="c3628-264">Hesaplanan alan eklemek için ifade tanımlama</span><span class="sxs-lookup"><span data-stu-id="c3628-264">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="c3628-265">**Formül** alanına, aşağıdaki ifadeyi girin:</span><span class="sxs-lookup"><span data-stu-id="c3628-265">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="c3628-266">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="c3628-266">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="c3628-267">**Vergilendirme düzeyi** parametresini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-267">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="c3628-268">**Veri kaynağını ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-268">Select **Add data source**.</span></span>
4. <span data-ttu-id="c3628-269">**Formül** alanında, ifadenin son şeklini vermek için Adım 1'de girdiğiniz ifadeye **'Taxation Level'))** ekleyin:</span><span class="sxs-lookup"><span data-stu-id="c3628-269">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="c3628-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span><span class="sxs-lookup"><span data-stu-id="c3628-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="c3628-271">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-271">Select **Save**.</span></span>
6. <span data-ttu-id="c3628-272">**Formül tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="c3628-272">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="c3628-273">Yeni hesaplanan alan eklemeyi bitirme</span><span class="sxs-lookup"><span data-stu-id="c3628-273">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="c3628-274">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-274">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="c3628-275">Biçim öğelerini bağlamak için yapılandırılmış hesaplanan alanı kullanma</span><span class="sxs-lookup"><span data-stu-id="c3628-275">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="c3628-276">Yapılandırılmış hesaplanan alanı seçmek için **Model.Data2.LevelRecord** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c3628-276">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="c3628-277">Yapılandırılmış hesaplanan alanının **Model.Data2.LevelRecord.aggregated** kapsayıcısını genişletin.</span><span class="sxs-lookup"><span data-stu-id="c3628-277">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="c3628-278">**Model.Data2.LevelRecord.aggregated.Base** alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-278">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="c3628-279">**Statement.Taxation.None** biçim öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-279">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="c3628-280">**Bağlamayı kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-280">Select **Unbind**.</span></span>
6. <span data-ttu-id="c3628-281">**Statement.Taxation.None.Base** biçim öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-281">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="c3628-282">**Bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-282">Select **Bind**.</span></span>
8. <span data-ttu-id="c3628-283">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-283">Select **Edit formula**.</span></span>
9. <span data-ttu-id="c3628-284">İfadeyi **Model.Data2.LevelRecord("None").aggregated.Base** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="c3628-284">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Güncelleştirilmiş ifade](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="c3628-286">Kullanılmayan hesaplanan alanları kaldırma</span><span class="sxs-lookup"><span data-stu-id="c3628-286">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="c3628-287">**Model.Data2.Level1** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-287">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="c3628-288">**Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-288">Select **Delete**.</span></span>
3. <span data-ttu-id="c3628-289">**Model.Data2.Level2** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-289">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="c3628-290">**Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-290">Select **Delete**.</span></span>
5. <span data-ttu-id="c3628-291">**Model.Data2.Level3** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-291">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="c3628-292">**Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-292">Select **Delete**.</span></span>
7. <span data-ttu-id="c3628-293">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-293">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="c3628-294">Aynı hesaplanan alanını **Model.Data2.Levels** biçim bağlamalarında birkaç kez yeniden kullandınız.</span><span class="sxs-lookup"><span data-stu-id="c3628-294">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="c3628-295">Tek bir hesaplanmış alanı kullanmak ve sürdürmek bunu birden çok benzer alan için yapmatan çok daha kolaydır.</span><span class="sxs-lookup"><span data-stu-id="c3628-295">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="c3628-296">**Biçim tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="c3628-296">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="c3628-297">Türetilmiş biçimin düzenlenmiş sürümünü tamamlama</span><span class="sxs-lookup"><span data-stu-id="c3628-297">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="c3628-298">**Sürümler** hızlı sekmesinde, **Durumu değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-298">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="c3628-299">**Tamamlandı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-299">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="c3628-300">Türetilmiş biçimin tamamlanmış sürümünü dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="c3628-300">Export completed version of a derived format</span></span>

1. <span data-ttu-id="c3628-301">Yapılandırma ağacında **Parametreli çağrıları öğrenmek için biçimlendirme (özel)** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-301">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="c3628-302">**Sürümler** hızlı sekmesinde tamamlanan 1.1.1. sürümünü seçin</span><span class="sxs-lookup"><span data-stu-id="c3628-302">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="c3628-303">**Döviz**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-303">Select **Exchange**.</span></span>
4. <span data-ttu-id="c3628-304">**XML dosyası olarak dışa aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-304">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="c3628-305">İndirilen yapılandırmayı yerel olarak XML biçiminde depolayın.</span><span class="sxs-lookup"><span data-stu-id="c3628-305">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="c3628-306">ER biçimlerini test etme</span><span class="sxs-lookup"><span data-stu-id="c3628-306">Test ER formats</span></span> 
<span data-ttu-id="c3628-307">Yapılandırılmış parametreli hesaplanan alanların doğru çalıştığından emin olmak için başlangıç ve geliştirilmiş ER biçimlerini çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3628-307">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="c3628-308">ER yapılandırmaları içe aktarın</span><span class="sxs-lookup"><span data-stu-id="c3628-308">Import ER configurations</span></span>
<span data-ttu-id="c3628-309">**RCS** türünün ER deposunu kullanarak RCS'den gözden geçirilmiş yapılandırmaları içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3628-309">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="c3628-310">[Düzenleyici Yapılandırma Hizmetleri'nden (RCS) Elektronik raporlama (ER) yapılandırmalarını içe aktarma](rcs-download-configurations.md) konusundaki adımları zaten biliyorsanız yapılandırmaları ortamınıza aktarmak için bu konuda daha önce açıklanan yapılandırılmış ER deposunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="c3628-310">If you already went through the steps in the topic, [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="c3628-311">Aksi halde, şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="c3628-311">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="c3628-312">**DEMF** şirketini seçin ve varsayılan panoda **Elektronik raporlama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-312">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="c3628-313">**Raporlama yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-313">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="c3628-314">Microsoft Download Center'dan indirilen yapılandırmaları şu sırada içe aktarın: veri modeli, model eşleme, biçim.</span><span class="sxs-lookup"><span data-stu-id="c3628-314">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="c3628-315">Her bir ER yapılandırması için aşağıdaki adımları tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="c3628-315">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="c3628-316">**Exchange**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-316">Select **Exchange.**</span></span>
    2. <span data-ttu-id="c3628-317">**XML dosyasından yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-317">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="c3628-318">XML biçimindeki gerekli ER yapılandırmasını seçmek için **Gözat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-318">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="c3628-319">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-319">Select **OK**.</span></span>

4. <span data-ttu-id="c3628-320">**Parametreli çağrıları öğrenmek için biçimlendirme (özel)** biçiminin RCS'den dışa aktarılan tamamlanmış 1.1.1 sürümünü içe aktarın:</span><span class="sxs-lookup"><span data-stu-id="c3628-320">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="c3628-321">**Exchange**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-321">Select **Exchange.**</span></span>
    2. <span data-ttu-id="c3628-322">**XML dosyasından yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-322">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="c3628-323">Yerel olarak depolanan XML biçimindeki **Parametreli çağrıları öğrenmek için biçimlendime (özel)** dosyasını seçmek için **Gözat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-323">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="c3628-324">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-324">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="c3628-325">ER biçimlerini çalıştırma</span><span class="sxs-lookup"><span data-stu-id="c3628-325">Run ER formats</span></span>

1. <span data-ttu-id="c3628-326">Yapıalndırma ağacında, **Parametreli çağrıları öğrenme modeli** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c3628-326">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="c3628-327">**Parametreli çağrıları öğrenmek için biçimlendirme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-327">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="c3628-328">En üst şerittteki **Çalıştır** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-328">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="c3628-329">Yerel olarak oluşturulan çıktıyı kaydedin.</span><span class="sxs-lookup"><span data-stu-id="c3628-329">Save the locally generated output.</span></span>
5. <span data-ttu-id="c3628-330">**Parametreli çağrıları öğrenmek için biçimlendirme (özel)** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-330">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="c3628-331">En üst şerittteki **Çalıştır** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3628-331">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="c3628-332">Oluşturulan çıktıyı yerel olarak kaydedin.</span><span class="sxs-lookup"><span data-stu-id="c3628-332">Save the generated output locally.</span></span> 
8. <span data-ttu-id="c3628-333">Oluşturulan çıktıların içeriğini karşılaştırın.</span><span class="sxs-lookup"><span data-stu-id="c3628-333">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3628-334">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c3628-334">Additional resources</span></span>

- [<span data-ttu-id="c3628-335">Elektronik raporlamada (ER) formül tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="c3628-335">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="c3628-336">Parametreli HESAPLANAN ALAN veri kaynakları ekleyerek ER çözümleri performansını iyileştirme</span><span class="sxs-lookup"><span data-stu-id="c3628-336">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]