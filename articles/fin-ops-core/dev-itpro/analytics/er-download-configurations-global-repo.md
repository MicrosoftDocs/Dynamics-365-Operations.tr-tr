---
title: Yapılandırma hizmeti genel deposundan ER yapılandırmalarını indir
description: Bu konu, genel amaçlı yapılandırma havuzundan elektronik raporlama (ER) yapılandırmalarının nasıl indirileceğini açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ed31cdee74c9db26ba76ed263b5e0578cd04bc3d
ms.sourcegitcommit: 7816902b59aa61d9183d54b50a86e282661e3971
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/02/2020
ms.locfileid: "3421714"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a><span data-ttu-id="b124a-103">Yapılandırma hizmeti genel deposundan ER yapılandırmalarını indir</span><span class="sxs-lookup"><span data-stu-id="b124a-103">Download ER configurations from the Global repository of Configuration service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b124a-104">Bu konu, genel amaçlı yapılandırma havuzundan [elektronik raporlama (ER) yapılandırmalarının](general-electronic-reporting.md#Configuration) nasıl indirileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="b124a-104">This topic explains how to download [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the Global repository of configuration service.</span></span> <span data-ttu-id="b124a-105">Daha fazla bilgi için, bkz [Microsoft Dynamics 365 for Finance and Operations - Regulatory services yapılandırma hizmeti](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="b124a-105">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="open-configurations-repository"></a><span data-ttu-id="b124a-106">Yapılandırmaların havuzu açın</span><span class="sxs-lookup"><span data-stu-id="b124a-106">Open configurations repository</span></span>

1. <span data-ttu-id="b124a-107">Aşağıdaki rollerden birini kullanarak Dynamics 365 Finance uygulamada oturum açın:</span><span class="sxs-lookup"><span data-stu-id="b124a-107">Sign in to the Dynamics 365 Finance application using one of the following roles:</span></span>

    - <span data-ttu-id="b124a-108">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="b124a-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="b124a-109">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="b124a-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="b124a-110">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="b124a-110">System administrator</span></span>

2. <span data-ttu-id="b124a-111">**Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="b124a-111">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="b124a-112">**Yapılandırma sağlayıcıları** bölümünde, **Microsoft** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="b124a-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
3. <span data-ttu-id="b124a-113">**Microsoft** kutucuğunda, **Depolar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b124a-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    ![Elektronik raporlama çalışma alanı](./media/er-download-configurations-global-repo-er-workspace.png)

4. <span data-ttu-id="b124a-115">**Yapılandırma depoları** sayfasında, kılavuz içerisinde, mevcut **Genel** türünün deposunu seçin.</span><span class="sxs-lookup"><span data-stu-id="b124a-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **Global** type.</span></span> <span data-ttu-id="b124a-116">Bu depo kılavuzda görünmüyorsa, aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="b124a-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="b124a-117">Yeni bir depo eklemek için **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b124a-117">Select **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="b124a-118">Havuz türü olarak **Global** 'i seçin ve sonra **Havuz oluştur** 'u seçin .</span><span class="sxs-lookup"><span data-stu-id="b124a-118">Select **Global** as the repository type, and then select **Create repository**.</span></span>
    3. <span data-ttu-id="b124a-119">İstenirse, yetkilendirme yönergelerini izleyin.</span><span class="sxs-lookup"><span data-stu-id="b124a-119">If prompted, follow the authorization instructions.</span></span>
    4. <span data-ttu-id="b124a-120">Havuz için bir ad ve açıklama girin ve sonra yeni havuz girişini onaylamak için **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b124a-120">Enter a name and description for the repository and then select **OK** to confirm the new repository entry.</span></span>
    5. <span data-ttu-id="b124a-121">Kılavuzda **Global** türündeki yeni depoyu seçin.</span><span class="sxs-lookup"><span data-stu-id="b124a-121">In the grid, select the new repository of the **Global** type.</span></span>

5. <span data-ttu-id="b124a-122">Seçilmiş depo için ER yapılandırmalarını görüntülemek için **Aç**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b124a-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    ![Yapılandırma havuzu sayfası](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a><span data-ttu-id="b124a-124">Tekli yapılandırmasını içe aktarma</span><span class="sxs-lookup"><span data-stu-id="b124a-124">Import a single configuration</span></span>

1. <span data-ttu-id="b124a-125">**Konfigürasyon depoları** sayfasında, yapılandırmalar ağacında, istediğiniz er yapılandırmasını seçin.</span><span class="sxs-lookup"><span data-stu-id="b124a-125">On the **Configuration repositories** page, in the configurations tree, select the ER configuration that you want.</span></span>
2. <span data-ttu-id="b124a-126">**Sürümler** FastTab üzerinde, seçili ER yapılandırmasının gerekli sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="b124a-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
3. <span data-ttu-id="b124a-127">Seçili sürümü Global depo'dan mevcut Finance örneğine indirmek için **İçe Aktarma**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b124a-127">Select **Import** to download the selected version from Global repository to the current Finance instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b124a-128">Mevcut Finance örnekte bulunan ER yapılandırma sürümleri için **İçe Aktar** düğmesi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="b124a-128">The **Import** button is unavailable for ER configuration versions that are already present in the current Finance instance.</span></span>

    ![Yapılandırma havuzu sayfası](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a><span data-ttu-id="b124a-130">Filtreli yapılandırmasını içe aktarma</span><span class="sxs-lookup"><span data-stu-id="b124a-130">Import filtered configurations</span></span>

1. <span data-ttu-id="b124a-131">**Konfigürasyon depoları** sayfasında, yapılandırmalar ağacında, **Filtre** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="b124a-131">On the **Configuration repositories** page, in the configurations tree, expand the **Filter** FastTab.</span></span>
2. <span data-ttu-id="b124a-132">**Etiketler** kılavuzunda, gerekli tüm etiketleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b124a-132">In the **Tags** grid, add any tags that are needed.</span></span>
3. <span data-ttu-id="b124a-133">**Ülke/bölge uygulanabilirlik** alanında, ilgili ülke/bölge kodlarını seçin ve **Filtre Uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b124a-133">In the **Country/region applicability** field, select the appropriate country/region codes, and then select  **Apply filter**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b124a-134">**Konfigürasyonlar** Hızlı sekmesi, belirtilen seçim koşullarını karşılayan tüm konfigürasyonları gösterir.</span><span class="sxs-lookup"><span data-stu-id="b124a-134">The **Configurations** FastTab shows all the configurations that satisfy the specified selection conditions.</span></span>

4. <span data-ttu-id="b124a-135">Filtre uygulanan konfigürasyonları Global depodan geçerli örneğe indirmek için **konfigürasyonlar** hızlı sekmesinde **içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b124a-135">On the **Configurations** FastTab, select **Import** to download the filtered configurations from the Global repository to the current instance.</span></span>
5. <span data-ttu-id="b124a-136">**Konfigürasyonlar** hızlı sekmesinde, belirtilen seçim koşullarını temizlemek için **filtreyi Sıfırla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b124a-136">On the **Configurations** FastTab, select **Reset filter** to clean up the specified selection conditions.</span></span>

    ![Yapılandırma havuzu sayfası](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> <span data-ttu-id="b124a-138">ER ayarlarına bağlı olarak yapılandırmalar içeri aktarıldıktan sonra doğrulanır.</span><span class="sxs-lookup"><span data-stu-id="b124a-138">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="b124a-139">Bulunan tutarsızlık sorunları hakkında haberdar edileceksiniz.</span><span class="sxs-lookup"><span data-stu-id="b124a-139">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="b124a-140">İçe aktarılmış yapılandırma sürümünü kullanmadan önce bu sorunları çözümlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b124a-140">Before you can use the imported configuration version, you must resolve the issues.</span></span> <span data-ttu-id="b124a-141">Daha fazla bilgi için bu konunun ilgili kaynaklar listesine göz atın.</span><span class="sxs-lookup"><span data-stu-id="b124a-141">For more information, see the list of related resources for this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="b124a-142">ER konfigürasyonları diğer konfigürasyonlara bağlı olarak konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="b124a-142">ER configurations can be configured as being dependent on other configurations.</span></span> <span data-ttu-id="b124a-143">Bu nedenle, seçili konfigürasyonla birlikte, diğer yapılandırmalar otomatik olarak içe aktarılabilir.</span><span class="sxs-lookup"><span data-stu-id="b124a-143">Therefore, along with a selected configuration, other configurations might be automatically imported.</span></span> <span data-ttu-id="b124a-144">Konfigürasyon bağımlılıkları hakkında daha fazla bilgi için, [diğer bileşenlerde ER yapılandırmalarının bağımlılığını tanımlama konusuna](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md) bakın.</span><span class="sxs-lookup"><span data-stu-id="b124a-144">For more about configuration dependencies, see [Define the dependency of ER configurations on other components](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b124a-145">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b124a-145">Additional resources</span></span>

[<span data-ttu-id="b124a-146">Elektronik raporlamaya (ER) genel bakış</span><span class="sxs-lookup"><span data-stu-id="b124a-146">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
