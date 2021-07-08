---
title: Stok yenileme yöntemleri ve miktar değişikliği
description: Bu konu, Planlamayı En İyi Duruma Getirme'deki stok yenileme yöntemleri hakkında bilgi sağlar. Ayrıca, bir ürün için birden çok sipariş miktarının sonucu nasıl etkilediğini açıklar.
author: crytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e0e671e624de2646a47647ef08d3567599b884
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261708"
---
# <a name="replenishment-methods-and-quantity-modification"></a><span data-ttu-id="241c9-104">Stok yenileme yöntemleri ve miktar değişikliği</span><span class="sxs-lookup"><span data-stu-id="241c9-104">Replenishment methods and quantity modification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="241c9-105">Bu konu, Planlamayı En İyi Duruma Getirme'deki stok yenileme yöntemleri hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="241c9-105">This topic provides information about replenishment methods in Planning Optimization.</span></span> <span data-ttu-id="241c9-106">Ayrıca, bir ürün için birden çok sipariş miktarının sonucu nasıl etkilediğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="241c9-106">It also explains how the multiple order quantity for a product affects the result.</span></span>

<span data-ttu-id="241c9-107">Stok yenileme yöntemleri, karşılama yöntemleri ve lot boyutlandırma yöntemleri olarak da bilinir.</span><span class="sxs-lookup"><span data-stu-id="241c9-107">Replenishment methods are also known as coverage methods and lot-sizing methods.</span></span>

## <a name="coverage-codes"></a><span data-ttu-id="241c9-108">Karşılama kodları</span><span class="sxs-lookup"><span data-stu-id="241c9-108">Coverage codes</span></span>

<span data-ttu-id="241c9-109">Planlamayı En İyi Duruma Getirme farklı stok yenileme yöntemleri kullanacak şekilde yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="241c9-109">Planning Optimization can be configured to use different replenishment methods.</span></span> <span data-ttu-id="241c9-110">Stok yenileme yöntemleri, sistemin bir ürünün gereksinimlerini hesaplamak için kullandığı tekniklerdir.</span><span class="sxs-lookup"><span data-stu-id="241c9-110">The replenishment methods are the techniques that the system uses to calculate requirements for a product.</span></span> <span data-ttu-id="241c9-111">Stok yenileme yöntemleri, karşılama grubunda veya üründe ayarlayabileceğiniz karşılama kodları tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="241c9-111">Replenishment methods are defined by coverage codes that you can set up on either the coverage group or the product.</span></span>

<span data-ttu-id="241c9-112">Planlamayı En İyi Duruma Getirme'de aşağıdaki karşılama kodları kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="241c9-112">The following coverage codes can be used in Planning Optimization:</span></span>

- <span data-ttu-id="241c9-113">**Dönem**: Ürün için bir döneme ait tüm talepleri tek bir siparişte olacak şekilde birleştiren stok karşılama yöntemi.</span><span class="sxs-lookup"><span data-stu-id="241c9-113">**Period** – The replenishment method combines all the demand for a period into one order for the product.</span></span> <span data-ttu-id="241c9-114">Sipariş dönemin ilk günü için planlanacaktır ve miktarı ayarlanan dönem içindeki net gereksinimleri karşılayacaktır.</span><span class="sxs-lookup"><span data-stu-id="241c9-114">The order will be planned for the first day of the period, and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="241c9-115">Dönem, ürüne yapılan ilk taleple başlar ve tanımlanan süreyi olduğu gibi kapsar.</span><span class="sxs-lookup"><span data-stu-id="241c9-115">The period starts with the first demand of the product and covers the defined length of time.</span></span> <span data-ttu-id="241c9-116">Sonraki dönem, ürünün sonraki gereksinimleri itibarıyla başlar.</span><span class="sxs-lookup"><span data-stu-id="241c9-116">The next period will start with the next requirements of the product.</span></span> <span data-ttu-id="241c9-117">*Dönem* karşılama kodu genellikle tahmin edilemeyen stok çekme, sezondan etkilenen ürünler veya yüksek maliyetli ürünler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="241c9-117">The *Period* coverage code is often used for non-predictable inventory draw, season-influenced products, or high-cost products.</span></span> <span data-ttu-id="241c9-118">Aşağıdaki şekilde bir örneği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="241c9-118">The following illustration shows an example.</span></span>

    <span data-ttu-id="241c9-119">![Dönem karşılama kodu kullanımı örneği](./media/coverage-code-period.png "Dönem karşılama kodu kullanımı örneği")</span><span class="sxs-lookup"><span data-stu-id="241c9-119">![Example of Period coverage code use](./media/coverage-code-period.png "Example of Period coverage code use")</span></span>

- <span data-ttu-id="241c9-120">**Gereksinim**: Sistemin ürün için her gereksinim başına bir planlı satınalma, transfer veya üretim emri oluşturduğu stok yenileme yöntemidir.</span><span class="sxs-lookup"><span data-stu-id="241c9-120">**Requirement** – In the replenishment method, the system creates a planned purchase, transfer, or production order per requirement for the product.</span></span> <span data-ttu-id="241c9-121">Bu yöntem, aralıklı talebi olan pahalı ürünler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="241c9-121">This method is used for expensive products that have intermittent demand.</span></span> <span data-ttu-id="241c9-122">*Gereksinim* karşılama kodu genellikle yapılandırılabilir ürünler veya siparişe göre üretim senaryoları için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="241c9-122">The *Requirement* coverage code is often used for configurable products or make-to-order scenarios.</span></span> <span data-ttu-id="241c9-123">Aşağıdaki şekilde bir örneği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="241c9-123">The following illustration shows an example.</span></span>

    <span data-ttu-id="241c9-124">![Gereksinim karşılama kodu kullanımı örneği](./media/coverage-code-requirement.png "Gereksinim karşılama kodu kullanımı örneği")</span><span class="sxs-lookup"><span data-stu-id="241c9-124">![Example of Requirement coverage code use](./media/coverage-code-requirement.png "Example of Requirement coverage code use")</span></span>

- <span data-ttu-id="241c9-125">**Minimum/Maksimum**</span><span class="sxs-lookup"><span data-stu-id="241c9-125">**Min./Max.**</span></span> <span data-ttu-id="241c9-126">– Stok yenileme yöntemi stok düzeyini temel alır.</span><span class="sxs-lookup"><span data-stu-id="241c9-126">– The replenishment method is based on the inventory level.</span></span> <span data-ttu-id="241c9-127">Tahmin edilen eldeki düzey belirli bir eşiğin altında olduğunda, stoğun belirli bir düzeye kadar yenilenmesini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="241c9-127">It defines the replenishment of inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span> <span data-ttu-id="241c9-128">Stok yenileme miktarı maksimum düzey ve eldeki tahmini düzey arasındaki fark olur.</span><span class="sxs-lookup"><span data-stu-id="241c9-128">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span> <span data-ttu-id="241c9-129">*Min./Maks.*</span><span class="sxs-lookup"><span data-stu-id="241c9-129">The *Min./Max.*</span></span> <span data-ttu-id="241c9-130">karşılama kodu genellikle öngörülebilir stok çekme, hızlı giden öğeler veya daha ucuz ürünler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="241c9-130">coverage code is often used for predictable inventory draw, high runners, or less expensive products.</span></span> <span data-ttu-id="241c9-131">Aşağıdaki şekilde bir örneği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="241c9-131">The following illustration shows an example.</span></span>

    <span data-ttu-id="241c9-132">![Min./Maks. karşılama kodu kullanımı örneği](./media/coverage-code-min-max.png "Min./Maks. karşılama kodu kullanımı örneği")</span><span class="sxs-lookup"><span data-stu-id="241c9-132">![Example of Min./Max. coverage code use](./media/coverage-code-min-max.png "Example of Min./Max. coverage code use")</span></span>

- <span data-ttu-id="241c9-133">**El ile**: Sistemin ürün için satın alma, transfer veya üretim emirleri önermediği stok yenileme yöntemi.</span><span class="sxs-lookup"><span data-stu-id="241c9-133">**Manual** – In the replenishment method, the system doesn't suggest purchase, transfer, or production orders for the product.</span></span> <span data-ttu-id="241c9-134">Bunun yerine, ürünün planlayıcısı, ürün stoğunun yenilenmesi için gerekli siparişleri oluşturmaktan sorumludur.</span><span class="sxs-lookup"><span data-stu-id="241c9-134">Instead, the planner for the product is responsible for creating the required orders for the replenishment of the product.</span></span> <span data-ttu-id="241c9-135">*Manuel* karşılama kodu genellikle sistem tarafından oluşturulan planlı siparişlerin istenmediği ürünler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="241c9-135">The *Manual* coverage code is often used for products that system-generated planned orders aren't wanted for.</span></span>

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a><span data-ttu-id="241c9-136">Sipariş miktarının ayarlarındaki sipariş miktarının etkisi</span><span class="sxs-lookup"><span data-stu-id="241c9-136">Impact of the order quantity from default order settings</span></span>

<span data-ttu-id="241c9-137">Serbest bırakılmış bir ürünün **Varsayılan sipariş ayarı** sayfasında, **Satınalma siparişi**, **Stok** ve **Satış siparişi** Hızlı Sekmelerinde aşağıdaki miktar ayarlarının her birini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="241c9-137">On the **Default order setting** page for a released product, you can specify each of following quantity settings on the **Purchase order**, **Inventory**, and **Sales order** FastTabs.</span></span> <span data-ttu-id="241c9-138">(**Stok** Hızlı Sekmesi hem transfer emirleri hem de üretim emirleri için kullanılır.)</span><span class="sxs-lookup"><span data-stu-id="241c9-138">(The **Inventory** FastTab is used for both transfer orders and production orders.)</span></span>

- <span data-ttu-id="241c9-139">**Çarpan**: Planlı siparişler bu miktarın katı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="241c9-139">**Multiple** – Planned orders will be a multiple of this quantity.</span></span>

    <span data-ttu-id="241c9-140">Örneğin, **Çarpan** alanı *5* olarak ayarlanmışsa, sipariş 5, 10, 15, 20 vb. bir miktar için olabilir.</span><span class="sxs-lookup"><span data-stu-id="241c9-140">For example, if the **Multiple** field is set to *5*, an order can be for a quantity of 5, 10, 15, 20, and so on.</span></span>

- <span data-ttu-id="241c9-141">**Minimum sipariş miktarı**: Planlı siparişler belirtilen değerden az olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="241c9-141">**Min. order quantity** – Planned orders won't be less than the specified value.</span></span>

    <span data-ttu-id="241c9-142">Örneğin, **Minimum sipariş miktarı** alanı *10* olarak ayarlanırsa, talebi karşılamak için yalnızca dört tane gerekli olsa bile, 10 adet için planlı bir sipariş oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="241c9-142">For example, if the **Min. order quantity** field is set to *10*, a planned order for a quantity of 10 will be created, even if only four are required to fulfill the demand.</span></span>

- <span data-ttu-id="241c9-143">**Maksimum sipariş miktarı**: Planlı siparişler belirtilen değeri aşamaz.</span><span class="sxs-lookup"><span data-stu-id="241c9-143">**Max. order quantity** – Planned orders won't exceed the specified value.</span></span> <span data-ttu-id="241c9-144">Talep **Maksimum sipariş miktarı** değerinden fazlaysa, bunu karşılamak için birden çok planlı sipariş oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="241c9-144">If the demand is more than the **Max. order quantity** value, multiple planned orders will be created to cover it.</span></span>

    <span data-ttu-id="241c9-145">Örneğin, **Maksimum sipariş miktarı** alanı *100* olarak ayarlanırsa ve talep 450 ise, 100 miktarı için dört planlı sipariş ve 50 miktarı için bir planlı sipariş oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="241c9-145">For example, if the **Max. order quantity** field is set to *100*, and the demand is 450, four planned orders for a quantity of 100 and one planned order for a quantity of 50 will be created.</span></span>

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a><span data-ttu-id="241c9-146">Min/Maks kullanan stok yenileme örnekleri</span><span class="sxs-lookup"><span data-stu-id="241c9-146">Examples of replenishment that use the Min./Max.</span></span> <span data-ttu-id="241c9-147">karşılama kodu</span><span class="sxs-lookup"><span data-stu-id="241c9-147">coverage code</span></span>

<span data-ttu-id="241c9-148">**Varsayılan sipariş ayarı** sayfasındaki bir ürün için **Çarpan** alanında bir değer belirtmezseniz ve *Min/Maks* stok yenileme yöntemi</span><span class="sxs-lookup"><span data-stu-id="241c9-148">If you don't specify a value in the **Multiple** field for a product on the **Default order setting** page, and if you're using the *Min./Max.*</span></span> <span data-ttu-id="241c9-149">kullanıyorsanız Planlamayı En İyi Duruma Getirme, tahmin edilen eldeki stok düzeyi belirli bir eşiğin altında olduğunda, stoğun belirli bir düzeye kadar yeniler.</span><span class="sxs-lookup"><span data-stu-id="241c9-149">replenishment method, Planning Optimization will replenish the inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span>

<span data-ttu-id="241c9-150">Bir ürün için çarpan miktarı tanımlarsanız, *Min./Maks.*</span><span class="sxs-lookup"><span data-stu-id="241c9-150">If you define a multiple quantity for a product, the *Min./Max.*</span></span> <span data-ttu-id="241c9-151">yenileme yöntemi davranışını değiştirir ve **Çarpan** değerini dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="241c9-151">replenishment method changes its behavior and considers the **Multiple** value.</span></span>

<span data-ttu-id="241c9-152">Başka bir deyişle, Planlamayı En İyi Duruma Getirme, tahmin edilen eldeki stok düzeyi tanımlanan minimum düzeyden daha az olduğunda stoğu tanımlanan maksimum düzeye kadar yenilemeye devam eder.</span><span class="sxs-lookup"><span data-stu-id="241c9-152">In other words, Planning Optimization will still replenish the inventory up to the defined maximum level when the predicted on-hand level is less than the defined minimum level.</span></span> <span data-ttu-id="241c9-153">Ancak, stok yenileme miktarı **Çarpan** değerinin katı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="241c9-153">However, the replenishment quantity must be a multiple of the **Multiple** value.</span></span>

<span data-ttu-id="241c9-154">Stok yenileme miktarı (maksimum düzey ile tahmin edilen eldeki stok düzeyi arasındaki fark) tanımlanan çarpan miktarının katı değilse, Planlamayı En İyi Duruma Getirme, tahmin edilen eldeki stok düzeyiyle birlikte en yüksek düzeyin altında olacak ilk olası değeri kullanır.</span><span class="sxs-lookup"><span data-stu-id="241c9-154">If the replenishment quantity (the difference between the maximum level and the predicted on-hand level) isn't a multiple of the defined multiple quantity, Planning Optimization uses the first possible value that, together with predicted on-hand level, will be below the maximum level.</span></span> <span data-ttu-id="241c9-155">Toplam minimum düzeyden küçükse, Planlamayı En İyi Duruma Getirme, tahmin edilen eldeki stokla birlikte maksimum düzeyin üzerinde olacak ilk değeri kullanır.</span><span class="sxs-lookup"><span data-stu-id="241c9-155">If the sum is less than the minimum level, Planning Optimization uses the first value that, together with predicted on-hand, will be above the maximum level.</span></span>

<span data-ttu-id="241c9-156">Aşağıdaki alt bölümler, bir ürün için çarpan miktarının *Min./Maks* stok yenileme yönteminin sonucunu nasıl etkilediğini</span><span class="sxs-lookup"><span data-stu-id="241c9-156">The following subsections provide some examples that show how the multiple order quantity for a product affects the result of the *Min./Max.*</span></span> <span data-ttu-id="241c9-157">gösteren bazı örnekler sağlar.</span><span class="sxs-lookup"><span data-stu-id="241c9-157">replenishment method.</span></span>

### <a name="example-1"></a><span data-ttu-id="241c9-158">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="241c9-158">Example 1</span></span>

<span data-ttu-id="241c9-159">Bir ürün aşağıdaki yapılandırmaya sahiptir:</span><span class="sxs-lookup"><span data-stu-id="241c9-159">A product has the following configuration:</span></span>

- <span data-ttu-id="241c9-160">**Karşılama kodu:** *Min./Maks.*</span><span class="sxs-lookup"><span data-stu-id="241c9-160">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="241c9-161">**Minimum:** *15*</span><span class="sxs-lookup"><span data-stu-id="241c9-161">**Minimum:** *15*</span></span>
- <span data-ttu-id="241c9-162">**Maksimum:** *22*</span><span class="sxs-lookup"><span data-stu-id="241c9-162">**Maximum:** *22*</span></span>
- <span data-ttu-id="241c9-163">**Çarpan:** *0*</span><span class="sxs-lookup"><span data-stu-id="241c9-163">**Multiple:** *0*</span></span>

<span data-ttu-id="241c9-164">Ürün için eldeki stok 10 adettir ve başka bir talep veya tedarik yoktur.</span><span class="sxs-lookup"><span data-stu-id="241c9-164">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="241c9-165">Master planlama çalıştırıldığında, stoğu maksimum miktara yenilemek için 12 parça için planlı bir sipariş oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="241c9-165">When master planning runs, a planned order for 12 pieces is created to replenish inventory to the maximum quantity.</span></span>

### <a name="example-2"></a><span data-ttu-id="241c9-166">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="241c9-166">Example 2</span></span>

<span data-ttu-id="241c9-167">Bir ürün aşağıdaki yapılandırmaya sahiptir:</span><span class="sxs-lookup"><span data-stu-id="241c9-167">A product has the following configuration:</span></span>

- <span data-ttu-id="241c9-168">**Karşılama kodu:** *Min./Maks.*</span><span class="sxs-lookup"><span data-stu-id="241c9-168">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="241c9-169">**Minimum:** *15*</span><span class="sxs-lookup"><span data-stu-id="241c9-169">**Minimum:** *15*</span></span>
- <span data-ttu-id="241c9-170">**Maksimum:** *22*</span><span class="sxs-lookup"><span data-stu-id="241c9-170">**Maximum:** *22*</span></span>
- <span data-ttu-id="241c9-171">**Çarpan:** *5*</span><span class="sxs-lookup"><span data-stu-id="241c9-171">**Multiple:** *5*</span></span>

<span data-ttu-id="241c9-172">Ürün için eldeki stok 10 adettir ve başka bir talep veya tedarik yoktur.</span><span class="sxs-lookup"><span data-stu-id="241c9-172">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="241c9-173">Master planlama çalıştırılğında, 10 adet için planlı bir sipariş oluşturulur (çünkü 15 adet stok yenileme artı 10 adet eldeki stok maksimum miktarı aşacaktır).</span><span class="sxs-lookup"><span data-stu-id="241c9-173">When master planning runs, a planned order for 10 pieces is created (because 15 pieces of replenishment plus 10 pieces of on-hand inventory will exceed the maximum quantity).</span></span>

### <a name="example-3"></a><span data-ttu-id="241c9-174">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="241c9-174">Example 3</span></span>

<span data-ttu-id="241c9-175">Bir ürün aşağıdaki yapılandırmaya sahiptir:</span><span class="sxs-lookup"><span data-stu-id="241c9-175">A product has the following configuration:</span></span>

- <span data-ttu-id="241c9-176">**Karşılama kodu:** *Min./Maks.*</span><span class="sxs-lookup"><span data-stu-id="241c9-176">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="241c9-177">**Minimum:** *21*</span><span class="sxs-lookup"><span data-stu-id="241c9-177">**Minimum:** *21*</span></span>
- <span data-ttu-id="241c9-178">**Maksimum:** *24*</span><span class="sxs-lookup"><span data-stu-id="241c9-178">**Maximum:** *24*</span></span>
- <span data-ttu-id="241c9-179">**Çarpan:** *5*</span><span class="sxs-lookup"><span data-stu-id="241c9-179">**Multiple:** *5*</span></span>

<span data-ttu-id="241c9-180">Ürün için eldeki stok 10 adettir ve başka bir talep veya tedarik yoktur.</span><span class="sxs-lookup"><span data-stu-id="241c9-180">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="241c9-181">Master planlama çalıştırılğında, 15 adet için planlı bir sipariş oluşturulur (çünkü 10 adet stok yenileme artı 10 adet eldeki minimum miktardan az olacaktır).</span><span class="sxs-lookup"><span data-stu-id="241c9-181">When master planning runs, the planned order for 15 pieces is created (because 10 pieces of replenishment plus 10 pieces of on-hand inventory will be less than the minimum quantity).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
