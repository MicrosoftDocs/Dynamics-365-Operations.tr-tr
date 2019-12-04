---
title: Veri tümleştirme sorunlarını giderme kılavuzu
description: Bu konu, Finance and Operations uygulamaları ile Common Data Service arasında veri tümleştirme hakkında sorun giderme bilgileri sağlar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 35c0a1e6342008bc2ee6ff25a1663e199c8cb985
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771037"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="1e043-103">Veri tümleştirme sorunlarını giderme kılavuzu</span><span class="sxs-lookup"><span data-stu-id="1e043-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a><span data-ttu-id="1e043-104">Common Data Service'teki Eklenti izleme günlüklerini etkinleştirin ve çift yazma eklentisi hata ayrıntılarını kontrol edin</span><span class="sxs-lookup"><span data-stu-id="1e043-104">Enable plug-in trace logs in Common Data Service and inspect the dual-write plug-in error details</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e043-105">Çift-yazma eşitleme sırasında bir sorunla veya hatayla karşılaşırsanız izleme günlüğündeki hataları denetlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="1e043-105">If you experience an issue or error during dual-write synchronization, follow these steps to inspect the errors in the trace log.</span></span>

1. <span data-ttu-id="1e043-106">Hataları incelemeniz için önce eklenti izleme günlüklerini etkinleştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="1e043-106">Before you can inspect the errors, you must enable plug-in trace logs.</span></span> <span data-ttu-id="1e043-107">Yönergeler için [Öğretici: Bir ekletiyi yazma ve kaydetme](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs)'deki "İzleme günlüğü görüntüle" bölümüne bakınız.</span><span class="sxs-lookup"><span data-stu-id="1e043-107">For instructions, see the "View trace logs" section of [Tutorial: Write and register a plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span></span>

    <span data-ttu-id="1e043-108">Şimdi hataları inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1e043-108">You can now inspect the errors.</span></span>

2. <span data-ttu-id="1e043-109">Microsoft Dynamics 365 Sales'te oturum açın.</span><span class="sxs-lookup"><span data-stu-id="1e043-109">Sign in to Microsoft Dynamics 365 Sales.</span></span>
3. <span data-ttu-id="1e043-110">**Ayarlar** düğmesini (çark simgesi) seçin ve sonra **Gelişmiş ayarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1e043-110">Select the **Settings** button (the gear symbol), and then select **Advanced Settings**.</span></span>
4. <span data-ttu-id="1e043-111">**Ayarlar** menüsünde **Özelleştirme \> Eklenti izleme günlüğü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="1e043-111">On the **Settings** menu, select **Customization \> Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="1e043-112">Hata ayrıntılarını görüntülemek için **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**'i tür adı olarak seçin.</span><span class="sxs-lookup"><span data-stu-id="1e043-112">Select **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** as the type name to show the error details.</span></span>

## <a name="inspect-dual-write-synchronization-errors"></a><span data-ttu-id="1e043-113">Çift yazma eşitleme hatalarını denetleyin</span><span class="sxs-lookup"><span data-stu-id="1e043-113">Inspect dual-write synchronization errors</span></span>

<span data-ttu-id="1e043-114">Test sırasında hataları incelemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="1e043-114">Follow these steps to inspect errors during testing.</span></span>

1. <span data-ttu-id="1e043-115">Microsoft Dynamics Lifecycle Services (LCS)'de oturum açın.</span><span class="sxs-lookup"><span data-stu-id="1e043-115">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="1e043-116">Çift-yazma testi yapmak için LCS projesini açın.</span><span class="sxs-lookup"><span data-stu-id="1e043-116">Open the LCS project to do dual-write testing for.</span></span>
3. <span data-ttu-id="1e043-117">**Bulutta barındırılan ortamlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1e043-117">Select **Cloud-hosted environments**.</span></span>
4. <span data-ttu-id="1e043-118">LCS 'de gösterilen yerel hesabı kullanarak uygulama sanal makinesinde (VM) Uzak Masaüstü bağlantısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1e043-118">Make a Remote desktop connection to the application virtual machine (VM) by using local account that is shown in LCS.</span></span>
5. <span data-ttu-id="1e043-119">Olay Görüntüleyiciyi açın.</span><span class="sxs-lookup"><span data-stu-id="1e043-119">Open Event Viewer.</span></span> 
6. <span data-ttu-id="1e043-120">**Uygulamalar ve Hizmetler günlükleri \> Microsoft \> Dynamics \> AX-DualWriteSync \> İşletim**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="1e043-120">Go to **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span> <span data-ttu-id="1e043-121">Hatalar ve ayrıntılar görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="1e043-121">The errors and details are shown.</span></span>

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a><span data-ttu-id="1e043-122">Uygulamadan bir Common Data Service ortam bağlantısını kaldırın ve başka bir ortama bağlayın</span><span class="sxs-lookup"><span data-stu-id="1e043-122">Unlink one Common Data Service environment from the application and link another environment</span></span>

<span data-ttu-id="1e043-123">Bağlantıları güncelleştirmek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="1e043-123">Follow these steps to update links.</span></span>

1. <span data-ttu-id="1e043-124">Uygulama ortamına gidin.</span><span class="sxs-lookup"><span data-stu-id="1e043-124">Go to the application environment.</span></span>
2. <span data-ttu-id="1e043-125">Veri Yönetimini açın.</span><span class="sxs-lookup"><span data-stu-id="1e043-125">Open Data Management.</span></span>
3. <span data-ttu-id="1e043-126">**Uygulamalar için CDS bağlantısı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="1e043-126">Select **Link to CDS for apps**.</span></span>
4. <span data-ttu-id="1e043-127">Çalışan tüm eşlemeleri seçin ve **Durdur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="1e043-127">Select all the mappings that are running, and then select **Stop**.</span></span>
5. <span data-ttu-id="1e043-128">Tüm eşlemeleri seçin ve **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1e043-128">Select all the mappings, and then select **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1e043-129">**CustomerV3-Account** şablonu seçiliyse **Sil** seçeneği uygun olmaz.</span><span class="sxs-lookup"><span data-stu-id="1e043-129">The **Delete** option isn't available if the **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="1e043-130">Bu şablonun seçimini gerektiği gibi temizleyin.</span><span class="sxs-lookup"><span data-stu-id="1e043-130">Clear the selection of this template as required.</span></span> <span data-ttu-id="1e043-131">**CustomerV3-Account** eski bir sağlanan şablondur ve Müşteri Adayı'ndan Nakde çözümü ile çalışır.</span><span class="sxs-lookup"><span data-stu-id="1e043-131">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="1e043-132">Genel olarak yayımlandığından tüm şablonlar altında gösterir.</span><span class="sxs-lookup"><span data-stu-id="1e043-132">Because it's globally released, it appears under all templates.</span></span>

6. <span data-ttu-id="1e043-133">**Ortam bağlantısını kaldırma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="1e043-133">Select **Unlink environment**.</span></span>
7. <span data-ttu-id="1e043-134">Operasyonu onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1e043-134">Select **Yes** to confirm the operation.</span></span>
8. <span data-ttu-id="1e043-135">Yeni ortamı bağlamak için, [yükleme kılavuzundaki](https://aka.ms/dualwrite-docs) adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="1e043-135">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>
