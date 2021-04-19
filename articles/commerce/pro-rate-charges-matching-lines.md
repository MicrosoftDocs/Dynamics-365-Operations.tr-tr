---
title: Başlık giderlerini eşleşen satış satırlarına eşit dağıt
description: Bu konu, Commerce kanal siparişlerine otomatik giderlerin hesaplanmasını ve uygulanması için ek yeterlilikleri, gelişmiş otomatik masraf özelliğini kullanarak açıklar.
author: hhaines
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 22939e8fd63a355effecf0c16fecd20377faa3a6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791066"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a><span data-ttu-id="7f8c7-103">Başlık giderlerini eşleşen satış satırlarına eşit dağıt</span><span class="sxs-lookup"><span data-stu-id="7f8c7-103">Prorate header charges to matching sales lines</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7f8c7-104">Bu konu, başlık düzeyi otomatik masrafları gruplandırmayı ve bunları ticaret satış satırlarına eşit dağıtmak için özelliği açıklar.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-104">This topic describes the functionality for grouping header-level auto-charges and prorating them to commerce sales lines.</span></span> <span data-ttu-id="7f8c7-105">Bu özellik, Retail sürüm 10.0.1 içinde satış noktası (POS) içerisinde ve Retail sürüm 10.0.2 içinde çağrı merkezinde oluşturulmuş hareketler için kullanılabilirdir.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-105">This functionality is available for transactions that are created at the point of sale (POS) in Retail version 10.0.1 and sales that are created in a call center in Retail version 10.0.2.</span></span>

<span data-ttu-id="7f8c7-106">Bu özellik, yalnızca [gelişmiş otomatik masraflar](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) özelliği, **Commerce parametreleri** sayfasındaki seçenek kullanılarak açılmışsa kullanılabilirdir.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-106">This functionality is available only if the [advanced auto-charges](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) feature is turned on by using the option on the **Commerce parameters** page.</span></span> <span data-ttu-id="7f8c7-107">Ek olarak, otomatik giderler için gelişmiş hesaplama yöntemi, yalnızca ticaret kanalları aracılığıyla oluşturulmuş (POS, çağrı merkezi ve Dynamics e-Ticaret platformu) ticaret satış siparişlerine uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-107">Additionally, the enhanced calculation method for auto-charges can be applied only to sales orders that are created through commerce channels (the POS, a call center, and the Dynamics e-Commerce platform).</span></span>

<span data-ttu-id="7f8c7-108">Bu yeni özellik, başlık düzeyi otomatik masrafların hesaplanmasına ve satış hareketlerine uygulanmasında kuruluşlara daha fazla esneklik verir.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-108">This new functionality gives organizations more flexibility in the way that header-level auto-charges are calculated and applied to sales transactions.</span></span>

<span data-ttu-id="7f8c7-109">Sürüm 10.0.1'den önceki uygulama sürümlerinde, belirli bir teslimat modu ilişkisine sahip başlık düzeyi otomatik giderleri, yalnızca satış siparişi başlığında tanımlanmış teslimat modu ile bir eşleşme olduğunda hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-109">In versions of the app earlier than version 10.0.1, header-level auto-charges that have a specific mode of delivery relation are calculated only when there is a match with the mode of delivery that is defined on the sales order header.</span></span>

<span data-ttu-id="7f8c7-110">Örneğin, başlık düzeyi otomatik masraflar, teslimat modu **99** ve teslimat modu **11** için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-110">For example, header-level auto-charges are defined for mode of delivery **99** and mode of delivery **11**.</span></span> <span data-ttu-id="7f8c7-111">Bir satış siparişi oluşturulur ve teslimat modu **99**, sipariş başlığında tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-111">A sales order is created, and mode of delivery **99** is defined on the order header.</span></span> <span data-ttu-id="7f8c7-112">Ancak, satış satırlarının bazıları, teslimat modu **11** kullanılarak sevk edilmek üzere ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-112">However, some of the sale lines are set up so that they're shipped by using mode of delivery **11**.</span></span> <span data-ttu-id="7f8c7-113">Bu durumda, yalnızca teslimat modu **99** ile bağlantılı başlık düzeyi masrafları dikkate alınır ve satış siparişine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-113">In this case, only the header-level charges that are linked to mode of delivery **99** are considered and applied to the sales order.</span></span>

<span data-ttu-id="7f8c7-114">Commerce içinde, başlık düzeyi masrafları, bir [katmanlı masraf yapılandırması](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery) tanımlamanıza izin veren ek bir özelliğe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-114">In Commerce, the header-level charges have an additional feature that lets you define a [tiered charge configuration](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery) that is based on the order value.</span></span> <span data-ttu-id="7f8c7-115">Örneğin, sipariş değeri 50,00 $ ve 200,00 $ arasındaysa, bir kuruluş 5,00 $ tutarında navlun gideri isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-115">For example, if the order value is between $50.00 and $200.00, an organization might want to charge a freight charge of $5.00.</span></span> <span data-ttu-id="7f8c7-116">Ancak, siparişin değeri 200,01 $ ve 500,00 $ arasındaysa, navlun ücreti 4,00 $ olabilir.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-116">However, if the order value is between $200.01 and $500.00, the freight charge might be $4.00.</span></span>

<span data-ttu-id="7f8c7-117">Bazı kuruluşlar, başlık düzeyi masraflarla sağlanan katmanlı masraf hesaplamasından faydalanmak ister.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-117">Some organizations want the benefits of the tiered charge calculation that is provided with header-level charges.</span></span> <span data-ttu-id="7f8c7-118">Ancak, karma teslimat modları içeren bazı senaryolarda, hesaplanan masrafların her bir satış satırında tanımlanmış teslimat modu ile eşleşmeye dayanmasını da temin etmek isterler.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-118">However, in scenarios that involve mixed modes of delivery, they also want to make sure that the charges that are calculated are based on a match with the mode of delivery that is defined on each sales line.</span></span>

<span data-ttu-id="7f8c7-119">Şimdi başlık düzeyi otomatik masrafları, sipariş üzerindeki tüm teslimat modlarının masraflar hesaplanırken dikkate alınmasını sağlayacak şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-119">You can now configure header-level auto-charges so that all modes of delivery on the order are considered when charges are calculated.</span></span> <span data-ttu-id="7f8c7-120">Bu özellik, başlık düzeyi masrafları hesaplamak için daha karmaşık bir hesaplama mantığı gerektirir.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-120">This functionality requires a more complex calculation logic to calculate the header-level charges.</span></span> <span data-ttu-id="7f8c7-121">Mantık, aynı teslimat modu kullanılarak sevk edilen tüm öğeleri gruplar ve bu grubu, başlık düzeyi otomatik masrafları hesaplarken bir hesaplama grubu olarak kullanır.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-121">The logic groups together all the items that are shipped using the same mode of delivery, and it treats that group as the calculation group for the items when it calculates the header-level auto-charges.</span></span> <span data-ttu-id="7f8c7-122">Aynı teslimat moduna sahip öğeler için otomatik masraflar öğelerin birleştirilmiş satış değerine dayanarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-122">For items that have the same mode of delivery, auto-charges are calculated based on the combined sales value of the items.</span></span> <span data-ttu-id="7f8c7-123">Bu şekilde, uygun otomatik masraf katmanı belirlenir.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-123">In this way, the appropriate auto-charge tier is determined.</span></span>

<span data-ttu-id="7f8c7-124">Uygun başlık düzeyi masraflar aynı teslimat modunu kullanan satış satırları için alındıktan sonra, hesaplanan masraflar satış satırı düzeyine eşit şekilde dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-124">After the appropriate header-level charges are obtained for the sales lines that are shipped using the same mode of delivery, the calculated charges are prorated down to the sales line level.</span></span> <span data-ttu-id="7f8c7-125">Bu masraflar satır düzeyinde olduğundan ve başlık düzeyinde tutulmadığından, daha belirgin bir bağlantı öğe ve bunun için hesaplanan masraf değer arasında yapılır.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-125">Because these charges are at the line level and not kept at the header level, a more specific link is made between the item and the charge value that calculated for it.</span></span> <span data-ttu-id="7f8c7-126">Bu davranış, kuruluşun yalnızca bazı öğeler iade edildiğinde masrafın tamamı yerine yalnızca bir kısmının geri ödenmesini istediği, kısmi iade senaryolarında faydalı olabilir.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-126">This behavior can be useful in partial return scenarios, where an organization wants to refund only part of the charge instead of the whole charge when only some items are returned.</span></span>

## <a name="scenarios"></a><span data-ttu-id="7f8c7-127">Senaryolar</span><span class="sxs-lookup"><span data-stu-id="7f8c7-127">Scenarios</span></span>

<span data-ttu-id="7f8c7-128">Aşağıdaki iki örnek senaryo, bu masrafların yeni özellik kullanıldığında ve kullanılmadığında nasıl hesaplandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-128">The following two sample scenarios outline how these charges are calculated both when the new functionality is used and when it isn't used.</span></span>

### <a name="scenario-1"></a><span data-ttu-id="7f8c7-129">Senaryo 1</span><span class="sxs-lookup"><span data-stu-id="7f8c7-129">Scenario 1</span></span>

<span data-ttu-id="7f8c7-130">Bu senaryo, **Eşleşen satış satırlarına eşit dağıt** seçeneği, otomatik masraf kurulumunda **Hayır** olarak ayarlanmasını açıklar.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-130">This scenario outlines the behavior when the **Pro-rate to matching sales lines** option is set to **No** in the auto-charge setup.</span></span> <span data-ttu-id="7f8c7-131">(Davranış, sürüm 10.0.1'den önceki uygulama sürümlerindeki başlık düzeyi masrafların davranışına eşdeğerdir)</span><span class="sxs-lookup"><span data-stu-id="7f8c7-131">(The behavior is equivalent to the behavior of header-level charges in app versions that are earlier than version 10.0.1.)</span></span>

<span data-ttu-id="7f8c7-132">Bu senaryoda, kuruluş teslimat modu ilişkisi **99** ve teslimat modu ilişkisi **11** için başlık düzeyi masrafları tanımlamıştır.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-132">In this scenario, the organization has defined header-level charges for mode of delivery relation **99** and mode of delivery relation **11**.</span></span> <span data-ttu-id="7f8c7-133">Teslimat modu **21** için otomatik masraf yapılandırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-133">No auto-charges are configured for mode of delivery **21**.</span></span>

![Teslimat modu 99 için eşleşen satır eşit dağıtma kapalı olduğunda otomatik masraf](media/99_disabled.png)

![Teslimat modu 11 için eşleşen satır eşit dağıtma kapalı olduğunda otomatik masraf](media/11_disabled.png)

<span data-ttu-id="7f8c7-136">Bir satış siparişi çağrı merkezinde oluşturulur ve teslimat modu **99** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-136">A sales order is created in the call center, and the mode of delivery is set to **99**.</span></span> <span data-ttu-id="7f8c7-137">Bu sipariş beş öğe içerir.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-137">This order contains five items.</span></span> <span data-ttu-id="7f8c7-138">İki sipariş satırı, teslimat modu **99** kullanmak üzere yapılandırılmıştır, iki satır teslimat modu **11** kullanmak üzere yapılandırılmıştır ve bir satır teslimat modu **21** kullanmak üzere yapılandırılmıştır, aşağıdaki tabloda gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-138">Two order lines have been configured to use mode of delivery **99**, two lines have been configured to use mode of delivery **11**, and one line has been configured to use mode of delivery **21**, as shown in the following table.</span></span>

| <span data-ttu-id="7f8c7-139">Madde</span><span class="sxs-lookup"><span data-stu-id="7f8c7-139">Item</span></span>  | <span data-ttu-id="7f8c7-140">Satır miktarı</span><span class="sxs-lookup"><span data-stu-id="7f8c7-140">Line quantity</span></span> | <span data-ttu-id="7f8c7-141">Teslimat şekli</span><span class="sxs-lookup"><span data-stu-id="7f8c7-141">Delivery mode</span></span> | <span data-ttu-id="7f8c7-142">Birim başına fiyat</span><span class="sxs-lookup"><span data-stu-id="7f8c7-142">Price per unit</span></span> |
|-------|---------------|---------------|----------------|
| <span data-ttu-id="7f8c7-143">81331</span><span class="sxs-lookup"><span data-stu-id="7f8c7-143">81331</span></span> | <span data-ttu-id="7f8c7-144">1</span><span class="sxs-lookup"><span data-stu-id="7f8c7-144">1</span></span>             | <span data-ttu-id="7f8c7-145">11</span><span class="sxs-lookup"><span data-stu-id="7f8c7-145">11</span></span>            | <span data-ttu-id="7f8c7-146">10 $</span><span class="sxs-lookup"><span data-stu-id="7f8c7-146">$10</span></span>            |
| <span data-ttu-id="7f8c7-147">81332</span><span class="sxs-lookup"><span data-stu-id="7f8c7-147">81332</span></span> | <span data-ttu-id="7f8c7-148">1</span><span class="sxs-lookup"><span data-stu-id="7f8c7-148">1</span></span>             | <span data-ttu-id="7f8c7-149">99</span><span class="sxs-lookup"><span data-stu-id="7f8c7-149">99</span></span>            | <span data-ttu-id="7f8c7-150">$50</span><span class="sxs-lookup"><span data-stu-id="7f8c7-150">$50</span></span>            |
| <span data-ttu-id="7f8c7-151">81333</span><span class="sxs-lookup"><span data-stu-id="7f8c7-151">81333</span></span> | <span data-ttu-id="7f8c7-152">2</span><span class="sxs-lookup"><span data-stu-id="7f8c7-152">2</span></span>             | <span data-ttu-id="7f8c7-153">11</span><span class="sxs-lookup"><span data-stu-id="7f8c7-153">11</span></span>            | <span data-ttu-id="7f8c7-154">30 $</span><span class="sxs-lookup"><span data-stu-id="7f8c7-154">$30</span></span>            |
| <span data-ttu-id="7f8c7-155">81334</span><span class="sxs-lookup"><span data-stu-id="7f8c7-155">81334</span></span> | <span data-ttu-id="7f8c7-156">3</span><span class="sxs-lookup"><span data-stu-id="7f8c7-156">3</span></span>             | <span data-ttu-id="7f8c7-157">99</span><span class="sxs-lookup"><span data-stu-id="7f8c7-157">99</span></span>            | <span data-ttu-id="7f8c7-158">10 $</span><span class="sxs-lookup"><span data-stu-id="7f8c7-158">$10</span></span>            |
| <span data-ttu-id="7f8c7-159">81334</span><span class="sxs-lookup"><span data-stu-id="7f8c7-159">81334</span></span> | <span data-ttu-id="7f8c7-160">3</span><span class="sxs-lookup"><span data-stu-id="7f8c7-160">3</span></span>             | <span data-ttu-id="7f8c7-161">21</span><span class="sxs-lookup"><span data-stu-id="7f8c7-161">21</span></span>            | <span data-ttu-id="7f8c7-162">5 $</span><span class="sxs-lookup"><span data-stu-id="7f8c7-162">$5</span></span>             |

<span data-ttu-id="7f8c7-163">Bu senaryoda, siparişin tamamı teslimat modu **99** için otomatik masraf tablosuna karşı değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-163">In this scenario, the whole order is evaluated against the auto-charge table for mode of delivery **99**.</span></span> <span data-ttu-id="7f8c7-164">Tüm satış satırlarının son toplamı, otomatik masraf yapılandırmasında eşleşen bir katmanı belirlemek için kullanılır ve bu masraf sipariş başlığı düzeyinde uygulanır.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-164">The full total of all sales lines is used to determine a matching tier in the auto-charge configuration, and this charge is applied at the order header level.</span></span> <span data-ttu-id="7f8c7-165">Bu örnekte, sipariş toplamı 165,00 $ tutarındadır ve 15,00 $ navlun masrafı sipariş başlığına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-165">In this example, the order total is $165.00, and the $15.00 freight charge is applied to the order header.</span></span> <span data-ttu-id="7f8c7-166">Teslimat modu **11** için yapılandırılan otomatik masraflara hiçbir zaman başvurulmaz veya uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-166">Auto-charges that are configured for mode of delivery **11** are never referenced or applied.</span></span>

<span data-ttu-id="7f8c7-167">Bu senaryoda, bir müşteri siparişteki bazı öğeleri iade ederse ve [iade edileceği şekilde masraf kodu yapılandırılmışsa](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), toplam başlık düzeyi masrafı iadeye sistematik olarak uygulanır, yalnızca bazı öğeler iade edilmiş olsa bile.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-167">In this scenario, if a customer returns some of the items on the order, and if the [charge code has been configured so that it will be refunded](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), the total header-level charge is systematically applied to the refund, even if only some of the items are returned.</span></span>

### <a name="scenario-2"></a><span data-ttu-id="7f8c7-168">Senaryo 2</span><span class="sxs-lookup"><span data-stu-id="7f8c7-168">Scenario 2</span></span>

<span data-ttu-id="7f8c7-169">Bu senaryoda, teslimat modu ilişkisi **99** ve teslimat modu ilişkisi **11** için başlık düzeyi masrafları tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-169">In this scenario, header-level charges are defined for mode of delivery relation **99** and mode of delivery relation **11**.</span></span> <span data-ttu-id="7f8c7-170">Ancak, **Eşleşen satış satırlarına eşit dağıt** seçeneği bu otomatik masraf tabloları için **Evet** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-170">However, the **Pro-rate to matching sales lines** option is set to **Yes** for these auto-charge tables.</span></span>

![Teslimat modu 99 için eşleşen satır eşit dağıtma açık olduğunda otomatik masraf](media/99_enabled.png)

![Teslimat modu 11 için eşleşen satır eşit dağıtma açık olduğunda otomatik masraf](media/11_enabled.png)

<span data-ttu-id="7f8c7-173">Bu senaryo, beş satır içeren aynı satış siparişini kullanır.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-173">This scenario uses the same sales order that contains five lines.</span></span> <span data-ttu-id="7f8c7-174">Sipariş başlığındaki teslimat modu **99** olarak ayarlanmıştır ancak satış siparişindeki her bir öğenin teslimat modu aşağıdaki tablodaki gibi yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-174">The mode of delivery on the order header is set to **99**, but the mode of delivery for each item on the sales order is configured as shown in the following table.</span></span>

| <span data-ttu-id="7f8c7-175">Madde</span><span class="sxs-lookup"><span data-stu-id="7f8c7-175">Item</span></span>  | <span data-ttu-id="7f8c7-176">Satır miktarı</span><span class="sxs-lookup"><span data-stu-id="7f8c7-176">Line quantity</span></span> | <span data-ttu-id="7f8c7-177">Teslimat şekli</span><span class="sxs-lookup"><span data-stu-id="7f8c7-177">Delivery mode</span></span> | <span data-ttu-id="7f8c7-178">Birim başına fiyat</span><span class="sxs-lookup"><span data-stu-id="7f8c7-178">Price per unit</span></span> |
|-------|---------------|---------------|----------------|
| <span data-ttu-id="7f8c7-179">81331</span><span class="sxs-lookup"><span data-stu-id="7f8c7-179">81331</span></span> | <span data-ttu-id="7f8c7-180">1</span><span class="sxs-lookup"><span data-stu-id="7f8c7-180">1</span></span>             | <span data-ttu-id="7f8c7-181">11</span><span class="sxs-lookup"><span data-stu-id="7f8c7-181">11</span></span>            | <span data-ttu-id="7f8c7-182">10 $</span><span class="sxs-lookup"><span data-stu-id="7f8c7-182">$10</span></span>            |
| <span data-ttu-id="7f8c7-183">81332</span><span class="sxs-lookup"><span data-stu-id="7f8c7-183">81332</span></span> | <span data-ttu-id="7f8c7-184">1</span><span class="sxs-lookup"><span data-stu-id="7f8c7-184">1</span></span>             | <span data-ttu-id="7f8c7-185">99</span><span class="sxs-lookup"><span data-stu-id="7f8c7-185">99</span></span>            | <span data-ttu-id="7f8c7-186">$50</span><span class="sxs-lookup"><span data-stu-id="7f8c7-186">$50</span></span>            |
| <span data-ttu-id="7f8c7-187">81333</span><span class="sxs-lookup"><span data-stu-id="7f8c7-187">81333</span></span> | <span data-ttu-id="7f8c7-188">2</span><span class="sxs-lookup"><span data-stu-id="7f8c7-188">2</span></span>             | <span data-ttu-id="7f8c7-189">11</span><span class="sxs-lookup"><span data-stu-id="7f8c7-189">11</span></span>            | <span data-ttu-id="7f8c7-190">30 $</span><span class="sxs-lookup"><span data-stu-id="7f8c7-190">$30</span></span>            |
| <span data-ttu-id="7f8c7-191">81334</span><span class="sxs-lookup"><span data-stu-id="7f8c7-191">81334</span></span> | <span data-ttu-id="7f8c7-192">3</span><span class="sxs-lookup"><span data-stu-id="7f8c7-192">3</span></span>             | <span data-ttu-id="7f8c7-193">99</span><span class="sxs-lookup"><span data-stu-id="7f8c7-193">99</span></span>            | <span data-ttu-id="7f8c7-194">10 $</span><span class="sxs-lookup"><span data-stu-id="7f8c7-194">$10</span></span>            |
| <span data-ttu-id="7f8c7-195">81334</span><span class="sxs-lookup"><span data-stu-id="7f8c7-195">81334</span></span> | <span data-ttu-id="7f8c7-196">3</span><span class="sxs-lookup"><span data-stu-id="7f8c7-196">3</span></span>             | <span data-ttu-id="7f8c7-197">21</span><span class="sxs-lookup"><span data-stu-id="7f8c7-197">21</span></span>            | <span data-ttu-id="7f8c7-198">5 $</span><span class="sxs-lookup"><span data-stu-id="7f8c7-198">$5</span></span>             |

<span data-ttu-id="7f8c7-199">Otomatik masraf yapılandırması, eşleşen satış satırlarına eşit dağıtılmak üzere yapılandırıldığından, sistem aşağıdaki hesaplama adımlarını gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-199">Because the auto-charge configuration is set to prorate to matching sales lines, the system performs the following calculation steps.</span></span>

1. <span data-ttu-id="7f8c7-200">Aynı teslimat moduna sahip tüm öğeler birlikte gruplanır ve sistem, gruptaki öğelerin toplam ürün değerini hesaplar.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-200">All items that have the same mode of delivery are grouped together, and the system calculates the total product value of the items in the group.</span></span>

    <span data-ttu-id="7f8c7-201">**Teslimat modu 11**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-201">**Delivery mode 11**</span></span>

    - <span data-ttu-id="7f8c7-202">Öğe 81331, miktar 1 = 10 $</span><span class="sxs-lookup"><span data-stu-id="7f8c7-202">Item 81331, quantity 1 = $10</span></span>
    - <span data-ttu-id="7f8c7-203">Öğe 81333, miktar 2 = 60 $ net (birim başına 30 $)</span><span class="sxs-lookup"><span data-stu-id="7f8c7-203">Item 81333, quantity 2 = $60 net ($30 per unit)</span></span>
    - <span data-ttu-id="7f8c7-204">**Teslimat modu 11 için toplam ürün değeri = 70 $**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-204">**Total product value for delivery mode 11 = $70**</span></span>

    <span data-ttu-id="7f8c7-205">**Teslimat modu 99**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-205">**Delivery mode 99**</span></span>

    - <span data-ttu-id="7f8c7-206">Öğe 81332, miktar 1 = 50 $</span><span class="sxs-lookup"><span data-stu-id="7f8c7-206">Item 81332, quantity 1 = $50</span></span>
    - <span data-ttu-id="7f8c7-207">Öğe 81334, miktar 3 = 30 $ net</span><span class="sxs-lookup"><span data-stu-id="7f8c7-207">Item 81334, quantity 3 = $30 net</span></span>
    - <span data-ttu-id="7f8c7-208">**Teslimat modu 99 için toplam ürün değeri = 80 $**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-208">**Total product value for delivery mode 99 = $80**</span></span>

    <span data-ttu-id="7f8c7-209">**Teslimat modu 21**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-209">**Delivery mode 21**</span></span>

    - <span data-ttu-id="7f8c7-210">Öğe 81334, miktar 3 = 15 $ net</span><span class="sxs-lookup"><span data-stu-id="7f8c7-210">Item 81334, quantity 3 = $15 net</span></span>
    - <span data-ttu-id="7f8c7-211">**Teslimat modu 21 için toplam ürün değeri = 15 $**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-211">**Total product value for delivery mode 21 = $15**</span></span>

2. <span data-ttu-id="7f8c7-212">Sistem, her bir öğe grubu için teslimat modunun ve müşterinin eşleştiği başlık düzeyi otomatik masrafları için yapılandırmayı arar.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-212">The system looks for the configuration for header-level auto-charges that matches the customer and mode of delivery settings for each group of items.</span></span> <span data-ttu-id="7f8c7-213">Yapılandırma bulunursa, sistem katmanlı yapılandırmaya bakarak uygulanacak masrafı bulur, teslimat modu grubundaki öğelerin toplam ürün değerine dayanarak.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-213">If the configuration is found, the system looks in the tiered configuration to find the charge that should be applied, based on the total product value of items in the mode of delivery group.</span></span>

    <span data-ttu-id="7f8c7-214">**Teslimat modu 11**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-214">**Delivery mode 11**</span></span>

    - <span data-ttu-id="7f8c7-215">Toplam ürün değeri = 70 $</span><span class="sxs-lookup"><span data-stu-id="7f8c7-215">Total product value = $70</span></span>
    - <span data-ttu-id="7f8c7-216">**Masraf değeri = 7 $**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-216">**Charge value = $7**</span></span>

    <span data-ttu-id="7f8c7-217">**Teslimat modu 99**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-217">**Delivery mode 99**</span></span>

    - <span data-ttu-id="7f8c7-218">Toplam ürün değeri = 80 $</span><span class="sxs-lookup"><span data-stu-id="7f8c7-218">Total product value = $80</span></span>
    - <span data-ttu-id="7f8c7-219">**Masraf değeri = 15 $**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-219">**Charge value = $15**</span></span>

    <span data-ttu-id="7f8c7-220">**Teslimat modu 21**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-220">**Delivery mode 21**</span></span>

    - <span data-ttu-id="7f8c7-221">Toplam ürün değeri = 15 $</span><span class="sxs-lookup"><span data-stu-id="7f8c7-221">Total product value = $15</span></span>
    - <span data-ttu-id="7f8c7-222">**Masraf değeri = 0 $** (Bu müşteri ve teslimat modu için herhangi bir otomatik masraf yapılandırılmamıştır.)</span><span class="sxs-lookup"><span data-stu-id="7f8c7-222">**Charge value = $0** (No auto-charges have been configured for this combination of a customer and a mode of delivery.)</span></span>

    ![Teslimat modu 11 masrafları, vurgulanan katmana düşer](media/step2mode11.png)

    ![Teslimat modu 99 masrafları, vurgulanan katmana düşer](media/step2mode99.png)

3. <span data-ttu-id="7f8c7-225">Sistem, her bir satıra uygulanacak masraf değerini, satırın grubun toplam ürün değerine orantısal ilişkisini dikkate alan eşit dağıtma mantığına dayanarak hesaplar.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-225">The system calculates the charge value that should be applied to each line, based on proration logic that considers the proportional value of the line in relation to the group's total product value.</span></span>

    <span data-ttu-id="7f8c7-226">**Teslimat modu 11**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-226">**Delivery mode 11**</span></span>

    - <span data-ttu-id="7f8c7-227">Masraf değeri = 7 $</span><span class="sxs-lookup"><span data-stu-id="7f8c7-227">Charge value = $7</span></span>
    - <span data-ttu-id="7f8c7-228">Grup ürün değeri = 70 $</span><span class="sxs-lookup"><span data-stu-id="7f8c7-228">Group product value = $70</span></span>
    - <span data-ttu-id="7f8c7-229">Satır 1 değeri = 10 $ (= grup değerinin yüzde 14,2857'si)</span><span class="sxs-lookup"><span data-stu-id="7f8c7-229">Line 1 value = $10 (= 14.2857 percent of the group value)</span></span>
    - <span data-ttu-id="7f8c7-230">Satır 3 değeri = 60 $ (= grup değerinin yüzde 85,7143'si)</span><span class="sxs-lookup"><span data-stu-id="7f8c7-230">Line 3 value = $60 (= 85.7143 percent of the group value)</span></span>
    - <span data-ttu-id="7f8c7-231">**Satır 1 için satır masrafı = 1 $**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-231">**Line charge for line 1 = $1**</span></span>
    - <span data-ttu-id="7f8c7-232">**Satır 3 için satır masrafı = 6 $**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-232">**Line charge for line 3 = $6**</span></span>

    <span data-ttu-id="7f8c7-233">**Teslimat modu 99**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-233">**Delivery mode 99**</span></span>

    - <span data-ttu-id="7f8c7-234">Masraf değeri = 15 $</span><span class="sxs-lookup"><span data-stu-id="7f8c7-234">Charge value = $15</span></span>
    - <span data-ttu-id="7f8c7-235">Grup ürün değeri = 80 $</span><span class="sxs-lookup"><span data-stu-id="7f8c7-235">Group product value = $80</span></span>
    - <span data-ttu-id="7f8c7-236">Satır 2 değeri = 50 $ (= grup değerinin yüzde 62,5'si)</span><span class="sxs-lookup"><span data-stu-id="7f8c7-236">Line 2 value = $50 (= 62.5 percent of the group value)</span></span>
    - <span data-ttu-id="7f8c7-237">Satır 4 değeri = 30 $ (= grup değerinin yüzde 37,5'si)</span><span class="sxs-lookup"><span data-stu-id="7f8c7-237">Line 4 value = $30 (= 37.5 percent of the group value)</span></span>
    - <span data-ttu-id="7f8c7-238">**Satır 2 için satır masrafı = 9,38 $**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-238">**Line charge for line 2 = $9.38**</span></span>
    - <span data-ttu-id="7f8c7-239">**Satır 4 için satır masrafı = 5,62 $**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-239">**Line charge for line 4 = $5.62**</span></span>

    <span data-ttu-id="7f8c7-240">**Teslimat modu 21**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-240">**Delivery mode 21**</span></span>

    - <span data-ttu-id="7f8c7-241">Masraf değeri = 0 $</span><span class="sxs-lookup"><span data-stu-id="7f8c7-241">Charge value = $0</span></span>
    - <span data-ttu-id="7f8c7-242">Grup ürün değeri = 15 $</span><span class="sxs-lookup"><span data-stu-id="7f8c7-242">Group product value = $15</span></span>
    - <span data-ttu-id="7f8c7-243">Satır 5 değeri = 15 $ (= grup değerinin yüzde 100'si)</span><span class="sxs-lookup"><span data-stu-id="7f8c7-243">Line 5 value = $15 (= 100 percent of the group value)</span></span>
    - <span data-ttu-id="7f8c7-244">**Satır 5 için satır masrafı = 0 $**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-244">**Line charge for line 5 = $0**</span></span>

<span data-ttu-id="7f8c7-245">Bu nedenle, bu örnek için öğe 81334'e 5,62 $ tutarında bir navlun masrafı atanacaktır.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-245">Therefore, for this example, item 81334 will be assigned a freight charge of $5.62.</span></span> <span data-ttu-id="7f8c7-246">Bu giderleri satış satırı için **Giderleri koru** sayfasında görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-246">You can view these charges on the **Maintain charges** page for the sales line.</span></span> <span data-ttu-id="7f8c7-247">Aşağıdaki çizim, bu sayfanın öğe 81334 için nasıl gözükeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-247">The following illustration shows what this page looks like for item 81334.</span></span>

![Öğe 81334 için satış satırında eşit dağıtılmış masraflar](media/proratedlinecharge.png)

<span data-ttu-id="7f8c7-249">Bu hesaplama yöntemi, kısmi iade senaryoları için kullanılırsa, masraf kodu iade edilebilirse, masrafın yalnızca bu satıra tahsis edilmiş kısmı, öğe iade edildiğinde geri ödenecektir.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-249">When this method of calculation is used in a partial return scenario, if the charge code is refundable, only the part of the charge that is allocated to that line will be refunded when the item is returned.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7f8c7-250">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7f8c7-250">Additional resources</span></span>

[<span data-ttu-id="7f8c7-251">Çok yönlü kanal gelişmiş otomatik masrafları</span><span class="sxs-lookup"><span data-stu-id="7f8c7-251">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="7f8c7-252">Kanala göre otomatik masrafları etkinleştirme ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7f8c7-252">Enable and configure auto charges by channel</span></span>](auto-charges-by-channel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]