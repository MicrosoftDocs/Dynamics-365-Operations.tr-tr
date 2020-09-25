---
title: Madde fiyatları depolama raporunu karşılaştırma
description: Madde fiyatlarını karşılaştırma depolama raporunun nasıl oluşturulacağını öğrenin ve sonucu bulun ve/veya dışa aktarın.
author: AndersGirke
manager: tfehr
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage, InventItemPriceCompareStorageDetailsChart, InventItemPriceCompareStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 73e43a685f390fd718028de6add0370dfcd6cf3b
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759652"
---
# <a name="compare-item-prices-storage-report"></a><span data-ttu-id="d51cb-103">Madde fiyatları depolama raporunu karşılaştırma</span><span class="sxs-lookup"><span data-stu-id="d51cb-103">Compare item prices storage report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d51cb-104">Bu konuda, **Madde fiyatlarını karşılaştırma** raporunun nasıl çalıştırılacağı ve çıktının Dynamics 365 Supply Chain Management'ta etkileşimli bir sayfa ya da birkaç biçimden birinde dışa aktarılan belge olarak dijital biçimde nasıl sunulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d51cb-104">This topic explains how to run a **Compare item prices storage** report and make the output available digitally, either as an interactive page in Dynamics 365 Supply Chain Management, or as an exported document in any of several formats.</span></span>

<span data-ttu-id="d51cb-105">Raporu tarayıcınızda görüntülediğinizde, sütunlar ve toplam bakiyeler yapılandırılan düzeninize göre dinamik olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d51cb-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on your configured layout.</span></span> <span data-ttu-id="d51cb-106">Sonuçları sıralayabilir, filtreleyebilir ve verilerde detaya inebilir ve daha fazlasını yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d51cb-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="d51cb-107">Rapor sonuçları, sonuçları filtreleyerek CSV veya Microsoft Excel gibi bir biçimde dışa aktarmanızı sağlayan **Madde fiyatlarını karşılaştır** veri varlığında saklanır.</span><span class="sxs-lookup"><span data-stu-id="d51cb-107">Report results are stored in the **Compare item prices** data entity, which lets you filter and export the results to a format such as CSV or Microsoft Excel.</span></span>

<span data-ttu-id="d51cb-108">**Madde fiyatlarını karşılaştırma depolama** raporu, çıktının birçok satır içerdiği durumlarda yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="d51cb-108">The **Compare item prices storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="d51cb-109">Örneğin, maliyetlendirme sürümünde bekleyen bir madde fiyatını tutan 40.000'den fazla maddeye sahipseniz çıkış birçok satır içerir.</span><span class="sxs-lookup"><span data-stu-id="d51cb-109">For example, the output will contain many lines if you have more than 40,000 items holding a pending item price in the costing version.</span></span>

## <a name="enable-compare-item-prices-storage"></a><span data-ttu-id="d51cb-110">Madde fiyatları depolamasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="d51cb-110">Enable compare item prices storage</span></span>

<span data-ttu-id="d51cb-111">Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d51cb-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="d51cb-112">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="d51cb-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="d51cb-113">Burada, özellik şu şekilde listelenmiştir:</span><span class="sxs-lookup"><span data-stu-id="d51cb-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="d51cb-114">**Modül**: Maliyet yönetimi</span><span class="sxs-lookup"><span data-stu-id="d51cb-114">**Module** - Cost management</span></span>
- <span data-ttu-id="d51cb-115">**Özellik adı**: Madde fiyatı depolamasını karşılaştır</span><span class="sxs-lookup"><span data-stu-id="d51cb-115">**Feature name** - Compare item price storage</span></span>

## <a name="generate-a-compare-item-prices-storage-report"></a><span data-ttu-id="d51cb-116">Madde fiyatlarını karşılaştırma depolama raporu oluşturma</span><span class="sxs-lookup"><span data-stu-id="d51cb-116">Generate a Compare item prices storage report</span></span>

<span data-ttu-id="d51cb-117">Bir **Madde fiyatları karşılaştırma depolama** raporu oluşturmak ve depolamak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="d51cb-117">Follow these steps to generate and store a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="d51cb-118">**Maliyet yönetimi > Sorgular ve raporlar > Önceden belirlenmiş maliyet raporları > Madde fiyatlarını karşılaştırma depolama** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-118">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="d51cb-119">**Yeni**'yi seçerek **Ürün fiyatlarını karşılaştırma** bölmesini açın.</span><span class="sxs-lookup"><span data-stu-id="d51cb-119">Select **New** to open the **Compare item prices** pane.</span></span> <span data-ttu-id="d51cb-120">Raporunuzda hangi fiyatların karşılaştırılacağını tanımlamak için aşağıdaki seçenekleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d51cb-120">Set the following options to define which prices to compare in your report:</span></span>

    - <span data-ttu-id="d51cb-121">**Parametreler** hızlı sekmesinde, rapora benzersiz bir **Ad** verin ve karşılaştırılacak fiyatları ve tarihleri tanımlamak üzere **Karşılaştırılacak beklemedeki fiyatlar** ve **Karşılaştırma için kullanılan fiyatlar** bölümlerindeki alanları kullanın.</span><span class="sxs-lookup"><span data-stu-id="d51cb-121">On the **Parameters** FastTab, give the report a unique **Name** and use the fields in the **Pending prices to compare** and **Prices used for comparison** sections to define which prices and dates to compare.</span></span>
    - <span data-ttu-id="d51cb-122">**Dahil edilecek kayıtlar** hızlı sekmesinde, rapora dahil edilecek verileri tanımlamak için filtreler ve sınırlamalar ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d51cb-122">On the **Records to include** FastTab, set up filters and constraints to define which data to include in the report.</span></span>
    - <span data-ttu-id="d51cb-123">**Arka planda çalıştır** hızlı sekmesinde, raporu nasıl, ne zaman ve ne sıklıkta oluşturmak istediğinizi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d51cb-123">On the **Run in the background** FastTab, set up how, when, and the frequency at which you want to generate the report.</span></span>
    > [!NOTE]
    > <span data-ttu-id="d51cb-124">Bu rapor her zaman bir toplu işin parçası olarak yürütülür.</span><span class="sxs-lookup"><span data-stu-id="d51cb-124">This report is always executed as part of a batch job.</span></span>

1. <span data-ttu-id="d51cb-125">Ayarlarınızı uygulayıp bölmeyi kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-125">Select **OK** to apply your settings and close the pane.</span></span>

1. <span data-ttu-id="d51cb-126">Toplu iş tamamlandıktan sonra, **Madde fiyatlarını karşılaştırma depolama** sayfasında listelenir.</span><span class="sxs-lookup"><span data-stu-id="d51cb-126">After the batch job is completed, it will be listed on the **Compare item prices storage** page.</span></span> <span data-ttu-id="d51cb-127">Raporu görmek için sayfayı yenilemeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="d51cb-127">You may need to refresh the page to see the report.</span></span>

## <a name="explore-the-compare-item-prices-storage-report"></a><span data-ttu-id="d51cb-128">Madde fiyatlarını karşılaştırma depolama raporunu keşfedin</span><span class="sxs-lookup"><span data-stu-id="d51cb-128">Explore the Compare item prices storage report</span></span>

<span data-ttu-id="d51cb-129">Raporu oluşturduktan sonra, istediğiniz zaman aşağıdaki gibi görüntüleyebilir ve keşfedebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d51cb-129">After you've generated a report, you can view and explore it at any time as follows:</span></span>

1. <span data-ttu-id="d51cb-130">**Maliyet yönetimi > Sorgular ve raporlar > Önceden belirlenmiş maliyet raporları > Madde fiyatlarını karşılaştırma depolama** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-130">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="d51cb-131">Listeden bir rapor seçin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-131">Select a report from the list.</span></span>

1. <span data-ttu-id="d51cb-132">Aşağıdakilerden birini yapın:</span><span class="sxs-lookup"><span data-stu-id="d51cb-132">Do one of the following:</span></span>

    - <span data-ttu-id="d51cb-133">Rapor sonuçlarınıza ilişkin bir genel bakış elde etmek için **Genel bakış**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-133">Select **Overview** to get an overview of your report results.</span></span>
    - <span data-ttu-id="d51cb-134">Raporunuzun daha ayrıntılı bir görünümünü elde etmek için **Ayrıntıları görüntüle**'yi seçin</span><span class="sxs-lookup"><span data-stu-id="d51cb-134">Select **View details** to get a more detailed view of your report</span></span>

1. <span data-ttu-id="d51cb-135">Seçili görünüm açıldıktan sonra, aşağıdakileri yapabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d51cb-135">After the selected view opens, you can do the following:</span></span>

    - <span data-ttu-id="d51cb-136">Tabloları, Supply Chain Management'taki standart formların çoğunda olduğu gibi, o sütundaki değerlere göre sıralamak veya filtrelemek için neredeyse her sütun başlığını seçin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-136">Select almost any column heading to sort or filter the table by values in that column, just as with most standard forms in Supply Chain Management.</span></span> <span data-ttu-id="d51cb-137">Hesaplanan bir alan olduğundan, **Net değişiklik fiyatı %'si** sütununu sıralayamazsınız veya filtreleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="d51cb-137">Note, you can't sort or filter the **Net change price %** column because it's a calculated field.</span></span>
    - <span data-ttu-id="d51cb-138">Forma eklenecek boyut sütununu seçebileceğiniz bir bölme açmak için **Boyut ekranı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-138">Select **Dimension display** to open a pane where you can choose which dimension column to include on the form.</span></span> <span data-ttu-id="d51cb-139">Sonraki açışınızda korunmaları için bu ayarları kaydetmek istiyorsanız **Ayarı kaydet**'i **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d51cb-139">Set **Save setup** to **Yes** if you'd like to save these settings so they will be preserved the next time you open the report.</span></span> <span data-ttu-id="d51cb-140">Ayarlarınızı uygulayıp kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-140">Select **OK** to apply your settings and close.</span></span>
    - <span data-ttu-id="d51cb-141">Formdaki herhangi bir satırı seçin ve seçili maddeyle ilgili daha fazla bilgi görmek için **Ayrıntıları görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-141">Select any row in the form and then select **View details** to see more information about the selected item.</span></span> <span data-ttu-id="d51cb-142">Burada, verilerde detaya inebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d51cb-142">You'll be able to drill down into the data from here.</span></span>
    - <span data-ttu-id="d51cb-143">Formdaki herhangi bir satırı seçin ve ardından sonuçlarınızın etkileşimli grafik sunumunu seçtiğiniz öğeye göre görüntülemek için **Karşılaştırma grafiğini görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-143">Select any row in the form and then select **View comparison chart** to see an interactive graphical representation of your results as they relate to your selected item.</span></span> <span data-ttu-id="d51cb-144">Bu sonuçları grafik ve grafik göstergesinde çeşitli grafiksel öğeler seçerek keşfedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d51cb-144">You can explore these results by selecting various graphical elements in the chart and chart legend.</span></span>
    - <span data-ttu-id="d51cb-145">Formdaki herhangi bir satırı seçin ve seçili maddeyle ilgili hesaplamalar hakkında daha fazla bilgi görmek için **Hesaplama ayrıntılarını görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-145">Select any row in the form and then select **View calculation details** to see more information about calculations related to the selected item.</span></span> <span data-ttu-id="d51cb-146">Burada, verilerde detaya inebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d51cb-146">You'll be able to drill down into the data from here.</span></span>

## <a name="export-the-compare-item-prices-storage-report"></a><span data-ttu-id="d51cb-147">Madde fiyatlarını karşılaştırma depolama raporunu dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="d51cb-147">Export the Compare item prices storage report</span></span>

<span data-ttu-id="d51cb-148">Oluşturduğunuz her rapor, **Madde fiyatlarını karşılaştır** veri varlığında depolanır.</span><span class="sxs-lookup"><span data-stu-id="d51cb-148">Each report that you generate is stored in the **Compare item prices** data entity.</span></span> <span data-ttu-id="d51cb-149">Bu varlıktaki verileri CSV veya Microsoft Excel gibi desteklenen herhangi bir veri biçiminde dışa aktarmak için Supply Chain Management'ın standart veri yönetimi özelliklerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d51cb-149">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, including CSV or Microsoft Excel.</span></span>

<span data-ttu-id="d51cb-150">Aşağıda, **Madde fiyatlarını karşılaştırma depolama** raporunun nasıl dışa aktarılacağına ilişkin bir örnek verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="d51cb-150">The following is an example of how to export a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="d51cb-151">**Sistem yönetimi > Çalışma alanları > Veri yönetimi** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-151">Go to **System administration > Workspaces > Data management**.</span></span>

1. <span data-ttu-id="d51cb-152">**Veri Yönetimi** bölümünde **Dışa aktar** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-152">Select the **Export** button in the **Data management** section.</span></span>

1. <span data-ttu-id="d51cb-153">Dışa aktarma işinizi ayarlamak için kullanacağınız **Dışa aktarma** sayfası açılır.</span><span class="sxs-lookup"><span data-stu-id="d51cb-153">The **Export** page opens, which you'll use to set up your export job.</span></span> <span data-ttu-id="d51cb-154">İşinize bir **Grup adı** vererek işe başlayın.</span><span class="sxs-lookup"><span data-stu-id="d51cb-154">Start by giving your job a **Group name**.</span></span>

1. <span data-ttu-id="d51cb-155">**Seçili varlıklar** bölümünde, aşağıdaki seçenekleri ayarlayabileceğiniz iletişim kutusunu açmak için **Varlık Ekle**'yi seçin:</span><span class="sxs-lookup"><span data-stu-id="d51cb-155">In the **Selected entities** section, select **Add entity** to open a dialog box where you can set the following options:</span></span>

    - <span data-ttu-id="d51cb-156">**Varlık adı**: **Madde fiyatlarını karşılaştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-156">**Entity name** - Select **Compare item prices**.</span></span>
    - <span data-ttu-id="d51cb-157">**Hedef veri biçimi**: Dışa aktarmak istediğiniz biçimi seçin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-157">**Target data format** - Choose the format that you want to export to.</span></span>

1. <span data-ttu-id="d51cb-158">Yeni satırı eklemek için **Ekle**'yi, iletişim kutusunu kapatmak için ise **Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-158">Select **Add** to add the new row and then select **Close** to close the dialog box.</span></span>

1. <span data-ttu-id="d51cb-159">Genellikle bir seferde tek bir rapor dışa aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d51cb-159">Usually you'll export one report at a time.</span></span> <span data-ttu-id="d51cb-160">Bunu yapmak için **Sorgu** bölmesine yeni eklediğiniz satır için bir **Filtre** ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d51cb-160">To do this, set up a **Filter** for the row you just added to the **Inquiry** pane.</span></span> <span data-ttu-id="d51cb-161">Böylece dışa aktarma işleminize **Madde fiyatlarını karşılaştırma** varlığındaki hangi raporları dahil etmek istediğinizi tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d51cb-161">This will let you define which reports from the **Compare item prices** entity that you want to include in your export.</span></span> <span data-ttu-id="d51cb-162">Tek bir raporu dışa aktarmak için aşağıdaki filtre seçeneklerini ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d51cb-162">Set the following filter options to export a single report:</span></span>

    - <span data-ttu-id="d51cb-163">**Aralık** sekmesinde, yeni satır eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-163">On the **Range** tab, select **Add** to add a new row.</span></span>
    - <span data-ttu-id="d51cb-164">**Tablo**'yu **Madde fiyatlarını karşılaştır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d51cb-164">Set **Table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="d51cb-165">**Türetilen tablo**'yu **Madde fiyatlarını karşılaştır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d51cb-165">Set **Derived table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="d51cb-166">**Alanı** filtrelemek istediğiniz alan olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d51cb-166">Set **Field** to the field that you want to filter by.</span></span> <span data-ttu-id="d51cb-167">Genellikle **Yürütme adı** veya **Yürütme zamanı**'nı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d51cb-167">Usually you'll use **Execution name** or **Execution time**.</span></span>
    - <span data-ttu-id="d51cb-168">**Ölçütler**'i aramak istediğiniz seçili alandaki değer (raporun adı veya raporun oluşturulduğu saat) olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d51cb-168">Set **Criteria** to the value from your selected field that you want to look for (either the name of the report or the time the report was generated).</span></span>
    - <span data-ttu-id="d51cb-169">Gerekirse aradığınız raporu benzersiz olarak tanımlayıncaya kadar **Aralık** tablosuna daha fazla satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-169">If necessary, add more rows to the **Range** table until you have uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="d51cb-170">Ayarlarınızı kaydedip kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-170">Select **OK** to save your settings and close.</span></span>

1. <span data-ttu-id="d51cb-171">Dışa aktarma ayarınızı kaydetmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-171">Select **Save** to save your export setup.</span></span>

1. <span data-ttu-id="d51cb-172">**Dışa aktarma seçenekleri** sekmesini açın ve dışa aktarma dosyasını oluşturmak için **Şimdi dışa aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-172">Open the **Export options** tab and select **Export now** to generate the export file.</span></span>

1. <span data-ttu-id="d51cb-173">Dışa aktarma işinizin durumunu ve dışa aktarılan varlıkların listesini görebileceğiniz **Yürütme özeti** sayfası açılır.</span><span class="sxs-lookup"><span data-stu-id="d51cb-173">The **Execution summary** page opens, where you can see the status of your export job and a list of entities that were exported.</span></span> <span data-ttu-id="d51cb-174">**Varlık işleme durumu** alanında listelenen **Madde fiyatlarını karşılaştır** varlığını seçin ve ardından söz konusu varlıktan dışa aktarılan verileri indirmek için **Dosyayı indir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d51cb-174">Select the **Compare item prices** entity listed in the **Entity processing status** area and then select **Download file** to download the data exported from that entity.</span></span>

<span data-ttu-id="d51cb-175">Veri yönetimini kullanarak verileri dışa aktarma hakkında daha fazla bilgi için bkz. [Veri içe ve dışa aktarma işlerine genel bakış](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="d51cb-175">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>
