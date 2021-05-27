---
title: Microsoft Teams'de önceden var olan ekipler varsa mağazaları ve ekipleri eşleme
description: Bu konu, kuruluşunuz Commerce tümleştirmesinden önce Microsoft Teams'de oluşturulan ekiplere sahipse Dynamics 365 Commerce Headquarters'da mağazaların ve ilgili ekiplerin nasıl eşlendiğini açıklar.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ccc2cbf11e405facf310d93e5458cfe12a43146d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020231"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a><span data-ttu-id="05bfb-103">Microsoft Teams'de önceden var olan ekipler varsa mağazaları ve ekipleri eşleme</span><span class="sxs-lookup"><span data-stu-id="05bfb-103">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="05bfb-104">Bu konu, kuruluşunuz Commerce tümleştirmesinden önce Microsoft Teams'de oluşturulan ekiplere sahipse Dynamics 365 Commerce Headquarters'da mağazaların ve ilgili ekiplerin nasıl eşlendiğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="05bfb-104">This topic covers how to map stores and corresponding teams in Dynamics 365 Commerce headquarters if your organization has already created teams in Microsoft Teams before Commerce integration.</span></span>

<span data-ttu-id="05bfb-105">Kuruluşunuz Dynamics 365 Commerce ve Microsoft Teams'i tümleştirmeden önce mağazalarınızın bir kısmı veya tümü için oluşturulmuş ekiplere sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="05bfb-105">Your organization may have teams created for some or all of your stores before integrating Dynamics 365 Commerce and Microsoft Teams.</span></span> <span data-ttu-id="05bfb-106">Bu durumda, Commerce POS ve Microsoft Teams arasında görev eşitlemesi oluşturmak için mağazaların ve ilgili ekibin Commerce Headquarters'da eşlemesini sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="05bfb-106">If this is the case, to establish task synchronization between Commerce POS and Microsoft Teams you must provide the mapping of stores and corresponding team in Commerce headquarters.</span></span>

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a><span data-ttu-id="05bfb-107">Commerce Headquarters'da mağazaları ve ilgili ekipleri eşleme</span><span class="sxs-lookup"><span data-stu-id="05bfb-107">Map stores and corresponding teams in Commerce headquarters</span></span> 

<span data-ttu-id="05bfb-108">Commerce Headquarters'da mağazaları ve ilgili ekipleri eşlemek için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="05bfb-108">To map stores and corresponding teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="05bfb-109">**Sistem Yönetimi \> Çalışma alanı \> Veri yönetimi** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-109">Go to **System Administration \> Workspace \> Data management**.</span></span>
1. <span data-ttu-id="05bfb-110">**Dışa Aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-110">Select **Export**.</span></span> 
1. <span data-ttu-id="05bfb-111">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-111">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="05bfb-112">**Grup adı** altında "Teams eşlemesini dışa aktarma"'yı girin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-112">Under **Group name**, enter "Export Teams mapping".</span></span>
1. <span data-ttu-id="05bfb-113">**Seçili varlıklar** hızlı sekmesinde **Varlık ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-113">On the **Selected entities** FastTab, select **Add entity**.</span></span> <span data-ttu-id="05bfb-114">**Varlık Ekle** iletişim kutusu görünür.</span><span class="sxs-lookup"><span data-stu-id="05bfb-114">The **Add entity** dialog box appears.</span></span>  
1. <span data-ttu-id="05bfb-115">**Varlık adı** açılan listesinde, **kaynak ve ekip arasında Teams eşlemesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-115">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="05bfb-116">**Hedef veri biçimi** açılan listesinde **CSV**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-116">In the **Target data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="05bfb-117">**Ekle**'yi ve ardından **Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-117">Select **Add**, and then select **Close**.</span></span>
1. <span data-ttu-id="05bfb-118">Eylem bölmesinin sol üstünde, **Şimdi dışa aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-118">On the top left under the Action Pane, select **Export now**.</span></span>
1. <span data-ttu-id="05bfb-119">**Varlık işleme durumu** altında, **dosyayı indir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-119">Under **Entity processing status**, select **Download file**.</span></span>
1. <span data-ttu-id="05bfb-120">Dışa aktarılan CSV dosyasında, **SOURCETYPE**, **SourceId** ve **TEAMID** değerlerini aşağıdaki gibi girin:</span><span class="sxs-lookup"><span data-stu-id="05bfb-120">In the exported CSV file, enter values for **SOURCETYPE**, **SOURCEID**, and **TEAMID** as follows:</span></span>
    - <span data-ttu-id="05bfb-121">**SOURCETYPE** için "RetailStore" girin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-121">For **SOURCETYPE**, enter "RetailStore".</span></span> 
    - <span data-ttu-id="05bfb-122">**SOURCEID** olarak, mağaza numarasını girin (örneğin, San Francisco mağazası için "000135").</span><span class="sxs-lookup"><span data-stu-id="05bfb-122">For **SOURCEID**, enter the store number (for example, "000135" for the San Francisco store).</span></span> <span data-ttu-id="05bfb-123">Mağaza numaralarını **Retail ve Commerce \> kanallar \> Mağazalar**'da bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="05bfb-123">You can find store numbers at **Retail and Commerce \> Channels \> Stores**.</span></span>
    - <span data-ttu-id="05bfb-124">**TEAMID** için, Microsoft Teams'den ilgili ekip kodunu (örneğin, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c") girin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-124">For **TEAMID**, enter the corresponding team ID from Microsoft Teams (for example, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span></span> <span data-ttu-id="05bfb-125">Ekip kodu bilgilerini [admin.teams.microsoft.com](https://admin.teams.microsoft.com) adresinden bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="05bfb-125">You can find team ID information at [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span></span>
1. <span data-ttu-id="05bfb-126">CSV dosyasını yerel makinenize kaydedin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-126">Save the CSV file to your local machine.</span></span>
1. <span data-ttu-id="05bfb-127">**Sistem Yönetimi \> Çalışma alanı \> Veri yönetimi** seçeneğine gidin ve **İçe Aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-127">Go to **System Administration \> Workspace \> Data management**, and then select **Import**.</span></span>
1. <span data-ttu-id="05bfb-128">**Seçili varlıklar** hızlı sekmesinde **Dosya ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-128">On the **Selected entities** FastTab, select **Add file**.</span></span> <span data-ttu-id="05bfb-129">**Dosya Ekle** iletişim kutusu görünür.</span><span class="sxs-lookup"><span data-stu-id="05bfb-129">The **Add file** dialog box appears.</span></span>
1. <span data-ttu-id="05bfb-130">**Varlık adı** açılan listesinde, **kaynak ve ekip arasında Teams eşlemesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-130">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="05bfb-131">**Kaynak veri biçimi** açılan listesinde **CSV**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-131">In the **Source data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="05bfb-132">**Yükle ve Ekle**'yi seçin, daha önce kaydetmiş olduğunuz CSV dosyasını seçin ve **aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-132">Select **Upload and add**, select the CSV file that you saved previously, and then select **Open**.</span></span>
1. <span data-ttu-id="05bfb-133">**Dosya Ekle** iletişim kutusunda **Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-133">In the **Add file** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="05bfb-134">Eylem Bölmesinde, **Kaydet**'i ve sonra **İçe Aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-134">On the Action Pane, select **Save** , and then select **Import**.</span></span>

<span data-ttu-id="05bfb-135">Aşağıdaki örnek görüntü, Commerce'te **varlık ekle** öğeleri ve dışa aktarılan CSV dosyası üstbilgilerinin vurgulandığı **Ekip eşlemesini dışa aktar** grubunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="05bfb-135">The following example image shows the **Export teams mapping** group in Commerce with **Add entity** elements and the exported CSV file headers highlighted.</span></span>

![Commerce'te varlık ekle öğeleri ve dışa aktarılan CSV dosyası üstbilgilerinin vurgulandığı Ekip eşlemesini dışa aktar grubu](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> <span data-ttu-id="05bfb-137">Önceki adımları tamamladıktan sonra, görev yönetimini eşlemek için [Microsoft Teams ve POS arasında görev eşleme](synchronize-tasks-teams-pos.md) adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="05bfb-137">After you complete the preceeding steps, follow the steps in [Synchronize task management between Microsoft Teams and POS](synchronize-tasks-teams-pos.md) to synchronize task management.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="05bfb-138">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="05bfb-138">Additional resources</span></span>

[<span data-ttu-id="05bfb-139">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bakış</span><span class="sxs-lookup"><span data-stu-id="05bfb-139">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="05bfb-140">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="05bfb-140">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="05bfb-141">Dynamics 365 Commerce'ten Microsoft Teams sağlama</span><span class="sxs-lookup"><span data-stu-id="05bfb-141">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="05bfb-142">Microsoft Teams ve Dynamics 365 Commerce POS arasında görev yönetimini eşitleme</span><span class="sxs-lookup"><span data-stu-id="05bfb-142">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="05bfb-143">Microsoft Teams'de kullanıcı rollerini yönetme</span><span class="sxs-lookup"><span data-stu-id="05bfb-143">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="05bfb-144">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi SSS</span><span class="sxs-lookup"><span data-stu-id="05bfb-144">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
