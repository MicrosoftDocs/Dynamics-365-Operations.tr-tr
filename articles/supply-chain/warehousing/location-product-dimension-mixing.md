---
title: Yerleşim ürün boyutu karıştırması
description: Bu konu, konum ürün boyutu karıştırma hakkında bilgiler sağlar. Bu konum profili işlevi, kullanım sektörü gibi ürün çeşitleri veya boyutları olan ürünler kullanıldığında yerleşim yönetiminin artırılmasına yardımcı olur. Konfigürasyonların, renklerin, stillerin ve boyutların belirli bir yerleşim profili için karıştırılıp karışlamayacağını veya bu boyutlardan yalnızca birinin veya bunların bir bileşimin aynı konuma konulacağını belirlemenize olanak tanır.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: c4e42864bfde9ed0650a88961b5a71b33b34c89d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004614"
---
# <a name="location-product-dimension-mixing"></a><span data-ttu-id="e5d7d-105">Yerleşim ürün boyutu karıştırması</span><span class="sxs-lookup"><span data-stu-id="e5d7d-105">Location product dimension mixing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5d7d-106">Konum ürün boyutu karıştırma, kullanım sektörü gibi ürün çeşitleri veya boyutları olan ürünler kullanıldığında yerleşim yönetiminin artırılmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-106">Location product dimension mixing is location profile functionality that helps improve location management when product variants or products that have dimensions are used, such as in the fashion industry.</span></span> <span data-ttu-id="e5d7d-107">Konfigürasyonların, renklerin, stillerin ve boyutların belirli bir yerleşim profili için karıştırılıp karışlamayacağını veya bu boyutlardan yalnızca birinin veya bunların bir bileşimin aynı konuma konulacağını belirlemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-107">It lets you decide whether configurations, colors, styles, and sizes can be mixed for a specific location profile, or whether just one of these dimensions or a combination of them can be put to the same location.</span></span>

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a><span data-ttu-id="e5d7d-108">Ürün boyut karıştırma özelliğini aç</span><span class="sxs-lookup"><span data-stu-id="e5d7d-108">Turn on the Location product dimension mixing feature</span></span>

<span data-ttu-id="e5d7d-109">Konum ürün boyutu karıştırma özelliğini kullanabilmeniz için sisteminizde etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-109">Before you can use location product dimension mixing, the feature must be turned on in your system.</span></span> <span data-ttu-id="e5d7d-110">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="e5d7d-111">Burada, özellik aşağıdaki şekilde listelenmiştir:</span><span class="sxs-lookup"><span data-stu-id="e5d7d-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e5d7d-112">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="e5d7d-113">**Özellik adı:** *Konum Ürün boyut karıştırma*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-113">**Feature name:** *Location product dimension mixing*</span></span>

## <a name="setup"></a><span data-ttu-id="e5d7d-114">Ayar</span><span class="sxs-lookup"><span data-stu-id="e5d7d-114">Setup</span></span>

<span data-ttu-id="e5d7d-115">Ambardaki her konumun, konum özelliklerini açıklayan, kendisiyle ilişkili bir konum profiline sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-115">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location.</span></span> <span data-ttu-id="e5d7d-116">Bu nedenle, oluşturulduktan sonra, aynı yerleşim profilini kullanan tüm konumlar ürün boyutu karıştırmaya izin verebilir.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-116">Therefore, all locations that use the same location profile will be able to allow product dimension mixing after it has been set up.</span></span>

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a><span data-ttu-id="e5d7d-117">Ürün boyutu karıştırılmasına izin vermek için yerleşim profillerini konfigüre et</span><span class="sxs-lookup"><span data-stu-id="e5d7d-117">Configure location profiles to allow product dimension mixing</span></span>

1. <span data-ttu-id="e5d7d-118">**Ambar yönetimi \> Kurulum \> Ambar \> Konum profilleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-118">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="e5d7d-119">Yerleşim profilleri listesinde **toplu** 'u seçin .</span><span class="sxs-lookup"><span data-stu-id="e5d7d-119">In the list of location profiles, select **BULK**.</span></span>
1. <span data-ttu-id="e5d7d-120">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-120">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="e5d7d-121">**Genel** hızlı sekmesinde, **ürün boyutuna özel karıştırma** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-121">On the **General** FastTab, set the **Enable location product dimension specific mixing** option to *Yes*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e5d7d-122">Bu seçeneği yalnızca, **karışık öğelere izin ver** seçeneği *Hayır* olarak ayarlanmışsa *Evet* olarak ayarlayabilirsiniz .</span><span class="sxs-lookup"><span data-stu-id="e5d7d-122">You can set this option to *Yes* only if the **Allow mixed items** option is set to *No*.</span></span>

1. <span data-ttu-id="e5d7d-123">**İzin verilen ürün boyutlandırma karışımı** hızlı sekmesinde, **Boyut** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-123">On the **Allowed product dimension mixing** FastTab, set the **Size** option to *Yes*.</span></span> <span data-ttu-id="e5d7d-124">Bu konuda açıklanan senaryoda, karıştırma yalnızca farklı **boyut** boyutları olan ürünler için yapılabilir .</span><span class="sxs-lookup"><span data-stu-id="e5d7d-124">In the scenario that is described in this topic, mixing can be done only for products that have different **Size** dimensions.</span></span> <span data-ttu-id="e5d7d-125">Ancak diğer seçenekler de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-125">However, other options are also available.</span></span>
1. <span data-ttu-id="e5d7d-126">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-126">Select **Save**.</span></span>

### <a name="create-a-new-product-master-and-product-variants"></a><span data-ttu-id="e5d7d-127">Yeni ana ürünler ve ürün çeşitleri oluşturun</span><span class="sxs-lookup"><span data-stu-id="e5d7d-127">Create a new product master and product variants</span></span>

1. <span data-ttu-id="e5d7d-128">**Ürün bilgi yönetimi \> Ürünler \> Ana ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-128">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="e5d7d-129">Eylem bölmesinde **Yeni**'yi seçerek ürün uzmanı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-129">On the Action Pane, select **New** to create a product master.</span></span>
1. <span data-ttu-id="e5d7d-130">**Yeni ürün** iletişim kutusunda aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-130">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e5d7d-131">**Ürün türü:** *Madde*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-131">**Product type:** *Item*</span></span>
    - <span data-ttu-id="e5d7d-132">**Ürün alt türü:** *Ürün Yöneticisi*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-132">**Product subtype:** *Product master*</span></span>
    - <span data-ttu-id="e5d7d-133">**Ürün numarası:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-133">**Product number:** *B0001*</span></span>
    - <span data-ttu-id="e5d7d-134">**Ürün adı:** *B0001 boyutu*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-134">**Product name:** *B0001 Size*</span></span>
    - <span data-ttu-id="e5d7d-135">**Ürün boyut grubu:** *Boyut*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-135">**Product dimension group:** *Size*</span></span>
    - <span data-ttu-id="e5d7d-136">**Yapılandırma teknolojisi:** *Önceden tanımlanan değişken*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-136">**Configuration technology:** *Predefined variant*</span></span>

1. <span data-ttu-id="e5d7d-137">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-137">Select **OK**.</span></span>
1. <span data-ttu-id="e5d7d-138">**Ürün ayrıntıları** sayfasında, **genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e5d7d-138">On the **Product details** page, on the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e5d7d-139">**Çeşitleri otomatik olarak oluştur:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-139">**Generate variants automatically:** *Yes*</span></span>
    - <span data-ttu-id="e5d7d-140">**Boyut grubu:** *CASUALDHIR*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-140">**Size group:** *CASUALDHIR*</span></span>

1. <span data-ttu-id="e5d7d-141">Önceden tanımlanmış varyantları görüntülemek için eylem bölmesinde **ürün varyantlarını** seçin .</span><span class="sxs-lookup"><span data-stu-id="e5d7d-141">To view the predefined variants, on the Action Pane, select **Product variants**.</span></span>

    <span data-ttu-id="e5d7d-142">**Ürün çeşitleri** sayfası görüntülenir ve boyut grubu konfigürasyonundaki varyantlar listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-142">The **Product variants** page appears and shows a list of variants from the configuration of the size group.</span></span>

### <a name="release-products-to-the-usmf-company"></a><span data-ttu-id="e5d7d-143">USMF şirketi ürünlerini serbest bırakın</span><span class="sxs-lookup"><span data-stu-id="e5d7d-143">Release products to the USMF company</span></span>

1. <span data-ttu-id="e5d7d-144">Eylem bölmesinde **Ürünleri kullanıma sun**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-144">On the Action Pane, select **Release products**.</span></span>
1. <span data-ttu-id="e5d7d-145">**Serbest bırakmak için ürünleri seçin** sayfasında, ürün numarası *B0001* listede olduğunu onaylayın ve **ileri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-145">On the **Select products to release** page, confirm that product number *B0001* is in the list, and then select **Next**.</span></span>
1. <span data-ttu-id="e5d7d-146">Serbest bırakmak üzere ürün varyantlarını onaylamak için **ileri** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-146">Select **Next** to confirm the product variants to release.</span></span>
1. <span data-ttu-id="e5d7d-147">**Yayınlanacak firmaları seçin** sayfasında, *USMF*'yi seçin ve sonra seçimi onaylamak için **ileri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-147">On the **Select companies to release to** page, select *USMF*, and then select **Next** to confirm the selection.</span></span>
1. <span data-ttu-id="e5d7d-148">**Seçimi Onayla** sayfasında, yayımı tamamlamak için **son**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-148">On the **Confirm selection** page, select **Finish** to complete the release.</span></span>

    <span data-ttu-id="e5d7d-149">Bir "İş Tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-149">You receive an "Operation completed" message.</span></span>

### <a name="update-a-released-product-in-the-usmf-company"></a><span data-ttu-id="e5d7d-150">USMF şirketinde yayınlanmış bir ürünü güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e5d7d-150">Update a released product in the USMF company</span></span>

1. <span data-ttu-id="e5d7d-151">**USMF** şirketinde oturum açtığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-151">Make sure that you're signed in to the **USMF** company.</span></span>
1. <span data-ttu-id="e5d7d-152">Serbest bırakılan ürün ayrıntıları sayfasını açmak için **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılan ürünler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-152">Go to **Product information management \> Products \> Released products** to finish creating the released product.</span></span>
1. <span data-ttu-id="e5d7d-153">**Serbest bırakılmış ürün ayrıntıları** sayfasını açmak için madde numarası *B0001* bulun ve seçin .</span><span class="sxs-lookup"><span data-stu-id="e5d7d-153">Find and select item number *B0001* to open the **Released product details** page.</span></span>
1. <span data-ttu-id="e5d7d-154">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-154">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="e5d7d-155">**Genel** hızlı sekmesinde, **Madde modeli grubu** alanının *FIFO* olarak ayarlandığından emin olun .</span><span class="sxs-lookup"><span data-stu-id="e5d7d-155">On the **General** FastTab, make sure that the **Item model group** field is set to *FIFO*.</span></span>
1. <span data-ttu-id="e5d7d-156">Eylem Bölmesi'nde, **Ürün** sekmesindeki **Ayar** gurubunda **Boyut grupları**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-156">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Dimension groups**.</span></span>
1. <span data-ttu-id="e5d7d-157">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e5d7d-157">Set the following values:</span></span>

    - <span data-ttu-id="e5d7d-158">**Depolama boyutu grubu:** *Ambar*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-158">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="e5d7d-159">**İzleme boyutu grubu:** *Yok*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-159">**Tracking dimension group:** *None*</span></span>

1. <span data-ttu-id="e5d7d-160">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-160">Select **OK**.</span></span>
1. <span data-ttu-id="e5d7d-161">Eylem Bölmesi'nde, **Ürün** sekmesindeki **Ayar** gurubunda **Rezervasyon hiyerarşisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-161">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Reservation hierarchy**.</span></span>
1. <span data-ttu-id="e5d7d-162">**Rezervasyon hiyerarşisi** alanını *varsayılan* olarak ayarlayın ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-162">Set the **Reservation hierarchy** field to *Default*, and then select **OK**.</span></span>
1. <span data-ttu-id="e5d7d-163">**Genel** hızlı sekmesinde, **Yönetim** bölümünde seçimlerinizin güncelleştirilmiş olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-163">On the **General** FastTab, in the **Administration** section, notice that your selections have been updated.</span></span>
1. <span data-ttu-id="e5d7d-164">**Satın alma** hızlı sekmesinde, **Fiyat** alanında, *10* girin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-164">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="e5d7d-165">**Maliyetleri yönet** hızlı sekmesinde, **Madde grubu** alanında *Ses* girin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-165">On the **Manage costs** FastTab, in the **Item group** field, enter *Audio*.</span></span>
1. <span data-ttu-id="e5d7d-166">**Satın alma** hızlı sekmesinde, **Fiyat** alanında, *10* girin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-166">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="e5d7d-167">**Ambar** hızlı sekmesinde, **Ünite sıralama grubu kodu** alanına, *beher*'ı girin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-167">On the **Warehouse** FastTab, in the **Unit sequence group ID** field, enter *ea*.</span></span>
1. <span data-ttu-id="e5d7d-168">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-168">Select **Save**.</span></span>

### <a name="create-a-location-directive"></a><span data-ttu-id="e5d7d-169">Yerleşim yönergeleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="e5d7d-169">Create a location directive</span></span>

1. <span data-ttu-id="e5d7d-170">**Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-170">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="e5d7d-171">Sol bölmedeki **İş emri türü** alanında *Satın alma emirleri*'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-171">In the left pane, in the **Work order type** field, select *Purchase orders*.</span></span>
1. <span data-ttu-id="e5d7d-172">Listede, *24 SAS Direct* olarak adlandırılan konum yönergesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-172">In the list, select the location directive that is named *24 PO Direct*.</span></span>
1. <span data-ttu-id="e5d7d-173">**Konum Yönerge Eylemleri** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-173">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="e5d7d-174">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e5d7d-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="e5d7d-175">**Sıra numarası:** *1*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-175">**Sequence number:** *1*</span></span>

        <span data-ttu-id="e5d7d-176">Yeni satır önceden varolan satırın önünde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-176">The new line should be in front of the previously existing line.</span></span> <span data-ttu-id="e5d7d-177">Değişikliği yapmak için, araç çubuğunda **yukarı taşı** ve **Aşağı Taşı** düğmelerini kullanın veya varolan satırın **sıra numarası** değerini *2* olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-177">To make the change, use the **Move up** and **Move down** buttons on the toolbar, or change the existing line's **Sequence number** value to *2*.</span></span>

    - <span data-ttu-id="e5d7d-178">**Ad:** *toplu yerleşim profiline koy*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-178">**Name:** *Put to BULK Location profile*</span></span>
    - <span data-ttu-id="e5d7d-179">**Sabit yerleşim kullanımı:** *Sabit ve sabit olmayan yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-179">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>
    - <span data-ttu-id="e5d7d-180">**Negatif stoka izin ver:** *Bu onay kutusunun işaretini kaldırın (=Hayır)*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-180">**Allow negative inventory:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="e5d7d-181">**Toplu iş etkin:** *Bu onay kutusunun işaretini kaldırın (=Hayır)*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-181">**Batch enabled:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="e5d7d-182">**Strateji:** *Yok*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-182">**Strategy:** *None*</span></span>

1. <span data-ttu-id="e5d7d-183">Yeni satır seçiliyken, kılavuzun üzerinde **Düzenle sorgu** seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-183">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="e5d7d-184">Sorgu iletişim kutusundaki **Aralık** sekmesinde **Ekle**'yi seçerek kılavuza bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e5d7d-184">In the query dialog box, on the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="e5d7d-185">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e5d7d-185">On the new line, set the following values:</span></span>

    - <span data-ttu-id="e5d7d-186">**Tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-186">**Table:** *Locations*</span></span>
    - <span data-ttu-id="e5d7d-187">**Türetilmiş tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-187">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="e5d7d-188">**Alan:** *Yerleşim profili kodu*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-188">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="e5d7d-189">**Ölçüt:** *BULK*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-189">**Criteria:** *BULK*</span></span>

1. <span data-ttu-id="e5d7d-190">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-190">Select **OK**.</span></span>
1. <span data-ttu-id="e5d7d-191">**Konum direktifleri** sayfasında, yeni yerleşim yönergesini kaydetmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-191">On the **Location directives** page, on the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="e5d7d-192">**Konum yönergesi eylemleri** Hızlı sekmesi **strateji** alanında, *Sağlamlaştırma* konum stratejisini kullanırsanız **yerleşim profillerinde** **izin verilen ürün boyut karıştırma** hızlı sekmesinin kurulumu geçersiz kılınır ve bu davranışa kurulum tarafından izin verilmese bile maddeler aynı yerleşime yerleştirilir.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-192">On the **Location Directive Actions** FastTab **Strategy** field, if you use the *Consolidate* location strategy, the setup of the **Allowed product dimension mixing** FastTab on the **Location profiles** will be overridden, and items will be put to the same location even if this behavior isn't allowed by the setup.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="e5d7d-193">Mobil cihaz menü öğesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e5d7d-193">Create a mobile device menu item</span></span>

1. <span data-ttu-id="e5d7d-194">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-194">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="e5d7d-195">Eylem bölmesinde, sıralama amacıyla kullanılacak menü öğesini oluşturmak için **yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-195">On the Action Pane, select **New** to create a menu item to use for sorting.</span></span>
1. <span data-ttu-id="e5d7d-196">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e5d7d-196">In the header, set the following values:</span></span>

    - <span data-ttu-id="e5d7d-197">**Menü madde adı:** *Satınalma siparişi satın alma*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-197">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="e5d7d-198">**Başlık:** *Satınalma siparişi satın alma*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-198">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="e5d7d-199">**Mod:** *İş*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-199">**Mode:** *Work*</span></span>
    - <span data-ttu-id="e5d7d-200">**Varolan çalışmayı kullan:** *Hayır*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-200">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="e5d7d-201">**Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e5d7d-201">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e5d7d-202">**İş oluşturma işlemi:** *Satınalma siparişi satırı alma ve yerleştirme*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-202">**Work creation process:** *Purchase order line receiving and putaway*</span></span>
    - <span data-ttu-id="e5d7d-203">**Plaka oluştur:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-203">**Generate license plate:** *Yes*</span></span>

1. <span data-ttu-id="e5d7d-204">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-204">Select **Save**.</span></span>

### <a name="configure-the-mobile-device-menu"></a><span data-ttu-id="e5d7d-205">Mobil cihaz menüsünü yapılandırma</span><span class="sxs-lookup"><span data-stu-id="e5d7d-205">Configure the mobile device menu</span></span>

1. <span data-ttu-id="e5d7d-206">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="e5d7d-207">Menüler listesinde **Gelen**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-207">In the list of menus, select **Inbound**.</span></span>
1. <span data-ttu-id="e5d7d-208">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-208">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="e5d7d-209">**Mevcut menüler ve menü öğeleri** listesinde, **SAS satırı teslim** menüsü maddesini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-209">In the **Available Menus And Menu Items** list, find and select the **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="e5d7d-210">**SAS satırı alma** menü öğesini **menü yapısı** listesine taşımak için sağ ok düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-210">Select the right arrow button to move the **PO line receiving** menu item to the **Menu Structure** list.</span></span> <span data-ttu-id="e5d7d-211">Böylece, yeni menü öğesini seçili menüye eklersiniz.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-211">In this way, you add your new menu item to the selected menu.</span></span>
1. <span data-ttu-id="e5d7d-212">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-212">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="e5d7d-213">Senaryo</span><span class="sxs-lookup"><span data-stu-id="e5d7d-213">Scenario</span></span>

<span data-ttu-id="e5d7d-214">Bu gösteri senaryosu, *yerleşim profili karışık maddeler* için izin vermediği halde Ürün boyutu karıştırma özelliği etkin olduğunda, iki farklı ürün varyantın aynı yerleşime nasıl koyulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-214">This demo scenario shows how two different product variants can be put to the same location when the location profile doesn't allow for mixed items, but the *Location product dimension mixing* feature is enabled.</span></span> <span data-ttu-id="e5d7d-215">Bu durumda **ölçüt** olarak size varyantını kullanacaksınız.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-215">In this case, you will use the **Size** variant as the criterion.</span></span>

<span data-ttu-id="e5d7d-216">Başlamadan önce, ambar *24*'te *toplu* yerleşim profili kullanan boş konumlar olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-216">Before you begin, make sure that there are empty locations in warehouse *24* that use the *BULK* location profile.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="e5d7d-217">Satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e5d7d-217">Create a purchase order</span></span>

<span data-ttu-id="e5d7d-218">Üç satır içeren bir satınalma siparişi oluşturulur: aynı ürün numarası için iki satır, ancak farklı **Boyut** çeşitleri ve çeşitlere sahip olmayan farklı bir ürün için üçüncü bir satır oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-218">You will create a purchase order that has three lines: two lines for the same product number but different **Size** variants, and a third line for a different product that has no variants.</span></span>

1. <span data-ttu-id="e5d7d-219">**Borç hesapları \> Satın alma siparişleri \> Tüm satınalma siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-219">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="e5d7d-220">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-220">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e5d7d-221">**Satın alma siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e5d7d-221">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e5d7d-222">**Satıcı hesabı:** *1001*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-222">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="e5d7d-223">**Ambar:** *24*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-223">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="e5d7d-224">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-224">Select **OK**.</span></span>
1. <span data-ttu-id="e5d7d-225">Satınalma siparişi oluşturulur ve **Satınalma siparişi satırları** hızlı sekmesi üzerine yeni bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-225">The purchase order is created, and a new line is added on the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="e5d7d-226">Satın alma siparişi numarasını not edin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-226">Make a note of the purchase order number.</span></span>
1. <span data-ttu-id="e5d7d-227">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e5d7d-227">On the new line, set the following values:</span></span>

    - <span data-ttu-id="e5d7d-228">**Madde numarası:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-228">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="e5d7d-229">**Boyut** *L*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-229">**Size** *L*</span></span>
    - <span data-ttu-id="e5d7d-230">**Miktar:** *2*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-230">**Quantity:** *2*</span></span>

1. <span data-ttu-id="e5d7d-231">Kılavuzun üzerinde **Satır ekle**'yi seçerek ikinci bir saıtın alma sipariş satırı ekleyin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e5d7d-231">Select **Add line** above the grid to add a second purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="e5d7d-232">**Madde numarası:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-232">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="e5d7d-233">**Boyut** *XL*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-233">**Size** *XL*</span></span>
    - <span data-ttu-id="e5d7d-234">**Miktar:** *2*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-234">**Quantity:** *2*</span></span>

1. <span data-ttu-id="e5d7d-235">**Satır ekle**'yi seçerek üçüncü satın alma siparişi satırı ekleyin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e5d7d-235">Select **Add line** to add a third purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="e5d7d-236">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-236">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="e5d7d-237">**Miktar:** *1*</span><span class="sxs-lookup"><span data-stu-id="e5d7d-237">**Quantity:** *1*</span></span>

<span data-ttu-id="e5d7d-238">1. **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-238">1.Select **Save**.</span></span>

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a><span data-ttu-id="e5d7d-239">Ambar uygulamasında satınalma siparişi satırları al</span><span class="sxs-lookup"><span data-stu-id="e5d7d-239">Receive purchase order lines in the warehouse app</span></span>

1. <span data-ttu-id="e5d7d-240">Ambar *24*'te etkin olan bir kullanıcı olarak ambarı uygulamasına oturum açın.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-240">Sign in to the warehouse app as a user who is enabled for warehouse *24*.</span></span>
1. <span data-ttu-id="e5d7d-241">**Gelen** menüsünü seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-241">Select the **Inbound** menu.</span></span>
1. <span data-ttu-id="e5d7d-242">**Satın alma satırı alma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-242">Select **PO Line receiving**.</span></span>
1. <span data-ttu-id="e5d7d-243">**PONUM** alanını seçin ve satınalma siparişi numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-243">Select the **PONUM** field, and then enter the purchase order number.</span></span>
1. <span data-ttu-id="e5d7d-244">Sayfanın altındaki Onayla düğmesini (✔) seçerek girişinizi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-244">Confirm your entry by selecting the confirm button ( ✔ ) at the bottom of the page.</span></span>
1. <span data-ttu-id="e5d7d-245">Alınmakta olan satınalma siparişindeki satır numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-245">Enter the line number from the purchase order that is being received.</span></span> <span data-ttu-id="e5d7d-246">**LINENUM** alanını seçin ve *1* girmek için numara panelini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-246">Select the **LINENUM** field, and then use the number pad to enter *1*.</span></span>
1. <span data-ttu-id="e5d7d-247">Girişinizi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-247">Confirm your entry.</span></span>
1. <span data-ttu-id="e5d7d-248">Alınacak miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-248">Enter the quantity to receive.</span></span> <span data-ttu-id="e5d7d-249">**Miktar** alanındaki değeri *2* olarak artırmak için iki kez artı işareti (**+**) düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-249">Select the plus sign (**+**) button two times to increase the value in the **Qty** field to *2*.</span></span>
1. <span data-ttu-id="e5d7d-250">Sayfanın alt kısmındaki düğmeyi (✔) seçerek girdinizi kaydedin ve sonra düğmeyi (✔) tekrar seçerek girdinizi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-250">Register your entry by selecting the button ( ✔ ) at the bottom of the page, and then confirm your entry by selecting the button ( ✔ ) again.</span></span>
1. <span data-ttu-id="e5d7d-251">**Satınalma siparişleri: Koyma** sayfası hakkındaki bilgileri görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-251">View the information on the **Purchase orders: Put** page.</span></span> <span data-ttu-id="e5d7d-252">Bu sayfa, yerine koyma (iş 1) için oluşturulan işi gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-252">This page shows the work that has been created for the put-away (Work 1).</span></span>

    <span data-ttu-id="e5d7d-253">Alınan maddenin yerleştirileceği yerleşim, lisans levhası, madde, boyut ve henüz tamamladığınız **SAS satırı alma** görevinin miktarı gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-253">The location where the received item will be put away, the license plate, the item, the size, and the quantity of the **PO Line receiving** task that you just completed are shown.</span></span>

1. <span data-ttu-id="e5d7d-254">Yerine koyma işini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-254">Confirm the put-away work.</span></span>
1. <span data-ttu-id="e5d7d-255">Satınalma siparişi satırı 2 için 4- 11 adımlarını tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-255">Repeat the steps 4 through 11 for the purchase order line 2.</span></span> <span data-ttu-id="e5d7d-256">Ancak 8. adımda bir miktar *1* olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-256">However, in step 8, specify a quantity of *1*.</span></span>

    <span data-ttu-id="e5d7d-257">Yeni yerine koyma çalışması (İş 2) çalışma 1 ile aynı yerleşim için oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-257">New put-away work (Work 2) is created for the same location as Work 1.</span></span>

1. <span data-ttu-id="e5d7d-258">Satınalma siparişi satırı 2 için 4 -11 adımlarını tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-258">Repeat the steps 4 through 11 again for purchase order line 2.</span></span> <span data-ttu-id="e5d7d-259">8. adımda kalan miktarı *1* olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-259">In step 8, specify the remaining quantity of *1*.</span></span>

    <span data-ttu-id="e5d7d-260">Yeni yerine koyma çalışması (İş 3) İŞ 1 ve İş 2 ile aynı yerleşim için oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-260">New put-away work (Work 3) is created for the same location as Work 1 and Work 2.</span></span> <span data-ttu-id="e5d7d-261">Bu davranış, *Sağlamlaştırma* yerleşim yönergesi stratejisinin kullanıldığı ve *toplu* **yerleşim profilleri** kuruluu üzerindeki **izin verilen ürün boyut karıştırma** Hızlı sekmesinin **Boyut** değişkenin bir konumda karıştırılmasına olanak sağladığından oluşur.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-261">This behavior occurs because the *Consolidate* location directive strategy is used, and the **Allowed product dimension mixing** FastTab on the *Bulk* **Location profiles** setup allows the **Size** variant to be mixed on a location.</span></span>

1. <span data-ttu-id="e5d7d-262">Satınalma siparişi satırı 3 için 4- 11 adımlarını tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-262">Repeat the steps 4 through 11 for purchase order line 3.</span></span> <span data-ttu-id="e5d7d-263">8. adımda *A0001* madde numarası için *1* miktarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-263">In step 8, specify a quantity of *1* for item number *A0001*.</span></span>

    <span data-ttu-id="e5d7d-264">Yeni yerine koyma çalışması (İş 4), satınalma siparişi satırları 1 ve 2 için kullanılan konumdan farklı bir yerleşim için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-264">New put-away work (Work 4) is created for a different location than the location that is used for purchase order lines 1 and 2.</span></span> <span data-ttu-id="e5d7d-265">Bu davranış, yerleşim profilinin karışık ürünlere izin vermediği, ancak aynı ürün yöneticisinin karma boyutlarına izin vermediği için oluşur.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-265">This behavior occurs because the location profile doesn't allow for mixed products, but it does allow for mixed dimensions of the same product master.</span></span>

1. <span data-ttu-id="e5d7d-266">Sayfanın üst kısmındaki menü düğmesini seçin (bazen hamburger veya hamburger düğmesi olarak da adlandırılır) ve **SS satırı teslim alma** programından çıkmak için **iptal**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-266">Select the Menu button at the top of the page (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit **PO Line receiving**.</span></span>

> [!TIP]
> <span data-ttu-id="e5d7d-267">Bu senaryoyu tekrarlayabilirsiniz ancak bu sefer *TOPLU* **yerleşim profillerindeki** **Ürün boyut karışımına izin ver** hızlı sekmesi altında **Boyut**  - *Hayır* ayarlayın, böylece ürün boyutlarının hiçbiri karışmaz.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-267">You can repeat this scenario, but this time, set **Size** - *No* under the **Allow product dimension mixing** FastTab on the *BULK* **Location profiles**, so that none of the product dimensions can be mixed.</span></span> <span data-ttu-id="e5d7d-268">Bu durumda, satınalma siparişi aldığınızda, her ürün çeşidi yeni bir konuma yerleştirilecek.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-268">In this case, when you receive the purchase order, each product variant will be put to a new location.</span></span>