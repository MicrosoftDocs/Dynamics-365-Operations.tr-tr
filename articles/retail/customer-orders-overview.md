---
title: "Müşteri siparişlerine genel bakış"
description: "Bu konu, Perakende Modern POS (MPOS) içerisindeki müşteri siparişleri hakkında bilgi sağlar. Müşteri siparişleri, özel siparişler olarak da adlandırılır. Bu konu, ilgili parametreler ve hareket akışları hakkında bir tartışma içerir."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ce6774ede836eb29e6ef2cd8d4baa9efb931020c
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="customer-orders-overview"></a><span data-ttu-id="b19ca-105">Müşteri siparişlerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="b19ca-105">Customer orders overview</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="b19ca-106">Bu konu, Perakende Modern POS (MPOS) içerisindeki müşteri siparişleri hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="b19ca-106">This topic provides information about customer orders in Retail Modern POS (MPOS).</span></span> <span data-ttu-id="b19ca-107">Müşteri siparişleri, özel siparişler olarak da adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="b19ca-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="b19ca-108">Bu konu, ilgili parametreler ve hareket akışları hakkında bir tartışma içerir.</span><span class="sxs-lookup"><span data-stu-id="b19ca-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="b19ca-109">Çok kanallı perakende dünyasında pek çok perakendeci, çeşitli ürün ve yerine getirme gereksinimlerini karşılamak için müşteri siparişleri seçeneği veya özel siparişler sağlar.</span><span class="sxs-lookup"><span data-stu-id="b19ca-109">In an omni-channel retail world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="b19ca-110">Burada bazı tipik senaryolar vardır:</span><span class="sxs-lookup"><span data-stu-id="b19ca-110">Here are some typical scenarios:</span></span>

-   <span data-ttu-id="b19ca-111">Bir müşteri, ürünler belirli bir tarihte belirli bir adrese teslim edilmesini istiyor.</span><span class="sxs-lookup"><span data-stu-id="b19ca-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
-   <span data-ttu-id="b19ca-112">Bir müşteri, ürünleri, müşterinin satın aldığı mağazadan başka bir konumda bulunan bir mağazadan teslim almak istiyor.</span><span class="sxs-lookup"><span data-stu-id="b19ca-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
-   <span data-ttu-id="b19ca-113">Bir müşteri, müşterinin satın aldığı ürünleri bir başkasının teslim almasını istiyor.</span><span class="sxs-lookup"><span data-stu-id="b19ca-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="b19ca-114">Ayrıca, perakendeciler müşteri siparişlerini, aksi takdirde stok kesintilerinin ortaya çıkabileceği kayıp satışları en aza indirmek için kullanır, çünkü ürünler farklı bir zaman veya yerde teslim edilebilir veya çekilebilir.</span><span class="sxs-lookup"><span data-stu-id="b19ca-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="b19ca-115">Müşteri siparişleri ayarlamak</span><span class="sxs-lookup"><span data-stu-id="b19ca-115">Set up customer orders</span></span>
<span data-ttu-id="b19ca-116">Müşteri siparişlerinin nasıl karşılandıklarını tanımlamak için **Perakende parametreleri** sayfası üzerinde ayarlanabilecek bazı parametrelerin bunlardır:</span><span class="sxs-lookup"><span data-stu-id="b19ca-116">Here are some of the parameters that can be set on the **Retail parameters** page to define how customer orders are fulfilled:</span></span>

-   <span data-ttu-id="b19ca-117">**Varsayılan depozito yüzdesi** – Siparişin onaylanabilmesi için önce müşterinin ödemesi gereken depozito tutarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b19ca-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="b19ca-118">Varsayılan depozito tutarı, sipariş değerinin bir yüzdesi olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="b19ca-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="b19ca-119">Ayrıcalıklara bağlı olarak bir mağaza yetkilisi tutarı **Depozito geçersiz kılma** kullanarak geçersiz kılabilir.</span><span class="sxs-lookup"><span data-stu-id="b19ca-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
-   <span data-ttu-id="b19ca-120">**İptal ücreti yüzdesi** – Müşteri siparişi iptal edildiğinde, bir kesinti uygulanacaksa bu giderin tutarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b19ca-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
-   <span data-ttu-id="b19ca-121">**İptal masrafı kodu** – Müşteri siparişi iptal edildiğinde bir masraf uygulanacaksa, bu masraf masraf kodu altında yansıtılacaktır.</span><span class="sxs-lookup"><span data-stu-id="b19ca-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="b19ca-122">İptal masrafı kodu tanımlamak için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="b19ca-122">Use this parameter to define the cancellation charge code.</span></span>
-   <span data-ttu-id="b19ca-123">**Kargo masrafı kodu** – Perakendeciler malları müşteriye sevk etmek için ek bir masraf kesebilirler.</span><span class="sxs-lookup"><span data-stu-id="b19ca-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="b19ca-124">Bu sevkiyat masrafının tutarı, masraf kodu altında yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="b19ca-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="b19ca-125">Bu parametreyi, sevkiyat masraf kodunu müşteri siparişi üzerindeki sevkiyat masrafları ile eşleştirmek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="b19ca-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
-   <span data-ttu-id="b19ca-126">**İade kargo ücretleri** – Müşteri siparişi ile ilişkili sevkiyat masraflarının iade edilip edilemeyeceğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="b19ca-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
-   <span data-ttu-id="b19ca-127">**Onayı olmadan maksimum tutar** – Sevkiyat masrafları iade edilebilirse, iade siparişleri arasında iade edilebilecek maksimum tutarı belirtin.</span><span class="sxs-lookup"><span data-stu-id="b19ca-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="b19ca-128">Bu tutar aşılırsa, iade ile devam etmek için yönetici tarafından geçersiz kılma gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b19ca-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="b19ca-129">Aşağıdaki senaryolara karşılık verebilmek için sevkiyat masraflarının iadesi, ilk olarak ödenen tutarı geçebilir:</span><span class="sxs-lookup"><span data-stu-id="b19ca-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>
    -   <span data-ttu-id="b19ca-130">Masraflar, satış siparişi üstbilgisi seviyesinde uygulanır ve ürün satırının bir miktarı iade edildiğinde, ürünler için izin verilen sevkiyat masrafının maksimum iadesi ve miktar, tüm perakende müşterileri için geçerli olacak bir şekilde belirlenemez.</span><span class="sxs-lookup"><span data-stu-id="b19ca-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all retail customers.</span></span>
    -   <span data-ttu-id="b19ca-131">Sevkiyat giderleri her sevkiyat örneği için alınır.</span><span class="sxs-lookup"><span data-stu-id="b19ca-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="b19ca-132">Bir müşteri, ürünleri birden fazla defa iade ederse ve perakendecinin ilkesi, iade sevkiyatı masraflarının karşılanacağını belirtiyorsa, iade sevkiyatı masrafları, gerçek sevkiyat masraflarından fazla olacaktır.</span><span class="sxs-lookup"><span data-stu-id="b19ca-132">If a customer returns products multiple times, and the retailer’s policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="b19ca-133">Müşteri siparişleri için hareket akışı</span><span class="sxs-lookup"><span data-stu-id="b19ca-133">Transaction flow for customer orders</span></span>
### <a name="create-a-customer-order-in-retail-modern-pos"></a><span data-ttu-id="b19ca-134">Perakende Modern POS'ta bir müşteri siparişi oluştur</span><span class="sxs-lookup"><span data-stu-id="b19ca-134">Create a customer order in Retail Modern POS</span></span>

1.  <span data-ttu-id="b19ca-135">Harekete bir müşteri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b19ca-135">Add a customer to the transaction.</span></span>
2.  <span data-ttu-id="b19ca-136">Sepete ürünler ekle.</span><span class="sxs-lookup"><span data-stu-id="b19ca-136">Add products to the cart.</span></span>
3.  <span data-ttu-id="b19ca-137">**Müşteri siparişi oluştur** üzerine tıklayın ve daha sonra sipariş türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="b19ca-137">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="b19ca-138">Sipariş türü **Müşteri siparişi** veya **Teklif** olabilir.</span><span class="sxs-lookup"><span data-stu-id="b19ca-138">The order type can be either **Customer order** or **Quote**.</span></span>
4.  <span data-ttu-id="b19ca-139">**Seçileni sevk et** veya **Tümünü sevk et** üzerine tıklayarak müşteri hesabındaki bir adrese ürünleri sevk edin, istenen sevkiyat tarihini belirtin ve sevkiyat masraflarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b19ca-139">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5.  <span data-ttu-id="b19ca-140">Geçerli mağazadan veya başka bir mağazadan belirli bir tarihte çekilecek ürünleri seçmek için **Seçileni çek** veya **Hepsini çek** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b19ca-140">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6.  <span data-ttu-id="b19ca-141">Depozito gerekiyorsa, depozito tutarını tahsil edin.</span><span class="sxs-lookup"><span data-stu-id="b19ca-141">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="b19ca-142">Geçerli bir müşteri siparişini düzenle</span><span class="sxs-lookup"><span data-stu-id="b19ca-142">Edit an existing customer order</span></span>

1.  <span data-ttu-id="b19ca-143">Giriş sayfasında **Bir siparişi bul** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b19ca-143">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="b19ca-144">Düzenlemek için siparişi bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b19ca-144">Find and select the order to edit.</span></span> <span data-ttu-id="b19ca-145">Sayfanın altında, **Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b19ca-145">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="b19ca-146">Bir siparişi çekmek</span><span class="sxs-lookup"><span data-stu-id="b19ca-146">Pick up an order</span></span>

1.  <span data-ttu-id="b19ca-147">Giriş sayfasında **Bir siparişi bul** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b19ca-147">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="b19ca-148">Çekilecek siparişi seçin.</span><span class="sxs-lookup"><span data-stu-id="b19ca-148">Select the order to pick up.</span></span> <span data-ttu-id="b19ca-149">Sayfanın altında, **Çekme ve paketleme**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b19ca-149">At the bottom of the page, click **Picking and packing**.</span></span>
3.  <span data-ttu-id="b19ca-150">**Çekme** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b19ca-150">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="b19ca-151">Bir siparişi iptal edin</span><span class="sxs-lookup"><span data-stu-id="b19ca-151">Cancel an order</span></span>

1.  <span data-ttu-id="b19ca-152">Giriş sayfasında **Bir siparişi bul** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b19ca-152">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="b19ca-153">İptal edilecek siparişi seçin.</span><span class="sxs-lookup"><span data-stu-id="b19ca-153">Select the order to cancel.</span></span> <span data-ttu-id="b19ca-154">Sayfanın altında, **İptal**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b19ca-154">At the bottom of the page, click **Cancel**.</span></span>

#### <a name="create-a-return-order"></a><span data-ttu-id="b19ca-155">Sipariş iadesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b19ca-155">Create a return order</span></span>

1.  <span data-ttu-id="b19ca-156">Giriş sayfasında **Bir siparişi bul** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b19ca-156">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="b19ca-157">İade edilecek siparişi seçin, siparişin faturasını seçin ve daha sonra iade edilecek ürünler için ürün satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="b19ca-157">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3.  <span data-ttu-id="b19ca-158">Sayfanın altında, **Siparişi iade et**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b19ca-158">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="b19ca-159">Müşteri siparişleri için zaman uyumsuz işlem akışı</span><span class="sxs-lookup"><span data-stu-id="b19ca-159">Asynchronous transaction flow for customer orders</span></span>
<span data-ttu-id="b19ca-160">Müşteri siparişleri satış noktası (POS) istemcisinden zaman uyumlu ya da zaman uyumsuz modda oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="b19ca-160">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="b19ca-161">Müşteri siparişlerinin zaman uyumsuz modunda oluşturulmasını etkinleştirin</span><span class="sxs-lookup"><span data-stu-id="b19ca-161">Enable customer orders to be created in asynchronous mode</span></span>

1.  <span data-ttu-id="b19ca-162">**Perakende** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS profili** &gt; **İşlev profilleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b19ca-162">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2.  <span data-ttu-id="b19ca-163">**Genel** hızlı sekmesi üzerinde, **Müşteri siparişlerini zaman uyumsuz modda oluştur** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b19ca-163">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="b19ca-164">**Müşteri siparişlerini zaman uyumsuz moda oluştur** seçeneği **Evet** olarak ayarlanmışsa, müşteri siparişleri her defasında zaman uyumsuz modda oluşturulur, Perakende İşlem Hizmeti (RTS) etkin olsa bile.</span><span class="sxs-lookup"><span data-stu-id="b19ca-164">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="b19ca-165">Bu seçeneği **Hayır** olarak ayarlarsanız, müşteri siparişleri her defasında zaman uyumlu modda RTS kullanarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b19ca-165">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="b19ca-166">Müşteri siparişleri zaman uyumsuz modda oluşturulduklarında, Retail içerisine Çekme (P) işleri ile çekilir ve eklenir.</span><span class="sxs-lookup"><span data-stu-id="b19ca-166">When customer orders are created in asynchronous mode, they are pulled and inserted into Retail by Pull (P) jobs.</span></span> <span data-ttu-id="b19ca-167">Karşılık gelen satış siparişleri, Retail içerisinde **Senkronizasyon siparişleri** elle veya toplu bir iş aracılığıyla çalıştırıldıklarında oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b19ca-167">The corresponding sales orders are created in Retail when **Synchronize orders** is run either manually or through a batch process.</span></span>

<a name="see-also"></a><span data-ttu-id="b19ca-168">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="b19ca-168">See also</span></span>
--------

[<span data-ttu-id="b19ca-169">Karma müşteri siparişleri</span><span class="sxs-lookup"><span data-stu-id="b19ca-169">Hybrid customer orders</span></span>](hybrid-customer-orders.md)




