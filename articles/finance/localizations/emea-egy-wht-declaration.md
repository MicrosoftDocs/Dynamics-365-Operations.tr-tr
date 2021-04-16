---
title: Mısır için stopaj vergisi beyanı
description: Bu konu, Mısır için stopaj vergisi beyanının nasıl yapılandırılacağını ve oluşturulacağını açıklar.
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4e3d68ac003fabaa504ffe81b8bf2f7ff8d7538d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839804"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a><span data-ttu-id="de0bd-103">Mısır için stopaj vergisi beyanı (EG-00005)</span><span class="sxs-lookup"><span data-stu-id="de0bd-103">Withholding tax declaration for Egypt (EG-00005)</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a><span data-ttu-id="de0bd-104">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="de0bd-104">Overview</span></span>
<span data-ttu-id="de0bd-105">Bu konu, Mısır'da yasal varlıklar için stopaj vergisi beyanı ve stopaj vergisi beyanı formları Form 41 ve Form 11'in nasıl ayarlanacağını ve oluşturulacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="de0bd-105">This topic explains how to set up and generate the withholding tax declaration and the withholding tax declaration forms 41 and 11 for legal entities in Egypt</span></span> 

<span data-ttu-id="de0bd-106">Tüm Mısırlı varlıklar yerel tedarikçiler ve servis sağlayıcılarından alınan tüm vergileri özetleyen Form 41'i hazırlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="de0bd-106">All Egyptian entities must prepare the form  41 which summarizes all taxes that are retained from local suppliers and service providers.</span></span> <span data-ttu-id="de0bd-107">Form 41'in yanı sıra, yabancı sağlayıcılardan alınan tüm vergilerin ayrıntılarını belirtmek için form 11'i oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="de0bd-107">In addition to form 41, form 11 must be generated to detail all of the retained taxed from foreign providers.</span></span> 

<span data-ttu-id="de0bd-108">Dynamics 365 Finance'deki **stopaj vergisi beyan** raporu aşağıdaki raporları içerir:</span><span class="sxs-lookup"><span data-stu-id="de0bd-108">The **Withholding tax declaration** report in Dynamics 365 Finance includes the following reports:</span></span>

- <span data-ttu-id="de0bd-109">Beyan formu No.</span><span class="sxs-lookup"><span data-stu-id="de0bd-109">Declaration form No.</span></span> <span data-ttu-id="de0bd-110">41</span><span class="sxs-lookup"><span data-stu-id="de0bd-110">41</span></span>
- <span data-ttu-id="de0bd-111">Beyan formu No.</span><span class="sxs-lookup"><span data-stu-id="de0bd-111">Declaration form No.</span></span> <span data-ttu-id="de0bd-112">11</span><span class="sxs-lookup"><span data-stu-id="de0bd-112">11</span></span>
    
    
## <a name="prerequisites"></a><span data-ttu-id="de0bd-113">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="de0bd-113">Prerequisites</span></span>
<span data-ttu-id="de0bd-114">Yasal varlığın birincil adresi Mısır'da olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="de0bd-114">The primary address of the legal entity must be in Egypt.</span></span>
<span data-ttu-id="de0bd-115">**Özellik yönetimi** çalışma alanında şu özellik etkinleştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="de0bd-115">In the **Feature management** workspace, the following feature must be enabled:</span></span>

   - <span data-ttu-id="de0bd-116">**Genel stopaj vergisi**</span><span class="sxs-lookup"><span data-stu-id="de0bd-116">**Global withholding tax**</span></span>

<span data-ttu-id="de0bd-117">Özellikleri etkinleştirme hakkında daha fazla bilgi için [Özellik yönetimine genel bakış](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'a bakın</span><span class="sxs-lookup"><span data-stu-id="de0bd-117">For more information about how to enable features, see [Feature management overview.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span></span>

1. <span data-ttu-id="de0bd-118">**Vergi** > **Kurulum** > **Parametreler** > **Genel kayıt defteri parametreleri**'ne gidin ve **Stopaj vergisi** sekmesinde **Genel stopaj vergisini etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="de0bd-118">Go to **Tax** > **Setup** > **Parameters** > **General ledger parameters**, and on the **Withholding tax** tab, set **Enable global withholding tax** to **Yes**.</span></span>
2. <span data-ttu-id="de0bd-119">**Elektronik raporlama** çalışma alanında, aşağıdaki elektronik raporlama biçimlerini depodan içe aktarın:</span><span class="sxs-lookup"><span data-stu-id="de0bd-119">In the **Electronic reporting** workspace, import the following Electronic reporting formats from the repository:</span></span>

    - <span data-ttu-id="de0bd-120">WHT Beyannamesi Excel'i(EG)</span><span class="sxs-lookup"><span data-stu-id="de0bd-120">WHT Declaration Excel (EG)</span></span>

    > [!NOTE]
    > <span data-ttu-id="de0bd-121">Yukarıdaki biçim **Vergi beyanı modeline** dayanır ve **vergi beyanı model eşleştirmesini** kullanır.</span><span class="sxs-lookup"><span data-stu-id="de0bd-121">The format above is based on the **Tax declaration model** and uses the **Tax declaration model mapping**.</span></span> <span data-ttu-id="de0bd-122">Bu ek yapılandırmalar otomatik olarak alınır.</span><span class="sxs-lookup"><span data-stu-id="de0bd-122">This additional configuration is automatically imported.</span></span>

<span data-ttu-id="de0bd-123">Elektronik raporlama yapılandırmalarını içe aktarma hakkında daha fazla bilgi için, bkz. [Elektronik raporlama yapılandırmalarını Lifecycle Services'den indirme](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="de0bd-123">For more information about how to import Electronic reporting configurations, see [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

## <a name="download-electronic-reporting-configurations"></a><span data-ttu-id="de0bd-124">Elektronik raporlama yapılandırmalarını indirme</span><span class="sxs-lookup"><span data-stu-id="de0bd-124">Download Electronic reporting configurations</span></span>

<span data-ttu-id="de0bd-125">Mısır için WHT beyan formunun uygulanması, elektronik raporlama (ER) yapılandırmalarına dayanır.</span><span class="sxs-lookup"><span data-stu-id="de0bd-125">The implementation of the WHT declaration forms for Egypt is based on Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="de0bd-126">Yapılandırılabilir raporlamanın özellikleri ve kavramları hakkında daha fazla bilgi için [Elektronik raporlama](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="de0bd-126">For more information about the capabilities and concepts of configurable reporting, see [Electronic reporting](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

<span data-ttu-id="de0bd-127">Üretim ve Kullanıcı kabul sınamaları (UAT) ortamları için, [Elektronik raporlama yapılandırmalarını Lifecycle Services'den indirme](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md) konusundaki yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-127">For production and user acceptance testing (UAT) environments, follow the instructions in the topic, [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

<span data-ttu-id="de0bd-128">Bir Mısır yasal varlığında stopaj beyanları oluşturmak için, aşağıdaki yapılandırmaları yüklemeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="de0bd-128">To generate the Withholding declarations in an Egyptian legal entity, you need to upload the following configurations:</span></span>

- <span data-ttu-id="de0bd-129">Vergi beyanı modeli.sürüm.82.xml veya sonraki sürüm</span><span class="sxs-lookup"><span data-stu-id="de0bd-129">Tax declaration model.version.82.xml or later version</span></span>
- <span data-ttu-id="de0bd-130">Vergi beyanı modeli eşleme.sürümü.82.133.xml veya sonraki sürüm</span><span class="sxs-lookup"><span data-stu-id="de0bd-130">Tax declaration model mapping.version.82.133.xml or a later version</span></span>
- <span data-ttu-id="de0bd-131">WHT Beyanı Excel'i (EG).sürüm.82.21 veya sonraki bir sürüm</span><span class="sxs-lookup"><span data-stu-id="de0bd-131">WHT Declaration Excel (EG).version.82.21  or a later version</span></span>

<span data-ttu-id="de0bd-132">Lifecycle Services (LCS) veya genel depodan ER yapılandırmalarını indirmeyi tamamladıktan sonra aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="de0bd-132">After you finish downloading the ER configurations from Lifecycle Services (LCS) or the global repository, complete the following steps.</span></span>

1. <span data-ttu-id="de0bd-133">**Elektronik raporlama** çalışma alanına gidin ve **Raporlama yapılandırmaları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-133">Go to the **Electronic reporting** workspace and select the **Reporting configurations** tile.</span></span>
1. <span data-ttu-id="de0bd-134">**Yapılandırmalar** sayfasında Eylem Bölmesindeki **Değiştir > XML dosyasından yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-134">On the **Configurations** page, on the Action Pane, select **Exchange > Load from XML file**.</span></span>
1. <span data-ttu-id="de0bd-135">Tüm dosyaları önceki madde işaretlerinde listelendikleri sırayla yükleyin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-135">Upload all the files in the order in which they are listed in the previous bullets.</span></span> <span data-ttu-id="de0bd-136">Tüm yapılandırmalar yüklendikten sonra, yapılandırma ağacının Finance'te bulunması gerekir.</span><span class="sxs-lookup"><span data-stu-id="de0bd-136">After all of the configurations are uploaded, the configuration tree should be present in Finance.</span></span>

## <a name="set-up-application-specific-parameters"></a><span data-ttu-id="de0bd-137">Uygulamaya özgü parametreleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="de0bd-137">Set up application-specific parameters</span></span>

<span data-ttu-id="de0bd-138">Uygulamaya özgü parametreler seçeneği, **Stopaj vergisi öğe grubu** yapılandırmasına veya aramanın tanımında belirtilen başka kriterlere bağlı olarak kullanıcıların vergi işlemlerinin oluşturulan raporun her satırında nasıl sınıflandırılacağını ve hesaplanacağını belirten kriterleri belirlemesine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="de0bd-138">The application-specific parameters option lets users establish the criteria of how the tax transactions will be classified and calculated in each line of a generated report depending on the configuration of **withholding tax item group** or other criteria established in the definition of lookup.</span></span>

<span data-ttu-id="de0bd-139">Stopaj beyanı formu Form 41, stopaj vergisi işlemlerinin **indirim kodu türü** adlı vergi dairesi sınıflandırmasına göre sınıflandırılmasının gerektiği belirli bir sütun içerir.</span><span class="sxs-lookup"><span data-stu-id="de0bd-139">Withholding declaration form 41 includes a specific column where the withholding tax transaction must be classified in accordance with the tax authority classification named **Discount code type**.</span></span> <span data-ttu-id="de0bd-140">İşlemler deftere nakledilirken bu yeni sınıflandırmaları yeni giriş verileri olarak eklemek yerine, sınıflandırmalar, Mısır için stopaj raporlarının gereksinimlerini karşılayacak şekilde **Yapılandırmalar** > **Uygulamaya özgü parametreler ayarla** > **Ayarla** bölümünde sunulan farklı aramalara göre belirlenecektir.</span><span class="sxs-lookup"><span data-stu-id="de0bd-140">Instead of including these new classifications as new entry data when the transactions are posted, the classifications will be determined based on the different lookups introduced in **Configurations** > **Set up application-specific parameters** > **Setup** to meet the requirements of withholding reports for Egypt.</span></span> 

<span data-ttu-id="de0bd-141">Aşağıdaki yapılandırma stopaj beyanı formu Form 41 raporunda bulunan işlemleri sınıflandırmak için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="de0bd-141">The following configuration is used to classify the transactions in the Withholding declaration form 41 report:</span></span>

- <span data-ttu-id="de0bd-142">**DiscountTaxTypeLookup** -> Sütun No 18</span><span class="sxs-lookup"><span data-stu-id="de0bd-142">**DiscountTaxTypeLookup**-> Column No 18</span></span> 

<span data-ttu-id="de0bd-143">WHT beyanı ve ilgili defter raporları oluşturmak için kullanılan farklı aramaları ayarlamak üzere aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="de0bd-143">Complete the following steps to set up the different lookups used to generate the WHT declaration and related books reports.</span></span> 

1. <span data-ttu-id="de0bd-144">**Elektronik raporlama** çalışma alanında, WHT beyan raporunda işlemleri sınıflandırma kurallarını ayarlamak için **Yapılandırmalar** > **Ayarla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-144">In the **Electronic reporting** workspace, select **Configurations** > **Setup** to set up the rules to identify how transactions are classified in the WHT declaration report.</span></span> 
2. <span data-ttu-id="de0bd-145">Geçerli sürümü seçin ve **aramalar** hızlı sekmesinde arama adını seçin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-145">Select the current version, and on the **Lookups** FastTab, select the lookup name.</span></span> <span data-ttu-id="de0bd-146">Örneğin, **DiscountTaxTypeLookup**.</span><span class="sxs-lookup"><span data-stu-id="de0bd-146">For example, **DiscountTaxTypeLookup**.</span></span> <span data-ttu-id="de0bd-147">Bu arama vergi dairesi için gereken indirim tiplerinin listesini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="de0bd-147">This lookup identifies the list of discount types required by the tax authority.</span></span>
3. <span data-ttu-id="de0bd-148">**Koşullar** hızlı sekmesinde, **Ekle**'yi seçin ve **Arama sonucu** sütunundaki yeni satıra **Sütun 18**'deki sınıflandırmayı temsil eden ilgili satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-148">On the **Conditions** FastTab, select **Add** and in the new line in the **Lookup result** column, select the related line that represents the classification in the **Column 18**.</span></span>
4. <span data-ttu-id="de0bd-149">**Stopaj vergisi öğe grubu** sütununda, Sınıflandırmayı tanımlamak için kullanılan ilgili kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-149">In the **Withholding tax item group** column, select the related code that's used to identify the classification.</span></span> <span data-ttu-id="de0bd-150">Örneğin, **izin verilen indirim**.</span><span class="sxs-lookup"><span data-stu-id="de0bd-150">For example, **Allowed discount**.</span></span>  
5. <span data-ttu-id="de0bd-151">Tüm kullanılabilir aramalar için 3. ve 4. adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-151">Repeat steps 3 and 4 for all available lookups.</span></span>
6. <span data-ttu-id="de0bd-152">Son kayıt satırını eklemek için **Ekle**'yi tekrar seçin ve **Arama sonucu** sütununda **Geçerli değil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-152">Select **Add** again to include the final record line, and in the **Lookup result** column, select **Not applicable**.</span></span> 
7. <span data-ttu-id="de0bd-153">Kalan sütunlarda, **boş değil** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-153">In the remaining columns, select **Not blank**.</span></span> 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a><span data-ttu-id="de0bd-154">Genel kayıt defteri parametreleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="de0bd-154">Set up General ledger parameters</span></span>

<span data-ttu-id="de0bd-155">Microsoft Excel biçiminde WHT beyan formu raporları oluşturmak için **Genel kayıt defteri parametreleri** sayfasında bir ER biçimi tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="de0bd-155">To generate the WHT declaration form reports in Microsoft Excel, define an ER format on the **General ledger parameters** page.</span></span>

1. <span data-ttu-id="de0bd-156">**Vergi** > **Ayar** > **Genel kayıt defteri parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-156">Go to **Tax** > **Setup** > **General ledger parameters**.</span></span>
2. <span data-ttu-id="de0bd-157">**Stopaj vergisi** sekmesinde, **WHT beyan biçimi eşlemesi** alanında, **WHT Beyanı Excel'i (EG)** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-157">On the **Withholding tax** tab, in the **WHT declaration format mapping** field, select **WHT Declaration Excel (EG)**.</span></span> <span data-ttu-id="de0bd-158">Alanı boş bırakırsanız, SSRS biçiminde standart satış vergisi raporu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="de0bd-158">If you leave the field blank, the standard sales tax report will be generated in SSRS format.</span></span>


![Beyan formu](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a><span data-ttu-id="de0bd-160">Stopaj beyanı formlarını oluştur</span><span class="sxs-lookup"><span data-stu-id="de0bd-160">Generate the Withholding declaration forms</span></span>
<span data-ttu-id="de0bd-161">Stopaj beyanı formunun belirli bir dönem için hazırlanması ve gönderilmesi işlemi, ödeme vergisini kapatma ve deftere nakletme işi sırasında deftere nakledilen stopaj vergisi işlemlerine dayanır.</span><span class="sxs-lookup"><span data-stu-id="de0bd-161">The process of preparing and submitting a Withholding declaration form for a specific period is based on the withholding tax transactions posted during the settle and post payment tax job.</span></span> <span data-ttu-id="de0bd-162">Genel stopaj vergisi hakkında daha fazla bilgi için bkz. [Genel stopaj vergisi](../general-ledger/global-withholding-tax-overview.md).</span><span class="sxs-lookup"><span data-stu-id="de0bd-162">For more information about global withholding tax, see [Global withholding tax](../general-ledger/global-withholding-tax-overview.md).</span></span>

<span data-ttu-id="de0bd-163">Vergi beyanı raporunu oluşturmak için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="de0bd-163">Complete the following steps to generate the tax declaration report.</span></span>

1. <span data-ttu-id="de0bd-164">**Vergi** > **Beyanlar** > **Stopaj vergisi** > \**Stopaj vergisi ödemesi*'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-164">Go to **Tax** > **Declarations** > **Withholding tax** > \**Withholding tax payment*.</span></span>
2. <span data-ttu-id="de0bd-165">Kapatma dönemini seçin ve rapor için başlangıç tarihini seçin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-165">Select the settlement period and then select the from date for the report.</span></span> 
3. <span data-ttu-id="de0bd-166">İşlem tarihini girin ve ardından **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-166">Enter the transaction date and then select **OK**.</span></span>
4. <span data-ttu-id="de0bd-167">Açılan iletişim kutusunda bir veya daha fazla form türü seçin **Form No. 41**, **Form No. 11** veya **yok**.</span><span class="sxs-lookup"><span data-stu-id="de0bd-167">In the dialog box that opens, select one or more of the form types \*\*Form No 41 \*\*, **Form No 11**, or **None**.</span></span> <span data-ttu-id="de0bd-168">**Yok** seçeneğini belirlerseniz standart rapor oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="de0bd-168">If you select **None**, the standard report is generated.</span></span> 
5. <span data-ttu-id="de0bd-169">Dili seçin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-169">Select the language.</span></span> <span data-ttu-id="de0bd-170">Tüm raporlar **en-us** ve **ar-eg** dillerine çevrilir.</span><span class="sxs-lookup"><span data-stu-id="de0bd-170">All reports are translated in **en-us** and **ar-eg**.</span></span>
6. <span data-ttu-id="de0bd-171">Vergi ödemesinin yapılacağı bankanın adını ve şubesini girin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-171">Enter the branch and name of the bank where the tax payment will be paid.</span></span>
7. <span data-ttu-id="de0bd-172">İş türünü seçin ve sonra çek ve belge numaralarını girin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-172">Select the business type and then enter the check and document numbers.</span></span> 
8. <span data-ttu-id="de0bd-173">Varlık tipini girin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-173">Enter the entity type.</span></span> 
9. <span data-ttu-id="de0bd-174">Formu atamak için kayıtlı kişinin adını girin ve rapor oluşturmayı onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="de0bd-174">Enter the name of person registered to assign the form and select **OK** to confirm the report generation.</span></span> 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
