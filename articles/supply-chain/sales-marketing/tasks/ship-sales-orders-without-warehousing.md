--- 
title: "Satış siparişlerini ambarlama olmadan sevk etme"
description: "Bu kılavuz, ürünler müşteriye sevk edildiğinde bir satış siparişinin nasıl güncelleştireceğini açıklamaktadır."
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 16feadb3a2e30e3400d85829c73f6f20780e7b71
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="968cf-103">Satış siparişlerini ambarlama olmadan sevk etme</span><span class="sxs-lookup"><span data-stu-id="968cf-103">Ship sales orders without warehousing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="968cf-104">Bu kılavuz, ürünler müşteriye sevk edildiğinde bir satış siparişinin nasıl güncelleştireceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="968cf-104">This guide demonstrates how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="968cf-105">Kılavuz, ambar yönetimi (temel veya gelişmiş depolama) için ayarlanmamış olan karşılama akışı için geçerlidir ve bu nedenle ürün çekme işleminin sevkiyat öncesinde kaydedilmesini gerektirmez.</span><span class="sxs-lookup"><span data-stu-id="968cf-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="968cf-106">Bu yordamı, kendi verilerinizle veya USMF demo verisi şirketin çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="968cf-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="968cf-107">Her iki durumda da, bu göreve başlamadan önce stoklanmış bir ürünün, 1'den büyük bir miktar ile bir satış siparişini oluşturun.</span><span class="sxs-lookup"><span data-stu-id="968cf-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="968cf-108">Bir deftere nakil hatasını önlemek için ürünün siparişte seçmiş olduğunuz tesisteki ve ambardaki eldeki miktarının, siparişteki miktarı karşıladığından emin olduğunu kontrol etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="968cf-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you’ve selected on the order covers the order quantity.</span></span>


## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="968cf-109">Sipariş için sevk irsaliyesini deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="968cf-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="968cf-110">Sales and marketing > Sales orders > All sales orders (Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="968cf-110">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="968cf-111">Listede, bu görev için oluşturduğunuz siparişi bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="968cf-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="968cf-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="968cf-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="968cf-113">Eylem Bölmesinde, Çek ve paketle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="968cf-113">On the Action Pane, click Pick and pack.</span></span>
5. <span data-ttu-id="968cf-114">Sevk irsaliyesini deftere naklet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="968cf-114">Click Post packing slip.</span></span>
6. <span data-ttu-id="968cf-115">Parametreler bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="968cf-115">Expand or collapse the Parameters section.</span></span>
7. <span data-ttu-id="968cf-116">Miktar alanında, 'Tümü' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="968cf-116">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="968cf-117">Diğer seçenekler arasında Şimdi teslim et ve Malzeme çekildi bulunur.</span><span class="sxs-lookup"><span data-stu-id="968cf-117">Other options include Deliver now and Picked.</span></span> <span data-ttu-id="968cf-118">Sipariş satırı kısmen sevk edilecek şeklindeyse ve sipariş satırındaki Şimdi teslim et alanında bir miktar belirtilmişse, Şimdi teslim et'i seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="968cf-118">If the order line is to be shipped partially and the Deliver now field on the order line contains a quantity, you would select Deliver now.</span></span> <span data-ttu-id="968cf-119">Malzeme çekme faaliyeti kuruluşunuzun karşılama akışı içerisinde bir malzeme çekme listesiyle yönetilen ve kaydedilen ayrı bir işlem olarak bulunuyorsa, Malzeme çekildi'yi seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="968cf-119">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select Picked.</span></span>  
    * <span data-ttu-id="968cf-120">Deftere nakil seçeneğinin Evet olarak ayarlanmış olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="968cf-120">Check that the Posting option is set to Yes.</span></span>  
8. <span data-ttu-id="968cf-121">Sevk irsaliyesini yazdır seçeneğini Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="968cf-121">Set the Print packing slip option to Yes.</span></span>
    * <span data-ttu-id="968cf-122">Genel bakış sekmesinde bu nakil sırasında oluşturulacak sevk irsaliyelerinin bir listesi bulunur.</span><span class="sxs-lookup"><span data-stu-id="968cf-122">The Overview tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="968cf-123">Tek sipariş gönderiyorsanız, genellikle tek bir sevk irsaliyesi olur.</span><span class="sxs-lookup"><span data-stu-id="968cf-123">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="968cf-124">Ancak, bu siparişlerin satırları farklı tesisler üzerinden sevk edilecekse, deftere nakil işlemi otomatik olarak uygun sayıda belgeye bölünür.</span><span class="sxs-lookup"><span data-stu-id="968cf-124">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="968cf-125">Bu, değiştirilemez zorunlu bir durumdur.</span><span class="sxs-lookup"><span data-stu-id="968cf-125">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="968cf-126">Benzer şekilde, sipariş satırları farklı teslimat adreslerine sevk edilecekse, deftere nakil işlemi yine birden çok belgeye bölünür ve sevkiyat ilkesi bölünme istenecek şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="968cf-126">Similarly, the posting will also be split into multiple documents if the order’s lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
9. <span data-ttu-id="968cf-127">Satırlar sekmesinde, sevk edilecek sipariş satırı için bir satır seçin.</span><span class="sxs-lookup"><span data-stu-id="968cf-127">On the Lines tab, select the row for the order line to be shipped.</span></span>
10. <span data-ttu-id="968cf-128">Güncelleştir alanında orijinal miktardan daha düşük bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="968cf-128">In the Update field, enter a number lower than the original quantity.</span></span>
11. <span data-ttu-id="968cf-129">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="968cf-129">Click OK.</span></span>
12. <span data-ttu-id="968cf-130">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="968cf-130">Click Yes.</span></span>
13. <span data-ttu-id="968cf-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="968cf-131">Close the page.</span></span>
14. <span data-ttu-id="968cf-132">Eylem Bölmesinde, Seçenekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="968cf-132">On the Action Pane, click Options.</span></span>
15. <span data-ttu-id="968cf-133">Görünümü değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="968cf-133">Click Change view.</span></span>
16. <span data-ttu-id="968cf-134">Başlık görünümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="968cf-134">Click Header view.</span></span>
    * <span data-ttu-id="968cf-135">Siparişteki tüm satırlar tamamen sevk edilmişse, sipariş durumu Açık durumundan Teslim edildi'ye değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="968cf-135">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    * <span data-ttu-id="968cf-136">Bu örnekte, sipariş satırı kısmen sevk edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="968cf-136">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="968cf-137">Bu nedenle, sipariş durumu Açık şeklinde kalır.</span><span class="sxs-lookup"><span data-stu-id="968cf-137">This is why the order status remains Open.</span></span>     
    * <span data-ttu-id="968cf-138">Siparişi satırlarının en az biri sevk edildiğinden Belge durumu alanını Sevk irsaliyesi şeklinde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="968cf-138">The Document status field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
17. <span data-ttu-id="968cf-139">Eylem Bölmesinde, Genel öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="968cf-139">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="968cf-140">Satırı miktarı'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="968cf-140">Click Line quantity.</span></span>
19. <span data-ttu-id="968cf-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="968cf-141">Close the page.</span></span>
20. <span data-ttu-id="968cf-142">Eylem Bölmesinde, Çek ve paketle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="968cf-142">On the Action Pane, click Pick and pack.</span></span>
21. <span data-ttu-id="968cf-143">Sevk irsaliyesi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="968cf-143">Click Packing slip.</span></span>
    * <span data-ttu-id="968cf-144">Sevk irsaliyesi günlüğü sayfası, siparişiniz için oluşturulan tüm sevk irsaliyesi belgelerini içerir.</span><span class="sxs-lookup"><span data-stu-id="968cf-144">The Packing slip journal page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="968cf-145">Her belgenin ayrıntılarını gözden geçirebilir ve isterseniz bunları yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="968cf-145">You can review details of each document and print them, if needed.</span></span>  


