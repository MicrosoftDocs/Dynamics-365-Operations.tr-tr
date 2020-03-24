---
title: Ambar ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir kanalla kullanılacak bir ambarın nasıl ayarlanacağı açıklanmaktadır.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6da72ae612f0520965a2b11a21123d4642303ac3
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113771"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="ddeaa-103">Ambarı ayarlama</span><span class="sxs-lookup"><span data-stu-id="ddeaa-103">Warehouse set up</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ddeaa-104">Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir kanalla kullanılacak bir ambarın nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ddeaa-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="ddeaa-105">Overview</span></span>

<span data-ttu-id="ddeaa-106">Her Commerce kanalı, yapılandırılmış bir ambarın kendisiyle ilişkilendirilmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-106">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="ddeaa-107">Aşağıdaki yordamlarda, bir Commerce kanalı için ambar ayarlamak üzere gereken minimum yapılandırma verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-107">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="ddeaa-108">Ambar kurulumuyla ilgili daha fazla bilgi için lütfen [Ambar yönetimine genel bakış](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)'a bakın.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-108">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="ddeaa-109">Bir ambar tesisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="ddeaa-109">Configure a warehouse site</span></span>

<span data-ttu-id="ddeaa-110">Ambarı ayarlamadan önce bir ambar tesisi yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-110">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="ddeaa-111">Bir ambar tesisini yapılandırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-111">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="ddeaa-112">Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Kanal kurulumu \> Tesisler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-112">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="ddeaa-113">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ddeaa-114">**Tesis** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-114">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="ddeaa-115">**Ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-115">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="ddeaa-116">**Genel** bölümünde, uygun **Saat dilimini** ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-116">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="ddeaa-117">**Adresler** bölümünde bir adres girin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-117">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="ddeaa-118">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ddeaa-119">Aşağıdaki resimde örnek bir ambar tesisi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-119">The following image shows an example warehouse site.</span></span>

![Örnek ambar tesisi](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="ddeaa-121">Ambar ayarlama</span><span class="sxs-lookup"><span data-stu-id="ddeaa-121">Set up a warehouse</span></span>

<span data-ttu-id="ddeaa-122">Bir ambarı ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-122">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="ddeaa-123">Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Kanal kurulumu \> Ambarlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-123">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="ddeaa-124">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-124">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ddeaa-125">**Ambar** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-125">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="ddeaa-126">Bu, bir mağazayla 1:1 eşleşme ise mağaza adını veya bir bölgesel dağıtım merkezinin adını kullanmayı düşünebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-126">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="ddeaa-127">**Ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-127">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="ddeaa-128">**Tesis** açılır listesinde, önceden oluşturulan ambar tesisini seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-128">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="ddeaa-129">**Tür** alanında, **Varsayılan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-129">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="ddeaa-130">Bir **Karantina ambarı** ayarlamak istiyorsanız, bu adımları izleyerek, **Tür** ayarı **Karantina** olan ek bir ambar oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-130">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="ddeaa-131">Bir **Transit ambarı** ayarlamak istiyorsanız, bu adımları izleyerek, **Tür** ayarı **Transit** olan ek bir ambar oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-131">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="ddeaa-132">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-132">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="ddeaa-133">Stok koridorlarını ayarla</span><span class="sxs-lookup"><span data-stu-id="ddeaa-133">Set up inventory aisles</span></span>

<span data-ttu-id="ddeaa-134">Stok koridorları ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-134">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="ddeaa-135">Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Kanal kurulumu \> Yerleşim ayarı \> Stok koridorları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-135">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="ddeaa-136">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ddeaa-137">**Ambar** açılır listesinde, önceden oluşturulan ambarı seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-137">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="ddeaa-138">**Koridor** alanına bir ad girin (örneğin "Var").</span><span class="sxs-lookup"><span data-stu-id="ddeaa-138">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="ddeaa-139">**Ad** alanına bir ad girin (örneğin "Varsayılan koridor").</span><span class="sxs-lookup"><span data-stu-id="ddeaa-139">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="ddeaa-140">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-140">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="ddeaa-141">Ambar stok yerleşimlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="ddeaa-141">Set up warehouse inventory locations</span></span>

<span data-ttu-id="ddeaa-142">Standart, hasarlı ve iade stok için ambar stok yerleşimleri ayarlamak üzere bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-142">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="ddeaa-143">Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Kanal kurulumu \> Ambarlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-143">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="ddeaa-144">Daha önce oluşturduğunuz ambarı seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-144">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="ddeaa-145">Eylem bölmesinde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-145">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="ddeaa-146">Eylem bölmesinde **Ambar**'ı ve ardından **Stok yerleşimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-146">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="ddeaa-147">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-147">On the action pane, select **New**.</span></span> <span data-ttu-id="ddeaa-148">**Ambar** açılır listesi varsayılan olarak yeni ambarınızı gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-148">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="ddeaa-149">**Koridor** kutusuna, daha önce belirttiğiniz koridorun adını girin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-149">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="ddeaa-150">**El ile güncelleştirme** ayarını **Evet** yapın.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-150">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="ddeaa-151">**Yerleşim** kutusuna ambarın adını girin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-151">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="ddeaa-152">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-152">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="ddeaa-153">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-153">On the action pane, select **New**.</span></span>  <span data-ttu-id="ddeaa-154">**Ambar** açılır listesi varsayılan olarak yeni ambarınızı gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-154">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="ddeaa-155">**Koridor** kutusuna, daha önce belirttiğiniz koridorun adını girin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-155">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="ddeaa-156">**El ile güncelleştirme** ayarını **Evet** yapın.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-156">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="ddeaa-157">**Yerleşim** kutusuna "Hasarlı" girin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-157">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="ddeaa-158">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-158">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="ddeaa-159">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-159">On the action pane, select **New**.</span></span>  <span data-ttu-id="ddeaa-160">**Ambar** açılır listesi varsayılan olarak yeni ambarınızı gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-160">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="ddeaa-161">**Koridor** kutusuna, daha önce belirttiğiniz koridorun adını girin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-161">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="ddeaa-162">**El ile güncelleştirme** ayarını **Evet** yapın.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-162">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="ddeaa-163">**Yerleşim** kutusuna "İadeler" girin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-163">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="ddeaa-164">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-164">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="ddeaa-165">Aşağıdaki resimde San Francisco'daki bir ambar stok yerleşiminin kurulumu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-165">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Örnek stok yerleşimi kurulumu](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="ddeaa-167">Ambar kurulumunu tamamlama</span><span class="sxs-lookup"><span data-stu-id="ddeaa-167">Complete warehouse setup</span></span>

<span data-ttu-id="ddeaa-168">Ambar kurulumunu tamamlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-168">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="ddeaa-169">Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Kanal kurulumu \> Ambarlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-169">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="ddeaa-170">Daha önce oluşturduğunuz ambarı seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-170">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="ddeaa-171">Eylem bölmesinde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-171">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="ddeaa-172">**Stok ve ambar yönetimi** altında:</span><span class="sxs-lookup"><span data-stu-id="ddeaa-172">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="ddeaa-173">**Varsayılan yerleşim konumu**'nu yukarıda oluşturulan varsayılan yerleşime ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-173">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="ddeaa-174">**Varsayılan çıkış yeri yerleşimi**'ni yukarıda oluşturulan varsayılan yerleşime ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-174">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="ddeaa-175">**Adresler** bölümü altında bir ambar adresi girin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-175">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="ddeaa-176">**Perakende** bölümünün altında:</span><span class="sxs-lookup"><span data-stu-id="ddeaa-176">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="ddeaa-177">**Varsayılan iade yerleşimi** kutusuna, önceden oluşturulan iade yerleşimini girin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-177">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="ddeaa-178">**Mağaza**'yı **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-178">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="ddeaa-179">**Ağırlık** ayarını **1,00** yapın.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-179">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="ddeaa-180">**Depolama Boyutları** kutusuna, önceden oluşturulan varsayılan yerleşimi girin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-180">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="ddeaa-181">**Ambar** bölümünün altında, **Fiziksel negatif stok** ayarını **Evet** yapın.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-181">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="ddeaa-182">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-182">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ddeaa-183">Aşağıdaki resimde, yapılandırılmış bir ambarın ayrıntıları gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ddeaa-183">The following image shows details for a configured warehouse.</span></span>

![Yapılandırılmış ambar örneği](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="ddeaa-185">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ddeaa-185">Additional resources</span></span>

[<span data-ttu-id="ddeaa-186">Ambar yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="ddeaa-186">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="ddeaa-187">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="ddeaa-187">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="ddeaa-188">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="ddeaa-188">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="ddeaa-189">Perakende kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="ddeaa-189">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="ddeaa-190">Çevrimiçi kanal ayarlama</span><span class="sxs-lookup"><span data-stu-id="ddeaa-190">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="ddeaa-191">Çağrı merkezi kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="ddeaa-191">Set up a call center channel</span></span>](channel-setup-callcenter.md)





