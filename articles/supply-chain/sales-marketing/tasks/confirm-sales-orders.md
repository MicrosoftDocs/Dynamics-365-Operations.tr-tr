--- 
title: "Satış siparişlerini onaylama"
description: "Bu yordam, satış siparişlerinin nasıl onaylanacağını göstermektedir."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b60dbe15eca10511f4aaaf472b512eb003fbf6bc
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="confirm-sales-orders"></a><span data-ttu-id="a9fa0-103">Satış siparişlerini onaylama</span><span class="sxs-lookup"><span data-stu-id="a9fa0-103">Confirm sales orders</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a9fa0-104">Bu yordam, satış siparişlerinin nasıl onaylanacağını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="a9fa0-105">Tek bir siparişin ve aynı anda birden fazla siparişin nasıl onaylanacağı size gösterilecektir.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-105">You’ll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="a9fa0-106">Bu görevler genellikler satış siparişi işlemcisi tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="a9fa0-107">Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="a9fa0-108">Başlamadan önce aynı müşteri için birkaç açık satış siparişleri bulunduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="a9fa0-109">USMF kullanıyorsanız, US-027 müşterisini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-109">If you’re using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="a9fa0-110">Tek bir satış siparişini onaylayın</span><span class="sxs-lookup"><span data-stu-id="a9fa0-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="a9fa0-111">Sales and marketing > Sales orders > All sales orders (Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-111">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="a9fa0-112">Listede, onaylamak istediğiniz siparişi bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="a9fa0-113">Seçili siparişi açmak için satış siparişi numarasındaki bağlantıyı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="a9fa0-114">Eylem Bölmesinde, Satış'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-114">On the Action Pane, click Sell.</span></span>
5. <span data-ttu-id="a9fa0-115">Satış siparişini onayla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-115">Click Confirm sales order.</span></span>
6. <span data-ttu-id="a9fa0-116">Parametreler bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-116">Expand or collapse the Parameters section.</span></span>
    * <span data-ttu-id="a9fa0-117">Deftere naklet evet alanının etkin olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-117">Make sure that the Posting Yes field is active.</span></span>  
7. <span data-ttu-id="a9fa0-118">Onayı yazdır seçeneğini Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-118">Set the Print confirmation option to Yes.</span></span>
    * <span data-ttu-id="a9fa0-119">Kredi limitini denetle alanı, bir müşterinin kalan kredisini hesaplamak için kullanılan yöntemi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-119">The Check credit limit field specifies the method that’s used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="a9fa0-120">Varsayılan olarak alacak hesapları parametreleri sayfasından kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-120">By default, it’s copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="a9fa0-121">Kredi limiti denetimini belirli bir satış siparişini onaylarken atlamak istiyorsanız, kredi limitini denetle'yi Yok olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-121">If you want to skip the credit limit check when confirming a specific sales order, set the Check credit limit to None.</span></span> <span data-ttu-id="a9fa0-122">Fakat, bu alan Yok olarak bile ayarlanmış olsa, ana müşteri verilerinde Zorunlu kredi limiti seçeneği seçili ise, kredi limiti denetlemesinin yine de gerçekleşecek olacağını gözden kaçırmayın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-122">However, you should be aware that even with if this field is set to None, the credit limit check will still be performed if the Mandatory credit limit option is selected on the customer master data.</span></span>  
8. <span data-ttu-id="a9fa0-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-123">Click OK.</span></span>
9. <span data-ttu-id="a9fa0-124">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-124">Click Yes.</span></span>
10. <span data-ttu-id="a9fa0-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-125">Close the page.</span></span>
11. <span data-ttu-id="a9fa0-126">Eylem Bölmesinde, Seçenekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="a9fa0-127">Görünümü değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-127">Click Change view.</span></span>
13. <span data-ttu-id="a9fa0-128">Başlık görünümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-128">Click Header view.</span></span>
    * <span data-ttu-id="a9fa0-129">Bir siparişi teyit edildiğinde, Belge durumu, Onay olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-129">When an order is confirmed, the Document status is set to Confirmation.</span></span>  
14. <span data-ttu-id="a9fa0-130">Eylem Bölmesinde, Satış'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-130">On the Action Pane, click Sell.</span></span>
15. <span data-ttu-id="a9fa0-131">Satış siparişi onayını görüntüle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-131">Click Sales order confirmation.</span></span>
16. <span data-ttu-id="a9fa0-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="a9fa0-133">Aynı anda birden fazla satış siparişi onayla</span><span class="sxs-lookup"><span data-stu-id="a9fa0-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="a9fa0-134">Satış ve pazarlama > Satış siparişleri > Sipariş teyidi > Satış siparişi onayla seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-134">Go to Sales and marketing > Sales orders > Order confirmation > Confirm sales order.</span></span>
2. <span data-ttu-id="a9fa0-135">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-135">Click Select.</span></span>
3. <span data-ttu-id="a9fa0-136">Aralık sekmesindeki listede, müşteri hesabı alanına ilişkin kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-136">In the list on the Range tab, find and select the record that references the Customer account field.</span></span>
4. <span data-ttu-id="a9fa0-137">Ölçütler alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-137">In the Criteria field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a9fa0-138">Listede, bulmak ve toplu onaylamak istediğiniz birden fazla siparişi olan müşteri hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span>
    * <span data-ttu-id="a9fa0-139">USMF kullanıyorsanız, hesap US-027'yi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-139">If you’re using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="a9fa0-140">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-140">Click OK.</span></span>
    * <span data-ttu-id="a9fa0-141">Genel sekmesi, sorgu ölçütleriyle eşleşen siparişlerin bir listesini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-141">The Overview tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="a9fa0-142">Bunlar onaya dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-142">These will be included in the confirmation.</span></span>  
    * <span data-ttu-id="a9fa0-143">Alana ilişkin Özet güncelleştirme,birden çok sipariş onayının bir tek onay belgesine özetlenirken kullanılacak parametreyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-143">The Summary update for field specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="a9fa0-144">Bu seçenek varsayılan olarak, Alacak hesapları parametreleri sayfasındaki Özet güncelleştirme seçeneğinin varsayılan değerlerinden kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-144">By default, the option is copied from the Default values for summary update setting on the Accounts receivable parameters page.</span></span>  
7. <span data-ttu-id="a9fa0-145">Alana ilişkin Özet güncelleştirmede 'Sırala' seçin.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-145">In the Summary update for field, select 'Order'.</span></span>
    * <span data-ttu-id="a9fa0-146">Özet güncelleştirmeleri oluşturmak için gereken minimum parametreler Fatura hesabı ve Para birimidir.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-146">The minimum parameters that are required to create summary updates are Invoice account and Currency.</span></span> <span data-ttu-id="a9fa0-147">Başka bir deyişle, farklı fatura hesapları ve farklı para birimlerine sahip Özet güncelleştirmeleri verilmez.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="a9fa0-148">Ek parametreler, alacak hesapları parametreleri sayfasından erişilebilen Özet güncelleştirme parametreleri sayfasında ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-148">Additional parameters can be set up in the Summary update parameters page which is accessible from the Accounts receivable parameters page.</span></span>  
8. <span data-ttu-id="a9fa0-149">Satış siparişi alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-149">In the Sales order field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a9fa0-150">Listede, özet siparişe karşılık gelmesini istediğiniz bir sipariş numarası seçin.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="a9fa0-151">Yerleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-151">Click Arrange.</span></span>
11. <span data-ttu-id="a9fa0-152">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-152">Click OK.</span></span>
12. <span data-ttu-id="a9fa0-153">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-153">Click OK.</span></span>


