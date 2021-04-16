---
title: Müşteri ödeme tahminlerini etkinleştirme (önizleme)
description: Bu konuda, Mali içgörülerde Müşteri ödeme tahminleri özelliğinin nasıl açılacağı ve yapılandırılacağı açıklanmaktadır.
author: ShivamPandey-msft
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ecc3851cc91c8fe17a7582f2be06e84cf9bc2d83
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818668"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="7fbaa-103">Müşteri ödeme tahminlerini etkinleştirme (önizleme)</span><span class="sxs-lookup"><span data-stu-id="7fbaa-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="7fbaa-104">Bu konuda, Mali içgörülerde Müşteri ödeme tahminleri özelliğinin nasıl açılacağı ve yapılandırılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="7fbaa-105">Özelliği **Özellik yönetimi** çalışma alanında açabilir ve yapılandırma ayarlarını **Mali içgörüler parametreleri** sayfasında girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="7fbaa-106">Bu konu ayrıca özelliği etkili şekilde kullanmanıza yardımcı olabilecek bilgiler de içerir.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="7fbaa-107">Aşağıdaki adımları tamamlamadan önce, [Mali içgörüler için yapılandırma](configure-for-fin-insites.md) konusundaki ön koşul adımlarını tamamladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="7fbaa-108">Ortamın birincil Azure SQL kurulumuna bağlanmak için Microsoft Dynamics Lifecycle Services (LCS) portalındaki ortam sayfasında yer alan bilgileri kullanın.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="7fbaa-109">Korumalı alan ortamına sınırlı dağıtımları açmak için aşağıdaki Transact-SQL (T-SQL) komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="7fbaa-110">(Uygulama Nesne Sunucusu \[AOS\] hizmetine uzaktan bağlanmadan önce IP adresinize erişimi açmanız gerekebilir.)</span><span class="sxs-lookup"><span data-stu-id="7fbaa-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > <span data-ttu-id="7fbaa-111">Microsoft Dynamics 365 Finance dağıtımınız Service Fabric dağıtımıysa bu adımı atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-111">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="7fbaa-112">Mali içgörüler ekibi, bu sınırlı dağıtımı sizin için açmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="7fbaa-113">Özelliği **Özellik yönetimi** çalışma alanında görmüyorsanız veya özelliği açmaya çalışırken sorun yaşıyorsanız <fiap@microsoft.com> adresiyle iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-113">If you don't see the feature in the **Feature management** workspace, or if experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="7fbaa-114">Müşteri ödeme içgörüleri özelliğini açın:</span><span class="sxs-lookup"><span data-stu-id="7fbaa-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="7fbaa-115">**Sistem yönetimi \> Çalışma alanları \> Özellik yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="7fbaa-116">**Müşteri ödeme içgörüleri (önizleme)** adlı özelliği bulun.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="7fbaa-117">**Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-117">Select **Enable now**.</span></span>

    <span data-ttu-id="7fbaa-118">Müşteri ödeme içgörüleri özelliği açılır ve yapılandırmaya hazır hale gelir.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="7fbaa-119">Müşteri ödeme içgörüleri özelliğini yapılandırın:</span><span class="sxs-lookup"><span data-stu-id="7fbaa-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="7fbaa-120">**Alacak ve tahsilatlar \> Kurulum \> Mali içgörüler \> Mali içgörü parametreleri** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="7fbaa-121">[![Özellik yapılandırılmadan önce mali içgörü parametreleri sayfası](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="7fbaa-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="7fbaa-122">**Mali içgörü parametreleri** sayfasındaki **Müşteri ödeme içgörüleri** sekmesinde, **Tahmin modeli için veri alanları** sayfasını açmak için **Tahmin modelinde kullanılan veri alanlarını göster** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="7fbaa-123">Burada, müşteri ödeme tahminleriyle ilgili yapay zeka (AI) tahmin modeli oluşturmak için kullanılan varsayılan alanların listesini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="7fbaa-124">Tahmin modelini oluşturmak için varsayılan alan listesini kullanmak üzere, **Tahmin modeli için veri alanları** sayfasını kapatın ve sonra **Mali içgörü parametreleri** sayfasında, **Özelliği etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="7fbaa-125">İşletmeniz için **Çok geç** tahmin demetinin ne anlama geldiğini tanımlamak için "çok geç" hareket dönemini belirtin.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="7fbaa-126">Her açık fatura için sistem, ödemenin olasılığını üç demette tahmin eder: **Zamanında**, **Geç** ve **Çok geç**.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="7fbaa-127">**Zamanında**: Bu demet, işlem vade tarihinde veya bu tarihten önce ödenmesi öngörülen ödemeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="7fbaa-128">**Geç**: Bu demet, hareket vade tarihinden sonra ancak "çok geç" hareket döneminin başlangıcından önce ödenmesi öngörülen ödemeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="7fbaa-129">**Çok geç**: Bu demet, "çok geç" hareket döneminin başlangıcından sonra ödenmesi öngörülen ödemeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="7fbaa-130">"Çok geç" hareket dönemini değiştirirseniz ve müşteri ödemeleri için AI tahmin modeli oluşturulduktan sonra **Geç eşiğini değiştir**'i seçerseniz, mevcut tahmin modeli silinir ve yeni bir model oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="7fbaa-131">Yeni tahmin modeli, dönemi tanımlamak için girilmiş olan ayarlara göre hareketleri "çok geç" dönemine taşır.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="7fbaa-132">"Çok geç" hareket dönemini tanımlamayı bitirdikten sonra, tahmin modelini oluşturmak için **Tahmin modeli oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="7fbaa-133">**Mali içgörü parametreleri** sayfasındaki **Tahmin modeli** bölümü, tahmin modelinin durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="7fbaa-134">Tahmin modeli oluşturulurken istediğiniz zaman, işlemi yeniden başlatmak için **Model oluşturma işlemini sıfırla**'yı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="7fbaa-135">Özellik şimdi yapılandırılmış ve kullanılmaya hazır olur.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="7fbaa-136">Özellik açılıp yapılandırıldıktan ve tahmin model oluşturulup çalışmaya başladıktan sonra, aşağıdaki şekilde gösterildiği gibi, **Mali içgörü parametreleri** sayfasının **Tahmin modeli** bölümü modelin doğruluğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="7fbaa-137">[![Mali içgörü parametreleri sayfasında tahmin modelinin doğruluğu](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="7fbaa-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="7fbaa-138">Serbest bırakma ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="7fbaa-138">Release details</span></span>

<span data-ttu-id="7fbaa-139">Mali içgörüler genel önizleme, Amerika Birleşik Devletleri, Avrupa ve Birleşik Krallık'ta denetim dağıtımları için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="7fbaa-140">Microsoft, destek sunduğu bölge sayısını kademeli olarak artırmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="7fbaa-141">Genel önizleme özellikleri, yalnızca Katman 2 korumalı alan ortamlarında açık olabilir ve açılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="7fbaa-142">Korumalı alan ortamında oluşturulan kurulum ve AI modelleri, üretim ortamına geçirilemez.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="7fbaa-143">Daha fazla bilgi için bkz. [Microsoft Dynamics 365 Önizlemeleri için Ek Kullanım Koşulları](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span><span class="sxs-lookup"><span data-stu-id="7fbaa-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="7fbaa-144">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="7fbaa-144">Privacy notice</span></span>

<span data-ttu-id="7fbaa-145">Önizlemeler (1), Dynamics 365 Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine (SLA) dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri işlemek için kullanılmamalıdır ve (4) sınırlı desteğe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-145">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]