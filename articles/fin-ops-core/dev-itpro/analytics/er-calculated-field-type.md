---
title: Hesaplanan alan türünün ER veri kaynaklarının parametreleştirilmiş çağrılarını destekleme
description: Bu konu, ER veri kaynakları için Hesaplanan alan türünün nasıl kullanılacağı hakkında bilgi sağlar.
author: NickSelin
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 20d48795b23628bbba2896bf48940936a25e0435
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550096"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="37ec0-103">Hesaplanan alan türünün ER veri kaynaklarının parametreleştirilmiş çağrılarını destekleme</span><span class="sxs-lookup"><span data-stu-id="37ec0-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37ec0-104">Bu konu **Hesaplanan alan** türünü kullanarak Elektronik raporlama (ER) veri kaynağını nasıl tasarlayabileceğinizi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="37ec0-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="37ec0-105">Bu veri kaynağı, yürütüldüğünde bu veri kaynağını çağıran bir bağlamada yapılandırılmış olan parametre bağımsız değişkenlerinin değerleriyle denetlenebilecek bir ER ifadesi içerebilir.</span><span class="sxs-lookup"><span data-stu-id="37ec0-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="37ec0-106">Bu tür bir veri kaynağının parametreleştirilmiş çağrılarını yapılandırarak, birçok bağlamada tek bir veri kaynağını yeniden kullanabilirsiniz ve böylece, ER model eşlemeleri veya ER biçimlerinde yapılandırılması gereken veri kaynaklarının toplam sayısı azalır.</span><span class="sxs-lookup"><span data-stu-id="37ec0-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="37ec0-107">Ayrıca, bakım maliyetlerini ve diğer tüketicilerin kullanım maliyetini azaltan yapılandırılmış ER bileşenini de basitleştirir.</span><span class="sxs-lookup"><span data-stu-id="37ec0-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="37ec0-108">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="37ec0-108">Prerequisites</span></span>
<span data-ttu-id="37ec0-109">Bu konudaki örnekleri tamamlamak için şu erişimlere sahip olmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="37ec0-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="37ec0-110">Aşağıdaki rollerden birine erişim:</span><span class="sxs-lookup"><span data-stu-id="37ec0-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="37ec0-111">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="37ec0-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="37ec0-112">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="37ec0-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="37ec0-113">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="37ec0-113">System administrator</span></span>

- <span data-ttu-id="37ec0-114">Aşağıdaki rollerden biri için, Finance and Operations ile aynı kiracı için sağlanan Regulatory Configuration Services'a (RCS) erişim:</span><span class="sxs-lookup"><span data-stu-id="37ec0-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="37ec0-115">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="37ec0-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="37ec0-116">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="37ec0-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="37ec0-117">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="37ec0-117">System administrator</span></span>

<span data-ttu-id="37ec0-118">[Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684)'dan, zipli (sıkıştırılmış) dosyayı **esaplanan alan türünün ER veri kaynaklarının parametreleştirilmiş çağrılarını destekleme** indirin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-118">From the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684), download the zipped (compressed) file **Support parameterized calls of ER data sources of Calculated field type**.</span></span> <span data-ttu-id="37ec0-119">Ayıklanması ve yerel olarak depolanması gereken aşağıdaki ER yapılandırmalarını içerir.</span><span class="sxs-lookup"><span data-stu-id="37ec0-119">It contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="37ec0-120">**İçerik**</span><span class="sxs-lookup"><span data-stu-id="37ec0-120">**Content**</span></span>                           | <span data-ttu-id="37ec0-121">**Dosya adı**</span><span class="sxs-lookup"><span data-stu-id="37ec0-121">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="37ec0-122">Örnek ER verisi modeli yapılandırması</span><span class="sxs-lookup"><span data-stu-id="37ec0-122">Sample ER data model configuration</span></span>    | <span data-ttu-id="37ec0-123">Parametreleştirilmiş calls.version.1.xml öğrenme modeli</span><span class="sxs-lookup"><span data-stu-id="37ec0-123">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="37ec0-124">Örnek ER meta verisi yapılandırması</span><span class="sxs-lookup"><span data-stu-id="37ec0-124">Sample ER metadata configuration</span></span>      | <span data-ttu-id="37ec0-125">Parametreleştirilmiş calls.version.1.xml öğrenmek için meta veri</span><span class="sxs-lookup"><span data-stu-id="37ec0-125">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="37ec0-126">Örnek ER model eşleme yapılandırması</span><span class="sxs-lookup"><span data-stu-id="37ec0-126">Sample ER model mapping configuration</span></span> | <span data-ttu-id="37ec0-127">Parametreleştirilmiş calls.version.1.xml öğrenmek için eşleme</span><span class="sxs-lookup"><span data-stu-id="37ec0-127">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="37ec0-128">Örnek ER biçim yapılandırması</span><span class="sxs-lookup"><span data-stu-id="37ec0-128">Sample ER format configuration</span></span>        | <span data-ttu-id="37ec0-129">Parametreleştirilmiş calls.version.1.xml öğrenmek için biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="37ec0-129">Format to learn parameterized calls.version.1.1.xml</span></span>  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="37ec0-130">RCS örneğinizde oturum açın</span><span class="sxs-lookup"><span data-stu-id="37ec0-130">Sign in to your RCS instance</span></span>
<span data-ttu-id="37ec0-131">Bu örnekte, Litware, Inc. adlı örnek şirket için bir yapılandırma oluşturacaksınız. Öncelikle RCS'de [ER Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="37ec0-131">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="37ec0-132">Varsayılan panoda **Elektronik raporlama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-132">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="37ec0-133">**Raporlama yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-133">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="37ec0-134">İndirilen yapılandırmaları RCS'de şu sırada içe aktarın: veri modeli, meta veriler, model eşleme, biçim.</span><span class="sxs-lookup"><span data-stu-id="37ec0-134">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="37ec0-135">Her bir ER yapılandırması için aşağıdaki adımları tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="37ec0-135">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="37ec0-136">**Exchange**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-136">Select **Exchange.**</span></span>
    2. <span data-ttu-id="37ec0-137">**XML dosyasından yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-137">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="37ec0-138">Gerekli ER yapılandırması için XML biçimini seçmek için **Gözat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-138">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="37ec0-139">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-139">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="37ec0-140">Sağlanan ER çözümünü gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="37ec0-140">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="37ec0-141">Model eşlemeyi gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="37ec0-141">Review model mapping</span></span>

1. <span data-ttu-id="37ec0-142">Yapıalndırma ağacında, **Parametreli çağrıları öğrenme modeli** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-142">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="37ec0-143">**Parametreli çağrıları öğrenmek için eşleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-143">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="37ec0-144">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-144">Select **Designer**.</span></span>
4. <span data-ttu-id="37ec0-145">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-145">Select **Designer**.</span></span>  
   
<span data-ttu-id="37ec0-146">Bu ER model eşlemesi aşağıdakileri yapacak şekilde tasarlanmıştır:</span><span class="sxs-lookup"><span data-stu-id="37ec0-146">This ER model mapping is designed to do the following:</span></span>

- <span data-ttu-id="37ec0-147">**TaxTable** tablosunda bulunan vergi kodlarının (**Vergi** veri kaynağı) listesini getirmek.</span><span class="sxs-lookup"><span data-stu-id="37ec0-147">Fetch the list of tax codes (**Tax** data source) residing in the   **TaxTable** table.</span></span>
- <span data-ttu-id="37ec0-148">**TaxTrans** tablosunda bulunan vergi hareketlerinin (**Hareket** veri kaynağı) listesini getirmek:</span><span class="sxs-lookup"><span data-stu-id="37ec0-148">Fetch the list of tax transactions (**Trans** data source) residing in the   **TaxTrans** table:</span></span>
    
    - <span data-ttu-id="37ec0-149">Getirilen hareketlerin (**GR** veri kaynağı) listesini vergi koduna göre gruplandırmak.</span><span class="sxs-lookup"><span data-stu-id="37ec0-149">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
    - <span data-ttu-id="37ec0-150">Vergi kodu başına toplanmış değerleri izleyen gruplanan hareketler için hesaplama yapmak:</span><span class="sxs-lookup"><span data-stu-id="37ec0-150">Calculate for grouped transactions following aggregated values per   tax code:</span></span>

        - <span data-ttu-id="37ec0-151">Vergi matrahı değerlerinin toplamı.</span><span class="sxs-lookup"><span data-stu-id="37ec0-151">Sum of tax base values.</span></span>
        - <span data-ttu-id="37ec0-152">Vergi değerlerinin toplamı.</span><span class="sxs-lookup"><span data-stu-id="37ec0-152">Sum of tax values.</span></span>
        - <span data-ttu-id="37ec0-153">Uygulanan vergi oranının minimum değeri.</span><span class="sxs-lookup"><span data-stu-id="37ec0-153">Minimum value of applied tax rate.</span></span>

<span data-ttu-id="37ec0-154">Bu yapılandırmadaki model eşlemesi, bu model için oluşturulan ve Finance and Operations'da yürütülen ER biçimleri için temel veri modelini uygular.</span><span class="sxs-lookup"><span data-stu-id="37ec0-154">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="37ec0-155">Sonuç olarak **Vergi** ve **Gr** veri kaynaklarının içeriği soyut veri kaynakları gibi ER biçimleri için sunulur.</span><span class="sxs-lookup"><span data-stu-id="37ec0-155">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

  ![Vergi ve Gr veri kaynaklarını gösteren model eşleme tasarımcısı sayfası](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="37ec0-157">**Model eşleme tasarımcısı** sayfasını kapatın</span><span class="sxs-lookup"><span data-stu-id="37ec0-157">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="37ec0-158">**Model eşleme** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="37ec0-158">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="37ec0-159">Biçimi gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="37ec0-159">Review format</span></span>

1. <span data-ttu-id="37ec0-160">Yapıalndırma ağacında, **Parametreli çağrıları öğrenme modeli** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-160">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="37ec0-161">**Parametreli çağrıları öğrenmek için biçimlendirme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-161">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="37ec0-162">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-162">Select **Designer**.</span></span> <span data-ttu-id="37ec0-163">Bu ER biçimi aşağıdakileri yapacak şekilde tasarlanmıştır:</span><span class="sxs-lookup"><span data-stu-id="37ec0-163">This ER format is designed to do the following:</span></span>

  - <span data-ttu-id="37ec0-164">XML biçiminde bir vergi beyanı oluşturmak.</span><span class="sxs-lookup"><span data-stu-id="37ec0-164">Generate a tax statement in XML format.</span></span>
  - <span data-ttu-id="37ec0-165">Vergi beyanında aşağıdaki vergilendirme düzeylerini sunmak: normal, azaltılmış ve yok.</span><span class="sxs-lookup"><span data-stu-id="37ec0-165">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
  - <span data-ttu-id="37ec0-166">Her bir vergilendirme düzeyinde birden çok ayrıntı sunmak ve her düzeyde farklı ayrıntılara sahip olmak.</span><span class="sxs-lookup"><span data-stu-id="37ec0-166">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

  ![Biçim tasarımcısı sayfası](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="37ec0-168">**Eşleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-168">Select **Mapping**.</span></span>
5. <span data-ttu-id="37ec0-169">**Model**, **Veri** ve **Özet** öğelerini genişletin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-169">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

   <span data-ttu-id="37ec0-170">Hesaplanan **Model.Data.Summary.Level** alanı, vergilendirme düzeyi kodunu döndüren ifadeyi içerir (**Normal**, **Azaltılmış**, **Yok** veya **Diğer)**; bu ifade çalışma zamanında **Model.Data.Summary** veri kaynağından elde edilebilecek vergi kodu için metin değeridir.</span><span class="sxs-lookup"><span data-stu-id="37ec0-170">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

  ![Parametreli çağrıları öğrenmek için veri modeli modelinin ayrıntılarını gösteren biçim tasarımcısı sayfası](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="37ec0-172">**Model**.**Data2** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-172">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="37ec0-173">**Model**.**Data2.Summary2** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-173">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
   <span data-ttu-id="37ec0-174">**Model**.**Data2.Summary2**, **Model.Data.Summary** veri kaynağı hareketi ayrıntılarını vergilendirme düzeyine göre (**Model.Data.Summary.Level** hesaplanan alanı tarafından döndürülen) gruplandırmak ve toplamları hesaplamak üzere yapılandıırlır.</span><span class="sxs-lookup"><span data-stu-id="37ec0-174">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

  ![Model.Data2.Summary2 veri kaynağının ayrıntılarını gösteren biçim tasarımcısı sayfası](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="37ec0-176">**Model**.**Data2.Level1**, **Model**.**Data2.Level2** ve **Model**.**Data2.Level3.** hesaplanan alanlarını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-176">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="37ec0-177">Bu hesaplanan alanlar **Model**.**Data2.Summary2** kayıtları listesini filtremek için kullanılır ve yalnızca belirli bir vergilendirme düzeyini temsil eden kayıtları döndürür.</span><span class="sxs-lookup"><span data-stu-id="37ec0-177">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="37ec0-178">**Biçim tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="37ec0-178">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="37ec0-179">Türetilmiş biçim oluşturma</span><span class="sxs-lookup"><span data-stu-id="37ec0-179">Create a derived format</span></span>
<span data-ttu-id="37ec0-180">Varolan üç alanı kullanmak yerine, gerekli vergilendirme düzeyini filtrelemek için bir hesaplanmış alan ekleyerek sağlanan biçimi geliştirebilirsiniz: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** ve **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="37ec0-180">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="37ec0-181">Gerekli vergilendirme düzeyi, bu yeni hesaplanan alanın çağrıldığı yerde belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="37ec0-181">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="37ec0-182">Yapıalndırma ağacında, **Parametreli çağrıları öğrenme modeli** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-182">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="37ec0-183">**Parametreli çağrıları öğrenmek için biçimlendirme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-183">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="37ec0-184">**Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-184">Select **Create configuration**.</span></span>
4. <span data-ttu-id="37ec0-185">**Ad'dan Türet: Parametreli çağrıları öğrenme biçimi, Microsoft** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-185">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="37ec0-186">**Ad** alanına **Parametreleri çağrıları öğrenme biçimi (özel)** girin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-186">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="37ec0-187">**Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-187">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="37ec0-188">Kayıt listesi döndüren parametreli bir hesaplanan alan yapılandırma</span><span class="sxs-lookup"><span data-stu-id="37ec0-188">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="37ec0-189">Yeni hesaplanan alan eklemeye başlama</span><span class="sxs-lookup"><span data-stu-id="37ec0-189">Start adding a new calculated field</span></span>

1. <span data-ttu-id="37ec0-190">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-190">Select **Designer**.</span></span>
2. <span data-ttu-id="37ec0-191">Tüm biçim öğelerini genişletmek için **Genişlet/Daralt**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-191">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="37ec0-192">**Eşleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-192">Select **Mapping**.</span></span>
4. <span data-ttu-id="37ec0-193">**Model** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-193">Expand the **Model** item.</span></span>
5. <span data-ttu-id="37ec0-194">**Model.Data2** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-194">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="37ec0-195">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-195">Select **Add**.</span></span>
7. <span data-ttu-id="37ec0-196">**İşlevler\\Hesaplanan alan** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-196">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="37ec0-197">**Ad** alanına, **Düzeyler** yazın.</span><span class="sxs-lookup"><span data-stu-id="37ec0-197">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="37ec0-198">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-198">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="37ec0-199">Hesaplanan alan eklemek için parametre tanımlama</span><span class="sxs-lookup"><span data-stu-id="37ec0-199">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="37ec0-200">**Parametreler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-200">Select **Parameters**.</span></span>
2. <span data-ttu-id="37ec0-201">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-201">Select **New**.</span></span>
3. <span data-ttu-id="37ec0-202">**Ad** alanına **Vergilendirme Düzeyi** girin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-202">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="37ec0-203">**Tür** alanında **Dize**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-203">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="37ec0-204">Parametrenin bağımsız değişkeninin türünü belirtmek için yalnızca temel veri türleri kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="37ec0-204">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="37ec0-205">Bu nedenle **Kayıt listesi**, **Kayıt** ve **Numaralandırma** türleri bu amaçla kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="37ec0-205">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="37ec0-206">Tek bir hesaplanan alan için belirtilebilecek maksimum parametre sayısı 8'dir.</span><span class="sxs-lookup"><span data-stu-id="37ec0-206">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Parametre veri kaynağı listesi](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="37ec0-208">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-208">Select **OK**.</span></span>

<span data-ttu-id="37ec0-209">Bu parametreyi ekleyerek, bu hesaplanan alanı çağırmak için yerinde olması gereken koşulu belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="37ec0-209">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="37ec0-210">Bu hesaplanan alanı çağırdığınızda, **Vergilendirme Düzeyi** parametresinin bağımsız değişkenini **Dize** biçimiyle bir değer olarak belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="37ec0-210">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="37ec0-211">Yalnızca bir kapsayıcıda bulunan hesaplanan alanlar için parametreler (**Kayıt listesi**, **Kayıt** veya **Kapsayıcı**) tanımladığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="37ec0-211">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="37ec0-212">Yapılandırılan parametre, bu hesaplanan alan için veri kaynakları listesinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="37ec0-212">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="37ec0-213">**Veri kaynağı ekle**'yi seçerek parametreyi yapılandırılan ifadeye ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="37ec0-213">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Veri kaynağı alanları](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="37ec0-215">Hesaplanan alan eklemek için ifade tanımlama</span><span class="sxs-lookup"><span data-stu-id="37ec0-215">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="37ec0-216">**Formül** alanına şunu girin:</span><span class="sxs-lookup"><span data-stu-id="37ec0-216">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="37ec0-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="37ec0-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="37ec0-218">Veri kaynakları listesinde **Vergilendirme Düzeyi** parametresini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-218">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="37ec0-219">**Veri kaynağını ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-219">Select **Add data source**.</span></span>
4. <span data-ttu-id="37ec0-220">**Formül** alanında, ifadeyi şu şekilde tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="37ec0-220">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="37ec0-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span><span class="sxs-lookup"><span data-stu-id="37ec0-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="37ec0-222">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-222">Select **Save**.</span></span>

    ![Veri kaynağı alanı bilgileri](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="37ec0-224">**Formül tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="37ec0-224">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="37ec0-225">Yeni hesaplanan alan eklemeyi bitirme</span><span class="sxs-lookup"><span data-stu-id="37ec0-225">Finish adding a new calculated field</span></span>

- <span data-ttu-id="37ec0-226">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-226">Select **OK**.</span></span>

<span data-ttu-id="37ec0-227">**Biçim Tasarımcısı** sayfasında, yapılandırılmış **Düzeyler** parametreli hesaplanan alanı bir **Dize** bağımsız değişkeni gerektirir.</span><span class="sxs-lookup"><span data-stu-id="37ec0-227">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Hesaplanan alan düzeylerinin genişletilmiş listesi](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="37ec0-229">Biçim öğelerini bağlamak için yapılandırılmış hesaplanan alanı kullanma</span><span class="sxs-lookup"><span data-stu-id="37ec0-229">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="37ec0-230">Yapılandırılmış hesaplanan alanı seçmek için **Model.Data2.Levels** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-230">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="37ec0-231">**Statement.Taxation.Regular** biçim öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-231">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="37ec0-232">**Bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-232">Select **Bind**.</span></span>
4. <span data-ttu-id="37ec0-233">Seçili biçim öğesinin tüm iç içe geçmiş biçim öğelerinde kullanılmakta olan **Level1** veri kaynağının yeni **Levels** veri kaynağıyla değiştirilmesini onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-233">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="37ec0-234">Uygulanan bağlama parametreli hesaplanan alan çağrısı olarak oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="37ec0-234">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="37ec0-235">Varsayılan olarak, bağlı biçim öğesinin adı aşağıdaki koşullarda parametreli hesaplanan alan için bağımsız değişken olarak kullanılır:</span><span class="sxs-lookup"><span data-stu-id="37ec0-235">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="37ec0-236">Hesaplanan alan tek bir parametre kullanacak şekilde yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="37ec0-236">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="37ec0-237">Bu parametrenin veri türü **Dize** olarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="37ec0-237">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="37ec0-238">Bağlı biçim öğesinin adı boş olduğunda, bu öğenin veri kaynağı adı uygulanan bağlamada kullanılır.</span><span class="sxs-lookup"><span data-stu-id="37ec0-238">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="37ec0-239">**Statement.Taxation.Reduced** biçim öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-239">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="37ec0-240">**Bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-240">Select **Bind**.</span></span>
7. <span data-ttu-id="37ec0-241">Seçili biçim öğesinin altında tüm iç içe geçmiş biçim öğelerinde kullanılmakta olan **Level2** veri kaynağının yeni **Levels** veri kaynağıyla değiştirilmesini onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-241">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="37ec0-242">**Statement.Taxation.None** biçim öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-242">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="37ec0-243">**Bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-243">Select **Bind**.</span></span>
10. <span data-ttu-id="37ec0-244">Seçili biçim öğesinin altında tüm iç içe geçmiş biçim öğelerinde kullanılmakta olan **Level3** veri kaynağının yeni **Levels** veri kaynağıyla değiştirilmesini onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-244">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="37ec0-245">Vergilendirme düzeyini temsil eden XML öğesi için parametreli hesaplanan alanın bağımsız değişkenini belirttiğinizde (örneğin, metin değeri olarak **Model.Data2.Levels("Reduced")**), iç içe geçmiş XML öznitelikleri için aynı işlemi yapmanız gerekmez — bunların bağlamaları, üst düzeyde tanımlanan bağımsız değişken değerini devralır(**Model.Data2.Levels("Reduced").aggregated.Base** değil **Model.Data2.Levels.aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="37ec0-245">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="37ec0-246">Parametreli hesaplanan alanın yinelenen çağrıları desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="37ec0-246">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="37ec0-247">**Formülü düzenle**'yi seçebilir ve seçili bağlamada parametreli hesaplanan alanın varsayılan olarak uygulanan bağımsız değişkenini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="37ec0-247">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="37ec0-248">Bu bağımsız değişken eksikse, çalışma zamanında hatalara neden olabilir — kullanıcılara, geçerli biçim doğrulandığında böyle bir durumla ilgili bilgi verilir.</span><span class="sxs-lookup"><span data-stu-id="37ec0-248">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Doğrulama uyarı bildirimi](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="37ec0-250">Bir kayıt döndüren parametreli bir hesaplanan alan yapılandırma</span><span class="sxs-lookup"><span data-stu-id="37ec0-250">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="37ec0-251">Parametreli hesaplanan alan bir kayıt döndürdüğünde, öğeleri biçimlendirmek için bu kaydın ayrı alanların bağlamasını desteklemesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="37ec0-251">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="37ec0-252">Bu gibi durumlarda parametreli hesaplanan alanı çağırmak için bir bağımsız değişkenin değerini içeren üst bir bağlama olmaz — bu değerin tek bir kayıt alanı bağlamasında tanımlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="37ec0-252">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="37ec0-253">Yeni hesaplanan alan eklemeye başlama</span><span class="sxs-lookup"><span data-stu-id="37ec0-253">Start adding a new calculated field</span></span>

1. <span data-ttu-id="37ec0-254">**Model.Data2** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-254">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="37ec0-255">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-255">Select **Add**.</span></span>
3. <span data-ttu-id="37ec0-256">**İşlevler\\Hesaplanan alan** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-256">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="37ec0-257">**Ad** alanına, **LevelRecord** girin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-257">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="37ec0-258">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-258">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="37ec0-259">Hesaplanan alan eklemek için parametre tanımlama</span><span class="sxs-lookup"><span data-stu-id="37ec0-259">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="37ec0-260">**Parametreler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-260">Select **Parameters**.</span></span>
2. <span data-ttu-id="37ec0-261">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-261">Select **New**.</span></span>
3. <span data-ttu-id="37ec0-262">**Ad** alanına **Vergilendirme Düzeyi** girin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-262">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="37ec0-263">**Tür** alanında **Dize**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-263">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="37ec0-264">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-264">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="37ec0-265">Hesaplanan alan eklemek için ifade tanımlama</span><span class="sxs-lookup"><span data-stu-id="37ec0-265">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="37ec0-266">**Formül** alanına, aşağıdaki ifadeyi girin:</span><span class="sxs-lookup"><span data-stu-id="37ec0-266">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="37ec0-267">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="37ec0-267">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="37ec0-268">**Vergilendirme düzeyi** parametresini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-268">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="37ec0-269">**Veri kaynağını ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-269">Select **Add data source**.</span></span>
4. <span data-ttu-id="37ec0-270">**Formül** alanında, ifadenin son şeklini vermek için Adım 1'de girdiğiniz ifadeye **'Taxation Level'))** ekleyin:</span><span class="sxs-lookup"><span data-stu-id="37ec0-270">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="37ec0-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span><span class="sxs-lookup"><span data-stu-id="37ec0-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="37ec0-272">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-272">Select **Save**.</span></span>
6. <span data-ttu-id="37ec0-273">**Formül tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="37ec0-273">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="37ec0-274">Yeni hesaplanan alan eklemeyi bitirme</span><span class="sxs-lookup"><span data-stu-id="37ec0-274">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="37ec0-275">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-275">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="37ec0-276">Biçim öğelerini bağlamak için yapılandırılmış hesaplanan alanı kullanma</span><span class="sxs-lookup"><span data-stu-id="37ec0-276">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="37ec0-277">Yapılandırılmış hesaplanan alanı seçmek için **Model.Data2.LevelRecord** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-277">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="37ec0-278">Yapılandırılmış hesaplanan alanının **Model.Data2.LevelRecord.aggregated** kapsayıcısını genişletin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-278">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="37ec0-279">**Model.Data2.LevelRecord.aggregated.Base** alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-279">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="37ec0-280">**Statement.Taxation.None** biçim öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-280">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="37ec0-281">**Bağlamayı kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-281">Select **Unbind**.</span></span>
6. <span data-ttu-id="37ec0-282">**Statement.Taxation.None.Base** biçim öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-282">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="37ec0-283">**Bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-283">Select **Bind**.</span></span>
8. <span data-ttu-id="37ec0-284">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-284">Select **Edit formula**.</span></span>
9. <span data-ttu-id="37ec0-285">İfadeyi **Model.Data2.LevelRecord("None").aggregated.Base** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-285">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Güncelleştirilmiş ifade](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="37ec0-287">Kullanılmayan hesaplanan alanları kaldırma</span><span class="sxs-lookup"><span data-stu-id="37ec0-287">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="37ec0-288">**Model.Data2.Level1** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-288">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="37ec0-289">**Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-289">Select **Delete**.</span></span>
3. <span data-ttu-id="37ec0-290">**Model.Data2.Level2** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-290">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="37ec0-291">**Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-291">Select **Delete**.</span></span>
5. <span data-ttu-id="37ec0-292">**Model.Data2.Level3** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-292">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="37ec0-293">**Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-293">Select **Delete**.</span></span>
7. <span data-ttu-id="37ec0-294">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-294">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="37ec0-295">Aynı hesaplanan alanını **Model.Data2.Levels** biçim bağlamalarında birkaç kez yeniden kullandınız.</span><span class="sxs-lookup"><span data-stu-id="37ec0-295">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="37ec0-296">Tek bir hesaplanmış alanı kullanmak ve sürdürmek bunu birden çok benzer alan için yapmatan çok daha kolaydır.</span><span class="sxs-lookup"><span data-stu-id="37ec0-296">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="37ec0-297">**Biçim tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="37ec0-297">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="37ec0-298">Türetilmiş biçimin düzenlenmiş sürümünü tamamlama</span><span class="sxs-lookup"><span data-stu-id="37ec0-298">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="37ec0-299">**Sürümler** hızlı sekmesinde, **Durumu değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-299">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="37ec0-300">**Tamamlandı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-300">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="37ec0-301">Türetilmiş biçimin tamamlanmış sürümünü dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="37ec0-301">Export completed version of a derived format</span></span>

1. <span data-ttu-id="37ec0-302">Yapılandırma ağacında **Parametreli çağrıları öğrenmek için biçimlendirme (özel)** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-302">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="37ec0-303">**Sürümler** hızlı sekmesinde tamamlanan 1.1.1. sürümünü seçin</span><span class="sxs-lookup"><span data-stu-id="37ec0-303">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="37ec0-304">**Döviz**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-304">Select **Exchange**.</span></span>
4. <span data-ttu-id="37ec0-305">**XML dosyası olarak dışa aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-305">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="37ec0-306">İndirilen yapılandırmayı yerel olarak XML biçiminde depolayın.</span><span class="sxs-lookup"><span data-stu-id="37ec0-306">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="37ec0-307">ER biçimlerini test etme</span><span class="sxs-lookup"><span data-stu-id="37ec0-307">Test ER formats</span></span> 
<span data-ttu-id="37ec0-308">Yapılandırılmış parametreli hesaplanan alanların doğru çalıştığından emin olmak için başlangıç ve geliştirilmiş ER biçimlerini çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="37ec0-308">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="37ec0-309">ER yapılandırmaları içe aktarın</span><span class="sxs-lookup"><span data-stu-id="37ec0-309">Import ER configurations</span></span>
<span data-ttu-id="37ec0-310">**RCS** türünün ER deposunu kullanarak RCS'den gözden geçirilmiş yapılandırmaları içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="37ec0-310">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="37ec0-311">[Regulatory Configuration Services'dan Elektronik raporlama yapılandırmalarını içe aktarma](rcs-download-configurations.md) konusundaki adımları zaten biliyorsanız, yapılandırmaları ortamınıza aktarmak için, bu konuda daha önce açıklanan yapılandırılmış ER deposunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="37ec0-311">If you already went through the steps in the topic, [Import Electronic reporting configurations from Regulatory Configuration Services](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="37ec0-312">Aksi halde, şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="37ec0-312">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="37ec0-313">**DEMF** şirketini seçin ve varsayılan panoda **Elektronik raporlama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-313">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="37ec0-314">**Raporlama yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-314">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="37ec0-315">Microsoft Download Center'dan indirilen yapılandırmaları şu sırada içe aktarın: veri modeli, model eşleme, biçim.</span><span class="sxs-lookup"><span data-stu-id="37ec0-315">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="37ec0-316">Her bir ER yapılandırması için aşağıdaki adımları tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="37ec0-316">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="37ec0-317">**Exchange**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-317">Select **Exchange.**</span></span>
    2. <span data-ttu-id="37ec0-318">**XML dosyasından yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-318">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="37ec0-319">XML biçimindeki gerekli ER yapılandırmasını seçmek için **Gözat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-319">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="37ec0-320">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-320">Select **OK**.</span></span>

4. <span data-ttu-id="37ec0-321">**Parametreli çağrıları öğrenmek için biçimlendirme (özel)** biçiminin RCS'den dışa aktarılan tamamlanmış 1.1.1 sürümünü içe aktarın:</span><span class="sxs-lookup"><span data-stu-id="37ec0-321">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="37ec0-322">**Exchange**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-322">Select **Exchange.**</span></span>
    2. <span data-ttu-id="37ec0-323">**XML dosyasından yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-323">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="37ec0-324">Yerel olarak depolanan XML biçimindeki **Parametreli çağrıları öğrenmek için biçimlendime (özel)** dosyasını seçmek için **Gözat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-324">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="37ec0-325">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-325">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="37ec0-326">ER biçimlerini çalıştırma</span><span class="sxs-lookup"><span data-stu-id="37ec0-326">Run ER formats</span></span>

1. <span data-ttu-id="37ec0-327">Yapıalndırma ağacında, **Parametreli çağrıları öğrenme modeli** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-327">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="37ec0-328">**Parametreli çağrıları öğrenmek için biçimlendirme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-328">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="37ec0-329">En üst şerittteki **Çalıştır** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-329">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="37ec0-330">Yerel olarak oluşturulan çıktıyı kaydedin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-330">Save the locally generated output.</span></span>
5. <span data-ttu-id="37ec0-331">**Parametreli çağrıları öğrenmek için biçimlendirme (özel)** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-331">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="37ec0-332">En üst şerittteki **Çalıştır** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-332">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="37ec0-333">Oluşturulan çıktıyı yerel olarak kaydedin.</span><span class="sxs-lookup"><span data-stu-id="37ec0-333">Save the generated output locally.</span></span> 
8. <span data-ttu-id="37ec0-334">Oluşturulan çıktıların içeriğini karşılaştırın.</span><span class="sxs-lookup"><span data-stu-id="37ec0-334">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="37ec0-335">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="37ec0-335">Additional resources</span></span>
[<span data-ttu-id="37ec0-336">Elektronik raporlamada formül tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="37ec0-336">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
