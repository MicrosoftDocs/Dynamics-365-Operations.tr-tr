---
title: Planlamayı En İyi Duruma Getirmeye başlayın
description: Bu konuda, Planlamayı En İyi Duruma Getirme işlevini kullanmaya nasıl başlanacağı açıklanmaktadır.
author: ChristianRytt
manager: AnnBe
ms.date: 01/17/2020
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
ms.openlocfilehash: 3e0371c6addc0412dc2fc105891b012941e92a06
ms.sourcegitcommit: e5a3c85a322a9216b8f176536d664fef40ae0bec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/17/2020
ms.locfileid: "2971476"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="73a17-103">Planlamayı En İyi Duruma Getirmeye başlayın</span><span class="sxs-lookup"><span data-stu-id="73a17-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="73a17-104">Planlamayı En İyi Duruma Getirme işlevi şu anda Microsoft Dynamics 365 Supply Chain Management'ta yerleşik olan planlama altyapısında kullanılabilen tüm özellikleri desteklememektedir.</span><span class="sxs-lookup"><span data-stu-id="73a17-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="73a17-105">Bu nedenle, Planlamayı En İyi Duruma Getirme hizmetinde şu anda mevcut olan özellik kümesinin gereksinimlerinizi karşılayıp karşılamadığını değerlendirmeniz önemlidir.</span><span class="sxs-lookup"><span data-stu-id="73a17-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="73a17-106">Varsayılan olarak, Planlamayı En İyi Duruma Getirme işlevi Dynamics Lifecycle Services'ta (LCS) açılmaz.</span><span class="sxs-lookup"><span data-stu-id="73a17-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="73a17-107">Bu nedenle, açılmadan önce değerlendirme yapma fırsatınız vardır.</span><span class="sxs-lookup"><span data-stu-id="73a17-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="73a17-108">Sonuç olarak, Planlamayı En İyi Duruma Getirme hizmeti var olan yerleşik Supply Chain Management planlama altyapısının yerini alacaktır.</span><span class="sxs-lookup"><span data-stu-id="73a17-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="73a17-109">Planlamayı En İyi Duruma Getirme hizmetini açmadan önce Planlamayı En İyi Duruma Getirme uygunluk analizinin sonuçlarını değerlendirmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="73a17-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="73a17-110">Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="73a17-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="73a17-111">Lisans</span><span class="sxs-lookup"><span data-stu-id="73a17-111">Licensing</span></span>

<span data-ttu-id="73a17-112">Geçerli lisansınızı kullanarak master planlamayı çalıştırabilirseniz Planlamayı En İyi Duruma Getirme hizmetini kullanmaya başlamak için ek lisans satın almanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="73a17-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="73a17-113">Eklentiyi yükleme</span><span class="sxs-lookup"><span data-stu-id="73a17-113">Install the add-in</span></span>

<span data-ttu-id="73a17-114">Planlamayı En İyi Duruma Getirme hizmetini kullanmak üzere Dynamics 365 Supply Chain Management için Planlamayı En İyi Duruma Getirme Eklentisi'ni yükleyin.</span><span class="sxs-lookup"><span data-stu-id="73a17-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="73a17-115">Eklentiye LCS projenizden ulaşabilir ve Supply Chain Management kullanıcı arabiriminden (UI) Planlamayı En İyi Duruma Getirme hizmetini açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73a17-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="73a17-116">LCS'de oturum açın ve istediğiniz ortamı açın.</span><span class="sxs-lookup"><span data-stu-id="73a17-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="73a17-117">**Tüm ayrıntılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="73a17-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="73a17-118">**Ortam eklentileri** hızlı sekmesinde aşağı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="73a17-118">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="73a17-119">**Yeni eklenti yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="73a17-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="73a17-120">**Planlamayı En İyi Duruma Getirme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="73a17-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="73a17-121">Yükleme kılavuzunu izleyin ve hüküm ve koşulları kabul edin.</span><span class="sxs-lookup"><span data-stu-id="73a17-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="73a17-122">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="73a17-122">Select **Install**.</span></span>
1. <span data-ttu-id="73a17-123">**Ortam eklentileri** hızlı sekmesinde, Planlamayı En İyi Duruma Getirme'nin yüklendiğin görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="73a17-123">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="73a17-124">Birkaç dakika sonra **Yükleme** durumunun değişip **Yüklendi**olarak değişecektir (sayfayı yenilemeniz gerekebilir).</span><span class="sxs-lookup"><span data-stu-id="73a17-124">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="73a17-125">Yüklendiğinde, Planlamayı En İyi Duruma Getirme'yi Dynamics 365 Supply Chain Management'ta etkinleştirmeye hazırsınız demektir.</span><span class="sxs-lookup"><span data-stu-id="73a17-125">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="73a17-126">Planlamayı En İyi Duruma Getirme tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="73a17-126">Planning Optimization integration</span></span>

<span data-ttu-id="73a17-127">Planlamayı En İyi Duruma Getirme eklentisinin master planlama için kullanılması gerekip gerekmediğini yapılandırmak üzere **Master planlama** \> **Ayar** \> **Planlamayı En İyi Duruma Getirme parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="73a17-127">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="73a17-128">Bağlantı durumu</span><span class="sxs-lookup"><span data-stu-id="73a17-128">Connection status</span></span>

<span data-ttu-id="73a17-129">Bağlantı durumu, Supply Chain Management ile Planlamayı En İyi Duruma Getirme hizmeti arasındaki bağlantının geçerli durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="73a17-129">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="73a17-130">Aşağıdaki tabloda, olası değerler gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="73a17-130">The following table shows the possible values.</span></span>

| <span data-ttu-id="73a17-131">Bağlantı durumu</span><span class="sxs-lookup"><span data-stu-id="73a17-131">Connection status</span></span> | <span data-ttu-id="73a17-132">Tanım</span><span class="sxs-lookup"><span data-stu-id="73a17-132">Description</span></span> | <span data-ttu-id="73a17-133">Planlamayı En İyi Duruma Getirme kullanılabilir mi?</span><span class="sxs-lookup"><span data-stu-id="73a17-133">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="73a17-134">Bağlı</span><span class="sxs-lookup"><span data-stu-id="73a17-134">Connected</span></span> | <span data-ttu-id="73a17-135">Planlamayı En İyi Duruma Getirme hizmeti ile Supply Chain Management arasında bir bağlantı oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="73a17-135">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="73a17-136">Evet</span><span class="sxs-lookup"><span data-stu-id="73a17-136">Yes</span></span> |
| <span data-ttu-id="73a17-137">Bağlantı etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="73a17-137">Enabling connection</span></span> | <span data-ttu-id="73a17-138">Planlamayı En İyi Duruma Getirme hizmeti için bağlantıyı açma isteği şu anda devam ediyor.</span><span class="sxs-lookup"><span data-stu-id="73a17-138">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="73a17-139">Hayır</span><span class="sxs-lookup"><span data-stu-id="73a17-139">No</span></span> |
| <span data-ttu-id="73a17-140">Bağlantı kesildi</span><span class="sxs-lookup"><span data-stu-id="73a17-140">Disconnected</span></span> | <span data-ttu-id="73a17-141">Planlamayı En İyi Duruma Getirme hizmeti için bağlantı mevcut değil.</span><span class="sxs-lookup"><span data-stu-id="73a17-141">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="73a17-142">Bağlantı, bu konuda daha önce açıklandığı gibi LCS'den açılabilir.</span><span class="sxs-lookup"><span data-stu-id="73a17-142">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="73a17-143">Hayır</span><span class="sxs-lookup"><span data-stu-id="73a17-143">No</span></span> |
| <span data-ttu-id="73a17-144">Bağlantı devre dışı bırakılıyor</span><span class="sxs-lookup"><span data-stu-id="73a17-144">Disabling connection</span></span> | <span data-ttu-id="73a17-145">Planlamayı En İyi Duruma Getirme hizmeti için bağlantıyı kapatma isteği şu anda devam ediyor.</span><span class="sxs-lookup"><span data-stu-id="73a17-145">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="73a17-146">Hayır</span><span class="sxs-lookup"><span data-stu-id="73a17-146">No</span></span> |
| <span data-ttu-id="73a17-147">Durum alınıyor</span><span class="sxs-lookup"><span data-stu-id="73a17-147">Getting status</span></span> | <span data-ttu-id="73a17-148">Sistem, Planlamayı En İyi Duruma Getirme hizmetinden durum bilgisi bekliyor.</span><span class="sxs-lookup"><span data-stu-id="73a17-148">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="73a17-149">Hayır</span><span class="sxs-lookup"><span data-stu-id="73a17-149">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="73a17-150">Planlamayı En İyi Duruma Getirmeyi Kullan seçeneği</span><span class="sxs-lookup"><span data-stu-id="73a17-150">The Use Planning Optimization option</span></span>

<span data-ttu-id="73a17-151">**Planlamayı En İyi Duruma Getirmeyi Kullan** seçeneği, master planlama için hangi planlama altyapısının kullanılacağını belirler:</span><span class="sxs-lookup"><span data-stu-id="73a17-151">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="73a17-152">**Evet**: Master planlama için Planlamayı En İyi Duruma Getirme hizmeti kullanılır.</span><span class="sxs-lookup"><span data-stu-id="73a17-152">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="73a17-153">**Hayır**: Master planlama için yerleşik Supply Chain Management planlama altyapısı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="73a17-153">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="73a17-154">Yerleşik Supply Chain Management planlama altyapısı için oluşturulan mevcut planlama toplu işleri, **Planlamayı En İyi Duruma Getirmeyi Kullan** seçeneği **Evet** olarak ayarlanırken tetiklenirse bu işler başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="73a17-154">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="73a17-155">Ayarla tümleştirme</span><span class="sxs-lookup"><span data-stu-id="73a17-155">Integration with the setup</span></span>

<span data-ttu-id="73a17-156">Planlamayı En İyi Duruma Getirme önizlemesi açıksa master planlama, Planlamayı En İyi Duruma Getirme Eklentisi'ni kullanarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="73a17-156">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="73a17-157">Bu durumda, master planlama sonuçları ve özellikleri etkilenir.</span><span class="sxs-lookup"><span data-stu-id="73a17-157">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="73a17-158">İlgili kaynaklar</span><span class="sxs-lookup"><span data-stu-id="73a17-158">Related resources</span></span>

[<span data-ttu-id="73a17-159">Önizleme için hüküm ve koşullar</span><span class="sxs-lookup"><span data-stu-id="73a17-159">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="73a17-160">Planlamayı En İyi Duruma Getirmeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="73a17-160">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="73a17-161">Planlamayı En İyi Duruma Getirme uygunluk analizi</span><span class="sxs-lookup"><span data-stu-id="73a17-161">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="73a17-162">Plan geçmişini ve planlama günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="73a17-162">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="73a17-163">Plana filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="73a17-163">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="73a17-164">Planlama işini iptal etme</span><span class="sxs-lookup"><span data-stu-id="73a17-164">Cancel a planning job</span></span>](cancel-planning-job.md)
