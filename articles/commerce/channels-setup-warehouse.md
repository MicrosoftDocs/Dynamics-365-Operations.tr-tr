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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 772c7584549b30a34e371a7911131edc01214ed8
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477646"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="47434-103">Ambarı ayarlama</span><span class="sxs-lookup"><span data-stu-id="47434-103">Warehouse set up</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="47434-104">Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir kanalla kullanılacak bir ambarın nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="47434-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="47434-105">Her Commerce kanalı, yapılandırılmış bir ambarın kendisiyle ilişkilendirilmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="47434-105">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="47434-106">Aşağıdaki yordamlarda, bir Commerce kanalı için ambar ayarlamak üzere gereken minimum yapılandırma verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="47434-106">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="47434-107">Ambar kurulumuyla ilgili daha fazla bilgi için lütfen [Ambar yönetimine genel bakış](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)'a bakın.</span><span class="sxs-lookup"><span data-stu-id="47434-107">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="47434-108">Bir ambar tesisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="47434-108">Configure a warehouse site</span></span>

<span data-ttu-id="47434-109">Ambarı ayarlamadan önce bir ambar tesisi yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="47434-109">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="47434-110">Bir ambar tesisini yapılandırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="47434-110">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="47434-111">Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Kanal kurulumu \> Tesisler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="47434-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="47434-112">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="47434-113">**Tesis** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="47434-113">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="47434-114">**Ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="47434-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="47434-115">**Genel** bölümünde, uygun **Saat dilimini** ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="47434-115">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="47434-116">**Adresler** bölümünde bir adres girin.</span><span class="sxs-lookup"><span data-stu-id="47434-116">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="47434-117">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-117">On the action pane, select **Save**.</span></span>

<span data-ttu-id="47434-118">Aşağıdaki resimde örnek bir ambar tesisi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="47434-118">The following image shows an example warehouse site.</span></span>

![Örnek ambar tesisi](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="47434-120">Ambar ayarlama</span><span class="sxs-lookup"><span data-stu-id="47434-120">Set up a warehouse</span></span>

<span data-ttu-id="47434-121">Bir ambarı ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="47434-121">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="47434-122">Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Kanal kurulumu \> Ambarlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="47434-122">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="47434-123">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-123">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="47434-124">**Ambar** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="47434-124">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="47434-125">Bu, bir mağazayla 1:1 eşleşme ise mağaza adını veya bir bölgesel dağıtım merkezinin adını kullanmayı düşünebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47434-125">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="47434-126">**Ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="47434-126">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="47434-127">**Tesis** açılır listesinde, önceden oluşturulan ambar tesisini seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-127">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="47434-128">**Tür** alanında, **Varsayılan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-128">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="47434-129">Bir **Karantina ambarı** ayarlamak istiyorsanız, bu adımları izleyerek, **Tür** ayarı **Karantina** olan ek bir ambar oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="47434-129">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="47434-130">Bir **Transit ambarı** ayarlamak istiyorsanız, bu adımları izleyerek, **Tür** ayarı **Transit** olan ek bir ambar oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="47434-130">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="47434-131">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-131">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="47434-132">Stok koridorlarını ayarla</span><span class="sxs-lookup"><span data-stu-id="47434-132">Set up inventory aisles</span></span>

<span data-ttu-id="47434-133">Stok koridorları ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="47434-133">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="47434-134">Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Kanal kurulumu \> Yerleşim ayarı \> Stok koridorları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="47434-134">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="47434-135">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-135">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="47434-136">**Ambar** açılır listesinde, önceden oluşturulan ambarı seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-136">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="47434-137">**Koridor** alanına bir ad girin (örneğin "Var").</span><span class="sxs-lookup"><span data-stu-id="47434-137">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="47434-138">**Ad** alanına bir ad girin (örneğin "Varsayılan koridor").</span><span class="sxs-lookup"><span data-stu-id="47434-138">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="47434-139">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-139">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="47434-140">Ambar stok yerleşimlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="47434-140">Set up warehouse inventory locations</span></span>

<span data-ttu-id="47434-141">Standart, hasarlı ve iade stok için ambar stok yerleşimleri ayarlamak üzere bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="47434-141">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="47434-142">Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Kanal kurulumu \> Ambarlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="47434-142">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="47434-143">Daha önce oluşturduğunuz ambarı seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-143">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="47434-144">Eylem bölmesinde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-144">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="47434-145">Eylem bölmesinde **Ambar**'ı ve ardından **Stok yerleşimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-145">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="47434-146">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-146">On the action pane, select **New**.</span></span> <span data-ttu-id="47434-147">**Ambar** açılır listesi varsayılan olarak yeni ambarınızı gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="47434-147">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="47434-148">**Koridor** kutusuna, daha önce belirttiğiniz koridorun adını girin.</span><span class="sxs-lookup"><span data-stu-id="47434-148">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="47434-149">**El ile güncelleştirme** ayarını **Evet** yapın.</span><span class="sxs-lookup"><span data-stu-id="47434-149">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="47434-150">**Yerleşim** kutusuna ambarın adını girin.</span><span class="sxs-lookup"><span data-stu-id="47434-150">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="47434-151">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-151">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="47434-152">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-152">On the action pane, select **New**.</span></span>  <span data-ttu-id="47434-153">**Ambar** açılır listesi varsayılan olarak yeni ambarınızı gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="47434-153">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="47434-154">**Koridor** kutusuna, daha önce belirttiğiniz koridorun adını girin.</span><span class="sxs-lookup"><span data-stu-id="47434-154">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="47434-155">**El ile güncelleştirme** ayarını **Evet** yapın.</span><span class="sxs-lookup"><span data-stu-id="47434-155">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="47434-156">**Yerleşim** kutusuna "Hasarlı" girin.</span><span class="sxs-lookup"><span data-stu-id="47434-156">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="47434-157">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-157">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="47434-158">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-158">On the action pane, select **New**.</span></span>  <span data-ttu-id="47434-159">**Ambar** açılır listesi varsayılan olarak yeni ambarınızı gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="47434-159">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="47434-160">**Koridor** kutusuna, daha önce belirttiğiniz koridorun adını girin.</span><span class="sxs-lookup"><span data-stu-id="47434-160">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="47434-161">**El ile güncelleştirme** ayarını **Evet** yapın.</span><span class="sxs-lookup"><span data-stu-id="47434-161">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="47434-162">**Yerleşim** kutusuna "İadeler" girin.</span><span class="sxs-lookup"><span data-stu-id="47434-162">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="47434-163">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-163">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="47434-164">Aşağıdaki resimde San Francisco'daki bir ambar stok yerleşiminin kurulumu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="47434-164">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Örnek stok yerleşimi kurulumu](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="47434-166">Ambar kurulumunu tamamlama</span><span class="sxs-lookup"><span data-stu-id="47434-166">Complete warehouse setup</span></span>

<span data-ttu-id="47434-167">Ambar kurulumunu tamamlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="47434-167">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="47434-168">Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Kanal kurulumu \> Ambarlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="47434-168">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="47434-169">Daha önce oluşturduğunuz ambarı seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-169">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="47434-170">Eylem bölmesinde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-170">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="47434-171">**Stok ve ambar yönetimi** altında:</span><span class="sxs-lookup"><span data-stu-id="47434-171">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="47434-172">**Varsayılan yerleşim konumu**'nu yukarıda oluşturulan varsayılan yerleşime ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="47434-172">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="47434-173">**Varsayılan çıkış yeri yerleşimi**'ni yukarıda oluşturulan varsayılan yerleşime ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="47434-173">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="47434-174">**Adresler** bölümü altında bir ambar adresi girin.</span><span class="sxs-lookup"><span data-stu-id="47434-174">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="47434-175">**Perakende** bölümünün altında:</span><span class="sxs-lookup"><span data-stu-id="47434-175">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="47434-176">**Varsayılan iade yerleşimi** kutusuna, önceden oluşturulan iade yerleşimini girin.</span><span class="sxs-lookup"><span data-stu-id="47434-176">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="47434-177">**Mağaza**'yı **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="47434-177">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="47434-178">**Ağırlık** ayarını **1,00** yapın.</span><span class="sxs-lookup"><span data-stu-id="47434-178">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="47434-179">**Depolama Boyutları** kutusuna, önceden oluşturulan varsayılan yerleşimi girin.</span><span class="sxs-lookup"><span data-stu-id="47434-179">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="47434-180">**Ambar** bölümünün altında, **Fiziksel negatif stok** ayarını **Evet** yapın.</span><span class="sxs-lookup"><span data-stu-id="47434-180">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="47434-181">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="47434-181">On the action pane, select **Save**.</span></span>

<span data-ttu-id="47434-182">Aşağıdaki resimde, yapılandırılmış bir ambarın ayrıntıları gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="47434-182">The following image shows details for a configured warehouse.</span></span>

![Yapılandırılmış ambar örneği](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="47434-184">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="47434-184">Additional resources</span></span>

[<span data-ttu-id="47434-185">Ambar yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="47434-185">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="47434-186">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="47434-186">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="47434-187">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="47434-187">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="47434-188">Perakende kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="47434-188">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="47434-189">Çevrimiçi kanal ayarlama</span><span class="sxs-lookup"><span data-stu-id="47434-189">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="47434-190">Çağrı merkezi kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="47434-190">Set up a call center channel</span></span>](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]
