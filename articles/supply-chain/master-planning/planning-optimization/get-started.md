---
title: Planlamayı En İyi Duruma Getirmeye başlayın
description: Bu konuda, Planlamayı En İyi Duruma Getirme işlevini kullanmaya nasıl başlanacağı açıklanmaktadır.
author: ChristianRytt
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 2867a4f9418e9435e2980fc24314914595ec44d0
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301686"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="7c4dd-103">Planlamayı En İyi Duruma Getirmeyi kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="7c4dd-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7c4dd-104">[Daha önce duyurulduğu](../../get-started/removed-deprecated-features-scm-updates.md#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios) gibi, Planlamayı En İyi Duruma Getirme varolan yerleşik master planlama altyapısının yerini almak üzere planlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-104">As [previously announced](../../get-started/removed-deprecated-features-scm-updates.md#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="7c4dd-105">Yerleşik Master planlama altyapısını kullanıyorsanız, şimdi Planlamayı En İyi Duruma Getirme için geçişinizi planlamaya başlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="7c4dd-106">Yükseltme işlemi zorlandığında işlemleriniz etkilenebileceğinden, geçiş işlemini hemen başlatmak önemlidir.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="7c4dd-107">Kullanımdan kaldırma zorunlu olduğunda yaşanacak son dakika sorunlarını önlemek için geçişi 1 Aralık 2020'den önce tamamlamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="7c4dd-108">Planlamayı En İyi Duruma Getirme işlevi şu anda Microsoft Supply Chain Management'ta yerleşik olan planlama altyapısında kullanılabilen tüm özellikleri desteklememektedir.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="7c4dd-109">Bu nedenle, Planlamayı En İyi Duruma Getirme hizmetinde şu anda mevcut olan özellik kümesinin gereksinimlerinizi karşılayıp karşılamadığını değerlendirmeniz önemlidir.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="7c4dd-110">Planlamayı En İyi Duruma Getirme işlevi şu anda Dynamics Lifecycle Services (LCS)'de varsayılan olarak etkin değil; bu nedenle özellik açılmadan önce değerlendirme yapma fırsatına sahipsiniz.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="7c4dd-111">Master planlama işleminiz üretim (Master planlamayla oluşturulmuş planlanmış üretim emirleri) içermiyorsa ve yerleşik Master planlama altyapısının 10.0.15 üstü sürümü olmasını istiyorsanız, Planlamayı En İyi Duruma Getirme işlevine geçiş için bir özel durum istemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="7c4dd-112">Sürüm 10.0.16 itibarıyla, planlı üretim emirleri olmadan yerleşik master planlama çalıştırıldığında ortamlarda bir hata gösterilecektir.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="7c4dd-113">Master planlama sırasında planlı üretim emirleri oluşturmayan tüm yeni dağıtımlar için Planlamayı En İyi Duruma Getirme işlevi kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="7c4dd-114">Planlı üretim emirleri olmadan Yerleşik Master planlama altyapısını çalıştıran mevcut ortamların sahipleri, özel durum işlemiyle ilgili ayrıntıların bulunduğu bir posta alacaktır.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="7c4dd-115">Planlamayı En İyi Duruma Getirme için geçişi değerlendirmek ve planlamak üzere bir iş ortağı ile çalışmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="7c4dd-116">Planlamayı En İyi Duruma Getirme hizmetini açmadan önce Planlamayı En İyi Duruma Getirme uygunluk analizinin sonuçlarını değerlendirmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="7c4dd-117">Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7c4dd-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="availability"></a><span data-ttu-id="7c4dd-118">Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="7c4dd-118">Availability</span></span>

<span data-ttu-id="7c4dd-119">Planlamayı En İyi Duruma Getirme şu anda şu Azure coğrafi bölgelerinde kullanılabilir: Amerika Birleşik Devletleri, Kanada, Avrupa, Birleşik Krallık, Avustralya ve Asya Pasifik.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, Australia, and Asia Pacific.</span></span> <span data-ttu-id="7c4dd-120">Eklentiyi başka bir coğrafi bölgeden yüklemeye çalışırsanız, LCS bu coğrafi bölgenin desteklenmediğini belirten bir ileti gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="7c4dd-121">Planlamayı En İyi Duruma Getirme'nin Dynamics 365 Supply Chain Management şirket içi dağıtımlarını desteklemediğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

## <a name="licensing"></a><span data-ttu-id="7c4dd-122">Lisans</span><span class="sxs-lookup"><span data-stu-id="7c4dd-122">Licensing</span></span>

<span data-ttu-id="7c4dd-123">Geçerli lisansınızı kullanarak master planlamayı çalıştırabilirseniz Planlamayı En İyi Duruma Getirme hizmetini kullanmaya başlamak için ek lisans satın almanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

## <a name="install-and-enable-planning-optimization"></a><span data-ttu-id="7c4dd-124">Planlamayı En İyi Duruma Getirmeyi yükleme ve etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7c4dd-124">Install and enable Planning Optimization</span></span>

<span data-ttu-id="7c4dd-125">Planlamayı En İyi Duruma Getirme'yi kullanmak için, sisteminizin tüm ön koşulları karşıladığından emin olmanız ve ardından lisans anahtarını etkinleştirip Dynamics 365 Supply Chain Management için Planlamayı En İyi Duruma Getirme Eklentisi'ni yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-125">To use Planning Optimization, you must make sure your system has all of the prerequisites in place and then enable its license key and install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7c4dd-126">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="7c4dd-126">Prerequisites</span></span>

<span data-ttu-id="7c4dd-127">Planlamayı En İyi Duruma Getirme Eklentisini yüklemeden önce aşağıdaki ön koşulların karşılanması gerekir:</span><span class="sxs-lookup"><span data-stu-id="7c4dd-127">Before you install the Planning Optimization Add-in, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="7c4dd-128">Supply Chain Management'da şurada çalıştırıyor olmanız gerekir: LCS etkin yüksek kullanılabilirlik ortamı, katman 2 veya üstü (OneBox ortamı değil); Dynamics 365 Supply Chain Management sürüm 10.0.7 veya sonraki bir sürüm.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-128">You must be running Supply Chain Management on an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="7c4dd-129">Eklentiyi OneBox ortamına yüklemeye çalışırsanız, yükleme tamamlanmaz ve yükleme işlemini iptal etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-129">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

- <span data-ttu-id="7c4dd-130">Sisteminiz, Power Platform tümleştirmesi için ayarlanmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-130">Your system must be set up for Power Platform integration.</span></span> <span data-ttu-id="7c4dd-131">Daha fazla bilgi için, bkz. [Finance and Operations uygulamaları ile Microsoft Power Platform tümleştirmesi.](../../../fin-ops-core/dev-itpro/power-platform/overview.md).</span><span class="sxs-lookup"><span data-stu-id="7c4dd-131">For more information, see [Microsoft Power Platform integration with Finance and Operations apps](../../../fin-ops-core/dev-itpro/power-platform/overview.md).</span></span>

### <a name="enable-the-planning-optimization-license"></a><span data-ttu-id="7c4dd-132">Planlamayı En İyi Duruma Getirme lisansını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7c4dd-132">Enable the Planning Optimization license</span></span>

<span data-ttu-id="7c4dd-133">Planlamayı En İyi Duruma Getirme eklentisini kullanabilmek için yapılandırma anahtarını etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-133">To use Planning Optimization, you must enable its configuration key.</span></span> <span data-ttu-id="7c4dd-134">Bunun için:</span><span class="sxs-lookup"><span data-stu-id="7c4dd-134">To do so:</span></span>

1. <span data-ttu-id="7c4dd-135">Sisteminizi [Bakım modu](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) bölümünde anlatıldığı şekilde bakım moduna alın.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-135">Put your system into maintenance mode, as described in [Maintenance mode](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="7c4dd-136">**Sistem yönetimi \> Kurulum \> Lisans yapılandırma** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-136">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="7c4dd-137">**Yapılandırma anahtarları** sekmesinde, **Planlamayı En İyi Duruma Getirme** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-137">On the **Configuration keys** tab, select the check box for **Planning Optimization**.</span></span>
1. <span data-ttu-id="7c4dd-138">[Bakım modu](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) bölümünde anlatıldığı şekilde bakım modunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-138">Turn off maintenance mode, as described in [Maintenance mode](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

### <a name="install-the-planning-optimization-add-in"></a><span data-ttu-id="7c4dd-139">Planlamayı En İyi Duruma Getirme Eklentisini Yükleme</span><span class="sxs-lookup"><span data-stu-id="7c4dd-139">Install the Planning Optimization Add-in</span></span>

<span data-ttu-id="7c4dd-140">Eklentiyi LCS projenizden yüklemeniz ve Supply Chain Management kullanıcı arabiriminden Planlamayı En İyi Duruma Getirme işlevini açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-140">You must install the add-in from your LCS project and then turn on the Planning Optimization functionality from the Supply Chain Management user interface.</span></span>

<span data-ttu-id="7c4dd-141">Planlamayı En İyi Duruma Getirme Eklentisini yüklemek için:</span><span class="sxs-lookup"><span data-stu-id="7c4dd-141">To install the Planning Optimization Add-in:</span></span>

1. <span data-ttu-id="7c4dd-142">LCS'de oturum açın ve istediğiniz ortamı açın.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-142">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="7c4dd-143">**Tüm ayrıntılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-143">Go to **Full details**.</span></span>
1. <span data-ttu-id="7c4dd-144">**Ortam eklentileri** hızlı sekmesinde aşağı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-144">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="7c4dd-145">**Yeni eklenti yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-145">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="7c4dd-146">**Planlamayı En İyi Duruma Getirme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-146">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="7c4dd-147">Yükleme kılavuzunu izleyin ve hüküm ve koşulları kabul edin.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-147">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="7c4dd-148">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-148">Select **Install**.</span></span>
1. <span data-ttu-id="7c4dd-149">**Ortam eklentileri** hızlı sekmesinde, Planlamayı En İyi Duruma Getirme'nin yüklendiğini görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-149">On the **Environment add-ins** FastTab, you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="7c4dd-150">Birkaç dakika sonra **Yükleniyor** durumu **Yüklendi** olarak değişecektir (sayfayı yenilemeniz gerekebilir).</span><span class="sxs-lookup"><span data-stu-id="7c4dd-150">After a few minutes, **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="7c4dd-151">Yüklendiğinde, Planlamayı En İyi Duruma Getirme'yi Dynamics 365 Supply Chain Management'ta etkinleştirmeye hazırsınız demektir.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-151">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="7c4dd-152">Planlamayı En İyi Duruma Getirme Eklentisini yüklemenin temel amacı, hizmet ile ortamı bağlamaktır.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-152">The main purpose of installing the Planning Optimization Add-in is to connect the service and the environment.</span></span> <span data-ttu-id="7c4dd-153">Bu nedenle, ortamlar arasına taşınacak kod ne olursa olsun, eklentiyi, Planlama İyileştirmesi'ni kullanacağınız her ortama ayrı ayrı yüklemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-153">Therefore, you must install the add-in separately on each environment where you will use Planning Optimization, regardless of any code moved between the environments.</span></span>

## <a name="integrate-planning-optimization-with-your-system"></a><span data-ttu-id="7c4dd-154">Planlamayı En İyi Duruma Getirme ile sisteminizi tümleştirme</span><span class="sxs-lookup"><span data-stu-id="7c4dd-154">Integrate Planning Optimization with your system</span></span>

<span data-ttu-id="7c4dd-155">Planlamayı En İyi Duruma Getirme eklentisinin master planlama için kullanılması gerekip gerekmediğini yapılandırmak üzere **Master planlama** \> **Ayar** \> **Planlamayı En İyi Duruma Getirme parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-155">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

### <a name="connection-status"></a><span data-ttu-id="7c4dd-156">Bağlantı durumu</span><span class="sxs-lookup"><span data-stu-id="7c4dd-156">Connection status</span></span>

<span data-ttu-id="7c4dd-157">Bağlantı durumu, Supply Chain Management ile Planlamayı En İyi Duruma Getirme hizmeti arasındaki bağlantının geçerli durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-157">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="7c4dd-158">Aşağıdaki tabloda, olası değerler gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-158">The following table shows the possible values.</span></span>

| <span data-ttu-id="7c4dd-159">Bağlantı durumu</span><span class="sxs-lookup"><span data-stu-id="7c4dd-159">Connection status</span></span> | <span data-ttu-id="7c4dd-160">Tanım</span><span class="sxs-lookup"><span data-stu-id="7c4dd-160">Description</span></span> | <span data-ttu-id="7c4dd-161">Planlamayı En İyi Duruma Getirme kullanılabilir mi?</span><span class="sxs-lookup"><span data-stu-id="7c4dd-161">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="7c4dd-162">Bağlı</span><span class="sxs-lookup"><span data-stu-id="7c4dd-162">Connected</span></span> | <span data-ttu-id="7c4dd-163">Planlamayı En İyi Duruma Getirme hizmeti ile Supply Chain Management arasında bir bağlantı oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-163">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="7c4dd-164">Evet</span><span class="sxs-lookup"><span data-stu-id="7c4dd-164">Yes</span></span> |
| <span data-ttu-id="7c4dd-165">Bağlantı etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="7c4dd-165">Enabling connection</span></span> | <span data-ttu-id="7c4dd-166">Planlamayı En İyi Duruma Getirme hizmeti için bağlantıyı açma isteği şu anda devam ediyor.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-166">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="7c4dd-167">Hayır</span><span class="sxs-lookup"><span data-stu-id="7c4dd-167">No</span></span> |
| <span data-ttu-id="7c4dd-168">Bağlantı kesildi</span><span class="sxs-lookup"><span data-stu-id="7c4dd-168">Disconnected</span></span> | <span data-ttu-id="7c4dd-169">Planlamayı En İyi Duruma Getirme hizmeti için bağlantı mevcut değil.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-169">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="7c4dd-170">Bağlantı, bu konuda daha önce açıklandığı gibi LCS'den açılabilir.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-170">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="7c4dd-171">Hayır</span><span class="sxs-lookup"><span data-stu-id="7c4dd-171">No</span></span> |
| <span data-ttu-id="7c4dd-172">Bağlantı devre dışı bırakılıyor</span><span class="sxs-lookup"><span data-stu-id="7c4dd-172">Disabling connection</span></span> | <span data-ttu-id="7c4dd-173">Planlamayı En İyi Duruma Getirme hizmeti için bağlantıyı kapatma isteği şu anda devam ediyor.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-173">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="7c4dd-174">Hayır</span><span class="sxs-lookup"><span data-stu-id="7c4dd-174">No</span></span> |
| <span data-ttu-id="7c4dd-175">Durum alınıyor</span><span class="sxs-lookup"><span data-stu-id="7c4dd-175">Getting status</span></span> | <span data-ttu-id="7c4dd-176">Sistem, Planlamayı En İyi Duruma Getirme hizmetinden durum bilgisi bekliyor.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-176">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="7c4dd-177">Hayır</span><span class="sxs-lookup"><span data-stu-id="7c4dd-177">No</span></span> |

### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="7c4dd-178">Planlamayı En İyi Duruma Getirmeyi Kullan seçeneği</span><span class="sxs-lookup"><span data-stu-id="7c4dd-178">The Use Planning Optimization option</span></span>

<span data-ttu-id="7c4dd-179">**Planlamayı En İyi Duruma Getirmeyi Kullan** seçeneği, master planlama için hangi planlama altyapısının kullanılacağını belirler:</span><span class="sxs-lookup"><span data-stu-id="7c4dd-179">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="7c4dd-180">**Evet**: Master planlama için Planlamayı En İyi Duruma Getirme hizmeti kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-180">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="7c4dd-181">**Hayır**: Master planlama için yerleşik Supply Chain Management planlama altyapısı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-181">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

<span data-ttu-id="7c4dd-182">Bu ayar tüm tüzel kişilikler (şirketler) için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-182">This setting applies to all legal entities (companies).</span></span> <span data-ttu-id="7c4dd-183">Planlamayı En İyi Duruma Getirme bazı tüzel kişiliklerde mümkün değildir. Bazı tüzel kişiliklerde ise master planlama kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-183">It is not possible to use Planning Optimization in some legal entities and the built-in master planning in other legal entities.</span></span>

> [!NOTE]
> <span data-ttu-id="7c4dd-184">Yerleşik Supply Chain Management planlama altyapısı için oluşturulan mevcut planlama toplu işleri, **Planlamayı En İyi Duruma Getirmeyi Kullan** seçeneği **Evet** olarak ayarlanırken tetiklenirse bu işler başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-184">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="7c4dd-185">Ayarla tümleştirme</span><span class="sxs-lookup"><span data-stu-id="7c4dd-185">Integration with the setup</span></span>

<span data-ttu-id="7c4dd-186">Planlama İyileştirmesi açıksa master planlama, Planlama İyileştirmesi Eklentisi'ni kullanarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-186">If the Planning Optimization is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="7c4dd-187">Bu durumda, master planlama sonuçları ve özellikleri etkilenir.</span><span class="sxs-lookup"><span data-stu-id="7c4dd-187">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c4dd-188">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7c4dd-188">Additional resources</span></span>

[<span data-ttu-id="7c4dd-189">Önizleme için hüküm ve koşullar</span><span class="sxs-lookup"><span data-stu-id="7c4dd-189">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="7c4dd-190">Planlamayı En İyi Duruma Getirmeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="7c4dd-190">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="7c4dd-191">Planlamayı En İyi Duruma Getirme uygunluk analizi</span><span class="sxs-lookup"><span data-stu-id="7c4dd-191">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="7c4dd-192">Plan geçmişini ve planlama günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="7c4dd-192">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="7c4dd-193">Plana filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="7c4dd-193">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="7c4dd-194">Planlama işini iptal etme</span><span class="sxs-lookup"><span data-stu-id="7c4dd-194">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
