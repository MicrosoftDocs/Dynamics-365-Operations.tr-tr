---
title: Ürün sahipleri
description: Bu konuda ürün sahipleri hakkında bilgiler sağlanmaktadır. Ürün sahibi, belirli ürünlerden sorumlu kullanıcılardan oluşan bir gruptur. Yalnızca grubun üyeleri bu ürünleri serbest bırakabilir. Ürün sahibi ayrıca onay iş akışında da kullanılabilir.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 679712b2397f220e263da3df07ecd03c99bebf3f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842045"
---
# <a name="product-owners"></a><span data-ttu-id="be55c-106">Ürün sahipleri</span><span class="sxs-lookup"><span data-stu-id="be55c-106">Product owners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be55c-107">Ürün sahibi, belirli ürünlerden sorumlu kullanıcılardan oluşan bir gruptur.</span><span class="sxs-lookup"><span data-stu-id="be55c-107">The product owner is a group of users who are responsible for specific products.</span></span> <span data-ttu-id="be55c-108">Bir ürün sahibi grubu bir ürüne atandığında, yalnızca bu grubun üyeleri ürünü serbest bırakabilir.</span><span class="sxs-lookup"><span data-stu-id="be55c-108">When a product owner group is assigned to a product, only the members of that group can release the product.</span></span> <span data-ttu-id="be55c-109">Ürün sahibi mühendislik değişikliği yönetiminde onay iş akışında da kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="be55c-109">The product owner can also be used in the approval workflow in engineering change management.</span></span>

<span data-ttu-id="be55c-110">Ürün sahipleri genel ayarlardır.</span><span class="sxs-lookup"><span data-stu-id="be55c-110">Product owners are global settings.</span></span> <span data-ttu-id="be55c-111">Bu nedenle, tüm tüzel kişilikler için kullanılabilirdir.</span><span class="sxs-lookup"><span data-stu-id="be55c-111">Therefore, they are available to all legal entities.</span></span>

## <a name="create-a-product-owner-group"></a><span data-ttu-id="be55c-112">Ürün sahibi grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="be55c-112">Create a product owner group</span></span>

<span data-ttu-id="be55c-113">Bir ürün sahibi grubu oluşturmak ve bu gruba üye eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="be55c-113">To create a product owner group and add members to it, follow these steps.</span></span>

1. <span data-ttu-id="be55c-114">**Mühendislik değişikliği yönetimi \> Kurulum \> Ürün sahipleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="be55c-114">Go to **Engineering change management \> Setup \> Product owners**.</span></span>
2. <span data-ttu-id="be55c-115">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="be55c-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="be55c-116">**Ürün sahibi** alanına, ürün grubu için açıklayıcı bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="be55c-116">In the **Product owner** field, enter a name for the group.</span></span>
4. <span data-ttu-id="be55c-117">**Ad** alanına grubun kısa bir açıklamasını yazın.</span><span class="sxs-lookup"><span data-stu-id="be55c-117">In the **Name** field, enter a description of the group.</span></span>
5. <span data-ttu-id="be55c-118">**Üyeler** hızlı sekmesinde, grubun üyesi olması gereken çalışanları ekleyin.</span><span class="sxs-lookup"><span data-stu-id="be55c-118">On the **Members** FastTab, add the workers who should be members of the group.</span></span>

## <a name="assign-a-product-owner-to-a-product"></a><span data-ttu-id="be55c-119">Bir ürüne ürün sahibi atama</span><span class="sxs-lookup"><span data-stu-id="be55c-119">Assign a product owner to a product</span></span>

<span data-ttu-id="be55c-120">Bir ürüne ürün sahibi atamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="be55c-120">To assign a product owner to a product, follow these steps.</span></span>

1. <span data-ttu-id="be55c-121">İlgili ürün veya ana ürünün **Ürün ayrıntıları** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="be55c-121">Open the **Product details** page for the relevant product or product master.</span></span>
1. <span data-ttu-id="be55c-122">**Genel** hızlı sekmesinde, **Ürün sahibi** alanını ilgili ürün sahibi grubunun adına ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="be55c-122">On the **General** FastTab, set the **Product owner** field to the name of the relevant product owner group.</span></span>

<span data-ttu-id="be55c-123">Ürün sahibi bir ürüne atandığında, yalnızca ürün sahibi grubunun üyeleri **ürün sahibi** ayarını düzenleyebilir.</span><span class="sxs-lookup"><span data-stu-id="be55c-123">While a product owner is assigned to a product, only the members of the product owner group can edit the **Product owner** setting.</span></span>

<span data-ttu-id="be55c-124">Ürün sahibi **Serbest bırakılan ürünler** sayfasında da görünür.</span><span class="sxs-lookup"><span data-stu-id="be55c-124">The product owner is also visible on the **Released products** page.</span></span>

## <a name="product-owners-and-product-releases"></a><span data-ttu-id="be55c-125">Ürün sahipleri ve ürün serbest bırakmaları</span><span class="sxs-lookup"><span data-stu-id="be55c-125">Product owners and product releases</span></span>

<span data-ttu-id="be55c-126">Yalnızca bir ürünün ürün sahibi grubundaki kullanıcılar söz konusu ürünü serbest bırakabilir.</span><span class="sxs-lookup"><span data-stu-id="be55c-126">Only users from a product's product owner group can release that product.</span></span> <span data-ttu-id="be55c-127">Ancak, ürün bir alt öğe olduğunda ve üst öğesi üst öğenin sahibi tarafından serbest bırakıldığında bir özel durum vardır.</span><span class="sxs-lookup"><span data-stu-id="be55c-127">However, there is an exception when the product is a child item, and its parent is released by the parent's owner.</span></span> <span data-ttu-id="be55c-128">Başka bir deyişle, ürün başka bir ürünün ürün reçetesinin parçasıysa, sistem ürün reçetesindeki her maddenin ürün sahibini denetlemez.</span><span class="sxs-lookup"><span data-stu-id="be55c-128">In other words, if the product is part of the BOM of another product, the system doesn't check the product owner of each item in the BOM.</span></span> <span data-ttu-id="be55c-129">Yalnızca ana maddenin ürün sahibini denetler.</span><span class="sxs-lookup"><span data-stu-id="be55c-129">It checks only the product owner of the parent item.</span></span>

<span data-ttu-id="be55c-130">Örneğin, X ürünü *Tasarım dolapları* ürün sahibi grubuna atanır.</span><span class="sxs-lookup"><span data-stu-id="be55c-130">For example, product X is assigned to the *Design cabinets* product owner group.</span></span> <span data-ttu-id="be55c-131">X ürünü, *Tasarım Hoparlörleri* ürün sahibi grubuna atanmış, Y ürününün ürün reçetesinin de bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="be55c-131">Product X is also part of the BOM of product Y, which is assigned to the *Design Speakers* product owner group.</span></span> <span data-ttu-id="be55c-132">*Tasarım Hoparlörleri* ürün sahibi grubundaki bir kullanıcı, Y ürününü ve ürün reçetesini serbest bıraktığında, X ürünü, Y ürünü ile birlikte serbest bırakılacaktır.</span><span class="sxs-lookup"><span data-stu-id="be55c-132">If a user from the *Design Speakers* product owner group releases product Y and its BOM, product X will be released together with product Y.</span></span>

## <a name="product-owners-and-approvals"></a><span data-ttu-id="be55c-133">Ürün sahipleri ve onaylar</span><span class="sxs-lookup"><span data-stu-id="be55c-133">Product owners and approvals</span></span>

<span data-ttu-id="be55c-134">Ürün sahipleri belirli mühendislik değişikliklerinin ürünleri için faydalı olup olmadığını bildiğinden, bunları mühendislik değişikliği yönetimi içindeki onay sürecinin bir parçası olarak eklemek mantıklı olur.</span><span class="sxs-lookup"><span data-stu-id="be55c-134">Because product owners know whether specific engineering changes will benefit their products, it often makes sense to include them as part of the approval process in engineering change management.</span></span> <span data-ttu-id="be55c-135">Bu yaklaşımı, mühendislik değişikliği yönetimi için kullanılan iş akışlarında katılımcı sağlayıcılar olarak ürün sahiplerini ayarlayarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="be55c-135">You can implement this approach by setting up the product owners as participant providers in the workflows that are used for engineering change management.</span></span> <span data-ttu-id="be55c-136">Sistem daha sonra, mühendislik değişikliği istekleri ve mühendislik değişikliği emirlerindeki ürünlere göre iş akışlarında onay görevleri atayacaktır.</span><span class="sxs-lookup"><span data-stu-id="be55c-136">The system will then assign approval tasks in the workflows, based on the products that are in engineering change requests and engineering change orders.</span></span> <span data-ttu-id="be55c-137">Daha fazla bilgi için bkz. [Mühendislik ürünlerindeki değişiklikleri yönetme](engineering-change-management.md).</span><span class="sxs-lookup"><span data-stu-id="be55c-137">For more information, see [Manage changes to engineering products](engineering-change-management.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]