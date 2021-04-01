---
title: Dalga şablonu gruplandırması
description: Dalga şablonu gruplandırması, sistemin serbest bırakılan satırları nasıl böleceğini ve yeni ya da varolan dalgalara nasıl atayacağını (tanımladığınız ölçütlere dayanarak) belirlemek için dalga şablonu kurulumları kullanmasını sağlar. Bu özellik, dalgaların belirli ölçütlere göre oluşturulduğu ancak yöneticilerin dalgaları el ile değil otomatik oluşturmayı tercih ettikleri ambarlar için yararlı olabilir.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 520338683443105ffd1df7fc2569cd95a5f50879
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245142"
---
# <a name="wave-template-grouping"></a><span data-ttu-id="581b7-104">Dalga şablonu gruplandırması</span><span class="sxs-lookup"><span data-stu-id="581b7-104">Wave template grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="581b7-105">Dalga şablonu gruplandırması, sistemin serbest bırakılan satırları nasıl böleceğini ve yeni ya da varolan dalgalara nasıl atayacağını (tanımladığınız ölçütlere dayanarak) belirlemek için [dalga şablonu](tasks/configure-wave-processing.md) kurulumları kullanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="581b7-105">Wave template grouping enables the system to use [wave template](tasks/configure-wave-processing.md) setups to determine, based on criteria that you define, how it should split released lines and assign them to new or existing waves.</span></span> <span data-ttu-id="581b7-106">Bu özellik, dalgaların belirli ölçütlere göre oluşturulduğu ancak yöneticilerin dalgaları el ile değil otomatik oluşturmayı tercih ettikleri ambarlar için yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="581b7-106">This feature can be useful in warehouses where waves are created based on specific criteria, but where managers prefer to create waves automatically instead of manually.</span></span> <span data-ttu-id="581b7-107">Sistemin, eşleşen gruplandırma alan değerleri olduğunu saptadığı ilk dalgaya her yeni serbest bırakılan sevkiyatı eklemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="581b7-107">It enables the system to add each newly released shipment to the first wave that it finds that has matching grouping field values.</span></span> <span data-ttu-id="581b7-108">Eşleşme bulunamazsa, sistem yeni sevkiyat için yeni bir dalga oluşturur.</span><span class="sxs-lookup"><span data-stu-id="581b7-108">If no match is found, the system creates a new wave for the new shipment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="581b7-109">Dalga şablonu gruplandırması *üretim hammadde çekme* veya *Kanban çekme* iş türlerinde desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="581b7-109">Wave template grouping isn't supported for the work types *production raw material picking* or *Kanban picking*.</span></span> <span data-ttu-id="581b7-110">Bunun nedeni, dalga gruplandırmasının sevkiyatları temel alması ve bu iş türlerinin sevkiyatları kullanmamasıdır.</span><span class="sxs-lookup"><span data-stu-id="581b7-110">This is because wave grouping is based on shipments and these work types don't use shipments.</span></span>

## <a name="turn-on-the-wave-template-grouping-feature"></a><span data-ttu-id="581b7-111">Dalga şablonu gruplandırması özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="581b7-111">Turn on the Wave template grouping feature</span></span>

<span data-ttu-id="581b7-112">*Dalga şablonu gruplandırması* özelliğini kullanabilmeniz için sisteminizde etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="581b7-112">Before you can use the *Wave template grouping* feature, it must be turned on in your system.</span></span> <span data-ttu-id="581b7-113">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="581b7-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="581b7-114">**Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="581b7-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="581b7-115">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="581b7-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="581b7-116">**Özellik adı:** *Dalga şablonu gruplandırması*</span><span class="sxs-lookup"><span data-stu-id="581b7-116">**Feature name:** *Wave template grouping*</span></span>

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a><span data-ttu-id="581b7-117">Dalga şablonu gruplandırmasını kullanmak için bir dalga şablonu ayarlama</span><span class="sxs-lookup"><span data-stu-id="581b7-117">Set a wave template to use wave template grouping</span></span>

<span data-ttu-id="581b7-118">Dalga şablonu gruplandırmasını kullanılabilir hale getirmek için, bu adımları izleyerek [dalga şablonunuzu](tasks/configure-wave-processing.md) ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="581b7-118">To make wave template grouping available, follow these steps to set up your [wave template](tasks/configure-wave-processing.md).</span></span>

1. <span data-ttu-id="581b7-119">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="581b7-119">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="581b7-120">Sol bölmede, ayarlanacak dalga şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-120">In the left pane, select the wave template to set up.</span></span> <span data-ttu-id="581b7-121">Bu konudaki tanıtım verilerini kullanarak daha sonra senaryo üzerinde çalışmaya hazırlanıyorsanız, **62 Sevkiyat varsayılanı** şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-121">If you're preparing to work through the scenario later in this topic by using demo data, select the **62 Shipping default** template.</span></span>
1. <span data-ttu-id="581b7-122">Sayfayı düzenleme moduna sokmak için **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-122">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="581b7-123">**Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="581b7-123">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="581b7-124">**Dalga oluşturmayı otomatikleştir:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="581b7-124">**Automate wave creation:** *Yes*</span></span>
    - <span data-ttu-id="581b7-125">**Açık dalgalara ata:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="581b7-125">**Assign to open waves:** *Yes*</span></span>
    - <span data-ttu-id="581b7-126">**Dalgayı ambara serbest bırakma sırasında işle**: *Hayır*</span><span class="sxs-lookup"><span data-stu-id="581b7-126">**Process wave at release to warehouse:** *No*</span></span>

1. <span data-ttu-id="581b7-127">Eylem bölmesinde, **Sorguyu düzenle**'yi seçerek sorgu iletişim kutusunu açın.</span><span class="sxs-lookup"><span data-stu-id="581b7-127">On the Action Pane, select **Edit query** to open the query dialog box.</span></span>
1. <span data-ttu-id="581b7-128">Sorgu iletişim kutusundaki **Sıralama** sekmesinde sıralama ölçütlerini gözden geçirin ve dalgalarınızı gruplandırmak için kullanmak istediğiniz alanı içeren bir kural olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="581b7-128">In the query dialog box, on the **Sorting** tab, review the sorting criteria, and make sure that there is a rule that includes the field that you want to use to group your waves.</span></span>

    <span data-ttu-id="581b7-129">Tanıtım verilerini kullanarak senaryo üzerinden çalışmaya hazırlanıyorsanız aşağıdaki değerleri taşıyan bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="581b7-129">If you're preparing to work through the scenario by using demo data, add a row that has the following values:</span></span>

    - <span data-ttu-id="581b7-130">**Tablo:** *Sevkiyatlar*</span><span class="sxs-lookup"><span data-stu-id="581b7-130">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="581b7-131">**Türetilmiş tablo:** *Sevkiyatlar*</span><span class="sxs-lookup"><span data-stu-id="581b7-131">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="581b7-132">**Alan:** *Taşıyıcı hizmeti*</span><span class="sxs-lookup"><span data-stu-id="581b7-132">**Field:** *Carrier service*</span></span>

        > [!NOTE]
        > <span data-ttu-id="581b7-133">Bu değeri seçtikten sonra şu iletiyi alabilirsiniz: "Taşıyıcı hizmeti alanı bir dizin alanı değil.</span><span class="sxs-lookup"><span data-stu-id="581b7-133">After you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="581b7-134">Bunun üzerinde sıralama eklemek istiyor musunuz?"</span><span class="sxs-lookup"><span data-stu-id="581b7-134">Do you want to add sorting on this?"</span></span> <span data-ttu-id="581b7-135">Sıralama eklemek için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-135">Select **Yes** to add sorting.</span></span>

    - <span data-ttu-id="581b7-136">**Arama yönü:** *Artan*</span><span class="sxs-lookup"><span data-stu-id="581b7-136">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="581b7-137">Değişikliklerinizi kaydedip sorgu iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-137">Select **OK** to save your changes and close the query dialog box.</span></span>
1. <span data-ttu-id="581b7-138">Eylem bölmesinde, **Dalga şablonu gruplandırması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-138">On the Action Pane, select **Wave template grouping**.</span></span>
1. <span data-ttu-id="581b7-139">**Dalga şablonu gruplandırması** sayfasında, sipariş satırlarını dalgalar halinde gerektiği gibi gruplandırmak için kullanmak istediğiniz her satır için **Gruplandırma ölçütü** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="581b7-139">On the **Wave template grouping** page, select the **Group by** check box for each row that you want to use to group your order lines into waves, as required.</span></span> <span data-ttu-id="581b7-140">Tanıtım verilerini kullanarak senaryo üzerinden çalışmaya hazırlanıyorsanız, *Taşıyıcı hizmeti* satırı için **Gruplandırma ölçütü** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="581b7-140">If you're preparing to work through the scenario by using demo data, select the **Group by** check box for the *Carrier service* row.</span></span>
1. <span data-ttu-id="581b7-141">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-141">Select **Save**.</span></span>
1. <span data-ttu-id="581b7-142">**Dalga şablonu gruplandırması** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="581b7-142">Close the **Wave template grouping** page.</span></span>
1. <span data-ttu-id="581b7-143">Şablonunuzu kaydetmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-143">Select **Save** to save your template.</span></span>

## <a name="scenario"></a><span data-ttu-id="581b7-144">Senaryo</span><span class="sxs-lookup"><span data-stu-id="581b7-144">Scenario</span></span>

<span data-ttu-id="581b7-145">Bu bölüm, özelliğin ne yaptığını ve bu özellikle nasıl çalışılacağını öğrenmek için kullanabileceğiniz bir metin sunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="581b7-145">This section provides a script that you can work through to learn what this feature does and how to work with it.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="581b7-146">Örnek verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="581b7-146">Make sample data available</span></span>

<span data-ttu-id="581b7-147">Burada belirtilen örnek kayıtları ve değerleri kullanarak bu senaryo üzerinden çalışmak için, standart [tanıtım verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="581b7-147">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="581b7-148">Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="581b7-148">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="581b7-149">Bu senaryodan, üretim sisteminde çalışırken özelliği kullanmaya yönelik kılavuz olarak da yararlanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="581b7-149">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="581b7-150">Ancak, bu durumda kendi değerlerinizi değiştirmeniz gerekir ve standart tanıtım verilerinin sağladığı bazı gerekli kayıt türleri kaybolabilir.</span><span class="sxs-lookup"><span data-stu-id="581b7-150">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="scenario-wave-template-grouping"></a><span data-ttu-id="581b7-151">Senaryo: Dalga şablonu gruplandırması</span><span class="sxs-lookup"><span data-stu-id="581b7-151">Scenario: Wave template grouping</span></span>

<span data-ttu-id="581b7-152">Bu senaryo, bir dalga şablonunda tanımlanan gruplandırma ölçütlerine göre çoklu dalgaları otomatik olarak oluşturmak için dalga şablonu gruplandırmasının nasıl kullanılacağını gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="581b7-152">This scenario shows how to use wave template grouping to automatically create multiple waves, based on grouping criteria that are defined in a wave template.</span></span> <span data-ttu-id="581b7-153">Bu senaryoda, dalga şablonu, sistemde taşıyıcı hizmeti başına bir dalga oluşturmak üzere ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="581b7-153">In this scenario, the wave template is set up in the system to create one wave per carrier service.</span></span>

<span data-ttu-id="581b7-154">Başlamadan önce, bu konuda daha önce ele alınan [Dalga şablonu gruplandırmasını kullanmak için bir dalga şablonu ayarlama](#set-up-template) bölümünde açıklandığı şekilde dalga şablonunuzu hazırlayın.</span><span class="sxs-lookup"><span data-stu-id="581b7-154">Before you begin, prepare your wave template as described in the [Set a wave template to use wave template grouping](#set-up-template) section earlier in this topic.</span></span> <span data-ttu-id="581b7-155">Bu senaryo için tanıtım verileriyle çalışacaksanız, o yordamda önerilen tanıtım veri değerlerini kullandığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="581b7-155">If you will be working with demo data for this scenario, be sure to use the demo data values that are suggested in that procedure.</span></span> <span data-ttu-id="581b7-156">Bu kurulum, dalgalarınızı her bir satış siparişi için ayarlanan taşıyıcı hizmetine göre gruplandıracaktır.</span><span class="sxs-lookup"><span data-stu-id="581b7-156">This setup will group your waves according to the carrier service that is set for each sales order.</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="581b7-157">Satış siparişi oluşturma 1</span><span class="sxs-lookup"><span data-stu-id="581b7-157">Create sales order 1</span></span>

1. <span data-ttu-id="581b7-158">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="581b7-158">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="581b7-159">Satış siparişi oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-159">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="581b7-160">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="581b7-160">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="581b7-161">**Müşteri** hızlı sekmesinde, **Müşteri hesabı** alanını *ABD-004* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="581b7-161">On the **Customer** FastTab, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="581b7-162">**Genel** hızlı sekmesinde, **Ambar** alanının ayarını *62* yapın.</span><span class="sxs-lookup"><span data-stu-id="581b7-162">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="581b7-163">Satış siparişini oluşturmak ve **Satış siparişi oluştur** iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-163">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="581b7-164">Yeni satış siparişi **Satırlar** görünümünde açılır.</span><span class="sxs-lookup"><span data-stu-id="581b7-164">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="581b7-165">Satış siparişi numarasını not edin.</span><span class="sxs-lookup"><span data-stu-id="581b7-165">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="581b7-166">**Üst bilgi** görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-166">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="581b7-167">**Teslimat** hızlı sekmesinde, **Taşıma** bölümünde aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="581b7-167">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="581b7-168">**Sevkiyat taşıyıcısı:** *Hava nakliyesi*</span><span class="sxs-lookup"><span data-stu-id="581b7-168">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="581b7-169">**Taşıyıcı hizmeti:** *Hava*</span><span class="sxs-lookup"><span data-stu-id="581b7-169">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="581b7-170">**Satırlar** görünümüne dönün.</span><span class="sxs-lookup"><span data-stu-id="581b7-170">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="581b7-171">**Satış siparişi satırları** bölümünde, kılavuza satır maddesi eklemek için **Satır ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-171">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="581b7-172">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="581b7-172">On the new line, set the following values:</span></span>

    - <span data-ttu-id="581b7-173">**Madde numarası:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="581b7-173">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="581b7-174">**Miktar:** *2*</span><span class="sxs-lookup"><span data-stu-id="581b7-174">**Quantity:** *2*</span></span>

1. <span data-ttu-id="581b7-175">Yeni sipariş satırını seçin ve ardından kılavuzun yukarısındaki **Stok** menüsünde **Rezervasyon**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-175">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="581b7-176">**Rezervasyon** sayfasında, Eylem bölmesinde, ambardaki seçili satırın tüm miktarını rezerve etmek için **Lot ayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-176">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="581b7-177">Satış siparişine dönmek için **Rezervasyon** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="581b7-177">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="581b7-178">Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda, **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-178">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="581b7-179">Bu sipariş için sevkiyatı ve dalgayı gösteren bir bilgi iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="581b7-179">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="581b7-180">Dalga kodu numarasını ve sevkiyat kodu numaralarını not edin.</span><span class="sxs-lookup"><span data-stu-id="581b7-180">Make a note of the wave ID number and the shipment ID numbers.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a><span data-ttu-id="581b7-181">Satış siparişi 1'den oluşturulan dalgayı görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="581b7-181">View the wave that was created from sales order 1</span></span>

1. <span data-ttu-id="581b7-182">**Ambar yönetimi \> Giden dalgalar \> Sevkiyat dalgaları \> Tüm dalgalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="581b7-182">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="581b7-183">Satış siparişinden oluşturulan dalga kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-183">Select the wave ID that was created from the sales order.</span></span>
1. <span data-ttu-id="581b7-184">Dalga ayrıntıları sayfasını açmak için dalga kodu bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-184">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="581b7-185">Sevkiyatın **Dalga satırları** hızlı sekmesine eklendiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="581b7-185">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="581b7-186">Satış siparişi oluşturma 2</span><span class="sxs-lookup"><span data-stu-id="581b7-186">Create sales order 2</span></span>

1. <span data-ttu-id="581b7-187">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="581b7-187">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="581b7-188">Satış siparişi oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-188">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="581b7-189">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="581b7-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="581b7-190">**Müşteri** hızlı sekmesinde, **Müşteri hesabı** alanını *ABD-005* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="581b7-190">On the **Customer** FastTab, set the **Customer account** field to *US-005*.</span></span>
    - <span data-ttu-id="581b7-191">**Genel** hızlı sekmesinde, **Ambar** alanının ayarını *62* yapın.</span><span class="sxs-lookup"><span data-stu-id="581b7-191">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="581b7-192">Satış siparişini oluşturmak ve **Satış siparişi oluştur** iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-192">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="581b7-193">Yeni satış siparişi **Satırlar** görünümünde açılır.</span><span class="sxs-lookup"><span data-stu-id="581b7-193">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="581b7-194">Satış siparişi numarasını not edin.</span><span class="sxs-lookup"><span data-stu-id="581b7-194">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="581b7-195">**Üst bilgi** görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-195">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="581b7-196">**Teslimat** hızlı sekmesinde, **Taşıma** bölümünde aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="581b7-196">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="581b7-197">**Sevkiyat taşıyıcısı:** *Çiçek taşıma*</span><span class="sxs-lookup"><span data-stu-id="581b7-197">**Shipping carrier:** *Flower moving*</span></span>
    - <span data-ttu-id="581b7-198">**Taşıyıcı hizmeti:** *Std*</span><span class="sxs-lookup"><span data-stu-id="581b7-198">**Carrier service:** *Std*</span></span>

1. <span data-ttu-id="581b7-199">**Satırlar** görünümüne dönün.</span><span class="sxs-lookup"><span data-stu-id="581b7-199">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="581b7-200">**Satış siparişi satırları** bölümünde, kılavuza satır maddesi eklemek için **Satır ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-200">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="581b7-201">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="581b7-201">On the new line, set the following values:</span></span>

    - <span data-ttu-id="581b7-202">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="581b7-202">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="581b7-203">**Miktar:** *1*</span><span class="sxs-lookup"><span data-stu-id="581b7-203">**Quantity:** *1*</span></span>

1. <span data-ttu-id="581b7-204">Yeni sipariş satırını seçin ve ardından kılavuzun yukarısındaki **Stok** menüsünde **Rezervasyon**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-204">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="581b7-205">**Rezervasyon** sayfasında, Eylem bölmesinde, ambardaki seçili satırın tüm miktarını rezerve etmek için **Lot ayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="581b7-206">Satış siparişine dönmek için **Rezervasyon** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="581b7-206">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="581b7-207">Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda, **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-207">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="581b7-208">Bu sipariş için sevkiyatı ve dalgayı gösteren bir bilgi iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="581b7-208">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="581b7-209">Dalga kodu numarasını ve sevkiyat kodu numaralarını not edin.</span><span class="sxs-lookup"><span data-stu-id="581b7-209">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="581b7-210">Dalga kodunun ilk satış siparişinin dalga kodundan farklı olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="581b7-210">Notice that the wave ID differs from the wave ID of the first sales order.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a><span data-ttu-id="581b7-211">Satış siparişi 2'den oluşturulan dalgayı görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="581b7-211">View the wave that was created from sales order 2</span></span>

1. <span data-ttu-id="581b7-212">**Ambar yönetimi \> Giden dalgalar \> Sevkiyat dalgaları \> Tüm dalgalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="581b7-212">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="581b7-213">İkinci satış siparişinden oluşturulan dalga kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-213">Select the wave ID that was created from the second sales order.</span></span>
1. <span data-ttu-id="581b7-214">Dalga ayrıntıları sayfasını açmak için dalga kodu bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-214">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="581b7-215">Sevkiyatın **Dalga satırları** hızlı sekmesine eklendiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="581b7-215">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

<span data-ttu-id="581b7-216">Bu sevkiyat için yeni bir dalga oluşturulmuştur çünkü ilk satış siparişinden farklı bir taşıyıcı hizmeti kullanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="581b7-216">A new wave was created for this shipment, because it uses a different carrier service than the first sales order.</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="581b7-217">Satış siparişi oluşturma 3</span><span class="sxs-lookup"><span data-stu-id="581b7-217">Create sales order 3</span></span>

1. <span data-ttu-id="581b7-218">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="581b7-218">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="581b7-219">Satış siparişi oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-219">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="581b7-220">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="581b7-220">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="581b7-221">**Müşteri** hızlı sekmesinde, **Müşteri hesabı** alanını *ABD-006* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="581b7-221">On the **Customer** FastTab, set the **Customer account** field to *US-006*.</span></span>
    - <span data-ttu-id="581b7-222">**Genel** hızlı sekmesinde, **Ambar** alanının ayarını *62* yapın.</span><span class="sxs-lookup"><span data-stu-id="581b7-222">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="581b7-223">Satış siparişini oluşturmak ve **Satış siparişi oluştur** iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-223">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="581b7-224">Yeni satış siparişi **Satırlar** görünümünde açılır.</span><span class="sxs-lookup"><span data-stu-id="581b7-224">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="581b7-225">Satış siparişi numarasını not edin.</span><span class="sxs-lookup"><span data-stu-id="581b7-225">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="581b7-226">**Üst bilgi** görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-226">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="581b7-227">**Teslimat** hızlı sekmesinde, **Taşıma** bölümünde aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="581b7-227">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="581b7-228">**Sevkiyat taşıyıcısı:** *Hava Nakliyesi*</span><span class="sxs-lookup"><span data-stu-id="581b7-228">**Shipping carrier:** *Air Cargo*</span></span>
    - <span data-ttu-id="581b7-229">**Taşıyıcı hizmeti:** *Hava*</span><span class="sxs-lookup"><span data-stu-id="581b7-229">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="581b7-230">**Satırlar** görünümüne dönün.</span><span class="sxs-lookup"><span data-stu-id="581b7-230">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="581b7-231">**Satış siparişi satırları** bölümünde, kılavuza satır maddesi eklemek için **Satır ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-231">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="581b7-232">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="581b7-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="581b7-233">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="581b7-233">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="581b7-234">**Miktar:** *1*</span><span class="sxs-lookup"><span data-stu-id="581b7-234">**Quantity:** *1*</span></span>

1. <span data-ttu-id="581b7-235">Yeni sipariş satırını seçin ve ardından kılavuzun yukarısındaki **Stok** menüsünde **Rezervasyon**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-235">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="581b7-236">**Rezervasyon** sayfasında, Eylem bölmesinde, ambardaki seçili satırın tüm miktarını rezerve etmek için **Lot ayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-236">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="581b7-237">Satış siparişine dönmek için **Rezervasyon** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="581b7-237">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="581b7-238">Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda, **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-238">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="581b7-239">Bu sipariş için sevkiyatı ve dalgayı gösteren bir bilgi iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="581b7-239">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="581b7-240">Dalga kodu numarasını ve sevkiyat kodu numaralarını not edin.</span><span class="sxs-lookup"><span data-stu-id="581b7-240">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="581b7-241">Sevkiyat, ilk satış siparişinden varolan dalgaya atanmıştır.</span><span class="sxs-lookup"><span data-stu-id="581b7-241">The shipment has been assigned to the existing wave from the first sales order.</span></span>

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a><span data-ttu-id="581b7-242">1 ve 3 numaralı satış siparişleriyle ilgili dalgayı görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="581b7-242">View the wave for sales orders 1 and 3</span></span>

1. <span data-ttu-id="581b7-243">**Ambar yönetimi \> Giden dalgalar \> Sevkiyat dalgaları \> Tüm dalgalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="581b7-243">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="581b7-244">Üçüncü satış siparişinden oluşturulan dalga kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-244">Select the wave ID that was created from the third sales order.</span></span>
1. <span data-ttu-id="581b7-245">Dalga ayrıntıları sayfasını açmak için dalga kodu bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="581b7-245">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="581b7-246">İlk satış siparişi için sevkiyatla birlikte, sevkiyatın **Dalga satırları** hızlı sekmesine eklendiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="581b7-246">Notice that the shipment has been added to the **Wave lines** FastTab, together with the shipment for the first sales order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]