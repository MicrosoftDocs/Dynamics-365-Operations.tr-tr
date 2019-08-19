---
title: Veri tümleştirme sorunlarını giderme kılavuzu
description: Bu konu, Microsoft Dynamics 365 for Finance and Operations ile Common Data Service arasında veri tümleştirme hakkında sorun giderme bilgileri sağlar.
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
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797287"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="e77e1-103">Veri tümleştirme sorunlarını giderme kılavuzu</span><span class="sxs-lookup"><span data-stu-id="e77e1-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a><span data-ttu-id="e77e1-104">Common Data Service'teki Plugin Trace'i etkinleştirin ve çift yazma eklentisi hata ayrıntılarını kontrol edin</span><span class="sxs-lookup"><span data-stu-id="e77e1-104">Enable Plugin Trace in Common Data Service and check the dual-write Plugin error details</span></span>

<span data-ttu-id="e77e1-105">Bir sorun veya çift yazma eşitlemesi hatasıyla karşı karşıya iseniz, izleme günlüğünde hataları inceleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="e77e1-105">If you are facing an issue or error with dual-write synchronization, you can inspect the errors in the trace log:</span></span>

1. <span data-ttu-id="e77e1-106">Hataları incelemek için önce Eklenti izlemeyi etkinleştirmek için [Kayıt eklentisi](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) yönergelerini kullanarak Eklenti izlemeyi etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e77e1-106">Before you can inspect the errors, you must enable Plugin trace using the instructions in [Register plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) to enable Plugin trace.</span></span> <span data-ttu-id="e77e1-107">Şimdi hataları inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e77e1-107">Now you can inspect the errors.</span></span>
2. <span data-ttu-id="e77e1-108">Dynamics 365 for Sales'de oturum açın.</span><span class="sxs-lookup"><span data-stu-id="e77e1-108">Login to Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="e77e1-109">Ayarlar simgesine (dişli) tıklayın ve **Gelişmiş ayarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e77e1-109">Click on the Settings icon (a gear), and select **Advanced Settings**.</span></span>
4. <span data-ttu-id="e77e1-110">**Ayarlar** menüsünde **Özelleştirme > Eklenti izleme günlüğünü**seçin.</span><span class="sxs-lookup"><span data-stu-id="e77e1-110">In the **Settings** menu, choose **Customization > Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="e77e1-111">Hata ayrıntılarını görüntülemek için **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** türü adını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e77e1-111">Click the type name **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** to display the error details.</span></span>

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="e77e1-112">Finance and Operations'ta çift yazma eşitleme hatalarını denetle</span><span class="sxs-lookup"><span data-stu-id="e77e1-112">Check dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="e77e1-113">Aşağıdaki adımları izleyerek test sırasında hataları denetleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="e77e1-113">You can check the errors during testing by following these steps:</span></span>

+ <span data-ttu-id="e77e1-114">LifeCycle Services (LCS)'ye giriş yapın.</span><span class="sxs-lookup"><span data-stu-id="e77e1-114">Login to LifeCycle Services (LCS).</span></span>
+ <span data-ttu-id="e77e1-115">Çift yazma sınaması gerçekleştirmek için seçtiğiniz LCS projesini açın.</span><span class="sxs-lookup"><span data-stu-id="e77e1-115">Open the LCS project that you chose to perform dual-write testing.</span></span>
+ <span data-ttu-id="e77e1-116">Bulutta Barındırılan Ortamlar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="e77e1-116">Go to Cloud Hosted Environments.</span></span>
+ <span data-ttu-id="e77e1-117">LCS'de görüntülenen yerel hesabı kullanarak Finance and Operations VM'ye uzak masaüstü.</span><span class="sxs-lookup"><span data-stu-id="e77e1-117">Remote desktop to Finance and Operations VM using local account that is displayed in LCS.</span></span>
+ <span data-ttu-id="e77e1-118">Olay görüntüleyiciyi açın.</span><span class="sxs-lookup"><span data-stu-id="e77e1-118">Open the event viewer.</span></span> 
+ <span data-ttu-id="e77e1-119">**Uygulamalar ve Hizmetler günlükleri > Microsoft > Dynamics > AX-DualWriteSync > İşletim**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="e77e1-119">Navigate to **Applications and Services logs > Microsoft > Dynamics > AX-DualWriteSync > Operational**.</span></span> <span data-ttu-id="e77e1-120">Hatalar ve ayrıntılar görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e77e1-120">The errors and details are displayed.</span></span>

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a><span data-ttu-id="e77e1-121">Finance and Operations'tan başka bir Common Data Service ortam bağlantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="e77e1-121">How to unlink and link another Common Data Service environment from Finance and Operations</span></span>

<span data-ttu-id="e77e1-122">Aşağıdaki adımları izleyerek bağlantıları güncelleştirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="e77e1-122">You can update links by following these steps:</span></span>

+ <span data-ttu-id="e77e1-123">Finance and Operations ortamınıza gidin.</span><span class="sxs-lookup"><span data-stu-id="e77e1-123">Navigate to the Finance and Operations environment.</span></span>
+ <span data-ttu-id="e77e1-124">Veri Yönetimini açın.</span><span class="sxs-lookup"><span data-stu-id="e77e1-124">Open Data Management.</span></span>
+ <span data-ttu-id="e77e1-125">**Uygulamalar için CDS bağlantısı**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e77e1-125">Click on **Link to CDS for apps**.</span></span>
+ <span data-ttu-id="e77e1-126">Çalışan tüm eşlemeleri seçin ve **Durdur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e77e1-126">Select all the running mappings and click **Stop**.</span></span> 
+ <span data-ttu-id="e77e1-127">Tüm eşlemeleri seçin ve **Sil**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e77e1-127">Select all the mappings and click **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e77e1-128">**CustomerV3-Account** şablonu seçiliyse **Sil** seçeneği görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="e77e1-128">The **Delete** option will not appear if **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="e77e1-129">Gerekirse seçimi kaldırın.</span><span class="sxs-lookup"><span data-stu-id="e77e1-129">Unselect it if needed.</span></span> <span data-ttu-id="e77e1-130">**CustomerV3-Account** eski bir sağlanan şablondur ve Müşteri Adayı'ndan Nakde çözümü ile çalışır.</span><span class="sxs-lookup"><span data-stu-id="e77e1-130">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="e77e1-131">Genel olarak yayımlandığından tüm şablonlar altında gösterir.</span><span class="sxs-lookup"><span data-stu-id="e77e1-131">Because it is globally released, it shows up under all templates.</span></span>

+ <span data-ttu-id="e77e1-132">**Ortam bağlantısını kaldırma**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e77e1-132">Click **Unlink environment**.</span></span>
+ <span data-ttu-id="e77e1-133">Onay için **Evet**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e77e1-133">Click **Yes** for confirmation.</span></span>
+ <span data-ttu-id="e77e1-134">Yeni ortamı bağlamak için, [yükleme kılavuzundaki](https://aka.ms/dualwrite-docs) adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e77e1-134">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>

