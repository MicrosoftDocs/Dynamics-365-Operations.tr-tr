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
ms.openlocfilehash: c16268338085d414468f17362294fb7e933d1b57
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249121"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="0889a-103">Veri tümleştirme sorunlarını giderme kılavuzu</span><span class="sxs-lookup"><span data-stu-id="0889a-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a><span data-ttu-id="0889a-104">Common Data Service'teki Eklenti izleme günlüklerini etkinleştirin ve çift yazma eklentisi hata ayrıntılarını kontrol edin</span><span class="sxs-lookup"><span data-stu-id="0889a-104">Enable plug-in trace logs in Common Data Service and inspect the dual-write plug-in error details</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="0889a-105">Çift-yazma eşitleme sırasında bir sorunla veya hatayla karşılaşırsanız izleme günlüğündeki hataları denetlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0889a-105">If you experience an issue or error during dual-write synchronization, follow these steps to inspect the errors in the trace log.</span></span>

1. <span data-ttu-id="0889a-106">Hataları incelemeniz için önce eklenti izleme günlüklerini etkinleştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="0889a-106">Before you can inspect the errors, you must enable plug-in trace logs.</span></span> <span data-ttu-id="0889a-107">Yönergeler için [Öğretici: Bir ekletiyi yazma ve kaydetme](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs)'deki "İzleme günlüğü görüntüle" bölümüne bakınız.</span><span class="sxs-lookup"><span data-stu-id="0889a-107">For instructions, see the "View trace logs" section of [Tutorial: Write and register a plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span></span>

    <span data-ttu-id="0889a-108">Şimdi hataları inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0889a-108">You can now inspect the errors.</span></span>

2. <span data-ttu-id="0889a-109">Microsoft Dynamics 365 Sales'te oturum açın.</span><span class="sxs-lookup"><span data-stu-id="0889a-109">Sign in to Microsoft Dynamics 365 Sales.</span></span>
3. <span data-ttu-id="0889a-110">**Ayarlar** düğmesini (çark simgesi) seçin ve sonra **Gelişmiş ayarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0889a-110">Select the **Settings** button (the gear symbol), and then select **Advanced Settings**.</span></span>
4. <span data-ttu-id="0889a-111">**Ayarlar** menüsünde **Özelleştirme \> Eklenti izleme günlüğü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="0889a-111">On the **Settings** menu, select **Customization \> Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="0889a-112">Hata ayrıntılarını görüntülemek için **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**'i tür adı olarak seçin.</span><span class="sxs-lookup"><span data-stu-id="0889a-112">Select **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** as the type name to show the error details.</span></span>

## <a name="inspect-dual-write-synchronization-errors"></a><span data-ttu-id="0889a-113">Çift yazma eşitleme hatalarını denetleyin</span><span class="sxs-lookup"><span data-stu-id="0889a-113">Inspect dual-write synchronization errors</span></span>

<span data-ttu-id="0889a-114">Test sırasında hataları incelemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0889a-114">Follow these steps to inspect errors during testing.</span></span>

1. <span data-ttu-id="0889a-115">Microsoft Dynamics Lifecycle Services (LCS)'de oturum açın.</span><span class="sxs-lookup"><span data-stu-id="0889a-115">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="0889a-116">Çift-yazma testi yapmak için LCS projesini açın.</span><span class="sxs-lookup"><span data-stu-id="0889a-116">Open the LCS project to do dual-write testing for.</span></span>
3. <span data-ttu-id="0889a-117">**Bulutta barındırılan ortamlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0889a-117">Select **Cloud-hosted environments**.</span></span>
4. <span data-ttu-id="0889a-118">LCS 'de gösterilen yerel hesabı kullanarak uygulama sanal makinesinde (VM) Uzak Masaüstü bağlantısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0889a-118">Make a Remote desktop connection to the application virtual machine (VM) by using local account that is shown in LCS.</span></span>
5. <span data-ttu-id="0889a-119">Olay Görüntüleyiciyi açın.</span><span class="sxs-lookup"><span data-stu-id="0889a-119">Open Event Viewer.</span></span> 
6. <span data-ttu-id="0889a-120">**Uygulamalar ve Hizmetler günlükleri \> Microsoft \> Dynamics \> AX-DualWriteSync \> İşletim**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="0889a-120">Go to **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span> <span data-ttu-id="0889a-121">Hatalar ve ayrıntılar görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="0889a-121">The errors and details are shown.</span></span>

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a><span data-ttu-id="0889a-122">Uygulamadan bir Common Data Service ortam bağlantısını kaldırın ve başka bir ortama bağlayın</span><span class="sxs-lookup"><span data-stu-id="0889a-122">Unlink one Common Data Service environment from the application and link another environment</span></span>

<span data-ttu-id="0889a-123">Bağlantıları güncelleştirmek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0889a-123">Follow these steps to update links.</span></span>

1. <span data-ttu-id="0889a-124">Uygulama ortamına gidin.</span><span class="sxs-lookup"><span data-stu-id="0889a-124">Go to the application environment.</span></span>
2. <span data-ttu-id="0889a-125">Veri Yönetimini açın.</span><span class="sxs-lookup"><span data-stu-id="0889a-125">Open Data Management.</span></span>
3. <span data-ttu-id="0889a-126">**Uygulamalar için CDS bağlantısı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="0889a-126">Select **Link to CDS for apps**.</span></span>
4. <span data-ttu-id="0889a-127">Çalışan tüm eşlemeleri seçin ve **Durdur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="0889a-127">Select all the mappings that are running, and then select **Stop**.</span></span>
5. <span data-ttu-id="0889a-128">Tüm eşlemeleri seçin ve **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0889a-128">Select all the mappings, and then select **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0889a-129">**CustomerV3-Account** şablonu seçiliyse **Sil** seçeneği uygun olmaz.</span><span class="sxs-lookup"><span data-stu-id="0889a-129">The **Delete** option isn't available if the **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="0889a-130">Bu şablonun seçimini gerektiği gibi temizleyin.</span><span class="sxs-lookup"><span data-stu-id="0889a-130">Clear the selection of this template as required.</span></span> <span data-ttu-id="0889a-131">**CustomerV3-Account** eski bir sağlanan şablondur ve Müşteri Adayı'ndan Nakde çözümü ile çalışır.</span><span class="sxs-lookup"><span data-stu-id="0889a-131">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="0889a-132">Genel olarak yayımlandığından tüm şablonlar altında gösterir.</span><span class="sxs-lookup"><span data-stu-id="0889a-132">Because it's globally released, it appears under all templates.</span></span>

6. <span data-ttu-id="0889a-133">**Ortam bağlantısını kaldırma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="0889a-133">Select **Unlink environment**.</span></span>
7. <span data-ttu-id="0889a-134">Operasyonu onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0889a-134">Select **Yes** to confirm the operation.</span></span>
8. <span data-ttu-id="0889a-135">Yeni ortamı bağlamak için, [yükleme kılavuzundaki](https://aka.ms/dualwrite-docs) adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0889a-135">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>
