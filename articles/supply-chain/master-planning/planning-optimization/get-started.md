---
title: Planlamayı En İyi Duruma Getirmeye başlayın
description: Bu konuda, Planlamayı En İyi Duruma Getirme işlevini kullanmaya nasıl başlanacağı açıklanmaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 49025d0aa0f6a627b816a43dd4260449942b400c
ms.sourcegitcommit: ae04c7cb48f7ecafe71bbe77a0f97715e6290991
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973488"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="b10ce-103">Planlamayı En İyi Duruma Getirmeyi kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="b10ce-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b10ce-104">[Daha önce duyurulduğu](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios) gibi, Planlamayı En İyi Duruma Getirme varolan yerleşik master planlama altyapısının yerini almak üzere planlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="b10ce-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="b10ce-105">Yerleşik Master planlama altyapısını kullanıyorsanız, şimdi Planlamayı En İyi Duruma Getirme için geçişinizi planlamaya başlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b10ce-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="b10ce-106">Yükseltme işlemi zorlandığında işlemleriniz etkilenebileceğinden, geçiş işlemini hemen başlatmak önemlidir.</span><span class="sxs-lookup"><span data-stu-id="b10ce-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="b10ce-107">Kullanımdan kaldırma zorunlu olduğunda yaşanacak son dakika sorunlarını önlemek için geçişi 1 Aralık 2020'den önce tamamlamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="b10ce-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="b10ce-108">Planlamayı En İyi Duruma Getirme işlevi şu anda Microsoft Supply Chain Management'ta yerleşik olan planlama altyapısında kullanılabilen tüm özellikleri desteklememektedir.</span><span class="sxs-lookup"><span data-stu-id="b10ce-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="b10ce-109">Bu nedenle, Planlamayı En İyi Duruma Getirme hizmetinde şu anda mevcut olan özellik kümesinin gereksinimlerinizi karşılayıp karşılamadığını değerlendirmeniz önemlidir.</span><span class="sxs-lookup"><span data-stu-id="b10ce-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="b10ce-110">Planlamayı En İyi Duruma Getirme işlevi şu anda Dynamics Lifecycle Services (LCS)'de varsayılan olarak etkin değil; bu nedenle özellik açılmadan önce değerlendirme yapma fırsatına sahipsiniz.</span><span class="sxs-lookup"><span data-stu-id="b10ce-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="b10ce-111">Master planlama işleminiz üretim (Master planlamayla oluşturulmuş planlanmış üretim emirleri) içermiyorsa ve yerleşik Master planlama altyapısının 10.0.15 üstü sürümü olmasını istiyorsanız, Planlamayı En İyi Duruma Getirme işlevine geçiş için bir özel durum istemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b10ce-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="b10ce-112">Sürüm 10.0.16 itibarıyla, planlı üretim emirleri olmadan yerleşik master planlama çalıştırıldığında ortamlarda bir hata gösterilecektir.</span><span class="sxs-lookup"><span data-stu-id="b10ce-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="b10ce-113">Master planlama sırasında planlı üretim emirleri oluşturmayan tüm yeni dağıtımlar için Planlamayı En İyi Duruma Getirme işlevi kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b10ce-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="b10ce-114">Planlı üretim emirleri olmadan Yerleşik Master planlama altyapısını çalıştıran mevcut ortamların sahipleri, özel durum işlemiyle ilgili ayrıntıların bulunduğu bir posta alacaktır.</span><span class="sxs-lookup"><span data-stu-id="b10ce-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="b10ce-115">Planlamayı En İyi Duruma Getirme için geçişi değerlendirmek ve planlamak üzere bir iş ortağı ile çalışmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="b10ce-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="b10ce-116">Planlamayı En İyi Duruma Getirme hizmetini açmadan önce Planlamayı En İyi Duruma Getirme uygunluk analizinin sonuçlarını değerlendirmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="b10ce-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="b10ce-117">Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b10ce-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="b10ce-118">Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="b10ce-118">Availability</span></span>
<span data-ttu-id="b10ce-119">Planlamayı En İyi Duruma Getirme şu anda şu Azure coğrafi bölgelerinde kullanılabilir: Amerika Birleşik Devletleri, Kanada, Avrupa, Birleşik Krallık ve Avustralya.</span><span class="sxs-lookup"><span data-stu-id="b10ce-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="b10ce-120">Eklentiyi başka bir coğrafi bölgeden yüklemeye çalışırsanız, LCS bu coğrafi bölgenin desteklenmediğini belirten bir ileti gösterir.</span><span class="sxs-lookup"><span data-stu-id="b10ce-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="b10ce-121">Planlamayı En İyi Duruma Getirme'nin Dynamics 365 Supply Chain Management şirket içi dağıtımlarını desteklemediğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="b10ce-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="b10ce-122">Lisans</span><span class="sxs-lookup"><span data-stu-id="b10ce-122">Licensing</span></span>

<span data-ttu-id="b10ce-123">Geçerli lisansınızı kullanarak master planlamayı çalıştırabilirseniz Planlamayı En İyi Duruma Getirme hizmetini kullanmaya başlamak için ek lisans satın almanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="b10ce-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="b10ce-124">Eklentiyi yükleme</span><span class="sxs-lookup"><span data-stu-id="b10ce-124">Install the add-in</span></span>

<span data-ttu-id="b10ce-125">Planlamayı En İyi Duruma Getirme hizmetini kullanmak üzere Dynamics 365 Supply Chain Management için Planlamayı En İyi Duruma Getirme Eklentisi'ni yükleyin.</span><span class="sxs-lookup"><span data-stu-id="b10ce-125">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="b10ce-126">Eklentiye LCS projenizden ulaşabilir ve Supply Chain Management kullanıcı arabiriminden (UI) Planlamayı En İyi Duruma Getirme hizmetini açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b10ce-126">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="b10ce-127">Planlamayı En İyi Duruma Getirme için gereksinim, bir LCS etkin yüksek kullanılabilirlik ortamı, katman 2 veya üstüdür (OneBox ortamı değil); Dynamics 365 Supply Chain Management sürüm 10.0.7 veya daha yenisine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b10ce-127">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="b10ce-128">Eklentiyi OneBox ortamına yüklemeye çalışırsanız, yükleme tamamlanmaz ve yükleme işlemini iptal etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b10ce-128">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="b10ce-129">LCS'de oturum açın ve istediğiniz ortamı açın.</span><span class="sxs-lookup"><span data-stu-id="b10ce-129">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="b10ce-130">**Tüm ayrıntılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="b10ce-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="b10ce-131">**Ortam eklentileri** hızlı sekmesinde aşağı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="b10ce-131">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="b10ce-132">**Yeni eklenti yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b10ce-132">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="b10ce-133">**Planlamayı En İyi Duruma Getirme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b10ce-133">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="b10ce-134">Yükleme kılavuzunu izleyin ve hüküm ve koşulları kabul edin.</span><span class="sxs-lookup"><span data-stu-id="b10ce-134">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="b10ce-135">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b10ce-135">Select **Install**.</span></span>
1. <span data-ttu-id="b10ce-136">**Ortam eklentileri** hızlı sekmesinde, Planlamayı En İyi Duruma Getirme'nin yüklendiğin görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b10ce-136">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="b10ce-137">Birkaç dakika sonra **Yükleme** durumunun değişip **Yüklendi**olarak değişecektir (sayfayı yenilemeniz gerekebilir).</span><span class="sxs-lookup"><span data-stu-id="b10ce-137">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="b10ce-138">Yüklendiğinde, Planlamayı En İyi Duruma Getirme'yi Dynamics 365 Supply Chain Management'ta etkinleştirmeye hazırsınız demektir.</span><span class="sxs-lookup"><span data-stu-id="b10ce-138">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="b10ce-139">Planlamayı En İyi Duruma Getirme tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="b10ce-139">Planning Optimization integration</span></span>

<span data-ttu-id="b10ce-140">Planlamayı En İyi Duruma Getirme eklentisinin master planlama için kullanılması gerekip gerekmediğini yapılandırmak üzere **Master planlama** \> **Ayar** \> **Planlamayı En İyi Duruma Getirme parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b10ce-140">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="b10ce-141">Bağlantı durumu</span><span class="sxs-lookup"><span data-stu-id="b10ce-141">Connection status</span></span>

<span data-ttu-id="b10ce-142">Bağlantı durumu, Supply Chain Management ile Planlamayı En İyi Duruma Getirme hizmeti arasındaki bağlantının geçerli durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b10ce-142">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="b10ce-143">Aşağıdaki tabloda, olası değerler gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b10ce-143">The following table shows the possible values.</span></span>

| <span data-ttu-id="b10ce-144">Bağlantı durumu</span><span class="sxs-lookup"><span data-stu-id="b10ce-144">Connection status</span></span> | <span data-ttu-id="b10ce-145">Tanım</span><span class="sxs-lookup"><span data-stu-id="b10ce-145">Description</span></span> | <span data-ttu-id="b10ce-146">Planlamayı En İyi Duruma Getirme kullanılabilir mi?</span><span class="sxs-lookup"><span data-stu-id="b10ce-146">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="b10ce-147">Bağlı</span><span class="sxs-lookup"><span data-stu-id="b10ce-147">Connected</span></span> | <span data-ttu-id="b10ce-148">Planlamayı En İyi Duruma Getirme hizmeti ile Supply Chain Management arasında bir bağlantı oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="b10ce-148">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="b10ce-149">Evet</span><span class="sxs-lookup"><span data-stu-id="b10ce-149">Yes</span></span> |
| <span data-ttu-id="b10ce-150">Bağlantı etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="b10ce-150">Enabling connection</span></span> | <span data-ttu-id="b10ce-151">Planlamayı En İyi Duruma Getirme hizmeti için bağlantıyı açma isteği şu anda devam ediyor.</span><span class="sxs-lookup"><span data-stu-id="b10ce-151">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="b10ce-152">Hayır</span><span class="sxs-lookup"><span data-stu-id="b10ce-152">No</span></span> |
| <span data-ttu-id="b10ce-153">Bağlantı kesildi</span><span class="sxs-lookup"><span data-stu-id="b10ce-153">Disconnected</span></span> | <span data-ttu-id="b10ce-154">Planlamayı En İyi Duruma Getirme hizmeti için bağlantı mevcut değil.</span><span class="sxs-lookup"><span data-stu-id="b10ce-154">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="b10ce-155">Bağlantı, bu konuda daha önce açıklandığı gibi LCS'den açılabilir.</span><span class="sxs-lookup"><span data-stu-id="b10ce-155">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="b10ce-156">Hayır</span><span class="sxs-lookup"><span data-stu-id="b10ce-156">No</span></span> |
| <span data-ttu-id="b10ce-157">Bağlantı devre dışı bırakılıyor</span><span class="sxs-lookup"><span data-stu-id="b10ce-157">Disabling connection</span></span> | <span data-ttu-id="b10ce-158">Planlamayı En İyi Duruma Getirme hizmeti için bağlantıyı kapatma isteği şu anda devam ediyor.</span><span class="sxs-lookup"><span data-stu-id="b10ce-158">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="b10ce-159">Hayır</span><span class="sxs-lookup"><span data-stu-id="b10ce-159">No</span></span> |
| <span data-ttu-id="b10ce-160">Durum alınıyor</span><span class="sxs-lookup"><span data-stu-id="b10ce-160">Getting status</span></span> | <span data-ttu-id="b10ce-161">Sistem, Planlamayı En İyi Duruma Getirme hizmetinden durum bilgisi bekliyor.</span><span class="sxs-lookup"><span data-stu-id="b10ce-161">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="b10ce-162">Hayır</span><span class="sxs-lookup"><span data-stu-id="b10ce-162">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="b10ce-163">Planlamayı En İyi Duruma Getirmeyi Kullan seçeneği</span><span class="sxs-lookup"><span data-stu-id="b10ce-163">The Use Planning Optimization option</span></span>

<span data-ttu-id="b10ce-164">**Planlamayı En İyi Duruma Getirmeyi Kullan** seçeneği, master planlama için hangi planlama altyapısının kullanılacağını belirler:</span><span class="sxs-lookup"><span data-stu-id="b10ce-164">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="b10ce-165">**Evet**: Master planlama için Planlamayı En İyi Duruma Getirme hizmeti kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b10ce-165">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="b10ce-166">**Hayır**: Master planlama için yerleşik Supply Chain Management planlama altyapısı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b10ce-166">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="b10ce-167">Yerleşik Supply Chain Management planlama altyapısı için oluşturulan mevcut planlama toplu işleri, **Planlamayı En İyi Duruma Getirmeyi Kullan** seçeneği **Evet** olarak ayarlanırken tetiklenirse bu işler başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="b10ce-167">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="b10ce-168">Ayarla tümleştirme</span><span class="sxs-lookup"><span data-stu-id="b10ce-168">Integration with the setup</span></span>

<span data-ttu-id="b10ce-169">Planlamayı En İyi Duruma Getirme önizlemesi açıksa master planlama, Planlamayı En İyi Duruma Getirme Eklentisi'ni kullanarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="b10ce-169">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="b10ce-170">Bu durumda, master planlama sonuçları ve özellikleri etkilenir.</span><span class="sxs-lookup"><span data-stu-id="b10ce-170">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b10ce-171">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b10ce-171">Additional resources</span></span>

[<span data-ttu-id="b10ce-172">Önizleme için hüküm ve koşullar</span><span class="sxs-lookup"><span data-stu-id="b10ce-172">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="b10ce-173">Planlamayı En İyi Duruma Getirmeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="b10ce-173">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="b10ce-174">Planlamayı En İyi Duruma Getirme uygunluk analizi</span><span class="sxs-lookup"><span data-stu-id="b10ce-174">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="b10ce-175">Plan geçmişini ve planlama günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="b10ce-175">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="b10ce-176">Plana filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="b10ce-176">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="b10ce-177">Planlama işini iptal etme</span><span class="sxs-lookup"><span data-stu-id="b10ce-177">Cancel a planning job</span></span>](cancel-planning-job.md)
