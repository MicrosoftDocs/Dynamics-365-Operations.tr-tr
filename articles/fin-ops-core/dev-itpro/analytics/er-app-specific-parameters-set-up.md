---
title: Her tüzel kişilik için ER biçiminin parametrelerini ayarlama
description: Bu konu, her tüzel kişilik için bir Elektronik raporlama (ER) biçimi parametrelerini nasıl ayarlayabileceğinizi açıklar.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
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
ms.openlocfilehash: b51a7ae8587a3cbb65efc4af574929efcbc8fbf8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681484"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a><span data-ttu-id="2cf99-103">Her tüzel kişilik için ER biçiminin parametrelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="2cf99-103">Set up the parameters of an ER format per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="2cf99-104">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="2cf99-104">Prerequisites</span></span>

<span data-ttu-id="2cf99-105">Bu adımları tamamlamak için önce [Her tüzel kişilik için belirtilen parametreleri kullanmak için ER biçimlerini yapılandırma](er-app-specific-parameters-configure-format.md) konusundaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2cf99-105">To complete these steps, you must first complete the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span>

<span data-ttu-id="2cf99-106">Bu konudaki örnekleri tamamlamak üzere aşağıdaki rollerden biri için Microsoft Dynamics 365 Finance'e (Finance) erişiminiz olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="2cf99-106">To complete the examples in this topic, you must have access to Microsoft Dynamics 365 Finance (Finance) for one of the following roles:</span></span>

- <span data-ttu-id="2cf99-107">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="2cf99-107">Electronic reporting developer</span></span>
- <span data-ttu-id="2cf99-108">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="2cf99-108">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="2cf99-109">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="2cf99-109">System administrator</span></span>

## <a name="import-er-configurations"></a><span data-ttu-id="2cf99-110">ER yapılandırmaları içe aktarın</span><span class="sxs-lookup"><span data-stu-id="2cf99-110">Import ER configurations</span></span>

1.  <span data-ttu-id="2cf99-111">Ortamınızda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="2cf99-111">Sign in to your environment.</span></span>
2.  <span data-ttu-id="2cf99-112">Varsayılan panoda **Elektronik raporlama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-112">On the default dashboard, select **Electronic reporting**.</span></span>
3.  <span data-ttu-id="2cf99-113">**Raporlama yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-113">Select **Reporting configurations**.</span></span>
4.  <span data-ttu-id="2cf99-114">[Her tüzel kişilik için belirtilen parametreleri kullanmak için ER biçimlerini yapılandırma](er-app-specific-parameters-configure-format.md) konusundaki adımları tamamlarken Regulatory Configuration Services (RCS) aracından dışa aktardığınız yapılandırmaları Finance uygulamasının geçerli kurulumuna içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="2cf99-114">Import, into the current instance of Finance, the configurations that you exported from Regulatory Configuration Services (RCS) while you were completing the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span> <span data-ttu-id="2cf99-115">Her Elektronik raporlama (ER) yapılandırması için aşağıdaki adımları takip edin: veri modeli, model eşleme ve biçimler.</span><span class="sxs-lookup"><span data-stu-id="2cf99-115">Follow these steps for each Electronic reporting (ER) configuration, in the following order: data model, model mapping, and formats.</span></span>

    1. <span data-ttu-id="2cf99-116">**Değişim \> XML dosyasından yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-116">Select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="2cf99-117">Gerekli ER yapılandırması için XML biçimindeki dosyayı seçmek üzere **Gözat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-117">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="2cf99-118">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-118">Select **OK**.</span></span>
    
    <span data-ttu-id="2cf99-119">Aşağıdaki şekil, tamamladığınızda sahip olmanız gereken yapılandırmaları gösterir.</span><span class="sxs-lookup"><span data-stu-id="2cf99-119">The following illustration shows the configurations that you must have when you've finished.</span></span>

    ![ER yapılandırma sayfası](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a><span data-ttu-id="2cf99-121">DEMF şirketi için parametreleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="2cf99-121">Set up parameters for the DEMF company</span></span>

<span data-ttu-id="2cf99-122">ER biçimi için uygulamaya özel parametreleri ayarlamak üzere ER çerçevesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2cf99-122">You can use the ER framework to set up application-specific parameters for an ER format.</span></span>

1.  <span data-ttu-id="2cf99-123">**DEMF** tüzel kişiliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-123">Select the **DEMF** legal entity.</span></span>
2.  <span data-ttu-id="2cf99-124">Yapılandırma ağacında **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** biçimini seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-124">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
3.  <span data-ttu-id="2cf99-125">Eylem Bölmesinde, **Yapılandırmalar** sekmesindeki **Uygulama özel parametreleri** grubunda **Ayar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-125">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>

    ![ER uygulaması özel parametreler sayfası](./media/GER-AppSpecParms-LookupForm.PNG)
    
    <span data-ttu-id="2cf99-127">**Uygulama özel parametreleri** sayfasında **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** biçiminin **Seçici** veri kaynağı için kuralları yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2cf99-127">On the **Application specific parameters** page, you can configure the rules for the **Selector** data source of the **Format to learn how to lookup LE data** format.</span></span>
    
    <span data-ttu-id="2cf99-128">Temel ER biçimi, **Arama** türünde birkaç veri kaynağı içerecekse veri kaynağı için kurallar kümesini yapılandırmaya başlamadan önce **Aramalar** hızlı sekmesinde istediğiniz veri kaynağını seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="2cf99-128">If the base ER format will contain several data sources of the **Lookup** type, you must select the desired data source on the **Lookups** FastTab before you can start to configure the set of rules for the data source.</span></span>
    
    <span data-ttu-id="2cf99-129">Her veri kaynağı için seçilen ER biçiminin her sürümüne ayrı kurallar yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2cf99-129">For each data source, you can configure separate rules for each version of the selected ER format.</span></span>
    
    <span data-ttu-id="2cf99-130">Temel ER biçiminin seçilen sürümünde var olan tüm arama veri kaynakları için kuralların tamamı, ER biçiminin uygulama özel parametrelerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2cf99-130">The whole set of rules for all lookup data sources that are available in the selected version of the base ER format makes up the application-specific parameters for the ER format.</span></span>

4.  <span data-ttu-id="2cf99-131">ER biçiminin **1.1.1** sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-131">Select version **1.1.1** of the ER format.</span></span>
5.  <span data-ttu-id="2cf99-132">**Koşullar** hızlı sekmesinde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-132">On the **Conditions** FastTab, select **Add**.</span></span>
6.  <span data-ttu-id="2cf99-133">Yeni kaydın **Kod** alanında aramayı açmak için açılır oku seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-133">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="2cf99-134">Arama, seçim için vergi kodlarının bir listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2cf99-134">The lookup presents the list of tax codes for selection.</span></span> <span data-ttu-id="2cf99-135">Bu liste, temel ER biçiminde yapılandırılmış **Model.Data.Tax** veri kaynağı tarafından döndürülür.</span><span class="sxs-lookup"><span data-stu-id="2cf99-135">This list is returned by the **Model.Data.Tax** data source that has been configured in the base ER format.</span></span> <span data-ttu-id="2cf99-136">Bu veri kaynağı **Ad** alanını içerdiğinden her vergi kodunun adı aramada görünür.</span><span class="sxs-lookup"><span data-stu-id="2cf99-136">Because this data source contains the **Name** field, the name of each tax code appears in the lookup.</span></span>

    ![ER uygulaması özel parametreler sayfası](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  <span data-ttu-id="2cf99-138">**VAT19** vergi kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-138">Select the **VAT19** tax code.</span></span>
8.  <span data-ttu-id="2cf99-139">Yeni kaydın **Arama sonucu** alanında aramayı açmak için açılır menü okunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-139">In the **Lookup result** field of the new record, select the drop-down arrow to open the lookup.</span></span> <span data-ttu-id="2cf99-140">Arama, seçimin TaxationLevel biçim numaralandırması için değerlerin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2cf99-140">The lookup presents the list of values for the TaxationLevel format enumeration for selection.</span></span>

    <span data-ttu-id="2cf99-141">Oturum açtığınız kullanıcının tercih ettiği dil olarak Almanca seçiliyse aramadaki değerlerin etiketlerinin temel ER biçiminde çevrilmiş olmaları koşuluyla Almanca olacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="2cf99-141">Note that, if German is selected as the preferred language of the user that you're signed in as, the labels of the values in the lookup will be in German, provided that they have been translated in the base ER format.</span></span> <span data-ttu-id="2cf99-142">Ek olarak, bir arama veri kaynağının etiketi çevrilmişse bu etiket kullanıcının **Aramalar** sekmesinde tercih ettiği dilde görünür.</span><span class="sxs-lookup"><span data-stu-id="2cf99-142">Additionally, if the label of a lookup data source has been translated, that label will appear in the user's preferred language on the **Lookups** tab.</span></span>

    ![ER uygulaması özel parametreler sayfası](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  <span data-ttu-id="2cf99-144">**Normal vergilendirme** değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-144">Select the **Regular taxation** value.</span></span>

    <span data-ttu-id="2cf99-145">Bu kaydı ekleyerek aşağıdaki kuralı tanımlarsınız: **Seçici** arama veri kaynağı talep edildiğinde ve **VAT19** vergi kodu bir bağımsız değişken olarak iletildiğinde istenen vergi seviyesi olarak **Normal vergilendirme** geri döndürülür.</span><span class="sxs-lookup"><span data-stu-id="2cf99-145">By adding this record, you define the following rule: Whenever the **Selector** lookup data source is requested, and the **VAT19** tax code is passed as an argument, **Regular taxation** will be returned as the requested taxation level.</span></span>

10. <span data-ttu-id="2cf99-146">**Ekle**'yi seçin ve ardından aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2cf99-146">Select **Add**, and then follow these steps:</span></span>

    1. <span data-ttu-id="2cf99-147">**Kod** alanında **InVAT19** vergi kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-147">In the **Code** field, select the **InVAT19** tax code.</span></span>
    2. <span data-ttu-id="2cf99-148">**Arama sonuçları** alanında **Normal vergilendirme** değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-148">In the **Lookup result** field, select the **Regular taxation** value.</span></span>
    
11. <span data-ttu-id="2cf99-149">Yeniden **Ekle**'yi seçin ve ardından aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2cf99-149">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="2cf99-150">**Kod** alanında **VAT7** vergi kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-150">In the **Code** field, select the **VAT7** tax code.</span></span>
    2. <span data-ttu-id="2cf99-151">**Arama sonuçları** alanında **Azaltılmış vergilendirme** değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-151">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
12. <span data-ttu-id="2cf99-152">Yeniden **Ekle**'yi seçin ve ardından aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2cf99-152">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="2cf99-153">**Kod** alanında **InVAT7** vergi kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-153">In the **Code** field, select the **InVAT7** tax code.</span></span>
    2. <span data-ttu-id="2cf99-154">**Arama sonuçları** alanında **Azaltılmış vergilendirme** değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-154">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
13. <span data-ttu-id="2cf99-155">Yeniden **Ekle**'yi seçin ve ardından aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2cf99-155">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="2cf99-156">**Kod** alanında **THIRD** vergi kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-156">In the **Code** field, select the **THIRD** tax code.</span></span>
    2. <span data-ttu-id="2cf99-157">**Arama sonuçları** alanında **Vergilendirme yok** değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-157">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
14. <span data-ttu-id="2cf99-158">Yeniden **Ekle**'yi seçin ve ardından aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2cf99-158">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="2cf99-159">**Kod** alanında **InVAT0** vergi kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-159">In the **Code** field, select the **InVAT0** tax code.</span></span>
    2. <span data-ttu-id="2cf99-160">**Arama sonuçları** alanında **Vergilendirme yok** değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-160">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
15. <span data-ttu-id="2cf99-161">Yeniden **Ekle**'yi seçin ve ardından aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2cf99-161">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="2cf99-162">**Kod** alanında **\*Boş değil\*** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-162">In the **Code** field, select the **\*Not blank\*** option.</span></span>
    2. <span data-ttu-id="2cf99-163">**Arama sonuçları** alanında **Diğer** değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-163">In the **Lookup result** field, select the **Other** value.</span></span>
    
    <span data-ttu-id="2cf99-164">Bu son kaydı ekleyerek aşağıdaki kuralı tanımlarsınız: Bağımsız değişken olarak geçirilen vergi kodu önceki kuralların herhangi birini karşılamadığında arama veri kaynağı istenen vergilendirme düzeyi olarak **Diğer** değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2cf99-164">By adding this last record, you define the following rule: Whenever the tax code that is passed as an argument doesn't satisfy any of the previous rules, the lookup data source will return **Other** as the requested taxation level.</span></span>

    ![ER uygulaması özel parametreler sayfası](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. <span data-ttu-id="2cf99-166">**Durum** alanında **Tamamlandı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-166">In the **State** field, select **Completed**.</span></span>

    <span data-ttu-id="2cf99-167">**Tamamlandı** veya **Paylaşılan** durumuna sahip bir ER biçimi sürümü çalıştırdığınızda bu kurallar kümesinin **Tamamlandı** durumunda olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2cf99-167">When you run an ER format version that has a status of either **Completed** or **Shared**, this set of rules must be in the **Completed** state.</span></span> <span data-ttu-id="2cf99-168">Aksi takdirde, **Seçici** arama veri kaynağı çalıştırılırken biçim, bu kurallar grubundan veri yüklemeye çalıştığında temel ER biçiminin yürütülmesi kesintiye uğrar.</span><span class="sxs-lookup"><span data-stu-id="2cf99-168">Otherwise, execution of the base ER format will be interrupted when the format tries to load data from this set of rules while the **Selector** lookup data source is being run.</span></span>
    
    <span data-ttu-id="2cf99-169">**Taslak** durumuna sahip bir ER biçimi sürümü çalıştırdığınızda temel ER biçimi, durumundan bağımsız olarak bu kurallara erişebilir.</span><span class="sxs-lookup"><span data-stu-id="2cf99-169">When you run an ER format version that has a status of **Draft**, the base ER format can access this set of rules, regardless of its state.</span></span>
    
17. <span data-ttu-id="2cf99-170">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-170">Select **Save**.</span></span>
18. <span data-ttu-id="2cf99-171">**Uygulama özel parametreleri** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="2cf99-171">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-demf-company"></a><span data-ttu-id="2cf99-172">DEMF şirketinde ER biçimini çalıştırma</span><span class="sxs-lookup"><span data-stu-id="2cf99-172">Run the ER format in the DEMF company</span></span>

1.  <span data-ttu-id="2cf99-173">Yapılandırma ağacında **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** biçimini seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-173">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="2cf99-174">Eylem Bölmesinde, **Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-174">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="2cf99-175">Görünen iletişim kutusunda **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-175">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="2cf99-176">Oluşturulan açıklamayı karşıdan yükleyin ve yerel olarak saklayın.</span><span class="sxs-lookup"><span data-stu-id="2cf99-176">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="2cf99-177">Oluşturulan açıklamada, **InVAT7** vergi kodunun özetinin **Azaltılmış** düzeye, **VAT19** ve **InVA19** vergi kodlarının özetlerinin **Normal** düzeye getirildiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-177">In the generated statement, notice that the summary of the **InVAT7** tax code has been put on the **Reduced** level, and the summaries of the **VAT19** and **InVA19** tax codes have been put on the **Regular** level.</span></span> <span data-ttu-id="2cf99-178">Bu davranış, tüzel kişiliğe bağlı kurallar kümesindeki yapılandırma tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="2cf99-178">This behavior is determined by the configuration in the legal entity–dependent set of rules.</span></span>
    
5.  <span data-ttu-id="2cf99-179">**Vergi \> Dolaylı vergiler \> Satış vergisi \> Satış vergisi kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-179">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>
6.  <span data-ttu-id="2cf99-180">**InVAT7** vergi kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-180">Select the **InVAT7** tax code.</span></span>
7.  <span data-ttu-id="2cf99-181">Vergi değeri ve vergi kodu başına uygulanan vergi oranı hakkındaki bilgileri görüntülemek için Eylem Bölmesinde, **Satış vergisi kodu** sekmesinde, **Sorgular** grubunda, **Deftere nakledilen satış vergisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-181">On the Action Pane, on the **Sales tax code** tab, in the **Inquiries** group, select **Posted sales tax** to view information about the tax value and applied tax rate per tax code.</span></span>

    ![Deftere nakledilen satış vergisi sayfası](./media/GER-AppSpecParms-Statement.PNG)

8.  <span data-ttu-id="2cf99-183">Deftere nakledilen satış vergisi sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="2cf99-183">Close the Posted sales tax page.</span></span>

## <a name="set-up-parameters-for-the-usmf-company"></a><span data-ttu-id="2cf99-184">USMF şirketi için parametreleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="2cf99-184">Set up parameters for the USMF company</span></span>

1.  <span data-ttu-id="2cf99-185">**USMF** tüzel kişiliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-185">Select the **USMF** legal entity.</span></span>
2.  <span data-ttu-id="2cf99-186">**Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="2cf99-186">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="2cf99-187">Yapılandırma ağacında, **Parametreli çağrıları öğrenme modeli** öğesini genişletin, **Parametreli çağrıları öğrenmek için biçimlendirme** öğesini genişletin ve **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** biçimini seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-187">In the configurations tree, expand the **Model to learn parameterized calls** item, expand the **Format to learn parameterized calls** item, and select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="2cf99-188">Eylem Bölmesinde, **Yapılandırmalar** sekmesindeki **Uygulama özel parametreleri** grubunda **Ayar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-188">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="2cf99-189">Seçili ER biçiminin **1.1.1** sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-189">Select version **1.1.1** of the selected ER format.</span></span>
6.  <span data-ttu-id="2cf99-190">**Koşullar** hızlı sekmesinde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-190">On the **Conditions** FastTab, select **Add**.</span></span>
7.  <span data-ttu-id="2cf99-191">Yeni kaydın **Kod** alanında aramayı açmak için açılır oku seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-191">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="2cf99-192">Arama şimdi, yapılan seçim için **USMF** şirket vergisinin vergi kodlarının bir listesini sunar.</span><span class="sxs-lookup"><span data-stu-id="2cf99-192">The lookup now presents the list of tax codes for the **USMF** company tax for selection.</span></span>

    ![ER uygulaması özel parametreler sayfası](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  <span data-ttu-id="2cf99-194">**EXEMPT** vergi kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-194">Select the **EXEMPT** tax code.</span></span>
9.  <span data-ttu-id="2cf99-195">Yeni kaydın **Arama sonuçları** alanında **Vergilendirme yok** değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-195">In the **Lookup resul** t field of the new record, select the **No taxation** value.</span></span>
10. <span data-ttu-id="2cf99-196">Yeniden **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-196">Select **Add** again.</span></span>
11. <span data-ttu-id="2cf99-197">Yeni kaydın **Kod** alanında **\*Boş değil\*** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-197">In the **Code** field of the new record, select the **\*Not blank\*** option.</span></span>
12. <span data-ttu-id="2cf99-198">Yeni kaydın **Arama sonuçları** alanında **Normal vergilendirme** değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-198">In the **Lookup result** field of the new record, select the **Regular taxation** value.</span></span>
13. <span data-ttu-id="2cf99-199">**Durum** alanında **Tamamlandı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-199">In the **State** field, select **Completed**.</span></span>
14. <span data-ttu-id="2cf99-200">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-200">Select **Save**.</span></span>

    ![ER uygulaması özel parametreler sayfası](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. <span data-ttu-id="2cf99-202">**Uygulama özel parametreleri** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="2cf99-202">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-usmf-company"></a><span data-ttu-id="2cf99-203">USMF şirketinde ER biçimini çalıştırma</span><span class="sxs-lookup"><span data-stu-id="2cf99-203">Run the ER format in the USMF company</span></span>

1.  <span data-ttu-id="2cf99-204">Yapılandırma ağacında **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** biçimini seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-204">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="2cf99-205">Eylem Bölmesinde, **Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-205">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="2cf99-206">Görünen iletişim kutusunda **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-206">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="2cf99-207">Oluşturulan açıklamayı karşıdan yükleyin ve yerel olarak saklayın.</span><span class="sxs-lookup"><span data-stu-id="2cf99-207">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="2cf99-208">Oluşturulan açıklamada, şimdi ER biçiminde herhangi bir ayarlama yapmadan aynı ER biçimini farklı bir tüzel kişilik için tekrar kullandığınız belirtilmektedir.</span><span class="sxs-lookup"><span data-stu-id="2cf99-208">In the generated statement, notice that you've now reused the same ER format for a different legal entity, but without making any adjustments to the ER format.</span></span>

## <a name="reuse-legal-entitydependent-parameters"></a><span data-ttu-id="2cf99-209">Tüzel kişiliye bağlı parametreleri yeniden kullanma</span><span class="sxs-lookup"><span data-stu-id="2cf99-209">Reuse legal entity–dependent parameters</span></span>

### <a name="export-parameters"></a><span data-ttu-id="2cf99-210">Parametreleri dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="2cf99-210">Export parameters</span></span>

1.  <span data-ttu-id="2cf99-211">**Organizasyon yönetimi \> Çalışma alanları \> Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-211">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2.  <span data-ttu-id="2cf99-212">**Raporlama yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-212">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="2cf99-213">Yapılandırma ağacında **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** biçimini seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-213">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="2cf99-214">Eylem Bölmesinde, **Yapılandırmalar** sekmesindeki **Uygulama özel parametreleri** grubunda **Ayar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-214">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="2cf99-215">ER biçiminin **1.1.1** sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-215">Select version **1.1.1** of the ER format.</span></span>
6.  <span data-ttu-id="2cf99-216">Eylem Bölmesinde **Dışa aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-216">On the Action Pane, select **Export**.</span></span>
7.  <span data-ttu-id="2cf99-217">Oluşturulan dosyayı karşıdan yükleyin ve yerel olarak saklayın.</span><span class="sxs-lookup"><span data-stu-id="2cf99-217">Download the file that is generated and store it locally.</span></span>

    <span data-ttu-id="2cf99-218">Yapılandırılmış uygulamaya özel parametreler kümesi artık bir XML dosyası olarak dışa aktarıldı.</span><span class="sxs-lookup"><span data-stu-id="2cf99-218">The configured set of application-specific parameters has now been exported as an XML file.</span></span>

### <a name="import-parameters"></a><span data-ttu-id="2cf99-219">Parametreleri içe aktarma</span><span class="sxs-lookup"><span data-stu-id="2cf99-219">Import parameters</span></span>

1.  <span data-ttu-id="2cf99-220">ER biçiminin **1.1.2** sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-220">Select version **1.1.2** of the ER format.</span></span>
2.  <span data-ttu-id="2cf99-221">Eylem Bölmesinde, **İçe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-221">On the Action Pane, select **Import**.</span></span>
3.  <span data-ttu-id="2cf99-222">Bu biçim sürümü için var olan uygulamaya özel parametreleri geçersiz kılmak istediğinizi onaylamak üzere **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-222">Select **Yes** to confirm that you want to override the existing application-specific parameters for this format version.</span></span>
4.  <span data-ttu-id="2cf99-223">**1.1.1** sürümü için dışa aktarılan uygulamaya özel parametreleri içeren dosyayı bulmak üzere **Gözat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-223">Select **Browse** to find the file that contains the exported application-specific parameters for version **1.1.1**.</span></span>
5.  <span data-ttu-id="2cf99-224">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-224">Select **OK**.</span></span>

    <span data-ttu-id="2cf99-225">ER biçiminin **1.1.2** sürümü, başlangıçta **1.1.1** sürümü için yapılandırdığınız uygulamaya özel parametrelere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="2cf99-225">Version **1.1.2** of the ER format now has the same application-specific parameters that you originally configured for version **1.1.1**.</span></span>
    
    <span data-ttu-id="2cf99-226">ER biçiminin uygulamaya özel parametrelerinin tüzel kişiliğe bağlı olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="2cf99-226">Note that the application-specific parameters of an ER format are legal entity–dependent.</span></span> <span data-ttu-id="2cf99-227">Bir tüzel kişilik için yapılandırılmış olan uygulamaya özel parametreleri farklı bir tüzel kişilikte yeniden kullanmak için ilk tüzel kişilikte oturum açtığınızda bunları dışa aktarmalı ve diğer tüzel kişilikte oturum açtıktan sonra içe aktarmalısınız.</span><span class="sxs-lookup"><span data-stu-id="2cf99-227">To reuse the application-specific parameters that were configured for one legal entity in a different legal entity, you must export them while you're signed in to the first legal entity and then import them after you sign in to the other legal entity.</span></span>

    <span data-ttu-id="2cf99-228">Bu yaklaşımı, ilk olarak bir Finance kurulumunda yapılandırılmış olan uygulamaya özel parametreleri ER biçimiyle ilgili başka bir Finance kurulumuna aktarmak için de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2cf99-228">You can also use this approach to transfer an ER format related application-specific parameters that were originally configured in one instance of Finance to another instance of Finance.</span></span>

    <span data-ttu-id="2cf99-229">ER biçiminin bir sürümü için uygulamaya özel parametreler yapılandırırsanız ve aynı biçimin daha yüksek bir sürümünü geçerli Finance kurulumuna içe aktarırsanız var olan uygulamaya özel parametrelerin, içe aktarılan sürüm için uygulanmayacağına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-229">Be aware that if you configure application-specific parameters for one version of an ER format and import a higher version of the same format into the current Finance instance, the existing application-specific parameters won't be applied for the imported version.</span></span>
    
    <span data-ttu-id="2cf99-230">Ayrıca, içe aktarmak için bir dosya seçtiğinizde bu dosyadaki uygulamaya özel parametrelerin yapısının, içe aktarma için seçilen ER biçimindeki **Arama** türünde karşılık gelen veri kaynağının yapısıyla karşılaştırıldığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="2cf99-230">Also be aware that, when you select a file for import, the structure of the application-specific parameters in that file is compared with the structure of the corresponding data source of the **Lookup** type in the ER format that is selected for import.</span></span> <span data-ttu-id="2cf99-231">İçe aktarma, uygulamaya özel her parametrenin yapısı içe aktarma için seçilen ER biçiminde ilgili veri kaynağının yapısıyla eşleştiğinde gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="2cf99-231">The import is done when the structure of each application-specific parameter matches the structure of the corresponding data source in the ER format that is selected for import.</span></span> <span data-ttu-id="2cf99-232">Yapılar eşleşmezse içe aktarmanın yapılamadığını bildiren bir uyarı iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="2cf99-232">If the structures don't match, you receive a warning message that states that the import can't be done.</span></span> <span data-ttu-id="2cf99-233">İçe aktarma işleminin yapılmasını zorlarsanız seçilen ER biçimi için uygulamaya özel var olan parametreler temizlenir ve bunları en baştan ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2cf99-233">If you force the import to be done, the existing application-specific parameters for the selected ER format will be cleaned up, and you must set them up from the beginning.</span></span>

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a><span data-ttu-id="2cf99-234">Uygulamaya özel parametreler ile ER biçimi arasındaki ilişki</span><span class="sxs-lookup"><span data-stu-id="2cf99-234">Relationship between application-specific parameters and an ER format</span></span>

<span data-ttu-id="2cf99-235">ER biçimi ile uygulamaya özel parametreler arasındaki ilişki, ER biçiminin kurulumdan bağımsız benzersiz tanımlama kodu ile kurulur.</span><span class="sxs-lookup"><span data-stu-id="2cf99-235">The relationship between an ER format and its application-specific parameters is established by the ER format's instance-independent unique identification code.</span></span> <span data-ttu-id="2cf99-236">Bu nedenle, bir ER biçimini Finance'tan kaldırdığınızda ER biçimi için yapılandırılmış olan uygulamaya özel parametreler geçerli Finance kurulumunda tutulur.</span><span class="sxs-lookup"><span data-stu-id="2cf99-236">Therefore, when you remove an ER format from Finance, the application-specific parameters that are configured for the ER format are kept in the current instance of Finance.</span></span> <span data-ttu-id="2cf99-237">Temel ER biçimi, bu Finance kurulumuna yeniden içe aktarıldığında bunlara erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="2cf99-237">They can be accessed whenever the base ER format is reimported into this instance of Finance.</span></span>

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a><span data-ttu-id="2cf99-238">ER çerçevesini kullanarak uygulamaya özel parametrelere erişme</span><span class="sxs-lookup"><span data-stu-id="2cf99-238">Access application-specific parameters by using the ER framework</span></span>

<span data-ttu-id="2cf99-239">Önceki örnekte, ER çerçevesini kullanarak ER biçimindeki uygulamaya özel parametrelere eriştiniz.</span><span class="sxs-lookup"><span data-stu-id="2cf99-239">In the preceding example, you have accessed application-specific parameters of an ER format by using the ER framework.</span></span> <span data-ttu-id="2cf99-240">Bu yaklaşım, belirli bir ER biçiminin uygulamaya özel parametrelerine erişimi kısıtlamanıza izin vermez.</span><span class="sxs-lookup"><span data-stu-id="2cf99-240">This approach doesn't let you restrict access to the application-specific parameters of a specific ER format.</span></span> <span data-ttu-id="2cf99-241">Bu tür kısıtlamalar uygulamanız gerekiyorsa aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2cf99-241">If you must apply such restrictions, follow these steps.</span></span> 

1.  <span data-ttu-id="2cf99-242">Var olan bir **ERSolutionAppSpecificParametersDesigner** menü öğesini yeniden kullanın veya kendi **ERSolutionAppSpecificParametersDesigner** menü öğenizi uygulayın.</span><span class="sxs-lookup"><span data-stu-id="2cf99-242">Either reuse an existing **ERSolutionAppSpecificParametersDesigner** menu item, or implement your own **ERSolutionAppSpecificParametersDesigner** menu item.</span></span>

    ![Visual Studio sayfası](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  <span data-ttu-id="2cf99-244">Şu adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="2cf99-244">Follow one of these steps:</span></span>

    1.  <span data-ttu-id="2cf99-245">Yeni bir menü öğesi düğmesi oluşturun ve **Veri Kaynağı** özelliğini **ERSolutionTable** olarak ayarlayarak **ERSolutionTable** tablosundan ilgili kayda bağlayın.</span><span class="sxs-lookup"><span data-stu-id="2cf99-245">Create a new menu item button, and link it to the corresponding record from the **ERSolutionTable** table by setting its **Data Source** property to **ERSolutionTable**.</span></span>
    
        ![Visual Studio sayfası](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  <span data-ttu-id="2cf99-247">Basit bir düğme oluşturun ve aşağıdaki örnekte gösterildiği gibi **Tıklandı** yöntemini geçersiz kılın.</span><span class="sxs-lookup"><span data-stu-id="2cf99-247">Create a simple button, and override the **Clicked** method as shown in the following example.</span></span>
    
        <span data-ttu-id="2cf99-248">Bu yaklaşımı kullanarak, yalnızca belirli bir ER biçiminin ve ondan türetilmiş alt öğe kopyalarının uygulamaya özel parametrelerine erişim izni vermek için (**GUID** değeri ile tanımlanmış) benzersiz bir çözüm kimliği belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2cf99-248">By using this approach, you can specify a unique solution ID (defined via the **GUID** value) to allow access to the application-specific parameters of only a specific ER format and descendant copies that have been derived from it.</span></span>
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a><span data-ttu-id="2cf99-249">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2cf99-249">Additional resources</span></span>

[<span data-ttu-id="2cf99-250">Elektronik raporlamada formül tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="2cf99-250">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="2cf99-251">Her tüzel kişilik için belirtilen parametreleri kullanmak için ER biçimlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2cf99-251">Configure ER formats to use parameters that are specified per legal entity</span></span>](er-app-specific-parameters-configure-format.md)
