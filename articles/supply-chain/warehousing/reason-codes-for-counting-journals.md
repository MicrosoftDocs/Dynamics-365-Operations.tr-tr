---
title: "Stok sayımı neden kodları"
description: "Bu konu sayım görevleri için neden kodlarının nasıl ayarlanacağını ve uygulanacağını açıklar."
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCountingReasonCodePolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 2f4332432ad73861cd9b6b6452685d3175ace56b
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---

# <a name="reason-codes-for-inventory-counting"></a><span data-ttu-id="bede6-103">Stok sayımı neden kodları</span><span class="sxs-lookup"><span data-stu-id="bede6-103">Reason codes for inventory counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bede6-104">Neden kodları sayım işleminin sonucunu ve bu işlem sırasında oluşan tutarsızlıkları analiz etmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="bede6-104">Reason codes let you analyze the results of a counting process and any discrepancies that occur during that process.</span></span> <span data-ttu-id="bede6-105">Kırılmış palet veya stok örneklerine dayanan stok ayarlaması gibi bir sayım yapma nedeni belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bede6-105">You can specify the reason for doing the count, such as a broken pallet or a stock adjustment that is based on inventory samples.</span></span>

## <a name="recommendation"></a><span data-ttu-id="bede6-106">Öneri</span><span class="sxs-lookup"><span data-stu-id="bede6-106">Recommendation</span></span>

<span data-ttu-id="bede6-107">Sistemi ayarlamadan önce neden kodları ile çalışmak için bir strateji tanımlamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="bede6-107">Before you set up the system, we recommend that you define a strategy for working with reason codes.</span></span> <span data-ttu-id="bede6-108">Örneğin, aşağıdaki soruları yanıtlamaya çalışın:</span><span class="sxs-lookup"><span data-stu-id="bede6-108">For example, try to answer the following questions:</span></span>

- <span data-ttu-id="bede6-109">Neden kodları ambarlarda zorunlu olmalı mı?</span><span class="sxs-lookup"><span data-stu-id="bede6-109">Should reason codes be mandatory on warehouses?</span></span>
- <span data-ttu-id="bede6-110">Neden kodları bazı maddelerde zorunlu mu yoksa veya isteğe bağlı mı olmalı?</span><span class="sxs-lookup"><span data-stu-id="bede6-110">Should reason codes be mandatory or optional on some items?</span></span>
- <span data-ttu-id="bede6-111">Ne kadar neden kodu gerekli?</span><span class="sxs-lookup"><span data-stu-id="bede6-111">How many reason codes do you require?</span></span>
- <span data-ttu-id="bede6-112">Barkod tarayıcısı kullanıcıları neden kodlarını nasıl kullanacak?</span><span class="sxs-lookup"><span data-stu-id="bede6-112">How should users of barcode scanners use reason codes?</span></span> <span data-ttu-id="bede6-113">Neden kodları önceden seçilmiş mi, zorunlu mu yoksa düzenlenemez mi olsun?</span><span class="sxs-lookup"><span data-stu-id="bede6-113">Should the reason codes be preselected, mandatory, or not editable?</span></span>
- <span data-ttu-id="bede6-114">Ambar çalışanları için mobil tarayıcıda farklı neden kodu davranışı gerekli mi?</span><span class="sxs-lookup"><span data-stu-id="bede6-114">Do warehouse workers require different reason code behavior on mobile scanners?</span></span> <span data-ttu-id="bede6-115">Yanıtınız evet ise, daha fazla menü öğesi oluşturabilir ve bunları farklı kişilere atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bede6-115">If the answer is yes, you can create more menu items and assign them to different people.</span></span>

## <a name="where-reason-codes-apply"></a><span data-ttu-id="bede6-116">Neden kodlarının uygulandığı yerler</span><span class="sxs-lookup"><span data-stu-id="bede6-116">Where reason codes apply</span></span>

<span data-ttu-id="bede6-117">Birden fazla neden kodu ilkesi oluşturabilirsiniz ve her neden kodu ilkesinin iki sayım nedeni kodu ilkesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="bede6-117">You can create multiple reason code policies, and each reason code policy can have two counting reason code policies.</span></span> <span data-ttu-id="bede6-118">Sayım neden kodu ilkeleri ambar düzeyi veya madde düzeyinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bede6-118">The counting reason code policies can be used at the warehouse level or the item level.</span></span>

## <a name="set-up-reason-code-policies"></a><span data-ttu-id="bede6-119">Neden kodu ilkeleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="bede6-119">Set up reason code policies</span></span>

1. <span data-ttu-id="bede6-120">**Stok yönetimi** \> **Kurulum** \> **Stok** \> **Sayım neden kodu ilkeleri**'ni seçin ve yeni bir neden kodu ilkesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bede6-120">Select **Inventory management** \> **Setup** \> **Inventory** \> **Counting reason code policies**, and create a new reason code policy.</span></span>
2. <span data-ttu-id="bede6-121">**Sayım neden kodu türü** alanında **Zorunlu** veya **İsteğe bağlı**'yı seçerek neden kodunun aşağıdaki sayım günlüklerinden birinde isteğe bağlı mı yoksa zorunlu bir eylem mi olması gerektiğini belirtin:</span><span class="sxs-lookup"><span data-stu-id="bede6-121">In the **Counting reason code type** field, select either **Mandatory** or **Optional** to specify whether selection of a reason code should be an optional or mandatory action in one of the following counting journals:</span></span>

    - <span data-ttu-id="bede6-122">Döngü Sayısı (mobil cihaz)</span><span class="sxs-lookup"><span data-stu-id="bede6-122">Cycle Count (mobile device)</span></span>
    - <span data-ttu-id="bede6-123">Nokta Sayısı (mobil cihaz)</span><span class="sxs-lookup"><span data-stu-id="bede6-123">Spot Count (mobile device)</span></span>
    - <span data-ttu-id="bede6-124">Eşik Sayısı (mobil cihaz)</span><span class="sxs-lookup"><span data-stu-id="bede6-124">Threshold Count (mobile device)</span></span>
    - <span data-ttu-id="bede6-125">Ayarlama etkin (mobil cihaz)</span><span class="sxs-lookup"><span data-stu-id="bede6-125">Adjustment In (mobile device)</span></span>
    - <span data-ttu-id="bede6-126">Ayarlama devre dışı (mobil cihaz)</span><span class="sxs-lookup"><span data-stu-id="bede6-126">Adjustment Out (mobile device)</span></span>
    - <span data-ttu-id="bede6-127">Sayım Günlüğü (zengin istemci)</span><span class="sxs-lookup"><span data-stu-id="bede6-127">Counting Journal (rich client)</span></span>

<span data-ttu-id="bede6-128">Ayrıca tek tek ambarlar ve ürünler için de neden kodu ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bede6-128">You can also set up reason codes for individual warehouses and for products.</span></span> <span data-ttu-id="bede6-129">Ürünler için neden kodu ayarı ambar ayarını yok sayabilir.</span><span class="sxs-lookup"><span data-stu-id="bede6-129">The reason code setup for products can disregard the setup for warehouses.</span></span>

## <a name="mandatory-reason-codes"></a><span data-ttu-id="bede6-130">Zorunlu neden kodları</span><span class="sxs-lookup"><span data-stu-id="bede6-130">Mandatory reason codes</span></span>

<span data-ttu-id="bede6-131">**Zorunlu** parametresi ambarlar veya maddeler için neden kodu yapılandırmasında ayarlanırsa, sayım günlüğü tamamlanamaz ve bir neden kodu sağlanan kadar kapatılır.</span><span class="sxs-lookup"><span data-stu-id="bede6-131">If the **Mandatory** parameter is set in the configuration of reason codes for warehouses or items, the counting journal can't be completed and closed until a reason code is provided.</span></span>

### <a name="set-up-reason-codes-for-warehouses"></a><span data-ttu-id="bede6-132">Ambarlar için neden kodları ayarlama</span><span class="sxs-lookup"><span data-stu-id="bede6-132">Set up reason codes for warehouses</span></span>

1. <span data-ttu-id="bede6-133">**Stok yönetimi** \> **Kurulum** \> **Stok dökümü** \> **Ambarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bede6-133">Select **Inventory Management** \> **Setup** \> **Inventory breakdown** \> **Warehouses**.</span></span>
2. <span data-ttu-id="bede6-134">**Ambar** sekmesindeki **Sayım neden kodu ilkesi** alanında, aşağıdaki seçeneklerden birini seçin:</span><span class="sxs-lookup"><span data-stu-id="bede6-134">On the **Warehouse** tab, in the **Counting reason code policy** field, select one of the following options:</span></span>

    - <span data-ttu-id="bede6-135">**Boş** – Madde için ayarlanan parametre sayım günlüklerinin ürün için zorunlu olup olmadığını belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bede6-135">**Blank** – The parameter that is set up for the item is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="bede6-136">**Zorunlu** – Ambar için sayım günlüklerinde daima bir neden kodu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="bede6-136">**Mandatory** – A reason code is always required on counting journals for the warehouse.</span></span>
    - <span data-ttu-id="bede6-137">**İsteğe bağlı** – Ambar için sayım günlüklerinde bir neden kodu gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="bede6-137">**Optional** – A reason code isn't required on counting journals for the warehouse.</span></span>

### <a name="set-up-reason-codes-for-products"></a><span data-ttu-id="bede6-138">Ürünler için neden kodları ayarlama</span><span class="sxs-lookup"><span data-stu-id="bede6-138">Set up reason codes for products</span></span>

1. <span data-ttu-id="bede6-139">**Ürün bilgileri yönetimi** \> **Ürünler** \> **Serbest bırakılan ürünler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bede6-139">Select **Product information management** \> **Products** \> **Released products**.</span></span>
2. <span data-ttu-id="bede6-140">**Ürün** sekmesinde **Sayım neden kodu ilkesi** 'ni ve aşağıdaki seçeneklerden birini seçin:</span><span class="sxs-lookup"><span data-stu-id="bede6-140">On the **Product** tab, select **Counting reason code policy**, and then select one of the following options:</span></span>

    - <span data-ttu-id="bede6-141">**Boş** – Ambar için ayarlanan parametre sayım günlüklerinin ürün için zorunlu olup olmadığını belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bede6-141">**Blank** – The parameter that is set up for the warehouse is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="bede6-142">**Zorunlu** – Ürün için sayım günlüklerinde daima bir neden kodu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="bede6-142">**Mandatory** – A reason code is always required on counting journals for the product.</span></span> <span data-ttu-id="bede6-143">Bu ayar ambar düzeyindeki neden kodu ayarını geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="bede6-143">This setting overrides any reason code setting at the warehouse level.</span></span>
    - <span data-ttu-id="bede6-144">**İsteğe bağlı** – Ürün için sayım günlüklerinde bir neden kodu gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="bede6-144">**Optional** – A reason code isn't required on counting journals for the product.</span></span> <span data-ttu-id="bede6-145">Bu ayar ambar düzeyindeki neden kodu ayarını geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="bede6-145">This setting overrides any reason code setting at the warehouse level.</span></span>

### <a name="use-reason-codes-in-counting-journals"></a><span data-ttu-id="bede6-146">Sayım günlüklerinde neden kodları kullanma</span><span class="sxs-lookup"><span data-stu-id="bede6-146">Use reason codes in counting journals</span></span>

<span data-ttu-id="bede6-147">Bir sayım günlüğüne, aşağıda türde sayımlar için neden kodları ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="bede6-147">In a counting journal, you can add reason codes for counts of the following types:</span></span>

- <span data-ttu-id="bede6-148">Döngü Sayımı</span><span class="sxs-lookup"><span data-stu-id="bede6-148">Cycle Count</span></span>
- <span data-ttu-id="bede6-149">Nokta Sayımı</span><span class="sxs-lookup"><span data-stu-id="bede6-149">Spot Count</span></span>
- <span data-ttu-id="bede6-150">Eşik Sayımı</span><span class="sxs-lookup"><span data-stu-id="bede6-150">Threshold Count</span></span>
- <span data-ttu-id="bede6-151">Ayarlama etkin</span><span class="sxs-lookup"><span data-stu-id="bede6-151">Adjustment In</span></span>
- <span data-ttu-id="bede6-152">Ayarlama devre dışı</span><span class="sxs-lookup"><span data-stu-id="bede6-152">Adjustment Out</span></span>

<span data-ttu-id="bede6-153">Neden kodları **Sayım günlüğü** türündeki sayım günlüklerindeki günlük satırlarına eklenir.</span><span class="sxs-lookup"><span data-stu-id="bede6-153">Reason codes are added to the journal lines in counting journals of the **Counting journal** type.</span></span>

1. <span data-ttu-id="bede6-154">**Stok Yönetimi** \> **Günlük girişleri** \> **Madde sayımı** \> **Sayım**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="bede6-154">Select **Inventory management** \> **Journal entries** \> **Item counting** \> **Counting**.</span></span>
2. <span data-ttu-id="bede6-155">Sayım günlüğü satır ayrıntılarında **Sayım neden kodu** alanında, bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="bede6-155">In the line details of the counting journal, in the **Counting reason code** field, select an option.</span></span>

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a><span data-ttu-id="bede6-156">Sayım geçmişini neden kodları tarafından kaydedildiği gibi görme</span><span class="sxs-lookup"><span data-stu-id="bede6-156">View the counting history as it's recorded by reason codes</span></span>

- <span data-ttu-id="bede6-157">**Stok yönetimi** \> **Sorgular ve raporlar** \> **Sayım geçmişi**'ni ve ardından **Sayım neden kodu** alanında bir neden kodu aracılığıyla kaydedilmiş olan sayım geçmişini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="bede6-157">Select **Inventory management** \> **Inquiries and reports** \> **Counting history**, and then, in the **Counting reason code** field, view the counting history that has been recorded through a reason code.</span></span>

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a><span data-ttu-id="bede6-158">Miktar ayarlaması için neden kodu kullanma</span><span class="sxs-lookup"><span data-stu-id="bede6-158">Use a reason code for a quantity adjustment</span></span>

1. <span data-ttu-id="bede6-159">**Eldeki stok** sayfasında **Miktarı ayarla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="bede6-159">On the **On-hand inventory** page, select **Adjust quantity**.</span></span> <span data-ttu-id="bede6-160">**Eldeki stok** sayfasını farklı yollarla açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bede6-160">You can open the **On-hand inventory** page in several ways.</span></span> <span data-ttu-id="bede6-161">Örneğin **Stok yönetimi** \> **Sorgular ve raporlar** \> **Eldeki stok**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="bede6-161">For example, select **Inventory management** \> **Inquiries and reports** \> **On-hand inventory**.</span></span>
2. <span data-ttu-id="bede6-162">**Miktarı ayarla**'yı ve daha sonra **Sayım neden kodu** alanından neden kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="bede6-162">Select **Adjust quantity**, and then, in the **Counting reason code** field, select a reason code.</span></span>

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a><span data-ttu-id="bede6-163">Mobil cihaz menü öğeleri için neden kodları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="bede6-163">Configure reason codes for mobile device menu items</span></span>

<span data-ttu-id="bede6-164">Bir mobil cihaz menü öğesinde herhangi bir sayım türü için neden kodları yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bede6-164">You can configure reason codes for any type of count on a mobile device menu item.</span></span> <span data-ttu-id="bede6-165">Mobil cihaz menü öğesi yapılandırması aşağıdaki bilgileri içerir:</span><span class="sxs-lookup"><span data-stu-id="bede6-165">The configuration of the mobile device menu item includes the following information:</span></span>

- <span data-ttu-id="bede6-166">Neden kodunun mobil cihaz çalışanına sayım sırasında gösterilip gösterilmeyeceği</span><span class="sxs-lookup"><span data-stu-id="bede6-166">Whether the reason code is shown to the mobile device worker during counting.</span></span>
- <span data-ttu-id="bede6-167">Mobil cihaz menü öğesinde gösterilen varsayılan neden kodu.</span><span class="sxs-lookup"><span data-stu-id="bede6-167">The default reason code that is shown on a mobile device menu item.</span></span>
- <span data-ttu-id="bede6-168">Kullanıcının neden kodunu düzenleyip düzenleyemeyeceği.</span><span class="sxs-lookup"><span data-stu-id="bede6-168">Whether the user can edit the reason code.</span></span>

### <a name="set-up-reason-codes-on-a-mobile-device"></a><span data-ttu-id="bede6-169">Mobil cihazda neden kodları ayarlama</span><span class="sxs-lookup"><span data-stu-id="bede6-169">Set up reason codes on a mobile device</span></span>

1. <span data-ttu-id="bede6-170">**Ambar yönetimi** \> **Kurulum** \> **Mobil cihaz** \> **Mobil cihaz menüsü öğeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="bede6-170">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="bede6-171">**Döngü sayısı** sekmesinde **Döngü sayımı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="bede6-171">On the **Cycle count** tab, select **Cycle counting**.</span></span>
3. <span data-ttu-id="bede6-172">**Varsayılan sayım neden kodu** alanında, sayım mobil cihaz menü öğesi kullanılarak yapıldığında kaydedilmesi gereken varsayılan neden kodunu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="bede6-172">In the **Default counting reason code** field, set the default reason code that should be recorded when counting is done by using the mobile device menu item.</span></span>
4. <span data-ttu-id="bede6-173">**Sayım neden kodunu görüntüle** alanında, her fark kaydedildikten sonra neden kodunun gösterilmesi için **Satır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bede6-173">In the **Display counting reason code** field, select **Line** to show the reason code after each variance is recorded.</span></span> <span data-ttu-id="bede6-174">Alternatif olarak, neden kodunun gösterilmemesi gerekiyorsa **Gizle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bede6-174">Alternatively, select **Hide** if the reason code shouldn't be shown.</span></span>
5. <span data-ttu-id="bede6-175">**Sayım neden kodunu düzenle** seçeneğini **Evet** veya **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="bede6-175">Set the **Edit counting reason code** option to either **Yes** or **No**.</span></span> <span data-ttu-id="bede6-176">Bu seçeneği **Evet** olarak ayarlarsanız, çalışan sayım sırasında mobil cihazda gösterildiğinde neden kodunu düzenleyebilir.</span><span class="sxs-lookup"><span data-stu-id="bede6-176">If you set this option to **Yes**, the worker can edit the reason code when it's shown on the mobile device during counting.</span></span>

> [!NOTE]
> <span data-ttu-id="bede6-177">**Döngü sayımı** düğmesi sayımın yapılabileceği herhangi bir mobil cihaz menüsünde etkinleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="bede6-177">The **Cycle counting** button can be enabled on any mobile device menu item where counting can be done.</span></span> <span data-ttu-id="bede6-178">Örnek nokta sayısı, kullanıcı yönlendirmeli iş ve sistem yönlendirmeli iş için menü öğelerini içerir.</span><span class="sxs-lookup"><span data-stu-id="bede6-178">Example include the menu items for spot counts, user-directed work, and system-directed work.</span></span>

## <a name="cycle-count-approvals"></a><span data-ttu-id="bede6-179">Döngü sayımı onayları</span><span class="sxs-lookup"><span data-stu-id="bede6-179">Cycle count approvals</span></span>

<span data-ttu-id="bede6-180">Bir sayım onaylanmadan önce kullanıcı sayımla ilişkili neden kodunu değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="bede6-180">Before a count is approved, the user can change the reason code that is associated with the count.</span></span> <span data-ttu-id="bede6-181">Sayım onaylandığında neden kodu sayım günlüğü satırlarına girilir.</span><span class="sxs-lookup"><span data-stu-id="bede6-181">When the count is approved, the reason code is entered on the counting journal lines.</span></span>

### <a name="modify-cycle-count-approvals"></a><span data-ttu-id="bede6-182">Döngü sayımı onaylarını değiştirme</span><span class="sxs-lookup"><span data-stu-id="bede6-182">Modify cycle count approvals</span></span>

1. <span data-ttu-id="bede6-183">**Ambar yönetimi** \> **Döngü sayımı** \> **İnceleme bekleyen döngü sayımı işi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="bede6-183">Select **Warehouse management** \> **Cycle counting** \> **Cycle count work pending review**.</span></span>
2. <span data-ttu-id="bede6-184">**Döngü sayımı**'nı seçin ve daha sonra **Neden kodu** alanından yeni bir neden kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="bede6-184">Select **Cycle counting**, and then, in the **Reason code** field, select a new reason code.</span></span>

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a><span data-ttu-id="bede6-185">Ayarlama etkin ve Ayarlama devre dışı için mobil cihaz menü öğesini değiştirme</span><span class="sxs-lookup"><span data-stu-id="bede6-185">Modify the mobile device menu item for Adjustment in and Adjustment out</span></span>

1. <span data-ttu-id="bede6-186">**Ambar yönetimi** \> **Kurulum** \> **Mobil cihaz** \> **Mobil cihaz menü öğeleri**'ni ve ardından **Ayarlama etkin ve devre dışı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="bede6-186">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**, and then select **Adjustment in and out**.</span></span>
2. <span data-ttu-id="bede6-187">**Mevcut işi kullan** seçeneğinde **Hayır**'ı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bede6-187">Set the **Use existing work** option to **No**.</span></span>
3. <span data-ttu-id="bede6-188">**İş oluşturma işlemi** alanında **Ayarlama etkin**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bede6-188">In the **Work creation process** field, select **Adjustment in**.</span></span>

<span data-ttu-id="bede6-189">İş oluşturma işlemi sırasında **Ayarlama etkin** veya **Ayarlama devre dışı** seçildiğinde aşağıdaki alanlar mobil cihaz menüsüne eklenir:</span><span class="sxs-lookup"><span data-stu-id="bede6-189">The following fields will be added to the mobile device menu item when **Adjustment in** or **Adjustment out** is selected during the work creation process:</span></span>

- <span data-ttu-id="bede6-190">Varsayılan sayım nedeni kodu</span><span class="sxs-lookup"><span data-stu-id="bede6-190">Default counting reason code</span></span>
- <span data-ttu-id="bede6-191">Sayım nedeni kodunu görüntüle</span><span class="sxs-lookup"><span data-stu-id="bede6-191">Display counting reason code</span></span>
- <span data-ttu-id="bede6-192">Sayım nedeni kodunu düzenle</span><span class="sxs-lookup"><span data-stu-id="bede6-192">Edit counting reason code</span></span>

