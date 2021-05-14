---
title: İndirim yönetimi grupları
description: Bu konuda, indirim yönetimi grupları için veri ayarlama yöntemi açıklanmaktadır. İndirim Yönetimi grupları, indirim hesaplamaları sırasında kullanılabilir ve bir ana kayda bağlanabilir.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: cef7abbbf2a94e26b6b9e66492cd7347d3b4d1f2
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920073"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="8a8ef-104">İndirim yönetimi grupları</span><span class="sxs-lookup"><span data-stu-id="8a8ef-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a8ef-105">İndirim ve kesinti hesaplamaları gruplar ile yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-105">Rebate and deduction calculations can be driven by groups.</span></span> <span data-ttu-id="8a8ef-106">İndirim Yönetimi grupları müşteriler, satıcılar ve maddeler için oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="8a8ef-107">Bunlar bir ana kayda eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="8a8ef-108">İndirim yönetimi müşteri grupları</span><span class="sxs-lookup"><span data-stu-id="8a8ef-108">Rebate management customer groups</span></span>

<span data-ttu-id="8a8ef-109">Bir müşteri grubu için hesaplama genellikle, süpermarket zinciri veya franchise şirket gibi bir şirketler zinciri için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="8a8ef-110">Bu hesaplama türü genellikle bir indirim ile ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="8a8ef-111">Bir kesinti genellikle, uygun siparişin kime satıldığını düşünmeden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="8a8ef-112">Ancak, istisnalar vardır.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-112">However, there are exceptions.</span></span> <span data-ttu-id="8a8ef-113">Örneğin, bir lisans sahibi, müşteri grubu A'nın yüzde 4 ancak müşteri grubu B'nin yalnızca yüzde 3 alacağı bir kesinti düzeni oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="8a8ef-114">Müşteri gruplarını ayarla</span><span class="sxs-lookup"><span data-stu-id="8a8ef-114">Set up customer groups</span></span>

<span data-ttu-id="8a8ef-115">İndirim yönetimi müşteri grubu ile çalışmak için, **indirim Yönetimi \> İndirim yönetim grupları kurulumu \> Müşteri grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="8a8ef-116">Gereken şekilde grupları eklemek ve kaldırmak için eylem bölmesindeki düğmeleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="8a8ef-117">Her grup için aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="8a8ef-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="8a8ef-118">**İndirim yönetimi grubu**: Grup için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="8a8ef-119">**Açıklama**: Nasıl kullanılması gerektiği hakkında daha fazla bilgi sağlayan grup açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="8a8ef-120">Müşteri grubu atamalarını Yönetme</span><span class="sxs-lookup"><span data-stu-id="8a8ef-120">Manage customer group assignments</span></span>

<span data-ttu-id="8a8ef-121">Her müşteri bir dizi indirim Yönetimi grubuna ait olabilir.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="8a8ef-122">Grup üyelerini görüntülemek ve atamak için, Grup listesinden veya müşteri listesinden başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="8a8ef-123">Seçili bir grup için müşterileri görüntülemek, eklemek veya kaldırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="8a8ef-124">**İndirim yönetimi \> indirim Yönetimi grupları kurulumu \> müşteri grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="8a8ef-125">Yönetilecek grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-125">Select the group to manage.</span></span>
1. <span data-ttu-id="8a8ef-126">Eylem Bölmesinde **Müşteriler** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="8a8ef-127">**İndirim Yönetimi grupları** sayfası görüntülenir ve zaten seçili grubun üyesi olan müşterilerin bir listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="8a8ef-128">Gruba yeni müşteri eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve ızgaraya bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="8a8ef-129">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="8a8ef-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="8a8ef-130">**Müşteri hesabı**: Müşteri hesap kimliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-130">**Customer account** – Select the customer account ID.</span></span>
    - <span data-ttu-id="8a8ef-131">**Ad**: Müşterinin adını ve/veya açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-131">**Name** – Enter a name and/or description of the customer.</span></span>

1. <span data-ttu-id="8a8ef-132">Bir müşteriyi gruptan kaldırmak için, müşteriyi seçin ve sonra Eylem bölmesinde **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-132">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="8a8ef-133">Seçili bir müşteri için grup atamalarını görüntülemek, eklemek veya kaldırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-133">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="8a8ef-134">**Alacak hesapları \> Müşteriler \> Tüm müşteriler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-134">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="8a8ef-135">Çalışmak istediğiniz müşteriyi seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-135">Select the customer to work with.</span></span>
1. <span data-ttu-id="8a8ef-136">Eylem Bölmesi'nde, **Müşteri** sekmesindeki **İndirim yönetimi** grubunda **İndirim yönetimi grupları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-136">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="8a8ef-137">**İndirim Yönetimi grupları** sayfası görüntülenir ve seçili müşterinin zaten üyesi olduğu bir grup listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-137">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="8a8ef-138">Müşteriyi yeni bir gruba eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve ızgaraya bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-138">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="8a8ef-139">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="8a8ef-139">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="8a8ef-140">**İndirim yönetimi grubu**: Müşterinin ekleneceği grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-140">**Rebate management group** – Select the group to add the customer to.</span></span>
    - <span data-ttu-id="8a8ef-141">**Açıklama**: Grubun açıklamasını girin (örneğin, müşterinin neden üyesi olduğunu açıklamak için).</span><span class="sxs-lookup"><span data-stu-id="8a8ef-141">**Description** – Enter a description of the group (for example, to explain why the customer is a member of it).</span></span>

1. <span data-ttu-id="8a8ef-142">Bir müşteriyi gruptan kaldırmak için, grubu seçin ve sonra Eylem bölmesinde **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-142">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="8a8ef-143">İndirim yönetimi satıcı grupları</span><span class="sxs-lookup"><span data-stu-id="8a8ef-143">Rebate management vendor groups</span></span>

<span data-ttu-id="8a8ef-144">Bir grup satıcı için hesaplama genellikle bir grup teslimat noktası için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-144">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="8a8ef-145">Bu hesaplama türü genellikle bir indirim ile ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-145">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="8a8ef-146">Satıcı gruplarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="8a8ef-146">Set up vendor groups</span></span>

<span data-ttu-id="8a8ef-147">İndirim yönetimi satıcı grubu ile çalışmak için, **indirim Yönetimi \> İndirim yönetim grupları kurulumu \> Satıcı grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-147">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="8a8ef-148">Gereken şekilde grupları eklemek ve kaldırmak için eylem bölmesindeki düğmeleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-148">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="8a8ef-149">Her grup için aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="8a8ef-149">For each group, set the following fields:</span></span>

- <span data-ttu-id="8a8ef-150">**İndirim yönetimi grubu**: Grup için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-150">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="8a8ef-151">**Açıklama**: Nasıl kullanılması gerektiği hakkında daha fazla bilgi sağlayan grup açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-151">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="8a8ef-152">Satıcı grubu atamalarını Yönetme</span><span class="sxs-lookup"><span data-stu-id="8a8ef-152">Manage vendor group assignments</span></span>

<span data-ttu-id="8a8ef-153">Her satıcı bir dizi indirim Yönetimi grubuna ait olabilir.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-153">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="8a8ef-154">Grup üyelerini görüntülemek ve atamak için, Grup listesinden veya satıcı listesinden başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-154">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="8a8ef-155">Seçili bir grup için satıcıları görüntülemek, eklemek veya kaldırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-155">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="8a8ef-156">**İndirim yönetimi \> indirim Yönetimi grupları kurulumu \> satıcı grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-156">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="8a8ef-157">Yönetilecek grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-157">Select the group to manage.</span></span>
1. <span data-ttu-id="8a8ef-158">Eylem Bölmesinde, **Satıcılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-158">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="8a8ef-159">**İndirim Yönetimi grupları** sayfası görüntülenir ve zaten seçili grubun üyesi olan satıcıların bir listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-159">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="8a8ef-160">Yeni bir satıcıyı gruba eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve ızgaraya bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-160">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="8a8ef-161">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="8a8ef-161">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="8a8ef-162">**satıcı hesabı**: satıcı hesap kimliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-162">**Vendor account** – Select the vendor account ID.</span></span>
    - <span data-ttu-id="8a8ef-163">**Ad**: Satıcının adını ve/veya açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-163">**Name** – Enter a name and/or description of the vendor.</span></span>

1. <span data-ttu-id="8a8ef-164">Bir satıcıyı gruptan kaldırmak için, satıcıyı seçin ve sonra Eylem bölmesinde **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-164">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="8a8ef-165">Seçili bir satıcı için grup atamalarını görüntülemek, eklemek veya kaldırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-165">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="8a8ef-166">**Borç hesapları \> Satıcılar \> Tüm satıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-166">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="8a8ef-167">Çalışmak istediğiniz satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-167">Select the vendor to work with.</span></span>
1. <span data-ttu-id="8a8ef-168">Eylem Bölmesi'nde, **satıcı** sekmesindeki **İndirim yönetimi** grubunda **İndirim yönetimi grupları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-168">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="8a8ef-169">**İndirim Yönetimi grupları** sayfası görüntülenir ve seçili satıcının zaten üyesi olduğu bir grup listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-169">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="8a8ef-170">Satıcıyı yeni bir gruba eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve ızgaraya bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-170">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="8a8ef-171">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="8a8ef-171">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="8a8ef-172">**İndirim yönetimi grubu**: Satıcının ekleneceği grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-172">**Rebate management group** – Select the group to add the vendor to.</span></span>
    - <span data-ttu-id="8a8ef-173">**Açıklama**: Grubun açıklamasını girin (örneğin, satıcının neden üyesi olduğunu açıklamak için).</span><span class="sxs-lookup"><span data-stu-id="8a8ef-173">**Description** – Enter a description of the group (for example, to explain why the vendor is a member of it).</span></span>

1. <span data-ttu-id="8a8ef-174">Bir satıcıyı gruptan kaldırmak için, grubu seçin ve sonra Eylem bölmesinde **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-174">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="8a8ef-175">Madde indirim grupları</span><span class="sxs-lookup"><span data-stu-id="8a8ef-175">Item rebate groups</span></span>

<span data-ttu-id="8a8ef-176">Öğeleri gruplandırarak, indirimler ve kesintiler hesaplanırken daha fazla esnekliğe sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-176">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="8a8ef-177">Bu yaklaşım genellikle müşteriler ve satıcılar için indirimleri ve kesintileri ayarlamak için daha etkili bir yoldur.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-177">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="8a8ef-178">Madde gruplarını ayarla</span><span class="sxs-lookup"><span data-stu-id="8a8ef-178">Set up item groups</span></span>

<span data-ttu-id="8a8ef-179">İndirim yönetimi madde grubu ile çalışmak için, **indirim Yönetimi \> İndirim yönetim grupları kurulumu \> Madde grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-179">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="8a8ef-180">Gereken şekilde grupları eklemek ve kaldırmak için eylem bölmesindeki düğmeleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-180">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="8a8ef-181">Her grup için aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="8a8ef-181">For each group, set the following fields:</span></span>

- <span data-ttu-id="8a8ef-182">**İndirim yönetimi grubu**: Grup için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-182">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="8a8ef-183">**Açıklama**: Nasıl kullanılması gerektiği hakkında daha fazla bilgi sağlayan grup açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-183">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="8a8ef-184">Madde grubu atamalarını Yönetme</span><span class="sxs-lookup"><span data-stu-id="8a8ef-184">Manage item group assignments</span></span>

<span data-ttu-id="8a8ef-185">Her madde bir dizi indirim Yönetimi grubuna ait olabilir.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-185">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="8a8ef-186">Grup üyelerini görüntülemek ve atamak için, Grup listesinden veya madde listesinden başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-186">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="8a8ef-187">Ayrıca kategori hiyerarşinize göre de madde ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-187">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="8a8ef-188">Seçili bir grup için maddeleri görüntülemek, eklemek veya kaldırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-188">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="8a8ef-189">**İndirim yönetimi \> indirim Yönetimi grupları kurulumu \> Madde grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-189">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="8a8ef-190">Yönetilecek grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-190">Select the group to manage.</span></span>
1. <span data-ttu-id="8a8ef-191">Eylem Bölmesinde, **Maddeler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-191">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="8a8ef-192">**İndirim Yönetimi grupları** sayfası görüntülenir ve zaten seçili grubun üyesi olan maddelerin bir listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-192">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="8a8ef-193">Yeni bir maddeyi gruba eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve ızgaraya bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-193">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="8a8ef-194">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="8a8ef-194">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="8a8ef-195">**Madde hesabı**: Madde hesap kimliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-195">**Item account** – Select the item account ID.</span></span>
    - <span data-ttu-id="8a8ef-196">**Ürün Adı**: Maddenin adını ve/veya açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-196">**Product name** – Enter a name and/or description of the item.</span></span>

1. <span data-ttu-id="8a8ef-197">Bir maddeyi gruptan kaldırmak için, maddeyi seçin ve sonra Eylem bölmesinde **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-197">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="8a8ef-198">Seçili bir madde için grup atamalarını görüntülemek, eklemek veya kaldırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-198">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="8a8ef-199">**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-199">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="8a8ef-200">Çalışmak istediğiniz maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-200">Select the item to work with.</span></span>
1. <span data-ttu-id="8a8ef-201">Eylem Bölmesi'nde, **Ürün** sekmesindeki **İndirim yönetimi** grubunda **İndirim yönetimi grupları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-201">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="8a8ef-202">**İndirim Yönetimi grupları** sayfası görüntülenir ve seçili maddenin zaten üyesi olduğu bir grup listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-202">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="8a8ef-203">Maddeyi yeni bir gruba eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve ızgaraya bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-203">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="8a8ef-204">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="8a8ef-204">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="8a8ef-205">**İndirim yönetimi grubu**: Maddenin ekleneceği grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-205">**Rebate management group** – Select the group to add the item to.</span></span>
    - <span data-ttu-id="8a8ef-206">**Açıklama**: Grubun açıklamasını girin (örneğin, maddenin neden üyesi olduğunu açıklamak için).</span><span class="sxs-lookup"><span data-stu-id="8a8ef-206">**Description** – Enter a description of the group (for example, to explain why the item is a member of it).</span></span>

1. <span data-ttu-id="8a8ef-207">Bir maddeyi gruptan kaldırmak için, grubu seçin ve sonra Eylem bölmesinde **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-207">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="8a8ef-208">Kategori hiyerarşinize dayalı olarak bir gruba madde eklemek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-208">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="8a8ef-209">**İndirim yönetimi \> indirim Yönetimi grupları kurulumu \> Madde grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-209">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="8a8ef-210">Yönetilecek grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-210">Select the group to manage.</span></span>
1. <span data-ttu-id="8a8ef-211">Eylem Bölmesinde, **Madde ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-211">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="8a8ef-212">**Madde Ekle** iletişim kutusunda, **Kategori hiyerarşisi** alanında, üst düzey bir kategori seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-212">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="8a8ef-213">Madde hiyerarşisi sol bölmede açılır.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-213">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="8a8ef-214">Aradığınız hiyerarşi düzeyini seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-214">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="8a8ef-215">Seçili hiyerarşi ve hiyerarşi düzeyindeki maddeler şimdi sağ bölmede listelenir.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-215">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="8a8ef-216">Bölmeyle çalışmak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="8a8ef-216">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="8a8ef-217">Eklemek istediğiniz her madde için onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-217">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="8a8ef-218">Listelenen tüm maddeleri seçmek için kılavuz üstbilgisindeki onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-218">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="8a8ef-219">Kılavuza yalnızca şimdiye kadar seçtiğiniz öğeleri gösterecek şekilde filtre uygulamak için **Seçileni göster** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-219">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="8a8ef-220">Tam listeye dönmek için düğmeyi tekrar seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-220">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="8a8ef-221">Madde seçiminizi seçili gruba uygulamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8a8ef-221">Select **OK** to apply your item selection to the selected group.</span></span>
