---
title: Maliyet muhasebesi hizmetini kullanmaya başlama
description: Bu konu, maliyet muhasebesi hizmeti için lisans ayrıntılarını ve yükleme yönergelerini sağlar.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cbbce7eaac264973bf0b95ad5175bf70ed2b4ae9
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276972"
---
# <a name="get-started-with-the-cost-accounting-service"></a><span data-ttu-id="8d408-103">Maliyet muhasebesi hizmetini kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="8d408-103">Get started with the cost accounting service</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="8d408-104">Bu konuda belirtilen işlev özel bir önizleme sürümünün bir parçası olarak sunulur.</span><span class="sxs-lookup"><span data-stu-id="8d408-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="8d408-105">Bu konunun içeriği ve tanımladığı işlevsellik değişebilir.</span><span class="sxs-lookup"><span data-stu-id="8d408-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="8d408-106">Önizleme sürümleri hakkında daha fazla bilgi için bkz. [Bir sürüm hizmeti güncelleştirmeleriyle ilgili SSS](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="8d408-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="8d408-107">Maliyet muhasebesi hizmeti, ayarlamış olduğunuz maliyet muhasebesi defterlerinde çoklu stok hesapları yapmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="8d408-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="8d408-108">Her bir maliyet muhasebesi defterini bir *kural* ile ilişkilendirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8d408-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="8d408-109">Kural, aşağıdaki muhasebe ilkesi türlerinin bir koleksiyondur:</span><span class="sxs-lookup"><span data-stu-id="8d408-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="8d408-110">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="8d408-110">Cost object</span></span>
- <span data-ttu-id="8d408-111">Giriş ölçümü esası</span><span class="sxs-lookup"><span data-stu-id="8d408-111">Input measurement basis</span></span>
- <span data-ttu-id="8d408-112">Maliyet akışı varsayımı</span><span class="sxs-lookup"><span data-stu-id="8d408-112">Cost flow assumption</span></span>
- <span data-ttu-id="8d408-113">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="8d408-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="8d408-114">Maliyet muhasebesi hizmetini açsanız bile, Microsoft Dynamics 365 Supply Chain Management'ta stok muhasebesini her zamanki gibi de yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8d408-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="8d408-115">Maliyet muhasebesi hizmeti bir eklentidir.</span><span class="sxs-lookup"><span data-stu-id="8d408-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="8d408-116">Özelliklerini kullanılabilir hale getirmek için Microsoft Dynamics Lifecycle Services'tan (LCS) yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8d408-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="8d408-117">Bu nedenle, üretim ortamları için etkinleştirmeden önce bir test ortamında değerlendirmeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8d408-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="8d408-118">Maliyet muhasebesi hizmeti şu anda Dynamics 365 Supply Chain Management'ta yerleşik olan tüm maliyet yönetimi özelliklerini desteklememektedir.</span><span class="sxs-lookup"><span data-stu-id="8d408-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="8d408-119">Bu nedenle, şu anda mevcut olan özellik kümesinin gereksinimlerinizi karşılayıp karşılamadığını değerlendirmeniz önemlidir.</span><span class="sxs-lookup"><span data-stu-id="8d408-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="licensing"></a><span data-ttu-id="8d408-120">Lisans</span><span class="sxs-lookup"><span data-stu-id="8d408-120">Licensing</span></span>

<span data-ttu-id="8d408-121">Maliyet muhasebesi hizmeti Supply Chain Management için kullanılabilir olan stok muhasebesi standart özellikleri ile birlikte lisanslanır.</span><span class="sxs-lookup"><span data-stu-id="8d408-121">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="8d408-122">Maliyet muhasebesi hizmetini kullanmak için ek lisans satın almanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="8d408-122">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><span data-ttu-id="8d408-123">Eklentiyi yükleme</span><span class="sxs-lookup"><span data-stu-id="8d408-123">Install the add-in</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d408-124">Maliyet muhasebesi hizmetini kullanmak için, LCS'nin etkin olduğu yüksek kullanılabilirlik ortamına sahip olmanız (OneBox ortamı değil) ve Dynamics 365 Supply Chain Management sürüm 10.0.11 veya üstünü çalıştırıyor olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8d408-124">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="8d408-125">Maliyet muhasebesi hizmetini kullanmak için, aşağıdaki yordamda açıklandığı şekilde Supply Chain Management için maliyet muhasebesi hizmeti eklentisini yükleyin.</span><span class="sxs-lookup"><span data-stu-id="8d408-125">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="8d408-126">LCS'de oturum açın</span><span class="sxs-lookup"><span data-stu-id="8d408-126">Sign in to LCS.</span></span>

1. <span data-ttu-id="8d408-127">**Özellik yönetimi önizlemesi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8d408-127">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="8d408-128">Artı işaretini (**+**) seçin.</span><span class="sxs-lookup"><span data-stu-id="8d408-128">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="8d408-129">**Kod** alanına maliyet muhasebesi hizmeti için eklenti beta anahtarınızı girin.</span><span class="sxs-lookup"><span data-stu-id="8d408-129">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="8d408-130">(Anahtarınızı e-posta ile almış olmanız gerekir.)</span><span class="sxs-lookup"><span data-stu-id="8d408-130">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="8d408-131">**Engellemeyi Kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8d408-131">Select **Unblock**.</span></span>

1. <span data-ttu-id="8d408-132">Hizmeti eklemek istediğiniz LCS ortamını açın.</span><span class="sxs-lookup"><span data-stu-id="8d408-132">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="8d408-133">**Tüm ayrıntılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="8d408-133">Go to **Full details**.</span></span>

1. <span data-ttu-id="8d408-134">**Ortam eklentileri** hızlı sekmesinde aşağı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="8d408-134">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="8d408-135">**Yeni eklenti yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8d408-135">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="8d408-136">**Maliyet muhasebesi hizmeti**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="8d408-136">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="8d408-137">Yükleme kılavuzunu izleyin ve hüküm ve koşulları kabul edin.</span><span class="sxs-lookup"><span data-stu-id="8d408-137">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="8d408-138">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8d408-138">Select **Install**.</span></span>

1. <span data-ttu-id="8d408-139">**Ortam eklentileri** hızlı sekmesinde, maliyet muhasebesi hizmetinin yüklenmekte olduğunu görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="8d408-139">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="8d408-140">Birkaç dakika sonra, durum **Yükleniyor** yerine **Yüklü** olarak değişmelidir.</span><span class="sxs-lookup"><span data-stu-id="8d408-140">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="8d408-141">(Bu değişikliği görmek için sayfayı yenilemeniz gerekebilir.) Bu noktada, maliyet muhasebesi hizmeti kullanıma hazırdır.</span><span class="sxs-lookup"><span data-stu-id="8d408-141">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="8d408-142">Tümleştirmeyi ayarlama</span><span class="sxs-lookup"><span data-stu-id="8d408-142">Set up the integration</span></span>

<span data-ttu-id="8d408-143">Maliyet muhasebesi hizmeti ve Dynamics 365 Supply Chain Management arasındaki tümleştirmeyi ayarlamak için:</span><span class="sxs-lookup"><span data-stu-id="8d408-143">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="8d408-144">**Sistem yönetimi > Özellik Yönetimi** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="8d408-144">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="8d408-145">**Güncelleştirmeleri denetle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8d408-145">Select **Check for updates**.</span></span>

1. <span data-ttu-id="8d408-146">**Tümü** sekmesini açın ve *Maliyet muhasebesi hizmeti* adlı özelliği arayın.</span><span class="sxs-lookup"><span data-stu-id="8d408-146">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="8d408-147">**Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8d408-147">Select **Enable now**.</span></span>

1. <span data-ttu-id="8d408-148">**Maliyet yönetimi > Maliyet muhasebesi hizmeti > Kurulum > Maliyet muhasebesi hizmeti parametreleri > Tümleştirme parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8d408-148">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="8d408-149">**Uygulama kodu** alanına aşağıdaki kodu girin:</span><span class="sxs-lookup"><span data-stu-id="8d408-149">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="8d408-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="8d408-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="8d408-151">**Veri hizmeti son noktası** alanında, aşağıdaki URL'yi girin:</span><span class="sxs-lookup"><span data-stu-id="8d408-151">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="8d408-152">**Maliyet muhasebesi hizmeti son noktası** alanında, aşağıdaki URL'yi girin:</span><span class="sxs-lookup"><span data-stu-id="8d408-152">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="8d408-153">Maliyet muhasebesi hizmeti artık kullanıma hazır.</span><span class="sxs-lookup"><span data-stu-id="8d408-153">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="8d408-154">İlgili kaynaklar</span><span class="sxs-lookup"><span data-stu-id="8d408-154">Related resources</span></span>

[<span data-ttu-id="8d408-155">Maliyet muhasebesi hizmeti giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="8d408-155">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
