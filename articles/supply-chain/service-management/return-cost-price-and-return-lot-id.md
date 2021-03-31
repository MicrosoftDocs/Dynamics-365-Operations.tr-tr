---
title: İade maliyet fiyatı ve iade lot kodu
description: İade edilen ürünlerin maliyetinin ürünleri müşteriye sattığınız zamandaki maliyete eşit olmasını isteyebilirsiniz. Bunu **İade lot kodu**'nu kullanarak yapabilirsiniz.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnInventTransIdLookup, ReturnItemNumLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b420c0716823f587ea3f349a5d654ace23d84f41
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219281"
---
# <a name="return-cost-price-and-return-lot-id"></a><span data-ttu-id="a4407-104">İade maliyet fiyatı ve iade lot kodu</span><span class="sxs-lookup"><span data-stu-id="a4407-104">Return cost price and return lot ID</span></span>        

[!include [banner](../includes/banner.md)]



<span data-ttu-id="a4407-105">Stoğa iade edilen ürünlerin maliyeti ürünlerin geçerli maliyeti kullanılarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="a4407-105">The cost of products that are returned to inventory is calculated by using the current cost of the products.</span></span> <span data-ttu-id="a4407-106">Ancak, iade edilen ürünlerin maliyetinin ürünleri müşteriye sattığınız zamandaki maliyete eşit olmasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4407-106">However, you might want the cost of the returned products to equal the cost of the products at the time when you sold the products to the customer.</span></span> <span data-ttu-id="a4407-107">Bunu **Satış siparişi** formundaki **Satır ayrıntıları** hızlı sekmesinde yer alan **İade lot kodu** alanını kullanarak yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4407-107">You can do this by using the **Return lot ID** field on the **Line details** FastTab in the **Sales order** form.</span></span>

<span data-ttu-id="a4407-108">Örneğin aşağıdaki senaryoyu dikkate alın:</span><span class="sxs-lookup"><span data-stu-id="a4407-108">For example, consider the following scenario.</span></span> <span data-ttu-id="a4407-109">Bir müşteriye fatura kesiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="a4407-109">You invoice a customer.</span></span> <span data-ttu-id="a4407-110">Daha sonra müşteri teslim edilen ürünleri size iade ediyor.</span><span class="sxs-lookup"><span data-stu-id="a4407-110">Then, the customer returns the delivered products to you.</span></span> <span data-ttu-id="a4407-111">Ürünleri stoğa iade ediyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="a4407-111">You return the products to stock.</span></span> <span data-ttu-id="a4407-112">Bu durumda, müşteriyi iade edilen ürünler için alacaklandırdığınızda, bu ürünlerin maliyeti ürünlerin geçerli maliyeti kullanılarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="a4407-112">In this case, when you credit the customer for the returned products, the cost of those products is calculated by using the current cost of the products.</span></span> <span data-ttu-id="a4407-113">Ancak, **İade lot kodu** alanını kullanırsanız, iade edilen ürünlerin maliyeti müşteriye yapılan orijinal satışın faturasındaki maliyet kullanılarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="a4407-113">However, if you use the **Return lot ID** field, the cost of the returned products is calculated by using the cost on the invoice of the original sale to the customer.</span></span>

<span data-ttu-id="a4407-114">Müşteriden gelen iadeler için geçerli maliyet dışında bir maliyet kullanmak için aşağıdaki yöntemlerden birini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a4407-114">To use a cost other than the current cost for returns from a customer, use one of the following methods.</span></span>

## <a name="method-1-manually-enter-the-return-cost-price"></a><span data-ttu-id="a4407-115">Yöntem 1: İade maliyet fiyatını el ile girin.</span><span class="sxs-lookup"><span data-stu-id="a4407-115">Method 1: Manually enter the return cost price</span></span>

<span data-ttu-id="a4407-116">Varsayılan olarak, bir iade siparişine maddeleri eklediğinizde, maddeler stoğa geçerli maliyet fiyatından iade edilir.</span><span class="sxs-lookup"><span data-stu-id="a4407-116">By default, when you add items to a return order, the items are returned to inventory at the current cost price.</span></span> <span data-ttu-id="a4407-117">Farklı bir iade maliyet fiyatı belirlemek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a4407-117">To specify a different return cost price, follow these steps.</span></span>

1.  <span data-ttu-id="a4407-118">**Satış ve pazarlama** \> **Genel** \> **İade siparişleri** \> **Tüm iade siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4407-118">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="a4407-119">**Eylem bölmesinde** **Yeni** grubunda **İade siparişi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4407-119">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="a4407-120">**İade siparişi oluştur** formunda, bir müşteri hesabı seçin ve ardından **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4407-120">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="a4407-121">**İade siparişi - RMA numarası: %1, %2** formunda bir madde seçin ve sonra **Miktar** alanına negatif bir miktar girin.</span><span class="sxs-lookup"><span data-stu-id="a4407-121">In the **Return order - RMA number: %1, %2** form, select an item, and then enter a negative quantity in the **Quantity** field.</span></span>

5.  <span data-ttu-id="a4407-122">**Satır ayrıntıları** hızlı sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4407-122">Click the **Line details** FastTab.</span></span>

6.  <span data-ttu-id="a4407-123">**Genel** sekmesinde, **İade maliyet fiyatı** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a4407-123">On the **General** tab, enter a value in the **Return cost price** field.</span></span> <span data-ttu-id="a4407-124">Bu değer mallar stoğa iade edildiğinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a4407-124">This value is used when the goods are returned to inventory.</span></span> <span data-ttu-id="a4407-125">Bir değer girmezseniz, mallar stoğa iade edildiğinde geçerli maliyet fiyatı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a4407-125">If you do not enter a value, the current cost price is used when the goods are returned to inventory.</span></span>

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a><span data-ttu-id="a4407-126">Yöntem 2: Maliyet fiyatının otomatik olarak müşteri fatura satırına bağlı olarak oluştur</span><span class="sxs-lookup"><span data-stu-id="a4407-126">Method 2: Automatically generate the cost price based on the customer invoice line</span></span>

<span data-ttu-id="a4407-127">İade satırları oluşturmak için tercih edilen yöntem budur.</span><span class="sxs-lookup"><span data-stu-id="a4407-127">This is the preferred method to use to create return lines.</span></span> <span data-ttu-id="a4407-128">Ürünleri müşteriye sattığınız andaki ürün maliyetini kullanmak için bir iade siparişi oluşturun ve iade edilecek bir satış satırı belirtin.</span><span class="sxs-lookup"><span data-stu-id="a4407-128">To use the cost of the products at the time when you sold the products to the customer, create a return order and specify a sales line to return.</span></span>

1.  <span data-ttu-id="a4407-129">**Satış ve pazarlama** \> **Genel** \> **İade siparişleri** \> **Tüm iade siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4407-129">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="a4407-130">**Eylem bölmesinde** **Yeni** grubunda **İade siparişi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4407-130">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="a4407-131">**İade siparişi oluştur** formunda, bir müşteri hesabı seçin ve ardından **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4407-131">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="a4407-132">**İade siparişi - RMA numarası: %1, %2** formunda, **Eylem Bölmesinde**, **Satış siparişini bul**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4407-132">In the **Return order - RMA number: %1, %2** form, on the **Action Pane**, click **Find sales order**.</span></span>

5.  <span data-ttu-id="a4407-133">**Satış siparişini bul** formunda, iade edilecek fatura satırını seçin ve **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4407-133">In the **Find sales order** form, select the invoice line to return, and then click **OK**.</span></span>
    
    <span data-ttu-id="a4407-134">**Genel** sekmesindeki **Satır ayrıntıları** hızlı sekmesinde **İade lot kodu** alanı orijinal satış satırındaki değeri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a4407-134">On the **Line details** FastTab, on the **General** tab, the **Return lot ID** field displays the value from the original sales line.</span></span> <span data-ttu-id="a4407-135">Ayrıca, **İade maliyet fiyatı** alanı orijinal satış satırındaki maliyet değerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a4407-135">Additionally, the **Return cost price** field displays the cost value from the original sales line.</span></span>

## <a name="cost-calculation-example"></a><span data-ttu-id="a4407-136">Maliyet hesaplama örneği</span><span class="sxs-lookup"><span data-stu-id="a4407-136">Cost calculation example</span></span>

<span data-ttu-id="a4407-137">İade maliyet fiyatını belirtmek için bir iade siparişi satırındaki **İade lot kodu** alanını kullandığınızda, iade siparişi satırındaki maliyet kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a4407-137">When you use the **Return lot ID** field on a return order line to specify the return cost price, the cost on the return order line is used.</span></span> <span data-ttu-id="a4407-138">Stok kapatma veya yeniden hesaplama işlevini çalıştırdığınızda, maliyet orijinal satış satırında ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="a4407-138">If you run the inventory close or recalculation functionality, the cost is adjusted on the original sales line.</span></span> <span data-ttu-id="a4407-139">İade siparişi satırındaki maliyet otomatik olarak parça başına aynı maliyeti yansıtacak şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="a4407-139">The cost on the return order line is automatically adjusted to reflect the same cost per piece.</span></span>

1.  <span data-ttu-id="a4407-140">Test adında bir ürün oluşturun ve serbest bırakın.</span><span class="sxs-lookup"><span data-stu-id="a4407-140">Create and release a product that is named Test.</span></span> <span data-ttu-id="a4407-141">**Serbest bırakılan ürün ayrıntıları** formunda, aşağıdaki bilgileri belirtin:</span><span class="sxs-lookup"><span data-stu-id="a4407-141">In the **Released product details** form, specify the following information:</span></span>
    
    1.  <span data-ttu-id="a4407-142">**Maliyetleri yönet** hızlı sekmesinde, **Madde grubu** alanında **Parçalar** grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="a4407-142">On the **Manage costs** FastTab, in the **Item group** field, select the **Parts** group.</span></span>
    
    2.  <span data-ttu-id="a4407-143">**Genel** hızlı sekmesinde, **Madde model grubu** alanında **DEF**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a4407-143">On the **General** FastTab, in the **Item model group** field, select **DEF**.</span></span>
    
    3.  <span data-ttu-id="a4407-144">**Satınalma** hızlı sekmesinde **Fiyat** alanına maddenin maliyet fiyatı olarak 10,00 yazın.</span><span class="sxs-lookup"><span data-stu-id="a4407-144">On the **Purchase** FastTab, in the **Price** field, type 10.00 as the cost price of the item.</span></span>
    
    4.  <span data-ttu-id="a4407-145">**Eylem Bölmesi**'nde **Boyut grupları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4407-145">On the **Action Pane**, click **Dimension groups**.</span></span> <span data-ttu-id="a4407-146">**Depolama boyutu grubu** alanında **Yalnızca Tesis ve Ambar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a4407-146">In the **Storage dimension group** field, select **Site and Warehouse only**.</span></span> <span data-ttu-id="a4407-147">**İzleme boyutu grubu** alanında **Etkin olmayan izleme boyutları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a4407-147">In the **Tracking dimension group** field, select **No active tracking dimensions**.</span></span>

2.  <span data-ttu-id="a4407-148">Parça başına 6,00 fiyatla Test maddesi için 10 parçalık bir satınalma siparişi oluşturun ve ardından satınalma siparişine ait faturayı deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="a4407-148">Create a purchase order for 10 pieces of the Test item at 6.00 per piece, and then post an invoice for the purchase order.</span></span>
    
    <span data-ttu-id="a4407-149">Parça başına 8,00 fiyatla Test maddesi için 10 parçalık ikinci bir satınalma siparişi oluşturun ve ardından satınalma siparişine ait faturayı deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="a4407-149">Create a second purchase order for 10 pieces of the Test item at 8.00 per piece, and then post an invoice for the purchase order.</span></span>

3.  <span data-ttu-id="a4407-150">Test maddesinden beş parça satış yapmak için satış siparişine ait faturayı deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="a4407-150">Post an invoice for a sales order to sell five pieces of the Test item.</span></span>
    
    <span data-ttu-id="a4407-151">Bu durumda, satış siparişi satırı maliyeti 35,00 olur (5 parça \*7,00 parça başına ortalama maliyet).</span><span class="sxs-lookup"><span data-stu-id="a4407-151">In this case, the sales order line is costed at 35.00 (5 pieces \* 7.00 average cost per piece).</span></span>

4.  <span data-ttu-id="a4407-152">Müşteri için yeni bir iade siparişi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a4407-152">Create a return order for the customer.</span></span> <span data-ttu-id="a4407-153">**Satış siparişini bul** formunda, fatura satırını seçin ve **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4407-153">In the **Find sales order** form, select the invoice line, and then click **OK**.</span></span>

5.  <span data-ttu-id="a4407-154">**İade emri - RMA numarası: %1, %2** formunda, Test maddesini iade etmek için iade siparişi oluşturulduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="a4407-154">In the **Return order - RMA number: %1, %2** form, verify that a return order is generated to return the Test item.</span></span> <span data-ttu-id="a4407-155">İade siparişi miktarı -5,00 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="a4407-155">The quantity of the return order is set to -5.00.</span></span>
    
    <span data-ttu-id="a4407-156">**İade lot kodu** alanında bir lot kodu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="a4407-156">The **Return lot ID** field displays a lot ID.</span></span> <span data-ttu-id="a4407-157">Bu lot kodu, müşteriye satılan maddenin orijinal satış siparişinden alınır.</span><span class="sxs-lookup"><span data-stu-id="a4407-157">This lot ID is taken from the original sales order of the item that was sold to the customer.</span></span> <span data-ttu-id="a4407-158">**İade maliyet fiyatı** alanı orijinal satış satırındaki maliyet fiyatını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a4407-158">The **Return cost price** field displays the cost price from the original sales line.</span></span>

6.  <span data-ttu-id="a4407-159">İade edilen maddelerin girişini kaydedin.</span><span class="sxs-lookup"><span data-stu-id="a4407-159">Register the receipt of the returned items.</span></span>

7.  <span data-ttu-id="a4407-160">İade edilen maddelerin sevk irsaliyesini deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="a4407-160">Post a packing slip for the returned items.</span></span>

8.  <span data-ttu-id="a4407-161">İade sipariş için faturayı deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="a4407-161">Post an invoice for the return order.</span></span> <span data-ttu-id="a4407-162">**Tüm satış siparişleri** liste sayfasında, sipariş türünün **İade siparişi** olduğu bir satış siparişi seçin.</span><span class="sxs-lookup"><span data-stu-id="a4407-162">On the **All sales orders** list page, select a sales order for which **Returned order** is the order type.</span></span>

9.  <span data-ttu-id="a4407-163">**Stok hareketleri** formunu açın.</span><span class="sxs-lookup"><span data-stu-id="a4407-163">Open the **Inventory transactions** form.</span></span> <span data-ttu-id="a4407-164">İadenin parça başına maliyetinin 7.00 olduğunu **İade maliyet fiyatı** alanındaki değeri kullanarak doğrulayın. **Maliyet tutarı** alanındaki toplam 35,00 olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a4407-164">Verify that the return is costed at 7.00 per piece by using the value in the **Return cost price** field, for a total of 35.00 in the **Cost amount** field.</span></span> <span data-ttu-id="a4407-165">**İade siparişi - RMA numarası: %1, %2** formundan **Stok hareketleri** formunu açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4407-165">You can open the **Inventory transactions** form from the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="a4407-166">**Satırlar** ızgarasında **Stok** \> **Hareketler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4407-166">In the **Lines** grid, click **Inventory** \> **Transactions**.</span></span>

10. <span data-ttu-id="a4407-167">Stok ve ambar yönetiminde **Kapanış ve düzeltme** formunu kullanarak **3. Kapat** yordamını çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="a4407-167">In Inventory and warehouse management, use the **Closing and adjustment** form to run the **3. Close** procedure.</span></span>
    
    <span data-ttu-id="a4407-168">Bu eylem orijinal satış satırında -35,00 olan maliyeti (5 parça \*7,00) -30,00 (5 parça \*6,00) olarak düzeltir.</span><span class="sxs-lookup"><span data-stu-id="a4407-168">This action adjusts the cost on the original sales line that was costed at -35.00 (5 pieces \* 7.00) to -30.00 (5 pieces \* 6.00).</span></span> <span data-ttu-id="a4407-169">Bunun nedeki stok model grubunun ilk giren ilk çıkar (FIFO) kullanması ve parça başına 6,00'ın ilk satınalma siparişindeki FIFO maliyeti olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="a4407-169">This is because the inventory model group uses First in, First out (FIFO), and 6.00 per piece is the FIFO cost from the first purchase order.</span></span> <span data-ttu-id="a4407-170">Ek olarak, eylem iade satış satırındaki maliyeti orijinal satış satırındaki parça başına maliyetle eşleşecek şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a4407-170">Additionally, the action adjusts the cost on the return sales line to match the cost per piece on the original sales line.</span></span> <span data-ttu-id="a4407-171">Bu nedenle, iade satırındaki maliyet 35,00 yerine 30,00 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="a4407-171">Therefore, the cost of the return line is adjusted from 35.00 to 30.00.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]