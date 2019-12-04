---
title: Lifecycle Services'dan Elektronik raporlama yapılandırmalarını karşıdan yükle
description: Bu konu, Elektronik raporlama (ER) yapılandırmalarını Microsoft Dynamics Lifecycle Services'dan (LCS) indirmeyi açıklar.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 49785835ee2da911d7b8d1360e1c42f850f1153f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771505"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="38198-103">Lifecycle Services'dan Elektronik raporlama yapılandırmalarını indirme</span><span class="sxs-lookup"><span data-stu-id="38198-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38198-104">Bu konu, Elektronik raporlama (ER) yapılandırmalarını Microsoft Dynamics Lifecycle Services'dan (LCS) indirmeyi açıklar.</span><span class="sxs-lookup"><span data-stu-id="38198-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="38198-105">Bu eğitim size Elektronik Raporlama (ER) yapılandırmalarının en yeni sürümlerinin, Microsoft Dynamics Lifecycle Services'dan (LCS) indirme sürecini öğretir.</span><span class="sxs-lookup"><span data-stu-id="38198-105">This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="38198-106">Aşağıdaki rollerden birini kullanarak uygulamada oturum açın:</span><span class="sxs-lookup"><span data-stu-id="38198-106">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="38198-107">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="38198-107">Electronic reporting developer</span></span>
    - <span data-ttu-id="38198-108">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="38198-108">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="38198-109">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="38198-109">System administrator</span></span>

2. <span data-ttu-id="38198-110">**Organizasyon yönetimi** &gt; **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="38198-110">Go to **Organization administration** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="38198-111">**Yapılandırma sağlayıcıları** bölümünde, **Microsoft** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="38198-111">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="38198-112">**Microsoft** kutucuğunda, **Depolar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="38198-112">On the **Microsoft** tile, click **Repositories**.</span></span>

    <span data-ttu-id="38198-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="38198-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="38198-114">**Yapılandırma depoları** sayfasında, kılavuz içerisinde, mevcut **LCS** türünün deposunu seçin.</span><span class="sxs-lookup"><span data-stu-id="38198-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="38198-115">Bu depo kılavuzda görünmüyorsa, aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="38198-115">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="38198-116">Yeni bir depo eklemek için **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="38198-116">Click **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="38198-117">Havuz türü olarak **LCS**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="38198-117">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="38198-118">**Depo oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="38198-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="38198-119">İstenirse, yetkilendirme yönergelerini izleyin.</span><span class="sxs-lookup"><span data-stu-id="38198-119">If prompted, follow the authorization instructions.</span></span>
    5. <span data-ttu-id="38198-120">Depo için bir ad ve açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="38198-120">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="38198-121">Yeni depo girişini onaylamak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="38198-121">Click **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="38198-122">Kılavuzda **LCS** türündeki yeni depoyu seçin.</span><span class="sxs-lookup"><span data-stu-id="38198-122">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="38198-123">Seçilmiş depo için ER yapılandırmalarını görüntülemek için **Aç**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="38198-123">Click **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="38198-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="38198-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

7. <span data-ttu-id="38198-125">Sol bölmedeki yapılandırmalar ağacında, gereksinim duyduğunuz ER yapılandırmalarını seçin.</span><span class="sxs-lookup"><span data-stu-id="38198-125">In the configurations tree in the left pane, select the ER configuration that you require.</span></span>
8. <span data-ttu-id="38198-126">**Sürümler** FastTab üzerinde, seçili ER yapılandırmasının gerekli sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="38198-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="38198-127">Seçili sürümü LCS'den mevcut örneğe indirmek için **İçe Aktar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="38198-127">Click **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="38198-128">Mevcut örnekte bulunan ER yapılandırma sürümleri için **İçe Aktar** düğmesi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="38198-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="38198-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="38198-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="38198-130">ER ayarlarına bağlı olarak yapılandırmalar içeri aktarıldıktan sonra doğrulanır.</span><span class="sxs-lookup"><span data-stu-id="38198-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="38198-131">Bulunan tutarsızlık sorunları hakkında haberdar edileceksiniz.</span><span class="sxs-lookup"><span data-stu-id="38198-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="38198-132">İçe aktarılmış yapılandırma sürümünü kullanmadan önce bu sorunları çözümlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="38198-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="38198-133">Daha fazla bilgi için bu konunun ilgili makaleleri listesine göz atın.</span><span class="sxs-lookup"><span data-stu-id="38198-133">For more information, see the list of related articles for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="38198-134">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="38198-134">Additional resources</span></span>

[<span data-ttu-id="38198-135">Elektronik raporlamaya (ER) genel bakış</span><span class="sxs-lookup"><span data-stu-id="38198-135">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
