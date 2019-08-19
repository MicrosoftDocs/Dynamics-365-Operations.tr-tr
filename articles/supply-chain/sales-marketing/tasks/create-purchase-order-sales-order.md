---
title: Satış siparişinden satınalma siparişi oluşturma
description: Bu yordam, bir satış siparişine göre nasıl satınalma siparişi oluşturulacağını gösterir.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5d7ce50532fb5bd6723b783d96d756085142e10
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843397"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="6b8d2-103">Satış siparişinden satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6b8d2-103">Create a purchase order from a sales order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b8d2-104">Bu yordam, bir satış siparişine göre nasıl satınalma siparişi oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-104">This procedure shows you how to create a purchase order that is based on a sales order.</span></span> <span data-ttu-id="6b8d2-105">Satınalma siparişindeki ürün miktarları kaynak satış siparişinin talebini karşılayacak şekilde belirlenir.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-105">The product's quantities on the purchase order are then designated to fulfill the demand of the originating sales order.</span></span> <span data-ttu-id="6b8d2-106">Satış talebinin bu şekilde karşılanması, daha kapsamlı ve iyi bir Dağıtım Gereksinimleri Planlaması yöntemi için alternatiftir.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-106">Fulfilling sales demand this way is an alternative to a more comprehensive and optimized method of Distribution Requirements Planning.</span></span> <span data-ttu-id="6b8d2-107">Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-107">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="6b8d2-108">Satış siparişinden satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6b8d2-108">Create a purchase order from a sales order</span></span>
1. <span data-ttu-id="6b8d2-109">Sales and marketing > Sales orders > All sales orders (Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="6b8d2-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-110">Click New.</span></span>
3. <span data-ttu-id="6b8d2-111">Müşteri hesabı alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6b8d2-112">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="6b8d2-113">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-113">Click OK.</span></span>
6. <span data-ttu-id="6b8d2-114">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="6b8d2-115">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6b8d2-116">USMF kullanıyorsanız, D0001 öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-116">If you're using USMF, you could select D0001.</span></span>  
8. <span data-ttu-id="6b8d2-117">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-117">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="6b8d2-118">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-118">Click Add line.</span></span>
10. <span data-ttu-id="6b8d2-119">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="6b8d2-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6b8d2-121">USMF kullanıyorsanız, T0020 öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-121">If you're using USMF, you could select T0020.</span></span>  
12. <span data-ttu-id="6b8d2-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-122">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="6b8d2-123">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-123">In the Quantity field, enter a number.</span></span>
14. <span data-ttu-id="6b8d2-124">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-124">Click Save.</span></span>
15. <span data-ttu-id="6b8d2-125">Eylem Bölmesinde, Satış siparişi öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-125">On the Action Pane, click Sales order.</span></span>
16. <span data-ttu-id="6b8d2-126">Satın alma siparişini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-126">Click Purchase order.</span></span>
    * <span data-ttu-id="6b8d2-127">Satınalma siparişi oluştur sayfası, satış siparişinden kopyalanmış tüm açık satış siparişi satırlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-127">The Create purchase order page lists all the open sales order lines which have been copied from the sales order.</span></span> <span data-ttu-id="6b8d2-128">Sipariş ayrıntılarını gözden geçirebilir ve gerekiyorsa satınalma oluşturmadan önce satınalma miktarı ve fiyatlandırma koşulları gibi seçilen ayrıntıları değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-128">You can review the order details, and if required, you can modify selected details such purchase quantity and pricing terms, before you create the purchases.</span></span>  
17. <span data-ttu-id="6b8d2-129">Tümünü dahil et seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-129">Select the Include all option.</span></span>
    * <span data-ttu-id="6b8d2-130">Satış siparişi satırlarının yalnızca bir alt kümesi için satınalma siparişleri oluşturmak istiyorsanız, bunları tek tek seçin.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-130">If you want to generate purchase orders for only a subset of the sales order lines, select these individually.</span></span>  
    * <span data-ttu-id="6b8d2-131">Satıcı hesabı alanı bir satıcı numarası ile önceden doldurulmuş olabilir.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-131">The Vendor account field may or may not already be populated with a vendor number.</span></span> <span data-ttu-id="6b8d2-132">Varsayılan satıcı ürün için (ilişkili ürün kapsamında) ayarlanmışsa, bu satıcı satıra kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-132">If the default vendor is set up for the product (on the associated Item coverage) then this vendor will be copied  to the line.</span></span> <span data-ttu-id="6b8d2-133">Aksi takdirde, manüel olarak bir satıcı girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-133">Otherwise, you must enter a vendor manually.</span></span>  <span data-ttu-id="6b8d2-134">Bu kılavuzda, Satıcı hesabı alanının önceden bir değer içerip içermediğine bakılmaksızın, aşağıdaki adımlar sizi her satır için farklı olan yeni bir satıcı seçmeniz için yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-134">In this guide, regardless of whether the Vendor account field already contains a value or not, the following steps instruct you to select a new vendor which is different for each line.</span></span>  
18. <span data-ttu-id="6b8d2-135">Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-135">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="6b8d2-136">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-136">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="6b8d2-137">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-137">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="6b8d2-138">İkincil sipariş satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-138">Select the second order line.</span></span>
22. <span data-ttu-id="6b8d2-139">Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-139">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="6b8d2-140">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-140">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="6b8d2-141">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-141">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="6b8d2-142">Doğrula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-142">Click Validate.</span></span>
26. <span data-ttu-id="6b8d2-143">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-143">Click OK.</span></span>
    * <span data-ttu-id="6b8d2-144">İleti, bir veya daha fazla satınalma siparişinin oluşturulduğunu bildirir.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-144">The message informs you that one or more purchase orders have been created.</span></span> <span data-ttu-id="6b8d2-145">Sistem, satış siparişi satırları için belirlenmiş her satıcıya ait ayrı bir satınalma siparişi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-145">The system generates a separate purchase order for each vendor that you specified for the sales order lines.</span></span> <span data-ttu-id="6b8d2-146">Başka bir deyişle, aynı satıcı tarafından birden fazla satış siparişi satırı sağlanırsa, birden fazla satıra sahip tek bir satınalma siparişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-146">This means that if several sales order lines are to be supplied by the same vendor, a single purchase order with multiple lines will be generated.</span></span>  

## <a name="review-purchase-orders-created-from-sales-orders"></a><span data-ttu-id="6b8d2-147">Satış siparişlerinden oluşturulan satınalma siparişlerini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-147">Review purchase orders created from sales orders</span></span>
1. <span data-ttu-id="6b8d2-148">Eylem Bölmesinde, Genel öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-148">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="6b8d2-149">İlgili siparişleri tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-149">Click Related orders.</span></span>
    * <span data-ttu-id="6b8d2-150">İlgili siparişler sayfası, satış siparişinden oluşturulan tüm siparişleri listeler.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-150">The Related orders page lists all the orders that were created from the sales order.</span></span> <span data-ttu-id="6b8d2-151">Bu örnekte, sırasıyla iki farklı satıcı için oluşturulan iki satınalma siparişi vardır.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-151">In this example, there are two purchase orders generated for two different vendors respectively.</span></span>  
3. <span data-ttu-id="6b8d2-152">Satınalma siparişi alanındaki bağlantıyı izlemek için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-152">Click to follow the link in the Purchase order field.</span></span>
    * <span data-ttu-id="6b8d2-153">Her satınalma siparişi satırı, satın almaya yol açan satış siparişi satırıyla ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-153">Each purchase order line is associated with the sales order line that led to the purchase.</span></span> <span data-ttu-id="6b8d2-154">Satış siparişinin ilişkisi Satır ayrıntıları FastTab'inde Ürün sekmesinde, Referans türü, Referans numarası ve Referans lotu alanlarında belirtilir.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-154">The relation to the sales order is indicated on the Product tab in the Line details FastTab, in the Reference type, Reference number, and Reference lot fields.</span></span>  
4. <span data-ttu-id="6b8d2-155">Satır ayrıntıları bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-155">Expand or collapse the Line details section.</span></span>
5. <span data-ttu-id="6b8d2-156">Ürün sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-156">Click the Product tab.</span></span>
    * <span data-ttu-id="6b8d2-157">Referans lotu, geçerli satınalmadan kaynaklanan maliyetlerin eklenmiş satış siparişine uygulanacağını garanti eder.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-157">The Reference lot guarantees that the costs from the current purchase are charged on the attached sales order.</span></span>  
    * <span data-ttu-id="6b8d2-158">Başvuru numarası alanındaki bağlantıyı açarak kaynak satış siparişine gidebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6b8d2-158">You can navigate to the originating sales order by opening the link in the Reference number field.</span></span>  

