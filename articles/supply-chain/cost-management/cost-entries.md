---
title: Maliyet girişleri
description: Bu makalede, maliyeti girişleri ve ne zaman oluşturuldukları hakkında bilgiler verilmektedir. Maliyet girişi, belirli bir etkinliğin miktarının ve maliyetinin yazıldığı bir kayıttır.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 12ff771cf44595420ca721605daabaa6b071a4ff
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967840"
---
# <a name="cost-entries"></a><span data-ttu-id="16a97-104">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="16a97-104">Cost entries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16a97-105">Bu makalede, maliyeti girişleri ve ne zaman oluşturuldukları hakkında bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="16a97-105">This article provides information about cost entries and when they are created.</span></span> <span data-ttu-id="16a97-106">Maliyet girişi, belirli bir etkinliğin miktarının ve maliyetinin yazıldığı bir kayıttır.</span><span class="sxs-lookup"><span data-stu-id="16a97-106">A cost entry is a record that registers the quantity and cost of a given event.</span></span>

<span data-ttu-id="16a97-107">Maliyet girişleri, etkin mali stok boyutlarında kaydedilen stok hareketlerinin toplamıdır.</span><span class="sxs-lookup"><span data-stu-id="16a97-107">Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.</span></span>

## <a name="examples"></a><span data-ttu-id="16a97-108">Örnekler</span><span class="sxs-lookup"><span data-stu-id="16a97-108">Examples</span></span>
### <a name="example-1-no-cost-entries-are-created"></a><span data-ttu-id="16a97-109">Örnek 1: Hiç maliyet girişi oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="16a97-109">Example 1: No cost entries are created</span></span>

<span data-ttu-id="16a97-110">Bir transfer günlüğü olayı kaydedilmiştir.</span><span class="sxs-lookup"><span data-stu-id="16a97-110">A transfer journal event is registered.</span></span> <span data-ttu-id="16a97-111">Olay, bir parça A maddesini A konumundan B konumuna transfer ediyor. Konum stok boyutu, maliyet nesnesinin bir parçası olarak değerlendirilmez.</span><span class="sxs-lookup"><span data-stu-id="16a97-111">The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object.</span></span> <span data-ttu-id="16a97-112">Bu nedenle, olay iki stok hareketi oluşturur; maliyet girişi oluşturmaz.</span><span class="sxs-lookup"><span data-stu-id="16a97-112">Therefore, the event creates two inventory transactions and no cost entries.</span></span>

### <a name="example-2-cost-entries-are-created"></a><span data-ttu-id="16a97-113">Örnek 2: Maliyet girişleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="16a97-113">Example 2: Cost entries are created</span></span>

<span data-ttu-id="16a97-114">Bir transfer günlüğü olayı kaydedilmiştir.</span><span class="sxs-lookup"><span data-stu-id="16a97-114">A transfer journal event is registered.</span></span> <span data-ttu-id="16a97-115">Olay bir madde parasını 1. siteden 2. siteye aktarır.</span><span class="sxs-lookup"><span data-stu-id="16a97-115">The event transfers one piece of item A from site 1 to site 2.</span></span> <span data-ttu-id="16a97-116">Site stok boyutu, maliyet nesnenin bir parçası olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="16a97-116">The Site inventory dimension is considered part of the cost object.</span></span> <span data-ttu-id="16a97-117">Bu nedenle, olay iki stok hareketi ve iki maliyet girişi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16a97-117">Therefore, the event creates two inventory transactions and two cost entries.</span></span>

### <a name="example-3-one-cost-entry-is-created"></a><span data-ttu-id="16a97-118">Örnek 3: Bir maliyet girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="16a97-118">Example 3: One cost entry is created</span></span>

<span data-ttu-id="16a97-119">Bir satınalma siparişi için bir ürün giriş olayı kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="16a97-119">A product receipt event is registered for a purchase order.</span></span> <span data-ttu-id="16a97-120">Olay 100 parça A maddesini 10,00 dolarlık (ABD) bir maliyet birimiyle kaydeder.</span><span class="sxs-lookup"><span data-stu-id="16a97-120">The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD).</span></span> <span data-ttu-id="16a97-121">A maddesi, stok yönetimi amacını izlemek üzere, alınan her bir madde için oluşturulan benzersiz bir seri numarası kullanır.</span><span class="sxs-lookup"><span data-stu-id="16a97-121">Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received.</span></span> <span data-ttu-id="16a97-122">Bu nedenle, olay 100 stok hareketi ve 1 maliyet girişi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16a97-122">Therefore, the event creates 100 inventory transactions and one cost entry.</span></span>

## <a name="cost-entries-page"></a><span data-ttu-id="16a97-123">Maliyet girişleri sayfası</span><span class="sxs-lookup"><span data-stu-id="16a97-123">Cost entries page</span></span>
<span data-ttu-id="16a97-124">Yeni **Maliyet girişleri** sayfası, miktar ve maliyet kayıtlarını görüntüleyip kontrol etmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="16a97-124">The new **Cost entries** page lets you view and control registrations of quantities and costs.</span></span> <span data-ttu-id="16a97-125">Bu sayfa, **Stok hareketi** ve **Stok kapatma** sayfalarını tamamlar.</span><span class="sxs-lookup"><span data-stu-id="16a97-125">This page complements the **Inventory transaction** and **Inventory settlement** pages.</span></span> <span data-ttu-id="16a97-126">Bir olay için kayıtlar kronolojik sırayla kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="16a97-126">Records are registered in chronological order for an event.</span></span> <span data-ttu-id="16a97-127">Bu sayede, bir belgeyle ilgili belirli bir olayın veya tüm olayların birikmiş maliyetlerini hızla bulup kontrol edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16a97-127">Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document.</span></span> <span data-ttu-id="16a97-128">Aşağıda bir örnek verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="16a97-128">Here is an example:</span></span>

-   <span data-ttu-id="16a97-129">A maddesi için bir ürün giriş olayı kaydedilmiştir. 10,00 dolar birim maliyetiyle yüz parça alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="16a97-129">A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.</span></span>
-   <span data-ttu-id="16a97-130">Fatura olayı kaydedildikten birkaç gün sonra maliyet 11,00 dolara çıkmıştır.</span><span class="sxs-lookup"><span data-stu-id="16a97-130">A few days after the invoice event is registered, the cost increases to 11.00 USD.</span></span> <span data-ttu-id="16a97-131">Böylece, toplam tutar 1.100 dolar olur.</span><span class="sxs-lookup"><span data-stu-id="16a97-131">Therefore, the total amount is 1,100 USD.</span></span> <span data-ttu-id="16a97-132">100 dolarlık farkı hesaba katmak için ikinci bir fiş oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="16a97-132">A second voucher is created to account for the difference of 100 USD.</span></span>
-   <span data-ttu-id="16a97-133">Birkaç gün sonra, satınalma siparişine, ulaştırma maliyetini kapsayan 15,00 dolarlık bir sair gider kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="16a97-133">A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.</span></span>

| <span data-ttu-id="16a97-134">Fiş</span><span class="sxs-lookup"><span data-stu-id="16a97-134">Voucher</span></span> | <span data-ttu-id="16a97-135">Tarih</span><span class="sxs-lookup"><span data-stu-id="16a97-135">Date</span></span>       | <span data-ttu-id="16a97-136">Referans</span><span class="sxs-lookup"><span data-stu-id="16a97-136">Reference</span></span>      | <span data-ttu-id="16a97-137">Sayı</span><span class="sxs-lookup"><span data-stu-id="16a97-137">Number</span></span> | <span data-ttu-id="16a97-138">Lot kodu</span><span class="sxs-lookup"><span data-stu-id="16a97-138">Lot ID</span></span>  | <span data-ttu-id="16a97-139">Miktar</span><span class="sxs-lookup"><span data-stu-id="16a97-139">Quantity</span></span> | <span data-ttu-id="16a97-140">Tutar</span><span class="sxs-lookup"><span data-stu-id="16a97-140">Amount</span></span>  |
|---------|------------|----------------|--------|---------|---------------|----|
| <span data-ttu-id="16a97-141">00001</span><span class="sxs-lookup"><span data-stu-id="16a97-141">00001</span></span>   | <span data-ttu-id="16a97-142">01-01-2015</span><span class="sxs-lookup"><span data-stu-id="16a97-142">01-01-2015</span></span> | <span data-ttu-id="16a97-143">Satın alma siparişi</span><span class="sxs-lookup"><span data-stu-id="16a97-143">Purchase order</span></span> | <span data-ttu-id="16a97-144">100001</span><span class="sxs-lookup"><span data-stu-id="16a97-144">100001</span></span> | <span data-ttu-id="16a97-145">0000101</span><span class="sxs-lookup"><span data-stu-id="16a97-145">0000101</span></span> | <span data-ttu-id="16a97-146">100,00</span><span class="sxs-lookup"><span data-stu-id="16a97-146">100.00</span></span>   | <span data-ttu-id="16a97-147">1000,00</span><span class="sxs-lookup"><span data-stu-id="16a97-147">1000.00</span></span> |
| <span data-ttu-id="16a97-148">00002</span><span class="sxs-lookup"><span data-stu-id="16a97-148">00002</span></span>   | <span data-ttu-id="16a97-149">20-01-2015</span><span class="sxs-lookup"><span data-stu-id="16a97-149">20-01-2015</span></span> | <span data-ttu-id="16a97-150">Satın alma siparişi</span><span class="sxs-lookup"><span data-stu-id="16a97-150">Purchase order</span></span> | <span data-ttu-id="16a97-151">100001</span><span class="sxs-lookup"><span data-stu-id="16a97-151">100001</span></span> | <span data-ttu-id="16a97-152">0000101</span><span class="sxs-lookup"><span data-stu-id="16a97-152">0000101</span></span> |          | <span data-ttu-id="16a97-153">100,00</span><span class="sxs-lookup"><span data-stu-id="16a97-153">100.00</span></span>  |
| <span data-ttu-id="16a97-154">00003</span><span class="sxs-lookup"><span data-stu-id="16a97-154">00003</span></span>   | <span data-ttu-id="16a97-155">31-01-2015</span><span class="sxs-lookup"><span data-stu-id="16a97-155">31-01-2015</span></span> | <span data-ttu-id="16a97-156">Ayarlama</span><span class="sxs-lookup"><span data-stu-id="16a97-156">Adjustment</span></span>     | <span data-ttu-id="16a97-157">100001</span><span class="sxs-lookup"><span data-stu-id="16a97-157">100001</span></span> | <span data-ttu-id="16a97-158">0000101</span><span class="sxs-lookup"><span data-stu-id="16a97-158">0000101</span></span> |          | <span data-ttu-id="16a97-159">15,00</span><span class="sxs-lookup"><span data-stu-id="16a97-159">15.00</span></span>   |

<span data-ttu-id="16a97-160">**Maliyet girişleri** sayfası, belge numarasına ve belge tarihine göre filtrelemeye olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="16a97-160">The **Cost entries** page enables filtering by document ID and document date.</span></span> 

> [!NOTE]
> <span data-ttu-id="16a97-161">Maliyet girişleri yalnızca [maliyet nesneleri](cost-object.md) veya serbest bırakılan ürünler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="16a97-161">Cost entries are available only for [cost objects](cost-object.md) or released products.</span></span>

<a name="additional-resources"></a><span data-ttu-id="16a97-162">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="16a97-162">Additional resources</span></span>
--------

[<span data-ttu-id="16a97-163">Maliyet nesneleri</span><span class="sxs-lookup"><span data-stu-id="16a97-163">Cost objects</span></span>](cost-object.md)



