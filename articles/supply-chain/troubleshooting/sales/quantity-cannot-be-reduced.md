---
title: Bir satış siparişi iptal edildiğinde miktar azaltılamaz
description: Bir satış siparişi iptal edildiğinde miktar azaltılamaz.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230848"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a><span data-ttu-id="a61b2-103">Bir satış siparişi iptal edildiğinde miktar azaltılamaz</span><span class="sxs-lookup"><span data-stu-id="a61b2-103">The quantity can't be reduced when a sales order is canceled</span></span>

<span data-ttu-id="a61b2-104">Hata kodu: SYS138831</span><span class="sxs-lookup"><span data-stu-id="a61b2-104">Error code: SYS138831</span></span>

## <a name="symptoms"></a><span data-ttu-id="a61b2-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="a61b2-105">Symptoms</span></span>

<span data-ttu-id="a61b2-106">Sistem, aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="a61b2-106">The system shows the following error message:</span></span>

> <span data-ttu-id="a61b2-107">Miktar azaltılamaz.</span><span class="sxs-lookup"><span data-stu-id="a61b2-107">The quantity cannot be reduced.</span></span> <span data-ttu-id="a61b2-108">Miktarı veya parçası bir çıkış siparişi veya üretim siparişi tarafından referans alındığından veya diğer hareketlere karşı işaretlendiğinden bir siparişteki stok hareketleri sayısı çok düşük.</span><span class="sxs-lookup"><span data-stu-id="a61b2-108">The number of inventory transactions on order is too low because the quantity or part of it is referenced by an output order or a production order or is marked against other transactions.</span></span>

## <a name="cause"></a><span data-ttu-id="a61b2-109">Nedeni</span><span class="sxs-lookup"><span data-stu-id="a61b2-109">Cause</span></span>

<span data-ttu-id="a61b2-110">İş bir satış siparişiyle ilişkilendirilmişse, iş iptal edilene ve ters çevrilinceye kadar satış siparişini iptal edemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="a61b2-110">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="a61b2-111">Bu gereksinim, satış siparişiyle ilişkilendirilmiş iş kapatılmış olsa bile geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="a61b2-111">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

## <a name="resolution"></a><span data-ttu-id="a61b2-112">Çözüm</span><span class="sxs-lookup"><span data-stu-id="a61b2-112">Resolution</span></span>

<span data-ttu-id="a61b2-113">Bu sorunu gidermek için aşağıdaki görevleri tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="a61b2-113">To fix this issue, complete the following tasks:</span></span>

1. <span data-ttu-id="a61b2-114">Açık çalışmayı iptal edin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-114">Cancel open work.</span></span>
1. <span data-ttu-id="a61b2-115">Yükü silin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-115">Delete the load.</span></span>
1. <span data-ttu-id="a61b2-116">Çekilen miktarı azaltın.</span><span class="sxs-lookup"><span data-stu-id="a61b2-116">Reduce the picked quantity.</span></span>

### <a name="cancel-open-work"></a><span data-ttu-id="a61b2-117">Açık çalışmayı iptal etme</span><span class="sxs-lookup"><span data-stu-id="a61b2-117">Cancel open work</span></span>

<span data-ttu-id="a61b2-118">Açık çalışmayı iptal etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-118">To cancel open work, follow these steps.</span></span>

1. <span data-ttu-id="a61b2-119">**Ambar yönetimi \> Periyodik görevler \> Temizleme \>Çalışmayı iptal et**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-119">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="a61b2-120">**Çalışma kodu** alanında, iptal etmek istediğiniz şu anda **Çalışma durumu** değeri *Açık*, *Devam ediyor*, *İptal edildi*, *Birleştirilmiş* veya *Kapalı* olan çalışmanın kodunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-120">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="a61b2-121">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-121">Select **OK**.</span></span>
1. <span data-ttu-id="a61b2-122">Çalışmayı iptal etmek istediğinizi onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-122">Select **Yes** to confirm that you want to cancel the work.</span></span>

### <a name="delete-the-load"></a><span data-ttu-id="a61b2-123">Yükü silme</span><span class="sxs-lookup"><span data-stu-id="a61b2-123">Delete the load</span></span>

<span data-ttu-id="a61b2-124">Yükü silmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-124">To delete a load, follow these steps.</span></span>

1. <span data-ttu-id="a61b2-125">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-125">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a61b2-126">İlgili satış siparişini açın.</span><span class="sxs-lookup"><span data-stu-id="a61b2-126">Open the relevant sales order.</span></span>
1. <span data-ttu-id="a61b2-127">**Satış siparişi satırları** hızlı sekmesinde **Ambar \> İş ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-127">On the **Sales order lines** FastTab, select **Warehouse \> Work details**.</span></span>
1. <span data-ttu-id="a61b2-128">**İş** sayfasında, Eylem Bölmesinde, **İş** sekmesinde, **İş** grubunda, **İşi iptal et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-128">On the **Work** page, on the Action Pane, on the **Work** tab, in the **Work** group, select **Cancel work**.</span></span>
1. <span data-ttu-id="a61b2-129">**İş durumu** alanının *İptal edildi* olarak ayarlandığını onaylayın.</span><span class="sxs-lookup"><span data-stu-id="a61b2-129">Confirm that the **Work status** field is set to *Canceled*.</span></span>
1. <span data-ttu-id="a61b2-130">**İş** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="a61b2-130">Close the **Work** page.</span></span>
1. <span data-ttu-id="a61b2-131">Satış siparişi ayrıntıları sayfasında, **Satış siparişi satırları** hızlı sekmesinde **Ambar \> Yük ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-131">On the sales order details page, on the **Sales order lines** FastTab, select **Warehouse \> Load details**.</span></span>
1. <span data-ttu-id="a61b2-132">Eylem Bölmesi'nde **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-132">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="a61b2-133">Yükü silmek istediğinizi onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-133">Select **Yes** to confirm that you want to delete the load.</span></span>
1. <span data-ttu-id="a61b2-134">**Yük** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="a61b2-134">Close the **Load** page.</span></span>

### <a name="reduce-the-picked-quantity"></a><span data-ttu-id="a61b2-135">Çekilen miktarı azaltma</span><span class="sxs-lookup"><span data-stu-id="a61b2-135">Reduce the picked quantity</span></span>

<span data-ttu-id="a61b2-136">Tüm işler iptal edildikten sonra çekilen miktarı azaltmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-136">After all work has been canceled, follow these steps to reduce the picked quantity.</span></span>

1. <span data-ttu-id="a61b2-137">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-137">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a61b2-138">İlgili satış siparişini açın.</span><span class="sxs-lookup"><span data-stu-id="a61b2-138">Open the relevant sales order.</span></span>
1. <span data-ttu-id="a61b2-139">**Satış siparişi satırları** hızlı sekmesinde, araç çubuğundan **Satırı güncelleştir \> Malzeme çek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-139">On the **Sales order lines** FastTab, select **Update line \> Pick** from the toolbar.</span></span>
1. <span data-ttu-id="a61b2-140">**Malzeme çekme** sayfasında, **Hareketler** bölümünde, **Çıkış durumu** alanının *Malzeme çekildi* olarak ayarlandığı satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-140">On the **Pick** page, in the **Transactions** section, select the line where the **Issue status** field is set to *Picked*.</span></span>
1. <span data-ttu-id="a61b2-141">**Hareketler** bölümünde, araç çubuğundan **Malzeme çekme satırı ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-141">In the **Transactions** section, select **Add picking line** from the toolbar.</span></span>
1. <span data-ttu-id="a61b2-142">**Malzeme çekme satırları** bölümünde, araç çubuğundan **Tümünü çekmeyi onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-142">In the **Picking lines** section, select **Confirm pick all** from the toolbar.</span></span>
1. <span data-ttu-id="a61b2-143">**Malzeme çekme** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="a61b2-143">Close the **Pick** page.</span></span>
1. <span data-ttu-id="a61b2-144">Satış siparişi ayrıntıları sayfasındaki Eylem Bölmesinde, **Satış siparişi** sekmesinde **Koruma** grubunda **İptal**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-144">On the sales order details page, on the Action Pane, on the **Sales order** tab, in the **Maintain** group, select **Cancel**.</span></span>
1. <span data-ttu-id="a61b2-145">Satış siparişini iptal etmek istediğinizi onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a61b2-145">Select **Yes** to confirm that you want to cancel the sales order.</span></span>
