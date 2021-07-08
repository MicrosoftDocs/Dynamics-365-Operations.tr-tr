---
title: İndirim yönetimi grupları
description: Bu konuda, indirim yönetimi grupları için veri ayarlama yöntemi açıklanmaktadır. İndirim Yönetimi grupları, indirim hesaplamaları sırasında kullanılabilir ve bir ana kayda bağlanabilir.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee5a195b3d2881ff70fb1f0d4063ed681e874648
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271089"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="a9686-104">İndirim yönetimi grupları</span><span class="sxs-lookup"><span data-stu-id="a9686-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9686-105">İndirim yönetimi hesaplamaları gruplar ile yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="a9686-105">Rebate management calculations can be driven by groups.</span></span> <span data-ttu-id="a9686-106">İndirim Yönetimi grupları müşteriler, satıcılar ve maddeler için oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="a9686-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="a9686-107">Bunlar bir ana kayda eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="a9686-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="a9686-108">İndirim yönetimi müşteri grupları</span><span class="sxs-lookup"><span data-stu-id="a9686-108">Rebate management customer groups</span></span>

<span data-ttu-id="a9686-109">Bir müşteri grubu için hesaplama genellikle, süpermarket zinciri veya franchise şirket gibi bir şirketler zinciri için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a9686-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="a9686-110">Bu hesaplama türü genellikle bir indirim ile ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="a9686-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="a9686-111">Bir kesinti genellikle, uygun siparişin kime satıldığını düşünmeden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="a9686-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="a9686-112">Ancak, istisnalar vardır.</span><span class="sxs-lookup"><span data-stu-id="a9686-112">However, there are exceptions.</span></span> <span data-ttu-id="a9686-113">Örneğin, bir lisans sahibi, müşteri grubu A'nın yüzde 4 ancak müşteri grubu B'nin yalnızca yüzde 3 alacağı bir kesinti düzeni oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="a9686-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="a9686-114">Müşteri gruplarını ayarla</span><span class="sxs-lookup"><span data-stu-id="a9686-114">Set up customer groups</span></span>

<span data-ttu-id="a9686-115">İndirim yönetimi müşteri grubu ile çalışmak için, **indirim Yönetimi \> İndirim yönetim grupları kurulumu \> Müşteri grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a9686-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="a9686-116">Gereken şekilde grupları eklemek ve kaldırmak için eylem bölmesindeki düğmeleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="a9686-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="a9686-117">Her grup için aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="a9686-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="a9686-118">**İndirim yönetimi grubu**: Grup için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="a9686-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="a9686-119">**Açıklama**: Nasıl kullanılması gerektiği hakkında daha fazla bilgi sağlayan grup açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="a9686-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="a9686-120">Müşteri grubu atamalarını Yönetme</span><span class="sxs-lookup"><span data-stu-id="a9686-120">Manage customer group assignments</span></span>

<span data-ttu-id="a9686-121">Her müşteri bir dizi indirim Yönetimi grubuna ait olabilir.</span><span class="sxs-lookup"><span data-stu-id="a9686-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="a9686-122">Grup üyelerini görüntülemek ve atamak için, Grup listesinden veya müşteri listesinden başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9686-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="a9686-123">Seçili bir grup için müşterileri görüntülemek, eklemek veya kaldırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a9686-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="a9686-124">**İndirim yönetimi \> indirim Yönetimi grupları kurulumu \> müşteri grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a9686-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="a9686-125">Yönetilecek grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-125">Select the group to manage.</span></span>
1. <span data-ttu-id="a9686-126">Eylem Bölmesinde **Müşteriler** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="a9686-127">**İndirim Yönetimi grupları** sayfası görüntülenir ve zaten seçili grubun üyesi olan müşterilerin bir listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9686-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="a9686-128">Gruba yeni müşteri eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve ızgaraya bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a9686-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="a9686-129">Ardından yeni satırda aşağıdaki alanı ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="a9686-129">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="a9686-130">**Müşteri hesabı**: Müşteri hesap kimliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-130">**Customer account** – Select the customer account ID.</span></span>

1. <span data-ttu-id="a9686-131">Bir müşteriyi gruptan kaldırmak için, müşteriyi seçin ve sonra Eylem bölmesinde **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-131">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="a9686-132">Seçili bir müşteri için grup atamalarını görüntülemek, eklemek veya kaldırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a9686-132">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="a9686-133">**Alacak hesapları \> Müşteriler \> Tüm müşteriler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="a9686-133">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="a9686-134">Çalışmak istediğiniz müşteriyi seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-134">Select the customer to work with.</span></span>
1. <span data-ttu-id="a9686-135">Eylem Bölmesi'nde, **Müşteri** sekmesindeki **İndirim yönetimi** grubunda **İndirim yönetimi grupları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-135">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="a9686-136">**İndirim Yönetimi grupları** sayfası görüntülenir ve seçili müşterinin zaten üyesi olduğu bir grup listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9686-136">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="a9686-137">Müşteriyi yeni bir gruba eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve ızgaraya bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a9686-137">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="a9686-138">Ardından yeni satırda aşağıdaki alanı ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="a9686-138">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="a9686-139">**İndirim yönetimi grubu**: Müşterinin ekleneceği grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-139">**Rebate management group** – Select the group to add the customer to.</span></span>

1. <span data-ttu-id="a9686-140">Bir müşteriyi gruptan kaldırmak için, grubu seçin ve sonra Eylem bölmesinde **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-140">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="a9686-141">İndirim yönetimi satıcı grupları</span><span class="sxs-lookup"><span data-stu-id="a9686-141">Rebate management vendor groups</span></span>

<span data-ttu-id="a9686-142">Bir grup satıcı için hesaplama genellikle bir grup teslimat noktası için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a9686-142">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="a9686-143">Bu hesaplama türü genellikle bir indirim ile ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="a9686-143">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="a9686-144">Satıcı gruplarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="a9686-144">Set up vendor groups</span></span>

<span data-ttu-id="a9686-145">İndirim yönetimi satıcı grubu ile çalışmak için, **indirim Yönetimi \> İndirim yönetim grupları kurulumu \> Satıcı grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a9686-145">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="a9686-146">Gereken şekilde grupları eklemek ve kaldırmak için eylem bölmesindeki düğmeleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="a9686-146">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="a9686-147">Her grup için aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="a9686-147">For each group, set the following fields:</span></span>

- <span data-ttu-id="a9686-148">**İndirim yönetimi grubu**: Grup için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="a9686-148">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="a9686-149">**Açıklama**: Nasıl kullanılması gerektiği hakkında daha fazla bilgi sağlayan grup açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="a9686-149">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="a9686-150">Satıcı grubu atamalarını Yönetme</span><span class="sxs-lookup"><span data-stu-id="a9686-150">Manage vendor group assignments</span></span>

<span data-ttu-id="a9686-151">Her satıcı bir dizi indirim Yönetimi grubuna ait olabilir.</span><span class="sxs-lookup"><span data-stu-id="a9686-151">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="a9686-152">Grup üyelerini görüntülemek ve atamak için, Grup listesinden veya satıcı listesinden başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9686-152">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="a9686-153">Seçili bir grup için satıcıları görüntülemek, eklemek veya kaldırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a9686-153">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="a9686-154">**İndirim yönetimi \> indirim Yönetimi grupları kurulumu \> satıcı grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a9686-154">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="a9686-155">Yönetilecek grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-155">Select the group to manage.</span></span>
1. <span data-ttu-id="a9686-156">Eylem Bölmesinde, **Satıcılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-156">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="a9686-157">**İndirim Yönetimi grupları** sayfası görüntülenir ve zaten seçili grubun üyesi olan satıcıların bir listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9686-157">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="a9686-158">Yeni bir satıcıyı gruba eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve ızgaraya bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a9686-158">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="a9686-159">Ardından yeni satırda aşağıdaki alanı ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="a9686-159">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="a9686-160">**satıcı hesabı**: satıcı hesap kimliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-160">**Vendor account** – Select the vendor account ID.</span></span>

1. <span data-ttu-id="a9686-161">Bir satıcıyı gruptan kaldırmak için, satıcıyı seçin ve sonra Eylem bölmesinde **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-161">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="a9686-162">Seçili bir satıcı için grup atamalarını görüntülemek, eklemek veya kaldırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a9686-162">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="a9686-163">**Borç hesapları \> Satıcılar \> Tüm satıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="a9686-163">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="a9686-164">Çalışmak istediğiniz satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-164">Select the vendor to work with.</span></span>
1. <span data-ttu-id="a9686-165">Eylem Bölmesi'nde, **satıcı** sekmesindeki **İndirim yönetimi** grubunda **İndirim yönetimi grupları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-165">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="a9686-166">**İndirim Yönetimi grupları** sayfası görüntülenir ve seçili satıcının zaten üyesi olduğu bir grup listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9686-166">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="a9686-167">Satıcıyı yeni bir gruba eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve ızgaraya bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a9686-167">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="a9686-168">Ardından yeni satırda aşağıdaki alanı ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="a9686-168">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="a9686-169">**İndirim yönetimi grubu**: Satıcının ekleneceği grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-169">**Rebate management group** – Select the group to add the vendor to.</span></span>

1. <span data-ttu-id="a9686-170">Bir satıcıyı gruptan kaldırmak için, grubu seçin ve sonra Eylem bölmesinde **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-170">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="a9686-171">Madde indirim grupları</span><span class="sxs-lookup"><span data-stu-id="a9686-171">Item rebate groups</span></span>

<span data-ttu-id="a9686-172">Öğeleri gruplandırarak, indirimler ve kesintiler hesaplanırken daha fazla esnekliğe sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="a9686-172">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="a9686-173">Bu yaklaşım genellikle müşteriler ve satıcılar için indirimleri ve kesintileri ayarlamak için daha etkili bir yoldur.</span><span class="sxs-lookup"><span data-stu-id="a9686-173">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="a9686-174">Madde gruplarını ayarla</span><span class="sxs-lookup"><span data-stu-id="a9686-174">Set up item groups</span></span>

<span data-ttu-id="a9686-175">İndirim yönetimi madde grubu ile çalışmak için, **indirim Yönetimi \> İndirim yönetim grupları kurulumu \> Madde grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a9686-175">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="a9686-176">Gereken şekilde grupları eklemek ve kaldırmak için eylem bölmesindeki düğmeleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="a9686-176">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="a9686-177">Her grup için aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="a9686-177">For each group, set the following fields:</span></span>

- <span data-ttu-id="a9686-178">**İndirim yönetimi grubu**: Grup için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="a9686-178">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="a9686-179">**Açıklama**: Nasıl kullanılması gerektiği hakkında daha fazla bilgi sağlayan grup açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="a9686-179">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="a9686-180">Madde grubu atamalarını Yönetme</span><span class="sxs-lookup"><span data-stu-id="a9686-180">Manage item group assignments</span></span>

<span data-ttu-id="a9686-181">Her madde bir dizi indirim Yönetimi grubuna ait olabilir.</span><span class="sxs-lookup"><span data-stu-id="a9686-181">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="a9686-182">Grup üyelerini görüntülemek ve atamak için, Grup listesinden veya madde listesinden başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9686-182">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="a9686-183">Ayrıca kategori hiyerarşinize göre de madde ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9686-183">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="a9686-184">Seçili bir grup için maddeleri görüntülemek, eklemek veya kaldırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a9686-184">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="a9686-185">**İndirim yönetimi \> indirim Yönetimi grupları kurulumu \> Madde grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a9686-185">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="a9686-186">Yönetilecek grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-186">Select the group to manage.</span></span>
1. <span data-ttu-id="a9686-187">Eylem Bölmesinde, **Maddeler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-187">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="a9686-188">**İndirim Yönetimi grupları** sayfası görüntülenir ve zaten seçili grubun üyesi olan maddelerin bir listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9686-188">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="a9686-189">Yeni bir maddeyi gruba eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve ızgaraya bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a9686-189">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="a9686-190">Ardından yeni satırda aşağıdaki alanı ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="a9686-190">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="a9686-191">**Madde hesabı**: Madde hesap kimliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-191">**Item account** – Select the item account ID.</span></span>

1. <span data-ttu-id="a9686-192">Bir maddeyi gruptan kaldırmak için, maddeyi seçin ve sonra Eylem bölmesinde **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-192">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="a9686-193">Seçili bir madde için grup atamalarını görüntülemek, eklemek veya kaldırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a9686-193">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="a9686-194">**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="a9686-194">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="a9686-195">Çalışmak istediğiniz maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-195">Select the item to work with.</span></span>
1. <span data-ttu-id="a9686-196">Eylem Bölmesi'nde, **Ürün** sekmesindeki **İndirim yönetimi** grubunda **İndirim yönetimi grupları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-196">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="a9686-197">**İndirim Yönetimi grupları** sayfası görüntülenir ve seçili maddenin zaten üyesi olduğu bir grup listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9686-197">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="a9686-198">Maddeyi yeni bir gruba eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve ızgaraya bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a9686-198">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="a9686-199">Ardından yeni satırda aşağıdaki alanı ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="a9686-199">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="a9686-200">**İndirim yönetimi grubu**: Maddenin ekleneceği grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-200">**Rebate management group** – Select the group to add the item to.</span></span>

1. <span data-ttu-id="a9686-201">Bir maddeyi gruptan kaldırmak için, grubu seçin ve sonra Eylem bölmesinde **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-201">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="a9686-202">Kategori hiyerarşinize dayalı olarak bir gruba madde eklemek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a9686-202">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="a9686-203">**İndirim yönetimi \> indirim Yönetimi grupları kurulumu \> Madde grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a9686-203">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="a9686-204">Yönetilecek grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-204">Select the group to manage.</span></span>
1. <span data-ttu-id="a9686-205">Eylem Bölmesinde, **Madde ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-205">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="a9686-206">**Madde Ekle** iletişim kutusunda, **Kategori hiyerarşisi** alanında, üst düzey bir kategori seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-206">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="a9686-207">Madde hiyerarşisi sol bölmede açılır.</span><span class="sxs-lookup"><span data-stu-id="a9686-207">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="a9686-208">Aradığınız hiyerarşi düzeyini seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-208">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="a9686-209">Seçili hiyerarşi ve hiyerarşi düzeyindeki maddeler şimdi sağ bölmede listelenir.</span><span class="sxs-lookup"><span data-stu-id="a9686-209">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="a9686-210">Bölmeyle çalışmak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="a9686-210">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="a9686-211">Eklemek istediğiniz her madde için onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a9686-211">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="a9686-212">Listelenen tüm maddeleri seçmek için kılavuz üstbilgisindeki onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-212">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="a9686-213">Kılavuza yalnızca şimdiye kadar seçtiğiniz öğeleri gösterecek şekilde filtre uygulamak için **Seçileni göster** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-213">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="a9686-214">Tam listeye dönmek için düğmeyi tekrar seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-214">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="a9686-215">Madde seçiminizi seçili gruba uygulamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a9686-215">Select **OK** to apply your item selection to the selected group.</span></span>
