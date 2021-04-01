---
title: Maliyet muhasebesi hizmetini (özel önizleme) kullanmaya başlama
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
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: bbf2df112657342245aca2bd02e06cee7e51ea82
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251062"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a><span data-ttu-id="2b357-103">Maliyet muhasebesi hizmetini (özel önizleme) kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="2b357-103">Get started with the cost accounting service (private preview)</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="2b357-104">Bu konuda belirtilen işlev özel bir önizleme sürümünün bir parçası olarak sunulur.</span><span class="sxs-lookup"><span data-stu-id="2b357-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="2b357-105">Bu konunun içeriği ve tanımladığı işlevsellik değişebilir.</span><span class="sxs-lookup"><span data-stu-id="2b357-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="2b357-106">Önizleme sürümleri hakkında daha fazla bilgi için bkz. [Bir sürüm hizmeti güncelleştirmeleriyle ilgili SSS](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="2b357-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="2b357-107">Maliyet muhasebesi hizmeti, ayarlamış olduğunuz maliyet muhasebesi defterlerinde çoklu stok hesapları yapmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="2b357-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="2b357-108">Her bir maliyet muhasebesi defterini bir *kural* ile ilişkilendirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b357-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="2b357-109">Kural, aşağıdaki muhasebe ilkesi türlerinin bir koleksiyondur:</span><span class="sxs-lookup"><span data-stu-id="2b357-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="2b357-110">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2b357-110">Cost object</span></span>
- <span data-ttu-id="2b357-111">Giriş ölçümü esası</span><span class="sxs-lookup"><span data-stu-id="2b357-111">Input measurement basis</span></span>
- <span data-ttu-id="2b357-112">Maliyet akışı varsayımı</span><span class="sxs-lookup"><span data-stu-id="2b357-112">Cost flow assumption</span></span>
- <span data-ttu-id="2b357-113">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="2b357-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="2b357-114">Maliyet muhasebesi hizmetini açsanız bile, Microsoft Dynamics 365 Supply Chain Management'ta stok muhasebesini her zamanki gibi de yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b357-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="2b357-115">Maliyet muhasebesi hizmeti bir eklentidir.</span><span class="sxs-lookup"><span data-stu-id="2b357-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="2b357-116">Özelliklerini kullanılabilir hale getirmek için Microsoft Dynamics Lifecycle Services'tan (LCS) yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b357-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="2b357-117">Bu nedenle, üretim ortamları için etkinleştirmeden önce bir test ortamında değerlendirmeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b357-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="2b357-118">Maliyet muhasebesi hizmeti şu anda Dynamics 365 Supply Chain Management'ta yerleşik olan tüm maliyet yönetimi özelliklerini desteklememektedir.</span><span class="sxs-lookup"><span data-stu-id="2b357-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="2b357-119">Bu nedenle, şu anda mevcut olan özellik kümesinin gereksinimlerinizi karşılayıp karşılamadığını değerlendirmeniz önemlidir.</span><span class="sxs-lookup"><span data-stu-id="2b357-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a><span data-ttu-id="2b357-120">Maliyet muhasebesi hizmetini (özel önizleme) alma</span><span class="sxs-lookup"><span data-stu-id="2b357-120">How to get the cost accounting service (private preview)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2b357-121">Maliyet muhasebesi hizmetini kullanmak için, LCS'nin etkin olduğu yüksek kullanılabilirlik ortamına sahip olmanız (OneBox ortamı değil) ve Dynamics 365 Supply Chain Management sürüm 10.0.11 veya üstünü çalıştırıyor olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b357-121">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="2b357-122">Maliyet muhasebesi hizmet özel önizlemesine kaydolmak için lütfen LCS ortam kimliğinizi [Maliyet muhasebesi hizmetine (özel önizleme)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29) e-posta ile gönderin.</span><span class="sxs-lookup"><span data-stu-id="2b357-122">To sign up for the cost accounting service private preview, please send your LCS environment ID by email to [Cost accounting service (private preview)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span></span> <span data-ttu-id="2b357-123">Program için onay aldığınızda, maliyet muhasebesi hizmeti beta anahtarını içeren bir takip e-postası alacaksınız.</span><span class="sxs-lookup"><span data-stu-id="2b357-123">On approving you for the program, we will send you a follow up email that contains a cost accounting service beta key.</span></span> <span data-ttu-id="2b357-124">Beta anahtarını aldığınızda, [eklentiyi yükleyerek](#install) devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b357-124">On receiving the beta key, you can proceed by [installing the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="2b357-125">Lisans</span><span class="sxs-lookup"><span data-stu-id="2b357-125">Licensing</span></span>

<span data-ttu-id="2b357-126">Maliyet muhasebesi hizmeti Supply Chain Management için kullanılabilir olan stok muhasebesi standart özellikleri ile birlikte lisanslanır.</span><span class="sxs-lookup"><span data-stu-id="2b357-126">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="2b357-127">Maliyet muhasebesi hizmetini kullanmak için ek lisans satın almanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="2b357-127">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="2b357-128">Eklentiyi yükleme</span><span class="sxs-lookup"><span data-stu-id="2b357-128">Install the add-in</span></span>

<span data-ttu-id="2b357-129">Maliyet muhasebesi hizmetini kullanmak için, aşağıdaki yordamda açıklandığı şekilde Supply Chain Management için maliyet muhasebesi hizmeti eklentisini yükleyin.</span><span class="sxs-lookup"><span data-stu-id="2b357-129">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="2b357-130">Maliyet muhasebesi hizmetine (özel önizleme) [kaydolun](#sign-up).</span><span class="sxs-lookup"><span data-stu-id="2b357-130">[Sign up](#sign-up) for the cost accounting service (private preview).</span></span>

1. <span data-ttu-id="2b357-131">LCS'de oturum açın</span><span class="sxs-lookup"><span data-stu-id="2b357-131">Sign in to LCS.</span></span>

1. <span data-ttu-id="2b357-132">**Özellik yönetimi önizlemesi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2b357-132">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="2b357-133">Artı işaretini (**+**) seçin.</span><span class="sxs-lookup"><span data-stu-id="2b357-133">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="2b357-134">**Kod** alanına maliyet muhasebesi hizmeti için eklenti beta anahtarınızı girin.</span><span class="sxs-lookup"><span data-stu-id="2b357-134">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="2b357-135">(Anahtarınızı e-posta ile almış olmanız gerekir.)</span><span class="sxs-lookup"><span data-stu-id="2b357-135">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="2b357-136">**Engellemeyi Kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b357-136">Select **Unblock**.</span></span>

1. <span data-ttu-id="2b357-137">Hizmeti eklemek istediğiniz LCS ortamını açın.</span><span class="sxs-lookup"><span data-stu-id="2b357-137">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="2b357-138">**Tüm ayrıntılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="2b357-138">Go to **Full details**.</span></span>

1. <span data-ttu-id="2b357-139">**Ortam eklentileri** hızlı sekmesinde aşağı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="2b357-139">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="2b357-140">**Yeni eklenti yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b357-140">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="2b357-141">**Maliyet muhasebesi hizmeti**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2b357-141">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="2b357-142">Yükleme kılavuzunu izleyin ve hüküm ve koşulları kabul edin.</span><span class="sxs-lookup"><span data-stu-id="2b357-142">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="2b357-143">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b357-143">Select **Install**.</span></span>

1. <span data-ttu-id="2b357-144">**Ortam eklentileri** hızlı sekmesinde, maliyet muhasebesi hizmetinin yüklenmekte olduğunu görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="2b357-144">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="2b357-145">Birkaç dakika sonra, durum **Yükleniyor** yerine **Yüklü** olarak değişmelidir.</span><span class="sxs-lookup"><span data-stu-id="2b357-145">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="2b357-146">(Bu değişikliği görmek için sayfayı yenilemeniz gerekebilir.) Bu noktada, maliyet muhasebesi hizmeti kullanıma hazırdır.</span><span class="sxs-lookup"><span data-stu-id="2b357-146">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="2b357-147">Tümleştirmeyi ayarlama</span><span class="sxs-lookup"><span data-stu-id="2b357-147">Set up the integration</span></span>

<span data-ttu-id="2b357-148">Maliyet muhasebesi hizmeti ve Dynamics 365 Supply Chain Management arasındaki tümleştirmeyi ayarlamak için:</span><span class="sxs-lookup"><span data-stu-id="2b357-148">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="2b357-149">**Sistem yönetimi > Özellik Yönetimi** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="2b357-149">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="2b357-150">**Güncelleştirmeleri denetle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b357-150">Select **Check for updates**.</span></span>

1. <span data-ttu-id="2b357-151">**Tümü** sekmesini açın ve *Maliyet muhasebesi hizmeti* adlı özelliği arayın.</span><span class="sxs-lookup"><span data-stu-id="2b357-151">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="2b357-152">**Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b357-152">Select **Enable now**.</span></span>

1. <span data-ttu-id="2b357-153">**Maliyet yönetimi > Maliyet muhasebesi hizmeti > Kurulum > Maliyet muhasebesi hizmeti parametreleri > Tümleştirme parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2b357-153">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="2b357-154">**Uygulama kodu** alanına aşağıdaki kodu girin:</span><span class="sxs-lookup"><span data-stu-id="2b357-154">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="2b357-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="2b357-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="2b357-156">**Veri hizmeti son noktası** alanında, aşağıdaki URL'yi girin:</span><span class="sxs-lookup"><span data-stu-id="2b357-156">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="2b357-157">**Maliyet muhasebesi hizmeti son noktası** alanında, aşağıdaki URL'yi girin:</span><span class="sxs-lookup"><span data-stu-id="2b357-157">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="2b357-158">Maliyet muhasebesi hizmeti artık kullanıma hazır.</span><span class="sxs-lookup"><span data-stu-id="2b357-158">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="2b357-159">İlgili kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2b357-159">Related resources</span></span>

[<span data-ttu-id="2b357-160">Maliyet muhasebesi hizmeti giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="2b357-160">Cost accounting service home page</span></span>](cost-accounting-service-home.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]