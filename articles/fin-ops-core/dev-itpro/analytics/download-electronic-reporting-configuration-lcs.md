---
title: Lifecycle Services'dan Elektronik raporlama yapılandırmalarını karşıdan yükle
description: Bu konu, Elektronik raporlama (ER) yapılandırmalarını Microsoft Dynamics Lifecycle Services'dan (LCS) indirmeyi açıklar.
author: NickSelin
manager: AnnBe
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
ms.openlocfilehash: 8aaa3be426c0321da7e72d6acc18918d8b0ecee2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570382"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="036c0-103">Lifecycle Services'dan Elektronik raporlama yapılandırmalarını indirme</span><span class="sxs-lookup"><span data-stu-id="036c0-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="036c0-104">Bu konu, en yeni [Elektronik raporlama (ER) yapılandırmaları sürümünün](general-electronic-reporting.md#Configuration) Microsoft Dynamics Lifecycle Services'deki (LCS) [Paylaşılan varlık kitaplığı'ndan](../lifecycle-services/asset-library.md) nasıl indirileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="036c0-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="036c0-105">Aşağıdaki rollerden birini kullanarak uygulamada oturum açın:</span><span class="sxs-lookup"><span data-stu-id="036c0-105">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="036c0-106">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="036c0-106">Electronic reporting developer</span></span>
    - <span data-ttu-id="036c0-107">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="036c0-107">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="036c0-108">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="036c0-108">System administrator</span></span>

2. <span data-ttu-id="036c0-109">**Organizasyon yönetimi** &gt; **Çalışma alanları** &gt; **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="036c0-109">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="036c0-110">**Yapılandırma sağlayıcıları** bölümünde, **Microsoft** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="036c0-110">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="036c0-111">**Microsoft** kutucuğunda, **Depolar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="036c0-111">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="036c0-112">[![Yerelleştirme yapılandırmaları sayfasında Microsoft kutucuğu](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="036c0-112">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="036c0-113">**Yapılandırma depoları** sayfasında, kılavuz içerisinde, mevcut **LCS** türünün deposunu seçin.</span><span class="sxs-lookup"><span data-stu-id="036c0-113">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="036c0-114">Bu depo kılavuzda görünmüyorsa, aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="036c0-114">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="036c0-115">Yeni bir depo eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="036c0-115">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="036c0-116">Havuz türü olarak **LCS**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="036c0-116">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="036c0-117">**Depo oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="036c0-117">Select **Create repository**.</span></span>
    4. <span data-ttu-id="036c0-118">Yetkilendirme konusunda bir bildirim geldiğinde, ekrandaki yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="036c0-118">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="036c0-119">Depo için bir ad ve açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="036c0-119">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="036c0-120">Yeni depo girişini onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="036c0-120">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="036c0-121">Kılavuzda **LCS** türündeki yeni depoyu seçin.</span><span class="sxs-lookup"><span data-stu-id="036c0-121">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="036c0-122">Seçilmiş depo için ER yapılandırmalarını görüntülemek için **Aç**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="036c0-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="036c0-123">[![Yapılandırma havuzu sayfası](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="036c0-123">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="036c0-124">LCS 'de Paylaşılan varlık kitaplığı'ndan yapılandırmaları indirmek için LCS deposuna erişmede sorun yaşıyorsanız, yapılandırmaları [Global havuzdan](er-download-configurations-global-repo.md) indirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="036c0-124">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="036c0-125">Sol bölmedeki yapılandırmalar ağacında, gerekli ER yapılandırmalarını seçin.</span><span class="sxs-lookup"><span data-stu-id="036c0-125">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="036c0-126">**Sürümler** FastTab üzerinde, seçili ER yapılandırmasının gerekli sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="036c0-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="036c0-127">Seçili sürümü LCS'den mevcut örneğe indirmek için **İçe Aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="036c0-127">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="036c0-128">Mevcut örnekte bulunan ER yapılandırma sürümleri için **İçe Aktar** düğmesi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="036c0-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="036c0-129">[![Yapılandırma havuzu sayfası](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="036c0-129">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="036c0-130">ER ayarlarına bağlı olarak yapılandırmalar içeri aktarıldıktan sonra doğrulanır.</span><span class="sxs-lookup"><span data-stu-id="036c0-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="036c0-131">Bulunan tutarsızlık sorunları hakkında haberdar edileceksiniz.</span><span class="sxs-lookup"><span data-stu-id="036c0-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="036c0-132">İçe aktarılmış yapılandırma sürümünü kullanmadan önce bu sorunları çözümlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="036c0-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="036c0-133">Daha fazla bilgi için bu konunun ilgili konu listesine göz atın.</span><span class="sxs-lookup"><span data-stu-id="036c0-133">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="036c0-134">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="036c0-134">Additional resources</span></span>

[<span data-ttu-id="036c0-135">Elektronik raporlamaya (ER) genel bakış</span><span class="sxs-lookup"><span data-stu-id="036c0-135">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="036c0-136">Yapılandırma hizmeti genel deposundan ER yapılandırmalarını indir</span><span class="sxs-lookup"><span data-stu-id="036c0-136">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]