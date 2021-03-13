---
title: Varlıkları satınalma siparişlerine göre oluşturma
description: Bu konu, Varlık Yönetiminde bakım işleri için varlıklar oluşturmak üzere temel olarak kullanılabilecek bir varlık maddeleri listesini nasıl oluşturabileceğinizi açıklar.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 83419fa5c6b6aee0b321c526565c3518deaf4bd0
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016996"
---
# <a name="create-assets-based-on-purchase-orders"></a><span data-ttu-id="0d070-103">Varlıkları satınalma siparişlerine göre oluşturma</span><span class="sxs-lookup"><span data-stu-id="0d070-103">Create assets based on purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="0d070-104">Bu konu, Varlık Yönetiminde bakım işleri için varlıklar oluşturmak üzere temel olarak kullanılabilecek bir varlık maddeleri listesini nasıl oluşturabileceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="0d070-104">This topic explains how you can create a list of asset items that can be used as a basis for creating assets for maintenance jobs in Asset Management.</span></span> <span data-ttu-id="0d070-105">Varlık maddelerine göre, bu maddelerde oluşturulan satınalma siparişi satırlarının listesini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d070-105">Based on the asset items, you are able to view a list of the purchase order lines that have been created on those items.</span></span> <span data-ttu-id="0d070-106">Bu işlevin amacı, Varlık Yönetiminde bir satınalma siparişini temel alarak kolayca bir varlık oluşturmaktır.</span><span class="sxs-lookup"><span data-stu-id="0d070-106">The purpose of this functionality is to easily create an asset in Asset Management based on a purchase order.</span></span>

<span data-ttu-id="0d070-107">İlk olarak, **Varlık maddeleri**'ndeki bir satınalma siparişinden varlıklar oluşturmak için kullanılacak maddeler ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0d070-107">First, you set up the items to be used for creating assets from a purchase order in **Asset items**.</span></span> <span data-ttu-id="0d070-108">Bir satınalma siparişi satırı oluşturduktan sonra, **Bekleyen varlıklar**'da varlıklar oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0d070-108">After creating a purchase order line, you create the assets in **Pending assets**.</span></span> <span data-ttu-id="0d070-109">Varlığın satınalma siparişinin hangi aşamasında oluşturulması gerektiğine karar vermek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="0d070-109">It is possible to decide at which stage of the purchase order the asset should be created.</span></span>


## <a name="select-asset-items"></a><span data-ttu-id="0d070-110">Varlık maddelerini seçin</span><span class="sxs-lookup"><span data-stu-id="0d070-110">Select asset items</span></span>

1. <span data-ttu-id="0d070-111">**Varlık yönetimi** > **Kurulum** > **Varlıklar** > **Maddeler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0d070-111">Click **Asset management** > **Setup** > **Assets** > **Items**.</span></span>
2. <span data-ttu-id="0d070-112">Yeni bir varlık maddesi oluşturmak için **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0d070-112">Click **New** to create a new asset item.</span></span>
3. <span data-ttu-id="0d070-113">**Madde numarası** alanında bir maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="0d070-113">Select the item in the **Item number** field.</span></span> <span data-ttu-id="0d070-114">Bu alandan çıktığınızda, madde adı otomatik olarak **Ürün adı** alanına eklenir.</span><span class="sxs-lookup"><span data-stu-id="0d070-114">When you leave that field, the item name is automatically inserted in the **Product name** field.</span></span>
4. <span data-ttu-id="0d070-115">**Genel** hızlı sekmesinde, madde için bir varlık türü seçin.</span><span class="sxs-lookup"><span data-stu-id="0d070-115">On the **General** FastTab, select an asset type for the item.</span></span>
5. <span data-ttu-id="0d070-116">Madde için varlık üreticisi ve modeli seçin.</span><span class="sxs-lookup"><span data-stu-id="0d070-116">Select asset manufacturer and model for the item.</span></span>
6. <span data-ttu-id="0d070-117">Maddeyi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="0d070-117">Save the item.</span></span>


## <a name="create-assets-from-pending-assets"></a><span data-ttu-id="0d070-118">Bekleyen varlıklardan varlıklar oluşturma</span><span class="sxs-lookup"><span data-stu-id="0d070-118">Create assets from pending assets</span></span>

1. <span data-ttu-id="0d070-119">**Varlık yönetimi** > **Genel** > **Varlıklar** > **Bekleyen Varlıklar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0d070-119">Click **Asset management** > **Common** > **Assets** > **Pending Assets**.</span></span>
2. <span data-ttu-id="0d070-120">**Varlık maddeleri**'nde seçilen maddelere göre satınalma siparişlerinin güncelleştirilmiş bir listesini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="0d070-120">You will see an updated list of the purchase orders based on the items selected in **Asset items**.</span></span>
3. <span data-ttu-id="0d070-121">Varlığın oluşturulması gereken yaşam döngüsü durumunu seçmek için satınalma siparişlerinin durumunu filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d070-121">You can filter the status of purchase orders to select at which lifecycle state the asset should be created.</span></span> <span data-ttu-id="0d070-122">Örneğin, yalnızca bir satınalma siparişinde bir ürün girişi deftere nakledildiğinde varlıklar oluşturmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d070-122">For example, you may only want to create assets when a product receipt has been posted on a purchase order.</span></span>
4. <span data-ttu-id="0d070-123">Maddeyle ilgili ayrıntılı bilgileri görüntülemek için satınalma siparişi satırındaki **Referans numarası** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="0d070-123">Select the **Reference number** link on a purchase order line to view detailed information about the item.</span></span>
5. <span data-ttu-id="0d070-124">**Stok boyutları** hızlı sekmesinde hangi boyutların görüntüleneceğini düzenlemek istiyorsanız, **Boyutları Görüntüle** düğmesine tıklayın ve seçimlerinizi yapın.</span><span class="sxs-lookup"><span data-stu-id="0d070-124">If you want to edit which dimensions are displayed on the **Inventory dimensions** FastTab, click the **Display Dimensions** button, and make your selections.</span></span>
6. <span data-ttu-id="0d070-125">Bir satınalma siparişi satırına dayalı bir varlık oluşturmak istiyorsanız, liste sayfasında bu satır için **İşaretle** sütunundaki onay kutusunu seçin ve **Varlıklar oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0d070-125">If you want to create an asset based on a purchase order line, select the check box in the **Mark** column for that line on the list page, and click **Create assets**.</span></span> <span data-ttu-id="0d070-126">Varlık kodunu size bildiren bir ileti görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="0d070-126">A message will be displayed informing you of the asset ID.</span></span>
7. <span data-ttu-id="0d070-127">**Tüm varlıklar** listesinde varlığı seçin ve varlığa daha fazla bilgi eklemek için **Düzenle** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0d070-127">Select the asset in the **All assets** list and click **Edit** to add more information to the asset.</span></span>
8. <span data-ttu-id="0d070-128">**Bekleyen varlıklar**'da, bir varlık oluşturmak istemediğiniz için bir satırı silmek istiyorsanız, ilgili satırın **İşaretle** sütunundaki onay kutusunu seçin ve **Bekleyen varlıkları at**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0d070-128">In **Pending assets**, if you want to delete a line because you don't want to create an asset, select the check box in the **Mark** column for that line, and click **Discard pending assets**.</span></span> <span data-ttu-id="0d070-129">Varlık kodunu size bildiren bir ileti görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="0d070-129">A message will be displayed informing you of the asset ID.</span></span> <span data-ttu-id="0d070-130">Satınalma siparişini veya satış siparişini silmezsiniz. Yalnızca **Varlık Yönetimi**'nde varlık oluşturabildiğiniz kaydı silersiniz.</span><span class="sxs-lookup"><span data-stu-id="0d070-130">You are not deleting the purchase order or sales order, just the record from which you could have created an asset in **Asset Management**.</span></span>

>[!NOTE]
><span data-ttu-id="0d070-131">Tüm ürün boyutları (boyut, renk, yapılandırma, vb.) otomatik olarak varlık özniteliklerine aktarılır.</span><span class="sxs-lookup"><span data-stu-id="0d070-131">All product dimensions (size, color, configuration etc.) are automatically transferred to the asset attributes.</span></span> <span data-ttu-id="0d070-132">İzleme boyutları (seri numarası), varlık oluşturulduğunda doğrudan varlığa depolanır.</span><span class="sxs-lookup"><span data-stu-id="0d070-132">Tracking dimensions (serial number) are stored directly on the asset when the asset is created.</span></span>


## <a name="find-pending-assets"></a><span data-ttu-id="0d070-133">Bekleyen varlıkları bulma</span><span class="sxs-lookup"><span data-stu-id="0d070-133">Find pending assets</span></span>

<span data-ttu-id="0d070-134">Bekleyen varlıkları denetlemek için **Bekleyen varlık sayımı** çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d070-134">You can run a **Pending asset count** to check for pending assets.</span></span> <span data-ttu-id="0d070-135">Örneğin, bu işlev bekleyen bir varlık, varlık olarak oluşturulmaya hazır olduğunda bir bildirim almak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0d070-135">For example, this function can be used for receiving a notification each time a pending asset is ready to be created as an asset.</span></span>

1. <span data-ttu-id="0d070-136">**Varlık yönetimi** > **Periyodik** > **Varlıklar** > **Bekleyen varlık sayısı**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0d070-136">Click **Asset management** > **Periodic** > **Assets** > **Pending asset count**.</span></span>
2. <span data-ttu-id="0d070-137">İşi çalıştırmak için **Tamam**'a tıklayın ve **Bekleyen varlıklar**'daki listeyi güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="0d070-137">Click **OK** to run the job and update the list in **Pending assets**.</span></span>
3. <span data-ttu-id="0d070-138">Bu işi, örneğin her gün bir toplu iş olarak çalışacak şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d070-138">You can set up this job to run as a batch job, for example, once each day.</span></span>

<span data-ttu-id="0d070-139">**Dikkat:** Bir satınalma siparişinde ilgili maddeyi temel alarak bir varlık oluşturduktan *sonra* veri dğiştirilirse, bu değişiklikler varlığa yansıtılmaz.</span><span class="sxs-lookup"><span data-stu-id="0d070-139">**Caution:** If data is changed on a purchase order *after* you have created an asset based on the appertaining item, those changes will not be reflected on the asset.</span></span>
