---
title: Planlamayı En İyi Duruma Getirme ile otomatik kesinleştirme
description: Bu konuda, Planlamayı En İyi Duruma Getirme işlevi ile otomatik kesinleştirmenin nasıl kullanılacağı açıklanmaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: d014fcd542462e092f6e88232dff8fd5ee2253c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963472"
---
# <a name="autofirming-with-planning-optimization"></a><span data-ttu-id="9aacb-103">Planlamayı En İyi Duruma Getirme ile otomatik kesinleştirme</span><span class="sxs-lookup"><span data-stu-id="9aacb-103">Autofirming with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9aacb-104">Otomatik kesinleştirme, planlı siparişleri master planlama işleminin parçası olarak kesinleştirmenize (başka bir deyişle, serbest bırakmanıza) olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="9aacb-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="9aacb-105">Planlı siparişler kesinleştirildiğinde, gerçek satınalma siparişlerine, transfer emirlerine veya üretim emirlerine dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="9aacb-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="9aacb-106">Planlamayı En İyi Duruma Getirme işlevi kullanıldığında sipariş tarihi kesinleştirme zaman dilimi içindeyse planlı siparişler, bir master planlama çalışması sırasında kesinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="9aacb-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="9aacb-107">Planlanan bir satınalma siparişinin otomatik kesinleştirilmesi için bir maddenin bir satıcı ile ilişkilendirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="9aacb-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>

## <a name="turn-on-autofirming"></a><span data-ttu-id="9aacb-108">Otomatik kesinleştirmeyi açma</span><span class="sxs-lookup"><span data-stu-id="9aacb-108">Turn on autofirming</span></span>

<span data-ttu-id="9aacb-109">Otomatik kesinleştirmeyi açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9aacb-109">To turn on autofirming, follow these steps.</span></span>

1. <span data-ttu-id="9aacb-110">**Özellik yönetimi** çalışma alanındaki **Yeni** sekmesinde listeden **Planlamayı En İyi Duruma Getirmek için otomatik kesinleştirme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9aacb-110">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="9aacb-111">Özellik, **Yeni** sekmesinde görünmüyorsa **Etkileştirilmemiş** ve **Tümü** sekmelerine bakın.</span><span class="sxs-lookup"><span data-stu-id="9aacb-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="9aacb-112">**Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9aacb-112">Select **Enable now**.</span></span> <span data-ttu-id="9aacb-113">Alternatif olarak, **Planla**'yı seçin ve ardından özelliğin açılmasını istediğiniz zamanı seçin.</span><span class="sxs-lookup"><span data-stu-id="9aacb-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="9aacb-114">Kesinleştirme zaman dilimini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9aacb-114">Set up the firming time fence</span></span>

<span data-ttu-id="9aacb-115">Kesinleştirme zaman dilimi master planlama çalıştırma tarihinden ileriye doğru hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="9aacb-115">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="9aacb-116">Girdiğiniz gün sayısına göre tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="9aacb-116">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="9aacb-117">Kesinleştirme zaman dilimini aşağıdaki yollarla kontrol edebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="9aacb-117">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="9aacb-118">Bir kapsam grubu için varsayılan kesinleştirme zaman dilimini tanımlamak üzere **Master planlama** \> **Ayar** \> **Karşılama** \> **Karşılama grupları**'na gidin ve bir karşılama grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="9aacb-118">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="9aacb-119">Ardından **Diğer** hızlı sekmesinde, **Otomatik kesinleştirme zaman dilimi (gün sayısı)** alanına gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="9aacb-119">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="9aacb-120">Belirli bir maddenin karşılama grubu için tanımlanan kesinleştirme zaman dilimini geçersiz kılmak için **Ürün bilgileri yönetimi** \> **Serbest bırakılan ürünler**'e gidin ve ardından Eylem Bölmesi'nden **Plan**'ı ve **Madde karşılama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="9aacb-120">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the Action Pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="9aacb-121">Ardından **Genel** sekmesinde, **Zaman dilimini geçersiz kıl**'ı seçin ve **Otomatik kesinleştirme zaman dilimi (gün)** alanına gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="9aacb-121">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="9aacb-122">Belirli bir master planın kapsam grubu ve madde kapsamı için tanımlanan kesinleştirme zaman dilimi üzerine yazmak için **Master planlama** \> **Ayar** \> **Master planlar**'a gidin ve bir Master plan seçin.</span><span class="sxs-lookup"><span data-stu-id="9aacb-122">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="9aacb-123">Ardından **Gün cinsinden zaman dilimi** hızlı sekmesinde, **Kesinleştir** seçeneğini **Evet** olarak ayarlayın ve gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="9aacb-123">Then, on the **Time fence in days** FastTab, set **Firming** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="9aacb-124">Planlama İyileştirmesi işlevini kullanan otomatik kesinleştirme özelliği bir master planlama çalışması için açılırsa otomatik kesinleştirme işlemi, otomatik kesinleştirme ayarına göre gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="9aacb-124">If autofirming is turned on for a master planning run that uses Planning Optimization, the autofirming process is done according to the autofirming setup.</span></span> <span data-ttu-id="9aacb-125">Otomatik kesinleştirme açılmazsa veya planlama **Net gereksinimler** sayfasından başlatılırsa otomatik kesinleştirme işlemi atlanır.</span><span class="sxs-lookup"><span data-stu-id="9aacb-125">If autofirming isn't turned on, or if planning is started from the **Net requirements** page, the autofirming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="9aacb-126">Planlamayı En İyi Duruma Getirme işleviyle yerleşik Supply Chain Management planlama altyapısının karşılaştırılması</span><span class="sxs-lookup"><span data-stu-id="9aacb-126">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="9aacb-127">Planlamayı En İyi Duruma Getirme ve Microsoft Dynamics 365 Supply Chain Management'ta yerleşik olan planlama altyapısı işlevlerinin ikisi de planlı siparişleri kesinleştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9aacb-127">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to autofirm planned orders.</span></span> <span data-ttu-id="9aacb-128">Ancak, bazı önemli farklar vardır.</span><span class="sxs-lookup"><span data-stu-id="9aacb-128">However, there are some important differences.</span></span> <span data-ttu-id="9aacb-129">Örneğin, Planlamayı En İyi Duruma Getirme işlevi hangi planlı siparişlerin kesinleştirileceğini belirlemek için sipariş tarihini (başka bir deyişle, başlangıç tarihi) kullanırken yerleşik Supply Chain Management planlama altyapısı gereksinim tarihini (başka bir deyişle, bitiş tarihi) kullanır.</span><span class="sxs-lookup"><span data-stu-id="9aacb-129">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="9aacb-130">Aşağıda, farkların bir özeti verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="9aacb-130">Here is a summary of the differences.</span></span>

<span data-ttu-id="9aacb-131">**Planlamayı En İyi Duruma Getirme**</span><span class="sxs-lookup"><span data-stu-id="9aacb-131">**Planning Optimization**</span></span>

- <span data-ttu-id="9aacb-132">Otomatik kesinleştirme, sipariş tarihini (başlangıç tarihi) temel alır.</span><span class="sxs-lookup"><span data-stu-id="9aacb-132">Autofirming is based on the order date (start date).</span></span>
- <span data-ttu-id="9aacb-133">Sipariş tarihi (başlangıç tarihi) kesinleştirmeyi tetiklediğinden sağlama süresini kesinleştirme zaman diliminin bir parçası olarak düşünmeniz gerekmez.</span><span class="sxs-lookup"><span data-stu-id="9aacb-133">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="9aacb-134">Geçerli haftada başlaması gereken tüm siparişleri kesinleştirmek istiyorsanız kesinleştirme zaman dilimi bir hafta olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9aacb-134">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="9aacb-135">**Yerleşik Supply Chain Management planlama altyapısı**</span><span class="sxs-lookup"><span data-stu-id="9aacb-135">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="9aacb-136">Otomatik kesinleştirme, gereksinim tarihini (bitiş tarihi) temel alır.</span><span class="sxs-lookup"><span data-stu-id="9aacb-136">Autofirming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="9aacb-137">Siparişlerin vade tarihinde kesinleştirilmesini garanti etmeye yardımcı olması için kesinleştirme zaman dilimi, sağlama süresinden daha uzun olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9aacb-137">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="9aacb-138">Geçerli haftada başlaması gereken tüm siparişleri kesinleştirmek istiyorsanız kesinleştirme zaman dilimi, sağlama süresi artı bir hafta olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9aacb-138">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>
