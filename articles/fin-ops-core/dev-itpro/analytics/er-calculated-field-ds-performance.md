---
title: Parametreli HESAPLANAN ALAN veri kaynakları ekleyerek ER çözümleri performansını iyileştirme
description: Bu konuda, parametreli HESAPLANAN ALAN veri kaynaklarını ekleyerek, Elektronik raporlama (ER) çözümlerinin performansını artırmaya nasıl yardımcı olabileceğiniz açıklanmaktadır.
author: NickSelin
ms.date: 04/23/2021
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
ms.openlocfilehash: 4ee5a074c5c6d2e2144181e39917b1cc42dfc015
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944861"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a><span data-ttu-id="f449a-103">Parametreli HESAPLANAN ALAN veri kaynakları ekleyerek ER çözümleri performansını iyileştirme</span><span class="sxs-lookup"><span data-stu-id="f449a-103">Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f449a-104">Bu konuda çalıştırılan [Elektronik raporlama (ER)](general-electronic-reporting.md) biçimlerinin [performans izlemelerini](trace-execution-er-troubleshoot-perf.md) nasıl alabileceğinizi açıklanır ve sonra da bu izlemelerden alınan bilgileri kullanarak parametreli **Hesaplanan alan** veri kaynağı yapılandırarak nasıl performansı artırabileceğiniz açıklanır.</span><span class="sxs-lookup"><span data-stu-id="f449a-104">This topic explains how you can take [performance traces](trace-execution-er-troubleshoot-perf.md) of [Electronic reporting (ER)](general-electronic-reporting.md) formats that are run, and then use the information from those traces to help improve performance by configuring a parameterized **Calculated field** data source.</span></span>

<span data-ttu-id="f449a-105">ER yapılandırmalarının iş belgeleri oluşturmak amacıyla tasarlanması işleminin bir parçası olarak, uygulamadan veri getirmek ve oluşturulan çıktıya girmek için kullanılan yöntemi tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="f449a-105">As part of the process of designing ER configurations to generate business documents, you define the method that is used to retrieve data from the application and enter it in the generated output.</span></span> <span data-ttu-id="f449a-106">**Hesaplanmış alan** türünde bir parametreli ER veri kaynağı tasarlayarak, veritabanı çağrılarının sayısını azaltabilir ve ER ile yapılan biçimlendirme çalışmasının ayrıntılarını toplamada yer alan zaman ve maliyeti önemli ölçüde azaltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f449a-106">By designing a parametrized ER data source of the **Calculated field** type, you can reduce the number of database calls, and significantly reduce the time and cost that are involved in collecting the details of ER format execution.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f449a-107">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="f449a-107">Prerequisites</span></span>

- <span data-ttu-id="f449a-108">Bu konudaki örnekleri tamamlamak için aşağıdaki [rollerden](../sysadmin/tasks/assign-users-security-roles.md) birine erişiminiz olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="f449a-108">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="f449a-109">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="f449a-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="f449a-110">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="f449a-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="f449a-111">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="f449a-111">System administrator</span></span>

- <span data-ttu-id="f449a-112">Şirketin **DEMF** olarak ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f449a-112">The company must be set to **DEMF**.</span></span>
- <span data-ttu-id="f449a-113">Bu konunun [Ek 1](#appendix1) bölümündeki adımları izleyerek konudaki örnekleri tamamlamak için gerekli olan Microsoft ER çözümü bileşenlerini indirin.</span><span class="sxs-lookup"><span data-stu-id="f449a-113">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the sample Microsoft ER solution that is required to complete the examples in this topic.</span></span>
- <span data-ttu-id="f449a-114">Örnek Microsoft er çözümünün performansını artırmaya yardımcı olmak amacıyla ER altyapısını kullanmak için gereken en az ER parametre kümesini yapılandırmak için bu konunun [Ek 2](#appendix2) bölümündeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f449a-114">Follow the steps in [Appendix 2](#appendix2) of this topic to configure the minimal set of ER parameters that is required to use the ER framework to help improve the performance of the sample Microsoft ER solution.</span></span>

## <a name="import-the-sample-er-solution"></a><span data-ttu-id="f449a-115">Örnek ER çözümünü içe aktarma</span><span class="sxs-lookup"><span data-stu-id="f449a-115">Import the sample ER solution</span></span>

<span data-ttu-id="f449a-116">Satıcı hareketleri sunan yeni bir rapor oluşturmak üzere yeni bir ER çözümü tasarladığınızı düşünün.</span><span class="sxs-lookup"><span data-stu-id="f449a-116">Imagine that you must design an ER solution to generate a new report that shows vendor transactions.</span></span> <span data-ttu-id="f449a-117">Şu anda, seçilen satıcı için hareketleri **Satıcı hareketleri** sayfasında bulabilirsiniz. (**Borç hesapları** \> **Satıcılar** \> **Tüm satıcılar**'a gidin, bir satıcı seçin ve Eylem Panosu üzerinde, **Satıcı** sekmesinde, **Hareketler** grubunda, **Hareketler**'i seçin.)</span><span class="sxs-lookup"><span data-stu-id="f449a-117">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable** \> **Vendors** \> **All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="f449a-118">Ancak, tüm satıcı hareketinin aynı anda elektronik bir belgede XML biçiminde olmasını istersiniz.</span><span class="sxs-lookup"><span data-stu-id="f449a-118">However, you want to have all vendor transactions together in one electronic document in XML format.</span></span> <span data-ttu-id="f449a-119">Bu çözüm, gerekli veri modelini, model eşlemeyi ve biçim bileşenlerini içeren birkaç ER yapılandırmasından oluşur.</span><span class="sxs-lookup"><span data-stu-id="f449a-119">This solution will consist of several ER configurations that contain the required data model, model mapping, and format components.</span></span>

<span data-ttu-id="f449a-120">İlk adım, satıcı hareketleri raporu oluşturmak için örnek ER çözümünü içe aktarmaktır.</span><span class="sxs-lookup"><span data-stu-id="f449a-120">The first step is to import the sample ER solution to generate a vendor transactions report.</span></span>

1. <span data-ttu-id="f449a-121">Şirketiniz için sağlanan Microsoft Dynamics 365 Finance örneğinde oturum açın.</span><span class="sxs-lookup"><span data-stu-id="f449a-121">Sign in to the instance of Microsoft Dynamics 365 Finance that is provisioned for your company.</span></span>
2. <span data-ttu-id="f449a-122">Bu konuda, **Litware, Inc.** örnek şirket için yapılandırmalar oluşturacak ve değiştireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="f449a-122">In this topic, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="f449a-123">Bu yapılandırma sağlayıcısının Finance'e eklenmiş olduğundan ve etkin olarak seçildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="f449a-123">Make sure that this configuration provider has been added to your Finance instance and is marked as active.</span></span> <span data-ttu-id="f449a-124">Daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f449a-124">For more information, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="f449a-125">**Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-125">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="f449a-126">**Yapılandırmalar** sayfasında, önkoşul olarak karşıdan yüklediğiniz ER yapılandırmalarını aşağıdaki sırada Finance içine aktarın: veri modeli, model eşleme, biçim.</span><span class="sxs-lookup"><span data-stu-id="f449a-126">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into Finance, in the following order: data model, model mapping, format.</span></span> <span data-ttu-id="f449a-127">Her bir yapılandırma için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f449a-127">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="f449a-128">Eylem Bölmesinde, **Exchange** \> **XML dosyasından yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-128">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="f449a-129">ER yapılandırması için XML biçiminde uygun dosyayı seçmek için **Gözat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-129">Select **Browse**, and select the appropriate file for the ER configuration in XML format.</span></span>
    3. <span data-ttu-id="f449a-130">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-130">Select **OK**.</span></span>

![Yapılandırmalar sayfasında içe aktarılan yapılandırmalar](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a><span data-ttu-id="f449a-132">Örnek ER çözümüne göz atma</span><span class="sxs-lookup"><span data-stu-id="f449a-132">Review the sample ER solution</span></span>

### <a name="review-the-model-mapping"></a><span data-ttu-id="f449a-133">Model eşlemeyi gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="f449a-133">Review the model mapping</span></span>

1. <span data-ttu-id="f449a-134">**Yapılandırmalar** sayfasında yapılandırma ağacında, **Performans geliştirme modeli**'ni genişletin ve **Performans geliştirme eşleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-134">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="f449a-135">Eylem Bölmesinde, **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-135">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="f449a-136">**Veri kaynağı eşleme modeli** sayfasında Eylem Panosu üzerinde **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-136">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>

    <span data-ttu-id="f449a-137">Bu ER model eşlemesi aşağıdaki eylemleri gerçekleştirmek üzere tasarlanmıştır:</span><span class="sxs-lookup"><span data-stu-id="f449a-137">This ER model mapping is designed to perform the following actions:</span></span>

    - <span data-ttu-id="f449a-138">VendTrans tablosunda (**Trans** veri kaynağı) saklanan satıcı hareketlerinin listesini getirir.</span><span class="sxs-lookup"><span data-stu-id="f449a-138">Fetch the list of vendor transactions that are stored in the VendTrans table (**Trans** data source).</span></span>
    - <span data-ttu-id="f449a-139">Her hareket için, VendTable tablosundan, hareketin ( satıcı veri kaynağı) deftere nakledildiği satıcının kaydını (**\#Vend** veri kaynağı) getir.</span><span class="sxs-lookup"><span data-stu-id="f449a-139">For every transaction, fetch, from the VendTable table, the record of a vendor that the transaction has been posted for (**\#Vend** data source).</span></span>

    > [!NOTE]
    > <span data-ttu-id="f449a-140">**\#Vend** veri kaynağı, var olan çok-bir ilişkisi **\@\>Relations'.VendTable\_AccountNum** kullanarak ilgili satıcı kaydını getirmek üzere yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="f449a-140">The **\#Vend** data source is configured to fetch the corresponding vendor record by using the existing many-to-one relation **\@.'\>Relations'.VendTable\_AccountNum**.</span></span>

    <span data-ttu-id="f449a-141">Bu yapılandırmadaki model eşlemesi, bu model için oluşturulan ve Finance'de yürütülen ER biçimleri için temel veri modelini uygular.</span><span class="sxs-lookup"><span data-stu-id="f449a-141">The model mapping in this configuration implements the base data model for any ER formats that are created for this model and run in Finance.</span></span> <span data-ttu-id="f449a-142">Bu nedenle **Trans** veri kaynaklarının içeriği soyut **model** veri kaynakları gibi ER biçimleri için sunulur.</span><span class="sxs-lookup"><span data-stu-id="f449a-142">Therefore, the content of the **Trans** data source is exposed for ER formats such as abstract **model** data sources.</span></span>

    ![Model eşleme tasarımcı sayfasında Trans veri kaynağı](media/er-calculated-field-ds-performance-mapping-1.png)

4. <span data-ttu-id="f449a-144">**Model eşleme tasarımcısı** sayfasını kapatın</span><span class="sxs-lookup"><span data-stu-id="f449a-144">Close the **Model mapping designer** page.</span></span>
5. <span data-ttu-id="f449a-145">**Veri kaynağı modeli eşleme** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="f449a-145">Close the **Model to datasource mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="f449a-146">Biçimi gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="f449a-146">Review format</span></span>

1. <span data-ttu-id="f449a-147">**Yapılandırmalar** sayfasında yapılandırma ağacında, **Performans geliştirme modeli**'ni genişletin ve **Performans geliştirme biçimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-147">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement format**.</span></span>
2. <span data-ttu-id="f449a-148">Eylem Bölmesinde, **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-148">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="f449a-149">**Biçim tasarımcısı** sayfasında **Eşleme** sekmesinde **Genişlet/Daralt** seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="f449a-149">On the **Format designer** page, on the **Mapping** tab, select **Expand/Collapse**.</span></span>
4. <span data-ttu-id="f449a-150">**Model**, **Veri** ve **Hareket** öğelerini genişletin.</span><span class="sxs-lookup"><span data-stu-id="f449a-150">Expand the **Model**, **Data,** and **Transaction** items.</span></span>

    <span data-ttu-id="f449a-151">Bu ER biçimi, XML biçiminde satıcı hareketleri raporu oluşturmak için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="f449a-151">This ER format is designed to generate a vendor transactions report in XML format.</span></span>

    ![Biçim tasarımcısı sayfasında veri kaynaklarını ve yapılandırılmış biçim öğelerinin bağlarını biçimlendirme](media/er-calculated-field-ds-performance-format.png)

5. <span data-ttu-id="f449a-153">**Biçim tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="f449a-153">Close the **Format designer** page.</span></span>

## <a name="run-the-sample-er-solution-to-trace-execution"></a><span data-ttu-id="f449a-154">Yürütülmesini izlemek için örnek ER çözümünü çalıştırma</span><span class="sxs-lookup"><span data-stu-id="f449a-154">Run the sample ER solution to trace execution</span></span>

<span data-ttu-id="f449a-155">ER çözümünün ilk sürümünü tasarlamayı bitirdiğinizi varsayalım.</span><span class="sxs-lookup"><span data-stu-id="f449a-155">Imagine that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="f449a-156">Şimdi çözümü Finance örneğiniz içinde test etmek ve yürütme performansını analiz etmek istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="f449a-156">You now want to test the solution in your Finance instance and analyze the execution performance.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="f449a-157">ER performans izlemesini aç</span><span class="sxs-lookup"><span data-stu-id="f449a-157">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="f449a-158">**DEMF** şirketini seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-158">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="f449a-159">Bir ER biçimi çalıştırılırken, performans izleme oluşturmak için [ER performans izlemesini aç](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="f449a-159">Follow the steps in [Turn on the ER performance trace](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) to generate a performance trace while an ER format is run.</span></span>

    ![Kullanıcı parametreleri iletişim kutusu](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a><span data-ttu-id="f449a-161">ER biçimini çalıştır</span><span class="sxs-lookup"><span data-stu-id="f449a-161">Run the ER format</span></span>

1. <span data-ttu-id="f449a-162">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="f449a-162">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f449a-163">**Yapılandırmalar** sayfasında, yapılandırma ağacında, **Performans geliştirme biçimi** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-163">On the **Configurations** page, in the configuration tree, select **Performance improvement format**.</span></span>
3. <span data-ttu-id="f449a-164">Eylem Bölmesinde, **Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-164">On the Action Pane, select **Run**.</span></span>

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a><span data-ttu-id="f449a-165">Model eşleme performansını çözümlemek için performans izlemesini kullanma</span><span class="sxs-lookup"><span data-stu-id="f449a-165">Use the performance trace to analyze model mapping performance</span></span>

1. <span data-ttu-id="f449a-166">**Yapılandırmalar** sayfasında, yapılandırma ağacında, **Performans geliştirme eşleme** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-166">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="f449a-167">Eylem Bölmesinde, **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-167">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="f449a-168">**Model eşlemeleri** sayfasında Eylem Panosu üzerinde **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-168">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="f449a-169">**Model eşleme tasarımcısı** sayfasında, Eylem Panosu üzerinde, **Performans izleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-169">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="f449a-170">Oluşturulan en son izlemeyi seçin ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-170">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="f449a-171">Geçerli model eşleştirmesinin bazı veri kaynağı öğeleri için yeni bilgiler artık kullanılabilir hale gelir:</span><span class="sxs-lookup"><span data-stu-id="f449a-171">New information is now available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="f449a-172">Veri kaynağı kullanılarak veri almada harcanan gerçek süre</span><span class="sxs-lookup"><span data-stu-id="f449a-172">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="f449a-173">Aynı zaman, tüm model eşleşmesinin yürütülmesi için harcanan toplam sürenin yüzdesi olarak ifade edilen saat</span><span class="sxs-lookup"><span data-stu-id="f449a-173">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

![Model eşleme tasarımcısı sayfasında yürütme zamanı ayrıntıları](./media/er-calculated-field-ds-performance-mapping-2.png)

<span data-ttu-id="f449a-175">**Performans istatistikleri** kılavuzunda, **Trans** veri kaynağının VendTrans tablosunu bir kez çağırdığı gösterilir.</span><span class="sxs-lookup"><span data-stu-id="f449a-175">The **Performance statistics** grid shows that the **Trans** data source calls the VendTrans table one time.</span></span> <span data-ttu-id="f449a-176">**Trans** veri kaynağının **\[265\]\[Q:265\]** değeri, uygulama tablosundan 265 satıcı hareketinin getirildiğini ve veri modeline döndürüldüğünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="f449a-176">The value **\[265\]\[Q:265\]** of the **Trans** data source indicates that 265 vendor transactions have been fetched from the application table and returned to the data model.</span></span>

<span data-ttu-id="f449a-177">**Performans istatistikleri** kılavuzu ayrıca geçerli model eşleştirmesinin, **\#Vend** veri kaynağı çalıştırılırken veritabanı isteklerinin çoğaltılacağını da gösterir.</span><span class="sxs-lookup"><span data-stu-id="f449a-177">The **Performance statistics** grid also shows that the current model mapping duplicates database requests while the **\#Vend** data source is run.</span></span> <span data-ttu-id="f449a-178">Bu çoğaltma işlemi aşağıdaki nedenlerle yapılır:</span><span class="sxs-lookup"><span data-stu-id="f449a-178">This duplication occurs for the following reasons:</span></span>

- <span data-ttu-id="f449a-179">Toplam 530 çağrı için satıcı tablosu, her 265 tekrarlandırılmış satıcı hareketi için iki kez çağrılır:</span><span class="sxs-lookup"><span data-stu-id="f449a-179">The vendor table is called two times for each of the 265 iterated vendor transactions, for a total of 530 calls:</span></span>

    - <span data-ttu-id="f449a-180">Satıcı hesap numarasını girmek için bir çağrı yapılır.</span><span class="sxs-lookup"><span data-stu-id="f449a-180">One call is made to enter the vendor account number.</span></span>
    - <span data-ttu-id="f449a-181">Satıcı adını girmek için bir çağrı yapılır.</span><span class="sxs-lookup"><span data-stu-id="f449a-181">One call is made to enter the vendor name.</span></span>

- <span data-ttu-id="f449a-182">Alınan hareketler yalnızca beş satıcı için deftere nakledildiğinden, tekrarlandırılmış her satıcı hareketi için satıcı tablosu çağrılır.</span><span class="sxs-lookup"><span data-stu-id="f449a-182">The vendor table is called for each iterated vendor transaction, even though the fetched transactions have been posted for only five vendors.</span></span> <span data-ttu-id="f449a-183">530 çağrının 525 tanesi çoğaltılır.</span><span class="sxs-lookup"><span data-stu-id="f449a-183">Of the 530 calls, 525 are duplicates.</span></span> <span data-ttu-id="f449a-184">Aşağıdaki şekilde, tekrarlanan çağrılar (veritabanı istekleri) hakkında aldığınız ileti gösterilir.</span><span class="sxs-lookup"><span data-stu-id="f449a-184">The following illustration shows the message that you receive about duplicate calls (database requests).</span></span>

![Model eşleme tasarımcısı sayfasındaki yinelenen veritabanı istekleri hakkında ileti](./media/er-calculated-field-ds-performance-mapping-2a.png)

<span data-ttu-id="f449a-186">Toplam model eşleme yürütme süresinin (yaklaşık sekiz saniye), yüzde 80'ninden fazlasının (yaklaşık 6 saniye) VendTable uygulama tablosundan değerleri alırken harcandığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="f449a-186">Of the total model mapping execution time (approximately eight seconds), notice that more than 80 percent (approximately six seconds) has been spent retrieving values from the VendTable application table.</span></span> <span data-ttu-id="f449a-187">Bu yüzde beş satıcının iki özniteliği için çok büyük olup, VendTrans uygulama tablosundaki bilginin hacmiyle karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="f449a-187">That percentage is too large for two attributes of five vendors, compared with the volume of information from the VendTrans application table.</span></span>

<span data-ttu-id="f449a-188">Her hareket için satıcı ayrıntılarını almak amacıyla yapılan çağrı sayısını azaltmak ve model eşleme performansını artırmak için, **\#Vend** veri kaynağı için önbelleğe alma özelliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f449a-188">To reduce the number of calls that are made to get the vendor details for every transaction, and to improve the performance of the model mapping, you can use caching for the **\#Vend** data source.</span></span>

> [!NOTE]
> <span data-ttu-id="f449a-189">**Trans\\\#Vend** veri kaynağı, çalışma süresinde, **Trans** veri kaynağının geçerli hareketinin kapsamında önbelleğe alınır.</span><span class="sxs-lookup"><span data-stu-id="f449a-189">The **Trans\\\#Vend** data source will be cached in the scope of the current transaction of the **Trans** data source at runtime.</span></span>

<span data-ttu-id="f449a-190">**\#Vend** veri kaynağını önbelleğe alarak, çoğaltılan çağrıların sayısını 525'ten 260'a düşürürsünüz, ancak çoğaltma işlemini tamamen ortadan kalkmaz.</span><span class="sxs-lookup"><span data-stu-id="f449a-190">By caching the **\#Vend** data source, you reduce the number of duplicated calls from 525 to 260, but you don't completely eliminate the duplication.</span></span> <span data-ttu-id="f449a-191">Çoğaltmayı tamamen kaldırmak için, **Hesaplanmış alan** türünde yeni bir parametreli veri kaynağı yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f449a-191">To completely eliminate duplication, you can configure a new parameterized data source of the **Calculated field** type.</span></span>

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="f449a-192">Yürütme izlemesinin bilgilerine dayalı olarak model eşlemeyi geliştirin</span><span class="sxs-lookup"><span data-stu-id="f449a-192">Improve the model mapping based on information from the execution trace</span></span>

### <a name="change-the-logic-of-the-model-mapping"></a><span data-ttu-id="f449a-193">Model eşlemenin mantığını değiştirme</span><span class="sxs-lookup"><span data-stu-id="f449a-193">Change the logic of the model mapping</span></span>

<span data-ttu-id="f449a-194">Veritabanında çoğaltılan çağrıların engellenmesine yardımcı olmak amacıyla, önbelleğe almayı ve **Hesaplanan alan** türü veri kaynağını kullanmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f449a-194">Follow these steps to use caching and a data source of the **Calculated field** type, to help prevent duplicate calls to the database.</span></span>

1. <span data-ttu-id="f449a-195">**Yapılandırmalar** sayfasında, yapılandırma ağacında, **Performans geliştirme eşleme** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-195">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="f449a-196">Eylem Bölmesinde, **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-196">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="f449a-197">**Model eşlemeleri** sayfasında Eylem Panosu üzerinde **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-197">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="f449a-198">**Model eşleme Tasarımcısı** sayfasında, VendTable uygulama tablosundaki kayıtlara erişmek üzere **Tablo kayıtları** türünde bir veri kaynağı eklemek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f449a-198">On the **Model mapping designer** page, follow these steps to add a data source of the **Table records** type to access records in the VendTable application table:</span></span>

    1. <span data-ttu-id="f449a-199">**Veri kaynağı türleri** bölmesinde, **Dynamics 365 for Operations** seçeneğini genişleterek **Tablo kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-199">In the **Data source types** pane, expand **Dynamics 365 for Operations**, and select **Table records**.</span></span>
    2. <span data-ttu-id="f449a-200">**Kök ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-200">Select **Add root**.</span></span>
    3. <span data-ttu-id="f449a-201">İletişim kutusunda, **Ad** alanına **Vend** girin.</span><span class="sxs-lookup"><span data-stu-id="f449a-201">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    4. <span data-ttu-id="f449a-202">**Tablo** alanına, **VendTable** girin.</span><span class="sxs-lookup"><span data-stu-id="f449a-202">In the **Table** field, enter **VendTable**.</span></span>
    5. <span data-ttu-id="f449a-203">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-203">Select **OK**.</span></span>

5. <span data-ttu-id="f449a-204">Yalnızca bu veri kaynakları bir kapsayıcıda bulunuyorsa, **Hesaplanmış alan** türündeki veri kaynaklarına yapılan çağrıları parametreleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f449a-204">You can parameterize calls to data sources of the **Calculated field** type only if those data sources reside in a container.</span></span> <span data-ttu-id="f449a-205">Bu nedenle, **Hesaplanan alan** türünde yeni bir parametreli veri kaynağı tutmak üzere **Boş kapsayıcı** türünde bir veri kaynağı eklemek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f449a-205">Therefore, follow these steps to add a data source of the **Empty container** type to hold a new parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="f449a-206">**Veri kaynağı türleri** bölmesinde, **Genel** seçeneğini genişleterek **Boş kapsayıcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-206">In the **Data source types** pane, expand **General**, and select **Empty container**.</span></span>
    2. <span data-ttu-id="f449a-207">**Kök ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-207">Select **Add root**.</span></span>
    3. <span data-ttu-id="f449a-208">İletişim kutusunda, **Ad** alanına **Kutu** girin.</span><span class="sxs-lookup"><span data-stu-id="f449a-208">In the dialog box, in the **Name** field, enter **Box**.</span></span>
    3. <span data-ttu-id="f449a-209">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-209">Select **OK**.</span></span>

    ![Model eşleme tasarımcı sayfasında Kutu veri kaynağı](./media/er-calculated-field-ds-performance-mapping-3.png)

6. <span data-ttu-id="f449a-211">**Hesaplanan alan** türüne ait parametreli bir veri kaynağı eklemek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f449a-211">Follow these steps to add a parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="f449a-212">**Veri kaynakları** bölmesinde **Kutu**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-212">In the **Data sources** pane, select **Box**.</span></span>
    2. <span data-ttu-id="f449a-213">**Veri kaynağı türleri** bölmesinde, **İşlevler** öğesini genişletin ve **Hesaplanan alan** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-213">In the **Data source types** pane, expand **Functions**, and select **Calculated field**.</span></span>
    3. <span data-ttu-id="f449a-214">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-214">Select **Add**.</span></span>
    4. <span data-ttu-id="f449a-215">İletişim kutusunda, **Ad** alanına **Vend** girin.</span><span class="sxs-lookup"><span data-stu-id="f449a-215">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    5. <span data-ttu-id="f449a-216">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-216">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="f449a-217">**Formül Tasarımcısı** sayfasında, bu veri kaynağı çağrıldığında sağlanması gereken parametreleri belirtmek için **Parametreler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-217">On the **Formula designer** page, select **Parameters** to specify the parameters that must be provided when this data source is called.</span></span>
    7. <span data-ttu-id="f449a-218">**Parametreler** iletişim kutusunda, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-218">In the **Parameters** dialog box, select **New**.</span></span>
    8. <span data-ttu-id="f449a-219">**Ad** alanına **parmVendAccNumber** girin.</span><span class="sxs-lookup"><span data-stu-id="f449a-219">In the **Name** field, enter **parmVendAccNumber**.</span></span>
    9. <span data-ttu-id="f449a-220">**Tür** alanında **Dize**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-220">In the **Type** field, select **String**.</span></span>
    10. <span data-ttu-id="f449a-221">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-221">Select **OK**.</span></span>
    11. <span data-ttu-id="f449a-222">**Formül** alanında, **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))** değerini girin.</span><span class="sxs-lookup"><span data-stu-id="f449a-222">In the **Formula** field, enter **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span></span>
    12. <span data-ttu-id="f449a-223">**Kaydet**'i seçin ve sonra **Formül tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="f449a-223">Select **Save**, and close the **Formula designer** page.</span></span>
    13. <span data-ttu-id="f449a-224">Yeni veri kaynağını eklemek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-224">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="f449a-225">Eklenen veri kaynağını yürütme sırasında önbelleğe alınmış olarak işaretlemek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f449a-225">Follow these steps to mark the added data source as cached during the execution:</span></span>

    1. <span data-ttu-id="f449a-226">**Veri kaynakları** bölmesinde **Box\\Vend** değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-226">In the **Data sources** pane, select **Box\\Vend**.</span></span>
    2. <span data-ttu-id="f449a-227">**Önbellek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-227">Select **Cache**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f449a-228">**Box\\Vend** veri kaynağı, çalışma süresinde, **Trans** veri kaynağının bütün satıcı hareketinin kapsamında önbelleğe alınır.</span><span class="sxs-lookup"><span data-stu-id="f449a-228">The **Box\\Vend** data source will be cached in the scope of all vendor transactions of the **Trans** data source at runtime.</span></span>

8. <span data-ttu-id="f449a-229">**Box\\Vend** veri kaynağı kutusunu kullanacak şekilde iç içe geçmiş **Trans\\\#Vend** veri kaynağını güncelleştirmek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f449a-229">Follow these steps to update the nested **Trans\\\#Vend** data source so that it uses the **Box\\Vend** data source:</span></span>

    1. <span data-ttu-id="f449a-230">**Veri kaynakları** bölmesinde **Trans** öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="f449a-230">In the **Data sources** pane, expand **Trans**.</span></span>
    2. <span data-ttu-id="f449a-231">**Trans\\\#Vend** veri kaynağını seçin ve **Düzenle** \> **Formülü düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-231">Select the **Trans\\\#Vend** data source, and then select **Edit** \> **Edit formula**.</span></span>
    3. <span data-ttu-id="f449a-232">**Formül Tasarımcısı** sayfasında, **Formül** alanına, **Box.Vend(\@.AccountNum)** değerini girin.</span><span class="sxs-lookup"><span data-stu-id="f449a-232">On the **Formula designer** page, in the **Formula** field, enter **Box.Vend(\@.AccountNum)**.</span></span>
    4. <span data-ttu-id="f449a-233">**Kaydet**'i seçin ve ardından **Formül tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="f449a-233">Select **Save**, and then close the **Formula designer** page.</span></span>
    5. <span data-ttu-id="f449a-234">Seçili veri kaynağındaki değişikliklerinizi tamamlamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-234">Select **OK** to complete your changes to the selected data source.</span></span>

9. <span data-ttu-id="f449a-235">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-235">Select **Save**.</span></span>

    ![Model eşleme tasarımcı sayfasında Vend veri kaynağı](./media/er-calculated-field-ds-performance-mapping-4.png)

10. <span data-ttu-id="f449a-237">**Model eşleme tasarımcısı** sayfasını kapatın</span><span class="sxs-lookup"><span data-stu-id="f449a-237">Close the **Model mapping designer** page.</span></span>
11. <span data-ttu-id="f449a-238">**Model eşlemeleri** sayfasını kapatın</span><span class="sxs-lookup"><span data-stu-id="f449a-238">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="f449a-239">ER model eşlemesinin değiştirilmiş sürümünü tamamlayın</span><span class="sxs-lookup"><span data-stu-id="f449a-239">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="f449a-240">**Yapılandırmalar** sayfasında, **Sürümler** hızlı sekmesinde, **Performans geliştirme eşleme** yapılandırmasının **1.2** sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-240">On the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance improvement mapping** configuration.</span></span>
2. <span data-ttu-id="f449a-241">**Durumu değiştir** \> **Tamamla** öğesini ve ardından **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-241">Select **Change status** \> **Complete**, and then select **OK**.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="f449a-242">Çalışmayı izlemek için değiştirilmiş ER çözümünü çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f449a-242">Run the modified ER solution to trace execution</span></span>

<span data-ttu-id="f449a-243">Yeni bir performans izleme oluşturmak için bu konuda daha önce işlenen [ER biçimini çalıştır](#run-format) bölümündeki adımları tekrar edin.</span><span class="sxs-lookup"><span data-stu-id="f449a-243">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a><span data-ttu-id="f449a-244">Model eşlemede ayarlamaları çözümlemek için performans izlemesini kullanma</span><span class="sxs-lookup"><span data-stu-id="f449a-244">Use the performance trace to analyze adjustments to the model mapping</span></span> 

1. <span data-ttu-id="f449a-245">**Yapılandırmalar** sayfasında, yapılandırma ağacında, **Performans geliştirme eşleme** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-245">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="f449a-246">Eylem Bölmesinde, **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-246">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="f449a-247">**Model eşlemeleri** sayfasında Eylem Panosu üzerinde **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-247">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="f449a-248">**Model eşleme tasarımcısı** sayfasında, Eylem Panosu üzerinde, **Performans izleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-248">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="f449a-249">Oluşturulan en son izlemeyi seçin ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-249">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="f449a-250">Model eşleştirmesinde yaptığınız ayarlamaların veritabanındaki yinelenen sorguları elediğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="f449a-250">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="f449a-251">Bu model eşleme için veritabanı tablolarına ve veri kaynaklarına yapılan çağrı sayısı da azaltılmıştır.</span><span class="sxs-lookup"><span data-stu-id="f449a-251">The number of calls to database tables and data sources for this model mapping has also been reduced.</span></span>

![Model eşleme tasarımcı sayfası 1'de bilgiyi izleme](./media/er-calculated-field-ds-performance-mapping-5.png)

<span data-ttu-id="f449a-253">Toplam yürütme süresi yaklaşık 20 kat düşürüldü (yaklaşık 8 saniyeden 400 milisaniyeye).</span><span class="sxs-lookup"><span data-stu-id="f449a-253">The total execution time has been reduced about 20 times (from about 8 seconds to about 400 milliseconds).</span></span> <span data-ttu-id="f449a-254">Bu nedenle, tüm ER çözümü performansı iyileştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="f449a-254">Therefore, the performance of the whole ER solution has been improved.</span></span>

![Model eşleme tasarımcı sayfası 2'de bilgiyi izleme](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a><span data-ttu-id="f449a-256">Ek 1: Örnek Microsoft ER çözümünün bileşenlerini indirme</span><span class="sxs-lookup"><span data-stu-id="f449a-256">Appendix 1: Download the components of the sample Microsoft ER solution</span></span>

<span data-ttu-id="f449a-257">Aşağıdaki dosyaları indirip yerel olarak saklamalısınız.</span><span class="sxs-lookup"><span data-stu-id="f449a-257">You must download the following files and store them locally.</span></span>

| <span data-ttu-id="f449a-258">Dosya</span><span class="sxs-lookup"><span data-stu-id="f449a-258">File</span></span>                                        | <span data-ttu-id="f449a-259">İçerik</span><span class="sxs-lookup"><span data-stu-id="f449a-259">Content</span></span> |
|---------------------------------------------|---------|
| <span data-ttu-id="f449a-260">Performans geliştirme modeli.sürüm.1</span><span class="sxs-lookup"><span data-stu-id="f449a-260">Performance improvement model.version.1</span></span>     | [<span data-ttu-id="f449a-261">Örnek ER verisi modeli yapılandırması</span><span class="sxs-lookup"><span data-stu-id="f449a-261">Sample ER data model configuration</span></span>](https://download.microsoft.com/download/4/6/f/46f0f3fa-782b-414a-8f7b-b6c64a388661/Performance_improvement_model.version.1.xml) |
| <span data-ttu-id="f449a-262">Performans geliştirme eşleştirme.sürümü.1.1</span><span class="sxs-lookup"><span data-stu-id="f449a-262">Performance improvement mapping.version.1.1</span></span> | [<span data-ttu-id="f449a-263">Örnek ER model eşleme yapılandırması</span><span class="sxs-lookup"><span data-stu-id="f449a-263">Sample ER model mapping configuration</span></span>](https://download.microsoft.com/download/8/9/1/8913a763-afb8-4bf4-aaf1-95ad793ffc5a/Performance_improvement_mapping.version.1.1.xml) |
| <span data-ttu-id="f449a-264">Performans geliştirme biçimi.sürümü.1.1</span><span class="sxs-lookup"><span data-stu-id="f449a-264">Performance improvement format.version.1.1</span></span>  | [<span data-ttu-id="f449a-265">Örnek ER biçim yapılandırması</span><span class="sxs-lookup"><span data-stu-id="f449a-265">Sample ER format configuration</span></span>](https://download.microsoft.com/download/9/0/c/90c75963-bc78-4edc-9096-556bbe281f10/Performance_improvement_format.version.1.1.xml) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a><span data-ttu-id="f449a-266">Ek 2: ER altyapısını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f449a-266">Appendix 2: Configure the ER framework</span></span>

<span data-ttu-id="f449a-267">Örnek Microsoft ER çözümünün performansını artırmak için ER altyapısını kullanmaya başlamadan önce, asgari ER parametre kümesini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f449a-267">Before you can start to use the ER framework to improve the performance of the sample Microsoft ER solution, you must configure the minimal set of ER parameters.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="f449a-268">ER parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f449a-268">Configure ER parameters</span></span>

1. <span data-ttu-id="f449a-269">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="f449a-269">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f449a-270">**Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Elektronik raporlama parametreleri** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-270">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="f449a-271">**Elektronik raporlama parametreler** sayfasında, **Genel** sekmesinde, **Tasarım modunu etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f449a-271">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="f449a-272">**Ekler** sekmesinde, aşağıdaki parametreleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="f449a-272">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="f449a-273">**Konfigürasyonlar** alanında, **DEMF** şirketi için **dosya** türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-273">In the **Configurations** field, select the **File** type for the **DEMF** company.</span></span>
    - <span data-ttu-id="f449a-274">**İş arşivi**, **Geçici**, **temel** ve **diğer** alanlarında **Dosya** tipini seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-274">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="f449a-275">ER parametresi hakkında daha fazla bilgi için, bkz. [ER çerçevesini yapılandırma](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f449a-275">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="f449a-276">ER yapılandırma sağlayıcısı etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="f449a-276">Activate an ER configuration provider</span></span>

<span data-ttu-id="f449a-277">Eklenen her ER yapılandırması bir ER konfigürasyon sağlayıcısı tarafından sahiplenilimli olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="f449a-277">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="f449a-278">**Elektronik raporlama** çalışma alanında etkinleştirilen ER yapılandırma sağlayıcısı Bu amaçla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f449a-278">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="f449a-279">Bu nedenle, ER konfigürasyonlarını eklemeye veya düzenlemeye başlamadan önce, **elektronik raporlama** çalışma alanında bir er yapılandırma sağlayıcısını etkinleştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="f449a-279">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="f449a-280">Yalnızca ER yapılandırmasının sahibi yapılandırmayı düzenleyebilir.</span><span class="sxs-lookup"><span data-stu-id="f449a-280">Only the owner of an ER configuration can edit the configuration.</span></span> <span data-ttu-id="f449a-281">Bu nedenle, ER konfigürasyonu düzenlemeye başlamadan önce, uygun ER yapılandırma sağlayıcısı **elektronik raporlama** çalışma alanında etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="f449a-281">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="f449a-282">ER yapılandırma sağlayıcıları listesini gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="f449a-282">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="f449a-283">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="f449a-283">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f449a-284">**Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Yapılandırma sağlayıcıları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-284">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="f449a-285">**Yapılandırma sağlayıcısı tablosu** sayfasında, her sağlayıcı kaydının benzersiz bir adı ve URL'si vardır.</span><span class="sxs-lookup"><span data-stu-id="f449a-285">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="f449a-286">Bu sayfanın içeriğini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="f449a-286">Review the contents of this page.</span></span> <span data-ttu-id="f449a-287">**Litware, Inc.** için zaten bir kayıt varsa, sonraki yordamı atlayıp [Yeni bir ER yapılandırma sağlayıcısı ekleme](#ActivateProvider) bölümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-287">If a record for **Litware, Inc.** already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="f449a-288">Yeni bir ER yapılandırması sağlayıcısı ekleme</span><span class="sxs-lookup"><span data-stu-id="f449a-288">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="f449a-289">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="f449a-289">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f449a-290">**Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Yapılandırma sağlayıcıları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-290">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="f449a-291">**Yapılandırma sağlayıcıları** sayfasında, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-291">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="f449a-292">**Ad** alanına **Litware, Inc.** yazın.</span><span class="sxs-lookup"><span data-stu-id="f449a-292">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="f449a-293">**İnternet adresi** alanına `https://www.litware.com` girin.</span><span class="sxs-lookup"><span data-stu-id="f449a-293">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="f449a-294">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-294">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="f449a-295">ER yapılandırma sağlayıcısı etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="f449a-295">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="f449a-296">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="f449a-296">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f449a-297">**Yerelleştirme konfigürasyonları** sayfasında, **Konfigürasyon sağlayıcıları** bölümünde, **Litware, Inc.** döşemesini seçin ve sonra **etkin ayarla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f449a-297">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="f449a-298">ER yapılandırma sağlayıcıları hakkında daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f449a-298">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f449a-299">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f449a-299">Additional resources</span></span>

- [<span data-ttu-id="f449a-300">Elektronik Raporlamaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="f449a-300">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="f449a-301">Performans sorunlarını gidermek için ER biçimlerinin yürütülmesini izleme</span><span class="sxs-lookup"><span data-stu-id="f449a-301">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="f449a-302">Hesaplanan alan türünün ER veri kaynaklarının parametreleştirilmiş çağrılarını destekleme</span><span class="sxs-lookup"><span data-stu-id="f449a-302">Support parameterized calls of ER data sources of the Calculated field type</span></span>](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
