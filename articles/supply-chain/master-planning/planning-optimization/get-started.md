---
title: Planlamayı En İyi Duruma Getirmeye başlayın
description: Bu konuda, Planlamayı En İyi Duruma Getirme işlevini kullanmaya nasıl başlanacağı açıklanmaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 05/06/2020
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
ms.openlocfilehash: 04b39469ccf4f088bb33bdfc73ce40eece6f5f2e
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2020
ms.locfileid: "3887276"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="af700-103">Planlamayı En İyi Duruma Getirmeye başlayın</span><span class="sxs-lookup"><span data-stu-id="af700-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="af700-104">Planlamayı En İyi Duruma Getirme işlevi şu anda Microsoft Dynamics 365 Supply Chain Management'ta yerleşik olan planlama altyapısında kullanılabilen tüm özellikleri desteklememektedir.</span><span class="sxs-lookup"><span data-stu-id="af700-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="af700-105">Bu nedenle, Planlamayı En İyi Duruma Getirme hizmetinde şu anda mevcut olan özellik kümesinin gereksinimlerinizi karşılayıp karşılamadığını değerlendirmeniz önemlidir.</span><span class="sxs-lookup"><span data-stu-id="af700-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="af700-106">Varsayılan olarak, Planlamayı En İyi Duruma Getirme işlevi Dynamics Lifecycle Services'ta (LCS) açılmaz.</span><span class="sxs-lookup"><span data-stu-id="af700-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="af700-107">Bu nedenle, açılmadan önce değerlendirme yapma fırsatınız vardır.</span><span class="sxs-lookup"><span data-stu-id="af700-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="af700-108">Sonuç olarak, Planlamayı En İyi Duruma Getirme hizmeti var olan yerleşik Supply Chain Management planlama altyapısının yerini alacaktır.</span><span class="sxs-lookup"><span data-stu-id="af700-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="af700-109">Planlamayı En İyi Duruma Getirme hizmetini açmadan önce Planlamayı En İyi Duruma Getirme uygunluk analizinin sonuçlarını değerlendirmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="af700-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="af700-110">Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="af700-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="af700-111">Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="af700-111">Availability</span></span>
<span data-ttu-id="af700-112">Planlamayı En İyi Duruma Getirme şu anda şu Azure coğrafi bölgelerinde kullanılabilir: Amerika Birleşik Devletleri, Kanada, Avrupa, Birleşik Krallık ve Avustralya.</span><span class="sxs-lookup"><span data-stu-id="af700-112">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="af700-113">Eklentiyi başka bir coğrafi bölgeden yüklemeye çalışırsanız, LCS bu coğrafi bölgenin desteklenmediğini belirten bir ileti gösterir.</span><span class="sxs-lookup"><span data-stu-id="af700-113">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="af700-114">Planlamayı En İyi Duruma Getirme'nin Dynamics 365 Supply Chain Management şirket içi dağıtımlarını desteklemediğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="af700-114">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="af700-115">Lisans</span><span class="sxs-lookup"><span data-stu-id="af700-115">Licensing</span></span>

<span data-ttu-id="af700-116">Geçerli lisansınızı kullanarak master planlamayı çalıştırabilirseniz Planlamayı En İyi Duruma Getirme hizmetini kullanmaya başlamak için ek lisans satın almanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="af700-116">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="af700-117">Eklentiyi yükleme</span><span class="sxs-lookup"><span data-stu-id="af700-117">Install the add-in</span></span>

<span data-ttu-id="af700-118">Planlamayı En İyi Duruma Getirme hizmetini kullanmak üzere Dynamics 365 Supply Chain Management için Planlamayı En İyi Duruma Getirme Eklentisi'ni yükleyin.</span><span class="sxs-lookup"><span data-stu-id="af700-118">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="af700-119">Eklentiye LCS projenizden ulaşabilir ve Supply Chain Management kullanıcı arabiriminden (UI) Planlamayı En İyi Duruma Getirme hizmetini açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af700-119">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="af700-120">Planlamayı En İyi Duruma Getirme için gereksinim, bir LCS etkin yüksek kullanılabilirlik ortamı, katman 2 veya üstüdür (OneBox ortamı değil); Dynamics 365 Supply Chain Management sürüm 10.0.7 veya daha yenisine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="af700-120">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="af700-121">Eklentiyi OneBox ortamına yüklemeye çalışırsanız, yükleme tamamlanmaz ve yükleme işlemini iptal etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="af700-121">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="af700-122">LCS'de oturum açın ve istediğiniz ortamı açın.</span><span class="sxs-lookup"><span data-stu-id="af700-122">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="af700-123">**Tüm ayrıntılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="af700-123">Go to **Full details**.</span></span>
1. <span data-ttu-id="af700-124">**Ortam eklentileri** hızlı sekmesinde aşağı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="af700-124">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="af700-125">**Yeni eklenti yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="af700-125">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="af700-126">**Planlamayı En İyi Duruma Getirme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="af700-126">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="af700-127">Yükleme kılavuzunu izleyin ve hüküm ve koşulları kabul edin.</span><span class="sxs-lookup"><span data-stu-id="af700-127">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="af700-128">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="af700-128">Select **Install**.</span></span>
1. <span data-ttu-id="af700-129">**Ortam eklentileri** hızlı sekmesinde, Planlamayı En İyi Duruma Getirme'nin yüklendiğin görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="af700-129">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="af700-130">Birkaç dakika sonra **Yükleme** durumunun değişip **Yüklendi**olarak değişecektir (sayfayı yenilemeniz gerekebilir).</span><span class="sxs-lookup"><span data-stu-id="af700-130">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="af700-131">Yüklendiğinde, Planlamayı En İyi Duruma Getirme'yi Dynamics 365 Supply Chain Management'ta etkinleştirmeye hazırsınız demektir.</span><span class="sxs-lookup"><span data-stu-id="af700-131">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="af700-132">Planlamayı En İyi Duruma Getirme tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="af700-132">Planning Optimization integration</span></span>

<span data-ttu-id="af700-133">Planlamayı En İyi Duruma Getirme eklentisinin master planlama için kullanılması gerekip gerekmediğini yapılandırmak üzere **Master planlama** \> **Ayar** \> **Planlamayı En İyi Duruma Getirme parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="af700-133">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="af700-134">Bağlantı durumu</span><span class="sxs-lookup"><span data-stu-id="af700-134">Connection status</span></span>

<span data-ttu-id="af700-135">Bağlantı durumu, Supply Chain Management ile Planlamayı En İyi Duruma Getirme hizmeti arasındaki bağlantının geçerli durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="af700-135">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="af700-136">Aşağıdaki tabloda, olası değerler gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="af700-136">The following table shows the possible values.</span></span>

| <span data-ttu-id="af700-137">Bağlantı durumu</span><span class="sxs-lookup"><span data-stu-id="af700-137">Connection status</span></span> | <span data-ttu-id="af700-138">Tanım</span><span class="sxs-lookup"><span data-stu-id="af700-138">Description</span></span> | <span data-ttu-id="af700-139">Planlamayı En İyi Duruma Getirme kullanılabilir mi?</span><span class="sxs-lookup"><span data-stu-id="af700-139">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="af700-140">Bağlı</span><span class="sxs-lookup"><span data-stu-id="af700-140">Connected</span></span> | <span data-ttu-id="af700-141">Planlamayı En İyi Duruma Getirme hizmeti ile Supply Chain Management arasında bir bağlantı oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="af700-141">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="af700-142">Evet</span><span class="sxs-lookup"><span data-stu-id="af700-142">Yes</span></span> |
| <span data-ttu-id="af700-143">Bağlantı etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="af700-143">Enabling connection</span></span> | <span data-ttu-id="af700-144">Planlamayı En İyi Duruma Getirme hizmeti için bağlantıyı açma isteği şu anda devam ediyor.</span><span class="sxs-lookup"><span data-stu-id="af700-144">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="af700-145">Hayır</span><span class="sxs-lookup"><span data-stu-id="af700-145">No</span></span> |
| <span data-ttu-id="af700-146">Bağlantı kesildi</span><span class="sxs-lookup"><span data-stu-id="af700-146">Disconnected</span></span> | <span data-ttu-id="af700-147">Planlamayı En İyi Duruma Getirme hizmeti için bağlantı mevcut değil.</span><span class="sxs-lookup"><span data-stu-id="af700-147">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="af700-148">Bağlantı, bu konuda daha önce açıklandığı gibi LCS'den açılabilir.</span><span class="sxs-lookup"><span data-stu-id="af700-148">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="af700-149">Hayır</span><span class="sxs-lookup"><span data-stu-id="af700-149">No</span></span> |
| <span data-ttu-id="af700-150">Bağlantı devre dışı bırakılıyor</span><span class="sxs-lookup"><span data-stu-id="af700-150">Disabling connection</span></span> | <span data-ttu-id="af700-151">Planlamayı En İyi Duruma Getirme hizmeti için bağlantıyı kapatma isteği şu anda devam ediyor.</span><span class="sxs-lookup"><span data-stu-id="af700-151">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="af700-152">Hayır</span><span class="sxs-lookup"><span data-stu-id="af700-152">No</span></span> |
| <span data-ttu-id="af700-153">Durum alınıyor</span><span class="sxs-lookup"><span data-stu-id="af700-153">Getting status</span></span> | <span data-ttu-id="af700-154">Sistem, Planlamayı En İyi Duruma Getirme hizmetinden durum bilgisi bekliyor.</span><span class="sxs-lookup"><span data-stu-id="af700-154">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="af700-155">Hayır</span><span class="sxs-lookup"><span data-stu-id="af700-155">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="af700-156">Planlamayı En İyi Duruma Getirmeyi Kullan seçeneği</span><span class="sxs-lookup"><span data-stu-id="af700-156">The Use Planning Optimization option</span></span>

<span data-ttu-id="af700-157">**Planlamayı En İyi Duruma Getirmeyi Kullan** seçeneği, master planlama için hangi planlama altyapısının kullanılacağını belirler:</span><span class="sxs-lookup"><span data-stu-id="af700-157">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="af700-158">**Evet**: Master planlama için Planlamayı En İyi Duruma Getirme hizmeti kullanılır.</span><span class="sxs-lookup"><span data-stu-id="af700-158">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="af700-159">**Hayır**: Master planlama için yerleşik Supply Chain Management planlama altyapısı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="af700-159">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="af700-160">Yerleşik Supply Chain Management planlama altyapısı için oluşturulan mevcut planlama toplu işleri, **Planlamayı En İyi Duruma Getirmeyi Kullan** seçeneği **Evet** olarak ayarlanırken tetiklenirse bu işler başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="af700-160">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="af700-161">Ayarla tümleştirme</span><span class="sxs-lookup"><span data-stu-id="af700-161">Integration with the setup</span></span>

<span data-ttu-id="af700-162">Planlamayı En İyi Duruma Getirme önizlemesi açıksa master planlama, Planlamayı En İyi Duruma Getirme Eklentisi'ni kullanarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="af700-162">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="af700-163">Bu durumda, master planlama sonuçları ve özellikleri etkilenir.</span><span class="sxs-lookup"><span data-stu-id="af700-163">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="af700-164">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="af700-164">Additional resources</span></span>

[<span data-ttu-id="af700-165">Önizleme için hüküm ve koşullar</span><span class="sxs-lookup"><span data-stu-id="af700-165">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="af700-166">Planlamayı En İyi Duruma Getirmeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="af700-166">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="af700-167">Planlamayı En İyi Duruma Getirme uygunluk analizi</span><span class="sxs-lookup"><span data-stu-id="af700-167">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="af700-168">Plan geçmişini ve planlama günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="af700-168">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="af700-169">Plana filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="af700-169">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="af700-170">Planlama işini iptal etme</span><span class="sxs-lookup"><span data-stu-id="af700-170">Cancel a planning job</span></span>](cancel-planning-job.md)
