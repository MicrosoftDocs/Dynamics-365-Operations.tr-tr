---
title: "Lifecycle Services'dan Elektronik raporlama yapılandırmalarını karşıdan yükle"
description: "Bu konu, Elektronik raporlama (ER) yapılandırmalarını Microsoft Dynamics Lifecycle Services'dan (LCS) indirmeyi açıklar."
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 116142ed7c1e48fa90d95b7a6f65a75568d4b0d2
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="08764-103">Lifecycle Services'dan Elektronik raporlama yapılandırmalarını karşıdan yükle</span><span class="sxs-lookup"><span data-stu-id="08764-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="08764-104">Bu konu, Elektronik raporlama (ER) yapılandırmalarını Microsoft Dynamics Lifecycle Services'dan (LCS) indirmeyi açıklar.</span><span class="sxs-lookup"><span data-stu-id="08764-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="08764-105">Bu eğitim size Elektronik Raporlama (ER) yapılandırmalarının en yeni sürümlerinin, Microsoft Dynamics Lifecycle Services'dan (LCS) indirme sürecini öğretir.</span><span class="sxs-lookup"><span data-stu-id="08764-105">This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1.  <span data-ttu-id="08764-106">Aşağıdaki rollerden birini kullanarak Finance and Operations'da oturum açın:</span><span class="sxs-lookup"><span data-stu-id="08764-106">Sign in to Finance and Operations by using one of the following roles:</span></span>
    -   <span data-ttu-id="08764-107">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="08764-107">Electronic reporting developer</span></span>
    -   <span data-ttu-id="08764-108">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="08764-108">Electronic reporting functional consultant</span></span>
    -   <span data-ttu-id="08764-109">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="08764-109">System administrator</span></span>

2.  <span data-ttu-id="08764-110">**Organizasyon yönetimi** &gt; **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="08764-110">Go to **Organization administration** &gt; **Electronic reporting**.</span></span>
3.  <span data-ttu-id="08764-111">**Yapılandırma sağlayıcıları** bölümünde, **Microsoft** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="08764-111">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4.  <span data-ttu-id="08764-112">**Microsoft** kutucuğunda, **Depolar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08764-112">On the **Microsoft** tile, click **Repositories**.</span></span> <span data-ttu-id="08764-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="08764-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>
5.  <span data-ttu-id="08764-114">**Yapılandırma depoları** sayfasında, kılavuz içerisinde, mevcut **LCS** türünün deposunu seçin.</span><span class="sxs-lookup"><span data-stu-id="08764-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="08764-115">Bu depo kılavuzda görünmüyorsa, aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="08764-115">If this repository doesn't appear in the grid, follow these steps:</span></span>
    1.  <span data-ttu-id="08764-116">Yeni bir depo eklemek için **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08764-116">Click **Add** to add a new repository.</span></span>
    2.  <span data-ttu-id="08764-117">Havuz türü olarak **LCS**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="08764-117">Select **LCS** as the repository type.</span></span>
    3.  <span data-ttu-id="08764-118">**Depo oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08764-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="08764-119">İstenirse, yetkilendirme yönergelerini izleyin.</span><span class="sxs-lookup"><span data-stu-id="08764-119">If prompted, follow the authorization instructions.</span></span>
    5.  <span data-ttu-id="08764-120">Depo için bir ad ve açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="08764-120">Enter a name and description for the repository.</span></span>
    6.  <span data-ttu-id="08764-121">Yeni depo girişini onaylamak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08764-121">Click **OK** to confirm the new repository entry.</span></span>
    7.  <span data-ttu-id="08764-122">Kılavuzda **LCS** türündeki yeni depoyu seçin.</span><span class="sxs-lookup"><span data-stu-id="08764-122">In the grid, select the new repository of the **LCS** type.</span></span>

6.  <span data-ttu-id="08764-123">Seçilmiş depo için ER yapılandırmalarını görüntülemek için **Aç**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08764-123">Click **Open** to view the list of ER configurations for the selected repository.</span></span> <span data-ttu-id="08764-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="08764-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>
7.  <span data-ttu-id="08764-125">Sol bölmedeki yapılandırmalar ağacında, gereksinim duyduğunuz ER yapılandırmalarını seçin.</span><span class="sxs-lookup"><span data-stu-id="08764-125">In the configurations tree in the left pane, select the ER configuration that you require.</span></span>
8.  <span data-ttu-id="08764-126">**Sürümler** FastTab üzerinde, seçili ER yapılandırmasının gerekli sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="08764-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9.  <span data-ttu-id="08764-127">Seçili sürümü LCS'den mevcut Finance and Operations örneğine indirmek için **İçe Aktarma**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08764-127">Click **Import** to download the selected version from LCS to the current Finance and Operations instance.</span></span> <span data-ttu-id="08764-128">**Not:** Mevcut Finance and Operations örneğinde bulunan ER yapılandırma sürümleri için **İçe Aktarma** düğmesi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="08764-128">**Note:** The **Import** button is unavailable for ER configuration versions that are already present in the current Finance and Operations instance.</span></span> <span data-ttu-id="08764-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="08764-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

<span data-ttu-id="08764-130">**Not:** ER ayarlarına bağlı olarak, yapılandırmalar içe aktarıldıktan sonra doğrulanır.</span><span class="sxs-lookup"><span data-stu-id="08764-130">**Note:** Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="08764-131">Bulunan tutarsızlık sorunları hakkında haberdar edileceksiniz.</span><span class="sxs-lookup"><span data-stu-id="08764-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="08764-132">İçe aktarılmış yapılandırma sürümünü kullanmadan önce bu sorunları çözümlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="08764-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="08764-133">Daha fazla bilgi için bu konunun ilgili makaleleri listesine göz atın.</span><span class="sxs-lookup"><span data-stu-id="08764-133">For more information, see the list of related articles for this topic.</span></span>

<a name="see-also"></a><span data-ttu-id="08764-134">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="08764-134">See also</span></span>
--------

[<span data-ttu-id="08764-135">Elektronik raporlamaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="08764-135">Electronic reporting overview</span></span>](general-electronic-reporting.md)




