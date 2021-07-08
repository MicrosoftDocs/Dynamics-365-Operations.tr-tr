---
title: Lifecycle Services'dan Elektronik raporlama yapılandırmalarını karşıdan yükle
description: Bu konu, Elektronik raporlama (ER) yapılandırmalarını Microsoft Dynamics Lifecycle Services'dan (LCS) indirmeyi açıklar.
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 14f0f2b1a4d63101d432b1361379c61a70ac9345
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271195"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="ad475-103">Lifecycle Services'dan Elektronik raporlama yapılandırmalarını indirme</span><span class="sxs-lookup"><span data-stu-id="ad475-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad475-104">Bu konu, en yeni [Elektronik raporlama (ER) yapılandırmaları sürümünün](general-electronic-reporting.md#Configuration) Microsoft Dynamics Lifecycle Services'deki (LCS) [Paylaşılan varlık kitaplığı'ndan](../lifecycle-services/asset-library.md) nasıl indirileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="ad475-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad475-105">LCS'nin, ER yapılandırmaları için saklama deposu olarak kullanılma özelliği [kullanım dışı bırakılıyor](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="ad475-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="ad475-106">Daha fazla bilgi için bkz. [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) depolamasının kullanım dışı bırakılması](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="ad475-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

1. <span data-ttu-id="ad475-107">Aşağıdaki rollerden birini kullanarak uygulamada oturum açın:</span><span class="sxs-lookup"><span data-stu-id="ad475-107">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="ad475-108">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="ad475-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="ad475-109">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="ad475-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="ad475-110">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="ad475-110">System administrator</span></span>

2. <span data-ttu-id="ad475-111">**Organizasyon yönetimi** &gt; **Çalışma alanları** &gt; **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="ad475-111">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="ad475-112">**Yapılandırma sağlayıcıları** bölümünde, **Microsoft** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ad475-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="ad475-113">**Microsoft** kutucuğunda, **Depolar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad475-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="ad475-114">[![Yerelleştirme yapılandırmaları sayfasında Microsoft kutucuğu](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="ad475-114">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="ad475-115">**Yapılandırma depoları** sayfasında, kılavuz içerisinde, mevcut **LCS** türünün deposunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ad475-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="ad475-116">Bu depo kılavuzda görünmüyorsa, aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="ad475-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="ad475-117">Yeni bir depo eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ad475-117">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="ad475-118">Havuz türü olarak **LCS**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ad475-118">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="ad475-119">**Depo oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="ad475-119">Select **Create repository**.</span></span>
    4. <span data-ttu-id="ad475-120">Yetkilendirme konusunda bir bildirim geldiğinde, ekrandaki yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="ad475-120">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="ad475-121">Depo için bir ad ve açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="ad475-121">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="ad475-122">Yeni depo girişini onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ad475-122">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="ad475-123">Kılavuzda **LCS** türündeki yeni depoyu seçin.</span><span class="sxs-lookup"><span data-stu-id="ad475-123">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="ad475-124">Seçilmiş depo için ER yapılandırmalarını görüntülemek için **Aç**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad475-124">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="ad475-125">[![Yapılandırma havuzu sayfası](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="ad475-125">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="ad475-126">LCS 'de Paylaşılan varlık kitaplığı'ndan yapılandırmaları indirmek için LCS deposuna erişmede sorun yaşıyorsanız, yapılandırmaları [Global havuzdan](er-download-configurations-global-repo.md) indirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ad475-126">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="ad475-127">Sol bölmedeki yapılandırmalar ağacında, gerekli ER yapılandırmalarını seçin.</span><span class="sxs-lookup"><span data-stu-id="ad475-127">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="ad475-128">**Sürümler** FastTab üzerinde, seçili ER yapılandırmasının gerekli sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="ad475-128">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="ad475-129">Seçili sürümü LCS'den mevcut örneğe indirmek için **İçe Aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ad475-129">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ad475-130">Mevcut örnekte bulunan ER yapılandırma sürümleri için **İçe Aktar** düğmesi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="ad475-130">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="ad475-131">[![Yapılandırma havuzu sayfası](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="ad475-131">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="ad475-132">ER ayarlarına bağlı olarak yapılandırmalar içeri aktarıldıktan sonra doğrulanır.</span><span class="sxs-lookup"><span data-stu-id="ad475-132">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="ad475-133">Bulunan tutarsızlık sorunları hakkında haberdar edileceksiniz.</span><span class="sxs-lookup"><span data-stu-id="ad475-133">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="ad475-134">İçe aktarılmış yapılandırma sürümünü kullanmadan önce bu sorunları çözümlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ad475-134">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="ad475-135">Daha fazla bilgi için bu konunun ilgili konu listesine göz atın.</span><span class="sxs-lookup"><span data-stu-id="ad475-135">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad475-136">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ad475-136">Additional resources</span></span>

[<span data-ttu-id="ad475-137">Elektronik raporlamaya (ER) genel bakış</span><span class="sxs-lookup"><span data-stu-id="ad475-137">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="ad475-138">Yapılandırma hizmeti genel deposundan ER yapılandırmalarını indir</span><span class="sxs-lookup"><span data-stu-id="ad475-138">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
