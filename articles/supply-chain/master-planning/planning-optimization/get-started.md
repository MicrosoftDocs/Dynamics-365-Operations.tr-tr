---
title: Planlamayı En İyi Duruma Getirmeye başlayın
description: Bu konuda, Planlamayı En İyi Duruma Getirme işlevini kullanmaya nasıl başlanacağı açıklanmaktadır.
author: ChristianRytt
manager: AnnBe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 3e64699005387adcc92e2e7c9fefad68a9de85c0
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076144"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="76800-103">Planlamayı En İyi Duruma Getirmeye başlayın</span><span class="sxs-lookup"><span data-stu-id="76800-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="76800-104">Planlamayı En İyi Duruma Getirme işlevi şu anda Microsoft Dynamics 365 Supply Chain Management'ta yerleşik olan planlama altyapısında kullanılabilen tüm özellikleri desteklememektedir.</span><span class="sxs-lookup"><span data-stu-id="76800-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="76800-105">Bu nedenle, Planlamayı En İyi Duruma Getirme hizmetinde şu anda mevcut olan özellik kümesinin gereksinimlerinizi karşılayıp karşılamadığını değerlendirmeniz önemlidir.</span><span class="sxs-lookup"><span data-stu-id="76800-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="76800-106">Varsayılan olarak, Planlamayı En İyi Duruma Getirme işlevi Dynamics Lifecycle Services'ta (LCS) açılmaz.</span><span class="sxs-lookup"><span data-stu-id="76800-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="76800-107">Bu nedenle, açılmadan önce değerlendirme yapma fırsatınız vardır.</span><span class="sxs-lookup"><span data-stu-id="76800-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="76800-108">Sonuç olarak, Planlamayı En İyi Duruma Getirme hizmeti var olan yerleşik Supply Chain Management planlama altyapısının yerini alacaktır.</span><span class="sxs-lookup"><span data-stu-id="76800-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="76800-109">Planlamayı En İyi Duruma Getirme hizmetini açmadan önce Planlamayı En İyi Duruma Getirme uygunluk analizinin sonuçlarını değerlendirmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="76800-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="76800-110">Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="76800-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="76800-111">Lisans</span><span class="sxs-lookup"><span data-stu-id="76800-111">Licensing</span></span>

<span data-ttu-id="76800-112">Geçerli lisansınızı kullanarak master planlamayı çalıştırabilirseniz Planlamayı En İyi Duruma Getirme hizmetini kullanmaya başlamak için ek lisans satın almanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="76800-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="76800-113">Eklentiyi yükleme</span><span class="sxs-lookup"><span data-stu-id="76800-113">Install the add-in</span></span>

<span data-ttu-id="76800-114">Planlamayı En İyi Duruma Getirme hizmetini kullanmak üzere Dynamics 365 Supply Chain Management için Planlamayı En İyi Duruma Getirme Eklentisi'ni yükleyin.</span><span class="sxs-lookup"><span data-stu-id="76800-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="76800-115">Eklentiye LCS projenizden ulaşabilir ve Supply Chain Management kullanıcı arabiriminden (UI) Planlamayı En İyi Duruma Getirme hizmetini açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="76800-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="76800-116">En iyi duruma getirme planlaması için gereksinim, bir LCS etkin yüksek kullanılabilirlik ortamıdır (OneBox ortamı değil); Dynamics 365 Supply Chain Management sürüm 10.0.7 veya daha yenisine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="76800-116">The requirement for Planning Optimization is an LCS enabled high-availability environment (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span>

1. <span data-ttu-id="76800-117">LCS'de oturum açın ve istediğiniz ortamı açın.</span><span class="sxs-lookup"><span data-stu-id="76800-117">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="76800-118">**Tüm ayrıntılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="76800-118">Go to **Full details**.</span></span>
1. <span data-ttu-id="76800-119">**Ortam eklentileri** hızlı sekmesinde aşağı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="76800-119">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="76800-120">**Yeni eklenti yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="76800-120">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="76800-121">**Planlamayı En İyi Duruma Getirme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="76800-121">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="76800-122">Yükleme kılavuzunu izleyin ve hüküm ve koşulları kabul edin.</span><span class="sxs-lookup"><span data-stu-id="76800-122">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="76800-123">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="76800-123">Select **Install**.</span></span>
1. <span data-ttu-id="76800-124">**Ortam eklentileri** hızlı sekmesinde, Planlamayı En İyi Duruma Getirme'nin yüklendiğin görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="76800-124">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="76800-125">Birkaç dakika sonra **Yükleme** durumunun değişip **Yüklendi**olarak değişecektir (sayfayı yenilemeniz gerekebilir).</span><span class="sxs-lookup"><span data-stu-id="76800-125">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="76800-126">Yüklendiğinde, Planlamayı En İyi Duruma Getirme'yi Dynamics 365 Supply Chain Management'ta etkinleştirmeye hazırsınız demektir.</span><span class="sxs-lookup"><span data-stu-id="76800-126">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="76800-127">Planlamayı En İyi Duruma Getirme tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="76800-127">Planning Optimization integration</span></span>

<span data-ttu-id="76800-128">Planlamayı En İyi Duruma Getirme eklentisinin master planlama için kullanılması gerekip gerekmediğini yapılandırmak üzere **Master planlama** \> **Ayar** \> **Planlamayı En İyi Duruma Getirme parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="76800-128">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="76800-129">Bağlantı durumu</span><span class="sxs-lookup"><span data-stu-id="76800-129">Connection status</span></span>

<span data-ttu-id="76800-130">Bağlantı durumu, Supply Chain Management ile Planlamayı En İyi Duruma Getirme hizmeti arasındaki bağlantının geçerli durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="76800-130">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="76800-131">Aşağıdaki tabloda, olası değerler gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="76800-131">The following table shows the possible values.</span></span>

| <span data-ttu-id="76800-132">Bağlantı durumu</span><span class="sxs-lookup"><span data-stu-id="76800-132">Connection status</span></span> | <span data-ttu-id="76800-133">Tanım</span><span class="sxs-lookup"><span data-stu-id="76800-133">Description</span></span> | <span data-ttu-id="76800-134">Planlamayı En İyi Duruma Getirme kullanılabilir mi?</span><span class="sxs-lookup"><span data-stu-id="76800-134">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="76800-135">Bağlı</span><span class="sxs-lookup"><span data-stu-id="76800-135">Connected</span></span> | <span data-ttu-id="76800-136">Planlamayı En İyi Duruma Getirme hizmeti ile Supply Chain Management arasında bir bağlantı oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="76800-136">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="76800-137">Evet</span><span class="sxs-lookup"><span data-stu-id="76800-137">Yes</span></span> |
| <span data-ttu-id="76800-138">Bağlantı etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="76800-138">Enabling connection</span></span> | <span data-ttu-id="76800-139">Planlamayı En İyi Duruma Getirme hizmeti için bağlantıyı açma isteği şu anda devam ediyor.</span><span class="sxs-lookup"><span data-stu-id="76800-139">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="76800-140">Hayır</span><span class="sxs-lookup"><span data-stu-id="76800-140">No</span></span> |
| <span data-ttu-id="76800-141">Bağlantı kesildi</span><span class="sxs-lookup"><span data-stu-id="76800-141">Disconnected</span></span> | <span data-ttu-id="76800-142">Planlamayı En İyi Duruma Getirme hizmeti için bağlantı mevcut değil.</span><span class="sxs-lookup"><span data-stu-id="76800-142">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="76800-143">Bağlantı, bu konuda daha önce açıklandığı gibi LCS'den açılabilir.</span><span class="sxs-lookup"><span data-stu-id="76800-143">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="76800-144">Hayır</span><span class="sxs-lookup"><span data-stu-id="76800-144">No</span></span> |
| <span data-ttu-id="76800-145">Bağlantı devre dışı bırakılıyor</span><span class="sxs-lookup"><span data-stu-id="76800-145">Disabling connection</span></span> | <span data-ttu-id="76800-146">Planlamayı En İyi Duruma Getirme hizmeti için bağlantıyı kapatma isteği şu anda devam ediyor.</span><span class="sxs-lookup"><span data-stu-id="76800-146">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="76800-147">Hayır</span><span class="sxs-lookup"><span data-stu-id="76800-147">No</span></span> |
| <span data-ttu-id="76800-148">Durum alınıyor</span><span class="sxs-lookup"><span data-stu-id="76800-148">Getting status</span></span> | <span data-ttu-id="76800-149">Sistem, Planlamayı En İyi Duruma Getirme hizmetinden durum bilgisi bekliyor.</span><span class="sxs-lookup"><span data-stu-id="76800-149">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="76800-150">Hayır</span><span class="sxs-lookup"><span data-stu-id="76800-150">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="76800-151">Planlamayı En İyi Duruma Getirmeyi Kullan seçeneği</span><span class="sxs-lookup"><span data-stu-id="76800-151">The Use Planning Optimization option</span></span>

<span data-ttu-id="76800-152">**Planlamayı En İyi Duruma Getirmeyi Kullan** seçeneği, master planlama için hangi planlama altyapısının kullanılacağını belirler:</span><span class="sxs-lookup"><span data-stu-id="76800-152">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="76800-153">**Evet**: Master planlama için Planlamayı En İyi Duruma Getirme hizmeti kullanılır.</span><span class="sxs-lookup"><span data-stu-id="76800-153">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="76800-154">**Hayır**: Master planlama için yerleşik Supply Chain Management planlama altyapısı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="76800-154">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="76800-155">Yerleşik Supply Chain Management planlama altyapısı için oluşturulan mevcut planlama toplu işleri, **Planlamayı En İyi Duruma Getirmeyi Kullan** seçeneği **Evet** olarak ayarlanırken tetiklenirse bu işler başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="76800-155">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="76800-156">Ayarla tümleştirme</span><span class="sxs-lookup"><span data-stu-id="76800-156">Integration with the setup</span></span>

<span data-ttu-id="76800-157">Planlamayı En İyi Duruma Getirme önizlemesi açıksa master planlama, Planlamayı En İyi Duruma Getirme Eklentisi'ni kullanarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="76800-157">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="76800-158">Bu durumda, master planlama sonuçları ve özellikleri etkilenir.</span><span class="sxs-lookup"><span data-stu-id="76800-158">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="76800-159">İlgili kaynaklar</span><span class="sxs-lookup"><span data-stu-id="76800-159">Related resources</span></span>

[<span data-ttu-id="76800-160">Önizleme için hüküm ve koşullar</span><span class="sxs-lookup"><span data-stu-id="76800-160">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="76800-161">Planlamayı En İyi Duruma Getirmeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="76800-161">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="76800-162">Planlamayı En İyi Duruma Getirme uygunluk analizi</span><span class="sxs-lookup"><span data-stu-id="76800-162">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="76800-163">Plan geçmişini ve planlama günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="76800-163">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="76800-164">Plana filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="76800-164">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="76800-165">Planlama işini iptal etme</span><span class="sxs-lookup"><span data-stu-id="76800-165">Cancel a planning job</span></span>](cancel-planning-job.md)
