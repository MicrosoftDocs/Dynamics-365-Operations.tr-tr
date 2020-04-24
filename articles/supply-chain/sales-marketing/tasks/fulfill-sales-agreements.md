---
title: Satış sözleşmelerini karşılama
description: Bu yordam, bir satış anlaşmasının satış siparişleri ile ilişkilendirerek nasıl yerine getirileceğini gösterir.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51ea8afc7c2f683790f697185d6637e0d24462fc
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204321"
---
# <a name="fulfill-sales-agreements"></a><span data-ttu-id="36207-103">Satış sözleşmelerini karşılama</span><span class="sxs-lookup"><span data-stu-id="36207-103">Fulfill sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="36207-104">Bu yordam, bir satış anlaşmasının satış siparişleri ile ilişkilendirerek nasıl yerine getirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="36207-104">This procedure shows you how to fulfill a sales agreement by associating sales orders with it.</span></span> <span data-ttu-id="36207-105">Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="36207-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="36207-106">Bu kılavuzu başlatmadan önce, "Ürün değeri taahhüdü" türünde etkin bir satış anlaşmanız olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="36207-106">Before starting this guide, make sure you have an effective sales agreement of type "Product value commitment".</span></span> <span data-ttu-id="36207-107">Alternatif olarak, "Satış anlaşmaları oluşturma" adı verilen görev kılavuzunu çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="36207-107">Alternatively, you can run the task guide called "Create sales agreements".</span></span>  




## <a name="release-a-sales-order-from-the-agreement"></a><span data-ttu-id="36207-108">Anlaşmadaki bir satış siparişini sevk etme</span><span class="sxs-lookup"><span data-stu-id="36207-108">Release a sales order from the agreement</span></span>
1. <span data-ttu-id="36207-109">Sales and marketing > Sales agreements > Sales agreements (Satış ve pazarlama > Satış anlaşmaları > Satış anlaşmaları) menüsüne gidin</span><span class="sxs-lookup"><span data-stu-id="36207-109">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="36207-110">Listede, siparişini sevk etmek istediğiniz anlaşmayı açın.</span><span class="sxs-lookup"><span data-stu-id="36207-110">In the list, open the agreement against which you want to release the order.</span></span>
3. <span data-ttu-id="36207-111">Eylem Bölmesinde, Satış anlaşması'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36207-111">On the Action Pane, click Sales agreement.</span></span>
4. <span data-ttu-id="36207-112">Sevk emri'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36207-112">Click Release order.</span></span>
    * <span data-ttu-id="36207-113">Sevk emrini oluştur sayfasının üstündeki metinde gösterildiği üzere, satış siparişi satırları için gerekli ayrıntılar anlaşmanın miktar mı yoksa değer esaslı mı olduğuna bağlı olarak farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="36207-113">As the text on top of the  Create release order page points out, the details required for the sales order lines will differ depending on whether the agreement is quantity- or value-based.</span></span>  
    * <span data-ttu-id="36207-114">Bu kılavuzdaki anlaşma "Ürün değeri taahhüdü" türündedir.</span><span class="sxs-lookup"><span data-stu-id="36207-114">The agreement in this guide is of type "Product value commitment".</span></span> <span data-ttu-id="36207-115">Bu nedenle, bu sayfanın Satırlar bölümü boştur.</span><span class="sxs-lookup"><span data-stu-id="36207-115">This is why the Lines section of this page is blank.</span></span> <span data-ttu-id="36207-116">Taahhüt miktarı esas alıyorsa, satır bilgilerinin sözleşmeden kopyalanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="36207-116">If the commitment was based on quantity, the line information would be copied from the agreement.</span></span>  
5. <span data-ttu-id="36207-117">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36207-117">Click Create.</span></span>
    * <span data-ttu-id="36207-118">İleti, bir satış siparişinin oluşturulduğunu bildirir.</span><span class="sxs-lookup"><span data-stu-id="36207-118">The message informs you that a sales order has been created.</span></span> <span data-ttu-id="36207-119">Sipariş hiçbir satır içermediğinden, serbest bırakma işlemini tamamlamak için sipariş satırı ayrıntılarını eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="36207-119">Since the order does not contain any lines, you must add order line details to complete the release process.</span></span>   
6. <span data-ttu-id="36207-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="36207-120">Close the page.</span></span>
7. <span data-ttu-id="36207-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="36207-121">Close the page.</span></span>
8. <span data-ttu-id="36207-122">Sales and marketing > Sales orders > All sales orders (Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="36207-122">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
9. <span data-ttu-id="36207-123">Listede, önceki görevde sevk edilen siparişin sonucunda oluşturulan siparişi bulun ve açın.</span><span class="sxs-lookup"><span data-stu-id="36207-123">In the list, find and open the order that was created as the result of the order release in the previous task.</span></span>
10. <span data-ttu-id="36207-124">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36207-124">Click Add line.</span></span>
11. <span data-ttu-id="36207-125">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="36207-125">In the Item number field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="36207-126">Ürün numarası alanında, ilişkili satış anlaşmasında belirtilen ürünü bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="36207-126">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
13. <span data-ttu-id="36207-127">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="36207-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="36207-128">İlişkili satış anlaşmasının değeri altındaki Net tutarı getiren bir miktar girdiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="36207-128">Make sure that you enter a quantity that brings the Net amount under the value of the associated sales agreement.</span></span>  
    * <span data-ttu-id="36207-129">Satış siparişi anlaşmaya bağlı olduğundan, üzerinde anlaşılan iskonto yüzdesinin sipariş satırına uygulanacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="36207-129">Notice that because the sales order is linked to the agreement, the negotiated discount percent is applied to the order line.</span></span>  
14. <span data-ttu-id="36207-130">Satırı güncelleştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36207-130">Click Update line.</span></span>
15. <span data-ttu-id="36207-131">İlişik öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36207-131">Click Attached.</span></span>
    * <span data-ttu-id="36207-132">İlişik anlaşma sayfası, satırın serbest bırakıldığı anlaşmanın kodunu ve şartlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="36207-132">The Attached agreement page shows the ID and terms of the agreement from which the line is released.</span></span>  
16. <span data-ttu-id="36207-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="36207-133">Close the page.</span></span>
17. <span data-ttu-id="36207-134">Eylem Bölmesinde, Genel öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36207-134">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="36207-135">İlişik satış anlaşması'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36207-135">Click Attached sales agreement.</span></span>
19. <span data-ttu-id="36207-136">Satır ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="36207-136">Expand the Line details section.</span></span>
20. <span data-ttu-id="36207-137">Karşılama sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36207-137">Click the Fulfillment tab.</span></span>
    * <span data-ttu-id="36207-138">Karşılama sekmesi, bu taahhüt ile ilişkilendirilmiş tüm satış siparişlerinin bir özetinin ve karşılama durumlarının yanı sıra henüz sevk edilmemiş tutarı veya miktarı gösterir.</span><span class="sxs-lookup"><span data-stu-id="36207-138">The Fulfillment tab shows a summary of all the sales order lines that are associated with this commitment, and their fulfillment state, as well as the amount or quantity that has not yet been released.</span></span>   
21. <span data-ttu-id="36207-139">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="36207-139">Close the page.</span></span>
22. <span data-ttu-id="36207-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="36207-140">Close the page.</span></span>
23. <span data-ttu-id="36207-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="36207-141">Close the page.</span></span>

## <a name="apply-sales-agreement-in-the-order-process"></a><span data-ttu-id="36207-142">Sipariş işleminde satış anlaşmasını uygulama</span><span class="sxs-lookup"><span data-stu-id="36207-142">Apply sales agreement in the order process</span></span>
1. <span data-ttu-id="36207-143">Sales and marketing > Sales orders > All sales orders (Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="36207-143">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="36207-144">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36207-144">Click New.</span></span>
3. <span data-ttu-id="36207-145">Müşteri hesabı alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36207-145">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="36207-146">Listede, satış anlaşmasında belirtilen müşteriyi bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="36207-146">In the list, find and select the customer specified on the sales agreement.</span></span>
5. <span data-ttu-id="36207-147">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36207-147">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="36207-148">Genel bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="36207-148">Expand the General section.</span></span>
7. <span data-ttu-id="36207-149">Satış anlaşması kodu alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36207-149">In the Sales agreement ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="36207-150">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36207-150">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="36207-151">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36207-151">Click Yes.</span></span>
10. <span data-ttu-id="36207-152">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36207-152">Click OK.</span></span>
11. <span data-ttu-id="36207-153">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="36207-153">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="36207-154">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="36207-154">In the Item number field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="36207-155">Ürün numarası alanında, ilişkili satış anlaşmasında belirtilen ürünü bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="36207-155">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
14. <span data-ttu-id="36207-156">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36207-156">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="36207-157">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36207-157">Click Save.</span></span>
16. <span data-ttu-id="36207-158">Eylem Bölmesinde, Çek ve paketle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36207-158">On the Action Pane, click Pick and pack.</span></span>
17. <span data-ttu-id="36207-159">Sevk irsaliyesini deftere naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36207-159">Click Post packing slip.</span></span>
18. <span data-ttu-id="36207-160">Parametreler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="36207-160">Expand the Parameters section.</span></span>
19. <span data-ttu-id="36207-161">Deftere nakil alanında 'Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="36207-161">Select Yes in the Posting field.</span></span>
20. <span data-ttu-id="36207-162">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36207-162">Click OK.</span></span>
21. <span data-ttu-id="36207-163">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36207-163">Click OK.</span></span>
22. <span data-ttu-id="36207-164">Eylem Bölmesinde, Genel öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36207-164">On the Action Pane, click General.</span></span>
23. <span data-ttu-id="36207-165">İlişik satış anlaşması'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36207-165">Click Attached sales agreement.</span></span>
24. <span data-ttu-id="36207-166">Karşılama sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36207-166">Click the Fulfillment tab.</span></span>

