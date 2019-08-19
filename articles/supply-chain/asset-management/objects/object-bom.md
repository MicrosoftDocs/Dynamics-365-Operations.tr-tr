---
title: Varlık Ürün Reçeteleri
description: Bu konuda, Varlık yönetimi'ndeki varlık ürün reçeteleri (BOM) açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 761364c8c58258baf2268f917cb174ac300c4528
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783668"
---
# <a name="asset-boms"></a><span data-ttu-id="f71fa-103">Varlık Ürün Reçeteleri</span><span class="sxs-lookup"><span data-stu-id="f71fa-103">Asset BOMs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="f71fa-104">Bu konuda, Varlık yönetimi'ndeki varlık ürün reçeteleri (BOM) açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f71fa-104">This topic describes asset bills of materials (BOMs) in Asset Management.</span></span> <span data-ttu-id="f71fa-105">**Varlık Ürün Reçetesi** sayfası, tüm kullanım ömrü boyunca bir varlık üzerinde kullanılan tüm öğelerin (yedek parça ve diğer öğeler) listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f71fa-105">The **Asset BOM** page shows a list of all items (spare parts and other items) that are used on an asset during its whole lifetime.</span></span> <span data-ttu-id="f71fa-106">Yeni bir varlık oluşturduğunuzda, kurulum yordamının bir parçası olarak bir varlık ürün reçetesi ayarlamayı düşünmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="f71fa-106">When you create a new asset, you should consider setting up an asset BOM as a part of the setup procedure.</span></span> <span data-ttu-id="f71fa-107">Bu şekilde, varlık için madde geçmişini oluşturma tarihinden itibaren takip edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f71fa-107">In this way, you can track item history for the asset from the creation date.</span></span>

<span data-ttu-id="f71fa-108">Bir bakım işini tamamladıktan ve madde tüketimi bir iş emrinee kaydettikten sonra, varlık üzerinde kullanılan yedek parça ve diğer maddelerin tüketimini izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f71fa-108">After you've completed a maintenance job, and item consumption has been registered on a work order, you can track consumption of spare parts and other items that are used on the asset.</span></span> <span data-ttu-id="f71fa-109">Bu işlev, tüm varlıklarınız için tam bir madde tüketim kaydı tutmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="f71fa-109">This functionality lets you keep a complete item consumption record for all your assets.</span></span> <span data-ttu-id="f71fa-110">Örneğin, belirli bir yedek parçanın sıklıkla değiştirilip değiştirilmediğini izlemek veya bir varlık üzerinde kullanılmakta olan yedek parçaları veya diğer maddeleri izlemek için bu kaydı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f71fa-110">For example, you can use the record to monitor whether a specific spare part is often replaced, or to keep track of the spare parts or other items that are currently used on an asset.</span></span>

> [!NOTE]
> <span data-ttu-id="f71fa-111">İş emrinde, madde tüketimi hem yedek parçaları hem de yağlama maddeleri, cıvatalar ve contalar gibi diğer ek maddeleri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="f71fa-111">On a work order, item consumption might include both spare parts and other, additional items, such as lubricants, bolts, and gaskets.</span></span>

<span data-ttu-id="f71fa-112">Bir varlık ürün reçetesi, Varlık Yönetimi'ndeki kurulumuna göre otomatik olarak güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="f71fa-112">An asset BOM can be automatically updated based on the setup in Asset Management.</span></span> <span data-ttu-id="f71fa-113">Sonlandırılmış veya tamamlanan iş emirlerini işlemek için bir iş emri yaşam döngüsü durumu oluşturulduysa ve bu iş emri yaşam döngüsü durumu için **İş emri yaşam döngüsü durumları** sayfasında **Varlık ürün reçetesini güncelleştir** seçeneği **Evet** olarak ayarlandıysa, iş emri bu yaşam döngüsü durumuna güncelleştirildiğinde iş emrinde kullanılan tüm maddeler **Varlık ürün reçetesi** sayfasında otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f71fa-113">If a work order lifecycle state has been created to handle finished or completed work orders, and if the **Update asset BOM** option for that work order lifecycle state is set to **Yes** on the **Work order lifecycle states** page, all items that are used on the work order will be automatically updated on the **Asset BOM** page when the work order is updated to that lifecycle state.</span></span> 


<span data-ttu-id="f71fa-114">Ayrıca, **Varlık ürün reçetesi** sayfasında yeni madde satırları oluşturarak bir varlık ürün reçetesini el ile de güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f71fa-114">You can also manually update an asset BOM by creating new item lines on the **Asset BOM** page.</span></span>

<span data-ttu-id="f71fa-115">**Varlık ürün reçetesi** sayfasında, madde tüketimi bir iş emrine kaydedildikten sonra varlıklar için yedek parça geçmişini izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f71fa-115">On the **Asset BOM** page, you can track spare parts history for assets after item consumption is registered on a work order.</span></span> <span data-ttu-id="f71fa-116">Bu işlevi kullanmak için, **Yedek parça madde grupları** sayfasında yedek parça kaydı için kullanılması gereken madde gruplarını seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f71fa-116">To use this functionality, you must select the item groups that should be used for spare parts registration on the **Spare parts item groups** page.</span></span>

<span data-ttu-id="f71fa-117">Varlık ürün reçetesi işlevini kullanmak için, önce gerekli yedek parça madde gruplarını ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f71fa-117">To use asset BOM functionality, you must first set up the required spare parts items groups.</span></span> <span data-ttu-id="f71fa-118">Daha sonra, bir iş emri tamamlandığında varlık ürün reçetesinin otomatik olarak güncelleştirilmesini istiyorsanız, bu güncelleştirmeyi işlemek için bir iş emri yaşam döngüsü durumu ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f71fa-118">Then, if you want the asset BOM to be automatically updated when a work order is completed, you can set up a work order lifecycle state to handle that update.</span></span> 


## <a name="set-up-spare-parts-item-groups"></a><span data-ttu-id="f71fa-119">Yedek parça madde gruplarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="f71fa-119">Set up spare parts item groups</span></span>

<span data-ttu-id="f71fa-120">Yedek parça geçmişi kurulumu, **Stok ve ambar yönetimi** modülünde oluşturulan madde gruplarını temel alır.</span><span class="sxs-lookup"><span data-stu-id="f71fa-120">The setup of spare parts history is based on item groups that are created in the **Inventory and warehouse management** module.</span></span> <span data-ttu-id="f71fa-121">Varlık Yönetiminde, seçili madde gruplarındaki maddelerin yedek parça geçmişini izleyebilebilmek için madde gruplarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f71fa-121">In Asset Management, you set up item groups so that you can track spare parts history for the items in the selected item groups.</span></span>

1. <span data-ttu-id="f71fa-122">**Varlık yönetimi** \> **Kurulum** \> **Varlık** \> **Yedek parça madde grupları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="f71fa-122">Select **Asset management** \> **Setup** \> **Asset** \> **Spare parts item groups**.</span></span>
2. <span data-ttu-id="f71fa-123">Bir madde grubu ayarlamak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f71fa-123">Select **New** to set up an item group.</span></span>
3. <span data-ttu-id="f71fa-124">**Madde grubu** alanında grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="f71fa-124">In the **Item group** field, select the group.</span></span> <span data-ttu-id="f71fa-125">Grubun adı otomatik olarak **Ad** alanına girilir.</span><span class="sxs-lookup"><span data-stu-id="f71fa-125">The name of the group is automatically entered in the **Name** field.</span></span>

## <a name="view-and-update-asset-boms"></a><span data-ttu-id="f71fa-126">Varlık ürün reçetelerini görüntüleme ve güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f71fa-126">View and update asset BOMs</span></span>

<span data-ttu-id="f71fa-127">Bir iş emrindeki madde tüketimini deftere naklettikten sonra, **Varlık ürün reçetesi** sayfasında kayıtlı madde tüketimini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f71fa-127">After you post item consumption on a work order, you can view the registered item consumption on the **Asset BOM** page.</span></span>

1. <span data-ttu-id="f71fa-128">**Varlık yönetimi** \> **Genel** \> **Varlıklar** \> **Etkin varlıklar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f71fa-128">Select **Asset management** \> **Common** \> **Assets** \> **Active assets**.</span></span> <span data-ttu-id="f71fa-129">Listeden varlığı seçin ve ardından **Varlık ürün reçetesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="f71fa-129">Select the asset in the list, and then select **Asset BOM**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f71fa-130">Tüm varlıklardaki tüm madde tüketim kayıtlarını görüntülemek için, **Varlık yönetimi** \> **Sorgular** \> **Varlıklar** \> **Varlık ürün reçetesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="f71fa-130">To view all item consumption registrations on all assets, select **Asset management** \> **Inquiries** \> **Assets** \> **Asset BOM**.</span></span>

2. <span data-ttu-id="f71fa-131">**Varlık ürün reçetesini güncelleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f71fa-131">Select **Update asset BOM**.</span></span> <span data-ttu-id="f71fa-132">**Seç** öğesini seçerek, güncelleştirmeye gereksinim duyduğunuz varlıkları, varlık türlerini ve kaynakları ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f71fa-132">You can add assets, asset types, and resources to the update as you require by selecting **Select**.</span></span> <span data-ttu-id="f71fa-133">Güncelleştirmeyi başlatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f71fa-133">Select **OK** to start the update.</span></span> <span data-ttu-id="f71fa-134">Güncelleştirme işlevini bir toplu iş olarak da ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f71fa-134">You can also set up the Update function as a batch job.</span></span>
3. <span data-ttu-id="f71fa-135">Maddelerle ilgili daha fazla bilgi görmek isterseniz, stok boyutları ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f71fa-135">If you want to see more information that is related to the items, you can add inventory dimensions.</span></span> <span data-ttu-id="f71fa-136">**Stok** \> **Boyutlar görünümü**'nü seçin ve ardından görmek istediğiniz boyutların onay kutularını işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f71fa-136">Select **Inventory** \> **Dimensions display**, and then select the check boxes for the dimensions that you want to see.</span></span> <span data-ttu-id="f71fa-137">Bu ayarı **Varlık Ürün Reçetesi** sayfasındaki tüm varlıklar için korumak amacıyla **Ayarı kaydet** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f71fa-137">To keep this setup for all assets on the **Asset BOM** page, set the **Save setup** option to **Yes**.</span></span>
4. <span data-ttu-id="f71fa-138">Varlık Yönetiminde seçilen satırdaki maddenin varlıklar, iş türü varsayılanları, yedek parçalar ve iş emirleriyle ilişkili olarak nerede kullanıldığıyla ilgili genel bir bakış edinmek için **Maddenin kullanıldığı yer**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f71fa-138">To get an overview of where in Asset Management the item on the selected line is used, in relation to assets, job type defaults, spare parts, and work orders, select **Item where used**.</span></span> 
5. <span data-ttu-id="f71fa-139">Yalnızca etkin madde satırlarını görmek istiyorsanız, **Görüntüle** \> **Geçerli**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f71fa-139">If you want to see only active item lines, select **View** \> **Current**.</span></span> <span data-ttu-id="f71fa-140">Bitiş erme tarihi geçerli tarihten önce olan satırlar dahil olmak üzere tüm madde satırlarını görmek için **Görüntüle** \> **Tümü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="f71fa-140">To see all item lines, including lines where the expiration date is earlier than the current date, select **View** \> **All**.</span></span>

> [!NOTE]
> <span data-ttu-id="f71fa-141">Bir iş emrini tamamladığınızda, ilişkili varlıkla ilgili bazı madde veya yedek parçaların süresi dolmuşsa veya başka maddeler veya yedek parçalarla değiştirilmişse, varlık ürün reçetesini buna göre güncelleştirmeniz önerilir.</span><span class="sxs-lookup"><span data-stu-id="f71fa-141">When you've completed a work order, if some items or spare parts that are related to the related asset have expired or have been replaced by other items or spare parts, we recommend that you update the asset BOM accordingly.</span></span>

## <a name="create-a-new-item-line-in-an-asset-bom"></a><span data-ttu-id="f71fa-142">Varlık ürün reçetesinde yeni madde satırı oluşturma</span><span class="sxs-lookup"><span data-stu-id="f71fa-142">Create a new item line in an asset BOM</span></span>

<span data-ttu-id="f71fa-143">Varlıklar için el ile madde satırları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f71fa-143">You can manually create item lines for assets.</span></span>

1. <span data-ttu-id="f71fa-144">**Varlık ürün reçetesi** sayfasında, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f71fa-144">On the **Asset BOM** page, select **New**.</span></span>
2. <span data-ttu-id="f71fa-145">**Varlık** alanında, madde satırı eklenecek varlığı seçin.</span><span class="sxs-lookup"><span data-stu-id="f71fa-145">In the **Asset** field, select the asset to add an item line for.</span></span>
3. <span data-ttu-id="f71fa-146">**Satır numarası** alanına sıralı bir satır numarası girin.</span><span class="sxs-lookup"><span data-stu-id="f71fa-146">In the **Line number** field, enter a sequential line number.</span></span>
4. <span data-ttu-id="f71fa-147">**Etkin** alanına madde için bir başlangıç tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="f71fa-147">In the **Effective** field, enter a start date for the item.</span></span>
5. <span data-ttu-id="f71fa-148">Maddenin süresi dolacaksa, **Bitiş** alanına bir bitiş tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="f71fa-148">If the item will expire, in the **Expiration** field, enter an end date.</span></span>
6. <span data-ttu-id="f71fa-149">**Madde numarası** alanında maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="f71fa-149">In the **Item number** field, select the item.</span></span> <span data-ttu-id="f71fa-150">Ad **Ürün adı** alanına otomatik olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="f71fa-150">The name is automatically entered in the **Product name** field.</span></span>
7. <span data-ttu-id="f71fa-151">**Miktar** alanına kullanılan miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="f71fa-151">In the **Quantity** field, enter the quantity that is used.</span></span> <span data-ttu-id="f71fa-152">**Birim** alanı otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f71fa-152">The **Unit** field is automatically updated.</span></span>
