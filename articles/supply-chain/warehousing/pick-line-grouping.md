---
title: Malzeme çekme satırı gruplandırması
description: Bu konu, çekme satırı gruplandırmasına genel bakış sağlamaktadır.
author: Mirzaab
manager: tfehr
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ab8cdd7cad5420aca0de53e59220da9e230d411
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234645"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="8bae5-103">Malzeme çekme satırı gruplandırması</span><span class="sxs-lookup"><span data-stu-id="8bae5-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8bae5-104">Malzeme çekme satırı gruplandırması, aynı madde ve yerleşime sahip birden çok iş satırı mobil cihazda kullanıcıya sunulan tek bir çekmede birleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="8bae5-104">Pick line grouping enables multiple work lines that have the same item and location to be combined into a single pick that is presented to the user on the mobile device.</span></span> <span data-ttu-id="8bae5-105">Bu nedenle, ambar çalışanları olası en etkili yönergeleri alabilir, ancak sistemdeki iş satırlarının gerekli ayrımı da (örneğin, farklı konteynerler, siparişler vb. için) sürdürülür.</span><span class="sxs-lookup"><span data-stu-id="8bae5-105">Therefore, warehouse workers can receive the most efficient instructions, but required work line separation (for different containers, orders, and so on) can still be maintained in the system.</span></span>

## <a name="turn-on-the-pick-line-grouping-feature"></a><span data-ttu-id="8bae5-106">İş çekme satırı gruplandırma özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="8bae5-106">Turn on the pick line grouping feature</span></span>

<span data-ttu-id="8bae5-107">Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8bae5-107">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="8bae5-108">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="8bae5-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="8bae5-109">Burada, özellik aşağıdaki şekilde listelenmiştir:</span><span class="sxs-lookup"><span data-stu-id="8bae5-109">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="8bae5-110">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="8bae5-110">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="8bae5-111">**Özellik adı:** *Malzeme çekme satırı gruplandırma*</span><span class="sxs-lookup"><span data-stu-id="8bae5-111">**Feature name:** *Pick line grouping*</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="8bae5-112">Çekme satırı gruplandırması ayarlama</span><span class="sxs-lookup"><span data-stu-id="8bae5-112">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="8bae5-113">Mobil cihaz menü öğesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8bae5-113">Create a mobile device menu item</span></span>

1. <span data-ttu-id="8bae5-114">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-114">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="8bae5-115">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-115">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="8bae5-116">**Menü madde adı** alanında, *Satış grubu satırı malzeme çekme*'yi girin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-116">In the **Menu item name** field, enter *Sales group line picking*.</span></span>
1. <span data-ttu-id="8bae5-117">**Başlık** alanında, *Satış grubu satırı malzeme çekme*'yi girin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-117">In the **Title** field, enter *Sales group line picking*.</span></span> <span data-ttu-id="8bae5-118">Bu başlık, mobil cihaz menüsünde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="8bae5-118">This title will be shown on the mobile device menu.</span></span>
1. <span data-ttu-id="8bae5-119">**Mod** alanında, *İş*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-119">In the **Mode** field, select *Work*.</span></span>
1. <span data-ttu-id="8bae5-120">**Mevcut işi kullan** seçeneğinde *Evet*'i işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-120">Set the **Use existing work** option to *Yes*.</span></span>
1. <span data-ttu-id="8bae5-121">**Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="8bae5-121">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="8bae5-122">**Yöneten** alanında *Kullanıcı tarafından yönetilen*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-122">In the **Directed by** field, select *User directed*.</span></span>
    - <span data-ttu-id="8bae5-123">**Lisans kalıbı oluştur** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8bae5-123">Set the **Generate license plate** option to *Yes*.</span></span>
    - <span data-ttu-id="8bae5-124">**Grup çekme** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8bae5-124">Set the **Group pick** option to *Yes*.</span></span>
    - <span data-ttu-id="8bae5-125">Kalan seçenekler için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-125">Accept the default values for the remaining options.</span></span>

1. <span data-ttu-id="8bae5-126">Mobil cihaz menü öğesi için geçerli iş sınıflarını yapılandırmak üzere aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="8bae5-126">Follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="8bae5-127">**İş sınıfları** hızlı sekmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-127">On the **Work classes** FastTab, elect **New**.</span></span>
    2. <span data-ttu-id="8bae5-128">**İş sınıfı kimliği** alanında, kullanacağınız ambara göre *Satış*'ı veya *Satış Siparişi Çekme*'yi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8bae5-128">In the **Work class ID** field, you can select either *Sales* or *SO Pick*, depending on the warehouse that you will use.</span></span> <span data-ttu-id="8bae5-129">Bu senaryo için *Satış Siparişi Çekme*'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-129">For this scenario, select *SO Pick*.</span></span>

        <span data-ttu-id="8bae5-130">**İş emri türü** alanı, otomatik olarak *Satış siparişleri* olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="8bae5-130">The **Work order type** field is automatically set to *Sales orders*.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="8bae5-131">Mobil cihaz menüsü ayarlama</span><span class="sxs-lookup"><span data-stu-id="8bae5-131">Set up a mobile device menu</span></span>

<span data-ttu-id="8bae5-132">Az önce oluşturduğunuz menü öğesini **Giden** menüsüne eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-132">Follow these steps to add the menu item that you just created to the **Outbound** menu.</span></span>

1. <span data-ttu-id="8bae5-133">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-133">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="8bae5-134">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-134">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="8bae5-135">Liste bölmesi, mevcut tüm mobil cihaz menülerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8bae5-135">The list pane shows all existing mobile device menus.</span></span> <span data-ttu-id="8bae5-136">Listede, *Giden*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-136">Select *Outbound* in the list.</span></span>
1. <span data-ttu-id="8bae5-137">**Kullanılabilir menüler ve menü öğeleri** listesinde, yeni oluşturduğunuz *Satış grubu satırı malzeme çekme* menü öğesini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-137">In the **Available menus and menu items** list, find and select the *Sales group line picking* menu item that you created.</span></span>
1. <span data-ttu-id="8bae5-138">*Satış grubu satırı malzeme çekme* menü öğesini **Menü yapısı** listesine taşımak için sağ ok düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-138">Select the right arrow button to move the *Sales group line picking* menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="8bae5-139">Menü öğesini menü yapısında istenen konuma taşımak için yukarı ok ve aşağı ok düğmelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8bae5-139">Use the up arrow and down arrow buttons to move the menu item into the desired position in the menu structure.</span></span>
1. <span data-ttu-id="8bae5-140">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-140">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="8bae5-141">İş şablonu ayarla</span><span class="sxs-lookup"><span data-stu-id="8bae5-141">Set up a work template</span></span>

1. <span data-ttu-id="8bae5-142">**Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-142">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="8bae5-143">**İş siparişi türü** alanında *Satış siparişi*'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-143">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="8bae5-144">**Özet** ızgarasında, bu işlevle kullanılması gereken çalışma şablonunu bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-144">In the **Overview** grid, find and select the work template that should be used with this function.</span></span> <span data-ttu-id="8bae5-145">Bu senaryo için *51 malzeme çekme* şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-145">For this scenario, select the *51 Pick to stage* template.</span></span>
1. <span data-ttu-id="8bae5-146">Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-146">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="8bae5-147">Sorgu düzenleyicisi iletişim kutusundaki **Sıralama** sekmesinde **Ekle**'yi seçin ve ardından yeni satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="8bae5-147">In the query editor dialog box, on the **Sorting** tab, select **Add**, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="8bae5-148">**Tablo** sütununda *Geçici iş hareketleri*'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-148">In the **Table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="8bae5-149">**Türetilmiş tablo** sütununda *Geçici iş hareketleri*'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-149">In the **Derived table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="8bae5-150">**Alan** sütununda, *Öğe numarası*'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-150">In the **Field** column, select *Item number*.</span></span>
    - <span data-ttu-id="8bae5-151">**Arama yönü** sütununda, *Artan*'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-151">In the **Search direction** column, select *Ascending*.</span></span>

1. <span data-ttu-id="8bae5-152">İletişim kutusunu kapatmak için **Tamam**'ı seçip seçiminizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-152">Select **OK** to close the dialog box and save your selection.</span></span>
1. <span data-ttu-id="8bae5-153">Aşağıdaki iletiyi alırsınız: "Gruplama sıfırlanacak, devam edilsin mi?"</span><span class="sxs-lookup"><span data-stu-id="8bae5-153">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="8bae5-154">Devam etmek için **Eve**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-154">Select **Yes** to continue.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8bae5-155">Satır gruplama çekme işlevinin çalışması için, iş satırlarının madde koduna göre sıralanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="8bae5-155">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="8bae5-156">Aynı maddeleri içeren satırlar başka bir satırdan sonra sıralanmamışsa, gruplandırılmaz.</span><span class="sxs-lookup"><span data-stu-id="8bae5-156">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="8bae5-157">Örnek</span><span class="sxs-lookup"><span data-stu-id="8bae5-157">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="8bae5-158">Malzeme çekme işi oluştur</span><span class="sxs-lookup"><span data-stu-id="8bae5-158">Create picking work</span></span>

<span data-ttu-id="8bae5-159">Çekme satırı gruplandırmasını ayarlamadan önce, uygun bazı giden işler oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8bae5-159">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="8bae5-160">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-160">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="8bae5-161">Satış siparişi oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-161">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="8bae5-162">**Müşteri hesabı** alanında *US-004*'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-162">In the **Customer account** field, select *US-004*.</span></span>
1. <span data-ttu-id="8bae5-163">**Genel** hızlı sekmesinde, **ambar** alanında, *51*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-163">On the **General** FastTab, in the **Warehouse** field, select *51*.</span></span>
1. <span data-ttu-id="8bae5-164">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-164">Select **OK**.</span></span>
1. <span data-ttu-id="8bae5-165">**Satış siparişi satırları** hızlı sekmesinde, aşağıdaki altı satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="8bae5-165">On the **Sales order lines** FastTab, add the following six lines:</span></span>

    - <span data-ttu-id="8bae5-166">**Satır 1:** **Öğe numarası** alanında, *M9200*'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-166">**Line 1:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="8bae5-167">**Miktar** alanına *3* yazın.</span><span class="sxs-lookup"><span data-stu-id="8bae5-167">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="8bae5-168">**Satır 2:** **Öğe numarası** alanında, *M9201*'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-168">**Line 2:** In the **Item number** field, select *M9201*.</span></span> <span data-ttu-id="8bae5-169">**Miktar** alanına *3* yazın.</span><span class="sxs-lookup"><span data-stu-id="8bae5-169">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="8bae5-170">**Satır 3:** **Öğe numarası** alanında, *M9202*'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-170">**Line 3:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="8bae5-171">**Miktar** alanına *2* yazın.</span><span class="sxs-lookup"><span data-stu-id="8bae5-171">In the **Quantity** field, enter *2*.</span></span>
    - <span data-ttu-id="8bae5-172">**Satır 4:** **Öğe numarası** alanında, *M9200*'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-172">**Line 4:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="8bae5-173">**Miktar** alanına *1* yazın.</span><span class="sxs-lookup"><span data-stu-id="8bae5-173">In the **Quantity** field, enter *1*.</span></span>
    - <span data-ttu-id="8bae5-174">**Satır 5:** **Öğe numarası** alanında, *M9200*'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-174">**Line 5:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="8bae5-175">**Miktar** alanına *3* yazın.</span><span class="sxs-lookup"><span data-stu-id="8bae5-175">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="8bae5-176">**Satır 6:** **Öğe numarası** alanında, *M9202*'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-176">**Line 6:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="8bae5-177">**Miktar** alanına *7* yazın.</span><span class="sxs-lookup"><span data-stu-id="8bae5-177">In the **Quantity** field, enter *7*.</span></span>

    <span data-ttu-id="8bae5-178">İşte her madde için toplam miktarların Özeti:</span><span class="sxs-lookup"><span data-stu-id="8bae5-178">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="8bae5-179">**Madde M9200:** her biri *7*</span><span class="sxs-lookup"><span data-stu-id="8bae5-179">**Item M9200:** *7* each</span></span>
    - <span data-ttu-id="8bae5-180">**Madde M9201:** her biri *3*</span><span class="sxs-lookup"><span data-stu-id="8bae5-180">**Item M9201:** *3* each</span></span>
    - <span data-ttu-id="8bae5-181">**Madde M9202:** her biri *9*</span><span class="sxs-lookup"><span data-stu-id="8bae5-181">**Item M9202:** *9* each</span></span>

1. <span data-ttu-id="8bae5-182">Siparişleri ambara serbest bırakmadan önce, çekme yerleşimlerinin tüm siparişlerdeki tüm maddeler için yeterli stok içerdiğinden emin olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8bae5-182">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="8bae5-183">Satış siparişi çekme için hangi malzeme çekme konumlarının kullanıldığını belirlemek için **yerleşim yönergesi** ayarını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-183">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span> <span data-ttu-id="8bae5-184">*51* ambarı için Contoso tanıtım veri ortamını kullanıyorsanız, kullanılabilir stok olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="8bae5-184">If you're using the Contoso demo data environment for warehouse *51*, confirm that there is available inventory.</span></span>

    <span data-ttu-id="8bae5-185">Şimdi her bir satır için stoku rezerve etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="8bae5-185">You must now reserve the inventory for each line.</span></span>

1. <span data-ttu-id="8bae5-186">**Satış siparişi satırları** hızlı sekmesinde, rezerve edilmesi gereken satırlardan birini seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-186">On the **Sales order lines** FastTab, select one of the lines that must be reserved.</span></span>
1. <span data-ttu-id="8bae5-187">Kılavuzun üzerindeki **stok** menüsünde **rezervasyon**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-187">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="8bae5-188">**Rezervasyon** sayfasındaki Eylem Bölmesi'nde rezervasyonu uygulamak için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-188">On the **Reservation** page, on the Action Pane, select **Reserve lot** to apply the reservation.</span></span> <span data-ttu-id="8bae5-189">Ardından sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8bae5-189">Then close the page.</span></span>
1. <span data-ttu-id="8bae5-190">Rezerve edilmesi gereken kalan satırlar için 8 ile 10 arasındaki adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-190">Repeat steps 8 through 10 for the remaining lines that must be reserved.</span></span>

    <span data-ttu-id="8bae5-191">Şimdi satış siparişini ambara serbest bırakmalısınız.</span><span class="sxs-lookup"><span data-stu-id="8bae5-191">You must now release the sales order to the warehouse.</span></span>

1. <span data-ttu-id="8bae5-192">Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-192">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="8bae5-193">Bir sevkiyat ve dalganın oluşturulduğunu ve dalganın toplu iş halinde çalıştırılmak üzere gönderildiğini bildiren bir ileti alırsınız.</span><span class="sxs-lookup"><span data-stu-id="8bae5-193">You receive a message that states that a shipment and a wave have been created, and that the wave has been submitted to run in a batch.</span></span>

    <span data-ttu-id="8bae5-194">Dalga ve tüm aşağı akış işleri tamamlandığında, altı satıra sahip bir iş için bir iş kodu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="8bae5-194">When the wave and all downstream jobs have been completed, a work ID is created for work that has six lines.</span></span> <span data-ttu-id="8bae5-195">Satırlar madde numarasına göre sıralanır.</span><span class="sxs-lookup"><span data-stu-id="8bae5-195">The lines are sorted by item number.</span></span>

1. <span data-ttu-id="8bae5-196">Oluşturulan işi görüntülemek için **Ambar yönetimi \> İş \> Tüm işler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-196">Go to **Warehouse management \> Work \> All work** to view the work that was created.</span></span> <span data-ttu-id="8bae5-197">Bir sonraki yordamda kullanmanız gerekeceğinden **İş kodu** değerini not edin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-197">Make a note of the **Work ID** value, because you will need it in the next procedure.</span></span>

### <a name="initiate-picking-from-the-mobile-device"></a><span data-ttu-id="8bae5-198">Mobil cihazdan malzeme çekme işlemini başlatma</span><span class="sxs-lookup"><span data-stu-id="8bae5-198">Initiate picking from the mobile device</span></span>

1. <span data-ttu-id="8bae5-199">Ambar *51* için ayarlanmış olan bir kullanıcı olarak mobil cihazda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="8bae5-199">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="8bae5-200">Mobil cihazda, yeni mobil aygıt menü öğesini içeren menüyü seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-200">On the mobile device, select the menu that includes the new mobile device menu item.</span></span> <span data-ttu-id="8bae5-201">Bu senaryo için **Giden**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-201">For this scenario, select **Outbound**.</span></span>
1. <span data-ttu-id="8bae5-202">Malzeme çekmeyi başlatmak için **Satış grubu satırı malzeme çekme** menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-202">Select the **Sales group line picking** menu item to initiate the pick.</span></span>
1. <span data-ttu-id="8bae5-203">Önceki yordamda not aldığınız **İş Kodu** değerini girin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-203">Enter the **Work ID** value that you made a note of in the previous procedure.</span></span>

    <span data-ttu-id="8bae5-204">*M9200* öğesinin tüm malzeme çekme satırlarının gruplandırıldığı bir malzeme çekme adımı görmeniz ve her bir *M9200* maddesi için *7* adet çekmeniz gerektiğini bildiren bir yönerge almanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8bae5-204">You should see a pick step where all pick lines for item *M9200* are grouped, and you should receive an instruction to pick *7* each of item *M9200*.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="8bae5-205">Mobil cihazda, üç malzeme çekme iş satırı için malzeme çekme işi kullanıcı için tek bir malzeme çekme adımında toplanır.</span><span class="sxs-lookup"><span data-stu-id="8bae5-205">On the mobile device, the pick work for the three pick work lines has been aggregated into one picking step for the user.</span></span>

1. <span data-ttu-id="8bae5-206">Çekme adımını onaylayın.</span><span class="sxs-lookup"><span data-stu-id="8bae5-206">Confirm the pick step.</span></span>
1. <span data-ttu-id="8bae5-207">İş kodunun iş sayfasına gidin ve madde *M9200* için üç çekme satırının aynı anda kapatıldığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-207">Go to the work page for the work ID, and notice that all three pick lines for item *M9200* were closed simultaneously.</span></span>
1. <span data-ttu-id="8bae5-208">Mobil cihaza geri dönün ve çekme işlemine devam edin.</span><span class="sxs-lookup"><span data-stu-id="8bae5-208">Go back to the mobile device, and continue to pick.</span></span> <span data-ttu-id="8bae5-209">*M9201* için iş satırı 4 gösterilmelidir.</span><span class="sxs-lookup"><span data-stu-id="8bae5-209">Work line 4 for item *M9201* should be presented.</span></span> <span data-ttu-id="8bae5-210">Siparişte yalnızca bir iş satırı bulunduğundan, toplanacak bir şey yoktur.</span><span class="sxs-lookup"><span data-stu-id="8bae5-210">Because there was only one work line on the order, there is nothing to aggregate.</span></span>
1. <span data-ttu-id="8bae5-211">Çekme adımını onaylayın.</span><span class="sxs-lookup"><span data-stu-id="8bae5-211">Confirm the pick step.</span></span>
1. <span data-ttu-id="8bae5-212">Mobil aygıttaki son çekme adımı, iş emrinden alınan son iki çekme satırını toplar.</span><span class="sxs-lookup"><span data-stu-id="8bae5-212">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>
1. <span data-ttu-id="8bae5-213">*M9202* maddesi için *9* adet malzeme çekme adımını tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="8bae5-213">Complete the pick step for *9* each of item *M9202*.</span></span>
1. <span data-ttu-id="8bae5-214">İşi tamamlamak için Yerine Koyma adımını ve ek çekme/yerine koyma çiftlerini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="8bae5-214">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!IMPORTANT]
>
> - <span data-ttu-id="8bae5-215">İş satırları yalnızca sıralı olduklarında gruplandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="8bae5-215">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="8bae5-216">Aşağıdaki işlevsellik desteklenmez:</span><span class="sxs-lookup"><span data-stu-id="8bae5-216">The following functionality isn't supported:</span></span>
>
>   - <span data-ttu-id="8bae5-217">Fiili ağırlık maddeleri</span><span class="sxs-lookup"><span data-stu-id="8bae5-217">Catch-weight items</span></span>
>
>    <span data-ttu-id="8bae5-218">İşte herhangi bir fiili ağırlık öğesi varsa, çekmeyi başlatmak için başlamadan önce bir hata iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="8bae5-218">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>
>   - <span data-ttu-id="8bae5-219">Parça çekme</span><span class="sxs-lookup"><span data-stu-id="8bae5-219">Piece picking</span></span>
>   - <span data-ttu-id="8bae5-220">Bitmemiş stok yenileme işi olan iş satırları</span><span class="sxs-lookup"><span data-stu-id="8bae5-220">Work lines that have unfinished replenishment work</span></span>
>   - <span data-ttu-id="8bae5-221">Fazla malzeme çekme</span><span class="sxs-lookup"><span data-stu-id="8bae5-221">Over-picking</span></span>
>   - <span data-ttu-id="8bae5-222">Yeniden tahsisatla eksik malzeme çekme</span><span class="sxs-lookup"><span data-stu-id="8bae5-222">Short picking with item reallocation</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]