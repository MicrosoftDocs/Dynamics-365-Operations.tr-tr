---
title: Malzeme çekme satırı gruplandırması
description: Bu konu, çekme satırı gruplandırmasına genel bakış sağlamaktadır.
author: Mirzaab
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1b1d0135d450bc9be7b1303240a9ca70f95ae38e
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906280"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="7e05f-103">Malzeme çekme satırı gruplandırması</span><span class="sxs-lookup"><span data-stu-id="7e05f-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e05f-104">Çekme satırı gruplandırmasında, aynı madde ve yerleşime sahip birden çok iş satırı mobil cihazda kullanıcıya sunulan tek bir çekmede birleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="7e05f-104">In pick line grouping, multiple work lines that have the same item and location can be combined into a single pick that is presented to the user on a mobile device.</span></span> <span data-ttu-id="7e05f-105">Bu nedenle, ambar çalışanları olası en etkili yönergeleri alabilir, ancak sistemdeki iş satırlarının gerekli ayrımı da sürdürülür (örneğin, farklı kapsayıcılar ve siparişler için).</span><span class="sxs-lookup"><span data-stu-id="7e05f-105">Therefore, warehouse workers can receive the most efficient instructions that are possible, but the required separation of work lines in the system is also maintained (for example, for different containers and orders).</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="7e05f-106">Çekme satırı gruplandırması ayarlama</span><span class="sxs-lookup"><span data-stu-id="7e05f-106">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="7e05f-107">Mobil cihaz menü öğesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7e05f-107">Create a mobile device menu item</span></span>

1. <span data-ttu-id="7e05f-108">**Ambar Yönetimi \> kurulum \> mobil cihaz \> mobil cihaz menüsü öğeleri**'ne gidin ve **Satış grubu satırı malzeme çekme – Kullanıcı yönlendirilen** adlı yeni bir menü öğesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7e05f-108">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**, and create a new menu item that is named **Sales group line picking – User directed**.</span></span>
2. <span data-ttu-id="7e05f-109">**Mobil cihaz için menü öğeleri** altında, aşağıdaki değerleri ayarla:</span><span class="sxs-lookup"><span data-stu-id="7e05f-109">Under **Mobile device menu items**, set the following values:</span></span>

    - <span data-ttu-id="7e05f-110">**Menü madde adı** alanında, **satış çekme- grup satırı**'nı girin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-110">In the **Menu item name** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="7e05f-111">**Başlık** alanında, **satış çekme- grup satırı**'nı girin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-111">In the **Title** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="7e05f-112">**Mod** alanında, **İş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-112">In the **Mode** field, select **Work**.</span></span>
    - <span data-ttu-id="7e05f-113">**Mevcut işi kullan** seçeneğinde **Evet**'i işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-113">Set the **Use existing work** option to **Yes**.</span></span>

3. <span data-ttu-id="7e05f-114">**Genel** Hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="7e05f-114">On the **General** FastTab, you can set the following values:</span></span>

    - <span data-ttu-id="7e05f-115">**Yöneten** alanında **Kullanıcı tarafından yönetilen**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-115">In the **Directed by** field, select **User directed**.</span></span>
    - <span data-ttu-id="7e05f-116">**Lisans kalıbı oluştur** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7e05f-116">Set the **Generate license plate** option to **Yes**.</span></span>
    - <span data-ttu-id="7e05f-117">**Grup çekme** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7e05f-117">Set the **Group pick** option to **Yes**.</span></span>

4. <span data-ttu-id="7e05f-118">**İş sınıfları** hızlı sekmesinde, mobil aygıt menü öğesi için geçerli iş sınıflarını konfigüre etmek üzere aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="7e05f-118">On the **Work classes** FastTab, follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="7e05f-119">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-119">Select **New**.</span></span>
    2. <span data-ttu-id="7e05f-120">**İş sınıfı kimliği** alanında, kullanacağınız ambara göre **satış**'ı veya **satış siparişi çekme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-120">In the **Work class ID** field, select **Sales** or **SO Pick**, depending on the warehouse that you will use.</span></span>
    3. <span data-ttu-id="7e05f-121">**İş siparişi türü** alanında **Satış siparişi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-121">In the **Work order type** field, select **Sales orders**.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="7e05f-122">Mobil cihaz menüsü ayarlama</span><span class="sxs-lookup"><span data-stu-id="7e05f-122">Set up a mobile device menu</span></span>

1. <span data-ttu-id="7e05f-123">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-123">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span> 
1. <span data-ttu-id="7e05f-124">Yeni oluşturduğunuz menü öğesini istenen menüye ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-124">Add the menu item that you just created to the desired menu.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="7e05f-125">İş şablonu ayarla</span><span class="sxs-lookup"><span data-stu-id="7e05f-125">Set up a work template</span></span>

1. <span data-ttu-id="7e05f-126">**Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-126">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="7e05f-127">Bu işlevle kullanılması gereken çalışma şablonunu bulun.</span><span class="sxs-lookup"><span data-stu-id="7e05f-127">Find the work template that should be used with this function.</span></span> <span data-ttu-id="7e05f-128">Bu örnek için, standart **51 malzeme çekme** Contoso iş şablonu ' nu seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-128">For this example, select the standard **51 Pick to stage** Contoso work template.</span></span>
1. <span data-ttu-id="7e05f-129">Menüde, **Düzenle sorgu** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-129">On the menu, select **Edit query**.</span></span>
1. <span data-ttu-id="7e05f-130">**Sıralama** sekmesinde **Ekle**'yi seçin ve sonra aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="7e05f-130">On the **Sorting** tab, select **Add**, and then set the following values:</span></span>

    - <span data-ttu-id="7e05f-131">**Tablo** alanında **Geçici iş hareketleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-131">In the **Table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="7e05f-132">**Türetilmiş tablo** alanında **Geçici iş hareketleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-132">In the **Derived table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="7e05f-133">**Alan** alanında, **Öğe numarasını** seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-133">In the **Field** field, select **Item number**.</span></span>
    - <span data-ttu-id="7e05f-134">**Arama yönü** alanında, **artan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-134">In the **Search direction** field, select **Ascending**.</span></span>

> [!NOTE]
> <span data-ttu-id="7e05f-135">Satır gruplama çekme işlevinin çalışması için, iş satırlarının madde koduna göre sıralanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7e05f-135">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="7e05f-136">Aynı maddeleri içeren satırlar başka bir satırdan sonra sıralanmamışsa, gruplandırılmaz.</span><span class="sxs-lookup"><span data-stu-id="7e05f-136">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="7e05f-137">Örnek</span><span class="sxs-lookup"><span data-stu-id="7e05f-137">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="7e05f-138">Malzeme çekme işi oluştur</span><span class="sxs-lookup"><span data-stu-id="7e05f-138">Create picking work</span></span>

<span data-ttu-id="7e05f-139">Çekme satırı gruplandırmasını ayarlamadan önce, uygun bazı giden işler oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7e05f-139">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="7e05f-140">**Satış ve Pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-140">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="7e05f-141">Satış siparişi oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-141">Select **New** to create a sales order.</span></span> 
3. <span data-ttu-id="7e05f-142">**Müşteri hesabı** alanından bir AB müşterisini seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-142">In the **Customer account** field, select any customer.</span></span> 
4. <span data-ttu-id="7e05f-143">**Genel** hızlı sekmesinde, **ambar** alanında, **51**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-143">On the **General** FastTab, in the **Warehouse** field, select **51**.</span></span> <span data-ttu-id="7e05f-144">Daha sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-144">Then select **OK**.</span></span>
5. <span data-ttu-id="7e05f-145">**Satış siparişi satırları** altında, aşağıdaki altı satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="7e05f-145">Under **Sales order lines**, add the following six lines:</span></span>

    - <span data-ttu-id="7e05f-146">**Satır 1:** **Öğe numarası** alanında, **M9200**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-146">**Line 1:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="7e05f-147">**Miktar** alanına **3** yazın.</span><span class="sxs-lookup"><span data-stu-id="7e05f-147">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="7e05f-148">**Satır 2:** **Öğe numarası** alanında, **M9201**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-148">**Line 2:** In the **Item number** field, select **M9201**.</span></span> <span data-ttu-id="7e05f-149">**Miktar** alanına **3** yazın.</span><span class="sxs-lookup"><span data-stu-id="7e05f-149">In the **Quantity** field, enter **3**.</span></span> 
    - <span data-ttu-id="7e05f-150">**Satır 3:** **Öğe numarası** alanında, **M9202**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-150">**Line 3:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="7e05f-151">**Miktar** alanına **2** yazın.</span><span class="sxs-lookup"><span data-stu-id="7e05f-151">In the **Quantity** field, enter **2**.</span></span> 
    - <span data-ttu-id="7e05f-152">**Satır 4:** **Öğe numarası** alanında, **M9200**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-152">**Line 4:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="7e05f-153">**Miktar** alanına **1** yazın.</span><span class="sxs-lookup"><span data-stu-id="7e05f-153">In the **Quantity** field, enter **1**.</span></span> 
    - <span data-ttu-id="7e05f-154">**Satır 5:** **Öğe numarası** alanında, **M9200**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-154">**Line 5:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="7e05f-155">**Miktar** alanına **3** yazın.</span><span class="sxs-lookup"><span data-stu-id="7e05f-155">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="7e05f-156">**Satır 6:** **Öğe numarası** alanında, **M9202**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-156">**Line 6:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="7e05f-157">**Miktar** alanına **7** yazın.</span><span class="sxs-lookup"><span data-stu-id="7e05f-157">In the **Quantity** field, enter **7**.</span></span> 

    <span data-ttu-id="7e05f-158">İşte her madde için toplam miktarların Özeti:</span><span class="sxs-lookup"><span data-stu-id="7e05f-158">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="7e05f-159">**Madde M9200:** her biri 7</span><span class="sxs-lookup"><span data-stu-id="7e05f-159">**Item M9200:** 7 each</span></span>
    - <span data-ttu-id="7e05f-160">**Madde M9201:** her biri 3</span><span class="sxs-lookup"><span data-stu-id="7e05f-160">**Item M9201:** 3 each</span></span>
    - <span data-ttu-id="7e05f-161">**Madde M9202:** her biri 9</span><span class="sxs-lookup"><span data-stu-id="7e05f-161">**Item M9202:** 9 each</span></span>

6. <span data-ttu-id="7e05f-162">Siparişleri ambara serbest bırakmadan önce, çekme yerleşimlerinin tüm siparişlerdeki tüm maddeler için yeterli stok içerdiğinden emin olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7e05f-162">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="7e05f-163">Satış siparişi çekme için hangi malzeme çekme konumlarının kullanıldığını belirlemek için **yerleşim yönergesi** ayarını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-163">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span>
7. <span data-ttu-id="7e05f-164">Stoku rezerve edin ve ambara serbest bırakın.</span><span class="sxs-lookup"><span data-stu-id="7e05f-164">Reserve the inventory, and release it to the warehouse.</span></span> <span data-ttu-id="7e05f-165">Altı satıra sahip bir iş kodu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7e05f-165">A work ID that has six lines is created.</span></span> <span data-ttu-id="7e05f-166">Satırlar madde numarasına göre sıralanır.</span><span class="sxs-lookup"><span data-stu-id="7e05f-166">The lines are sorted by item number.</span></span>

### <a name="run-the-mobile-device-flow"></a><span data-ttu-id="7e05f-167">Mobil cihaz akışı çalıştır</span><span class="sxs-lookup"><span data-stu-id="7e05f-167">Run the mobile device flow</span></span>

1. <span data-ttu-id="7e05f-168">Mobil cihazda, yeni mobil aygıt menü öğesini içeren menüyü seçin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-168">On the mobile device, select the menu that includes the new mobile device menu item.</span></span>
1. <span data-ttu-id="7e05f-169">**Satış çekme – Grup satırı** menü öğesini seçin ve çekmeyi başlatın.</span><span class="sxs-lookup"><span data-stu-id="7e05f-169">Select the **Sales Pick – Group line** menu item, and initiate the pick.</span></span>

    <span data-ttu-id="7e05f-170">Menüyü seçtikten ve iş kodunu girdikten sonra, madde M9200 için tüm çekme satırlarının gruplandırılacağı çekme adımını görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="7e05f-170">After you select the menu and enter the work ID, you see the pick step where all pick lines for item M9200 are grouped.</span></span> <span data-ttu-id="7e05f-171">7 tane Madde M9200 öğesini çekmek için bir talimat alırsınız.</span><span class="sxs-lookup"><span data-stu-id="7e05f-171">You receive an instruction to pick 7 each of item M9200.</span></span>

1. <span data-ttu-id="7e05f-172">Çekme adımını onaylayın.</span><span class="sxs-lookup"><span data-stu-id="7e05f-172">Confirm the pick step.</span></span> 
1. <span data-ttu-id="7e05f-173">Süren işin istemci ekranına gidin ve madde M9200 için üç çekme satırının aynı anda kapatıldığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="7e05f-173">Go to the client screen of the work in process, and notice that all three pick lines for item M9200 were closed simultaneously.</span></span>

    <span data-ttu-id="7e05f-174">İş satırı 4 gösterilir.</span><span class="sxs-lookup"><span data-stu-id="7e05f-174">Work line 4 is presented.</span></span>

1. <span data-ttu-id="7e05f-175">Çekme adımını onaylayın.</span><span class="sxs-lookup"><span data-stu-id="7e05f-175">Confirm the pick step.</span></span>

    <span data-ttu-id="7e05f-176">Mobil aygıttaki son çekme adımı, iş emrinden alınan son iki çekme satırını toplar.</span><span class="sxs-lookup"><span data-stu-id="7e05f-176">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>

1. <span data-ttu-id="7e05f-177">9 tane her Madde M9202 için çekme adımını tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="7e05f-177">Complete the pick step for 9 each of item M9202.</span></span>
1. <span data-ttu-id="7e05f-178">İşi tamamlamak için Yerine Koyma adımını ve ek çekme/yerine koyma çiftlerini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="7e05f-178">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!NOTE]
> - <span data-ttu-id="7e05f-179">İş satırları yalnızca sıralı olduklarında gruplandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="7e05f-179">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="7e05f-180">Aşağıdaki işlevsellik desteklenmez:</span><span class="sxs-lookup"><span data-stu-id="7e05f-180">The following functionality isn't supported:</span></span>
>
>    - <span data-ttu-id="7e05f-181">Fiili ağırlık maddeleri.</span><span class="sxs-lookup"><span data-stu-id="7e05f-181">Catch-weight items.</span></span> <span data-ttu-id="7e05f-182">İşte herhangi bir fiili ağırlık öğesi varsa, çekmeyi başlatmak için başlamadan önce bir hata iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="7e05f-182">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>    - <span data-ttu-id="7e05f-183">Parça çekme.</span><span class="sxs-lookup"><span data-stu-id="7e05f-183">Piece picking.</span></span>
>    - <span data-ttu-id="7e05f-184">Bitmemiş stok yenileme çalışması olan iş satırları.</span><span class="sxs-lookup"><span data-stu-id="7e05f-184">Work lines that have unfinished replenishment work.</span></span>
>    - <span data-ttu-id="7e05f-185">Fazla malzeme çekme.</span><span class="sxs-lookup"><span data-stu-id="7e05f-185">Over-picking.</span></span>
