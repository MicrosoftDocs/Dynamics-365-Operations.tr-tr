---
title: Uyarılara genel bakış
description: Bu konu uyarılar hakkında genel bilgileri sağlar. Uyarıları, iş günü sırasında izlemek istediğiniz olaylardan haberdar olmak için kullanabilirsiniz.
author: tjvass
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: e57b065dc1a2c0db593b38106f4391e281feb1e6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565050"
---
# <a name="alerts-overview"></a><span data-ttu-id="34653-104">Uyarılara genel bakış</span><span class="sxs-lookup"><span data-stu-id="34653-104">Alerts overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a><span data-ttu-id="34653-105">Uyarılar hakkında</span><span class="sxs-lookup"><span data-stu-id="34653-105">About alerts</span></span>
<span data-ttu-id="34653-106">Uyarılar, sistemdeki kritik olaylar için bir bildirim sistemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34653-106">Alerts form a notification system for critical events in the system.</span></span> <span data-ttu-id="34653-107">Uyarıları, iş günü sırasında izlemek istediğiniz olaylardan haberdar olmak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34653-107">You can use alerts to stay informed about events that you want to track during the workday.</span></span> <span data-ttu-id="34653-108">Vadesi geçen teslimatlar, silinmiş siparişler, değişen fiyatlar veya yanıtlamanız gereken diğer olaylar hakkında uyarılar almak için kendi kurallarınızı kolaylıkla oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34653-108">You can easily create your own set of alert rules so that you're alerted about deliveries that are overdue, orders that are deleted, prices that change, or other events that you must respond to.</span></span>

<span data-ttu-id="34653-109">Kurumsal kaynak planlamasında (ERP), uyarı özelliklerinin kullanılabileceği bazı tipik senaryolar vardır.</span><span class="sxs-lookup"><span data-stu-id="34653-109">In enterprise resource planning (ERP), there are several typical scenarios where the alerts feature can be used.</span></span> <span data-ttu-id="34653-110">Burada bazı örnekler verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="34653-110">Here are some examples.</span></span>

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a><span data-ttu-id="34653-111">Senaryo 1: Yeni satış siparişleri için bir uyarı kuralı oluşturun</span><span class="sxs-lookup"><span data-stu-id="34653-111">Scenario 1: Create an alert rule for new sales orders</span></span>

1. <span data-ttu-id="34653-112">**Tüm satış siparişleri** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="34653-112">Open the **All sales orders** page.</span></span>
2. <span data-ttu-id="34653-113">Eylem Bölmesinde, **Seçenekler** sekmesindeki **Paylaş** grubunda **Özel uyarı oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="34653-113">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
3. <span data-ttu-id="34653-114">**Uyarı kuralı oluştur** iletişim kutusunda **Beni uyarma zamanı** hızlı sekmesinde **Olay** alanında **Kayıt oluşturuldu**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="34653-114">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Event** field, select **Record has been created**.</span></span>

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a><span data-ttu-id="34653-115">Senaryo 2: Bir teslimat tarihinin ertelenmesi için bir uyarı kuralı oluşturun</span><span class="sxs-lookup"><span data-stu-id="34653-115">Scenario 2: Create an alert rule for postponement of a delivery date</span></span>

1. <span data-ttu-id="34653-116">**Tüm satınalma siparişleri** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="34653-116">Open the **All purchase orders** page.</span></span>
2. <span data-ttu-id="34653-117">Satınalma siparişi ayrıntılarına erişmek için bir satınalma siparişi kimliği seçin.</span><span class="sxs-lookup"><span data-stu-id="34653-117">Select a purchase order ID to access the purchase order details.</span></span>
3. <span data-ttu-id="34653-118">**Satın alma siparişi başlığı** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="34653-118">Expand the **Purchase order header** FastTab.</span></span>
4. <span data-ttu-id="34653-119">Eylem Bölmesinde, **Seçenekler** sekmesindeki **Paylaş** grubunda **Özel uyarı oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="34653-119">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
5. <span data-ttu-id="34653-120">**Uyarı kuralı oluştur** iletişim kutusunda **Beni uyarma zamanı** hızlı sekmesinde **Alan** alanında **Teslimat tarihi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="34653-120">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Field** field, select **Delivery date**.</span></span>
6. <span data-ttu-id="34653-121">**Olay** alanında **ertelendi**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="34653-121">In the **Event** field, select **has been postponed**.</span></span>
    
<span data-ttu-id="34653-122">**Uyarı kuralı oluştur** iletişim kutusunu kapattıktan sonra kuralınız, **Uyarı kurallarını yönet** sayfasında görünür.</span><span class="sxs-lookup"><span data-stu-id="34653-122">After you close the **Create alert rule** dialog box, your rule appears on the **Manage alert rules** page.</span></span> <span data-ttu-id="34653-123">Mevcut uyarı kurallarınızı güncelleştirmek için **Uyarı kurallarını yönet** sayfasını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34653-123">You can use the **Manage alert rules** page to update your existing alert rules.</span></span> <span data-ttu-id="34653-124">Örneğin, olay tetikleyicilerini değiştirebilir, olay bildirimlerini güncelleştirebilir ve bitiş tarihlerini güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34653-124">For example, you can modify event triggers, update event notifications, and update expiration dates.</span></span> <span data-ttu-id="34653-125">**Uyarı kurallarını yönet** sayfasını açmak için Eylem Bölmesinin **Seçenekler** sekmesinde **Beni uyar** düğmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="34653-125">To open the **Manage alert rules** page, use the **Alert me** button on the **Options** tab of the Action Pane.</span></span>

## <a name="what-occurs-when-an-alert-rule-is-created"></a><span data-ttu-id="34653-126">Uyarı kuralı oluşturulduğunda ne olur?</span><span class="sxs-lookup"><span data-stu-id="34653-126">What occurs when an alert rule is created?</span></span>

<span data-ttu-id="34653-127">Uyarı kuralları oluşturduğunuzda önceden tanımlanmış bir olayı belirli bir alanla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34653-127">When you create alert rules, you can associate a predefined event with a specific field.</span></span> <span data-ttu-id="34653-128">Örneğin, alanda belirtilen tarih geldiğinde veya alan içeriği değiştiğinde.</span><span class="sxs-lookup"><span data-stu-id="34653-128">For example, the date that is specified in the field arrives, or the contents of the field change.</span></span> <span data-ttu-id="34653-129">Alternatif olarak, bir olayı belirli bir sayfadaki kayıtlarla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34653-129">Alternatively, you can associate an event with the records on a specific page.</span></span> <span data-ttu-id="34653-130">Örneğin, bir kayıt oluşturulur veya bir kayıt silinir.</span><span class="sxs-lookup"><span data-stu-id="34653-130">For example, a record is created, or a record is deleted.</span></span>

<span data-ttu-id="34653-131">Alan veya sayfadaki bir kayıt için seçilen olay gerçekleşirse bir uyarı gönderilir.</span><span class="sxs-lookup"><span data-stu-id="34653-131">When the selected event occurs for the field or for a record on the page, an alert is sent to you.</span></span> <span data-ttu-id="34653-132">Örneğin, belirli bir satınalma sipariş satırında **Teslimat tarihi** alanını **bu kadar süre önce sona erdi** olayıyla ilişkilendirdiğiniz bir kural oluşturun.</span><span class="sxs-lookup"><span data-stu-id="34653-132">For example, you create a rule where you associate the **Delivery date** field on a specific purchase order line with the **was due this amount of time ago** event.</span></span> <span data-ttu-id="34653-133">Zaman dilimini beş gün olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="34653-133">You set the time frame to five days.</span></span> <span data-ttu-id="34653-134">Bu durumda, ilgili satınalma sipariş satırının teslimat tarihinden beş gün sonra bir uyarı gönderilir.</span><span class="sxs-lookup"><span data-stu-id="34653-134">In this case, an alert is sent five days after the delivery date of that purchase order line.</span></span>

<span data-ttu-id="34653-135">Ayrıca uyarı kurallarını koşullar ayarlayarak daraltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34653-135">Additionally, you can refine alert rules by setting conditions.</span></span> <span data-ttu-id="34653-136">Örneğin, belirli satıcı hesapları için oluşturulan yeni satınalma siparişleriyle ilgili uyarı alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34653-136">For example, you can be alerted about new purchase orders that are created for specific vendor accounts.</span></span>

## <a name="preparing-for-an-alert"></a><span data-ttu-id="34653-137">Uyarı için hazırlanma</span><span class="sxs-lookup"><span data-stu-id="34653-137">Preparing for an alert</span></span>

<span data-ttu-id="34653-138">Uyarı kuralını ayarlamadan önce, ne zaman ve hangi durumlarda uyarı almak istediğinize karar verin.</span><span class="sxs-lookup"><span data-stu-id="34653-138">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="34653-139">Hangi olay hakkında bilgilendirilmek istediğinizi bildiğinizde, bu olaya neden olan verilerin göründüğü sayfayı bulun.</span><span class="sxs-lookup"><span data-stu-id="34653-139">When you know which event you want to be notified about, find the page where the data that causes that event appears.</span></span> <span data-ttu-id="34653-140">Olay, gelecek bir tarih veya meydana gelen özel bir değişiklik olabilir.</span><span class="sxs-lookup"><span data-stu-id="34653-140">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="34653-141">Bu nedenle, tarihin belirtildiği veya değişen alanın bulunduğu ya da oluşturulan yeni kaydın göründüğü sayfayı bulmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="34653-141">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="34653-142">Bu bilgilere sahip olduktan sonra uyarı kuralını oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34653-142">After you have this information, you can create the alert rule.</span></span>

## <a name="components-of-an-alert-rule"></a><span data-ttu-id="34653-143">Uyarı kuralının bileşenleri</span><span class="sxs-lookup"><span data-stu-id="34653-143">Components of an alert rule</span></span>

<span data-ttu-id="34653-144">Uyarı kuralının beş bileşeni vardır:</span><span class="sxs-lookup"><span data-stu-id="34653-144">An alert rule has five components:</span></span>

- <span data-ttu-id="34653-145">**Olay**: Uyarı kuralını tetikleyen olay, gelecek bir tarih veya meydana gelen belirli bir değişiklik olabilir.</span><span class="sxs-lookup"><span data-stu-id="34653-145">**Event** – The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="34653-146">Olayları, **Uyarı kuralı oluştur** iletişim kutusunun **İş durumu değişiklikleri için e-posta uyarıları gönder** hızlı sekmesinde tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="34653-146">You define events on the **Send email alerts for job status changes** FastTab of the **Create alert rule** dialog box.</span></span>
- <span data-ttu-id="34653-147">**Koşul**: **Uyarı kuralı oluştur** iletişim kutusunun **Beni uyar** hızlı sekmesinde, olaylar hakkında ne zaman uyarılacağınızı denetlemek üzere koşulun kapsamını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34653-147">**Condition** – On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can select the scope of the condition, to control when you're alerted about events.</span></span> <span data-ttu-id="34653-148">Kuralı, yalnızca geçerli kayda veya sayfadaki tüm görünür kayıtlara uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34653-148">You can apply the rule either to the current record only or to all visible records on the page.</span></span> <span data-ttu-id="34653-149">Kural, tüzel kişiliklerde geçerliyse **Organizasyon çapında** seçeneğini **Evet** olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34653-149">If the rule applies across legal entities, you can set the **Organization-wide** option to **Yes**.</span></span>
- <span data-ttu-id="34653-150">**Kuralın sona ermesi**: **Uyarı kuralı oluştur** iletişim kutusunun **Beni şu tarihe kadar uyar** hızlı sekmesinde, uyarı kuralının ne kadar süreyle etkin olacağını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34653-150">**Expiry of rule** – On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>
- <span data-ttu-id="34653-151">**İçindekiler**: **Uyarı kuralı oluştur** iletişim kutusunun **Bana gönderilecek uyarı biçimi** hızlı sekmesinde, uyarı iletisinin kullanması gereken konu metnini ve ileti metnini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34653-151">**Contents** – On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>
- <span data-ttu-id="34653-152">**Kullanıcı**: **Uyarı kuralı oluştur** iletişim kutusunun **Uyarılacaklar** hızlı sekmesinde, uyarı iletisini hangi kullanıcının alması gerektiğini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34653-152">**User** – On the **Alert who** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="34653-153">Varsayılan olarak kullanıcı kimliğiniz seçilir.</span><span class="sxs-lookup"><span data-stu-id="34653-153">By default, your user ID is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="34653-154">Bu seçenek, kuruluş yöneticileriyle sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="34653-154">This option is restricted to organization administrators.</span></span>

## <a name="videos"></a><span data-ttu-id="34653-155">Videolar</span><span class="sxs-lookup"><span data-stu-id="34653-155">Videos</span></span>

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a><span data-ttu-id="34653-156">Filtrelenmiş verileri izlemek için uyarıları kullanma</span><span class="sxs-lookup"><span data-stu-id="34653-156">How to use alerts to monitor filtered data</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3DWZ3]

<span data-ttu-id="34653-157">[Filtrelenmiş verileri izlemek için uyarıları kullanma](https://youtu.be/ZYKMcv6kl9s) videosu (yukarıda gösterilir) YouTube'daki [Finance and Operations oynatma listesine](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="34653-157">The [How to use alerts to monitor filtered data](https://youtu.be/ZYKMcv6kl9s) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

### <a name="alert-rule-options"></a><span data-ttu-id="34653-158">Uyarı kuralı seçenekleri</span><span class="sxs-lookup"><span data-stu-id="34653-158">Alert rule options</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3E4PV]

<span data-ttu-id="34653-159">[Uyarı kuralı seçenekleri](https://youtu.be/cpzimwOjicM) videosu (yukarıda gösterilen), YouTube'da bulunan [Finance and Operations oynatma listesinde bulunmaktadır](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW).</span><span class="sxs-lookup"><span data-stu-id="34653-159">The [Alert rule options](https://youtu.be/cpzimwOjicM) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]