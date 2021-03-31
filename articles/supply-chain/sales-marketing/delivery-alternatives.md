---
title: Teslimat alternatifleri
description: Satış siparişi alanlar, Teslimat alternatif sayfasını, alternatif sipariş karşılama seçeneklerini bulmak için kullanabilirler.
author: ChristianRytt
manager: tfehr
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 783307ea5cc764f4a04d069dfd7d614a4f63dd2d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229267"
---
# <a name="delivery-alternatives"></a><span data-ttu-id="64905-103">Teslimat alternatifleri</span><span class="sxs-lookup"><span data-stu-id="64905-103">Delivery alternatives</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64905-104">Satış siparişi alanlar, **Teslimat alternatifleri** sayfasını, alternatif sipariş karşılama seçeneklerini bulmak için kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="64905-104">Sales order takers can use the **Delivery alternatives** page to discover alternative order fulfillment options.</span></span>

<span data-ttu-id="64905-105">**Teslimat alternatifleri** sayfasının düzeni, tüm alternatif seçenekler hakkında genel bir görünüm verir.</span><span class="sxs-lookup"><span data-stu-id="64905-105">The **Delivery alternatives** page layout gives an overview of all alternative options.</span></span> <span data-ttu-id="64905-106">Ayrıca sipariş alanların, geçerli şirketin karşılama fırsatlarının ötesine bakmalarına izin verir.</span><span class="sxs-lookup"><span data-stu-id="64905-106">It also lets order takers look beyond the current company for fulfillment opportunities.</span></span> <span data-ttu-id="64905-107">Şimdi hem şirketlerarası fırsatlar hem de harici satıcılardan fırsatları görebilirler.</span><span class="sxs-lookup"><span data-stu-id="64905-107">They can now view both intercompany opportunities and opportunities from external vendors.</span></span> <span data-ttu-id="64905-108">Seçenekleri teslimat tarihine göre dizerek, satış siparişi alanlar teslimat alternatiflerinin akıllı bir listesini görebilirler.</span><span class="sxs-lookup"><span data-stu-id="64905-108">By sorting the options by delivery date, sales order takers can view an intelligent list of delivery alternatives.</span></span> <span data-ttu-id="64905-109">Ek olarak, parametreler önerilen teslimatları daha iyi yönetmelerine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="64905-109">In addition, parameters help them better manage the suggested deliveries.</span></span> <span data-ttu-id="64905-110">Taşıma süresi teslimat tarihini etkileyebileceğinden, satış siparişi alanlar, taşıyıcının sunduğu çeşitli taşıma seçeneklerini keşfedebilirler.</span><span class="sxs-lookup"><span data-stu-id="64905-110">Because transport time can affect delivery dates, sales order takers can explore the various transportation choices that carriers offer.</span></span> <span data-ttu-id="64905-111">Her bir öneri için ayrıntılı bilgi sunulduğundan, sipariş alanlar **Teslimat alternatifleri** sayfasından doğrudan bilinçli kararlar verebilirler.</span><span class="sxs-lookup"><span data-stu-id="64905-111">Because detailed information is shown for each suggestion, order takers can make informed decisions directly from the **Delivery alternatives** page.</span></span>

## <a name="open-the-delivery-alternatives-page"></a><span data-ttu-id="64905-112">Teslimat alternatifleri sayfasını aç</span><span class="sxs-lookup"><span data-stu-id="64905-112">Open the Delivery alternatives page</span></span>

<span data-ttu-id="64905-113">**Teslimat alternatifleri** sayfasını satış siparişi satırından açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64905-113">You can open the **Delivery alternatives** page from the sales order line.</span></span>

1. <span data-ttu-id="64905-114">**Ürün ve tedarik \> Teslimat alternatifleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="64905-114">Select **Products and supply \> Delivery alternatives**.</span></span>
1. <span data-ttu-id="64905-115">**Satır ayrıntıları \> Teslimat \> Teslimat alternatifleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="64905-115">Select **Line details \> Delivery \> Delivery alternatives.**</span></span>

<span data-ttu-id="64905-116">**Teslimat alternatifleri** sayfasını, **Satış siparişi işleme ve sorgu** çalışma alanını açarak ve sonra **Siparişler ve sık kullanılanlar \> Ertelenen sipariş satırları \> Teslimat alternatifleri**'ni seçerek de açabilirsiniz. **Not**: **Teslimat alternatifleri** sayfasını, yalnızca aşağıdaki koşullar yerine getiriliyorsa açabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="64905-116">You can also open the **Delivery alternatives** page by opening the **Sales order processing and inquiry** workspace, and then selecting **Orders and favorites \> Delayed order lines \> Delivery alternatives** **Note:** You can open the **Delivery alternatives** page only if both the following conditions are met:</span></span>

- <span data-ttu-id="64905-117">Tüm zorunlu satış satır bilgileri girilmiştir.</span><span class="sxs-lookup"><span data-stu-id="64905-117">All mandatory sales line information is filled in.</span></span>
- <span data-ttu-id="64905-118">**Teslimat tarih denetimi** alanı, **Yok**'tan başka bir değere ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="64905-118">The **Delivery date control** field is set to a value other than **None**.</span></span>

## <a name="delivery-date-control-methods"></a><span data-ttu-id="64905-119">Teslimat tarihi kontrol yöntemleri</span><span class="sxs-lookup"><span data-stu-id="64905-119">Delivery date control methods</span></span>

<span data-ttu-id="64905-120">Teslimat tarihi denetim yöntemi, sistemin teslimat tarihlerini nasıl oluşturduğunu, teslimat alternatiflerinin nasıl hesaplandığını ve hangi bilginin gösterildiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="64905-120">The delivery date control method determines how the system establishes delivery dates, how delivery alternatives are calculated, and what information is shown.</span></span> <span data-ttu-id="64905-121">Teslimat tarihi denetiminin takvimleri dikkate aldığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="64905-121">Note that delivery date control takes calendars into consideration.</span></span> <span data-ttu-id="64905-122">Bu nedenle, aşağıdaki takvimler önerilen giriş tarihini etkileyebilir: Ambar takvimi, Taşıma takvimi, Satıcı takvimi ve Müşteri takvimi.</span><span class="sxs-lookup"><span data-stu-id="64905-122">Therefore, the following calendars can affect the suggested receipt date: Warehouse calendar, Transport calendar, Vendor calendar, and Customer calendar.</span></span> <span data-ttu-id="64905-123">Aşağıdaki tablo teslimat tarihi denetimi için her bir yöntemi açıklar.</span><span class="sxs-lookup"><span data-stu-id="64905-123">The following table describes each method for delivery date control.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64905-124"><strong>Yöntem</strong></span><span class="sxs-lookup"><span data-stu-id="64905-124"><strong>Method</strong></span></span></td>
<td><span data-ttu-id="64905-125"><strong>Açıklama</strong></span><span class="sxs-lookup"><span data-stu-id="64905-125"><strong>Description</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64905-126"><strong>Hiçbiri</strong></span><span class="sxs-lookup"><span data-stu-id="64905-126"><strong>None</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="64905-127">Satış satırları için teslimat alternatifleri desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="64905-127">Delivery alternatives for sales lines aren't supported.</span></span> <span data-ttu-id="64905-128">Bu seçenek teslimat tarihi denetimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="64905-128">This option turns off delivery date control.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64905-129"><strong>Satış sağlama süresi</strong></span><span class="sxs-lookup"><span data-stu-id="64905-129"><strong>Sales lead time</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="64905-130">Teslimat alternatifleri önceden tanımlanmış satış sağlama süresinde hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="64905-130">Delivery alternatives are calculated based on the predefined sales lead time.</span></span> <span data-ttu-id="64905-131">Taşıma günleri, teslimat şekline dayanarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="64905-131">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="64905-132">Teslimat alternatifleri, eldeki stoka sahip ambarları ve arz/talep siparişlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="64905-132">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64905-133"><strong>KM</strong></span><span class="sxs-lookup"><span data-stu-id="64905-133"><strong>ATP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="64905-134">Teslimat alternatifleri, karşılanabilir miktar (KM) mantığına göre hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="64905-134">Delivery alternatives are calculated based on available to promise (ATP) logic.</span></span> <span data-ttu-id="64905-135">Geçerli kullanılabilirlik ve beklenen gelecek kullanılabilirlik dikkate alınır.</span><span class="sxs-lookup"><span data-stu-id="64905-135">The current availability and expected future availability are considered.</span></span> <span data-ttu-id="64905-136">Taşıma günleri, teslimat şekline dayanarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="64905-136">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="64905-137">Teslimat alternatifleri, eldeki stoka sahip ambarları ve arz/talep siparişlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="64905-137">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64905-138"><strong>KM + Çıkış marjı</strong></span><span class="sxs-lookup"><span data-stu-id="64905-138"><strong>ATP + Issue margin</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="64905-139">Teslimat alternatifleri KM yönteminde olduğu gibi hesaplanır ancak çıkış marjı hesaplamaya dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="64905-139">Delivery alternatives are calculated as for the ATP method, but the issue margin is included in the calculation.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64905-140"><strong>TEM</strong></span><span class="sxs-lookup"><span data-stu-id="64905-140"><strong>CTP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="64905-141">Teslimat alternatifleri, teslim edilebilir miktar (TEM) mantığına göre hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="64905-141">Delivery alternatives are calculated based on the capable to promise (CTP) logic.</span></span> <span data-ttu-id="64905-142">MRP açılımı kullanılabilirliği belirlemek üzere kullanılır.</span><span class="sxs-lookup"><span data-stu-id="64905-142">MRP explosion is used to determine availability.</span></span> <span data-ttu-id="64905-143">En azından TEM mahsup işlemi teslimat tarihlerini satış sağlama süresine unutmayın.</span><span class="sxs-lookup"><span data-stu-id="64905-143">Note that, at a minimum, CTP offsets delivery dates to the sales lead time.</span></span> <span data-ttu-id="64905-144">Taşıma günleri, teslimat şekline dayanarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="64905-144">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="64905-145">Teslimat alternatifleri aşağıdaki ambarlar için önerileri içerir:</span><span class="sxs-lookup"><span data-stu-id="64905-145">Delivery alternatives include suggestions for the following warehouses:</span></span>
<ul>
<li><span data-ttu-id="64905-146">Geçerli ambar</span><span class="sxs-lookup"><span data-stu-id="64905-146">Current warehouse</span></span></li>
<li><span data-ttu-id="64905-147">Varsayılan ambar</span><span class="sxs-lookup"><span data-stu-id="64905-147">Default warehouse</span></span></li>
<li><span data-ttu-id="64905-148">Elde stok bulunduran tüm ambarlar</span><span class="sxs-lookup"><span data-stu-id="64905-148">All warehouses that have available on-hand inventory</span></span></li>
<li><span data-ttu-id="64905-149">Tedarik emirleri olan tüm ambarlar</span><span class="sxs-lookup"><span data-stu-id="64905-149">All warehouses that have supply orders</span></span></li>
<li><span data-ttu-id="64905-150">Etkin ürün reçetesi (BOM) sürümlerine sahip tüm ambarlar</span><span class="sxs-lookup"><span data-stu-id="64905-150">All warehouses that have active bill of materials (BOM) versions</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a><span data-ttu-id="64905-151">Teslimat alternatifleri hakkında bilgi görüntüle</span><span class="sxs-lookup"><span data-stu-id="64905-151">View information about delivery alternatives</span></span>

<span data-ttu-id="64905-152">Bu bölüm, **Teslimat alternatifleri** sayfasının her hızlı sekmesinde bulunan teslimat alternatifleri hakkında bilgileri açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="64905-152">This section describes the information about delivery alternatives that is available on each FastTab of the **Delivery alternatives** page.</span></span>

### <a name="the-product-fasttab"></a><span data-ttu-id="64905-153">Ürün hızlı sekmesi</span><span class="sxs-lookup"><span data-stu-id="64905-153">The Product FastTab</span></span>

<span data-ttu-id="64905-154">Bu hızlı sekme, geçerli satış satırının ürün ve ayrıntılarının bir özetini gösterir.</span><span class="sxs-lookup"><span data-stu-id="64905-154">This FastTab shows a summary of the product and details of the current sales line.</span></span>

### <a name="the-delivery-alternatives-fasttab"></a><span data-ttu-id="64905-155">Teslimat alternatifleri hızlı sekmesi</span><span class="sxs-lookup"><span data-stu-id="64905-155">The Delivery alternatives FastTab</span></span>

<span data-ttu-id="64905-156">Bu hızlı sekme, giriş tarihine göre sıralanan teslimat alternatiflerinin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="64905-156">This FastTab shows a list of delivery alternatives that is sorted by receipt date.</span></span> <span data-ttu-id="64905-157">Listenin yukarısında, önerilerin hangi seçeneklere dayanacağını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64905-157">Above the list, you can select which options to base the suggestions on.</span></span> <span data-ttu-id="64905-158">Ayrıca taşıma gününü belirleyen teslimat şeklini de seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64905-158">You can also select the mode of delivery, which determines the transport days.</span></span> <span data-ttu-id="64905-159">Aşağıdaki seçenekler bulunur:</span><span class="sxs-lookup"><span data-stu-id="64905-159">The following options are available:</span></span>

- <span data-ttu-id="64905-160">**Diğer ürün çeşitlerini dahil et** - Bu seçenek, ürün çeşitlerine sahip ürünler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="64905-160">**Include other product variants** - This option is available for products that have product variants.</span></span> <span data-ttu-id="64905-161">Ürünün diğer çeşitlerinin teslimat alternatiflerini dahil eder.</span><span class="sxs-lookup"><span data-stu-id="64905-161">It will include delivery alternatives for other variants of the product.</span></span> <span data-ttu-id="64905-162">Bu seçenek TEM için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="64905-162">This option isn't available for CTP.</span></span>
- <span data-ttu-id="64905-163">**Kısmi miktar dahil et** - Varsayılan olarak, yalnızca satış satırının tüm miktarını karşılayan öneriler dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="64905-163">**Include partial quantity** - By default, only suggestions that fulfill the full quantity of the sales line are included.</span></span> <span data-ttu-id="64905-164">Bu seçeneği işaretleyerek, satış siparişini kısmi olarak karşılayan önerileri dahil edin.</span><span class="sxs-lookup"><span data-stu-id="64905-164">Select this option to include suggestions that only partially fulfill the order line.</span></span> <span data-ttu-id="64905-165">Müşteri daha erken bir teslimat tarihi talep ediyor ve kısmi teslimatı kabul ediyorsa, bu seçenek yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="64905-165">This option is useful when the customer requests an earlier delivery date and accepts partial delivery.</span></span>
- <span data-ttu-id="64905-166">**Sonraki tarihleri dahil et** - Varsayılan olarak, yalnızca satış satırındaki tarihlerden daha iyi (erken) olan öneriler gösterilir.</span><span class="sxs-lookup"><span data-stu-id="64905-166">**Include later dates** - By default, only suggestions that are better (earlier) than the current dates on the sales line are shown.</span></span> <span data-ttu-id="64905-167">Sonraki tarihleri dahil etmek için bu seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="64905-167">Select this option to include later dates.</span></span> <span data-ttu-id="64905-168">Bu seçenek, tarihten başka parametrelerin önceliği olduğunda yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="64905-168">This option can be useful in situations where parameters other than the date have priority.</span></span> <span data-ttu-id="64905-169">Örneğin, belirli bir satıcı veya ambar tercih edilebilir.</span><span class="sxs-lookup"><span data-stu-id="64905-169">For example, a specific vendor or warehouse might be preferred.</span></span>
- <span data-ttu-id="64905-170">**Teslimat şekli** - Taşıma süresi ve maliyetini en iyi duruma getirmek için tercih edilen teslimat şeklini seçin.</span><span class="sxs-lookup"><span data-stu-id="64905-170">**Mode of delivery** - Select the preferred mode of delivery to optimize transport time and cost.</span></span> <span data-ttu-id="64905-171">Önerilen teslimat alternatifleri üzerindeki etkisi hemen görünür.</span><span class="sxs-lookup"><span data-stu-id="64905-171">You will immediately see the effect on the suggested delivery alternatives.</span></span> <span data-ttu-id="64905-172">Bu nedenle, bu alternatifleri karşılaştırmak kolaydır.</span><span class="sxs-lookup"><span data-stu-id="64905-172">Therefore, it's easy to compare the alternatives.</span></span>
- <span data-ttu-id="64905-173">**Tedariki dahil et** - Tedarik seçildiğinde, önerilen teslimat alternatifleri hem harici satıcıları ve hem de kuruluştaki diğer şirketleri (şirketlerarası) içerir.</span><span class="sxs-lookup"><span data-stu-id="64905-173">**Include procurement** - When procurement is selected, the suggested delivery alternatives include options to procure from both external vendors and other companies in the enterprise (intercompany).</span></span> <span data-ttu-id="64905-174">**Tedariki dahil et** seçeneği KM ve KM + çıkış marjı için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="64905-174">The **Include procurement** option is supported for ATP and ATP + Issue margin delivery date control.</span></span> <span data-ttu-id="64905-175">Ürün için varsayılan satınalma satıcısından tüm tedarik seçenekleri ve ürün için tüm onaylanan satıcılar dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="64905-175">Procurement options from the default purchase vendor for the product and all approved vendors for the product are included.</span></span>
- <span data-ttu-id="64905-176">Harici satıcılar için, hesaplama satınalma sağlama süresine dayanır.</span><span class="sxs-lookup"><span data-stu-id="64905-176">For external vendors, the calculation is based on the purchase lead time.</span></span>
- <span data-ttu-id="64905-177">Hesaplama, sirketlerarası için tedarikçi şirketten nelerin kullanılabilir olduğunu, tedarikçi şirketin teslimat tarihi denetimine dayanarak dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="64905-177">For intercompany, the calculation considers what is available from the sourcing company, based on delivery date control in the sourcing company.</span></span>
- <span data-ttu-id="64905-178">**Teslimat türü** (Tedarik için ilgili)</span><span class="sxs-lookup"><span data-stu-id="64905-178">**Delivery type** (Relevant for procurement)</span></span>
  - <span data-ttu-id="64905-179">**Stok** - Ürünler tedarikçi ambardan, satış hattındaki tesise/ambara sevk edilir.</span><span class="sxs-lookup"><span data-stu-id="64905-179">**Stock** - Products are shipped from the sourcing warehouse to the site/warehouse on the sales line.</span></span> <span data-ttu-id="64905-180">Daha sonra bu ambardan müşteriye sevk edilir.</span><span class="sxs-lookup"><span data-stu-id="64905-180">They are then shipped from that warehouse to the customer.</span></span>
  - <span data-ttu-id="64905-181">**Doğrudan teslim** - Ürünler doğrudan tedarikçi ambardan müşteriye sevk edilir.</span><span class="sxs-lookup"><span data-stu-id="64905-181">**Direct delivery** - Products are shipped directly from the sourcing warehouse to the customer.</span></span>

### <a name="the-availability-information-fasttab"></a><span data-ttu-id="64905-182">Kullanılabilirlik bilgileri hızlı sekmesi</span><span class="sxs-lookup"><span data-stu-id="64905-182">The Availability information FastTab</span></span>

<span data-ttu-id="64905-183">Bu hızlı sekme üzerindeki bilgi, seçilen teslimat alternatif satırıyla ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="64905-183">Information on this FastTab is related to the delivery alternative line that is selected.</span></span> <span data-ttu-id="64905-184">Satış satırındaki teslimat tarihi denetimine bağlı olarak aşağıdaki bilgiler gösterilir:</span><span class="sxs-lookup"><span data-stu-id="64905-184">The following information is shown, depending on the delivery date control for the sales line:</span></span>

- <span data-ttu-id="64905-185">**Satış sağlama süresi**</span><span class="sxs-lookup"><span data-stu-id="64905-185">**Sales lead time**</span></span>
  - <span data-ttu-id="64905-186">**Bugün kullanılabilir** - Eldeki fiziksel, fiziksel rezerve ve kullanılabilir fiziksel stoku göster.</span><span class="sxs-lookup"><span data-stu-id="64905-186">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
  - <span data-ttu-id="64905-187">**Parametreler** - Stok birimi ve satış sağlama sürelerini göster.</span><span class="sxs-lookup"><span data-stu-id="64905-187">**Parameters** - Show the inventory unit and sales lead time.</span></span>

- <span data-ttu-id="64905-188">**KM ve KM + çıkış marjı**</span><span class="sxs-lookup"><span data-stu-id="64905-188">**ATP and ATP + Issue margin**</span></span>
  - <span data-ttu-id="64905-189">**Bugün kullanılabilir** - Eldeki fiziksel, fiziksel rezerve ve kullanılabilir fiziksel stoku göster.</span><span class="sxs-lookup"><span data-stu-id="64905-189">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
  - <span data-ttu-id="64905-190">**Parametreler** - Stok birimi ve satış sağlama sürelerini göster.</span><span class="sxs-lookup"><span data-stu-id="64905-190">**Parameters** - Show the inventory unit and sales lead time.</span></span>
  - <span data-ttu-id="64905-191">**Gelecekteki kullanılabilirlik** - **Teslimat alternatifleri** altında seçili tesis ve ambar için mevcut ve gelecek kullanılabilirliğin görsel bir temsilini göster.</span><span class="sxs-lookup"><span data-stu-id="64905-191">**Future availability** - Show a graphical representation of current and future availability for the selected site and warehouse under **Delivery alternatives**.</span></span> <span data-ttu-id="64905-192">Ürünün gelecekteki bulunabilirliği hakkında daha ayrıntılı bilgi görmek için grafik sütunlarını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64905-192">You can select the chart columns to see more detailed information about the future availability of the product.</span></span> <span data-ttu-id="64905-193">Kaydırıcı, KM zaman dilimi içerisinde ilgili arz ve talep siparişlerinin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="64905-193">The slider shows a list of relevant demand and supply orders within the ATP time fence.</span></span>

- <span data-ttu-id="64905-194">**TEM**</span><span class="sxs-lookup"><span data-stu-id="64905-194">**CTP**</span></span>
  - <span data-ttu-id="64905-195">**Bugün kullanılabilir** - Eldeki fiziksel, fiziksel rezerve ve kullanılabilir fiziksel stoku göster.</span><span class="sxs-lookup"><span data-stu-id="64905-195">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
  - <span data-ttu-id="64905-196">**Parametreler** - Stok birimi ve satış sağlama sürelerini göster.</span><span class="sxs-lookup"><span data-stu-id="64905-196">**Parameters** - Show the inventory unit and sales lead time.</span></span>
  - <span data-ttu-id="64905-197">**Açılım** - Seçilen teslimat alternatifi için bir tedarik açılımı göster.</span><span class="sxs-lookup"><span data-stu-id="64905-197">**Explosion** - Show a supply explosion of the selected delivery alternative.</span></span> <span data-ttu-id="64905-198">Açılımda gösterilen alanları ve stok boyutlarını değiştirmek için **Kurulum**'u kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64905-198">You can use **Setup** to change the fields and inventory dimensions that are shown in the explosion.</span></span>

### <a name="the-impact-of-selected-alternative-fasttab"></a><span data-ttu-id="64905-199">Seçili alternatifin etkisi hızlı sekmesi</span><span class="sxs-lookup"><span data-stu-id="64905-199">The Impact of selected alternative FastTab</span></span>

<span data-ttu-id="64905-200">Bu hızlı sekme, seçili teslimat alternatifinin etkisini vurgular.</span><span class="sxs-lookup"><span data-stu-id="64905-200">This FastTab highlights the impact of the selected delivery alternative.</span></span> <span data-ttu-id="64905-201">**Tamam**'ı seçerseniz satış satırı SEÇİLİ sütunlarındaki vurgulanan değerlerle güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="64905-201">If you select **OK**, the sales line is updated with the highlighted values in the SELECTED columns.</span></span> <span data-ttu-id="64905-202">Seçilen teslimat alternatifindeki miktar, satış satırındaki miktardan az ise, bir teslimat planının oluşturulacağını ve sipariş satırının iki satıra ayrılacağını unutmayın: bir satır seçilen miktar için ve bir satır kalan miktar için.</span><span class="sxs-lookup"><span data-stu-id="64905-202">Note that, if the quantity on the selected delivery alternative is less than quantity on the sales line, a delivery schedule is created, and the order line is split into two lines: one line for the selected quantity and one line for the remaining quantity.</span></span> <span data-ttu-id="64905-203">Ticari satırı da planlı satırlar ile eşleşecek ve böylece fiyatlandırmayı etkileyecek şekilde güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64905-203">You can also update the commercial line so that it matches the schedule lines and affects the pricing.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64905-204">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="64905-204">Additional resources</span></span>

[<span data-ttu-id="64905-205">Sipariş taahhüdü</span><span class="sxs-lookup"><span data-stu-id="64905-205">Order promising</span></span>](delivery-dates-available-promise-calculations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]