---
title: Satış siparişlerini onaylama
description: Bu yordam, satış siparişlerinin nasıl onaylanacağını göstermektedir.
author: omulvad
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup, SalesUnconfirmedOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f53fea1c1a998b5d3ec4669d772ace2561cb2cec
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252762"
---
# <a name="confirm-sales-orders"></a><span data-ttu-id="e3c38-103">Satış siparişlerini onaylama</span><span class="sxs-lookup"><span data-stu-id="e3c38-103">Confirm sales orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3c38-104">Bu yordam, satış siparişlerinin nasıl onaylanacağını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="e3c38-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="e3c38-105">Tek bir siparişin ve aynı anda birden fazla siparişin nasıl onaylanacağı size gösterilecektir.</span><span class="sxs-lookup"><span data-stu-id="e3c38-105">You'll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="e3c38-106">Bu görevler genellikler satış siparişi işlemcisi tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="e3c38-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="e3c38-107">Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e3c38-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="e3c38-108">Başlamadan önce aynı müşteri için birkaç açık satış siparişleri bulunduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="e3c38-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="e3c38-109">USMF kullanıyorsanız, US-027 müşterisini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e3c38-109">If you're using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="e3c38-110">Tek bir satış siparişini onaylayın</span><span class="sxs-lookup"><span data-stu-id="e3c38-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="e3c38-111">**Gezinti bölmesi > Modüller > Satış ve pazarlama > Satış siperişler > Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e3c38-111">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="e3c38-112">Listede, onaylamak istediğiniz siparişi bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e3c38-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="e3c38-113">Seçili siparişi açmak için satış siparişi numarasındaki bağlantıyı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="e3c38-114">**Eylem bölmesi**'nde, **Satış**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-114">On the **Action Pane**, click **Sell**.</span></span>
5. <span data-ttu-id="e3c38-115">**Satış siparişini onayla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-115">Click **Confirm sales order**.</span></span>
6. <span data-ttu-id="e3c38-116">**Parametreler** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="e3c38-116">Expand the **Parameters** section.</span></span> <span data-ttu-id="e3c38-117">**Deftere nakil** seçeneğinin 'Evet' olarak ayarlanmış olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="e3c38-117">Make sure that the **Posting** option is set to 'Yes'.</span></span>  
7. <span data-ttu-id="e3c38-118">**Onayı yazdır seçeneğini** 'Evet' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-118">Set the **Print confirmation option** to 'Yes'.</span></span> <span data-ttu-id="e3c38-119">**Kredi limitini denetle** alanı, bir müşterinin kalan kredisini hesaplamak için kullanılan yöntemi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3c38-119">The **Check credit limit** field specifies the method that's used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="e3c38-120">Varsayılan olarak alacak hesapları parametreleri sayfasından kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="e3c38-120">By default, it's copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="e3c38-121">Kredi limiti denetimini belirli bir satış siparişini onaylarken atlamak istiyorsanız, **kredi limitini denetle**'yi 'Yok' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-121">If you want to skip the credit limit check when confirming a specific sales order, set the **Check credit limit** to 'None'.</span></span> <span data-ttu-id="e3c38-122">Fakat, bu alan 'Yok' olarak bile ayarlanmış olsa, ana müşteri verilerinde **Zorunlu kredi limiti** seçeneği seçili ise, kredi limiti denetlemesinin yine de gerçekleşecek olacağını gözden kaçırmayın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-122">However, you should be aware that even with if this field is set to 'None', the credit limit check will still be performed if the **Mandatory credit limit** option is selected on the customer master data.</span></span> 
8. <span data-ttu-id="e3c38-123">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-123">Click **OK**.</span></span>
9. <span data-ttu-id="e3c38-124">**Evet** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-124">Click **Yes**.</span></span>
10. <span data-ttu-id="e3c38-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-125">Close the page.</span></span>
11. <span data-ttu-id="e3c38-126">**Eylem Bölmesinde**, **Seçenekler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-126">On the **Action Pane**, click **Options**.</span></span>
12. <span data-ttu-id="e3c38-127">**Görünümü değiştir** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-127">Click **Change view**.</span></span>
13. <span data-ttu-id="e3c38-128">**Başlık görünümü** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-128">Click **Header view**.</span></span> <span data-ttu-id="e3c38-129">Bir siparişi teyit edildiğinde, **Belge durumu**, 'Onay' olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="e3c38-129">When an order is confirmed, the **Document status** is set to 'Confirmation'.</span></span> 
14. <span data-ttu-id="e3c38-130">**Eylem bölmesi**'nde, **Satış**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-130">On the **Action Pane**, click **Sell**.</span></span>
15. <span data-ttu-id="e3c38-131">**Satış siparişi onayı**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-131">Click **Sales order confirmation**.</span></span>
16. <span data-ttu-id="e3c38-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="e3c38-133">Aynı anda birden fazla satış siparişi onayla</span><span class="sxs-lookup"><span data-stu-id="e3c38-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="e3c38-134">**Satış ve pazarlama > Satış siparişleri > Sipariş teyidi > Satış siparişini onayla** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="e3c38-134">Go to **Sales and marketing > Sales orders > Order confirmation > Confirm sales order**.</span></span>
2. <span data-ttu-id="e3c38-135">**Seç**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-135">Click **Select**.</span></span>
3. <span data-ttu-id="e3c38-136">**Aralık** sekmesindeki listede, **Müşteri hesabı** alanına başvuran kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e3c38-136">In the list on the **Range** tab, find and select the record that references the **Customer account** field.</span></span>
4. <span data-ttu-id="e3c38-137">**Ölçütler** alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-137">In the **Criteria** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e3c38-138">Listede, bulmak ve toplu onaylamak istediğiniz birden fazla siparişi olan müşteri hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="e3c38-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span> <span data-ttu-id="e3c38-139">USMF kullanıyorsanız, hesap US-027'yi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e3c38-139">If you're using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="e3c38-140">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-140">Click **OK**.</span></span>
    - <span data-ttu-id="e3c38-141">**Genel** sekmesi, sorgu ölçütleriyle eşleşen siparişlerin bir listesini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="e3c38-141">The **Overview** tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="e3c38-142">Bunlar onaya dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="e3c38-142">These will be included in the confirmation.</span></span>  
    - <span data-ttu-id="e3c38-143">**Parametreler** bölümünün **Özet güncelleştirmesi** alanı birden çok sipariş onayı bir tek onay belgesine özetlenirken kullanılacak parametreyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3c38-143">The **Summary update for** field in the **Parameters** section specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="e3c38-144">Bu seçenek varsayılan olarak, **Alacak hesapları parametreleri** sayfasındaki **Özet güncelleştirme ayarının varsayılan değerlerinden** kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="e3c38-144">By default, the option is copied from the D **efault values for summary update setting** on the **Accounts receivable parameters** page.</span></span>  
7. <span data-ttu-id="e3c38-145">**Özet güncelleştirme** alanında 'Sipariş'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e3c38-145">In the **Summary update for** field, select 'Order'.</span></span> <span data-ttu-id="e3c38-146">Özet güncelleştirmeleri oluşturmak için gereken minimum parametreler **Fatura hesabı** ve **Para birimi**'dir.</span><span class="sxs-lookup"><span data-stu-id="e3c38-146">The minimum parameters that are required to create summary updates are **Invoice account** and **Currency**.</span></span> <span data-ttu-id="e3c38-147">Başka bir deyişle, farklı fatura hesapları ve farklı para birimlerine sahip Özet güncelleştirmeleri verilmez.</span><span class="sxs-lookup"><span data-stu-id="e3c38-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="e3c38-148">Ek parametreler, **Alacak hesapları parametreleri** sayfasından erişilebilen **Özet güncelleştirme parametreleri** sayfasında ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="e3c38-148">Additional parameters can be set up in the **Summary update parameters** page which is accessible from the **Accounts receivable parameters** page.</span></span> 
8. <span data-ttu-id="e3c38-149">**Satış siparişi** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-149">In the **Sales order** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="e3c38-150">Listede, özet siparişe karşılık gelmesini istediğiniz bir sipariş numarası seçin.</span><span class="sxs-lookup"><span data-stu-id="e3c38-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="e3c38-151">**Düzenle**'ye tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-151">Click **Arrange**.</span></span>
11. <span data-ttu-id="e3c38-152">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-152">Click **OK**.</span></span>
12. <span data-ttu-id="e3c38-153">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3c38-153">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]