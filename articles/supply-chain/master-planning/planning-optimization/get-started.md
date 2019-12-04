---
title: Planlamayı En İyi Duruma Getirmeye başlayın
description: Bu konuda, Planlamayı En İyi Duruma Getirme işlevini kullanmaya nasıl başlanacağı açıklanmaktadır.
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
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
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774067"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="944d3-103">Planlamayı En İyi Duruma Getirmeye başlayın</span><span class="sxs-lookup"><span data-stu-id="944d3-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="944d3-104">Planlamayı En İyi Duruma Getirme işlevi şu anda Microsoft Dynamics 365 Supply Chain Management'ta yerleşik olan planlama altyapısında kullanılabilen tüm özellikleri desteklememektedir.</span><span class="sxs-lookup"><span data-stu-id="944d3-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="944d3-105">Bu nedenle, Planlamayı En İyi Duruma Getirme hizmetinde şu anda mevcut olan özellik kümesinin gereksinimlerinizi karşılayıp karşılamadığını değerlendirmeniz önemlidir.</span><span class="sxs-lookup"><span data-stu-id="944d3-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="944d3-106">Varsayılan olarak, Planlamayı En İyi Duruma Getirme işlevi Dynamics Lifecycle Services'ta (LCS) açılmaz.</span><span class="sxs-lookup"><span data-stu-id="944d3-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="944d3-107">Bu nedenle, açılmadan önce değerlendirme yapma fırsatınız vardır.</span><span class="sxs-lookup"><span data-stu-id="944d3-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="944d3-108">Sonuç olarak, Planlamayı En İyi Duruma Getirme hizmeti var olan yerleşik Supply Chain Management planlama altyapısının yerini alacaktır.</span><span class="sxs-lookup"><span data-stu-id="944d3-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="944d3-109">Planlamayı En İyi Duruma Getirme hizmetini açmadan önce Planlamayı En İyi Duruma Getirme uygunluk analizinin sonuçlarını değerlendirmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="944d3-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="944d3-110">Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="944d3-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="944d3-111">Lisans</span><span class="sxs-lookup"><span data-stu-id="944d3-111">Licensing</span></span>

<span data-ttu-id="944d3-112">Geçerli lisansınızı kullanarak master planlamayı çalıştırabilirseniz Planlamayı En İyi Duruma Getirme hizmetini kullanmaya başlamak için ek lisans satın almanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="944d3-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="944d3-113">Eklentiyi yükleme</span><span class="sxs-lookup"><span data-stu-id="944d3-113">Install the add-in</span></span>

<span data-ttu-id="944d3-114">Planlamayı En İyi Duruma Getirme hizmetini kullanmak üzere Dynamics 365 Supply Chain Management için Planlamayı En İyi Duruma Getirme Eklentisi'ni yükleyin.</span><span class="sxs-lookup"><span data-stu-id="944d3-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="944d3-115">Eklentiye LCS projenizden ulaşabilir ve Supply Chain Management kullanıcı arabiriminden (UI) Planlamayı En İyi Duruma Getirme hizmetini açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="944d3-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="944d3-116">LCS'de oturum açın ve istediğiniz ortamı açın.</span><span class="sxs-lookup"><span data-stu-id="944d3-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="944d3-117">**Tüm ayrıntılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="944d3-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="944d3-118">**Bakım yap**'ı seçin veya **Ortam eklentileri** hızlı sekmesinde aşağı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="944d3-118">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="944d3-119">**Yeni eklenti yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="944d3-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="944d3-120">**Planlamayı En İyi Duruma Getirme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="944d3-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="944d3-121">Yükleme kılavuzunu izleyin ve hüküm ve koşulları kabul edin.</span><span class="sxs-lookup"><span data-stu-id="944d3-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="944d3-122">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="944d3-122">Select **Install**.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="944d3-123">Planlamayı En İyi Duruma Getirme tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="944d3-123">Planning Optimization integration</span></span>

<span data-ttu-id="944d3-124">Planlamayı En İyi Duruma Getirme Eklentisi'nin master planlama için kullanılması gerekip gerekmediğini yapılandırmak üzere **Master planlama** \> **Ayar** \> **Planlamayı En İyi Duruma Getirme tümleştirmesi** \> **Tümleştirme parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="944d3-124">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization integration** \> **Integration parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="944d3-125">Bağlantı durumu</span><span class="sxs-lookup"><span data-stu-id="944d3-125">Connection status</span></span>

<span data-ttu-id="944d3-126">Bağlantı durumu, Supply Chain Management ile Planlamayı En İyi Duruma Getirme hizmeti arasındaki bağlantının geçerli durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="944d3-126">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="944d3-127">Aşağıdaki tabloda, olası değerler gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="944d3-127">The following table shows the possible values.</span></span>

| <span data-ttu-id="944d3-128">Bağlantı durumu</span><span class="sxs-lookup"><span data-stu-id="944d3-128">Connection status</span></span> | <span data-ttu-id="944d3-129">Tanım</span><span class="sxs-lookup"><span data-stu-id="944d3-129">Description</span></span> | <span data-ttu-id="944d3-130">Planlamayı En İyi Duruma Getirme kullanılabilir mi?</span><span class="sxs-lookup"><span data-stu-id="944d3-130">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="944d3-131">Bağlı</span><span class="sxs-lookup"><span data-stu-id="944d3-131">Connected</span></span> | <span data-ttu-id="944d3-132">Planlamayı En İyi Duruma Getirme hizmeti ile Supply Chain Management arasında bir bağlantı oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="944d3-132">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="944d3-133">Evet</span><span class="sxs-lookup"><span data-stu-id="944d3-133">Yes</span></span> |
| <span data-ttu-id="944d3-134">Bağlantı etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="944d3-134">Enabling connection</span></span> | <span data-ttu-id="944d3-135">Planlamayı En İyi Duruma Getirme hizmeti için bağlantıyı açma isteği şu anda devam ediyor.</span><span class="sxs-lookup"><span data-stu-id="944d3-135">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="944d3-136">Hayır</span><span class="sxs-lookup"><span data-stu-id="944d3-136">No</span></span> |
| <span data-ttu-id="944d3-137">Bağlantı kesildi</span><span class="sxs-lookup"><span data-stu-id="944d3-137">Disconnected</span></span> | <span data-ttu-id="944d3-138">Planlamayı En İyi Duruma Getirme hizmeti için bağlantı mevcut değil.</span><span class="sxs-lookup"><span data-stu-id="944d3-138">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="944d3-139">Bağlantı, bu konuda daha önce açıklandığı gibi LCS'den açılabilir.</span><span class="sxs-lookup"><span data-stu-id="944d3-139">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="944d3-140">Hayır</span><span class="sxs-lookup"><span data-stu-id="944d3-140">No</span></span> |
| <span data-ttu-id="944d3-141">Bağlantı devre dışı bırakılıyor</span><span class="sxs-lookup"><span data-stu-id="944d3-141">Disabling connection</span></span> | <span data-ttu-id="944d3-142">Planlamayı En İyi Duruma Getirme hizmeti için bağlantıyı kapatma isteği şu anda devam ediyor.</span><span class="sxs-lookup"><span data-stu-id="944d3-142">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="944d3-143">Hayır</span><span class="sxs-lookup"><span data-stu-id="944d3-143">No</span></span> |
| <span data-ttu-id="944d3-144">Durum alınıyor</span><span class="sxs-lookup"><span data-stu-id="944d3-144">Getting status</span></span> | <span data-ttu-id="944d3-145">Sistem, Planlamayı En İyi Duruma Getirme hizmetinden durum bilgisi bekliyor.</span><span class="sxs-lookup"><span data-stu-id="944d3-145">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="944d3-146">Hayır</span><span class="sxs-lookup"><span data-stu-id="944d3-146">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="944d3-147">Planlamayı En İyi Duruma Getirmeyi Kullan seçeneği</span><span class="sxs-lookup"><span data-stu-id="944d3-147">The Use Planning Optimization option</span></span>

<span data-ttu-id="944d3-148">**Planlamayı En İyi Duruma Getirmeyi Kullan** seçeneği, master planlama için hangi planlama altyapısının kullanılacağını belirler:</span><span class="sxs-lookup"><span data-stu-id="944d3-148">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="944d3-149">**Evet**: Master planlama için Planlamayı En İyi Duruma Getirme hizmeti kullanılır.</span><span class="sxs-lookup"><span data-stu-id="944d3-149">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="944d3-150">**Hayır**: Master planlama için yerleşik Supply Chain Management planlama altyapısı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="944d3-150">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="944d3-151">Yerleşik Supply Chain Management planlama altyapısı için oluşturulan mevcut planlama toplu işleri, **Planlamayı En İyi Duruma Getirmeyi Kullan** seçeneği **Evet** olarak ayarlanırken tetiklenirse bu işler başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="944d3-151">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="944d3-152">Ayarla tümleştirme</span><span class="sxs-lookup"><span data-stu-id="944d3-152">Integration with the setup</span></span>

<span data-ttu-id="944d3-153">Planlamayı En İyi Duruma Getirme önizlemesi açıksa master planlama, Planlamayı En İyi Duruma Getirme Eklentisi'ni kullanarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="944d3-153">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="944d3-154">Bu durumda, master planlama sonuçları ve özellikleri etkilenir.</span><span class="sxs-lookup"><span data-stu-id="944d3-154">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="944d3-155">İlgili kaynaklar</span><span class="sxs-lookup"><span data-stu-id="944d3-155">Related resources</span></span>

[<span data-ttu-id="944d3-156">Önizleme için hüküm ve koşullar</span><span class="sxs-lookup"><span data-stu-id="944d3-156">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="944d3-157">Planlamayı En İyi Duruma Getirmeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="944d3-157">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="944d3-158">Planlamayı En İyi Duruma Getirme uygunluk analizi</span><span class="sxs-lookup"><span data-stu-id="944d3-158">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="944d3-159">Plan geçmişini ve planlama günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="944d3-159">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="944d3-160">Plana filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="944d3-160">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="944d3-161">Planlama işini iptal etme</span><span class="sxs-lookup"><span data-stu-id="944d3-161">Cancel a planning job</span></span>](cancel-planning-job.md)
