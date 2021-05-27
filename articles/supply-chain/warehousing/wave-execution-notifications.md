---
title: Dalga yürütme bildirimleri
description: Bu konu, dalga yürütme bildirimlerini ve bunları nasıl ayarlayabileceğinizi açıklamaktadır.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2022-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: fee112d3211f619b2146dd21c4f8a52ad33667d6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019166"
---
# <a name="wave-execution-notifications"></a><span data-ttu-id="c6514-103">Dalga yürütme bildirimleri</span><span class="sxs-lookup"><span data-stu-id="c6514-103">Wave execution notifications</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="c6514-104">*Dalga yürütme bildirimleri* özelliği, dalga yürütme ile ilgili bildirimler sağlamak için iş olaylarını ve eylem merkezini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c6514-104">The *Wave execution notifications* feature uses business events and the Action center to deliver notifications that are related to wave execution.</span></span> <span data-ttu-id="c6514-105">Bildirimler üreten olayların tiplerini, onları oluşturan ambarları ve onları alan kullanıcıları belirtmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="c6514-105">It lets you specify the types of events that generate notifications, the warehouses that generate them, and the users who receive them.</span></span>

<span data-ttu-id="c6514-106">Gezinti çubuğunun sağ tarafındaki **iletileri göster** düğmesi (çan sembolü), geçerli kullanıcı için bir Eylem Merkezi iletisinin ne zaman kullanılabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6514-106">The **Show messages** button (bell symbol) on the right side of the navigation bar indicates when an Action center message is available for the current user.</span></span> <span data-ttu-id="c6514-107">Kullanıcı, eylem merkezini açmak ve iletileri incelemek için **iletileri göster** düğmesini seçebilir.</span><span class="sxs-lookup"><span data-stu-id="c6514-107">The user can select the **Show messages** button to open the Action center and review the messages.</span></span>

<span data-ttu-id="c6514-108">İş olayları, iş süreçleri çalıştırıldığında oluşur.</span><span class="sxs-lookup"><span data-stu-id="c6514-108">Business events occur when business processes are run.</span></span> <span data-ttu-id="c6514-109">İş süreçleri görevlerden oluşur.</span><span class="sxs-lookup"><span data-stu-id="c6514-109">Business processes are made up of tasks.</span></span> <span data-ttu-id="c6514-110">Bir iş süreci sırasında, buna katılan kullanıcılar bu görevleri tamamlamak için iş eylemlerini gerçekleştirirler.</span><span class="sxs-lookup"><span data-stu-id="c6514-110">During a business process, the users who participate in it perform business actions to complete those tasks.</span></span> <span data-ttu-id="c6514-111">İş olayları, dış sistemlerin Finance and Operations uygulamalarından bildirimler almasına olanak tanıyan bir mekanizma sağlar.</span><span class="sxs-lookup"><span data-stu-id="c6514-111">Business events provide a mechanism that lets external systems receive notifications from Finance and Operations applications.</span></span> <span data-ttu-id="c6514-112">Bu şekilde, sistemler iş olaylarına yanıt olarak iş eylemlerini gerçekleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="c6514-112">In this way, the systems can perform business actions in response to the business events.</span></span> <span data-ttu-id="c6514-113">Daha fazla bilgi için bkz. [İş olaylarına genel bakış](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span><span class="sxs-lookup"><span data-stu-id="c6514-113">For more information, see [Business events overview](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span></span>

## <a name="turn-on-the-wave-execution-notifications-feature"></a><span data-ttu-id="c6514-114">Dalga yürütme bildirimleri özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="c6514-114">Turn on the Wave execution notifications feature</span></span>

<span data-ttu-id="c6514-115">*Dalga yürütme bildirimleri* özelliğini kullanabilmeniz için sisteminizde etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="c6514-115">Before you can use the *Wave execution notifications* feature, it must be turned on in your system.</span></span> <span data-ttu-id="c6514-116">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="c6514-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="c6514-117">Burada, özellik aşağıdaki şekilde listelenmiştir:</span><span class="sxs-lookup"><span data-stu-id="c6514-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c6514-118">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="c6514-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="c6514-119">**Özellik adı:** *Dalga yürütme bildirimleri*</span><span class="sxs-lookup"><span data-stu-id="c6514-119">**Feature name:** *Wave execution notifications*</span></span>

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a><span data-ttu-id="c6514-120">Senaryo: İşlem merkezine dalga toplu iş yürütme bildirimleri gönderme</span><span class="sxs-lookup"><span data-stu-id="c6514-120">Scenario: Send wave batch execution notifications to the Action center</span></span>

<span data-ttu-id="c6514-121">Bu senaryo, dalga toplu iş yürütme hataları hakkında, Eylem Merkezi aracılığıyla belirli bir role bildirim göndermek için uçtan uca akışı gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6514-121">This scenario shows the end-to-end flow for sending notifications about wave batch execution errors to a specific role via the Action center.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="c6514-122">Tanıtım verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="c6514-122">Make demo data available</span></span>

<span data-ttu-id="c6514-123">Bu senaryoyu izlemek için, demo verilerinin yüklenmiş olması ve **USMF** tüzel kişiliğini kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c6514-123">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a><span data-ttu-id="c6514-124">Dalgaların toplu iş modunda çalıştığından emin olun</span><span class="sxs-lookup"><span data-stu-id="c6514-124">Make sure that waves are run in batch mode</span></span>

1. <span data-ttu-id="c6514-125">**Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c6514-125">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="c6514-126">**Dalga işleme** hızlı sekmesinde, **Dalgaları Toplu işle** öğesini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c6514-126">On the **Wave processing** FastTab, set the **Process waves in batch** option to *Yes*.</span></span>

> [!NOTE]
> <span data-ttu-id="c6514-127">Dalga toplu yürütme bildirimlerini devre dışı bırakmak istiyorsanız, **dalga işleme toplu iş bildirimlerini devre dışı bırak** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c6514-127">If you want to disable wave batch execution notifications, set the **Disable wave processing batch notifications** option to *Yes*.</span></span>

### <a name="configure-a-wave-notification-policy"></a><span data-ttu-id="c6514-128">Dalga bildirim ilkesi Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="c6514-128">Configure a wave notification policy</span></span>

<span data-ttu-id="c6514-129">Dalga bildirim ilkeleri, gönderilen bildirim türlerini ve uyarılacak kullanıcıları tanımlar.</span><span class="sxs-lookup"><span data-stu-id="c6514-129">Wave notification policies define the types of notifications that are sent and the users who are notified.</span></span>

1. <span data-ttu-id="c6514-130">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga bildirim ilkeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c6514-130">Go to **Warehouse management \> Setup \> Waves \> Wave notification policies**.</span></span>
1. <span data-ttu-id="c6514-131">Aşağıdaki ayarlara sahip bir kayıt oluşturun:</span><span class="sxs-lookup"><span data-stu-id="c6514-131">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="c6514-132">**Dalga bildirim ilkesi:** *24BatchError*</span><span class="sxs-lookup"><span data-stu-id="c6514-132">**Wave notification policy:** *24BatchError*</span></span>
    - <span data-ttu-id="c6514-133">**Açıklama:** *Ambar 24 dalga toplu iş hatası*</span><span class="sxs-lookup"><span data-stu-id="c6514-133">**Description:** *Warehouse 24 wave batch error*</span></span>
    - <span data-ttu-id="c6514-134">**Bildirim gönderme:** *Yalnızca hata*</span><span class="sxs-lookup"><span data-stu-id="c6514-134">**Send notification on:** *Error only*</span></span>
    - <span data-ttu-id="c6514-135">**Gönderilen rol:** *Sistem Yöneticisi*</span><span class="sxs-lookup"><span data-stu-id="c6514-135">**To role:** *System administrator*</span></span>

        > [!NOTE]
        > <span data-ttu-id="c6514-136">Bu senaryo demo verileri kullandığı için, *Sistem Yöneticisi* rolü kolaylık olması için seçilir.</span><span class="sxs-lookup"><span data-stu-id="c6514-136">Because this scenario uses demo data, the *System administrator* role is selected for the sake of simplicity.</span></span> <span data-ttu-id="c6514-137">Bu nedenle, Sistem Yöneticisi kullanıcısı olarak oturum açtığınızdan, bildirimleri alacaksınız.</span><span class="sxs-lookup"><span data-stu-id="c6514-137">Therefore, because you're signed in as a system administrator user, you will receive the notifications.</span></span> <span data-ttu-id="c6514-138">Ancak uygulamada, dalga toplu yürütme hatalarını bildirmek için genellikle *Ambar Yöneticisi* gibi daha belirli bir rol seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="c6514-138">However, in practice, you should usually select a more specific role to notify about wave batch execution errors, such as *Warehouse manager*.</span></span>

1. <span data-ttu-id="c6514-139">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c6514-139">On the Action Pane, select **Save**.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="c6514-140">Dalga şablonu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="c6514-140">Configure a wave template</span></span>

<span data-ttu-id="c6514-141">Dalga şablonları, belirli dalga yöntemi örneklerini ilgili dalga etiketi şablonlarına bağlayabilmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="c6514-141">Wave templates let you link specific instances of wave methods to corresponding wave label templates.</span></span>

1. <span data-ttu-id="c6514-142">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="c6514-142">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="c6514-143">Liste bölmesinde, **dalga şablonu türü** alanını *sevkiyat* olarak ayarlayın ve sonra da Ambar 24 için *24 sevkiyat varsayılan* dalga şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c6514-143">In the list pane, set the **Wave template type** field to *Shipping*, and then select the *24 Shipping Default* wave template for warehouse 24.</span></span>
1. <span data-ttu-id="c6514-144">**Genel** hızlı sekmesinde, **Dalga bildirim ilkesi** alanını *24BatchError* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c6514-144">On the **General** FastTab, set the **Wave notification policy** field to *24BatchError*.</span></span>

### <a name="configure-a-work-template"></a><span data-ttu-id="c6514-145">İş şablonu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="c6514-145">Configure a work template</span></span>

<span data-ttu-id="c6514-146">İş şablonları, dalga yürütmesi sırasında iş oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c6514-146">Work templates are used during wave execution to generate work.</span></span> <span data-ttu-id="c6514-147">Bu senaryoda, dalga yürütmenin bir hata tetiklemesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="c6514-147">For this scenario, wave execution should trigger an error.</span></span> <span data-ttu-id="c6514-148">İş şablonu sorgusunu varolmayan bir ambarı kullanacak şekilde ayarlayarak, dalga yürütmenin başarısız olmasını ve dolayısıyla bir bildirim göndermesini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="c6514-148">By setting the work template query to use a nonexistent warehouse, you will ensure that wave execution fails and therefore sends a notification.</span></span>

1. <span data-ttu-id="c6514-149">**Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="c6514-149">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="c6514-150">Liste bölmesinde, **İş şablonu türü** alanını *Satış emirleri* olarak ayarlayın ve sonra da Ambar 24 için *24 SO Aşaması* iş şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c6514-150">In the list pane, set the **Work template type** field to *Sales orders* and then select the *24 SO Stage* work template for warehouse 24.</span></span>
1. <span data-ttu-id="c6514-151">Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c6514-151">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="c6514-152">Sorgu Düzenleyicisi iletişim kutusunda **Aralık** sekmesinde aşağıdaki satırı düzenleyin (veya yoksa ekleyin):</span><span class="sxs-lookup"><span data-stu-id="c6514-152">In the query editor dialog box, on the **Range** tab, edit the following row (or add it if it doesn't exist):</span></span>

    - <span data-ttu-id="c6514-153">**Tablo:** *geçici iş hareketleri*</span><span class="sxs-lookup"><span data-stu-id="c6514-153">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="c6514-154">**Türetilmiş tablo:** *geçici iş hareketleri*</span><span class="sxs-lookup"><span data-stu-id="c6514-154">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="c6514-155">**Alan:** *Ambar*</span><span class="sxs-lookup"><span data-stu-id="c6514-155">**Field:** *Warehouse*</span></span>
    - <span data-ttu-id="c6514-156">**Ölçüt:** Değeri *24*'ten *Hata*'ya değiştirin.</span><span class="sxs-lookup"><span data-stu-id="c6514-156">**Criteria:** Change the value from *24* to *Error*.</span></span>

1. <span data-ttu-id="c6514-157">**Tamam**'ı seçin ve değişikliği onaylayın.</span><span class="sxs-lookup"><span data-stu-id="c6514-157">Select **OK**, and confirm the change.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="c6514-158">Satış siparişi oluşturma ve ambara serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="c6514-158">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="c6514-159">**Satış ve pazarlama \> Satış siparişi \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c6514-159">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="c6514-160">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="c6514-160">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="c6514-161">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c6514-161">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c6514-162">**Ambar:** *24*</span><span class="sxs-lookup"><span data-stu-id="c6514-162">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="c6514-163">**Satış siparişi satırları** hızlı sekmesinde, aşağıdaki ayarlara sahip satış emri satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="c6514-163">On the **Sales order lines** FastTab, add a sales order line that has the following settings:</span></span>

    - <span data-ttu-id="c6514-164">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="c6514-164">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="c6514-165">**Miktar:** *10*</span><span class="sxs-lookup"><span data-stu-id="c6514-165">**Quantity:** *10*</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6514-166">Bu maddeler ve miktarlar yalnızca örnektir.</span><span class="sxs-lookup"><span data-stu-id="c6514-166">These items and quantities are only examples.</span></span> <span data-ttu-id="c6514-167">Belirtilen ambarda yeterli stok bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c6514-167">The specified warehouse must contain enough stock.</span></span>

1. <span data-ttu-id="c6514-168">Yeni satır **Satış siparişi satırları** hızlı sekmesinde seçiliyken, araç çubuğunda **Stok \> Rezervasyon**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="c6514-168">While the new line is still selected on the **Sales order lines** FastTab, select **Inventory \> Reservation** on the toolbar.</span></span>
1. <span data-ttu-id="c6514-169">**Rezervasyon** sayfasında, eylem bölmesinde, **Lot ayır** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c6514-169">On the **Reservation** page, on the Action Pane, select **Reserve lot**.</span></span> <span data-ttu-id="c6514-170">Ardından sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c6514-170">Then close the page.</span></span>
1. <span data-ttu-id="c6514-171">Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c6514-171">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

### <a name="notifications-from-wave-batch-job-execution"></a><span data-ttu-id="c6514-172">Dalga toplu iş yürütmeden bildirimler</span><span class="sxs-lookup"><span data-stu-id="c6514-172">Notifications from wave batch job execution</span></span>

<span data-ttu-id="c6514-173">İş olaylarınızın kurulumuna bağlı olarak, sonuçta dalga yürütme hatası hakkında bir bildirim alacaksınız.</span><span class="sxs-lookup"><span data-stu-id="c6514-173">Depending on the setup of your business events, you will eventually receive a notification about wave execution failure.</span></span> <span data-ttu-id="c6514-174">Eylem Merkezi iletisi aşağıdaki örneğe benzeyecek ve başarısız olan bir dalgaya bağlantı içerecektir.</span><span class="sxs-lookup"><span data-stu-id="c6514-174">The Action center message will resemble the following example and will include a link to the wave that failed.</span></span>

> <span data-ttu-id="c6514-175">**Dalga yürütme sırasında hata oluştu**</span><span class="sxs-lookup"><span data-stu-id="c6514-175">**Error during wave execution**</span></span>  
> <span data-ttu-id="c6514-176">Dalga USMF-000000001 yürütülürken hata oluştu.</span><span class="sxs-lookup"><span data-stu-id="c6514-176">An error occurred while executing wave USMF-000000001.</span></span>  
> <span data-ttu-id="c6514-177">Son iletiler: Dalga USMF-000000001 için iş oluşturulmadı.</span><span class="sxs-lookup"><span data-stu-id="c6514-177">Last messages: No Work was created for Wave USMF-000000001.</span></span>
>
> <span data-ttu-id="c6514-178">**DURUM**</span><span class="sxs-lookup"><span data-stu-id="c6514-178">**STATUS**</span></span>  
> <span data-ttu-id="c6514-179">Active</span><span class="sxs-lookup"><span data-stu-id="c6514-179">Active</span></span>
>
> <span data-ttu-id="c6514-180">Dalga ayrıntılarını aç</span><span class="sxs-lookup"><span data-stu-id="c6514-180">Open wave details</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
