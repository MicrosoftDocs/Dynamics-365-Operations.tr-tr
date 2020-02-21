---
title: Dağıtılmış sipariş yönetimi (DOM) için maliyet yapılandırması
description: Bu konuda, Dynamics 365 Commerce'deki dağıtılmış sipariş yönetimi (DOM) işlevi için maliyet yapılandırması açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7644cb9800a418fd123b32a0257b787277fcb19f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004240"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a><span data-ttu-id="5cbc2-103">Dağıtılmış sipariş yönetimi (DOM) için maliyet yapılandırması</span><span class="sxs-lookup"><span data-stu-id="5cbc2-103">Cost configuration for distributed order management (DOM)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5cbc2-104">Kuruluşlar, bir siparişin karşılanması gereken en iyi konumu belirlemek için birden fazla maliyet bileşenini dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-104">Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</span></span> <span data-ttu-id="5cbc2-105">Bu maliyet bileşenlerinden bazıları sevkiyat maliyeti, işleme maliyeti ve ambalaj maliyetidir.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-105">Some of these cost components are shipping cost, handling cost, and packaging cost.</span></span> <span data-ttu-id="5cbc2-106">Bu maliyetlerin birleşimi, karşılama konumunun belirlenmesi için hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-106">A combination of these costs is calculated to determine the fulfillment location.</span></span>

<span data-ttu-id="5cbc2-107">Dynamics 365 Commerce'de dağıtılmış sipariş yönetiminin (DOM) ilk yinelemesi siparişleri karşılama konumlarına atamayı en iyi duruma getirdiğinde, yalnızca mesafe dikkate alınıyordu.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-107">When the first iteration of distributed order management (DOM) in Dynamics 365 Commerce optimized the assignment of orders to fulfillment locations, it factored in distance only.</span></span> <span data-ttu-id="5cbc2-108">Mesafe maliyet ile ilişkili olabilmesine karşın maliyetle aynı değildir.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-108">Although distance can be correlated with cost, it isn't the same as cost.</span></span> <span data-ttu-id="5cbc2-109">Örneğin, gece sevkiyatı yöntemi aynı mesafeye yapılan üç günlük veya yedi günlük sevkiyattan daha maliyetlidir.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-109">For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</span></span>

<span data-ttu-id="5cbc2-110">Maliyet yapılandırması özelliği, perakendecilerin sipariş satırlarını karşılamak için en uygun konumu belirlemek üzere hesaplanacak ve dikkate alınacak ek maliyet bileşenlerini tanımlamasına ve yapılandırmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-110">The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</span></span>

<span data-ttu-id="5cbc2-111">Maliyet bileşenleri yapılandırıldığında DOM çözücü siparişi karşılamak üzere en uygun konumu belirlemek için bu maliyet tanımlarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-111">When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</span></span> <span data-ttu-id="5cbc2-112">Mesafe bileşenini maliyet olarak dikkate almaz.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-112">It doesn't consider the distance component as a cost.</span></span> <span data-ttu-id="5cbc2-113">Bununla birlikte, bileşenler yapılandırılmazsa DOM çözücü siparişi karşılamak üzere en uygun konumu belirlemek için mesafe bileşenini maliyet olarak kullanır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-113">However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</span></span>

## <a name="set-up-cost-components"></a><span data-ttu-id="5cbc2-114">Maliyet bileşenlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="5cbc2-114">Set up cost components</span></span>

<span data-ttu-id="5cbc2-115">Sistemde iki ana maliyet bileşeni türü tanımlanabilir: **Sevkiyat** ve **Diğer**.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-115">Two major cost component types can be defined in the system: **Shipping** and **Other**.</span></span>

<span data-ttu-id="5cbc2-116">Her iki maliyet bileşeni türü de aşağıdaki tabloda gösterildiği gibi çoklu hesaplama esaslarını destekler.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-116">Both cost component types support multiple calculation bases, as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5cbc2-117">Maliyet bileşeni türü</span><span class="sxs-lookup"><span data-stu-id="5cbc2-117">Cost component type</span></span></th>
<th><span data-ttu-id="5cbc2-118">Hesaplama esası</span><span class="sxs-lookup"><span data-stu-id="5cbc2-118">Calculation basis</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5cbc2-119">Sevkiyat</span><span class="sxs-lookup"><span data-stu-id="5cbc2-119">Shipping</span></span></td>
<td>
<ul>
<li><span data-ttu-id="5cbc2-120">Basit</span><span class="sxs-lookup"><span data-stu-id="5cbc2-120">Simple</span></span></li>
<li><span data-ttu-id="5cbc2-121">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="5cbc2-121">Tiered</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="5cbc2-122">Diğer</span><span class="sxs-lookup"><span data-stu-id="5cbc2-122">Other</span></span></td>
<td>
<ul>
<li><span data-ttu-id="5cbc2-123">Satış siparişi</span><span class="sxs-lookup"><span data-stu-id="5cbc2-123">Sales order</span></span></li>
<li><span data-ttu-id="5cbc2-124">Satış satırı</span><span class="sxs-lookup"><span data-stu-id="5cbc2-124">Sales line</span></span></li>
<li><span data-ttu-id="5cbc2-125">Konum</span><span class="sxs-lookup"><span data-stu-id="5cbc2-125">Location</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a><span data-ttu-id="5cbc2-126">Sevkiyat maliyeti bileşeni türü</span><span class="sxs-lookup"><span data-stu-id="5cbc2-126">Shipping cost component type</span></span>

<span data-ttu-id="5cbc2-127">Bu bölümde, **Sevkiyat** maliyeti bileşeni türü ve sevkiyat maliyetleri için hesaplama esası birleşiminin nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-127">This section explains how to set up each combination of the **Shipping** cost component type and a calculation basis for shipping costs.</span></span> <span data-ttu-id="5cbc2-128">Ayrıca, DOM çözücünün her bir birleşimi nasıl kullandığı da açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-128">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a><span data-ttu-id="5cbc2-129">Maliyet bileşeni türü = Sevkiyat ve Hesaplama esası = Basit</span><span class="sxs-lookup"><span data-stu-id="5cbc2-129">Cost component type = Shipping and Calculation basis = Simple</span></span>

<span data-ttu-id="5cbc2-130">**Sevkiyat** maliyeti bileşeni türü ve **Basit** hesaplama esası birlikte kullanılırsa bir teslimat şekline ait sevkiyat maliyeti, sabit maliyeti veya mesafeyi temel alır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-130">If a combination of the **Shipping** cost component type and the **Simple** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span>

<span data-ttu-id="5cbc2-131">Bu birleşim için aşağıdaki alanları ayarlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="5cbc2-131">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="5cbc2-132">**Maliyet faktörü**: Maliyet faktörü için benzersiz bir tanımlayıcı girin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-132">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="5cbc2-133">**Açıklama**: Maliyet faktörünün adını ve açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-133">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="5cbc2-134">**Başlangıç tarihi** ve **Bitiş tarihi**: Bu alanları, maliyet faktörünü belirli bir tarih aralığı için sınırlandırmak amacıyla kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-134">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="5cbc2-135">Bu alanları boş bırakırsanız maliyet faktörü belirsiz bir dönem için geçerli olur.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-135">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="5cbc2-136">**Etkin**: Maliyet faktörünün etkin olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-136">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="5cbc2-137">DOM yalnızca karşılama profiliyle ilişkili olan etkin maliyet faktörlerini dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-137">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="5cbc2-138">**Şirket**: Maliyet faktörünün yapılandırıldığı tüzel kişiliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-138">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="5cbc2-139">Hesaplama ölçütlerinin tüm satırları aynı tüzel kişilik için olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-139">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="5cbc2-140">**Teslimat şekilleri**: Maliyetin yapılandırıldığı teslimat şekillerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-140">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="5cbc2-141">**Hesaplama türü**: Maliyetin belirli bir teslimat şekli için nasıl hesaplanacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-141">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery.</span></span> <span data-ttu-id="5cbc2-142">İki hesaplama türü desteklenir:</span><span class="sxs-lookup"><span data-stu-id="5cbc2-142">Two calculation types are supported:</span></span>

    - <span data-ttu-id="5cbc2-143">**Sabit**: Teslimat şekli olarak düz maliyet kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-143">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="5cbc2-144">Bu hesaplama türünü seçerseniz **Maliyet** alanı düz maliyeti tanımlar.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-144">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="5cbc2-145">**Mesafe başına birim**: Teslimat şeklinin maliyeti, **Maliyet** alanında belirtilen maliyet değeri ile teslimat adresi ve konumlar arasındaki mesafe çarpılarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-145">**Per-distance unit** – The cost for the mode of delivery is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="5cbc2-146">**Maliyet**: Teslimat şeklinin maliyetini hesaplamak için **Hesaplama türü** alanıyla birlikte kullanılan maliyet değerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-146">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a><span data-ttu-id="5cbc2-147">Maliyet bileşeni türü = Sevkiyat ve Hesaplama esası = Katmanlı</span><span class="sxs-lookup"><span data-stu-id="5cbc2-147">Cost component type = Shipping and Calculation basis = Tiered</span></span>

<span data-ttu-id="5cbc2-148">**Sevkiyat** maliyeti bileşeni türü ve **Katmanlı** hesaplama esası birlikte kullanılırsa bir teslimat şekline ait sevkiyat maliyeti, sabit maliyeti veya mesafeyi temel alır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-148">If a combination of the **Shipping** cost component type and the **Tiered** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span> <span data-ttu-id="5cbc2-149">Ancak bu birleşimde, mesafe katmanlı bir mesafe aralığını temel alır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-149">However, in this combination, the distance is based on a tiered range of distances.</span></span>

<span data-ttu-id="5cbc2-150">Bu birleşim için aşağıdaki alanları ayarlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="5cbc2-150">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="5cbc2-151">**Maliyet faktörü**: Maliyet faktörü için benzersiz bir tanımlayıcı girin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-151">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="5cbc2-152">**Açıklama**: Maliyet faktörünün adını ve açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-152">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="5cbc2-153">**Varsayılan maliyet**: Teslimat adresi ile konum arasındaki mesafe teslimat şekline ilişkin katmanlı mesafelerden herhangi birine denk düşmezse, teslimat şekli için kullanılacak maliyeti belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-153">**Default cost** – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</span></span>
- <span data-ttu-id="5cbc2-154">**Başlangıç tarihi** ve **Bitiş tarihi**: Bu alanları, maliyet faktörünü belirli bir tarih aralığı için sınırlandırmak amacıyla kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-154">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="5cbc2-155">Bu alanları boş bırakırsanız maliyet faktörü belirsiz bir dönem için geçerli olur.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-155">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="5cbc2-156">**Etkin**: Maliyet faktörünün etkin olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-156">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="5cbc2-157">DOM yalnızca karşılama profiliyle ilişkili olan etkin maliyet faktörlerini dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-157">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="5cbc2-158">**Şirket**: Maliyet faktörünün yapılandırıldığı tüzel kişiliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-158">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="5cbc2-159">Hesaplama ölçütlerinin tüm satırları aynı tüzel kişilik için olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-159">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="5cbc2-160">**Teslimat şekilleri**: Maliyetin yapılandırıldığı teslimat şekillerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-160">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="5cbc2-161">**Mesafe türü**: Katmanlı mesafe tanımının bir havayolu mesafesi mi yoksa karayolu mesafesi mi olduğunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-161">**Distance type** – Specify whether the tiered distance definition is an aerial distance or a road distance.</span></span>
- <span data-ttu-id="5cbc2-162">**Mesafe birimleri**: Katmanlı mesafenin ölçüldüğü birimi belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-162">**Distance units** – Specify the unit that the tiered distance is measured in.</span></span>
- <span data-ttu-id="5cbc2-163">**Başlangıçtan mesafe**: Katmanlı mesafe için başlangıç aralığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-163">**Distance from** – Specify the start range for the tiered distance.</span></span>
- <span data-ttu-id="5cbc2-164">**Bitişe mesafe**: Katmanlı mesafe için bitiş aralığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-164">**Distance to** – Specify the end range for the tiered distance.</span></span>
- <span data-ttu-id="5cbc2-165">**Hesaplama türü**: Maliyetin belirli bir teslimat şekli ve katmanlı mesafe için nasıl hesaplanacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-165">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</span></span> <span data-ttu-id="5cbc2-166">İki hesaplama türü desteklenir:</span><span class="sxs-lookup"><span data-stu-id="5cbc2-166">Two calculation types are supported:</span></span>

    - <span data-ttu-id="5cbc2-167">**Sabit**: Teslimat şekli olarak düz maliyet kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-167">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="5cbc2-168">Bu hesaplama türünü seçerseniz **Maliyet** alanı düz maliyeti tanımlar.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-168">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="5cbc2-169">**Mesafe başına birim**: Teslimat şeklinin ve katmanlı mesafenin maliyeti, **Maliyet** alanında belirtilen maliyet değeri ile teslimat adresi ve konumlar arasındaki mesafe çarpılarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-169">**Per distance unit** – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="5cbc2-170">**Maliyet**: Teslimat şeklinin maliyetini hesaplamak için **Hesaplama türü** alanıyla birlikte kullanılan maliyet değerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-170">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

> [!NOTE]
> - <span data-ttu-id="5cbc2-171">Katmanlı mesafeler tanımladığınızda, sistem eksik veya çakışan mesafeler olmadığını doğrular.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-171">When you define tiered distances, the system validates that there are no missing or overlapping distances.</span></span>
> - <span data-ttu-id="5cbc2-172">Bir teslimat şekli için kullanılan mesafe türü, tüm katmanlı mesafelerde aynı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-172">The distance type that is used for a mode of delivery must be the same across all the tiered distances.</span></span>

### <a name="other-cost-component-type"></a><span data-ttu-id="5cbc2-173">Diğer maliyet bileşeni türü</span><span class="sxs-lookup"><span data-stu-id="5cbc2-173">Other cost component type</span></span>

<span data-ttu-id="5cbc2-174">Bu bölümde, **Diğer** maliyeti bileşeni türü ve sevkiyat dışı maliyetler için diğer maliyet türü birleşiminin nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-174">This section explains how to set up each combination of the **Other** cost component type and an other cost type for non-shipping costs.</span></span> <span data-ttu-id="5cbc2-175">Ayrıca, DOM çözücünün her bir birleşimi nasıl kullandığı da açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-175">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a><span data-ttu-id="5cbc2-176">Maliyet bileşeni türü = Diğer ve Diğer maliyet türü = Satış siparişi</span><span class="sxs-lookup"><span data-stu-id="5cbc2-176">Cost component type = Other and Other cost type = Sales order</span></span>

<span data-ttu-id="5cbc2-177">**Diğer** maliyet bileşeni türü ile **Satış siparişi** diğer maliyet türü satış siparişi düzeyindeki sevkiyat dışı maliyetlerin tanımlanması için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-177">A combination of the **Other** cost component type and the **Sales order** other cost type is used to define non-shipping costs at the sales order level.</span></span>

<span data-ttu-id="5cbc2-178">Bu birleşim için aşağıdaki alanları ayarlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="5cbc2-178">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="5cbc2-179">**Maliyet faktörü**: Maliyet faktörü için benzersiz bir tanımlayıcı girin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-179">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="5cbc2-180">**Açıklama**: Maliyet faktörünün adını ve açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-180">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="5cbc2-181">**Başlangıç tarihi** ve **Bitiş tarihi**: Bu alanları, maliyet faktörünü belirli bir tarih aralığı için sınırlandırmak amacıyla kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-181">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="5cbc2-182">Bu alanları boş bırakırsanız maliyet faktörü belirsiz bir dönem için geçerli olur.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-182">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="5cbc2-183">**Etkin**: Maliyet faktörünün etkin olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-183">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="5cbc2-184">DOM yalnızca karşılama profiliyle ilişkili olan etkin maliyet faktörlerini dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-184">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="5cbc2-185">**Maliyet**: Satış siparişi düzeyinde sevkiyat dışı bir maliyetin maliyet değerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-185">**Cost** – Specify the cost value for a non-shipping cost at the sales order level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a><span data-ttu-id="5cbc2-186">Maliyet bileşeni türü = Diğer ve Diğer maliyet türü = Satış satırı</span><span class="sxs-lookup"><span data-stu-id="5cbc2-186">Cost component type = Other and Other cost type = Sales line</span></span>

<span data-ttu-id="5cbc2-187">**Diğer** maliyet bileşeni türü ile **Satış satırı** diğer maliyet türü satış satırı düzeyindeki sevkiyat dışı maliyetlerin tanımlanması için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-187">A combination of the **Other** cost component type and the **Sales line** other cost type is used to define non-shipping costs at the sales order line level.</span></span>

<span data-ttu-id="5cbc2-188">Bu birleşim için aşağıdaki alanları ayarlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="5cbc2-188">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="5cbc2-189">**Maliyet faktörü**: Maliyet faktörü için benzersiz bir tanımlayıcı girin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-189">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="5cbc2-190">**Açıklama**: Maliyet faktörünün adını ve açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-190">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="5cbc2-191">**Başlangıç tarihi** ve **Bitiş tarihi**: Bu alanları, maliyet faktörünü belirli bir tarih aralığı için sınırlandırmak amacıyla kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-191">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="5cbc2-192">Bu alanları boş bırakırsanız maliyet faktörü belirsiz bir dönem için geçerli olur.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-192">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="5cbc2-193">**Etkin**: Maliyet faktörünün etkin olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-193">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="5cbc2-194">DOM yalnızca karşılama profiliyle ilişkili olan etkin maliyet faktörlerini dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-194">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="5cbc2-195">**Maliyet**: Satış satırı düzeyinde sevkiyat dışı bir maliyetin maliyet değerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-195">**Cost** – Specify the cost value for a non-shipping cost at the sales order line level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--location"></a><span data-ttu-id="5cbc2-196">Maliyet bileşeni türü = Diğer ve Diğer maliyet türü = Konum</span><span class="sxs-lookup"><span data-stu-id="5cbc2-196">Cost component type = Other and Other cost type = Location</span></span>

<span data-ttu-id="5cbc2-197">**Diğer** maliyet bileşeni türü ile **Konum** diğer maliyet türünün birleşimi, bir konum grubu veya tek bir konum için sevkiyat dışı maliyetleri tanımlamak amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-197">A combination of the **Other** cost component type and the **Location** other cost type is used to define non-shipping costs for a group of locations or an individual location.</span></span>

<span data-ttu-id="5cbc2-198">Bu birleşim için aşağıdaki alanları ayarlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="5cbc2-198">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="5cbc2-199">**Maliyet faktörü**: Maliyet faktörü için benzersiz bir tanımlayıcı girin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-199">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="5cbc2-200">**Açıklama**: Maliyet faktörünün adını ve açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-200">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="5cbc2-201">**Başlangıç tarihi** ve **Bitiş tarihi**: Bu alanları, maliyet faktörünü belirli bir tarih aralığı için sınırlandırmak amacıyla kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-201">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="5cbc2-202">Bu alanları boş bırakırsanız maliyet faktörü belirsiz bir dönem için geçerli olur.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-202">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="5cbc2-203">**Etkin**: Maliyet faktörünün etkin olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-203">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="5cbc2-204">DOM yalnızca karşılama profiliyle ilişkili olan etkin maliyet faktörlerini dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-204">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="5cbc2-205">**Karşılama grubu**: Sevkiyat dışı maliyetin tanımlandığı konum gruplarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-205">**Fulfillment group** – Specify the group of locations that the non-shipping cost is defined for.</span></span>
- <span data-ttu-id="5cbc2-206">**Karşılama konumu**: Sevkiyat dışı maliyetin tanımlandığı konumu belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-206">**Fulfillment location** – Specify the location that the non-shipping cost is defined for.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5cbc2-207">Konum tabanlı hesaplama ölçütleri için aynı satırda bir karşılama grubu ve karşılama konumu belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-207">You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</span></span>

- <span data-ttu-id="5cbc2-208">**Maliyet**: Karşılama grubu düzeyi veya karşılama konumu düzeyinde sevkiyat dışı maliyetin maliyet değerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-208">**Cost** – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5cbc2-209">DOM'ın çalıştırıldığında bu maliyetleri dikkate alması için maliyet faktörünü ilgili karşılama profiline eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5cbc2-209">For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</span></span>
