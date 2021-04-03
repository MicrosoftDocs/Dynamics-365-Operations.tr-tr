---
title: ER konfigürasyonlarının güncelleştirilmiş sürümlerini içe aktar
description: Bu konu, genel amaçlı yapılandırma havuzundan elektronik raporlama (ER) yapılandırmalarının güncel sürümlerinin nasıl içe aktarılacağı açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 0c65315c4fa6a42b4bbb0d008b58f8df9cc0ea3d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561890"
---
# <a name="import-updated-versions-of-er-configurations"></a><span data-ttu-id="06709-103">ER konfigürasyonlarının güncelleştirilmiş sürümlerini içe aktar</span><span class="sxs-lookup"><span data-stu-id="06709-103">Import updated versions of ER configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06709-104">Elektronik raporlama (ER) [depoları](general-electronic-reporting.md#Repository), [ER konfigürasyonları](general-electronic-reporting.md#Configuration) paylaşmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="06709-104">Electronic reporting (ER) [repositories](general-electronic-reporting.md#Repository) are used to share [ER configurations](general-electronic-reporting.md#Configuration).</span></span> <span data-ttu-id="06709-105">Farklı depolardaki ER yapılandırmalarını Microsoft Dynamics 365 Finance örneğiniz için [içe aktarabilirsiniz](download-electronic-reporting-configuration-lcs.md) .</span><span class="sxs-lookup"><span data-stu-id="06709-105">You can [import](download-electronic-reporting-configuration-lcs.md) ER configurations from different repositories into your instance of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="06709-106">ER yapılandırmalarını içe aktardığınızda, [Konfigürasyon sağlayıcıları](general-electronic-reporting.md#Provider)paylaşılabilecek şekilde yeni [sürümler](general-electronic-reporting.md#component-versioning) depoları yayımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="06709-106">When you import ER configurations, [configuration providers](general-electronic-reporting.md#Provider) can publish new [versions](general-electronic-reporting.md#component-versioning) repositories so that they can be shared.</span></span>

<span data-ttu-id="06709-107">Bu konu, genel amaçlı yapılandırma havuzundan ER yapılandırmalarının güncel sürümlerinin nasıl içe aktarılacağı açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="06709-107">This topic explains how to import updated versions of ER configurations from the Global repository of the Configuration service.</span></span> <span data-ttu-id="06709-108">Daha fazla bilgi için, bkz [Microsoft Dynamics 365 for Finance and Operations - Regulatory services yapılandırma hizmeti](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="06709-108">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="review-the-available-updated-versions"></a><span data-ttu-id="06709-109">Kullanılabilir güncelleştirilmiş sürümleri gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="06709-109">Review the available updated versions</span></span>

1. <span data-ttu-id="06709-110">Aşağıdaki rollerden birini kullanarak Finance'de oturum açın:</span><span class="sxs-lookup"><span data-stu-id="06709-110">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="06709-111">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="06709-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="06709-112">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="06709-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="06709-113">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="06709-113">System administrator</span></span>

2. <span data-ttu-id="06709-114">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="06709-114">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="06709-115">**Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Yapılandırma sürümleri güncellemelerini içe aktarma** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="06709-115">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>

    ![Yerelleştirme yapılandırmaları sayfası](./media/er-download-updated-versions-global-repo1.png)

4. <span data-ttu-id="06709-117">**Elektronik raporlama konfigürasyonları sürümleri güncelleştirmelerini içe aktar** iletişim kutusunda, **çalıştırma modu** alanında **yalnızca kullanılabilir güncelleştirmeleri göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="06709-117">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Only show available updates**.</span></span> <span data-ttu-id="06709-118">Daha sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="06709-118">Then select **OK**.</span></span> 

    ![Çalışma modu alanı yalnızca kullanılabilir güncelleştirmeleri gösterecek şekilde ayarlandı](./media/er-download-updated-versions-global-repo2.png)

5. <span data-ttu-id="06709-120">Aldığınız iletileri gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="06709-120">Review the messages that you receive.</span></span> <span data-ttu-id="06709-121">Bu iletiler, geçerli Finance örneğindeki ER konfigürasyonlarla ilgili aşağıdaki bilgileri ve bunların genel havuz içeriğiyle nasıl karşılaştırılacağını sağlar:</span><span class="sxs-lookup"><span data-stu-id="06709-121">These messages provide the following information about the ER configurations in the current Finance instance and how they compare to the content of the Global repository:</span></span>

    - <span data-ttu-id="06709-122">ER konfigürasyonların toplam sayısı</span><span class="sxs-lookup"><span data-stu-id="06709-122">The total number of ER configurations</span></span>
    - <span data-ttu-id="06709-123">Genel havuzda bulunmayan yapılandırmalar</span><span class="sxs-lookup"><span data-stu-id="06709-123">ER configurations that aren't present in the Global repository</span></span>
    - <span data-ttu-id="06709-124">Geçerli finans örneğinde en son sürümün zaten kullanılabildiği yapılandırmalar (Bu konfigürasyonların tam listesini görüntülemek Için **Mesaj ayrıntıları** bağlantısını seçin.)</span><span class="sxs-lookup"><span data-stu-id="06709-124">ER configurations for which the latest version is already available in the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        !["Aşağıdaki yapılandırmaların en son sürümleri zaten alındı" ileti ve ileti ayrıntıları](./media/er-download-updated-versions-global-repo3.png)

    - <span data-ttu-id="06709-126">Genel depoda kullanılabilir ve geçerli Finans örneğine en son sürümün zaten kullanılabildiği yapılandırmalar (Bu konfigürasyonların tam listesini görüntülemek Için **Mesaj ayrıntıları** bağlantısını seçin.)</span><span class="sxs-lookup"><span data-stu-id="06709-126">ER configurations for which the latest version is available in the Global repository and can be imported into the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        !["Kullanılabilir güncelleştirmeler" iletisi ve ileti ayrıntıları](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a><span data-ttu-id="06709-128">Kullanılabilir güncelleştirilmiş sürümleri içe aktarın</span><span class="sxs-lookup"><span data-stu-id="06709-128">Import available updated versions</span></span>

1. <span data-ttu-id="06709-129">Aşağıdaki rollerden birini kullanarak Finance'de oturum açın:</span><span class="sxs-lookup"><span data-stu-id="06709-129">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="06709-130">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="06709-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="06709-131">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="06709-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="06709-132">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="06709-132">System administrator</span></span>

2. <span data-ttu-id="06709-133">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="06709-133">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="06709-134">**Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Yapılandırma sürümleri güncellemelerini içe aktarma** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="06709-134">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>
4. <span data-ttu-id="06709-135">**Elektronik raporlama konfigürasyonları sürümleri güncelleştirmelerini içe aktar** iletişim kutusunda, **çalıştırma modu** alanında, Global depodan geçerli finans örneğine ER konfigürasyonların en son sürümlerini içe aktarmak için, **en son güncelleştirmeleri içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="06709-135">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Import latest updates** to import the latest versions of ER configurations from the Global repository into the current Finance instance.</span></span>
5. <span data-ttu-id="06709-136">İçe aktarma için bir toplu iş planlamak üzere, **Arka planda çalıştır** hızlı sekmesinde, **Toplu işleme** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="06709-136">To schedule a batch job for the import, on the **Run in the background** FastTab, set the **Batch processing** option to **Yes**.</span></span> <span data-ttu-id="06709-137">İçe aktarmayı belirli aralıklarla tekrarlamak istiyorsanız, gerekli yinelemeyi konfigüre edin.</span><span class="sxs-lookup"><span data-stu-id="06709-137">If you want to repeat the import periodically, configure the required recurrence.</span></span>

    ![En son güncelleştirmeleri Içe aktarmak için çalışma modu alanı ayarla](./media/er-download-updated-versions-global-repo5.png)

6. <span data-ttu-id="06709-139">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="06709-139">Select **OK**.</span></span>
7. <span data-ttu-id="06709-140">Hangi konfigürasyon sürümlerinin içe aktarıldığını öğrenmek için aşağıdaki adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="06709-140">To learn what configuration versions have been imported, follow one of these steps:</span></span>

    - <span data-ttu-id="06709-141">Toplu işi kullanmak yerine, içe aktarmayı etkileşimli olarak çalıştırırsanız, aldığınız iletileri gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="06709-141">If you run the import interactively instead of using a batch job, review the messages that you receive.</span></span>

        ![Etkileşimli içe aktarma çalıştırması sırasında alınan iletiler](./media/er-download-updated-versions-global-repo6.png)

    - <span data-ttu-id="06709-143">İçe aktarmayı toplu iş modunda çalıştırırsanız, şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="06709-143">If you run the import in batch mode, follow these steps:</span></span>

        1. <span data-ttu-id="06709-144">**Ortak** \> **Sorgular** \> **Toplu işler** \> **Toplu işlerim**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="06709-144">Go to **Common** \> **Inquiries** \> **Batch jobs** \> **My batch jobs**.</span></span>
        2. <span data-ttu-id="06709-145">**Elektronik raporlama konfigürasyonları güncelleştirmeleri güncelleştirmelerini içe aktar** işini bulun ve seçin ve sonra eylem bölmesinde, **toplu iş** sekmesinde, iş geçmişini görüntülemek için **toplu iş geçmişi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="06709-145">Find and select the **Import electronic reporting configurations versions updates** job, and then, on the Action Pane, on the **Batch job** tab, select **Batch job history** to view the job history.</span></span>
        3. <span data-ttu-id="06709-146">**Toplu iş geçmişi** sayfasında, **Günlük**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="06709-146">On the **Batch job history** page, select **Log**.</span></span> <span data-ttu-id="06709-147">Sonra, aldığınız iletide, iş günlüğünü görüntülemek için **Mesaj ayrıntıları** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="06709-147">Then, in the message that you receive, select the **Message details** link to view the job log.</span></span>

        ![İş günlükleri](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> <span data-ttu-id="06709-149">İçe aktarılan versiyonlar hemen kullanılabilir olacağından, ER konfigürasyonlarının güncelleştirilmiş sürümlerini doğrudan Global depodan üretim ortamına içe aktarmak için bir yinelenen toplu iş zamanlamanızı önermiyoruz.</span><span class="sxs-lookup"><span data-stu-id="06709-149">We don't recommend that you schedule a recurring batch job to import updated versions of ER configurations directly from the Global repository into a production environment, because the imported versions will immediately be available for use.</span></span> <span data-ttu-id="06709-150">Bunun yerine, ER konfigürasyonlarının sürümlerini bir korumalı alan ortamına dağıtmak için bu yaklaşımı kullanın.</span><span class="sxs-lookup"><span data-stu-id="06709-150">Instead, use this approach to deploy versions of ER configurations to a sandbox environment.</span></span> <span data-ttu-id="06709-151">Bunlar, daha sonra üretim ortamına dağıtılmadan önce korumalı alan ortamında değerlendirilebilirler.</span><span class="sxs-lookup"><span data-stu-id="06709-151">They can then be evaluated in the sandbox environment before they are deployed to a production environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06709-152">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="06709-152">Additional resources</span></span>

- [<span data-ttu-id="06709-153">Elektronik raporlamaya (ER) genel bakış</span><span class="sxs-lookup"><span data-stu-id="06709-153">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="06709-154">Yapılandırma hizmeti genel deposundan ER yapılandırmalarını indir</span><span class="sxs-lookup"><span data-stu-id="06709-154">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]